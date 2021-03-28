---
description: Wenn der Benutzer mit der rechten Maustaste auf einen Member eines Dateityps klickt, um das Eigenschaften Blatt Eigenschaften anzuzeigen, ruft die Shell die Eigenschaften Blatt Handler auf, die für den Dateityp registriert sind. Jeder Handler kann dem Standardeigenschaften Blatt eine benutzerdefinierte Seite hinzufügen.
title: Registrieren und Implementieren eines Eigenschaften Blatt Handlers für einen Dateityp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77cf54886f7819fa910da23393c6db488ddfee72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994663"
---
# <a name="how-to-register-and-implement-a-property-sheet-handler-for-a-file-type"></a><span data-ttu-id="faa2d-104">Registrieren und Implementieren eines Eigenschaften Blatt Handlers für einen Dateityp</span><span class="sxs-lookup"><span data-stu-id="faa2d-104">How to Register and Implement a Property Sheet Handler for a File Type</span></span>

<span data-ttu-id="faa2d-105">Wenn der Benutzer mit der rechten Maustaste auf einen Member eines Dateityps klickt, um das Eigenschaften Blatt Eigenschaften anzuzeigen, ruft die Shell die Eigenschaften Blatt Handler auf, die für den Dateityp registriert sind.</span><span class="sxs-lookup"><span data-stu-id="faa2d-105">When the user right-clicks a member of a file type to display the Properties property sheet, the Shell calls the property sheet handlers that are registered for the file type.</span></span> <span data-ttu-id="faa2d-106">Jeder Handler kann dem Standardeigenschaften Blatt eine benutzerdefinierte Seite hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="faa2d-106">Each handler can add one custom page to the default property sheet.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="faa2d-107">Was Sie wissen müssen</span><span class="sxs-lookup"><span data-stu-id="faa2d-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="faa2d-108">Technologien</span><span class="sxs-lookup"><span data-stu-id="faa2d-108">Technologies</span></span>

-   <span data-ttu-id="faa2d-109">Shell</span><span class="sxs-lookup"><span data-stu-id="faa2d-109">Shell</span></span>

### <a name="prerequisites"></a><span data-ttu-id="faa2d-110">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="faa2d-110">Prerequisites</span></span>

-   <span data-ttu-id="faa2d-111">Ein Verständnis der Kontextmenüs</span><span class="sxs-lookup"><span data-stu-id="faa2d-111">An understanding of shortcut menus</span></span>

## <a name="instructions"></a><span data-ttu-id="faa2d-112">Instructions</span><span class="sxs-lookup"><span data-stu-id="faa2d-112">Instructions</span></span>

### <a name="step-1-registering-a-property-sheet-handler-for-a-file-type"></a><span data-ttu-id="faa2d-113">Schritt 1: Registrieren eines Eigenschaften Blatt Handlers für einen Dateityp</span><span class="sxs-lookup"><span data-stu-id="faa2d-113">Step 1: Registering a Property Sheet Handler for a File Type</span></span>

<span data-ttu-id="faa2d-114">Fügen Sie dem **shellex** -Unterschlüssel des ProgID-Schlüssels der Anwendung, die dem Dateityp zugeordnet ist, neben der normalen Component Object Model Registrierung (com) einen **propertysheethandlers** -Unterschlüssel hinzu.</span><span class="sxs-lookup"><span data-stu-id="faa2d-114">In addition to normal Component Object Model (COM) registration, add a **PropertySheetHandlers** subkey to the **shellex** subkey of the ProgID key of the application associated with the file type.</span></span> <span data-ttu-id="faa2d-115">Erstellen Sie einen Unterschlüssel von **propertysheethandlers** mit dem Namen des Handlers, und legen Sie den Standardwert auf das Zeichen folgen Format der Klassen Bezeichner-GUID (CLSID) des Eigenschaften Blatts fest.</span><span class="sxs-lookup"><span data-stu-id="faa2d-115">Create a subkey of **PropertySheetHandlers** with the handler's name, and set the default value to the string form of the property sheet handler's class identifier (CLSID) GUID.</span></span>

