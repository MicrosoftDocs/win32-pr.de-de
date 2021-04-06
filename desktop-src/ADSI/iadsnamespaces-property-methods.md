---
title: Iadsnamespaces-Eigenschaften Methoden (IADs. h)
description: Die Eigenschaften Methoden der iadsnamespaces-Schnittstelle erhalten und legen die Eigenschaften fest, die in der folgenden Tabelle beschrieben werden. Weitere Informationen finden Sie unter Interface Property Methods.
ms.assetid: fe959741-429e-480a-8111-3ebadaf55f77
ms.tgt_platform: multiple
keywords:
- Iadsnamespaces-Eigenschaften Methoden ADSI
topic_type:
- apiref
api_name:
- IADsNamespaces Property Methods
- IADsNamespaces.DefaultContainer
- IADsNamespaces.get_DefaultContainer
- IADsNamespaces.put_DefaultContainer
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b30467e931d7e8790f9a17542d5da2070525fe0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742696"
---
# <a name="iadsnamespaces-property-methods"></a><span data-ttu-id="3ef53-105">Iadsnamespaces-Eigenschaften Methoden</span><span class="sxs-lookup"><span data-stu-id="3ef53-105">IADsNamespaces Property Methods</span></span>

<span data-ttu-id="3ef53-106">Die Eigenschaften Methoden der [**iadsnamespaces**](/windows/desktop/api/Iads/nn-iads-iadsnamespaces) -Schnittstelle erhalten und legen die Eigenschaften fest, die in der folgenden Tabelle beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="3ef53-106">The [**IADsNamespaces**](/windows/desktop/api/Iads/nn-iads-iadsnamespaces) interface property methods get and set the properties described in the following table.</span></span> <span data-ttu-id="3ef53-107">Weitere Informationen finden Sie unter [Interface Property Methods](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="3ef53-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="3ef53-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3ef53-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="3ef53-109">**DefaultContainer**</span><span class="sxs-lookup"><span data-stu-id="3ef53-109">**DefaultContainer**</span></span>
<span data-ttu-id="3ef53-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="3ef53-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="3ef53-111">Die **defaultcontainer** -Eigenschaft identifiziert ein Basis Container Objekt, das Sie binden und als Ausgangspunkt beim Durchsuchen verwenden können.</span><span class="sxs-lookup"><span data-stu-id="3ef53-111">The **DefaultContainer** property identifies a base container object to which you can bind and use as a starting point when browsing.</span></span> <span data-ttu-id="3ef53-112">Diese Daten werden gespeichert und aus dem folgenden Registrierungs Wert abgerufen.</span><span class="sxs-lookup"><span data-stu-id="3ef53-112">This data is stored and retrieved from the following registry value.</span></span>

```
HKEY_CURRENT_USER
   Software
      Microsoft
         ADs
            DefaultContainer
```

<span data-ttu-id="3ef53-113">ADSI definiert die **defaultcontainer** -Eigenschaft, um eine schnelle Möglichkeit zum Erstellen eines Zeigers auf ein zuvor definiertes ADSI-Container Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="3ef53-113">ADSI defines the **DefaultContainer** property to provide a quick way of getting a pointer to a previously defined ADSI container object.</span></span>

<dt>

<span data-ttu-id="3ef53-114">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="3ef53-114">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="3ef53-115">Skript Datentyp: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="3ef53-115">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_DefaultContainer(
  [out] BSTR* pbstrDefault
);
HRESULT put_DefaultContainer(
  [in] BSTR bstrDefault
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a><span data-ttu-id="3ef53-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3ef53-116">Remarks</span></span>

<span data-ttu-id="3ef53-117">Anbieter müssen diese Eigenschaft auf Benutzerbasis bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="3ef53-117">Providers must supply this property on a per-user basis.</span></span> <span data-ttu-id="3ef53-118">Der Standardcontainer wird unmittelbar nach dem Aufruf von **iadsnamespaces festgelegt::p UT \_ defaultcontainer**.</span><span class="sxs-lookup"><span data-stu-id="3ef53-118">The default container is set immediately after the invocation of **IADsNamespaces::put\_DefaultContainer**.</span></span> <span data-ttu-id="3ef53-119">Der Aufruf von " [**IADs.**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) \*" ist nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="3ef53-119">Calling [**IADs.SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) is not required.</span></span> <span data-ttu-id="3ef53-120">Tatsächlich gibt das vom System bereitgestellte Namespaces-Objekt **E \_ notimpl** für die **IADs. SetInfo** -Methode zurück, die für dieses Objekt aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="3ef53-120">In fact, the system-supplied namespaces object returns **E\_NOTIMPL** for the **IADs.SetInfo** method called on this object.</span></span> <span data-ttu-id="3ef53-121">Wenn ein Container das Namespaces-Objekt ist, führt ein Enumerationsvorgang immer zu einer Liste von anbieterspezifischen Namespace-Objekten.</span><span class="sxs-lookup"><span data-stu-id="3ef53-121">When a container is the namespaces object, an enumeration operation always results in a list of provider-specific namespace objects.</span></span> <span data-ttu-id="3ef53-122">Wenn [**IADsContainer. GetObject**](/windows/desktop/api/Iads/nf-iads-iadscontainer-getobject) zum Abrufen eines Namespace Objekts verwendet wird, wird der *bstrinclass* -Parameter ignoriert.</span><span class="sxs-lookup"><span data-stu-id="3ef53-122">When [**IADsContainer.GetObject**](/windows/desktop/api/Iads/nf-iads-iadscontainer-getobject) is used to obtain a namespace object, the *bstrClass* parameter is ignored.</span></span> <span data-ttu-id="3ef53-123">Dies liegt daran, dass der Container, d. h. das Namespaces-Objekt, nur einen Objekttyp enthält, nämlich anbieterspezifische Namespace Objekte.</span><span class="sxs-lookup"><span data-stu-id="3ef53-123">This is because the container, that is, the namespaces object, contains only one type of object, namely, provider-specific namespace objects.</span></span>

## <a name="requirements"></a><span data-ttu-id="3ef53-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3ef53-124">Requirements</span></span>



| <span data-ttu-id="3ef53-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3ef53-125">Requirement</span></span> | <span data-ttu-id="3ef53-126">Wert</span><span class="sxs-lookup"><span data-stu-id="3ef53-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3ef53-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3ef53-127">Minimum supported client</span></span><br/> | <span data-ttu-id="3ef53-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3ef53-128">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3ef53-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3ef53-129">Minimum supported server</span></span><br/> | <span data-ttu-id="3ef53-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3ef53-130">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3ef53-131">Header</span><span class="sxs-lookup"><span data-stu-id="3ef53-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="3ef53-132"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="3ef53-132"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="3ef53-133">DLL</span><span class="sxs-lookup"><span data-stu-id="3ef53-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3ef53-134"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3ef53-134"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="3ef53-135">IID</span><span class="sxs-lookup"><span data-stu-id="3ef53-135">IID</span></span><br/>                      | <span data-ttu-id="3ef53-136">IID \_ iadsnamespaces ist als 28b96ba0-B330-11CF-A9ad-00aa006bc149 definiert.</span><span class="sxs-lookup"><span data-stu-id="3ef53-136">IID\_IADsNamespaces is defined as 28B96BA0-B330-11CF-A9AD-00AA006BC149</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="3ef53-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3ef53-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ef53-138">**IADsContainer. GetObject**</span><span class="sxs-lookup"><span data-stu-id="3ef53-138">**IADsContainer.GetObject**</span></span>](/windows/desktop/api/Iads/nf-iads-iadscontainer-getobject)
</dt> <dt>

[<span data-ttu-id="3ef53-139">**Iadsnamespaces**</span><span class="sxs-lookup"><span data-stu-id="3ef53-139">**IADsNamespaces**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsnamespaces)
</dt> <dt>

[<span data-ttu-id="3ef53-140">Schnittstelleneigenschaften Methoden</span><span class="sxs-lookup"><span data-stu-id="3ef53-140">Interface Property Methods</span></span>](interface-property-methods.md)
</dt> </dl>

 

 





