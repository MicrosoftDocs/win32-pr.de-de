---
description: Benachrichtigt ein-Objekt, dass es seinen Generator für die angegebene Eigenschaft anzeigen soll.
ms.assetid: 4d855aed-aaa1-4cc8-be9d-1175c254a813
title: 'Iprovidepropertybuilder:: executebuilder-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IProvidePropertyBuilder.ExecuteBuilder
api_type:
- COM
api_location:
- Vsp.dll
ms.openlocfilehash: c37c2a4ca1003bd701ea141f1723f4ca16aa69c3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358255"
---
# <a name="iprovidepropertybuilderexecutebuilder-method"></a><span data-ttu-id="5fdd8-103">Iprovidepropertybuilder:: executebuilder-Methode</span><span class="sxs-lookup"><span data-stu-id="5fdd8-103">IProvidePropertyBuilder::ExecuteBuilder method</span></span>

<span data-ttu-id="5fdd8-104">Benachrichtigt ein-Objekt, dass es seinen Generator für die angegebene Eigenschaft anzeigen soll.</span><span class="sxs-lookup"><span data-stu-id="5fdd8-104">Notifies an object that it should display its builder for the specified property.</span></span>

## <a name="syntax"></a><span data-ttu-id="5fdd8-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5fdd8-105">Syntax</span></span>


```C++
void ExecuteBuilder(
  [in]          LONG      dispid,
  [in]          BSTR      bstrGuidBldr,
  [in]          IDispatch *pdispApp,
  [in]          LONG_PTR  hwndBldrOwner,
  [in, out]     LPVARIANT pvarValue,
  [out, retval] LPBOOL    pbActionCommitted
);
```



## <a name="parameters"></a><span data-ttu-id="5fdd8-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5fdd8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5fdd8-107">*DISPID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5fdd8-107">*dispid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5fdd8-108">Die DispID der Eigenschaft, für die der Generator angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="5fdd8-108">The DISPID of the property for which the builder displays.</span></span>

</dd> <dt>

<span data-ttu-id="5fdd8-109">*bstringuidbldr* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5fdd8-109">*bstrGuidBldr* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5fdd8-110">Der **BSTR** der aufzurufenden Generator-GUID.</span><span class="sxs-lookup"><span data-stu-id="5fdd8-110">The **BSTR** of the builder GUID to invoke.</span></span> <span data-ttu-id="5fdd8-111">Dies wird von [**maptopropertybuilder**](iprovidepropertybuilder-mappropertytobuilder.md)zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="5fdd8-111">This is returned from [**MapToPropertyBuilder**](iprovidepropertybuilder-mappropertytobuilder.md).</span></span>

</dd> <dt>

<span data-ttu-id="5fdd8-112">*pdispapp* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5fdd8-112">*pdispApp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5fdd8-113">Auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="5fdd8-113">Set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="5fdd8-114">*hwndbldrowner* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5fdd8-114">*hwndBldrOwner* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5fdd8-115">Ein Handle des übergeordneten Popup-Generator-Fensters.</span><span class="sxs-lookup"><span data-stu-id="5fdd8-115">A handle to the parent pop-up builder window.</span></span>

</dd> <dt>

<span data-ttu-id="5fdd8-116">*pvarvalue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="5fdd8-116">*pvarValue* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="5fdd8-117">Der aktuelle Wert der Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="5fdd8-117">The current value of the property.</span></span> <span data-ttu-id="5fdd8-118">Dieser Wert kann durch das-Objekt geändert werden und ändert sich in den neuen Wert, wenn *pbactioncommit* den Wert " **true**" hat.</span><span class="sxs-lookup"><span data-stu-id="5fdd8-118">This value can be modified by the object and changes to the new value if *pbActionCommitted* is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="5fdd8-119">*pbactioncommit* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="5fdd8-119">*pbActionCommitted* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="5fdd8-120">Ein Wert, der angibt, ob der Generator eine Aktion für das Objekt ausgeführt hat.</span><span class="sxs-lookup"><span data-stu-id="5fdd8-120">A value that indicates whether the builder performed an action on the object.</span></span> <span data-ttu-id="5fdd8-121">Kann verwendet werden, wenn ein Benutzer etwas ändert, und dann im Popup-Generator-Dialogfeld auf OK.</span><span class="sxs-lookup"><span data-stu-id="5fdd8-121">Can be used when a user modifies something, then presses OK on the pop-up builder dialog box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5fdd8-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5fdd8-122">Return value</span></span>

<span data-ttu-id="5fdd8-123">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="5fdd8-123">Returns an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="5fdd8-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5fdd8-124">Requirements</span></span>



| <span data-ttu-id="5fdd8-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5fdd8-125">Requirement</span></span> | <span data-ttu-id="5fdd8-126">Wert</span><span class="sxs-lookup"><span data-stu-id="5fdd8-126">Value</span></span> |
|----------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5fdd8-127">DLL</span><span class="sxs-lookup"><span data-stu-id="5fdd8-127">DLL</span></span><br/> | <dl> <span data-ttu-id="5fdd8-128"><dt>Vsp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5fdd8-128"><dt>Vsp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5fdd8-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5fdd8-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5fdd8-130">**Iprovidäpropertybuilder**</span><span class="sxs-lookup"><span data-stu-id="5fdd8-130">**IProvidePropertyBuilder**</span></span>](iprovidepropertybuilder.md)
</dt> </dl>

 

 