<span data-ttu-id="faa2d-116">Wenn Sie dem Eigenschaften Blatt mehr als eine Seite hinzufügen möchten, registrieren Sie einen Handler für jede Seite.</span><span class="sxs-lookup"><span data-stu-id="faa2d-116">To add more than one page to the property sheet, register a handler for each page.</span></span> <span data-ttu-id="faa2d-117">Die maximale Anzahl von Seiten, die von einem Eigenschaften Blatt unterstützt werden können, ist 32.</span><span class="sxs-lookup"><span data-stu-id="faa2d-117">The maximum number of pages that a property sheet can support is 32.</span></span> <span data-ttu-id="faa2d-118">Um mehrere Handler zu registrieren, erstellen Sie einen Schlüssel unter dem **shellex** -Schlüssel für jeden Handler, wobei der Standardwert auf die CLSID-GUID des Handlers festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="faa2d-118">To register multiple handlers, create a key under the **shellex** key for each handler, with the default value set to the handler's CLSID GUID.</span></span> <span data-ttu-id="faa2d-119">Es ist nicht erforderlich, für jeden Handler ein unterschiedliches Objekt zu erstellen, was bedeutet, dass mehrere Handler denselben GUID-Wert aufweisen können.</span><span class="sxs-lookup"><span data-stu-id="faa2d-119">It is not necessary to create a distinct object for each handler, which means that multiple handlers can all have the same GUID value.</span></span> <span data-ttu-id="faa2d-120">Die Seiten werden in der Reihenfolge angezeigt, in der Ihre Schlüssel unter **shellex** aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="faa2d-120">The pages will be displayed in the order that their keys are listed under **shellex**.</span></span>

<span data-ttu-id="faa2d-121">Das folgende Beispiel veranschaulicht einen Registrierungs Eintrag, der zwei Eigenschaften Blatt-Erweiterungs Handler für den Dateityp example. MYP aktiviert.</span><span class="sxs-lookup"><span data-stu-id="faa2d-121">The following example illustrates a registry entry that enables two property sheet extension handlers for an example .myp file type.</span></span> <span data-ttu-id="faa2d-122">In diesem Beispiel wird ein separates Objekt für jede Seite verwendet, aber es kann auch ein einzelnes Objekt für beide verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="faa2d-122">In this example, a separate object is used for each page, but a single object could also be used for both.</span></span>

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
   CLSID
      {Page 1 Property Sheet Handler CLSID GUID}
         InProcServer32
            (Default) = C:\MyDir\MyPropSheet1.dll
            ThreadingModel = Apartment
      {Page 2 Property Sheet Handler CLSID GUID}
         InProcServer32
            (Default) = C:\MyDir\MyPropSheet2.dll
            ThreadingModel = Apartment
   MyProgram.1
      (Default) = MyProgram Application
      shellex
         PropertySheetHandlers
            MyPropSheet1
               (Default) = {Page1 Property Sheet Handler CLSID GUID}
            MyPropSheet2
               (Default) = {Page2 Property Sheet Handler CLSID GUID}
