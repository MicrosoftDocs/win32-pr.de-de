---
description: IContextMenu ist die leistungsfähigste, aber auch die komplizierteste Schnittstelle, die implementiert werden kann.
ms.assetid: F0C1D60E-7A5A-4609-9136-F4E535E9F6F1
title: Implementieren der IContextMenu-Schnittstelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f251b9a64c3f401239eeb7c88286c016f399cc39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959691"
---
# <a name="how-to-implement-the-icontextmenu-interface"></a><span data-ttu-id="5fc99-103">Implementieren der IContextMenu-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="5fc99-103">How to Implement the IContextMenu Interface</span></span>

<span data-ttu-id="5fc99-104">[**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) ist die leistungsfähigste, aber auch die komplizierteste Schnittstelle, die implementiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="5fc99-104">[**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) is the most powerful but also the most complicated interface to implement.</span></span> <span data-ttu-id="5fc99-105">Es wird dringend empfohlen, dass Sie ein Verb mithilfe einer der statischen Verb-Methoden implementieren.</span><span class="sxs-lookup"><span data-stu-id="5fc99-105">We strongly recommend that you implement a verb by using one of the static verb methods.</span></span> <span data-ttu-id="5fc99-106">Weitere Informationen finden Sie unter [Auswählen einer statischen oder dynamischen Kontextmenü Methode](shortcut-choose-method.md).</span><span class="sxs-lookup"><span data-stu-id="5fc99-106">For more information, see [Choosing a Static or Dynamic Shortcut Menu Method](shortcut-choose-method.md).</span></span> <span data-ttu-id="5fc99-107">[**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) verfügt über drei Methoden: [**getcommandstring**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring), [**InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand)und [**querycontextmenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu), die hier ausführlich erläutert werden.</span><span class="sxs-lookup"><span data-stu-id="5fc99-107">[**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) has three methods, [**GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring), [**InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand), and [**QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu), which are discussed here in detail.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="5fc99-108">Was Sie wissen müssen</span><span class="sxs-lookup"><span data-stu-id="5fc99-108">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="5fc99-109">Technologien</span><span class="sxs-lookup"><span data-stu-id="5fc99-109">Technologies</span></span>

-   <span data-ttu-id="5fc99-110">C++</span><span class="sxs-lookup"><span data-stu-id="5fc99-110">C++</span></span>

### <a name="prerequisites"></a><span data-ttu-id="5fc99-111">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="5fc99-111">Prerequisites</span></span>

-   <span data-ttu-id="5fc99-112">Statisches Verb</span><span class="sxs-lookup"><span data-stu-id="5fc99-112">Static Verb</span></span>
-   <span data-ttu-id="5fc99-113">Kontextmenü</span><span class="sxs-lookup"><span data-stu-id="5fc99-113">Shortcut Menu</span></span>

## <a name="instructions"></a><span data-ttu-id="5fc99-114">Instructions</span><span class="sxs-lookup"><span data-stu-id="5fc99-114">Instructions</span></span>

### <a name="icontextmenugetcommandstring-method"></a><span data-ttu-id="5fc99-115">IContextMenu:: getcommandstring-Methode</span><span class="sxs-lookup"><span data-stu-id="5fc99-115">IContextMenu::GetCommandString Method</span></span>

<span data-ttu-id="5fc99-116">Die [**IContextMenu:: getcommandstring**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) -Methode des Handlers wird verwendet, um den kanonischen Namen eines Verbs zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="5fc99-116">The handler's [**IContextMenu::GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) method is used to return the canonical name for a verb.</span></span> <span data-ttu-id="5fc99-117">Diese Methode ist optional.</span><span class="sxs-lookup"><span data-stu-id="5fc99-117">This method is optional.</span></span> <span data-ttu-id="5fc99-118">In Windows XP und früheren Versionen von Windows wird diese Methode verwendet, um den Hilfetext abzurufen, der in der Statusleiste für ein Menü Element angezeigt wird, wenn Windows-Explorer über eine Status Leiste verfügt.</span><span class="sxs-lookup"><span data-stu-id="5fc99-118">In Windows XP and earlier versions of Windows, when Windows Explorer has a Status bar, this method is used to retrieve the help text that is displayed in the Status bar for a menu item.</span></span>

