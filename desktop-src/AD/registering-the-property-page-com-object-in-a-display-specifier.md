---
title: Registrieren des COM-Objekts der Eigenschaften Seite in einem Anzeigespezifizierer
description: In diesem Thema wird gezeigt, wie Sie eine Erweiterungs-DLL registrieren, die eine Active Directory Eigenschaften Blatt mit der Windows-Registrierung und Active Directory enthält.
ms.assetid: e2d6142b-c2fe-4435-b4af-83f7cd45218b
ms.tgt_platform: multiple
keywords:
- Das COM-Objekt der Eigenschaften Seite wird in einem Anzeige Spezifizierer registriert Active Directory
- COM-Objekt Active Directory der Eigenschaften Seite, registrieren in einem Anzeigespezifizierer
- Anzeige spezifiker Active Directory, Registrieren des COM-Objekts der Eigenschaften Seite in
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c5b08ac0ea6329026a6d367e71064bde917b1a6
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104101427"
---
# <a name="registering-the-property-page-com-object-in-a-display-specifier"></a><span data-ttu-id="9c789-106">Registrieren des COM-Objekts der Eigenschaften Seite in einem Anzeigespezifizierer</span><span class="sxs-lookup"><span data-stu-id="9c789-106">Registering the Property Page COM Object in a Display Specifier</span></span>

<span data-ttu-id="9c789-107">Wenn Sie com verwenden, um eine Eigenschaften Blatt-Erweiterungs-DLL für Active Directory Domain Services zu erstellen, müssen Sie die Erweiterung auch bei der Windows-Registrierung und Active Directory Domain Services registrieren.</span><span class="sxs-lookup"><span data-stu-id="9c789-107">When you use COM to create a property sheet extension DLL for Active Directory Domain Services, you must also register the extension with the Windows registry and Active Directory Domain Services.</span></span> <span data-ttu-id="9c789-108">Durch die Registrierung der Erweiterung können die Active Directory Verwaltungs-MMC-Snap-Ins und die Windows-Shell die Erweiterung erkennen.</span><span class="sxs-lookup"><span data-stu-id="9c789-108">Registering the extension enables the Active Directory administrative MMC snap-ins and the Windows shell to recognize the extension.</span></span>

## <a name="registering-in-the-windows-registry"></a><span data-ttu-id="9c789-109">Registrieren in der Windows-Registrierung</span><span class="sxs-lookup"><span data-stu-id="9c789-109">Registering in the Windows Registry</span></span>

