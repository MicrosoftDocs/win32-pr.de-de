---
description: Ruft die Schnittstellen-ID eines Agile-Verweises auf ein Objekt ab.
ms.assetid: 627A7EE4-CFEF-47F6-BA99-51BEB78C5D55
title: 'Iagilereferen:: Resolve-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAgileReference.Resolve
api_type:
- COM
api_location:
- objidl.h
ms.openlocfilehash: 1c3ac95802a44f4305abb24566744ad98c67b174
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106372820"
---
# <a name="iagilereferenceresolve-method"></a><span data-ttu-id="eaf5c-103">Iagilereferen:: Resolve-Methode</span><span class="sxs-lookup"><span data-stu-id="eaf5c-103">IAgileReference::Resolve method</span></span>

<span data-ttu-id="eaf5c-104">Ruft die Schnittstellen-ID eines Agile-Verweises auf ein Objekt ab.</span><span class="sxs-lookup"><span data-stu-id="eaf5c-104">Gets the interface ID of an agile reference to an object.</span></span>

## <a name="syntax"></a><span data-ttu-id="eaf5c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="eaf5c-105">Syntax</span></span>


```C++
HRESULT Resolve(
  [in]          REFIID riid,
  [out, retval] void   **ppvObjectReference
);
```



## <a name="parameters"></a><span data-ttu-id="eaf5c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="eaf5c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eaf5c-107">*riid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="eaf5c-107">*riid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eaf5c-108">Die Schnittstellen-ID der Schnittstelle, die aus dem Agile-Verweis abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="eaf5c-108">The interface ID of the interface to be retrieved from the agile reference.</span></span> <span data-ttu-id="eaf5c-109">Es muss nicht mit der registrierten Schnittstelle identisch sein.</span><span class="sxs-lookup"><span data-stu-id="eaf5c-109">It is not required to be the same as the registered interface.</span></span>

</dd> <dt>

<span data-ttu-id="eaf5c-110">*ppvobjectreferenzierung* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="eaf5c-110">*ppvObjectReference* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="eaf5c-111">Nach erfolgreichem Abschluss \* ist *ppvobjectreferenein* Zeiger auf die durch *riid* angegebene Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="eaf5c-111">On successful completion, \**ppvObjectReference* is a pointer to the interface specified by *riid*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eaf5c-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="eaf5c-112">Return value</span></span>

<span data-ttu-id="eaf5c-113">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="eaf5c-113">This method can return one of these values.</span></span>



| <span data-ttu-id="eaf5c-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="eaf5c-114">Return value</span></span>                                                                              | <span data-ttu-id="eaf5c-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="eaf5c-115">Description</span></span>                                                                    |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="eaf5c-116"><dt>S \_ OK</dt></span><span class="sxs-lookup"><span data-stu-id="eaf5c-116"><dt>S\_OK</dt></span></span> </dl>          | <span data-ttu-id="eaf5c-117">Die Methode wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="eaf5c-117">The method completed successfully.</span></span><br/>                                  |
| <dl> <span data-ttu-id="eaf5c-118"><dt>E \_ nointerface</dt></span><span class="sxs-lookup"><span data-stu-id="eaf5c-118"><dt>E\_NOINTERFACE</dt></span></span> </dl> | <span data-ttu-id="eaf5c-119">Die angeforderte Schnittstelle ist für das registrierte Objekt nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="eaf5c-119">The requested interface isn't implemented on the registered object.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="eaf5c-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="eaf5c-120">Remarks</span></span>

<span data-ttu-id="eaf5c-121">Rufen Sie die [**rogetagilereferenzierungsfunktion**](/windows/desktop/api/ComBaseApi/nf-combaseapi-rogetagilereference) auf, um einen agilen Verweis auf ein Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="eaf5c-121">Call the [**RoGetAgileReference**](/windows/desktop/api/ComBaseApi/nf-combaseapi-rogetagilereference) function to create an agile reference to an object.</span></span> <span data-ttu-id="eaf5c-122">Aufrufen der **Resolve** -Methode, um das Objekt in das Apartment zu lokalisieren, in dem **Resolve** aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="eaf5c-122">Call the **Resolve** method to localize the object into the apartment in which **Resolve** is called.</span></span>

## <a name="requirements"></a><span data-ttu-id="eaf5c-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="eaf5c-123">Requirements</span></span>



| <span data-ttu-id="eaf5c-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="eaf5c-124">Requirement</span></span> | <span data-ttu-id="eaf5c-125">Wert</span><span class="sxs-lookup"><span data-stu-id="eaf5c-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="eaf5c-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="eaf5c-126">Minimum supported client</span></span><br/> | <span data-ttu-id="eaf5c-127">Windows 8.1 \[ Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="eaf5c-127">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>            |
| <span data-ttu-id="eaf5c-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="eaf5c-128">Minimum supported server</span></span><br/> | <span data-ttu-id="eaf5c-129">Windows Server 2012 R2 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="eaf5c-129">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="eaf5c-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eaf5c-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eaf5c-131">**Iagilereferenzierung**</span><span class="sxs-lookup"><span data-stu-id="eaf5c-131">**IAgileReference**</span></span>](/windows/desktop/api/objidl/nn-objidl-iagilereference)
</dt> <dt>

[<span data-ttu-id="eaf5c-132">**Rogetagilereferenzierung**</span><span class="sxs-lookup"><span data-stu-id="eaf5c-132">**RoGetAgileReference**</span></span>](/windows/desktop/api/ComBaseApi/nf-combaseapi-rogetagilereference)
</dt> </dl>

 

 




