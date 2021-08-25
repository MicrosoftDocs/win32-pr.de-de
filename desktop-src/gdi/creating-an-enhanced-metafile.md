---
description: Dieser Abschnitt enthält ein Beispiel, das die Erstellung einer erweiterten Metadatei veranschaulicht, die auf einem Datenträger gespeichert ist, indem ein vom Benutzer angegebener Dateiname verwendet wird.
ms.assetid: 084b2737-eb55-4587-b8e8-3eb3fa3688c4
title: Erstellen einer erweiterten Metadatei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e53266ac0677da211308c7028f4d61869fc2890f27c06daeff9cfb6fea87e58
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119849230"
---
# <a name="creating-an-enhanced-metafile"></a>Erstellen einer erweiterten Metadatei

Dieser Abschnitt enthält ein Beispiel, das die Erstellung einer erweiterten Metadatei veranschaulicht, die auf einem Datenträger gespeichert ist, indem ein vom Benutzer angegebener Dateiname verwendet wird.

Im Beispiel wird ein Gerätekontext für das Anwendungsfenster als Referenzgerätekontext verwendet. (Das System speichert die Auflösungsdaten für dieses Gerät im Header der erweiterten Metadatei.) Die Anwendung ruft ein Handle ab, das diesen Gerätekontext identifiziert, indem die [**GetDC-Funktion**](/windows/desktop/api/Winuser/nf-winuser-getdc) aufgerufen wird.

Im Beispiel werden die Dimensionen des Clientbereichs der Anwendung verwendet, um die Dimensionen des Bildrahmens zu definieren. Mithilfe der rechteckigen Dimensionen, die von der [**GetClientRect-Funktion**](/windows/win32/api/winuser/nf-winuser-getclientrect) zurückgegeben werden, konvertiert die Anwendung die Geräteeinheiten in Einheiten mit 0,01 Mm und übergibt die konvertierten Werte an die [**CreateEnhMetaFile-Funktion.**](/windows/desktop/api/Wingdi/nf-wingdi-createenhmetafilea)

Im Beispiel wird ein allgemeines Dialogfeld **Speichern unter** angezeigt, in dem der Benutzer den Dateinamen der neuen erweiterten Metadatei angeben kann. Das System fügt die emf-Erweiterung mit drei Zeichen an diesen Dateinamen an und übergibt den Namen an die [**CreateEnhMetaFile-Funktion.**](/windows/desktop/api/Wingdi/nf-wingdi-createenhmetafilea)

Im Beispiel wird auch eine Textbeschreibung des Bilds in den Enhanced-Metafile-Header eingebettet. Diese Beschreibung wird als Ressource in der Zeichenfolgentabelle der Ressourcendatei der Anwendung angegeben. In einer funktionierenden Anwendung wird diese Zeichenfolge jedoch aus einem benutzerdefinierten Steuerelement in einem allgemeinen Dialogfeld oder aus einem separaten Dialogfeld abgerufen, das ausschließlich zu diesem Zweck angezeigt wird.


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



 

 