<span data-ttu-id="9c789-110">Wie alle com-Server muss eine Eigenschaften Blatt Erweiterung in der Windows-Registrierung registriert werden.</span><span class="sxs-lookup"><span data-stu-id="9c789-110">Like all COM servers, a property sheet extension must be registered in the Windows registry.</span></span> <span data-ttu-id="9c789-111">Die Erweiterung wird unter dem folgenden Schlüssel registriert.</span><span class="sxs-lookup"><span data-stu-id="9c789-111">The extension is registered under the following key.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      <clsid>
```

<span data-ttu-id="9c789-112">*<clsid>* die Zeichen folgen Darstellung der CLSID, die von der [**stringfromclsid**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) -Funktion erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="9c789-112">*<clsid>* is the string representation of the CLSID as produced by the [**StringFromCLSID**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) function.</span></span> <span data-ttu-id="9c789-113">Unter dem *<clsid>* Schlüssel gibt es einen **InProcServer32** -Schlüssel, der das-Objekt als 32-Bit-in-proc-Server identifiziert.</span><span class="sxs-lookup"><span data-stu-id="9c789-113">Under the *<clsid>* key, there is an **InProcServer32** key that identifies the object as a 32-bit in-proc server.</span></span> <span data-ttu-id="9c789-114">Unter der **InProcServer32** -Taste wird der Speicherort der dll im Standardwert angegeben, und das Threading Modell wird im **ThreadingModel** -Wert angegeben.</span><span class="sxs-lookup"><span data-stu-id="9c789-114">Under the **InProcServer32** key, the location of the DLL is specified in the default value and the threading model is specified in the **ThreadingModel** value.</span></span> <span data-ttu-id="9c789-115">Alle Eigenschaften Blatt Erweiterungen müssen das Threading Modell "Apartment" verwenden.</span><span class="sxs-lookup"><span data-stu-id="9c789-115">All property sheet extensions must use the "Apartment" threading model.</span></span>

## <a name="registering-with-active-directory-domain-services"></a><span data-ttu-id="9c789-116">Registrieren bei Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="9c789-116">Registering with Active Directory Domain Services</span></span>

<span data-ttu-id="9c789-117">Die Registrierung der Eigenschaften Blatt Erweiterung ist spezifisch für ein Gebiets Schema.</span><span class="sxs-lookup"><span data-stu-id="9c789-117">Property sheet extension registration is specific to one locale.</span></span> <span data-ttu-id="9c789-118">Wenn die Eigenschafts Blatt Erweiterung auf alle Gebiets Schemas angewendet wird, muss Sie in allen Gebiets Schema-subcontainern im Container "Display Specifiers" im Objektklasse " [**displaySpecifier**](/windows/desktop/ADSchema/c-displayspecifier) " registriert werden.</span><span class="sxs-lookup"><span data-stu-id="9c789-118">If the property sheet extension applies to all locales, it must be registered in the object class [**displaySpecifier**](/windows/desktop/ADSchema/c-displayspecifier) object in all of the locale subcontainers in the Display Specifiers container.</span></span> <span data-ttu-id="9c789-119">Wenn die Eigenschaften Blatt Erweiterung für ein bestimmtes Gebiets Schema lokalisiert wird, registrieren Sie Sie im **Display specifier** -Objekt in diesem Gebiets Schema-unter Container.</span><span class="sxs-lookup"><span data-stu-id="9c789-119">If the property sheet extension is localized for a certain locale, register it in the **displaySpecifier** object in that locale subcontainer.</span></span> <span data-ttu-id="9c789-120">Weitere Informationen über die Anzeige spezifischere Container und Gebiets Schemas finden Sie unter [Anzeigen von Bezeichner](display-specifiers.md) und [displaySpecifier-Containern](displayspecifiers-container.md).</span><span class="sxs-lookup"><span data-stu-id="9c789-120">For more information about the Display Specifiers container and locales, see [Display Specifiers](display-specifiers.md) and [DisplaySpecifiers Container](displayspecifiers-container.md).</span></span>

<span data-ttu-id="9c789-121">Es gibt drei anzeigespezifiziererattribute, unter denen eine Eigenschaften Blatt Erweiterung registriert werden kann.</span><span class="sxs-lookup"><span data-stu-id="9c789-121">There are three display specifier attributes that a property sheet extension can be registered under.</span></span> <span data-ttu-id="9c789-122">Dabei handelt es sich um [**adminPropertyPages**](/windows/desktop/ADSchema/a-adminpropertypages), [**shellpropertypages**](/windows/desktop/ADSchema/a-shellpropertypages)und [**adminmultiselectpropertypages**](/windows/desktop/ADSchema/a-adminmultiselectpropertypages).</span><span class="sxs-lookup"><span data-stu-id="9c789-122">These are [**adminPropertyPages**](/windows/desktop/ADSchema/a-adminpropertypages), [**shellPropertyPages**](/windows/desktop/ADSchema/a-shellpropertypages), and [**adminMultiselectPropertyPages**](/windows/desktop/ADSchema/a-adminmultiselectpropertypages).</span></span>

<span data-ttu-id="9c789-123">Das [**adminPropertyPages**](/windows/desktop/ADSchema/a-adminpropertypages) -Attribut identifiziert Verwaltungs Eigenschaften Seiten, die in Active Directory administrativen Snap-Ins angezeigt werden sollen. Die Eigenschaften Seite wird angezeigt, wenn der Benutzereigenschaften für Objekte der entsprechenden Klasse in einem der Active Directory Verwaltungs-MMC-Snap-Ins anzeigt.</span><span class="sxs-lookup"><span data-stu-id="9c789-123">The [**adminPropertyPages**](/windows/desktop/ADSchema/a-adminpropertypages) attribute identifies administrative property pages to display in Active Directory administrative snap-ins. The property page appears when the user views properties for objects of the appropriate class in one of the Active Directory administrative MMC snap-ins.</span></span>

<span data-ttu-id="9c789-124">Das [**shellpropertypages**](/windows/desktop/ADSchema/a-shellpropertypages) -Attribut identifiziert die Eigenschaften Seiten der Endbenutzer, die in der Windows-Shell angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="9c789-124">The [**shellPropertyPages**](/windows/desktop/ADSchema/a-shellpropertypages) attribute identifies end-user property pages to display in the Windows shell.</span></span> <span data-ttu-id="9c789-125">Die Eigenschaften Seite wird angezeigt, wenn der Benutzer die Eigenschaften für Objekte der entsprechenden Klasse im Windows-Explorer anzeigt.</span><span class="sxs-lookup"><span data-stu-id="9c789-125">The property page appears when the user views the properties for objects of the appropriate class in the Windows Explorer.</span></span> <span data-ttu-id="9c789-126">Ab den Windows Server 2003-Betriebssystemen werden von der Windows-Shell keine Objekte mehr aus Active Directory Domain Services angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9c789-126">Beginning with the Windows Server 2003 operating systems, the Windows shell no longer displays objects from Active Directory Domain Services.</span></span>

<span data-ttu-id="9c789-127">[**Adminmultiselectpropertypages**](/windows/desktop/ADSchema/a-adminmultiselectpropertypages) ist nur unter den Betriebssystemen Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="9c789-127">The [**adminMultiselectPropertyPages**](/windows/desktop/ADSchema/a-adminmultiselectpropertypages) is only available on the Windows Server 2003 operating systems.</span></span> <span data-ttu-id="9c789-128">Die Eigenschaften Seite wird angezeigt, wenn der Benutzer in einem der Active Directory-Verwaltungs-MMC-Snap-Ins Eigenschaften für mehr als ein Objekt der entsprechenden Klasse anzeigt.</span><span class="sxs-lookup"><span data-stu-id="9c789-128">The property page appears when the user views properties for more than one object of the appropriate class in one of the Active Directory administrative MMC snap-ins.</span></span>

<span data-ttu-id="9c789-129">Alle diese Attribute sind mehr wertig.</span><span class="sxs-lookup"><span data-stu-id="9c789-129">All of these attributes are multi-valued.</span></span>

<span data-ttu-id="9c789-130">Die Werte für die Attribute " [**adminPropertyPages**](/windows/desktop/ADSchema/a-adminpropertypages) " und " [**shellpropertypages**](/windows/desktop/ADSchema/a-shellpropertypages) " erfordern das folgende Format.</span><span class="sxs-lookup"><span data-stu-id="9c789-130">The values for the [**adminPropertyPages**](/windows/desktop/ADSchema/a-adminpropertypages) and [**shellPropertyPages**](/windows/desktop/ADSchema/a-shellpropertypages) attributes require the following format.</span></span>


```C++
<order number>,<clsid>,<optional data>
```



<span data-ttu-id="9c789-131">Die Werte für das [**adminmultiselectpropertypages**](/windows/desktop/ADSchema/a-adminmultiselectpropertypages) -Attribut erfordern das folgende Format.</span><span class="sxs-lookup"><span data-stu-id="9c789-131">The values for the [**adminMultiselectPropertyPages**](/windows/desktop/ADSchema/a-adminmultiselectpropertypages) attribute require the following format.</span></span>


```C++
<order number>,<clsid>
```



<span data-ttu-id="9c789-132">" &lt; Order Number &gt; " ist eine nicht signierte Zahl, die die Seitenposition im Blatt darstellt.</span><span class="sxs-lookup"><span data-stu-id="9c789-132">The "&lt;order number&gt;" is an unsigned number that represents the page position in the sheet.</span></span> <span data-ttu-id="9c789-133">Wenn ein Eigenschaften Blatt angezeigt wird, werden die Werte mithilfe eines Vergleichs der "Order Number"-Werte der einzelnen Werte sortiert &lt; &gt; .</span><span class="sxs-lookup"><span data-stu-id="9c789-133">When a property sheet is displayed, the values are sorted using a comparison of each value's "&lt;order number&gt;".</span></span> <span data-ttu-id="9c789-134">Wenn mehr als ein Wert dieselbe " &lt; Bestellnummer" aufweist &gt; , werden diese COM-Objekte der Eigenschaften Seite in der Reihenfolge geladen, in der Sie vom Active Directory Server gelesen werden.</span><span class="sxs-lookup"><span data-stu-id="9c789-134">If more than one value has the same "&lt;order number&gt;", those property page COM objects are loaded in the order they are read from the Active Directory server.</span></span> <span data-ttu-id="9c789-135">Wenn möglich, sollten Sie eine nicht vorhandene " &lt; Bestellnummer" verwenden, &gt; d. h. eine, die nicht von anderen Werten in der-Eigenschaft verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9c789-135">If possible, you should use a non-existing "&lt;order number&gt;"; that is, one not used by other values in the property.</span></span> <span data-ttu-id="9c789-136">Es gibt keine vorgeschriebene Anfangsposition, und Lücken sind in der Sequenz " &lt; Order Number &gt; " zulässig.</span><span class="sxs-lookup"><span data-stu-id="9c789-136">There is no prescribed starting position, and gaps are allowed in the "&lt;order number&gt;" sequence.</span></span>

<span data-ttu-id="9c789-137">Die " &lt; CLSID &gt; " ist die Zeichen folgen Darstellung der CLSID, die von der [**stringfromclsid**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) -Funktion erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="9c789-137">The "&lt;clsid&gt;" is the string representation of the CLSID as produced by the [**StringFromCLSID**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) function.</span></span>

<span data-ttu-id="9c789-138">" &lt; Optionale Daten &gt; " ist ein Zeichen folgen Wert, der nicht erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="9c789-138">The "&lt;optional data&gt;" is a string value that is not required.</span></span> <span data-ttu-id="9c789-139">Dieser Wert kann durch das COM-Objekt der Eigenschaften Seite abgerufen werden, indem der [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) -Zeiger an die zugehörige [**ishellextinit:: Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) -Methode weitergegeben wird.</span><span class="sxs-lookup"><span data-stu-id="9c789-139">This value can be retrieved by the property page COM object using the [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) pointer passed to its [**IShellExtInit::Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) method.</span></span> <span data-ttu-id="9c789-140">Das COM-Objekt der Eigenschaften Seite erhält diese Daten durch Aufrufen von [**IDataObject:: GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) mit dem Zwischenablage Format [**cfstr \_ dspropertypageinfo**](cfstr-dspropertypageinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="9c789-140">The property page COM object obtains this data by calling [**IDataObject::GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) with the [**CFSTR\_DSPROPERTYPAGEINFO**](cfstr-dspropertypageinfo.md) clipboard format.</span></span> <span data-ttu-id="9c789-141">Dadurch wird ein **HGLOBAL** bereitstellt, das eine [**dspropertypageinfo**](/windows/desktop/api/Dsclient/ns-dsclient-dspropertypageinfo) -Struktur enthält. die **dspropertypageinfo** -Struktur enthält eine Unicode-Zeichenfolge, die die " &lt; optionalen Daten &gt; " enthält.</span><span class="sxs-lookup"><span data-stu-id="9c789-141">This provides an **HGLOBAL** that contains a [**DSPROPERTYPAGEINFO**](/windows/desktop/api/Dsclient/ns-dsclient-dspropertypageinfo) structure The **DSPROPERTYPAGEINFO** structure contains a Unicode string that contains the "&lt;optional data&gt;".</span></span> <span data-ttu-id="9c789-142">Die " &lt; optionalen Daten &gt; " sind mit dem Attribut " [**adminmultiselectpropertypages**](/windows/desktop/ADSchema/a-adminmultiselectpropertypages) " nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="9c789-142">The "&lt;optional data&gt;" is not allowed with the [**adminMultiselectPropertyPages**](/windows/desktop/ADSchema/a-adminmultiselectpropertypages) attribute.</span></span> <span data-ttu-id="9c789-143">Im folgenden C/C++-Codebeispiel wird gezeigt, wie die " &lt; optionalen Daten" abgerufen werden &gt; .</span><span class="sxs-lookup"><span data-stu-id="9c789-143">The following C/C++ code example shows how to retrieve the "&lt;optional data&gt;".</span></span>


```C++
fe.cfFormat = RegisterClipboardFormat(CFSTR_DSPROPERTYPAGEINFO);
fe.ptd = NULL;
fe.dwAspect = DVASPECT_CONTENT;
fe.lindex = -1;
fe.tymed = TYMED_HGLOBAL;
hr = pDataObj->GetData(&fe, &stm);
if(SUCCEEDED(hr))
{
    DSPROPERTYPAGEINFO *pPageInfo;
    
    pPageInfo = (DSPROPERTYPAGEINFO*)GlobalLock(stm.hGlobal);
    if(pPageInfo)
    {
        LPWSTR  pwszData;

        pwszData = (LPWSTR)((LPBYTE)pPageInfo + pPageInfo->offsetString);
        pwszData = NULL;
        
        GlobalUnlock(stm.hGlobal);
    }

    ReleaseStgMedium(&stm);
}
```



<span data-ttu-id="9c789-144">Eine Eigenschaften Blatt Erweiterung kann mehr als eine Eigenschaften Seite implementieren. eine mögliche Verwendung der " &lt; optionalen Daten &gt; " besteht darin, die Seiten für die Anzeige zu benennen.</span><span class="sxs-lookup"><span data-stu-id="9c789-144">A property sheet extension can implement more than one property page; one possible use of the "&lt;optional data&gt;" is to name the pages to display.</span></span> <span data-ttu-id="9c789-145">Dies bietet die Flexibilität, mehrere COM-Objekte, eine für jede Seite oder ein einzelnes COM-Objekt zu implementieren, um mehrere Seiten zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="9c789-145">This provides the flexibility of choosing to implement multiple COM objects, one for each page, or a single COM object to handle multiple pages.</span></span>

<span data-ttu-id="9c789-146">Das folgende Codebeispiel ist ein Beispiel Wert, der für die Attribute [**adminPropertyPages**](/windows/desktop/ADSchema/a-adminpropertypages), [**shellpropertypages**](/windows/desktop/ADSchema/a-shellpropertypages)oder [**adminmultiselectpropertypages**](/windows/desktop/ADSchema/a-adminmultiselectpropertypages) verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="9c789-146">The following code example is an example value that can be used for the [**adminPropertyPages**](/windows/desktop/ADSchema/a-adminpropertypages), [**shellPropertyPages**](/windows/desktop/ADSchema/a-shellpropertypages), or [**adminMultiselectPropertyPages**](/windows/desktop/ADSchema/a-adminmultiselectpropertypages) attributes.</span></span>


```C++
1,{6dfe6485-a212-11d0-bcd5-00c04fd8d5b6}
```



> [!IMPORTANT]
> <span data-ttu-id="9c789-147">Bei der Windows-Shell werden Anzeige spezifiziererdaten bei der Benutzeranmeldung abgerufen und für die Benutzersitzung zwischengespeichert.</span><span class="sxs-lookup"><span data-stu-id="9c789-147">For the Windows shell, display specifier data is retrieved at user logon, and cached for the user session.</span></span> <span data-ttu-id="9c789-148">Bei administrativen Snap-Ins werden die Anzeige spezifiziererdaten abgerufen, wenn das Snap-In geladen wird. Sie werden für die Lebensdauer des Prozesses zwischengespeichert.</span><span class="sxs-lookup"><span data-stu-id="9c789-148">For administrative snap-ins, the display specifier data is retrieved when the snap-in is loaded, and is cached for the lifetime of the process.</span></span> <span data-ttu-id="9c789-149">Bei der Windows-Shell bedeutet dies, dass Änderungen an Anzeige spezifiken wirksam werden, nachdem ein Benutzer sich abmeldet und sich dann erneut anmeldet.</span><span class="sxs-lookup"><span data-stu-id="9c789-149">For the Windows shell, this indicates that changes to display specifiers take effect after a user logs off and then logs on again.</span></span> <span data-ttu-id="9c789-150">Bei den administrativen Snap-Ins werden die Änderungen wirksam, wenn das Snap-in oder die Konsolen Datei geladen wird.</span><span class="sxs-lookup"><span data-stu-id="9c789-150">For the administrative snap-ins, changes take effect when the snap-in or console file is loaded.</span></span>

 

## <a name="adding-a-value-to-the-property-sheet-extension-attributes"></a><span data-ttu-id="9c789-151">Hinzufügen eines Werts zu den Eigenschaften Blatt-Erweiterungs Attributen</span><span class="sxs-lookup"><span data-stu-id="9c789-151">Adding a Value to the Property Sheet Extension Attributes</span></span>

<span data-ttu-id="9c789-152">Im folgenden Verfahren wird beschrieben, wie Sie eine Eigenschaften Blatt Erweiterung unter einem der Eigenschaften Blatt-Erweiterungs Attribute registrieren.</span><span class="sxs-lookup"><span data-stu-id="9c789-152">The following procedure describes how to register a property sheet extension under one of the property sheet extension attributes.</span></span>

<span data-ttu-id="9c789-153">**Registrieren einer Eigenschaften Blatt Erweiterung unter einem der Eigenschaften Blatt-Erweiterungs Attribute**</span><span class="sxs-lookup"><span data-stu-id="9c789-153">**Registering a property sheet extension under one of the property sheet extension attributes**</span></span>

1.  <span data-ttu-id="9c789-154">Stellen Sie sicher, dass die Erweiterung nicht bereits in den Attributwerten vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="9c789-154">Ensure that the extension does not already exist in the attribute values.</span></span>
2.  <span data-ttu-id="9c789-155">Fügen Sie den neuen Wert am Ende der Bestellliste der Eigenschaften Seite hinzu.</span><span class="sxs-lookup"><span data-stu-id="9c789-155">Add the new value at the end of the property page ordering list.</span></span> <span data-ttu-id="9c789-156">Dies ist der " &lt; Order Number &gt; "-Teil des Attribut Werts auf den nächsten Wert nach der höchsten vorhandenen Bestellnummer festgelegt.</span><span class="sxs-lookup"><span data-stu-id="9c789-156">That is set the "&lt;order number&gt;" portion of the attribute value to the next value after the highest existing order number.</span></span>
3.  <span data-ttu-id="9c789-157">Die [**IADs::P utex**](/windows/desktop/api/iads/nf-iads-iads-putex) -Methode wird verwendet, um dem Attribut den neuen Wert hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="9c789-157">The [**IADs::PutEx**](/windows/desktop/api/iads/nf-iads-iads-putex) method is used to add the new value to the attribute.</span></span> <span data-ttu-id="9c789-158">Der Parameter " *lncontrolcode* " muss auf die Anzeige **Eigenschaft " \_ \_ Append** " festgelegt werden, damit der neue Wert an die vorhandenen Werte angehängt wird und die vorhandenen Werte daher nicht überschreibt.</span><span class="sxs-lookup"><span data-stu-id="9c789-158">The *lnControlCode* parameter must be set to **ADS\_PROPERTY\_APPEND** so that the new value is appended to the existing values and does not, therefore, overwrite the existing values.</span></span> <span data-ttu-id="9c789-159">Die [**IADs::**](/windows/desktop/api/iads/nf-iads-iads-setinfo) \*-Methode muss nachträglich aufgerufen werden, um die Änderung in das Verzeichnis zu übertragen.</span><span class="sxs-lookup"><span data-stu-id="9c789-159">The [**IADs::SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) method must be called afterward to commit the change to the directory.</span></span>

<span data-ttu-id="9c789-160">Beachten Sie, dass die gleiche Eigenschaften Blatt Erweiterung für mehr als eine Objektklasse registriert werden kann.</span><span class="sxs-lookup"><span data-stu-id="9c789-160">Be aware that the same property sheet extension can be registered for more than one object class.</span></span>

<span data-ttu-id="9c789-161">Die [**IADs::P utex**](/windows/desktop/api/iads/nf-iads-iads-putex) -Methode wird verwendet, um dem Attribut den neuen Wert hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="9c789-161">The [**IADs::PutEx**](/windows/desktop/api/iads/nf-iads-iads-putex) method is used to add the new value to the attribute.</span></span> <span data-ttu-id="9c789-162">Der Parameter " *lncontrolcode* " muss auf die **ADS-Eigenschaft " \_ \_ Append**" festgelegt werden, sodass der neue Wert an die vorhandenen Werte angehängt wird und die vorhandenen Werte daher nicht überschreibt.</span><span class="sxs-lookup"><span data-stu-id="9c789-162">The *lnControlCode* parameter must be set to **ADS\_PROPERTY\_APPEND**, so that the new value is appended to the existing values and does not, therefore, overwrite the existing values.</span></span> <span data-ttu-id="9c789-163">Die [**IADs::**](/windows/desktop/api/iads/nf-iads-iads-setinfo) \*-Methode muss nach aufgerufen werden, um die Änderung in das Verzeichnis zu übertragen.</span><span class="sxs-lookup"><span data-stu-id="9c789-163">The [**IADs::SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) method must be called after to commit the change to the directory.</span></span>

<span data-ttu-id="9c789-164">Im folgenden Codebeispiel wird der Group-Klasse im Standard Gebiets Schema des Computers eine Eigenschaften Blatt Erweiterung hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="9c789-164">The following code example adds a property sheet extension to the group class in the computer's default locale.</span></span> <span data-ttu-id="9c789-165">Beachten Sie, dass die **addpropertypagededisplayspecifier** -Funktion die CLSID der Eigenschafts Blatt Erweiterung in den vorhandenen Werten überprüft, die höchste Bestellnummer abruft und den Wert für die Eigenschaften Seite mithilfe von [**IADs::P utex**](/windows/desktop/api/iads/nf-iads-iads-putex) mit der **ADS- \_ Eigenschaft \_ Append** -Steuerungs Code hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="9c789-165">Be aware that the **AddPropertyPageToDisplaySpecifier** function verifies the property sheet extension CLSID in the existing values, gets the highest order number, and adds the value for the property page using [**IADs::PutEx**](/windows/desktop/api/iads/nf-iads-iads-putex) with the **ADS\_PROPERTY\_APPEND** control code.</span></span>


```C++
//  Add msvcrt.dll to the project.
//  Add activeds.lib to the project.
//  Add adsiid.lib to the project.

