---
description: 'IWiaUIExtension2::GetDeviceIcon-Methode: Ruft ein benutzerdefiniertes Gerätesymbol ab.'
ms.assetid: ea768dd1-22fe-4a0f-8851-b152e28d65fb
title: IWiaUIExtension2::GetDeviceIcon-Methode (Wiadevd.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaUIExtension2.GetDeviceIcon
api_type:
- COM
api_location:
- Wiadevd.h
ms.openlocfilehash: fe1498a804de5adeeea459464e95640b3b81ef06
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116618"
---
# <a name="iwiauiextension2getdeviceicon-method"></a><span data-ttu-id="4453e-103">IWiaUIExtension2::GetDeviceIcon-Methode</span><span class="sxs-lookup"><span data-stu-id="4453e-103">IWiaUIExtension2::GetDeviceIcon method</span></span>

<span data-ttu-id="4453e-104">Ruft ein benutzerdefiniertes Gerätesymbol ab.</span><span class="sxs-lookup"><span data-stu-id="4453e-104">Gets a custom device icon.</span></span>

## <a name="syntax"></a><span data-ttu-id="4453e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4453e-105">Syntax</span></span>


```C++
HRESULT GetDeviceIcon(
  [in]  BSTR  bstrDeviceId,
  [out] HICON *phIcon,
  [in]  ULONG nSize
);
```



## <a name="parameters"></a><span data-ttu-id="4453e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4453e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4453e-107">*bstrDeviceId* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="4453e-107">*bstrDeviceId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4453e-108">Typ: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="4453e-108">Type: **BSTR**</span></span>

<span data-ttu-id="4453e-109">Gibt die Geräte-ID des WIA-Geräts an, für das das Symbol abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="4453e-109">Specifies the device ID of the WIA device for which the icon is to be obtained.</span></span>

</dd> <dt>

<span data-ttu-id="4453e-110">*phIcon* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="4453e-110">*phIcon* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4453e-111">Typ: **HICON \***</span><span class="sxs-lookup"><span data-stu-id="4453e-111">Type: **HICON\***</span></span>

<span data-ttu-id="4453e-112">Zeigt auf eine Speicherposition, die ein Handle für das Symbol für das Gerät erhält.</span><span class="sxs-lookup"><span data-stu-id="4453e-112">Points to a memory location that will receive a handle for the icon for the device.</span></span>

</dd> <dt>

<span data-ttu-id="4453e-113">*nSize* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="4453e-113">*nSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4453e-114">Typ: **ULONG**</span><span class="sxs-lookup"><span data-stu-id="4453e-114">Type: **ULONG**</span></span>

<span data-ttu-id="4453e-115">Gibt die gewünschte Symbolgröße in Pixel an.</span><span class="sxs-lookup"><span data-stu-id="4453e-115">Specifies the desired icon size, in pixels.</span></span> <span data-ttu-id="4453e-116">Das Symbol wird als quadratisch angenommen, und nSize gibt sowohl die Breite als auch die Höhe des angeforderten Symbols an.</span><span class="sxs-lookup"><span data-stu-id="4453e-116">The icon is assumed to be square, and nSize specifies both the width and height of the requested icon.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4453e-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4453e-117">Return value</span></span>

<span data-ttu-id="4453e-118">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="4453e-118">Type: **HRESULT**</span></span>

<span data-ttu-id="4453e-119">Wenn die Methode erfolgreich ist, wird S \_ OK zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="4453e-119">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="4453e-120">Wenn die Methode fehlschlägt, wird ein entsprechender Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="4453e-120">If the method fails, it returns an appropriate error code.</span></span> <span data-ttu-id="4453e-121">In der folgenden Tabelle sind einige der möglichen Rückgabestatuscodes aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="4453e-121">The following table shows some of the possible return status codes.</span></span>



| <span data-ttu-id="4453e-122">Fehlercode</span><span class="sxs-lookup"><span data-stu-id="4453e-122">Error code</span></span>    | <span data-ttu-id="4453e-123">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4453e-123">Description</span></span>                                                                                                  |
|---------------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4453e-124">E \_ INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="4453e-124">E\_INVALIDARG</span></span> | <span data-ttu-id="4453e-125">Der Parameter bstrDeviceId oder phIcon ist **NULL,** oder bstrDeviceId verweist nicht auf eine gültige WIA-Geräte-ID-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="4453e-125">Parameter bstrDeviceId or phIcon is **NULL**, or bstrDeviceId does not point to a valid WIA device ID string</span></span> |
| <span data-ttu-id="4453e-126">E \_ FAIL</span><span class="sxs-lookup"><span data-stu-id="4453e-126">E\_FAIL</span></span>       | <span data-ttu-id="4453e-127">Es ist keine Symbolressource verfügbar.</span><span class="sxs-lookup"><span data-stu-id="4453e-127">No icon resource is available.</span></span>                                                                               |
| <span data-ttu-id="4453e-128">E \_ NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="4453e-128">E\_NOTIMPL</span></span>    | <span data-ttu-id="4453e-129">Es ist kein Symbol der angeforderten Größe verfügbar.</span><span class="sxs-lookup"><span data-stu-id="4453e-129">No icon of the size requested is available.</span></span>                                                                  |



 

## <a name="requirements"></a><span data-ttu-id="4453e-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4453e-130">Requirements</span></span>



| <span data-ttu-id="4453e-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4453e-131">Requirement</span></span> | <span data-ttu-id="4453e-132">Wert</span><span class="sxs-lookup"><span data-stu-id="4453e-132">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="4453e-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4453e-133">Minimum supported client</span></span><br/> | <span data-ttu-id="4453e-134">Nur Windows \[ XP-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4453e-134">Windows XP \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="4453e-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4453e-135">Minimum supported server</span></span><br/> | <span data-ttu-id="4453e-136">Nur Windows Server \[ 2003-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4453e-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="4453e-137">Header</span><span class="sxs-lookup"><span data-stu-id="4453e-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="4453e-138"><dt>Wiadevd.h</dt></span><span class="sxs-lookup"><span data-stu-id="4453e-138"><dt>Wiadevd.h</dt></span></span> </dl> |



 

 




