---
title: Verwenden von Symbolen
description: Dieser Abschnitt enthält Codebeispiele, die zeigen, wie Aufgaben im Zusammenhang mit Symbolen ausgeführt werden.
ms.assetid: 5021d59a-7aae-4ddc-be66-9abdc75ad316
keywords:
- Ressourcen, Symbole
- Symbole,Erstellen
- Symbole, anzeigen
- Symbole, Freigeben von Ressourcen
- Erstellen von Symbolen
- Anzeigen von Symbolen
- Freigeben von Symbolressourcen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03202c250502794d5f845bcc8c2ae263d919ea62
ms.sourcegitcommit: dc2f43e0f23f4a4ce239118cf9a5180f3ff0dd1d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/30/2021
ms.locfileid: "108327115"
---
# <a name="using-icons"></a><span data-ttu-id="03a0e-110">Verwenden von Symbolen</span><span class="sxs-lookup"><span data-stu-id="03a0e-110">Using Icons</span></span>

<span data-ttu-id="03a0e-111">In den folgenden Themen wird beschrieben, wie bestimmte Aufgaben im Zusammenhang mit Symbolen ausgeführt werden:</span><span class="sxs-lookup"><span data-stu-id="03a0e-111">The following topics describe how to perform certain tasks related to icons:</span></span>

