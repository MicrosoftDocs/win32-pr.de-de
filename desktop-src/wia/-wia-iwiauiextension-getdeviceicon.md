---
description: Ruft ein benutzerdefiniertes Gerätesymbol ab.
ms.assetid: 27763f39-80d8-4862-b045-e49c6e824c28
title: 'Iwiauiextension:: getdeviceicon-Methode (wiadevd. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaUIExtension.GetDeviceIcon
api_type:
- COM
api_location:
- Wiadevd.h
ms.openlocfilehash: 36b61a25de1acb9b84ce68dc897514e0d4612a1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129408"
---
# <a name="iwiauiextensiongetdeviceicon-method"></a><span data-ttu-id="836a6-103">Iwiauiextension:: getdeviceicon-Methode</span><span class="sxs-lookup"><span data-stu-id="836a6-103">IWiaUIExtension::GetDeviceIcon method</span></span>

<span data-ttu-id="836a6-104">Ruft ein benutzerdefiniertes Gerätesymbol ab.</span><span class="sxs-lookup"><span data-stu-id="836a6-104">Gets a custom device icon.</span></span>

## <a name="syntax"></a><span data-ttu-id="836a6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="836a6-105">Syntax</span></span>


```C++
HRESULT GetDeviceIcon(
  [in]  BSTR  bstrDeviceId,
  [out] HICON *phIcon,
  [in]  ULONG nSize
);
```



## <a name="parameters"></a><span data-ttu-id="836a6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="836a6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="836a6-107">*bstraude viceid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="836a6-107">*bstrDeviceId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="836a6-108">Typ: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="836a6-108">Type: **BSTR**</span></span>

<span data-ttu-id="836a6-109">Gibt die Geräte-ID des WIA-Geräts an, für das das Symbol abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="836a6-109">Specifies the device ID of the WIA device for which the icon is to be obtained.</span></span>

</dd> <dt>

<span data-ttu-id="836a6-110">*phicon* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="836a6-110">*phIcon* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="836a6-111">Typ: \**HICON \** _</span><span class="sxs-lookup"><span data-stu-id="836a6-111">Type: \**HICON\** _</span></span>

<span data-ttu-id="836a6-112">Verweist auf einen Speicherort, der ein Handle für das Symbol für das Gerät empfängt.</span><span class="sxs-lookup"><span data-stu-id="836a6-112">Points to a memory location that will receive a handle for the icon for the device.</span></span>

</dd> <dt>

<span data-ttu-id="836a6-113">_nSize \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="836a6-113">_nSize\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="836a6-114">Typ: **ulong**</span><span class="sxs-lookup"><span data-stu-id="836a6-114">Type: **ULONG**</span></span>

<span data-ttu-id="836a6-115">Gibt die gewünschte Symbolgröße in Pixel an.</span><span class="sxs-lookup"><span data-stu-id="836a6-115">Specifies the desired icon size, in pixels.</span></span> <span data-ttu-id="836a6-116">Es wird davon ausgegangen, dass das Symbol quadratisch ist, und nSize gibt sowohl die Breite als auch die Höhe des angeforderten Symbols an.</span><span class="sxs-lookup"><span data-stu-id="836a6-116">The icon is assumed to be square, and nSize specifies both the width and height of the requested icon.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="836a6-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="836a6-117">Return value</span></span>

<span data-ttu-id="836a6-118">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="836a6-118">Type: **HRESULT**</span></span>

<span data-ttu-id="836a6-119">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="836a6-119">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="836a6-120">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="836a6-120">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="836a6-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="836a6-121">Requirements</span></span>



| <span data-ttu-id="836a6-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="836a6-122">Requirement</span></span> | <span data-ttu-id="836a6-123">Wert</span><span class="sxs-lookup"><span data-stu-id="836a6-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="836a6-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="836a6-124">Minimum supported client</span></span><br/> | <span data-ttu-id="836a6-125">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="836a6-125">Windows XP \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="836a6-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="836a6-126">Minimum supported server</span></span><br/> | <span data-ttu-id="836a6-127">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="836a6-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="836a6-128">Header</span><span class="sxs-lookup"><span data-stu-id="836a6-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="836a6-129"><dt>Wiadevd. h</dt></span><span class="sxs-lookup"><span data-stu-id="836a6-129"><dt>Wiadevd.h</dt></span></span> </dl> |



 

 




