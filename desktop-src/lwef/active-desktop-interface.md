---
title: Verwenden des aktiven Desktop Objekts
description: Dieser Artikel enthält Informationen zum activedesktop-Objekt, das Teil der Windows-Shell-API ist. Mit diesem Objekt können Sie über die iactivedesktop-Schnittstelle Elemente auf dem Desktop hinzufügen, entfernen und ändern.
ms.assetid: 68d72b0f-f5e9-4fff-bb13-4c60d1dd7009
keywords:
- Activedesktop-Objekt
- Aktiver Desktop
- Enumeration, Desktop Elemente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7e61a4a9145386fc4c84a454aa79558b8d5df79
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104472805"
---
# <a name="using-the-active-desktop-object"></a><span data-ttu-id="c66dd-107">Verwenden des aktiven Desktop Objekts</span><span class="sxs-lookup"><span data-stu-id="c66dd-107">Using the Active Desktop Object</span></span>

<span data-ttu-id="c66dd-108">\[Dieses Feature wird nur unter Windows XP oder früher unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c66dd-108">\[This feature is supported only under Windows XP or earlier.</span></span> <span data-ttu-id="c66dd-109">\]</span><span class="sxs-lookup"><span data-stu-id="c66dd-109">\]</span></span>

<span data-ttu-id="c66dd-110">Dieser Artikel enthält Informationen zum **activedesktop-** Objekt, das Teil der Windows-Shell-API ist.</span><span class="sxs-lookup"><span data-stu-id="c66dd-110">This article contains information on the **ActiveDesktop** object that is part of the Windows Shell API.</span></span> <span data-ttu-id="c66dd-111">Mit diesem Objekt können Sie über die [**iactivedesktop**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop) -Schnittstelle Elemente auf dem Desktop hinzufügen, entfernen und ändern.</span><span class="sxs-lookup"><span data-stu-id="c66dd-111">This object, through its [**IActiveDesktop**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop) interface, enables you to add, remove, and change items on the desktop.</span></span>

## <a name="overview-of-the-active-desktop-interface"></a><span data-ttu-id="c66dd-112">Übersicht über die aktive Desktop Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="c66dd-112">Overview of the Active Desktop Interface</span></span>

-   [<span data-ttu-id="c66dd-113">Zugreifen auf den aktiven Desktop</span><span class="sxs-lookup"><span data-stu-id="c66dd-113">Accessing the Active Desktop</span></span>](#accessing-the-active-desktop)
-   [<span data-ttu-id="c66dd-114">Hinzufügen eines Desktop Elements</span><span class="sxs-lookup"><span data-stu-id="c66dd-114">Adding a Desktop Item</span></span>](#adding-a-desktop-item)
-   [<span data-ttu-id="c66dd-115">Auflisten der Desktop Elemente</span><span class="sxs-lookup"><span data-stu-id="c66dd-115">Enumerating the Desktop Items</span></span>](#enumerating-the-desktop-items)

<span data-ttu-id="c66dd-116">Der aktive Desktop ist eine in Microsoft Internet Explorer 4,0 eingeführte Funktion, mit der Sie HTML-Dokumente und-Elemente (z. b. Microsoft ActiveX-Steuerelemente und Java-Applets) direkt auf Ihren Desktop einbinden können.</span><span class="sxs-lookup"><span data-stu-id="c66dd-116">The Active Desktop is a feature introduced with Microsoft Internet Explorer 4.0 that enables you to include HTML documents and items (such as Microsoft ActiveX Controls and Java applets) directly to your desktop.</span></span> <span data-ttu-id="c66dd-117">Die [**iactivedesktop-**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop) Schnittstelle, die Teil der Windows-Shell-API ist, wird verwendet, um die Elemente auf dem Desktop Programm gesteuert hinzuzufügen, zu entfernen und zu ändern.</span><span class="sxs-lookup"><span data-stu-id="c66dd-117">The [**IActiveDesktop**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop) interface, which is part of the Windows Shell API, is used to programmatically add, remove, and modify the items on the desktop.</span></span> <span data-ttu-id="c66dd-118">Aktive Desktop Elemente können auch mithilfe einer CDF-Datei (Channel Definition Format) hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="c66dd-118">Active Desktop items can also be added using a Channel Definition Format (CDF) file.</span></span>

### <a name="accessing-the-active-desktop"></a><span data-ttu-id="c66dd-119">Zugreifen auf den aktiven Desktop</span><span class="sxs-lookup"><span data-stu-id="c66dd-119">Accessing the Active Desktop</span></span>

<span data-ttu-id="c66dd-120">Um auf den aktiven Desktop zuzugreifen, muss eine Client Anwendung eine Instanz des activedesktop-Objekts (CLSID \_ activedesktop) mit der [cokreateinstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) -Funktion erstellen und einen Zeiger auf die [**iactivedesktop**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop) -Schnittstelle des Objekts abrufen.</span><span class="sxs-lookup"><span data-stu-id="c66dd-120">To access the Active Desktop, a client application would need to create an instance of the ActiveDesktop object (CLSID\_ActiveDesktop) with the [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) function and retrieve a pointer to the object's [**IActiveDesktop**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop) interface.</span></span>

<span data-ttu-id="c66dd-121">Im folgenden Beispiel wird gezeigt, wie ein Zeiger auf die [**iactivedesktop-**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop) Schnittstelle abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="c66dd-121">The following sample shows how to retrieve a pointer to the [**IActiveDesktop**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop) interface.</span></span>


```
HRESULT hr;
IActiveDesktop *pActiveDesktop;

//Create an instance of the Active Desktop
hr = CoCreateInstance(CLSID_ActiveDesktop, NULL, CLSCTX_INPROC_SERVER,
                      IID_IActiveDesktop, (void**)&pActiveDesktop);

//Insert code to call the IActiveDesktop methods

// Call the Release method
pActiveDesktop->Release();
```



### <a name="adding-a-desktop-item"></a><span data-ttu-id="c66dd-122">Hinzufügen eines Desktop Elements</span><span class="sxs-lookup"><span data-stu-id="c66dd-122">Adding a Desktop Item</span></span>

<span data-ttu-id="c66dd-123">Es gibt drei Methoden, mit denen Sie ein Desktop Element hinzufügen können: [**iactivedesktop:: adddesktopitem**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitem), [**iactivedesktop:: adddesktopitemwithui**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitemwithui)und [**iactivedesktop:: addurl**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-addurl).</span><span class="sxs-lookup"><span data-stu-id="c66dd-123">There are three methods you can use to add a desktop item: [**IActiveDesktop::AddDesktopItem**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitem), [**IActiveDesktop::AddDesktopItemWithUI**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitemwithui), and [**IActiveDesktop::AddUrl**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-addurl).</span></span> <span data-ttu-id="c66dd-124">Jedes Desktop Element, das dem aktiven Desktop hinzugefügt wird, muss über eine andere Quell-URL verfügen.</span><span class="sxs-lookup"><span data-stu-id="c66dd-124">Each desktop item added to the Active Desktop must have a different source URL.</span></span>

<span data-ttu-id="c66dd-125">Mit der [**iactivedesktop:: adddesktopitemwithui**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitemwithui) -Methode und der [**iactivedesktop:: addurl**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-addurl) -Methode können die verschiedenen Benutzeroberflächen angezeigt werden, die angezeigt werden können, bevor dem aktiven Desktop ein Desktop Element hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="c66dd-125">The [**IActiveDesktop::AddDesktopItemWithUI**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitemwithui) and [**IActiveDesktop::AddUrl**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-addurl) methods both provide the option to display the various user interfaces that can be displayed before adding a desktop item to the Active Desktop.</span></span> <span data-ttu-id="c66dd-126">Überprüfen Sie, ob Benutzer das Desktop Element dem aktiven Desktop hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="c66dd-126">The interfaces verify whether users want to add the desktop item to their Active Desktop.</span></span> <span data-ttu-id="c66dd-127">Die Schnittstellen Benachrichtigen auch Benutzer über etwaige Sicherheitsrisiken, die durch die Einstellungen der URL-Sicherheitszone gewährleistet werden, und Fragen Benutzer, ob Sie ein Abonnement für dieses Desktop Element erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="c66dd-127">The interfaces also notify users of any security risks that are warranted by the URL security zone settings, and they ask users if they would like to create a subscription for this desktop item.</span></span> <span data-ttu-id="c66dd-128">Beide Methoden bieten auch eine Möglichkeit, die Benutzeroberflächen zu unterdrücken.</span><span class="sxs-lookup"><span data-stu-id="c66dd-128">Both methods also provide a way of suppressing the user interfaces.</span></span> <span data-ttu-id="c66dd-129">Die [**iactivedesktop:: adddesktopitem**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitem) -Methode erfordert einen [**iactivedesktop:: ApplyChanges**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-applychanges) -Anrufe, um die Registrierung zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="c66dd-129">The [**IActiveDesktop::AddDesktopItem**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitem) method requires a call to [**IActiveDesktop::ApplyChanges**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-applychanges) in order to update the registry.</span></span> <span data-ttu-id="c66dd-130">Für **iactivedesktop:: adddesktopitemwithui** muss die Client Anwendung die [**iactivedesktop-**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop) Schnittstelle sofort freigeben und dann die [cokreateinstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) -Funktion verwenden, um eine Schnittstelle zu einer Instanz des **activedesktop** -Objekts abzurufen, das das neu hinzugefügte Desktop Element enthält.</span><span class="sxs-lookup"><span data-stu-id="c66dd-130">For the **IActiveDesktop::AddDesktopItemWithUI**, the client application must immediately release the [**IActiveDesktop**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop) interface and then use the [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) function to retrieve an interface to an instance of the **ActiveDesktop** object that includes the newly added desktop item.</span></span>

<span data-ttu-id="c66dd-131">Die [**iactivedesktop:: adddesktopitem**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitem) -Methode fügt das angegebene Desktop Element dem aktiven Desktop ohne Benutzeroberfläche hinzu, es sei denn, die URL-Sicherheitszonen Einstellungen verhindern dies.</span><span class="sxs-lookup"><span data-stu-id="c66dd-131">The [**IActiveDesktop::AddDesktopItem**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitem) method adds the specified desktop item to the Active Desktop without any user interface, unless the URL security zone settings prevent it.</span></span> <span data-ttu-id="c66dd-132">Wenn die URL-Sicherheitszonen Einstellungen nicht zulassen, dass das Desktop Element hinzugefügt wird, ohne den Benutzer aufzufordern, schlägt die Methode fehl.</span><span class="sxs-lookup"><span data-stu-id="c66dd-132">If the URL security zone settings do not allow the desktop item to be added without prompting the user, the method fails.</span></span> <span data-ttu-id="c66dd-133">**Iactivedesktop:: adddesktopitem** erfordert auch einen [**iactivedesktop:: ApplyChanges**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-applychanges) -Anrufe, um die Registrierung zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="c66dd-133">**IActiveDesktop::AddDesktopItem** also requires a call to [**IActiveDesktop::ApplyChanges**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-applychanges) in order to update the registry.</span></span>

<span data-ttu-id="c66dd-134">Im folgenden Beispiel wird veranschaulicht, wie Sie ein Desktop Element mit der [**iactivedesktop:: adddesktopitem**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitem) -Methode hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="c66dd-134">The following sample demonstrates how to add a desktop item with the [**IActiveDesktop::AddDesktopItem**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitem) method.</span></span>


```
HRESULT hr;
IActiveDesktop *pActiveDesktop;
COMPONENT compDesktopItem;

//Create an instance of the Active Desktop
hr = CoCreateInstance(CLSID_ActiveDesktop, NULL, CLSCTX_INPROC_SERVER,
                      IID_IActiveDesktop, (void**)&pActiveDesktop);

// Initialize the COMPONENT structure
compDesktopItem.dwSize = sizeof(COMPONENT);

// Insert code that adds the information about the desktop item 
// to the COMPONENT structure

// Add the desktop item
pActiveDesktop->AddDesktopItem(&compDesktopItem,0);

// Save the changes to the registry
pActiveDesktop->ApplyChanges(AD_APPLY_ALL);
```



### <a name="enumerating-the-desktop-items"></a><span data-ttu-id="c66dd-135">Auflisten der Desktop Elemente</span><span class="sxs-lookup"><span data-stu-id="c66dd-135">Enumerating the Desktop Items</span></span>

<span data-ttu-id="c66dd-136">Zum Auflisten der aktuell auf dem aktiven Desktop installierten Desktop Elemente muss die Client Anwendung die Gesamtzahl der mithilfe der [**iactivedesktop:: getdesktopitemcount**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-getdesktopitemcount) -Methode installierten Desktop Elemente abrufen und dann eine Schleife erstellen, die die [**Komponenten**](/windows/desktop/api/shlobj_core/ns-shlobj_core-component) Struktur für jedes Desktop Element abruft, indem die [**iactivedesktop:: getdesktopitem**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-getdesktopitem) -Methode mithilfe des Desktop Element Indexes aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="c66dd-136">To enumerate the desktop items currently installed on the Active Desktop, the client application needs to retrieve the total number of desktop items installed using the [**IActiveDesktop::GetDesktopItemCount**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-getdesktopitemcount) method and then creating a loop that retrieves the [**COMPONENT**](/windows/desktop/api/shlobj_core/ns-shlobj_core-component) structure for each desktop item by calling the [**IActiveDesktop::GetDesktopItem**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-getdesktopitem) method using the desktop item index.</span></span>

<span data-ttu-id="c66dd-137">Im folgenden Beispiel wird eine Möglichkeit zum Auflisten der Desktop Elemente veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="c66dd-137">The following sample demonstrates one way to enumerate the desktop items.</span></span>


```
HRESULT hr;
IActiveDesktop *pActiveDesktop;
COMPONENT compDesktopItem;
int intCount;
int intIndex = 0;

//Create an instance of the Active Desktop
hr = CoCreateInstance(CLSID_ActiveDesktop, NULL, CLSCTX_INPROC_SERVER,
                      IID_IActiveDesktop, (void**)&pActiveDesktop);

pActiveDesktop->GetDesktopItemCount(&intCount,0);

compDesktopItem.dwSize = sizeof(COMPONENT);

while(intIndex<=(intCount-1))
{
    //get the COMPONENT structure for the current desktop item
    pActiveDesktop->GetDesktopItem(intIndex, &compDesktopItem,0);

    //Insert code that processes the structure

    //Increment the index
    intIndex++;

    //Insert code to clean-up structure for next component
}

// Call the Release method
pActiveDesktop->Release();
```



 

 