-   [<span data-ttu-id="03a0e-112">Erstellen eines Symbols</span><span class="sxs-lookup"><span data-stu-id="03a0e-112">Creating an Icon</span></span>](#creating-an-icon)
-   [<span data-ttu-id="03a0e-113">Anzeigen eines Symbols</span><span class="sxs-lookup"><span data-stu-id="03a0e-113">Displaying an Icon</span></span>](#displaying-an-icon)
-   [<span data-ttu-id="03a0e-114">Freigabesymbolressourcen</span><span class="sxs-lookup"><span data-stu-id="03a0e-114">Sharing Icon Resources</span></span>](#sharing-icon-resources)

## <a name="creating-an-icon"></a><span data-ttu-id="03a0e-115">Erstellen eines Symbols</span><span class="sxs-lookup"><span data-stu-id="03a0e-115">Creating an Icon</span></span>

<span data-ttu-id="03a0e-116">Um ein Symbol zu verwenden, muss Ihre Anwendung ein Handle für das Symbol abrufen.</span><span class="sxs-lookup"><span data-stu-id="03a0e-116">To use an icon, your application must get a handle to the icon.</span></span> <span data-ttu-id="03a0e-117">Das folgende Beispiel zeigt, wie sie zwei verschiedene Symbolhandles erstellen: einen für das Standardfragesymbol und einen für ein benutzerdefiniertes Symbol, das als Ressource in der Ressourcendefinitionsdatei der Anwendung enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="03a0e-117">The following example shows how to create two different icon handles: one for the standard question icon and one for a custom icon included as a resource in the application's resource-definition file.</span></span>


```
HICON hIcon1;   // icon handle 
HICON hIcon2;   // icon handle 
 
// Create a standard question icon. 
 
hIcon1 = LoadIcon(NULL, IDI_QUESTION); 
 
// Create a custom icon based on a resource. 
 
hIcon2 = LoadIcon(hinst, MAKEINTRESOURCE(460)); 
 
// Create a custom icon at run time.
 
```



<span data-ttu-id="03a0e-118">Eine Anwendung sollte benutzerdefinierte Symbole als Ressourcen implementieren und die [**LoadIcon-**](/windows/desktop/api/Winuser/nf-winuser-loadicona) oder [**LoadImage-Funktion**](/windows/desktop/api/Winuser/nf-winuser-loadimagea) verwenden, anstatt die Symbole zur Laufzeit zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="03a0e-118">An application should implement custom icons as resources and should use the [**LoadIcon**](/windows/desktop/api/Winuser/nf-winuser-loadicona) or [**LoadImage**](/windows/desktop/api/Winuser/nf-winuser-loadimagea) function, rather than create the icons at run-time.</span></span> <span data-ttu-id="03a0e-119">Dieser Ansatz vermeidet Geräteabhängigkeiten, vereinfacht die Lokalisierung und ermöglicht Anwendungen das Freigeben von Symbolbitmaps.</span><span class="sxs-lookup"><span data-stu-id="03a0e-119">This approach avoids device dependence, simplifies localization, and enables applications to share icon bitmaps.</span></span> <span data-ttu-id="03a0e-120">Im folgenden Beispiel wird jedoch [**CreateIcon**](/windows/desktop/api/Winuser/nf-winuser-createicon) verwendet, um zur Laufzeit ein benutzerdefiniertes Symbol basierend auf Bitmapbitmasken zu erstellen. es ist enthalten, um zu veranschaulichen, wie das System Symbolbitmap-Bitmasken interpretiert.</span><span class="sxs-lookup"><span data-stu-id="03a0e-120">However, the following example uses [**CreateIcon**](/windows/desktop/api/Winuser/nf-winuser-createicon) to create a custom icon at run-time, based on bitmap bitmasks; it is included to illustrate how the system interprets icon bitmap bitmasks.</span></span>


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



<span data-ttu-id="03a0e-121">Um das Symbol zu erstellen, wendet [**CreateIcon**](/windows/desktop/api/Winuser/nf-winuser-createicon) die folgende Wahrheitstabelle auf die AND- und XOR-Bitmasken an.</span><span class="sxs-lookup"><span data-stu-id="03a0e-121">To create the icon, [**CreateIcon**](/windows/desktop/api/Winuser/nf-winuser-createicon) applies the following truth table to the AND and XOR bitmasks.</span></span>



| <span data-ttu-id="03a0e-122">AND-Bitmaske</span><span class="sxs-lookup"><span data-stu-id="03a0e-122">AND bitmask</span></span> | <span data-ttu-id="03a0e-123">XOR-Bitmaske</span><span class="sxs-lookup"><span data-stu-id="03a0e-123">XOR bitmask</span></span> | <span data-ttu-id="03a0e-124">Anzeige</span><span class="sxs-lookup"><span data-stu-id="03a0e-124">Display</span></span>        |
|-------------|-------------|----------------|
| <span data-ttu-id="03a0e-125">0</span><span class="sxs-lookup"><span data-stu-id="03a0e-125">0</span></span>           | <span data-ttu-id="03a0e-126">0</span><span class="sxs-lookup"><span data-stu-id="03a0e-126">0</span></span>           | <span data-ttu-id="03a0e-127">Schwarz</span><span class="sxs-lookup"><span data-stu-id="03a0e-127">Black</span></span>          |
| <span data-ttu-id="03a0e-128">0</span><span class="sxs-lookup"><span data-stu-id="03a0e-128">0</span></span>           | <span data-ttu-id="03a0e-129">1</span><span class="sxs-lookup"><span data-stu-id="03a0e-129">1</span></span>           | <span data-ttu-id="03a0e-130">White</span><span class="sxs-lookup"><span data-stu-id="03a0e-130">White</span></span>          |
| <span data-ttu-id="03a0e-131">1</span><span class="sxs-lookup"><span data-stu-id="03a0e-131">1</span></span>           | <span data-ttu-id="03a0e-132">0</span><span class="sxs-lookup"><span data-stu-id="03a0e-132">0</span></span>           | <span data-ttu-id="03a0e-133">Screen</span><span class="sxs-lookup"><span data-stu-id="03a0e-133">Screen</span></span>         |
| <span data-ttu-id="03a0e-134">1</span><span class="sxs-lookup"><span data-stu-id="03a0e-134">1</span></span>           | <span data-ttu-id="03a0e-135">1</span><span class="sxs-lookup"><span data-stu-id="03a0e-135">1</span></span>           | <span data-ttu-id="03a0e-136">Reversebildschirm</span><span class="sxs-lookup"><span data-stu-id="03a0e-136">Reverse screen</span></span> |



 

<span data-ttu-id="03a0e-137">Vor dem Schließen muss Ihre Anwendung [**DestroyIcon**](/windows/desktop/api/Winuser/nf-winuser-destroyicon) verwenden, um alle Symbole zu zerstören, die sie mit [**createIconIndirect erstellt hat.**](/windows/desktop/api/Winuser/nf-winuser-createiconindirect)</span><span class="sxs-lookup"><span data-stu-id="03a0e-137">Before closing, your application must use [**DestroyIcon**](/windows/desktop/api/Winuser/nf-winuser-destroyicon) to destroy any icon it created by using [**CreateIconIndirect**](/windows/desktop/api/Winuser/nf-winuser-createiconindirect).</span></span> <span data-ttu-id="03a0e-138">Es ist nicht erforderlich, Symbole zu zerstören, die von anderen Funktionen erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="03a0e-138">It is not necessary to destroy icons created by other functions.</span></span>

## <a name="displaying-an-icon"></a><span data-ttu-id="03a0e-139">Anzeigen eines Symbols</span><span class="sxs-lookup"><span data-stu-id="03a0e-139">Displaying an Icon</span></span>

<span data-ttu-id="03a0e-140">Ihre Anwendung kann Symbole laden und erstellen, die im Clientbereich oder in untergeordneten Fenstern der Anwendung angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="03a0e-140">Your application can load and create icons to display in the application's client area or child windows.</span></span> <span data-ttu-id="03a0e-141">Im folgenden Beispiel wird veranschaulicht, wie sie ein Symbol im Clientbereich des Fensters zeichnen, dessen Gerätekontext (DC) durch den *hdc-Parameter identifiziert* wird.</span><span class="sxs-lookup"><span data-stu-id="03a0e-141">The following example demonstrates how to draw an icon in the client area of the window whose device context (DC) is identified by the *hdc* parameter.</span></span>


```
HICON hIcon1;   // icon handle  
HDC hdc;        // handle to display context 
 
DrawIcon(hdc, 10, 20, hIcon1); 
```



<span data-ttu-id="03a0e-142">Das System zeigt automatisch die Klassensymbole für ein Fenster an.</span><span class="sxs-lookup"><span data-stu-id="03a0e-142">The system automatically displays the class icon(s) for a window.</span></span> <span data-ttu-id="03a0e-143">Ihre Anwendung kann Klassensymbole beim Registrieren einer Fensterklasse zuweisen.</span><span class="sxs-lookup"><span data-stu-id="03a0e-143">Your application can assign class icons while registering a window class.</span></span> <span data-ttu-id="03a0e-144">Ihre Anwendung kann ein Klassensymbol mithilfe der [**SetClassLong-Funktion**](/windows/desktop/api/winuser/nf-winuser-setclasslonga) ersetzen.</span><span class="sxs-lookup"><span data-stu-id="03a0e-144">Your application can replace a class icon by using the [**SetClassLong**](/windows/desktop/api/winuser/nf-winuser-setclasslonga) function.</span></span> <span data-ttu-id="03a0e-145">Diese Funktion ändert die Standardfenstereinstellungen für alle Fenster einer bestimmten Klasse.</span><span class="sxs-lookup"><span data-stu-id="03a0e-145">This function changes the default window settings for all windows of a given class.</span></span> <span data-ttu-id="03a0e-146">Im folgenden Beispiel wird ein Klassensymbol durch das Symbol ersetzt, dessen Ressourcenbezeichner 480 ist.</span><span class="sxs-lookup"><span data-stu-id="03a0e-146">The following example replaces a class icon with the icon whose resource identifier is 480.</span></span>


```
HINSTANCE hinst;            // handle to current instance 
HWND hwnd;                  // main window handle  
 
// Change the icon for hwnd's window class. 
 
SetClassLongPtr(hwnd,          // window handle 
    GCLP_HICON,              // changes icon 
    (LONG_PTR) LoadIcon(hinst, MAKEINTRESOURCE(480))
   ); 
```



<span data-ttu-id="03a0e-147">Weitere Informationen zu Fensterklassen finden Sie unter [Fensterklassen.](/windows/desktop/winmsg/window-classes)</span><span class="sxs-lookup"><span data-stu-id="03a0e-147">For more information about window classes, see [Window Classes](/windows/desktop/winmsg/window-classes).</span></span>

## <a name="sharing-icon-resources"></a><span data-ttu-id="03a0e-148">Ressourcen des Freigabesymbols</span><span class="sxs-lookup"><span data-stu-id="03a0e-148">Sharing Icon Resources</span></span>

<span data-ttu-id="03a0e-149">Der folgende Code verwendet die Funktionen [**CreateIconFromResourceEx,**](/windows/desktop/api/Winuser/nf-winuser-createiconfromresourceex) [**DrawIcon**](/windows/desktop/api/Winuser/nf-winuser-drawicon)und [**LookupIconIdFromDirectoryEx**](/windows/desktop/api/Winuser/nf-winuser-lookupiconidfromdirectoryex)sowie einige der Ressourcenfunktionen, um ein Symbolhandle basierend auf Symboldaten aus einer anderen ausführbaren Datei zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="03a0e-149">The following code uses the functions [**CreateIconFromResourceEx**](/windows/desktop/api/Winuser/nf-winuser-createiconfromresourceex), [**DrawIcon**](/windows/desktop/api/Winuser/nf-winuser-drawicon), and [**LookupIconIdFromDirectoryEx**](/windows/desktop/api/Winuser/nf-winuser-lookupiconidfromdirectoryex), and several of the resource functions, to create an icon handle based on icon data from another executable file.</span></span> <span data-ttu-id="03a0e-150">Anschließend wird das Symbol in einem Fenster angezeigt.</span><span class="sxs-lookup"><span data-stu-id="03a0e-150">Then, it displays the icon in a window.</span></span>

<span data-ttu-id="03a0e-151">**Sicherheitswarnung:** Die [**falsche Verwendung von LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) kann die Sicherheit Ihrer Anwendung gefährden, indem die falsche DLL geladen wird.</span><span class="sxs-lookup"><span data-stu-id="03a0e-151">**Security Warning:** Using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) incorrectly can compromise the security of your application by loading the wrong DLL.</span></span> <span data-ttu-id="03a0e-152">Informationen zum ordnungsgemäßen Laden von DLLs mit verschiedenen Versionen von Windows finden Sie in der **LoadLibrary-Dokumentation.**</span><span class="sxs-lookup"><span data-stu-id="03a0e-152">Refer to the **LoadLibrary** documentation for information on how to correctly load DLLs with different versions of Windows.</span></span>


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



 

 