<span data-ttu-id="5fc99-119">Der *idcmd* -Parameter enthält den bezeichneroffset des Befehls, der beim [**Aufrufen von IContextMenu:: querycontextmenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) definiert wurde.</span><span class="sxs-lookup"><span data-stu-id="5fc99-119">The *idCmd* parameter holds the identifier offset of the command that was defined when [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) was called.</span></span> <span data-ttu-id="5fc99-120">Wenn eine Hilfe Zeichenfolge angefordert wird, wird *uFlags* auf **GCS \_ helptextw** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="5fc99-120">If a help string is requested, *uFlags* will be set to **GCS\_HELPTEXTW**.</span></span> <span data-ttu-id="5fc99-121">Kopieren Sie die Hilfe Zeichenfolge in den *pszName* -Puffer, und wandeln Sie Sie in ein **pwstr** um.</span><span class="sxs-lookup"><span data-stu-id="5fc99-121">Copy the help string to the *pszName* buffer, casting it to a **PWSTR**.</span></span> <span data-ttu-id="5fc99-122">Die Verb Zeichenfolge wird angefordert, indem *uFlags* auf **GCS- \_ verbw** festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="5fc99-122">The verb string is requested by setting *uFlags* to **GCS\_VERBW**.</span></span> <span data-ttu-id="5fc99-123">Kopieren Sie die entsprechende Zeichenfolge wie bei der Hilfe Zeichenfolge in *pszName*.</span><span class="sxs-lookup"><span data-stu-id="5fc99-123">Copy the appropriate string to *pszName*, just as with the help string.</span></span> <span data-ttu-id="5fc99-124">Die **\_ validatew** -Flags für **GCS \_ validatea** und GCS werden von Kontextmenü Handlern nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="5fc99-124">The **GCS\_VALIDATEA** and **GCS\_VALIDATEW** flags are not used by shortcut menu handlers.</span></span>

<span data-ttu-id="5fc99-125">Das folgende Beispiel zeigt eine einfache Implementierung von [**getcommandstring**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) , die dem im Abschnitt [IContextMenu:: querycontextmenu-Methode](shortcut-menu-using-dynamic-verbs.md) in diesem Thema angegebenen [**querycontextmenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) -Beispiel entspricht.</span><span class="sxs-lookup"><span data-stu-id="5fc99-125">The following example shows a simple implementation of [**GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) that corresponds to the [**QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) example given in the [IContextMenu::QueryContextMenu Method](shortcut-menu-using-dynamic-verbs.md) section of this topic.</span></span> <span data-ttu-id="5fc99-126">Da der Handler nur ein Menü Element hinzufügt, gibt es nur einen Satz von Zeichen folgen, die zurückgegeben werden können.</span><span class="sxs-lookup"><span data-stu-id="5fc99-126">Because the handler adds only one menu item, there is only one set of strings that can be returned.</span></span> <span data-ttu-id="5fc99-127">Die-Methode testet, ob *idcmd* gültig ist, und gibt, wenn dies der Fall ist, die angeforderte Zeichenfolge zurück.</span><span class="sxs-lookup"><span data-stu-id="5fc99-127">The method tests whether *idCmd* is valid and, if it is, returns the requested string.</span></span>

<span data-ttu-id="5fc99-128">Die [**StringCchCopy**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopya) -Funktion wird verwendet, um die angeforderte Zeichenfolge nach *pszName* zu kopieren, um sicherzustellen, dass die kopierte Zeichenfolge die Größe des durch *cchName* angegebenen Puffers nicht überschreitet.</span><span class="sxs-lookup"><span data-stu-id="5fc99-128">The [**StringCchCopy**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopya) function is used to copy the requested string to *pszName* to ensure that the copied string does not exceed the size of the buffer specified by *cchName*.</span></span> <span data-ttu-id="5fc99-129">In diesem Beispiel wird die Unterstützung nur für die Unicode-Werte von *uFlags* implementiert, da nur diese seit Windows 2000 in Windows-Explorer verwendet wurden.</span><span class="sxs-lookup"><span data-stu-id="5fc99-129">This example implements support only for the Unicode values of *uFlags*, because only those have been used in Windows Explorer since Windows 2000.</span></span>


