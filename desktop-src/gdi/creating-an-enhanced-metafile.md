---
description: Dieser Abschnitt enthält ein Beispiel, das die Erstellung einer erweiterten Metadatei veranschaulicht, die auf einem Datenträger gespeichert ist. dabei wird der vom Benutzer angegebene Dateiname verwendet.
ms.assetid: 084b2737-eb55-4587-b8e8-3eb3fa3688c4
title: Erstellen einer erweiterten Metadatei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4877481ed0a68d6379e7eaabb00bbe37cef74c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528385"
---
# <a name="creating-an-enhanced-metafile"></a>Erstellen einer erweiterten Metadatei

Dieser Abschnitt enthält ein Beispiel, das die Erstellung einer erweiterten Metadatei veranschaulicht, die auf einem Datenträger gespeichert ist. dabei wird der vom Benutzer angegebene Dateiname verwendet.

Das Beispiel verwendet einen Gerätekontext für das Anwendungsfenster als Verweis Gerätekontext. (Das System speichert die Auflösungs Daten für dieses Gerät im Header der erweiterten Metadatei.) Die Anwendung ruft ein Handle ab, das diesen Gerätekontext durch Aufrufen der [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) -Funktion identifiziert.

Im Beispiel werden die Dimensionen des-Client Bereichs der Anwendung verwendet, um die Dimensionen des Bild Rahmens zu definieren. Mithilfe der von der [**GetClientRect**](/windows/win32/api/winuser/nf-winuser-getclientrect) -Funktion zurückgegebenen Rechteck Dimensionen konvertiert die Anwendung die Geräte Einheiten in 01-Millimeter-Einheiten und übergibt die konvertierten Werte an [**die Funktion "**](/windows/desktop/api/Wingdi/nf-wingdi-createenhmetafilea) -Funktion".

Das Beispiel zeigt das Dialogfeld **als allgemein speichern** an, in dem der Benutzer den Dateinamen der neuen erweiterten Metadatei angeben kann. Das System fügt die Erweiterung mit drei Zeichen. EMF an diesen Dateinamen an und [**übergibt den Namen an die Funktion "**](/windows/desktop/api/Wingdi/nf-wingdi-createenhmetafilea) -Funktion".

Das Beispiel bettet außerdem eine Textbeschreibung des Bilds in den Enhanced-Metafile-Header ein. Diese Beschreibung wird als Ressource in der Zeichen folgen Tabelle der Ressourcen Datei der Anwendung angegeben. In einer funktionierenden Anwendung würde diese Zeichenfolge jedoch aus einem benutzerdefinierten Steuerelement in einem gemeinsamen Dialogfeld oder in einem separaten Dialogfeld, das ausschließlich für diesen Zweck angezeigt wird, abgerufen werden.


```C++
// Obtain a handle to a reference device context.  
 
hdcRef = GetDC(hWnd); 
 
// Determine the picture frame dimensions.  
// iWidthMM is the display width in millimeters.  
// iHeightMM is the display height in millimeters.  
// iWidthPels is the display width in pixels.  
// iHeightPels is the display height in pixels  
 
iWidthMM = GetDeviceCaps(hdcRef, HORZSIZE); 
iHeightMM = GetDeviceCaps(hdcRef, VERTSIZE); 
iWidthPels = GetDeviceCaps(hdcRef, HORZRES); 
iHeightPels = GetDeviceCaps(hdcRef, VERTRES); 
 
// Retrieve the coordinates of the client  
// rectangle, in pixels.  
 
GetClientRect(hWnd, &rect); 
 
// Convert client coordinates to .01-mm units.  
// Use iWidthMM, iWidthPels, iHeightMM, and  
// iHeightPels to determine the number of  
// .01-millimeter units per pixel in the x-  
//  and y-directions.  
 
rect.left = (rect.left * iWidthMM * 100)/iWidthPels; 
rect.top = (rect.top * iHeightMM * 100)/iHeightPels; 
rect.right = (rect.right * iWidthMM * 100)/iWidthPels; 
rect.bottom = (rect.bottom * iHeightMM * 100)/iHeightPels; 
 
// Load the filename filter from the string table.  
 
LoadString(hInst, IDS_FILTERSTRING, 
     (LPSTR)szFilter, sizeof(szFilter)); 
 
// Replace the '%' separators that are embedded  
// between the strings in the string-table entry  
// with '\0'.  
 
for (i=0; szFilter[i]!='\0'; i++) 
    if (szFilter[i] == '%') 
            szFilter[i] = '\0'; 
 
// Load the dialog title string from the table.  
 
LoadString(hInst, IDS_TITLESTRING, 
     (LPSTR)szTitle, sizeof(szTitle)); 
 
// Initialize the OPENFILENAME members.  
 
szFile[0] = '\0'; 
 
Ofn.lStructSize = sizeof(OPENFILENAME); 
Ofn.hwndOwner = hWnd; 
Ofn.lpstrFilter = szFilter; 
Ofn.lpstrFile= szFile; 
Ofn.nMaxFile = sizeof(szFile)/ sizeof(*szFile); 
Ofn.lpstrFileTitle = szFileTitle; 
Ofn.nMaxFileTitle = sizeof(szFileTitle); 
Ofn.lpstrInitialDir = (LPSTR)NULL; 
Ofn.Flags = OFN_SHOWHELP | OFN_OVERWRITEPROMPT; 
Ofn.lpstrTitle = szTitle; 
 
// Display the Filename common dialog box. The  
// filename specified by the user is passed  
// to the CreateEnhMetaFile function and used to  
// store the metafile on disk.  
 
GetSaveFileName(&Ofn); 
 
// Load the description from the string table.  
 
LoadString(hInst, IDS_DESCRIPTIONSTRING, 
     (LPSTR)szDescription, sizeof(szDescription)); 
 
// Replace the '%' string separators that are  
// embedded between strings in the string-table  
// entry with '\0'.  
 
for (i=0; szDescription[i]!='\0'; i++) 
{
    if (szDescription[i] == '%') 
            szDescription[i] = '\0'; 
}
 
// Create the metafile device context.  
 
hdcMeta = CreateEnhMetaFile(hdcRef, 
          (LPTSTR) Ofn.lpstrFile, 
          &rect, (LPSTR)szDescription); 
 
if (!hdcMeta) 
    errhandler("CreateEnhMetaFile", hWnd); 
 
// Release the reference device context.  
 
ReleaseDC(hWnd, hdcRef); 
```



 

 
