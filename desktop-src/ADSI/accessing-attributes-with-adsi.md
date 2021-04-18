---
title: Zugreifen auf Attribute mit ADSI
description: Die IADs. Get-Methode und die IADs. Getex-Methode werden verwendet, um benannte Attributwerte abzurufen.
ms.assetid: 8aa139e1-6b20-4745-92f1-d2f352071f33
ms.tgt_platform: multiple
keywords:
- Attribute, zugreifen mit ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4ee6990483b45e335bb6b830cef85e482f30e00
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "106337252"
---
# <a name="accessing-attributes-with-adsi"></a><span data-ttu-id="6b683-104">Zugreifen auf Attribute mit ADSI</span><span class="sxs-lookup"><span data-stu-id="6b683-104">Accessing Attributes with ADSI</span></span>

<span data-ttu-id="6b683-105">Die [**IADs. Get**](/windows/desktop/api/Iads/nf-iads-iads-get) -Methode und die [**IADs. Getex**](/windows/desktop/api/Iads/nf-iads-iads-getex) -Methode werden verwendet, um benannte Attributwerte abzurufen.</span><span class="sxs-lookup"><span data-stu-id="6b683-105">The [**IADs.Get**](/windows/desktop/api/Iads/nf-iads-iads-get) and [**IADs.GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) methods are used to retrieve named attribute values.</span></span> <span data-ttu-id="6b683-106">Beide Methoden geben einen [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="6b683-106">Both methods return a [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) value.</span></span> <span data-ttu-id="6b683-107">Diese Methoden sind nur für Verzeichnisse verfügbar, die ein Schema unterstützen.</span><span class="sxs-lookup"><span data-stu-id="6b683-107">These methods are available only for directories that support a schema.</span></span> <span data-ttu-id="6b683-108">Beim Zugriff auf Objekte in einem Verzeichnis ohne Schema müssen die Schnittstellen [**iadspropertyentry**](/windows/desktop/api/Iads/nn-iads-iadspropertyentry) und [**iadspropertyvalue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue) verwendet werden, um Attributwerte zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="6b683-108">When accessing objects in a directory without a schema, the [**IADsPropertyEntry**](/windows/desktop/api/Iads/nn-iads-iadspropertyentry) and [**IADsPropertyValue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue) interfaces must be used to manipulate attribute values.</span></span>

<span data-ttu-id="6b683-109">Die Methoden [**IADs. Get**](/windows/desktop/api/Iads/nf-iads-iads-get) und [**IADs. Getex**](/windows/desktop/api/Iads/nf-iads-iads-getex) geben eine [**Variante**](/windows/win32/api/oaidl/ns-oaidl-variant) zurück, die abhängig von der Anzahl der vom Server zurückgegebenen Werte ein **Variant** -Array sein kann oder nicht.</span><span class="sxs-lookup"><span data-stu-id="6b683-109">The [**IADs.Get**](/windows/desktop/api/Iads/nf-iads-iads-get) and [**IADs.GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) methods return a [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) which may, or may not, be a **VARIANT** array depending on the number of values returned by the server.</span></span> <span data-ttu-id="6b683-110">Wenn z. b. nur ein Wert vom Server zurückgegeben wird, unabhängig davon, ob es sich um ein einzelnes oder mehr wertiges Attribut handelt, gibt die Methode eine einzelne **Variante** zurück.</span><span class="sxs-lookup"><span data-stu-id="6b683-110">For example, if only one value is returned from the server, regardless of whether it is a single or multi-valued attribute, the method returns a single **VARIANT**.</span></span> <span data-ttu-id="6b683-111">Umgekehrt wird ein **Variant** -Array zurückgegeben, wenn mehrere Werte zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="6b683-111">Conversely, if multiple values are returned, a **VARIANT** array is returned.</span></span> <span data-ttu-id="6b683-112">Wenn ein **Variant** -Array zurückgegeben wird, enthält das **VT** -Element der **Variant** -Struktur die " **VT \_ Variant/vbVariant** "-und " **VT \_ Array/VBArray** "-Flags.</span><span class="sxs-lookup"><span data-stu-id="6b683-112">If a **VARIANT** array is returned, the **vt** member of the **VARIANT** structure contains the **VT\_VARIANT/vbVariant** and **VT\_ARRAY/vbArray** flags.</span></span>

<span data-ttu-id="6b683-113">Die [**IADs. Get**](/windows/desktop/api/Iads/nf-iads-iads-get) -Methode und die [**IADs. Getex**](/windows/desktop/api/Iads/nf-iads-iads-getex) -Methode können mithilfe der [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle auch ein COM-Objekt zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="6b683-113">The [**IADs.Get**](/windows/desktop/api/Iads/nf-iads-iads-get) and [**IADs.GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) methods can also return a COM object using the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="6b683-114">In diesem Fall enthält das **VT** -Element der [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) -Struktur das **VT \_ Dispatch/vbObject-** Flag.</span><span class="sxs-lookup"><span data-stu-id="6b683-114">In this case, the **vt** member of the [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) structure contains the **VT\_DISPATCH/vbObject** flag.</span></span> <span data-ttu-id="6b683-115">Um auf das COM-Objekt zuzugreifen, rufen Sie die [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) -Methode für die **IDispatch** -Schnittstelle auf, um die gewünschte Schnittstelle abzurufen.</span><span class="sxs-lookup"><span data-stu-id="6b683-115">To access the COM object, call the [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method on the **IDispatch** interface to obtain the desired interface.</span></span>

<span data-ttu-id="6b683-116">Ein anderer Datentyp, der von [**IADs. Get**](/windows/desktop/api/Iads/nf-iads-iads-get) -und [**IADs. Getex**](/windows/desktop/api/Iads/nf-iads-iads-getex) -Methoden zurückgegeben wird, sind binäre Daten.</span><span class="sxs-lookup"><span data-stu-id="6b683-116">Another data type returned by the [**IADs.Get**](/windows/desktop/api/Iads/nf-iads-iads-get) and [**IADs.GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) methods is binary data.</span></span> <span data-ttu-id="6b683-117">In diesem Fall werden die Daten als zusammenhängendes Bytearray bereitgestellt, und der **VT** -Member der [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) -Struktur enthält die **VT \_ UI1/vbByte** -und **VT \_ Array/VBArray** -Flags.</span><span class="sxs-lookup"><span data-stu-id="6b683-117">In this case, the data is supplied as a contiguous array of bytes and the **vt** member of the [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) structure will contain the **VT\_UI1/vbByte** and **VT\_ARRAY/vbArray** flags.</span></span>

> [!Note]  
> <span data-ttu-id="6b683-118">Microsoft Visual Basic, die Skript Edition unterstützt nur [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) -und **Variant** -Arrays.</span><span class="sxs-lookup"><span data-stu-id="6b683-118">Microsoft Visual Basic, Scripting Edition only supports [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) and **VARIANT** arrays.</span></span> <span data-ttu-id="6b683-119">Daher kann VBScript nicht zum Lesen von binären Eigenschafts Werten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6b683-119">Because of this, VBScript cannot be used to read binary property values.</span></span>

 

<span data-ttu-id="6b683-120">Viele ADSI-Schnittstellen definieren Schnittstellen spezifische Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="6b683-120">Many ADSI interfaces define interface-specific properties.</span></span> <span data-ttu-id="6b683-121">Die Schnittstelle [**iadscomputer**](/windows/desktop/api/Iads/nn-iads-iadscomputer) definiert z. b. die [**Location**](iadscomputer-property-methods.md) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="6b683-121">For example, the [**IADsComputer**](/windows/desktop/api/Iads/nn-iads-iadscomputer) interface defines the [**Location**](iadscomputer-property-methods.md) property.</span></span> <span data-ttu-id="6b683-122">Diese Schnittstellen definierten Eigenschaften können Daten enthalten, die mit einem der benannten Attribute identisch sind, aber die Eigenschaften sind spezifisch für den Objekttyp, auf den sich die Schnittstelle bezieht.</span><span class="sxs-lookup"><span data-stu-id="6b683-122">These interface-defined properties may contain data that is identical to one of the named attributes, but the properties are specific to the type of object the interface refers to.</span></span> <span data-ttu-id="6b683-123">In Sprachen, die Automation unterstützen, kann auf diese Schnittstellen definierten Eigenschaften mithilfe der Punkt Notation zugegriffen werden, wie im folgenden Codebeispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="6b683-123">In languages that support automation, these interface-defined properties can be accessed using the dot notation as shown in the following code example.</span></span>

## <a name="examples"></a><span data-ttu-id="6b683-124">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6b683-124">Examples</span></span>

<span data-ttu-id="6b683-125">Im folgenden Codebeispiel wird gezeigt, wie auf die ADsPath-Eigenschaft der IADs-Schnittstelle zugegriffen wird.</span><span class="sxs-lookup"><span data-stu-id="6b683-125">The following code example shows how to access the ADsPath property on the IADs interface.</span></span>


```VB
Dim oUser as IADs
Dim Path as String
 
' Bind to a specific user object.
set oUser = GetObject(
            "LDAP://CN=Jeff Smith,CN=Users,DC=fabrikam,DC=com")
 
' Get property.
Path = MyUser.ADsPath
```



<span data-ttu-id="6b683-126">In Sprachen, die nicht automatisiert werden, müssen die Eigenschaften Zugriffsmethoden für den Zugriff auf die Schnittstellen definierten Eigenschaften verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6b683-126">In non-automation languages, the property access methods must be used to access the interface-defined properties.</span></span> <span data-ttu-id="6b683-127">Beispielsweise wird die [**iadscomputer:: get \_ Location**](iadscomputer-property-methods.md) -Methode zum Abrufen der **iadscomputer. Location** -Eigenschaft verwendet.</span><span class="sxs-lookup"><span data-stu-id="6b683-127">For example, the [**IADsComputer::get\_Location**](iadscomputer-property-methods.md) method is used to retrieve the **IADsComputer.Location** property.</span></span>

<span data-ttu-id="6b683-128">Im folgenden C++-Codebeispiel wird veranschaulicht, wie die-Eigenschaften Zugriffsmethode in C++ verwendet wird, um den ADsPath eines Benutzers abzurufen.</span><span class="sxs-lookup"><span data-stu-id="6b683-128">The following C++ code example demonstrates how to use the property access method in C++ to retrieve the ADsPath of a user.</span></span>


```C++
HRESULT hr;
IADs *pUser; 
 
// Bind to user object.
hr = ADsGetObject(
     L"LDAP://CN=Jeff Smith,CN=Users,DC=fabrikam,DC=com", 
     IID_IADs, 
     (void**)&pUser);
if(SUCCEEDED(hr)) 
{
    BSTR bstrName;

    // Get property.
    hr = pUser->get_Name(&bstrName);
    if(SUCCEEDED(hr)) 
    {
        wprintf(bstrName);
 
        SysFreeString(bstrName);
    }

    pUser->Release();
}
```



<span data-ttu-id="6b683-129">Weitere Informationen zum Zugreifen auf Attribute mit ADSI finden Sie unter:</span><span class="sxs-lookup"><span data-stu-id="6b683-129">For more information about accessing attributes with ADSI, see:</span></span>

-   [<span data-ttu-id="6b683-130">Die Get-Methode</span><span class="sxs-lookup"><span data-stu-id="6b683-130">The Get Method</span></span>](the-get-method.md)
-   [<span data-ttu-id="6b683-131">Die Getex-Methode</span><span class="sxs-lookup"><span data-stu-id="6b683-131">The GetEx Method</span></span>](the-getex-method.md)
-   [<span data-ttu-id="6b683-132">Die GetInfo-Methode</span><span class="sxs-lookup"><span data-stu-id="6b683-132">The GetInfo Method</span></span>](the-getinfo-method.md)
-   [<span data-ttu-id="6b683-133">Optimierung mithilfe von "GetInfoEx"</span><span class="sxs-lookup"><span data-stu-id="6b683-133">Optimization Using GetInfoEx</span></span>](optimization-using-getinfoex.md)
-   [<span data-ttu-id="6b683-134">Zugreifen auf Attribute mit der IDirectoryObject-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="6b683-134">Accessing Attributes with the IDirectoryObject Interface</span></span>](accessing-attributes-with-the-idirectoryobject-interface.md)
-   [<span data-ttu-id="6b683-135">Beispiel Code zum Lesen von Attributen</span><span class="sxs-lookup"><span data-stu-id="6b683-135">Example Code for Reading Attributes</span></span>](example-code-for-reading-attributes.md)

 

 