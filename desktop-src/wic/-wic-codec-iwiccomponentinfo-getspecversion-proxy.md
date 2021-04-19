---
description: Proxy Funktion für die getspecversion-Methode.
ms.assetid: 363e55c2-d6e8-4ddc-a063-c5be08232a67
title: IWICComponentInfo_GetSpecVersion_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICComponentInfo_GetSpecVersion_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: a7b9b0a44eb5fd8404eecc3ad355ec280583d690
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106355455"
---
# <a name="iwiccomponentinfo_getspecversion_proxy-function"></a><span data-ttu-id="3f6e5-103">Iwiccomponentinfo \_ getspecversion- \_ Proxy Funktion</span><span class="sxs-lookup"><span data-stu-id="3f6e5-103">IWICComponentInfo\_GetSpecVersion\_Proxy function</span></span>

<span data-ttu-id="3f6e5-104">Proxy Funktion für die [**getspecversion**](/windows/desktop/api/Wincodec/nf-wincodec-iwiccomponentinfo-getspecversion) -Methode.</span><span class="sxs-lookup"><span data-stu-id="3f6e5-104">Proxy function for the [**GetSpecVersion**](/windows/desktop/api/Wincodec/nf-wincodec-iwiccomponentinfo-getspecversion) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f6e5-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3f6e5-105">Syntax</span></span>


```C++
HRESULT IWICComponentInfo_GetSpecVersion_Proxy(
  _In_    IWICComponentInfo *THIS_PTR,
  _In_    UINT              cchSpecVersion,
  _Inout_ WCHAR             *wzSpecVersion,
  _Out_   UINT              *pcchActual
);
```



## <a name="parameters"></a><span data-ttu-id="3f6e5-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3f6e5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f6e5-107">*Dies \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3f6e5-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f6e5-108">Typ: \**[**iwiccomponentinfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="3f6e5-108">Type: \**[**IWICComponentInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo)\** _</span></span>

<span data-ttu-id="3f6e5-109">Zeiger auf dieses [_ *iwiccomponentinfo* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="3f6e5-109">Pointer to this [_ *IWICComponentInfo*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo) object.</span></span>

</dd> <dt>

<span data-ttu-id="3f6e5-110">*cchspecversion* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3f6e5-110">*cchSpecVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f6e5-111">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="3f6e5-111">Type: **UINT**</span></span>

<span data-ttu-id="3f6e5-112">Die Größe des *wzspecversion* -Puffers.</span><span class="sxs-lookup"><span data-stu-id="3f6e5-112">The size of the *wzSpecVersion* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="3f6e5-113">*wzspecversion* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="3f6e5-113">*wzSpecVersion* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="3f6e5-114">Typ: \**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="3f6e5-114">Type: \**WCHAR\** _</span></span>

<span data-ttu-id="3f6e5-115">Wenn diese Methode zurückgegeben wird, enthalten Sie eine Kultur invarient-Zeichenfolge der Spezifikations Version der Komponente.</span><span class="sxs-lookup"><span data-stu-id="3f6e5-115">When this method returns, contain a culture invarient string of the component's specification version.</span></span> <span data-ttu-id="3f6e5-116">Das Versions Formular ist NN. NN. NN. NN.</span><span class="sxs-lookup"><span data-stu-id="3f6e5-116">The version form is NN.NN.NN.NN.</span></span>

</dd> <dt>

<span data-ttu-id="3f6e5-117">_pcchActual \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="3f6e5-117">_pcchActual\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3f6e5-118">Typ: \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="3f6e5-118">Type: \**UINT\** _</span></span>

<span data-ttu-id="3f6e5-119">Ein Zeiger, der die tatsächliche Länge der Spezifikations Version der Komponente empfängt.</span><span class="sxs-lookup"><span data-stu-id="3f6e5-119">A pointer that receives the actual length of the component's specification version.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3f6e5-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3f6e5-120">Return value</span></span>

<span data-ttu-id="3f6e5-121">Type: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="3f6e5-121">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="3f6e5-122">Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="3f6e5-122">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3f6e5-123">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="3f6e5-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="3f6e5-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3f6e5-124">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="3f6e5-125">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="3f6e5-125">Requirements</span></span>



| <span data-ttu-id="3f6e5-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3f6e5-126">Requirement</span></span> | <span data-ttu-id="3f6e5-127">Wert</span><span class="sxs-lookup"><span data-stu-id="3f6e5-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f6e5-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3f6e5-128">Minimum supported client</span></span><br/> | <span data-ttu-id="3f6e5-129">Windows XP mit SP2, nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3f6e5-129">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="3f6e5-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3f6e5-130">Minimum supported server</span></span><br/> | <span data-ttu-id="3f6e5-131">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3f6e5-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="3f6e5-132">DLL</span><span class="sxs-lookup"><span data-stu-id="3f6e5-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3f6e5-133"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3f6e5-133"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




