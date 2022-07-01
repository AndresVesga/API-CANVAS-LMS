# API-CANVAS-LMS
Connection to CANVAS LMS by Power BI

# M Lenguage
# Documentation: https://canvas.instructure.com/doc/api/

(course as text) => 

let
    Origen = Json.Document(Web.Contents("https://umb.instructure.com",    
    [RelativePath= "/api/v1/courses/" &(course)] &
    [Headers = [Authorization= "Bearer <ApiKey>"]]))
in    
    Origen
    
 
