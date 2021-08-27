---
title: Verwenden von Symbolen
description: Dieser Abschnitt enthält Codebeispiele, die zeigen, wie Sie Aufgaben im Zusammenhang mit Symbolen ausführen.
ms.assetid: 5021d59a-7aae-4ddc-be66-9abdc75ad316
keywords:
- Ressourcen,Symbole
- Symbole,erstellen
- Symbole,anzeigen
- Symbole,Gemeinsame Nutzung von Ressourcen
- Erstellen von Symbolen
- Anzeigen von Symbolen
- Ressourcen des Freigabesymbols
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40db7a5828c80dc27780ac54e4110e37a80f44938c9475904ce32089be50d84f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118472598"
---
# <a name="using-icons"></a>Verwenden von Symbolen

In den folgenden Themen wird beschrieben, wie sie bestimmte Aufgaben im Zusammenhang mit Symbolen ausführen:

-   [Erstellen eines Symbols](#creating-an-icon)
-   [Anzeigen eines Symbols](#displaying-an-icon)
-   [Ressourcen des Freigabesymbols](#sharing-icon-resources)

## <a name="creating-an-icon"></a>Erstellen eines Symbols

Um ein Symbol zu verwenden, muss Ihre Anwendung ein Handle für das Symbol erhalten. Das folgende Beispiel zeigt, wie sie zwei verschiedene Symbolhandles erstellen: einen für das Standardfragesymbol und einen für ein benutzerdefiniertes Symbol, das als Ressource in der Ressourcendefinitionsdatei der Anwendung enthalten ist.


```
HICON hIcon1;   // icon handle 
HICON hIcon2;   // icon handle 
 
// Create a standard question icon. 
 
hIcon1 = LoadIcon(NULL, IDI_QUESTION); 
 
// Create a custom icon based on a resource. 
 
hIcon2 = LoadIcon(hinst, MAKEINTRESOURCE(460)); 
 
// Create a custom icon at run time.
 
```



Eine Anwendung sollte benutzerdefinierte Symbole als Ressourcen implementieren und die [**LoadIcon-**](/windows/desktop/api/Winuser/nf-winuser-loadicona) oder [**LoadImage-Funktion**](/windows/desktop/api/Winuser/nf-winuser-loadimagea) verwenden, anstatt die Symbole zur Laufzeit zu erstellen. Dieser Ansatz vermeidet Geräteabhängigkeit, vereinfacht die Lokalisierung und ermöglicht Es Anwendungen, Symbolbitmaps gemeinsam zu nutzen. Im folgenden Beispiel wird jedoch [**CreateIcon**](/windows/desktop/api/Winuser/nf-winuser-createicon) verwendet, um zur Laufzeit ein benutzerdefiniertes Symbol basierend auf Bitmapbitmasken zu erstellen. es ist enthalten, um zu veranschaulichen, wie das System Symbolbitmapbitmasken interpretiert.


```
HICON hIcon3;      // icon handle 
 
// Yang icon AND bitmask 
 
BYTE ANDmaskIcon[] = {0xFF, 0xFF, 0xFF, 0xFF,   // line 1 
                      0xFF, 0xFF, 0xC3, 0xFF,   // line 2 
                      0xFF, 0xFF, 0x00, 0xFF,   // line 3 
                      0xFF, 0xFE, 0x00, 0x7F,   // line 4 
 
                      0xFF, 0xFC, 0x00, 0x1F,   // line 5 
                      0xFF, 0xF8, 0x00, 0x0F,   // line 6 
                      0xFF, 0xF8, 0x00, 0x0F,   // line 7 
                      0xFF, 0xF0, 0x00, 0x07,   // line 8 
 
                      0xFF, 0xF0, 0x00, 0x03,   // line 9 
                      0xFF, 0xE0, 0x00, 0x03,   // line 10 
                      0xFF, 0xE0, 0x00, 0x01,   // line 11 
                      0xFF, 0xE0, 0x00, 0x01,   // line 12 
 
                      0xFF, 0xF0, 0x00, 0x01,   // line 13 
                      0xFF, 0xF0, 0x00, 0x00,   // line 14 
                      0xFF, 0xF8, 0x00, 0x00,   // line 15 
                      0xFF, 0xFC, 0x00, 0x00,   // line 16 
 
                      0xFF, 0xFF, 0x00, 0x00,   // line 17 
                      0xFF, 0xFF, 0x80, 0x00,   // line 18 
                      0xFF, 0xFF, 0xE0, 0x00,   // line 19 
                      0xFF, 0xFF, 0xE0, 0x01,   // line 20 
 
                      0xFF, 0xFF, 0xF0, 0x01,   // line 21 
                      0xFF, 0xFF, 0xF0, 0x01,   // line 22 
                      0xFF, 0xFF, 0xF0, 0x03,   // line 23 
                      0xFF, 0xFF, 0xE0, 0x03,   // line 24 
 
                      0xFF, 0xFF, 0xE0, 0x07,   // line 25 
                      0xFF, 0xFF, 0xC0, 0x0F,   // line 26 
                      0xFF, 0xFF, 0xC0, 0x0F,   // line 27 
                      0xFF, 0xFF, 0x80, 0x1F,   // line 28 
 
                      0xFF, 0xFF, 0x00, 0x7F,   // line 29 
                      0xFF, 0xFC, 0x00, 0xFF,   // line 30 
                      0xFF, 0xF8, 0x03, 0xFF,   // line 31 
                      0xFF, 0xFC, 0x3F, 0xFF};  // line 32 
 
// Yang icon XOR bitmask 
 
BYTE XORmaskIcon[] = {0x00, 0x00, 0x00, 0x00,   // line 1 
                      0x00, 0x00, 0x00, 0x00,   // line 2 
                      0x00, 0x00, 0x00, 0x00,   // line 3 
                      0x00, 0x00, 0x00, 0x00,   // line 4 
 
                      0x00, 0x00, 0x00, 0x00,   // line 5 
                      0x00, 0x00, 0x00, 0x00,   // line 6 
                      0x00, 0x00, 0x00, 0x00,   // line 7 
                      0x00, 0x00, 0x38, 0x00,   // line 8 
 
                      0x00, 0x00, 0x7C, 0x00,   // line 9 
                      0x00, 0x00, 0x7C, 0x00,   // line 10 
                      0x00, 0x00, 0x7C, 0x00,   // line 11 
                      0x00, 0x00, 0x38, 0x00,   // line 12 
 
                      0x00, 0x00, 0x00, 0x00,   // line 13 
                      0x00, 0x00, 0x00, 0x00,   // line 14 
                      0x00, 0x00, 0x00, 0x00,   // line 15 
                      0x00, 0x00, 0x00, 0x00,   // line 16 
 
                      0x00, 0x00, 0x00, 0x00,   // line 17 
                      0x00, 0x00, 0x00, 0x00,   // line 18 
                      0x00, 0x00, 0x00, 0x00,   // line 19 
                      0x00, 0x00, 0x00, 0x00,   // line 20 
 
                      0x00, 0x00, 0x00, 0x00,   // line 21 
                      0x00, 0x00, 0x00, 0x00,   // line 22 
                      0x00, 0x00, 0x00, 0x00,   // line 23 
                      0x00, 0x00, 0x00, 0x00,   // line 24 
 
                      0x00, 0x00, 0x00, 0x00,   // line 25 
                      0x00, 0x00, 0x00, 0x00,   // line 26 
                      0x00, 0x00, 0x00, 0x00,   // line 27 
                      0x00, 0x00, 0x00, 0x00,   // line 28 
 
                      0x00, 0x00, 0x00, 0x00,   // line 29 
                      0x00, 0x00, 0x00, 0x00,   // line 30 
                      0x00, 0x00, 0x00, 0x00,   // line 31 
                      0x00, 0x00, 0x00, 0x00};  // line 32 
 
hIcon3 = CreateIcon(hinst,    // application instance  
             32,              // icon width 
             32,              // icon height 
             1,               // number of XOR planes 
             1,               // number of bits per pixel 
             ANDmaskIcon,     // AND bitmask  
             XORmaskIcon);    // XOR bitmask 
              
```



Zum Erstellen des Symbols wendet [**CreateIcon**](/windows/desktop/api/Winuser/nf-winuser-createicon) die folgende Wahrheitstabelle auf die AND- und XOR-Bitmasken an.



| AND-Bitmaske | XOR-Bitmaske | Anzeige        |
|-------------|-------------|----------------|
| 0           | 0           | Schwarz          |
| 0           | 1           | White          |
| 1           | 0           | Screen         |
| 1           | 1           | Reversebildschirm |



 

Vor dem Schließen muss Ihre Anwendung [**DestroyIcon**](/windows/desktop/api/Winuser/nf-winuser-destroyicon) verwenden, um alle Symbole zu zerstören, die sie mit [**createIconIndirect erstellt hat.**](/windows/desktop/api/Winuser/nf-winuser-createiconindirect) Es ist nicht erforderlich, Symbole zu zerstören, die von anderen Funktionen erstellt wurden.

## <a name="displaying-an-icon"></a>Anzeigen eines Symbols

Ihre Anwendung kann Symbole laden und erstellen, die im Clientbereich oder in untergeordneten Fenstern der Anwendung angezeigt werden. Im folgenden Beispiel wird veranschaulicht, wie sie ein Symbol im Clientbereich des Fensters zeichnen, dessen Gerätekontext (DC) durch den *hdc-Parameter identifiziert* wird.


```
HICON hIcon1;   // icon handle  
HDC hdc;        // handle to display context 
 
DrawIcon(hdc, 10, 20, hIcon1); 
```



Das System zeigt automatisch die Klassensymbole für ein Fenster an. Ihre Anwendung kann Klassensymbole beim Registrieren einer Fensterklasse zuweisen. Ihre Anwendung kann ein Klassensymbol mithilfe der [**SetClassLong-Funktion**](/windows/desktop/api/winuser/nf-winuser-setclasslonga) ersetzen. Diese Funktion ändert die Standardfenstereinstellungen für alle Fenster einer bestimmten Klasse. Im folgenden Beispiel wird ein Klassensymbol durch das Symbol ersetzt, dessen Ressourcenbezeichner 480 ist.


```
HINSTANCE hinst;            // handle to current instance 
HWND hwnd;                  // main window handle  
 
// Change the icon for hwnd's window class. 
 
SetClassLongPtr(hwnd,          // window handle 
    GCLP_HICON,              // changes icon 
    (LONG_PTR) LoadIcon(hinst, MAKEINTRESOURCE(480))
   ); 
```



Weitere Informationen zu Fensterklassen finden Sie unter [Fensterklassen.](/windows/desktop/winmsg/window-classes)

## <a name="sharing-icon-resources"></a>Ressourcen des Freigabesymbols

Der folgende Code verwendet die Funktionen [**CreateIconFromResourceEx,**](/windows/desktop/api/Winuser/nf-winuser-createiconfromresourceex) [**DrawIcon**](/windows/desktop/api/Winuser/nf-winuser-drawicon)und [**LookupIconIdFromDirectoryEx**](/windows/desktop/api/Winuser/nf-winuser-lookupiconidfromdirectoryex)sowie einige der Ressourcenfunktionen, um ein Symbolhandle basierend auf Symboldaten aus einer anderen ausführbaren Datei zu erstellen. Anschließend wird das Symbol in einem Fenster angezeigt.

**Sicherheitswarnung:** Die [**falsche Verwendung von LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) kann die Sicherheit Ihrer Anwendung gefährden, indem die falsche DLL geladen wird. In der **LoadLibrary-Dokumentation** finden Sie Informationen zum ordnungsgemäßen Laden von DLLs mit verschiedenen Versionen Windows.


```
HICON hIcon1;       // icon handle 
HINSTANCE hExe;     // handle to loaded .EXE file 
HRSRC hResource;    // handle to FindResource  
HRSRC hMem;         // handle to LoadResource 
BYTE *lpResource;   // pointer to resource data  
int nID;            // ID of resource that best fits current screen 
 
HDC hdc;        // handle to display context 
 
// Load the file from which to copy the icon. 
// Note: LoadLibrary should have a fully explicit path.
//
hExe = LoadLibrary("myapp.exe");
if (hExe == NULL)
{
    //Error loading module -- fail as securely as possible
    return;
}
 
 
// Find the icon directory whose identifier is 440. 
 
hResource = FindResource(hExe, 
    MAKEINTRESOURCE(440), 
    RT_GROUP_ICON); 
 
// Load and lock the icon directory. 
 
hMem = LoadResource(hExe, hResource); 
 
lpResource = LockResource(hMem); 
 
// Get the identifier of the icon that is most appropriate 
// for the video display. 
 
nID = LookupIconIdFromDirectoryEx((PBYTE) lpResource, TRUE, 
    CXICON, CYICON, LR_DEFAULTCOLOR); 
 
// Find the bits for the nID icon. 
 
hResource = FindResource(hExe, 
    MAKEINTRESOURCE(nID), 
    MAKEINTRESOURCE(RT_ICON)); 
 
// Load and lock the icon. 
 
hMem = LoadResource(hExe, hResource); 
 
lpResource = LockResource(hMem); 
 
// Create a handle to the icon. 
 
hIcon1 = CreateIconFromResourceEx((PBYTE) lpResource, 
    SizeofResource(hExe, hResource), TRUE, 0x00030000, 
    CXICON, CYICON, LR_DEFAULTCOLOR); 
 
// Draw the icon in the client area. 
 
DrawIcon(hdc, 10, 20, hIcon1); 
```



 

 
