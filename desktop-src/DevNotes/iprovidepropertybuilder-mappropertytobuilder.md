---
description: Überprüft, ob ein Generator einer bestimmten Eigenschaft zugeordnet werden soll.
ms.assetid: 8fab2dc2-3549-4559-b704-6783d929274e
title: 'Iprovidepropertybuilder:: mappropertydebuilder-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IProvidePropertyBuilder.MapPropertyToBuilder
api_type:
- COM
api_location:
- Vsp.dll
ms.openlocfilehash: 5fa755449bfb97940235fe45f9e299aa828e6faa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366900"
---
# <a name="iprovidepropertybuildermappropertytobuilder-method"></a><span data-ttu-id="8141d-103">Iprovidepropertybuilder:: mappropertydebuilder-Methode</span><span class="sxs-lookup"><span data-stu-id="8141d-103">IProvidePropertyBuilder::MapPropertyToBuilder method</span></span>

<span data-ttu-id="8141d-104">Überprüft, ob ein Generator einer bestimmten Eigenschaft zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="8141d-104">Checks whether a builder should be associated with a particular property.</span></span>

## <a name="syntax"></a><span data-ttu-id="8141d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8141d-105">Syntax</span></span>


```C++
void MapPropertyToBuilder(
  [in]          LONG   dispid,
  [out]         DWORD  *pdwCtlBldType,
  [out]         LPBSTR pbstrGuidBldr,
  [out, retval] LPBOOL builderAvailable
);
```



## <a name="parameters"></a><span data-ttu-id="8141d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8141d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8141d-107">*DISPID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8141d-107">*dispid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8141d-108">Die DispID der fraglichen Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="8141d-108">The DISPID of the property in question.</span></span>

</dd> <dt>

<span data-ttu-id="8141d-109">*pdwctlbldtype* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="8141d-109">*pdwCtlBldType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8141d-110">Der Generator, der zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="8141d-110">The builder to be mapped.</span></span> <span data-ttu-id="8141d-111">Dieser Parameter kann eine Kombination der folgenden Werte sein.</span><span class="sxs-lookup"><span data-stu-id="8141d-111">This parameter can be a combination of the following values.</span></span>



| <span data-ttu-id="8141d-112">Wert</span><span class="sxs-lookup"><span data-stu-id="8141d-112">Value</span></span>                                                                                                                                                                                                                                                          | <span data-ttu-id="8141d-113">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="8141d-113">Meaning</span></span>                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <span id="CTLBLDTYPE_FSTDPROPBUILDER"></span><span id="ctlbldtype_fstdpropbuilder"></span><dl> <span data-ttu-id="8141d-114"><dt>**Ctlbldtype \_ "F**</dt> <dt></dt> ", "f"</span><span class="sxs-lookup"><span data-stu-id="8141d-114"><dt>**CTLBLDTYPE\_FSTDPROPBUILDER**</dt> <dt>1</dt></span></span> </dl>    | <span data-ttu-id="8141d-115">Aufrufen eines Standardsystem-Generators (wird in Visual Studio nicht unterstützt).</span><span class="sxs-lookup"><span data-stu-id="8141d-115">Invoke a standard system builder (not supported in Visual Studio).</span></span><br/> |
| <span id="CTLBLDTYPE_FINTERNALBUILDER"></span><span id="ctlbldtype_finternalbuilder"></span><dl> <span data-ttu-id="8141d-116"><dt>**Ctlbldtype \_ Finternalbuilder**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="8141d-116"><dt>**CTLBLDTYPE\_FINTERNALBUILDER**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="8141d-117">Rufen Sie einen benutzerdefinierten Generator auf.</span><span class="sxs-lookup"><span data-stu-id="8141d-117">Invoke a custom builder.</span></span><br/>                                           |
| <span id="CTLBLDTYPE_EDITSOBJDIRECTLY"></span><span id="ctlbldtype_editsobjdirectly"></span><dl> <span data-ttu-id="8141d-118"><dt>**Ctlbldtype \_ Editsobjdirekt**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="8141d-118"><dt>**CTLBLDTYPE\_EDITSOBJDIRECTLY**</dt> <dt>4</dt></span></span> </dl> | <span data-ttu-id="8141d-119">Generator ändert das Objekt.</span><span class="sxs-lookup"><span data-stu-id="8141d-119">Builder modifies the object.</span></span> <span data-ttu-id="8141d-120">Dies ist ein gewöhnliches Verhalten.</span><span class="sxs-lookup"><span data-stu-id="8141d-120">This is common behavior.</span></span><br/>              |



 

</dd> <dt>

<span data-ttu-id="8141d-121">*pbstringuidbldr* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="8141d-121">*pbstrGuidBldr* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8141d-122">Die GUID, die den Generator für diese Eigenschaft identifiziert.</span><span class="sxs-lookup"><span data-stu-id="8141d-122">The GUID that identifies the builder for this property.</span></span>

</dd> <dt>

<span data-ttu-id="8141d-123">*builderavailable* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="8141d-123">*builderAvailable* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="8141d-124">Dieser Parameter ist **true** , wenn diese Eigenschaft derzeit einen Generator unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8141d-124">This parameter is **TRUE** if this property currently supports a builder.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8141d-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8141d-125">Return value</span></span>

<span data-ttu-id="8141d-126">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="8141d-126">Returns an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="8141d-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8141d-127">Requirements</span></span>



| <span data-ttu-id="8141d-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8141d-128">Requirement</span></span> | <span data-ttu-id="8141d-129">Wert</span><span class="sxs-lookup"><span data-stu-id="8141d-129">Value</span></span> |
|----------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8141d-130">DLL</span><span class="sxs-lookup"><span data-stu-id="8141d-130">DLL</span></span><br/> | <dl> <span data-ttu-id="8141d-131"><dt>Vsp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8141d-131"><dt>Vsp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8141d-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8141d-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8141d-133">**Iprovidäpropertybuilder**</span><span class="sxs-lookup"><span data-stu-id="8141d-133">**IProvidePropertyBuilder**</span></span>](iprovidepropertybuilder.md)
</dt> </dl>

 

 




