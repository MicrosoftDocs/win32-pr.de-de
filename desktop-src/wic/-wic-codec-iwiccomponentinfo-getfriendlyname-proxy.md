---
description: Proxy Funktion für die getfriendlyname-Methode.
ms.assetid: 8ac8f954-c2b9-47a2-88fe-b56710b5630c
title: IWICComponentInfo_GetFriendlyName_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICComponentInfo_GetFriendlyName_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 667571169818169cb7c7ea5a1f4d3d7eb6e1635e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349974"
---
# <a name="iwiccomponentinfo_getfriendlyname_proxy-function"></a><span data-ttu-id="9f6cb-103">Iwiccomponentinfo \_ getfriendlyname \_ Proxy-Funktion</span><span class="sxs-lookup"><span data-stu-id="9f6cb-103">IWICComponentInfo\_GetFriendlyName\_Proxy function</span></span>

<span data-ttu-id="9f6cb-104">Proxy Funktion für die [**getfriendlyname**](/windows/desktop/api/Wincodec/nf-wincodec-iwiccomponentinfo-getfriendlyname) -Methode.</span><span class="sxs-lookup"><span data-stu-id="9f6cb-104">Proxy function for the [**GetFriendlyName**](/windows/desktop/api/Wincodec/nf-wincodec-iwiccomponentinfo-getfriendlyname) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f6cb-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9f6cb-105">Syntax</span></span>


```C++
HRESULT IWICComponentInfo_GetFriendlyName_Proxy(
  _In_    IWICComponentInfo *THIS_PTR,
  _In_    UINT              cchFriendlyName,
  _Inout_ WCHAR             *wzFriendlyName,
  _Out_   UINT              *pcchActual
);
```



## <a name="parameters"></a><span data-ttu-id="9f6cb-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9f6cb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f6cb-107">*Dies \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9f6cb-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f6cb-108">Typ: \**[**iwiccomponentinfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="9f6cb-108">Type: \**[**IWICComponentInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo)\** _</span></span>

<span data-ttu-id="9f6cb-109">Zeiger auf dieses [_ *iwiccomponentinfo* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="9f6cb-109">Pointer to this [_ *IWICComponentInfo*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo) object.</span></span>

</dd> <dt>

<span data-ttu-id="9f6cb-110">*cchfriendlyname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9f6cb-110">*cchFriendlyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f6cb-111">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="9f6cb-111">Type: **UINT**</span></span>

<span data-ttu-id="9f6cb-112">Die Größe des *wzfriendlyname* -Puffers.</span><span class="sxs-lookup"><span data-stu-id="9f6cb-112">The size of the *wzFriendlyName* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="9f6cb-113">*wzfriendlyname* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="9f6cb-113">*wzFriendlyName* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="9f6cb-114">Typ: \**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="9f6cb-114">Type: \**WCHAR\** _</span></span>

<span data-ttu-id="9f6cb-115">Ein Zeiger, der den anzeigen amen der Komponente empfängt.</span><span class="sxs-lookup"><span data-stu-id="9f6cb-115">A pointer that receives the friendly name of the component.</span></span>

<span data-ttu-id="9f6cb-116">Die zurückgegebene Zeichenfolge ist Gebiets Schema spezifisch, 1033 standardmäßig.</span><span class="sxs-lookup"><span data-stu-id="9f6cb-116">The string returned is locale specific, 1033 by default.</span></span>

</dd> <dt>

<span data-ttu-id="9f6cb-117">_pcchActual \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="9f6cb-117">_pcchActual\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9f6cb-118">Typ: \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="9f6cb-118">Type: \**UINT\** _</span></span>

<span data-ttu-id="9f6cb-119">Ein Zeiger, der die tatsächliche Länge des anzeigen Amens der Komponente empfängt.</span><span class="sxs-lookup"><span data-stu-id="9f6cb-119">A pointer that receives the actual length of the component's friendly name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f6cb-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9f6cb-120">Return value</span></span>

<span data-ttu-id="9f6cb-121">Type: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="9f6cb-121">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="9f6cb-122">Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="9f6cb-122">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9f6cb-123">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9f6cb-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="9f6cb-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9f6cb-124">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="9f6cb-125">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="9f6cb-125">Requirements</span></span>



| <span data-ttu-id="9f6cb-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9f6cb-126">Requirement</span></span> | <span data-ttu-id="9f6cb-127">Wert</span><span class="sxs-lookup"><span data-stu-id="9f6cb-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f6cb-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9f6cb-128">Minimum supported client</span></span><br/> | <span data-ttu-id="9f6cb-129">Windows XP mit SP2, nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9f6cb-129">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="9f6cb-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9f6cb-130">Minimum supported server</span></span><br/> | <span data-ttu-id="9f6cb-131">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9f6cb-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="9f6cb-132">DLL</span><span class="sxs-lookup"><span data-stu-id="9f6cb-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9f6cb-133"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9f6cb-133"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