#include "stdafx.h"
#include <wchar.h>
#include <objbase.h>
#include <activeds.h>
#include "atlbase.h"

HRESULT AddPropertyPageToDisplaySpecifier(LPOLESTR szClassName, //  ldapDisplayName of the class.
                                          CLSID *pPropPageCLSID //  CLSID of property page COM object.
                                         );

HRESULT BindToDisplaySpecifiersContainerByLocale(LCID *locale,
                                                 IADsContainer **ppDispSpecCont
                                                 );

HRESULT GetDisplaySpecifier(IADsContainer *pContainer, LPOLESTR szDispSpec, IADs **ppObject);

//  Entry point for the application.
void wmain(int argc, wchar_t *argv[ ])
{

    wprintf(L"This program adds a sample property page to the display specifier for group class in the local computer's default locale.\n");

    // Initialize COM.
    CoInitialize(NULL);
    HRESULT hr = S_OK;

    //  Class ID for the sample property page.
    LPOLESTR szCLSID = L"{D9FCE809-8A10-11d2-A7E7-00C04F79DC0F}";
    LPOLESTR szClass = L"group";
    CLSID clsid;
    //  Convert to GUID.
    hr = CLSIDFromString(
        szCLSID,  //  Pointer to the string representation of the CLSID.
        &clsid    //  Pointer to the CLSID.
        );

    hr = AddPropertyPageToDisplaySpecifier(szClass, //  ldapDisplayName of the class.
                                           &clsid //  CLSID of property page COM object.
                                          );
    if (S_OK == hr)
        wprintf(L"Property page registered successfully\n");
    else if (S_FALSE == hr)
        wprintf(L"Property page was not added because it was already registered.\n");
    else
        wprintf(L"Property page was not added. HR: %x.\n");

    //  Uninitialize COM.
    CoUninitialize();
    return;
}

