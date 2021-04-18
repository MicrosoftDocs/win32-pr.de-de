---
description: Proxy Funktion für die GetVersion-Methode.
ms.assetid: b064b065-bc02-4943-b208-ce5e40c12aa2
title: IWICComponentInfo_GetVersion_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICComponentInfo_GetVersion_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: bad3677068802861bce9c0c7d0c1b03e5d06d0db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350978"
---
# <a name="iwiccomponentinfo_getversion_proxy-function"></a><span data-ttu-id="a4f1f-103">Iwiccomponentinfo- \_ GetVersion- \_ Proxy Funktion</span><span class="sxs-lookup"><span data-stu-id="a4f1f-103">IWICComponentInfo\_GetVersion\_Proxy function</span></span>

<span data-ttu-id="a4f1f-104">Proxy Funktion für die [**GetVersion**](/windows/desktop/api/Wincodec/nf-wincodec-iwiccomponentinfo-getversion) -Methode.</span><span class="sxs-lookup"><span data-stu-id="a4f1f-104">Proxy function for the [**GetVersion**](/windows/desktop/api/Wincodec/nf-wincodec-iwiccomponentinfo-getversion) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4f1f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a4f1f-105">Syntax</span></span>


```C++
HRESULT IWICComponentInfo_GetVersion_Proxy(
  _In_    IWICComponentInfo *THIS_PTR,
  _In_    UINT              cchVersion,
  _Inout_ WCHAR             *wzVersion,
  _Out_   UINT              *pcchActual
);
```



## <a name="parameters"></a><span data-ttu-id="a4f1f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a4f1f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4f1f-107">*Dies \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a4f1f-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4f1f-108">Typ: \**[**iwiccomponentinfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="a4f1f-108">Type: \**[**IWICComponentInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo)\** _</span></span>

<span data-ttu-id="a4f1f-109">Zeiger auf dieses [_ *iwiccomponentinfo* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="a4f1f-109">Pointer to this [_ *IWICComponentInfo*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo) object.</span></span>

</dd> <dt>

<span data-ttu-id="a4f1f-110">*cchversion* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a4f1f-110">*cchVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4f1f-111">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="a4f1f-111">Type: **UINT**</span></span>

<span data-ttu-id="a4f1f-112">Die Größe des *wzversion* -Puffers.</span><span class="sxs-lookup"><span data-stu-id="a4f1f-112">The size of the *wzVersion* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="a4f1f-113">*wzversion* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="a4f1f-113">*wzVersion* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a4f1f-114">Typ: \**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="a4f1f-114">Type: \**WCHAR\** _</span></span>

<span data-ttu-id="a4f1f-115">Ein Zeiger, der eine Kultur invarianter Zeichenfolge der Komponenten Version empfängt.</span><span class="sxs-lookup"><span data-stu-id="a4f1f-115">A pointer that receives a culture invariant string of the component's version.</span></span>

</dd> <dt>

<span data-ttu-id="a4f1f-116">_pcchActual \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="a4f1f-116">_pcchActual\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a4f1f-117">Typ: \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="a4f1f-117">Type: \**UINT\** _</span></span>

<span data-ttu-id="a4f1f-118">Ein Zeiger, der die tatsächliche Länge der Komponenten Version empfängt.</span><span class="sxs-lookup"><span data-stu-id="a4f1f-118">A pointer that receives the actual length of the component's version.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a4f1f-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a4f1f-119">Return value</span></span>

<span data-ttu-id="a4f1f-120">Type: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="a4f1f-120">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="a4f1f-121">Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="a4f1f-121">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a4f1f-122">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a4f1f-122">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="a4f1f-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a4f1f-123">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="a4f1f-124">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="a4f1f-124">Requirements</span></span>



| <span data-ttu-id="a4f1f-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a4f1f-125">Requirement</span></span> | <span data-ttu-id="a4f1f-126">Wert</span><span class="sxs-lookup"><span data-stu-id="a4f1f-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4f1f-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a4f1f-127">Minimum supported client</span></span><br/> | <span data-ttu-id="a4f1f-128">Windows XP mit SP2, nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a4f1f-128">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="a4f1f-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a4f1f-129">Minimum supported server</span></span><br/> | <span data-ttu-id="a4f1f-130">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a4f1f-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="a4f1f-131">DLL</span><span class="sxs-lookup"><span data-stu-id="a4f1f-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a4f1f-132"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a4f1f-132"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