```
IFACEMETHODIMP CMenuExtension::GetCommandString(UINT idCommand, 
                                                UINT uFlags, 
                                                UINT *pReserved, 
                                                PSTR pszName, 
                                                UINT cchName)
{
    HRESULT hr = E_INVALIDARG;

    if (idCommand == IDM_DISPLAY)
    {
        switch (uFlags)
        {
            case GCS_HELPTEXTW:
                // Only useful for pre-Vista versions of Windows that 
                // have a Status bar.
                hr = StringCchCopyW(reinterpret_cast<PWSTR>(pszName), 
                                    cchName, 
                                    L"Display File Name");
                break; 

            case GCS_VERBW:
                // GCS_VERBW is an optional feature that enables a caller
                // to discover the canonical name for the verb that is passed in
                // through idCommand.
                hr = StringCchCopyW(reinterpret_cast<PWSTR>(pszName), 
                                    cchName, 
                                    L"DisplayFileName");
                break; 
        }
    }
    return hr;
}
```



### <a name="icontextmenuinvokecommand-method"></a><span data-ttu-id="5fc99-130">IContextMenu:: InvokeCommand-Methode</span><span class="sxs-lookup"><span data-stu-id="5fc99-130">IContextMenu::InvokeCommand Method</span></span>

<span data-ttu-id="5fc99-131">Diese Methode wird aufgerufen, wenn ein Benutzer auf ein Menü Element klickt, um den Handler anzuweisen, den zugehörigen Befehl auszuführen.</span><span class="sxs-lookup"><span data-stu-id="5fc99-131">This method is called when a user clicks a menu item to tell the handler to run the associated command.</span></span> <span data-ttu-id="5fc99-132">Der *pici* -Parameter verweist auf eine-Struktur, die die zum Ausführen des Befehls erforderlichen Informationen enthält.</span><span class="sxs-lookup"><span data-stu-id="5fc99-132">The *pici* parameter points to a structure that contains the information required to run the command.</span></span>

<span data-ttu-id="5fc99-133">Obwohl *pici* in shlobj. h als [**cminvokecommandinfo**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo) -Struktur deklariert ist, verweist es in der Praxis häufig auf eine [**cminvokecommandinfoex**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfoex) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="5fc99-133">Although *pici* is declared in Shlobj.h as a [**CMINVOKECOMMANDINFO**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo) structure, in practice it often points to a [**CMINVOKECOMMANDINFOEX**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfoex) structure.</span></span> <span data-ttu-id="5fc99-134">Diese Struktur ist eine erweiterte Version von **cminvokecommandinfo** und verfügt über mehrere zusätzliche Member, die es ermöglichen, Unicode-Zeichen folgen zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="5fc99-134">This structure is an extended version of **CMINVOKECOMMANDINFO** and has several additional members that make it possible to pass Unicode strings.</span></span>

<span data-ttu-id="5fc99-135">Überprüfen Sie das **CBSIZE** -Member von *pici* , um zu bestimmen, welche Struktur übergeben wurde.</span><span class="sxs-lookup"><span data-stu-id="5fc99-135">Check the **cbSize** member of *pici* to determine which structure was passed in.</span></span> <span data-ttu-id="5fc99-136">Wenn es sich um eine [**cminvokecommandinfoex**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfoex) -Struktur handelt und für den **fmask** -Member das **CMIC \_ mask- \_ Unicode** -Flag festgelegt ist, wandeln Sie *pici* in **cminvokecommandinfoex** um.</span><span class="sxs-lookup"><span data-stu-id="5fc99-136">If it is a [**CMINVOKECOMMANDINFOEX**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfoex) structure and the **fMask** member has the **CMIC\_MASK\_UNICODE** flag set, cast *pici* to **CMINVOKECOMMANDINFOEX**.</span></span> <span data-ttu-id="5fc99-137">Dadurch kann Ihre Anwendung die Unicode-Informationen verwenden, die in den letzten fünf Membern der Struktur enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="5fc99-137">This enables your application to use the Unicode information that is contained in the last five members of the structure.</span></span>