//  Adds a property page to Active Directory admin snap-ins.
HRESULT AddPropertyPageToDisplaySpecifier(LPOLESTR szClassName, //  ldapDisplayName of class.
                                          CLSID *pPropPageCLSID //  CLSID of property page COM object.
                                         )
{
    HRESULT hr = E_FAIL;
    IADsContainer *pContainer = NULL;
    LPOLESTR szDispSpec = new OLECHAR[MAX_PATH];
    IADs *pObject = NULL;
    VARIANT var;
    CComBSTR sbstrProperty = L"adminPropertyPages";
    LCID locale = NULL;
    //  Get the display specifier container using default system locale.
    //  When adding a property page COM object, specify the locale
    //  because the registration is locale-specific.
    //  This means if you created a property page
    //  for German, explicitly add it to the 407 container,
    //  so that it will be used when a computer is running with locale
    //  set to German and not the locale set on the
    //  computer where this application is running.
    hr = BindToDisplaySpecifiersContainerByLocale(&locale,
                                                  &pContainer
                                                 );
    //  Handle fail case where dispspec object
    //  is not found and give option to create one.

    if (SUCCEEDED(hr))
    {
        //  Bind to display specifier object for the specified class.
        //  Build the display specifier name.
#ifdef _MBCS
        wcscpy_s(szDispSpec, szClassName);
        wcscat_s(szDispSpec, L"-Display");
        hr = GetDisplaySpecifier(pContainer, szDispSpec, &pObject);
#endif _MBCS#endif _MBCS
        if (SUCCEEDED(hr))
        {
            //  Convert GUID to string.
            LPOLESTR szDSGUID = new WCHAR [39];
            ::StringFromGUID2(*pPropPageCLSID, szDSGUID, 39); 

            //  Get the adminPropertyPages property.
            hr = pObject->GetEx(sbstrProperty, &var);
            if (SUCCEEDED(hr))
            {
                LONG lstart, lend;
                SAFEARRAY *sa = V_ARRAY(&var);
                VARIANT varItem;
                //  Get the lower and upper bound.
                hr = SafeArrayGetLBound(sa, 1, &lstart);
                if (SUCCEEDED(hr))
                {
                    hr = SafeArrayGetUBound(sa, 1, &lend);
                }
                if (SUCCEEDED(hr))
                {
                    //  Iterate the values to verify if the prop page CLSID
                    //  is already registered.
                    VariantInit(&varItem);
                    BOOL bExists = FALSE;
                    UINT uiLastItem = 0;
                    UINT uiTemp = 0;
                    INT iOffset = 0;
                    LPOLESTR szMainStr = new OLECHAR[MAX_PATH];
                    LPOLESTR szItem = new OLECHAR[MAX_PATH];
                    LPOLESTR szStr = NULL;
                    for (long idx=lstart; idx <= lend; idx++)
                    {
                        hr = SafeArrayGetElement(sa, &idx, &varItem);
                        if (SUCCEEDED(hr))
                        {
#ifdef _MBCS
                            //  Verify that the specified CLSID is already registered.
                            wcscpy_s(szMainStr,varItem.bstrVal);
                            if (wcsstr(szMainStr,szDSGUID))
                                bExists = TRUE;
                            //  Get the index which is the number before the first comma.
                            szStr = wcschr(szMainStr, ',');
                            iOffset = (int)(szStr - szMainStr);
                            wcsncpy_s(szItem, szMainStr, iOffset);
                            szItem[iOffset]=0L;
                            uiTemp = _wtoi(szItem);
                            if (uiTemp > uiLastItem)
                                uiLastItem = uiTemp;
                            VariantClear(&varItem);
#endif _MBCS
                        }
                    }
                    //  If the CLSID is not registered, add it.
                    if (!bExists)
                    {
                        //  Build the value to add.
                        LPOLESTR szValue = new OLECHAR[MAX_PATH];
                        //  Next index to add at end of list.
#ifdef _MBCS
                        uiLastItem++;
                        _itow_s(uiLastItem, szValue, 10);   
                        wcscat_s(szValue,L",");
                        //  Add the class ID for the property page.
                        wcscat_s(szValue,szDSGUID);
                        wprintf(L"Value to add: %s\n", szValue);
#endif _MBCS

                        VARIANT varAdd;
                        //  Only one value to add
                        LPOLESTR pszAddStr[1];
                        pszAddStr[0]=szValue;
                        ADsBuildVarArrayStr(pszAddStr, 1, &varAdd);

                        hr = pObject->PutEx(ADS_PROPERTY_APPEND, sbstrProperty, varAdd);
                        if (SUCCEEDED(hr))
                        {
                            //  Commit the change.
                            hr = pObject->SetInfo();
                        }
                    }
                    else
                        hr = S_FALSE;
                }
            }
            VariantClear(&var);
        }
        if (pObject)
            pObject->Release();
    }

    return hr;
}

