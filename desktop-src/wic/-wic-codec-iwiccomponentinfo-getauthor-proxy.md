---
description: Proxy Funktion für die getauthor-Methode.
ms.assetid: fb76009e-cc01-4dec-9403-04bf6b53db80
title: IWICComponentInfo_GetAuthor_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICComponentInfo_GetAuthor_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: f181a567ae4089870d324c7a7e0d67a34b965b5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364195"
---
# <a name="iwiccomponentinfo_getauthor_proxy-function"></a><span data-ttu-id="facde-103">Iwiccomponentinfo \_ getauthor- \_ Proxy Funktion</span><span class="sxs-lookup"><span data-stu-id="facde-103">IWICComponentInfo\_GetAuthor\_Proxy function</span></span>

<span data-ttu-id="facde-104">Proxy Funktion für die [**getauthor**](/windows/desktop/api/Wincodec/nf-wincodec-iwiccomponentinfo-getauthor) -Methode.</span><span class="sxs-lookup"><span data-stu-id="facde-104">Proxy function for the [**GetAuthor**](/windows/desktop/api/Wincodec/nf-wincodec-iwiccomponentinfo-getauthor) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="facde-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="facde-105">Syntax</span></span>


```C++
HRESULT IWICComponentInfo_GetAuthor_Proxy(
  _In_    IWICComponentInfo *THIS_PTR,
  _In_    UINT              cchAuthor,
  _Inout_ WCHAR             *wzAuthor,
  _Out_   UINT              *pcchActual
);
```



## <a name="parameters"></a><span data-ttu-id="facde-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="facde-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="facde-107">*Dies \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="facde-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="facde-108">Typ: \**[**iwiccomponentinfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="facde-108">Type: \**[**IWICComponentInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo)\** _</span></span>

<span data-ttu-id="facde-109">Zeiger auf dieses [_ *iwiccomponentinfo* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="facde-109">Pointer to this [_ *IWICComponentInfo*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo) object.</span></span>

</dd> <dt>

<span data-ttu-id="facde-110">*cchauthor* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="facde-110">*cchAuthor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="facde-111">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="facde-111">Type: **UINT**</span></span>

<span data-ttu-id="facde-112">Die Größe des *wzauthor* -Puffers.</span><span class="sxs-lookup"><span data-stu-id="facde-112">The size of the *wzAuthor* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="facde-113">*wzauthor* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="facde-113">*wzAuthor* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="facde-114">Typ: \**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="facde-114">Type: \**WCHAR\** _</span></span>

<span data-ttu-id="facde-115">Ein Zeiger, der den Namen des Autors der Komponente empfängt.</span><span class="sxs-lookup"><span data-stu-id="facde-115">A pointer that receives the name of the component's author.</span></span>

<span data-ttu-id="facde-116">Die zurückgegebene Zeichenfolge ist Gebiets Schema spezifisch, 1033 standardmäßig.</span><span class="sxs-lookup"><span data-stu-id="facde-116">The string returned is locale specific, 1033 by default.</span></span>

</dd> <dt>

<span data-ttu-id="facde-117">_pcchActual \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="facde-117">_pcchActual\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="facde-118">Typ: \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="facde-118">Type: \**UINT\** _</span></span>

<span data-ttu-id="facde-119">Ein Zeiger, der die tatsächliche Länge des Autoren namens der Komponente empfängt.</span><span class="sxs-lookup"><span data-stu-id="facde-119">A pointer that receives the actual length of the component's authors name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="facde-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="facde-120">Return value</span></span>

<span data-ttu-id="facde-121">Type: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="facde-121">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="facde-122">Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="facde-122">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="facde-123">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="facde-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="facde-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="facde-124">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="facde-125">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="facde-125">Requirements</span></span>



| <span data-ttu-id="facde-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="facde-126">Requirement</span></span> | <span data-ttu-id="facde-127">Wert</span><span class="sxs-lookup"><span data-stu-id="facde-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="facde-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="facde-128">Minimum supported client</span></span><br/> | <span data-ttu-id="facde-129">Windows XP mit SP2, nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="facde-129">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="facde-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="facde-130">Minimum supported server</span></span><br/> | <span data-ttu-id="facde-131">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="facde-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="facde-132">DLL</span><span class="sxs-lookup"><span data-stu-id="facde-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="facde-133"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="facde-133"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




