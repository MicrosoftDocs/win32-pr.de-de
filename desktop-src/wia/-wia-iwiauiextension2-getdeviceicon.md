---
description: Ruft ein benutzerdefiniertes Gerätesymbol ab.
ms.assetid: ea768dd1-22fe-4a0f-8851-b152e28d65fb
title: 'IWiaUIExtension2:: getdeviceicon-Methode (wiadevd. h)'
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
ms.openlocfilehash: d071332a1947c4eb6398235d6941a6843a4fa54c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526444"
---
# <a name="iwiauiextension2getdeviceicon-method"></a><span data-ttu-id="b2c57-103">IWiaUIExtension2:: getdeviceicon-Methode</span><span class="sxs-lookup"><span data-stu-id="b2c57-103">IWiaUIExtension2::GetDeviceIcon method</span></span>

<span data-ttu-id="b2c57-104">Ruft ein benutzerdefiniertes Gerätesymbol ab.</span><span class="sxs-lookup"><span data-stu-id="b2c57-104">Gets a custom device icon.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2c57-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b2c57-105">Syntax</span></span>


```C++
HRESULT GetDeviceIcon(
  [in]  BSTR  bstrDeviceId,
  [out] HICON *phIcon,
  [in]  ULONG nSize
);
```



## <a name="parameters"></a><span data-ttu-id="b2c57-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b2c57-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2c57-107">*bstraude viceid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b2c57-107">*bstrDeviceId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2c57-108">Typ: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="b2c57-108">Type: **BSTR**</span></span>

<span data-ttu-id="b2c57-109">Gibt die Geräte-ID des WIA-Geräts an, für das das Symbol abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="b2c57-109">Specifies the device ID of the WIA device for which the icon is to be obtained.</span></span>

</dd> <dt>

<span data-ttu-id="b2c57-110">*phicon* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="b2c57-110">*phIcon* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b2c57-111">Typ: \**HICON \** _</span><span class="sxs-lookup"><span data-stu-id="b2c57-111">Type: \**HICON\** _</span></span>

<span data-ttu-id="b2c57-112">Verweist auf einen Speicherort, der ein Handle für das Symbol für das Gerät empfängt.</span><span class="sxs-lookup"><span data-stu-id="b2c57-112">Points to a memory location that will receive a handle for the icon for the device.</span></span>

</dd> <dt>

<span data-ttu-id="b2c57-113">_nSize \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b2c57-113">_nSize\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2c57-114">Typ: **ulong**</span><span class="sxs-lookup"><span data-stu-id="b2c57-114">Type: **ULONG**</span></span>

<span data-ttu-id="b2c57-115">Gibt die gewünschte Symbolgröße in Pixel an.</span><span class="sxs-lookup"><span data-stu-id="b2c57-115">Specifies the desired icon size, in pixels.</span></span> <span data-ttu-id="b2c57-116">Es wird davon ausgegangen, dass das Symbol quadratisch ist, und nSize gibt sowohl die Breite als auch die Höhe des angeforderten Symbols an.</span><span class="sxs-lookup"><span data-stu-id="b2c57-116">The icon is assumed to be square, and nSize specifies both the width and height of the requested icon.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b2c57-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b2c57-117">Return value</span></span>

<span data-ttu-id="b2c57-118">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="b2c57-118">Type: **HRESULT**</span></span>

<span data-ttu-id="b2c57-119">Wenn die Methode erfolgreich ausgeführt wird, gibt Sie S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="b2c57-119">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="b2c57-120">Wenn die Methode fehlschlägt, wird ein entsprechender Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b2c57-120">If the method fails, it returns an appropriate error code.</span></span> <span data-ttu-id="b2c57-121">In der folgenden Tabelle sind einige der möglichen Rückgabestatus Codes aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="b2c57-121">The following table shows some of the possible return status codes.</span></span>



| <span data-ttu-id="b2c57-122">Fehlercode</span><span class="sxs-lookup"><span data-stu-id="b2c57-122">Error code</span></span>    | <span data-ttu-id="b2c57-123">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b2c57-123">Description</span></span>                                                                                                  |
|---------------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2c57-124">E \_ invalidArg</span><span class="sxs-lookup"><span data-stu-id="b2c57-124">E\_INVALIDARG</span></span> | <span data-ttu-id="b2c57-125">Der Parameter "bstrintoviceid" oder "phicon" ist **null**, oder bstrintoviceid verweist nicht auf eine gültige WIA-Geräte-ID-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="b2c57-125">Parameter bstrDeviceId or phIcon is **NULL**, or bstrDeviceId does not point to a valid WIA device ID string</span></span> |
| <span data-ttu-id="b2c57-126">E \_ fehlschlagen</span><span class="sxs-lookup"><span data-stu-id="b2c57-126">E\_FAIL</span></span>       | <span data-ttu-id="b2c57-127">Es ist keine Symbol Ressource verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b2c57-127">No icon resource is available.</span></span>                                                                               |
| <span data-ttu-id="b2c57-128">E \_ notimpl</span><span class="sxs-lookup"><span data-stu-id="b2c57-128">E\_NOTIMPL</span></span>    | <span data-ttu-id="b2c57-129">Es ist kein Symbol der angeforderten Größe verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b2c57-129">No icon of the size requested is available.</span></span>                                                                  |



 

## <a name="requirements"></a><span data-ttu-id="b2c57-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b2c57-130">Requirements</span></span>



| <span data-ttu-id="b2c57-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b2c57-131">Requirement</span></span> | <span data-ttu-id="b2c57-132">Wert</span><span class="sxs-lookup"><span data-stu-id="b2c57-132">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b2c57-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b2c57-133">Minimum supported client</span></span><br/> | <span data-ttu-id="b2c57-134">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b2c57-134">Windows XP \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="b2c57-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b2c57-135">Minimum supported server</span></span><br/> | <span data-ttu-id="b2c57-136">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b2c57-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="b2c57-137">Header</span><span class="sxs-lookup"><span data-stu-id="b2c57-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="b2c57-138"><dt>Wiadevd. h</dt></span><span class="sxs-lookup"><span data-stu-id="b2c57-138"><dt>Wiadevd.h</dt></span></span> </dl> |



 

 