//  This function returns a pointer to the display specifier container 
//  for the specified locale.
//  If locale is NULL, use the default system locale and then return the locale in the locale param.
HRESULT BindToDisplaySpecifiersContainerByLocale(LCID *locale,
                                                 IADsContainer **ppDispSpecCont
                                                )
{
    HRESULT hr = E_FAIL;

    if ((!ppDispSpecCont)||(!locale))
        return E_POINTER;

    //  If no locale is specified, use the default system locale.
    if (!(*locale))
    {
        *locale = GetSystemDefaultLCID();
        if (!(*locale))
            return E_FAIL;
    }

    //  Verify that it is a valid locale.
    if (!IsValidLocale(*locale, LCID_SUPPORTED))
        return E_INVALIDARG;

    LPOLESTR szPath = new OLECHAR[MAX_PATH*2];
    IADs *pObj = NULL;
    VARIANT var;

    hr = ADsOpenObject(L"LDAP://rootDSE",
                       NULL,
                       NULL,
                       ADS_SECURE_AUTHENTICATION, // Use Secure Authentication.
                       IID_IADs,
                       (void**)&pObj);

    if (SUCCEEDED(hr))
    {
        //  Get the DN to the config container.
        hr = pObj->Get(CComBSTR("configurationNamingContext"), &var);
        if (SUCCEEDED(hr))
        {
#ifdef _MBCS
            //  Build the string to bind to the DisplaySpecifiers container.
            swprintf_s(szPath,L"LDAP://cn=%x,cn=DisplaySpecifiers,%s", *locale, var.bstrVal);
            //  Bind to the DisplaySpecifiers container.
            *ppDispSpecCont = NULL;
            hr = ADsOpenObject(szPath,
                               NULL,
                               NULL,
                               ADS_SECURE_AUTHENTICATION, // Use Secure Authentication.
                               IID_IADsContainer,
                               (void**)ppDispSpecCont);
#endif _MBCS

            if(FAILED(hr))
            {
                if (*ppDispSpecCont)
                {
                    (*ppDispSpecCont)->Release();
                    (*ppDispSpecCont) = NULL;
                }
            }
        }
    }
    //   Cleanup.
    VariantClear(&var);
    if (pObj)
        pObj->Release();

    return hr;
}

HRESULT GetDisplaySpecifier(IADsContainer *pContainer, LPOLESTR szDispSpec, IADs **ppObject)
{
    HRESULT hr = E_FAIL;
    CComBSTR sbstrDSPath;
    IDispatch *pDisp = NULL;

    if (!pContainer)
    {
        hr = E_POINTER;
        return hr;
    }

    //  Verify other pointers.
    //  Initialize the output pointer.
    (*ppObject) = NULL;

    //  Build relative path to the display specifier object.
    sbstrDSPath = "CN=";
    sbstrDSPath += szDispSpec;

    //  Use child object binding with IADsContainer::GetObject.
    hr = pContainer->GetObject(CComBSTR("displaySpecifier"),
        sbstrDSPath,
        &pDisp);
    if (SUCCEEDED(hr))
    {
        hr = pDisp->QueryInterface(IID_IADs, (void**)ppObject);
        if (FAILED(hr))
        {
            //  Clean up.
            if (*ppObject)
                (*ppObject)->Release();
        }
    }

    if (pDisp)
        pDisp->Release();

    return hr;

}
```



 

 