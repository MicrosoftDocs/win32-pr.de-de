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
# <a name="creating-an-enhanced-metafile"></a><span data-ttu-id="09be0-103">Erstellen einer erweiterten Metadatei</span><span class="sxs-lookup"><span data-stu-id="09be0-103">Creating an Enhanced Metafile</span></span>

<span data-ttu-id="09be0-104">Dieser Abschnitt enthält ein Beispiel, das die Erstellung einer erweiterten Metadatei veranschaulicht, die auf einem Datenträger gespeichert ist. dabei wird der vom Benutzer angegebene Dateiname verwendet.</span><span class="sxs-lookup"><span data-stu-id="09be0-104">This section contains an example that demonstrates the creation of an enhanced metafile that is stored on a disk, using a file name specified by the user.</span></span>

<span data-ttu-id="09be0-105">Das Beispiel verwendet einen Gerätekontext für das Anwendungsfenster als Verweis Gerätekontext.</span><span class="sxs-lookup"><span data-stu-id="09be0-105">The example uses a device context for the application window as the reference device context.</span></span> <span data-ttu-id="09be0-106">(Das System speichert die Auflösungs Daten für dieses Gerät im Header der erweiterten Metadatei.) Die Anwendung ruft ein Handle ab, das diesen Gerätekontext durch Aufrufen der [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) -Funktion identifiziert.</span><span class="sxs-lookup"><span data-stu-id="09be0-106">(The system stores the resolution data for this device in the enhanced-metafile's header.) The application retrieves a handle identifying this device context by calling the [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) function.</span></span>

<span data-ttu-id="09be0-107">Im Beispiel werden die Dimensionen des-Client Bereichs der Anwendung verwendet, um die Dimensionen des Bild Rahmens zu definieren.</span><span class="sxs-lookup"><span data-stu-id="09be0-107">The example uses the dimensions of the application's client area to define the dimensions of the picture frame.</span></span> <span data-ttu-id="09be0-108">Mithilfe der von der [**GetClientRect**](/windows/win32/api/winuser/nf-winuser-getclientrect) -Funktion zurückgegebenen Rechteck Dimensionen konvertiert die Anwendung die Geräte Einheiten in 01-Millimeter-Einheiten und übergibt die konvertierten Werte an [**die Funktion "**](/windows/desktop/api/Wingdi/nf-wingdi-createenhmetafilea) -Funktion".</span><span class="sxs-lookup"><span data-stu-id="09be0-108">Using the rectangle dimensions returned by the [**GetClientRect**](/windows/win32/api/winuser/nf-winuser-getclientrect) function, the application converts the device units to .01-millimeter units and passes the converted values to the [**CreateEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-createenhmetafilea) function.</span></span>

<span data-ttu-id="09be0-109">Das Beispiel zeigt das Dialogfeld **als allgemein speichern** an, in dem der Benutzer den Dateinamen der neuen erweiterten Metadatei angeben kann.</span><span class="sxs-lookup"><span data-stu-id="09be0-109">The example displays a **Save As** common dialog box that enables the user to specify the file name of the new enhanced metafile.</span></span> <span data-ttu-id="09be0-110">Das System fügt die Erweiterung mit drei Zeichen. EMF an diesen Dateinamen an und [**übergibt den Namen an die Funktion "**](/windows/desktop/api/Wingdi/nf-wingdi-createenhmetafilea) -Funktion".</span><span class="sxs-lookup"><span data-stu-id="09be0-110">The system appends the three-character .emf extension to this file name and passes the name to the [**CreateEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-createenhmetafilea) function.</span></span>

<span data-ttu-id="09be0-111">Das Beispiel bettet außerdem eine Textbeschreibung des Bilds in den Enhanced-Metafile-Header ein.</span><span class="sxs-lookup"><span data-stu-id="09be0-111">The example also embeds a text description of the picture in the enhanced-metafile header.</span></span> <span data-ttu-id="09be0-112">Diese Beschreibung wird als Ressource in der Zeichen folgen Tabelle der Ressourcen Datei der Anwendung angegeben.</span><span class="sxs-lookup"><span data-stu-id="09be0-112">This description is specified as a resource in the string table of the application's resource file.</span></span> <span data-ttu-id="09be0-113">In einer funktionierenden Anwendung würde diese Zeichenfolge jedoch aus einem benutzerdefinierten Steuerelement in einem gemeinsamen Dialogfeld oder in einem separaten Dialogfeld, das ausschließlich für diesen Zweck angezeigt wird, abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="09be0-113">However, in a working application, this string would be retrieved from a custom control in a common dialog box or from a separate dialog box displayed solely for this purpose.</span></span>


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



 

 