<span data-ttu-id="5fc99-138">Der **lpverb** -oder **lpverbw** -Member der Struktur wird verwendet, um den auszuführenden Befehl zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="5fc99-138">The structure's **lpVerb** or **lpVerbW** member is used to identify the command to be executed.</span></span> <span data-ttu-id="5fc99-139">Befehle werden auf eine der beiden folgenden Arten identifiziert:</span><span class="sxs-lookup"><span data-stu-id="5fc99-139">Commands are identified in one of the following two ways:</span></span>

-   <span data-ttu-id="5fc99-140">Durch die Verb Zeichenfolge des Befehls</span><span class="sxs-lookup"><span data-stu-id="5fc99-140">By the command's verb string</span></span>
-   <span data-ttu-id="5fc99-141">Nach dem bezeichneroffset des Befehls</span><span class="sxs-lookup"><span data-stu-id="5fc99-141">By the command's identifier offset</span></span>

<span data-ttu-id="5fc99-142">Um zwischen diesen beiden Fällen zu unterscheiden, überprüfen Sie das höchst wertige Wort **lpverb** für die ANSI-Groß-/Kleinschreibung oder **lpverbw** für den Unicode-Fall.</span><span class="sxs-lookup"><span data-stu-id="5fc99-142">To distinguish between these two cases, check the high-order word of **lpVerb** for the ANSI case or **lpVerbW** for the Unicode case.</span></span> <span data-ttu-id="5fc99-143">Wenn das hochwertige Wort nicht NULL ist, enthält **lpverb** oder **lpverbw** eine Verb Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="5fc99-143">If the high-order word is nonzero, **lpVerb** or **lpVerbW** holds a verb string.</span></span> <span data-ttu-id="5fc99-144">Wenn das hochwertige Wort 0 (null) ist, befindet sich der Befehls Offset im nieder wertigen Wort **lpverb**.</span><span class="sxs-lookup"><span data-stu-id="5fc99-144">If the high-order word is zero, the command offset is in the low-order word of **lpVerb**.</span></span>

<span data-ttu-id="5fc99-145">Das folgende Beispiel zeigt eine einfache Implementierung von [**IContextMenu:: InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) , die den Beispielen " [**IContextMenu:: querycontextmenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) " und " [**IContextMenu:: getcommandstring**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) " entspricht, die vor und nach diesem Abschnitt angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="5fc99-145">The following example shows a simple implementation of [**IContextMenu::InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) that corresponds to the [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) and [**IContextMenu::GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) examples given before and after this section.</span></span> <span data-ttu-id="5fc99-146">Die-Methode bestimmt zunächst, welche Struktur an Sie übermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="5fc99-146">The method first determines which structure is being passed in.</span></span> <span data-ttu-id="5fc99-147">Anschließend bestimmt er, ob der Befehl durch seinen Offset oder sein Verb gekennzeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="5fc99-147">It then determines whether the command is identified by its offset or its verb.</span></span> <span data-ttu-id="5fc99-148">Wenn **lpverb** oder **lpverbw** ein gültiges Verb oder einen gültigen Offset enthält, zeigt die Methode ein Meldungs Feld an.</span><span class="sxs-lookup"><span data-stu-id="5fc99-148">If **lpVerb** or **lpVerbW** holds a valid verb or offset, the method displays a message box.</span></span>