```

### <a name="step-2-implementing-a-property-sheet-handler-for-a-file-type"></a><span data-ttu-id="faa2d-123">Schritt 2: Implementieren eines Eigenschaften Blatt Handlers für einen Dateityp</span><span class="sxs-lookup"><span data-stu-id="faa2d-123">Step 2: Implementing a Property Sheet Handler for a File Type</span></span>

<span data-ttu-id="faa2d-124">Zusätzlich zu der allgemeinen Implementierung, die unter [Funktionsweise von Eigenschaften Blatt Handlern](propsheet-handlers.md)erläutert wird, muss ein Eigenschaften Blatt Handler für einen Dateityp auch über eine entsprechende Implementierung der [**ishellpropsheetext**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext) -Schnittstelle verfügen.</span><span class="sxs-lookup"><span data-stu-id="faa2d-124">In addition to the general implementation discussed in [How Property Sheet Handlers Work](propsheet-handlers.md), a property sheet handler for a file type must also have an appropriate implementation of the [**IShellPropSheetExt**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext) interface.</span></span> <span data-ttu-id="faa2d-125">Nur die [**ishellpropsheetext:: addPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) -Methode benötigt eine nicht Token-Implementierung.</span><span class="sxs-lookup"><span data-stu-id="faa2d-125">Only the [**IShellPropSheetExt::AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) method needs a nontoken implementation.</span></span> <span data-ttu-id="faa2d-126">Die Shell ruft nicht [**ishellpropsheetext:: replacepage**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-replacepage)auf.</span><span class="sxs-lookup"><span data-stu-id="faa2d-126">The Shell does not call [**IShellPropSheetExt::ReplacePage**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-replacepage).</span></span>

<span data-ttu-id="faa2d-127">Mit der [**ishellpropsheetext:: addPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) -Methode kann ein Eigenschaften Blatt Handler eine Seite zu einem Eigenschaften Blatt hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="faa2d-127">The [**IShellPropSheetExt::AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) method allows a property sheet handler to add a page to a property sheet.</span></span> <span data-ttu-id="faa2d-128">Die-Methode verfügt über zwei Eingabeparameter.</span><span class="sxs-lookup"><span data-stu-id="faa2d-128">The method has two input parameters.</span></span> <span data-ttu-id="faa2d-129">Der erste *lpfnaddpage*-Wert ist ein Zeiger auf eine [*addpropsheetpageproc*](/windows/win32/api/prsht/nc-prsht-lpfnaddpropsheetpage) -Rückruffunktion, die verwendet wird, um der Shell die Informationen zur Verfügung zu stellen, die erforderlich sind, um die Seite dem Eigenschaften Blatt hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="faa2d-129">The first, *lpfnAddPage*, is a pointer to an [*AddPropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnaddpropsheetpage) callback function that is used to provide the Shell with the information needed to add the page to the property sheet.</span></span> <span data-ttu-id="faa2d-130">Der zweite *LPARAM*-Wert ist ein shelldefinierter Wert, der nicht vom Handler verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="faa2d-130">The second, *lParam*, is a Shell-defined value that is not processed by the handler.</span></span> <span data-ttu-id="faa2d-131">Sie wird einfach an die Shell zurückgegeben, wenn die Rückruffunktion aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="faa2d-131">It is simply passed back to the Shell when the callback function is called.</span></span>

<span data-ttu-id="faa2d-132">Das allgemeine Verfahren zum Implementieren von [**addPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) lautet wie folgt.</span><span class="sxs-lookup"><span data-stu-id="faa2d-132">The general procedure for implementing [**AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) is as follows.</span></span>

<span data-ttu-id="faa2d-133">**Implementieren der addPages-Methode**</span><span class="sxs-lookup"><span data-stu-id="faa2d-133">**Implementing the AddPages Method**</span></span>

1.  <span data-ttu-id="faa2d-134">Weisen Sie den Membern einer [**PROPSHEETPAGE**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v3) -Struktur geeignete Werte zu.</span><span class="sxs-lookup"><span data-stu-id="faa2d-134">Assign appropriate values to the members of a [**PROPSHEETPAGE**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v3) structure.</span></span> <span data-ttu-id="faa2d-135">Dies gilt insbesondere für:</span><span class="sxs-lookup"><span data-stu-id="faa2d-135">In particular:</span></span>
    -   <span data-ttu-id="faa2d-136">Weisen Sie die Variable, die den Verweis Zähler des Handlers enthält, dem **pkrefparent** -Member zu.</span><span class="sxs-lookup"><span data-stu-id="faa2d-136">Assign the variable that holds the handler's reference count to the **pcRefParent** member.</span></span> <span data-ttu-id="faa2d-137">Diese Vorgehensweise verhindert, dass das Handlerobjekt entladen wird, während das Eigenschaften Blatt noch angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="faa2d-137">This practice prevents the handler object from being unloaded while the property sheet is still being displayed.</span></span>
    -   <span data-ttu-id="faa2d-138">Sie können auch eine [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) -Rückruffunktion implementieren und Ihren Zeiger einem **pfncallback** -Member zuweisen.</span><span class="sxs-lookup"><span data-stu-id="faa2d-138">You can also implement a [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) callback function and assign its pointer to a **pfnCallback** member.</span></span> <span data-ttu-id="faa2d-139">Diese Funktion wird aufgerufen, wenn die Seite erstellt wird und wenn Sie gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="faa2d-139">This function is called when the page is created and when it is about to be destroyed.</span></span>
2.  <span data-ttu-id="faa2d-140">Erstellen Sie den hPage-Handle der Seite, indem Sie die [**PROPSHEETPAGE**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v3) -Struktur an [**die Funktion "**](/windows/win32/api/prsht/nf-prsht-createpropertysheetpagea) " in der Funktion "-Funktion" übergeben.</span><span class="sxs-lookup"><span data-stu-id="faa2d-140">Create the page's HPAGE handle by passing the [**PROPSHEETPAGE**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v3) structure to the [**CreatePropertySheetPage**](/windows/win32/api/prsht/nf-prsht-createpropertysheetpagea) function.</span></span>
3.  <span data-ttu-id="faa2d-141">Die Funktion, auf die von *lpfnaddpage* verwiesen wird, wird aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="faa2d-141">Call the function that is pointed to by *lpfnAddPage*.</span></span> <span data-ttu-id="faa2d-142">Legen Sie den ersten Parameter auf das hPage-Handle fest, das im vorherigen Schritt erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="faa2d-142">Set its first parameter to the HPAGE handle that was created in the previous step.</span></span> <span data-ttu-id="faa2d-143">Legen Sie den zweiten Parameter auf den *LPARAM* -Wert fest, der von der Shell an [**addPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) übergeben wurde.</span><span class="sxs-lookup"><span data-stu-id="faa2d-143">Set its second parameter to the *lParam* value that was passed in to [**AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) by the Shell.</span></span>
4.  <span data-ttu-id="faa2d-144">Alle der Seite zugeordneten Nachrichten werden an die Dialogfeld Prozedur, die dem **pfndlgproc** -Member der [**PROPSHEETPAGE**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v3) -Struktur zugewiesen wurde, übermittelt.</span><span class="sxs-lookup"><span data-stu-id="faa2d-144">Any messages associated with the page will be passed to the dialog box procedure that was assigned to the **pfnDlgProc** member of the [**PROPSHEETPAGE**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v3) structure.</span></span>
5.  <span data-ttu-id="faa2d-145">Wenn Sie **pfncallback** eine [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) -Rückruffunktion zugewiesen haben, wird Sie aufgerufen, wenn die Seite zerstört werden soll.</span><span class="sxs-lookup"><span data-stu-id="faa2d-145">If you assigned a [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) callback function to **pfnCallback**, it will be called when the page is about to be destroyed.</span></span> <span data-ttu-id="faa2d-146">Der Handler kann dann alle erforderlichen Bereinigungs Vorgänge ausführen, z. b. die Freigabe aller darin enthaltenen Verweise.</span><span class="sxs-lookup"><span data-stu-id="faa2d-146">Your handler can then perform any needed cleanup operations, such as releasing any references that it holds.</span></span>

<span data-ttu-id="faa2d-147">Im folgenden Codebeispiel wird eine einfache [**addPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) -Implementierung veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="faa2d-147">The following code sample illustrates a simple [**AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) implementation.</span></span>


```C++
STDMETHODIMP CShellPropSheetExt::AddPages(LPFNADDPROPSHEETPAGE, lpfnAddPage, LPARAM lParam)
{
    PROPSHEETPAGE  psp;
    HPROPSHEETPAGE hPage;

    psp.dwSize        = sizeof(psp);
    psp.dwFlags       = PSP_USEREFPARENT | PSP_USETITLE | PSP_USECALLBACK;
    psp.hInstance     = g_hInst;
    psp.pszTemplate   = MAKEINTRESOURCE(IDD_PAGEDLG);
    psp.hIcon         = 0;
    psp.pszTitle      = TEXT("Extension Page");
    psp.pfnDlgProc    = (DLGPROC)PageDlgProc;
    psp.pcRefParent   = &g_DllRefCount;
    psp.pfnCallback   = PageCallbackProc;
    psp.lParam        = (LPARAM)this;

    hPage = CreatePropertySheetPage(&psp);
            
    if(hPage) 
    {
        if(lpfnAddPage(hPage, lParam))
        {
            this->AddRef();
            return S_OK;
        }
        else
        {
            DestroyPropertySheetPage(hPage);
        }
    }
    else
    {
        return E_OUTOFMEMORY;
    }
    return E_FAIL;
}
```



<span data-ttu-id="faa2d-148">Die Variable **g \_ hInst** ist der Instanzhandle für die dll, und IDD \_ pagedlg ist die Ressourcen-ID der Dialogfeld Vorlage der Seite.</span><span class="sxs-lookup"><span data-stu-id="faa2d-148">The **g\_hInst** variable is the instance handle to the DLL, and IDD\_PAGEDLG is the resource ID of the page's dialog box template.</span></span> <span data-ttu-id="faa2d-149">Die **pagedlgproc** -Funktion ist die Dialogfeld Prozedur, die die Meldungen der Seite behandelt.</span><span class="sxs-lookup"><span data-stu-id="faa2d-149">The **PageDlgProc** function is the dialog box procedure that handles the page's messages.</span></span> <span data-ttu-id="faa2d-150">Die **g \_ dllref count** -Variable enthält den Verweis Zähler des Objekts.</span><span class="sxs-lookup"><span data-stu-id="faa2d-150">The **g\_DllRefCount** variable holds the object's reference count.</span></span> <span data-ttu-id="faa2d-151">Die [**addPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) -Methode ruft die [**adressf**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) auf, um die Anzahl zu erhöhen.</span><span class="sxs-lookup"><span data-stu-id="faa2d-151">The [**AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) method calls [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) to increment the count.</span></span> <span data-ttu-id="faa2d-152">Der Verweis Zähler wird jedoch von der Rückruffunktion **pagecallbackproc** freigegeben, wenn die Seite zerstört werden soll.</span><span class="sxs-lookup"><span data-stu-id="faa2d-152">However, the reference count is released by the callback function, **PageCallbackProc**, when the page is about to be destroyed.</span></span>

## <a name="remarks"></a><span data-ttu-id="faa2d-153">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="faa2d-153">Remarks</span></span>

<span data-ttu-id="faa2d-154">Eine allgemeine Erläuterung zum Registrieren von Shellerweiterungs Handlern finden Sie unter [Erstellen von Shellerweiterungs Handlern](handlers.md).</span><span class="sxs-lookup"><span data-stu-id="faa2d-154">For a general discussion of how to register Shell extension handlers, see [Creating Shell Extension Handlers](handlers.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="faa2d-155">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="faa2d-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="faa2d-156">**Ishellpropsheetext**</span><span class="sxs-lookup"><span data-stu-id="faa2d-156">**IShellPropSheetExt**</span></span>](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext)
</dt> </dl>

 

 