```
STDMETHODIMP CShellExtension::InvokeCommand(LPCMINVOKECOMMANDINFO lpcmi)
{
    BOOL fEx = FALSE;
    BOOL fUnicode = FALSE;

    if(lpcmi->cbSize == sizeof(CMINVOKECOMMANDINFOEX))
    {
        fEx = TRUE;
        if((lpcmi->fMask & CMIC_MASK_UNICODE))
        {
            fUnicode = TRUE;
        }
    }

    if( !fUnicode && HIWORD(lpcmi->lpVerb))
    {
        if(StrCmpIA(lpcmi->lpVerb, m_pszVerb))
        {
            return E_FAIL;
        }
    }

    else if( fUnicode && HIWORD(((CMINVOKECOMMANDINFOEX *) lpcmi)->lpVerbW))
    {
        if(StrCmpIW(((CMINVOKECOMMANDINFOEX *)lpcmi)->lpVerbW, m_pwszVerb))
        {
            return E_FAIL;
        }
    }

    else if(LOWORD(lpcmi->lpVerb) != IDM_DISPLAY)
    {
        return E_FAIL;
    }

    else
    {
        MessageBox(lpcmi->hwnd,
                   "The File Name",
                   "File Name",
                   MB_OK|MB_ICONINFORMATION);
    }

    return S_OK;
}
```



### <a name="icontextmenuquerycontextmenu-method"></a><span data-ttu-id="5fc99-149">IContextMenu:: querycontextmenu-Methode</span><span class="sxs-lookup"><span data-stu-id="5fc99-149">IContextMenu::QueryContextMenu Method</span></span>

<span data-ttu-id="5fc99-150">Die Shell ruft [**IContextMenu:: querycontextmenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) auf, damit der Kontextmenü Handler dem Menü die Menü Elemente hinzufügen kann.</span><span class="sxs-lookup"><span data-stu-id="5fc99-150">The Shell calls [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) to enable the shortcut menu handler to add its menu items to the menu.</span></span> <span data-ttu-id="5fc99-151">Sie übergibt den **HMENU** -Handle im *HMENU* -Parameter.</span><span class="sxs-lookup"><span data-stu-id="5fc99-151">It passes in the **HMENU** handle in the *hmenu* parameter.</span></span> <span data-ttu-id="5fc99-152">Der *indexmenu* -Parameter wird auf den Index festgelegt, der für das erste hinzu zufügende Menü Element verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="5fc99-152">The *indexMenu* parameter is set to the index to be used for the first menu item that is to be added.</span></span>

<span data-ttu-id="5fc99-153">Alle vom Handler hinzugefügten Menü Elemente müssen über Bezeichner verfügen, die zwischen den Werten in den Parametern *idcmdfirst* und *idcmdlast* liegen.</span><span class="sxs-lookup"><span data-stu-id="5fc99-153">Any menu items that are added by the handler must have identifiers that fall between the values in the *idCmdFirst* and *idCmdLast* parameters.</span></span> <span data-ttu-id="5fc99-154">In der Regel wird der erste Befehls Bezeichner auf *idcmdfirst* festgelegt, der für jeden zusätzlichen Befehl um eins (1) erhöht wird.</span><span class="sxs-lookup"><span data-stu-id="5fc99-154">Typically, the first command identifier is set to *idCmdFirst*, which is incremented by one (1) for each additional command.</span></span> <span data-ttu-id="5fc99-155">Mit dieser Vorgehensweise können Sie die Überschreitung von *idcmdlast* vermeiden und die Anzahl der verfügbaren Bezeichner maximieren, falls die Shell mehr als einen Handler aufruft.</span><span class="sxs-lookup"><span data-stu-id="5fc99-155">This practice helps you to avoid exceeding *idCmdLast* and maximizes the number of available identifiers in case the Shell calls more than one handler.</span></span>

<span data-ttu-id="5fc99-156">Der *Befehls Offset* eines Element Bezeichners ist der Unterschied zwischen dem Bezeichner und dem Wert in *idcmdfirst*.</span><span class="sxs-lookup"><span data-stu-id="5fc99-156">An item identifier's *command offset* is the difference between the identifier and the value in *idCmdFirst*.</span></span> <span data-ttu-id="5fc99-157">Speichern Sie den Offset der einzelnen Elemente, die der Handler dem Kontextmenü hinzufügt, da die Shell den Offset verwenden kann, um das Element zu identifizieren, wenn es anschließend [**IContextMenu:: getcommandstring**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) oder [**IContextMenu:: InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand)aufruft.</span><span class="sxs-lookup"><span data-stu-id="5fc99-157">Store the offset of each item that your handler adds to the shortcut menu, because the Shell might use the offset to identify the item if it subsequently calls [**IContextMenu::GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) or [**IContextMenu::InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand).</span></span>

<span data-ttu-id="5fc99-158">Sie sollten jedem Befehl, den Sie hinzufügen, auch ein [Verb](launch.md) zuweisen.</span><span class="sxs-lookup"><span data-stu-id="5fc99-158">You should also assign a [verb](launch.md) to each command that you add.</span></span> <span data-ttu-id="5fc99-159">Ein Verb ist eine Zeichenfolge, die anstelle des Offsets verwendet werden kann, um den Befehl zu identifizieren, wenn [**InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="5fc99-159">A verb is a string that can be used instead of the offset to identify the command when [**InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) is called.</span></span> <span data-ttu-id="5fc99-160">Sie wird auch von Funktionen wie [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) zum Ausführen von Kontextmenü Befehlen verwendet.</span><span class="sxs-lookup"><span data-stu-id="5fc99-160">It is also used by functions such as [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) to execute shortcut menu commands.</span></span>

<span data-ttu-id="5fc99-161">Es gibt drei Flags, die über den *uFlags* -Parameter übergeben werden können, die für Kontextmenü Handler relevant sind.</span><span class="sxs-lookup"><span data-stu-id="5fc99-161">There are three flags that can be passed in through the *uFlags* parameter that are relevant to shortcut menu handlers.</span></span> <span data-ttu-id="5fc99-162">Diese werden in der folgenden Tabelle beschrieben.</span><span class="sxs-lookup"><span data-stu-id="5fc99-162">They are described in the following table.</span></span>



| <span data-ttu-id="5fc99-163">Flag</span><span class="sxs-lookup"><span data-stu-id="5fc99-163">Flag</span></span>             | <span data-ttu-id="5fc99-164">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5fc99-164">Description</span></span>                                                                                                                                                                                                              |
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5fc99-165">CMF \_ DefaultOnly</span><span class="sxs-lookup"><span data-stu-id="5fc99-165">CMF\_DEFAULTONLY</span></span> | <span data-ttu-id="5fc99-166">Der Benutzer hat den Standardbefehl ausgewählt, in der Regel durch Doppelklicken auf das Objekt.</span><span class="sxs-lookup"><span data-stu-id="5fc99-166">The user has selected the default command, usually by double-clicking the object.</span></span> <span data-ttu-id="5fc99-167">[**IContextMenu:: querycontextmenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) sollte die Steuerung an die Shell zurückgeben, ohne das Menü zu ändern.</span><span class="sxs-lookup"><span data-stu-id="5fc99-167">[**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) should return control to the Shell without modifying the menu.</span></span> |
| <span data-ttu-id="5fc99-168">CMF- \_ NODEFAULT</span><span class="sxs-lookup"><span data-stu-id="5fc99-168">CMF\_NODEFAULT</span></span>   | <span data-ttu-id="5fc99-169">Kein Element im Menü sollte das Standardelement sein.</span><span class="sxs-lookup"><span data-stu-id="5fc99-169">No item in the menu should be the default item.</span></span> <span data-ttu-id="5fc99-170">Die-Methode sollte Ihre Befehle dem Menü hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="5fc99-170">The method should add its commands to the menu.</span></span>                                                                                                                          |
| <span data-ttu-id="5fc99-171">CMF \_ Normal</span><span class="sxs-lookup"><span data-stu-id="5fc99-171">CMF\_NORMAL</span></span>      | <span data-ttu-id="5fc99-172">Das Kontextmenü wird normal angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5fc99-172">The shortcut menu will be displayed normally.</span></span> <span data-ttu-id="5fc99-173">Die-Methode sollte Ihre Befehle dem Menü hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="5fc99-173">The method should add its commands to the menu.</span></span>                                                                                                                            |



 

<span data-ttu-id="5fc99-174">Verwenden Sie entweder [**InsertMenu**](/windows/win32/api/winuser/nf-winuser-insertmenua) oder [**InsertMenuItem**](/windows/win32/api/winuser/nf-winuser-insertmenuitema) , um der Liste Menü Elemente hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="5fc99-174">Use either [**InsertMenu**](/windows/win32/api/winuser/nf-winuser-insertmenua) or [**InsertMenuItem**](/windows/win32/api/winuser/nf-winuser-insertmenuitema) to add menu items to the list.</span></span> <span data-ttu-id="5fc99-175">Geben Sie anschließend einen **HRESULT** -Wert mit dem Schweregrad \_ Success an.</span><span class="sxs-lookup"><span data-stu-id="5fc99-175">Then return an **HRESULT** value with the severity set to SEVERITY\_SUCCESS.</span></span> <span data-ttu-id="5fc99-176">Legen Sie den Codewert auf den Offset des größten Befehls Bezeichners fest, der zugewiesen wurde, plus eins (1).</span><span class="sxs-lookup"><span data-stu-id="5fc99-176">Set the code value to the offset of the largest command identifier that was assigned, plus one (1).</span></span> <span data-ttu-id="5fc99-177">Nehmen Sie beispielsweise an, dass *idcmdfirst* auf 5 festgelegt ist und Sie dem Menü drei Elemente mit den Befehls bezeichlern 5, 7 und 8 hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="5fc99-177">For example, assume that *idCmdFirst* is set to 5 and you add three items to the menu with command identifiers of 5, 7, and 8.</span></span> <span data-ttu-id="5fc99-178">Der Rückgabewert muss \_ HRESULT lauten (Schweregrad \_ Success, 0, 8 + 1).</span><span class="sxs-lookup"><span data-stu-id="5fc99-178">The return value should be MAKE\_HRESULT(SEVERITY\_SUCCESS, 0, 8 + 1).</span></span>

<span data-ttu-id="5fc99-179">Das folgende Beispiel zeigt eine einfache Implementierung von [**querycontextmenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) , die einen einzelnen Befehl einfügt.</span><span class="sxs-lookup"><span data-stu-id="5fc99-179">The following example shows a simple implementation of [**QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) that inserts a single command.</span></span> <span data-ttu-id="5fc99-180">Der bezeichneroffset für den Befehl ist die IDM- \_ Anzeige, die auf 0 (null) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="5fc99-180">The identifier offset for the command is IDM\_DISPLAY, which is set to zero.</span></span> <span data-ttu-id="5fc99-181">Die Variablen **m \_ pszverb** und **m \_ pwszverb** sind private Variablen, die zum Speichern der zugeordneten sprachunabhängigen Verb Zeichenfolge im ANSI-und Unicode-Format verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5fc99-181">The **m\_pszVerb** and **m\_pwszVerb** variables are private variables that are used to store the associated language-independent verb string in both ANSI and Unicode formats.</span></span>


```
#define IDM_DISPLAY 0

STDMETHODIMP CMenuExtension::QueryContextMenu(HMENU hMenu,
                                              UINT indexMenu,
                                              UINT idCmdFirst,
                                              UINT idCmdLast,
                                              UINT uFlags)
{
    HRESULT hr;
    
    if(!(CMF_DEFAULTONLY & uFlags))
    {
        InsertMenu(hMenu, 
                   indexMenu, 
                   MF_STRING | MF_BYPOSITION, 
                   idCmdFirst + IDM_DISPLAY, 
                   "&Display File Name");

    
        
        hr = StringCbCopyA(m_pszVerb, sizeof(m_pszVerb), "display");
        hr = StringCbCopyW(m_pwszVerb, sizeof(m_pwszVerb), L"display");

        return MAKE_HRESULT(SEVERITY_SUCCESS, 0, USHORT(IDM_DISPLAY + 1));
    }

    return MAKE_HRESULT(SEVERITY_SUCCESS, 0, USHORT(0));}
```



## <a name="remarks"></a><span data-ttu-id="5fc99-182">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5fc99-182">Remarks</span></span>

<span data-ttu-id="5fc99-183">Informationen zu anderen Verb Implementierungsaufgaben finden Sie unter Erstellen von Kontext [Menü Handlern](context-menu-handlers.md).</span><span class="sxs-lookup"><span data-stu-id="5fc99-183">For other verb implementation tasks, see [Creating Shortcut Menu Handlers](context-menu-handlers.md).</span></span>

 

 
