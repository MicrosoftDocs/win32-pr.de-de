---
description: 'IWiaUIExtension::GetDeviceIcon-Methode: Ruft ein benutzerdefiniertes Gerätesymbol ab.'
ms.assetid: 27763f39-80d8-4862-b045-e49c6e824c28
title: IWiaUIExtension::GetDeviceIcon-Methode (Wiadevd.h)
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
ms.openlocfilehash: 9bfa8e87736412822c1a70f75b129aeec30af20e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116658"
---
# <a name="iwiauiextensiongetdeviceicon-method"></a><span data-ttu-id="198ef-103">IWiaUIExtension::GetDeviceIcon-Methode</span><span class="sxs-lookup"><span data-stu-id="198ef-103">IWiaUIExtension::GetDeviceIcon method</span></span>

<span data-ttu-id="198ef-104">Ruft ein benutzerdefiniertes Gerätesymbol ab.</span><span class="sxs-lookup"><span data-stu-id="198ef-104">Gets a custom device icon.</span></span>

## <a name="syntax"></a><span data-ttu-id="198ef-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="198ef-105">Syntax</span></span>


```C++
HRESULT GetDeviceIcon(
  [in]  BSTR  bstrDeviceId,
  [out] HICON *phIcon,
  [in]  ULONG nSize
);
```



## <a name="parameters"></a><span data-ttu-id="198ef-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="198ef-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="198ef-107">*bstrDeviceId* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="198ef-107">*bstrDeviceId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="198ef-108">Typ: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="198ef-108">Type: **BSTR**</span></span>

<span data-ttu-id="198ef-109">Gibt die Geräte-ID des WIA-Geräts an, für das das Symbol abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="198ef-109">Specifies the device ID of the WIA device for which the icon is to be obtained.</span></span>

</dd> <dt>

<span data-ttu-id="198ef-110">*phIcon* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="198ef-110">*phIcon* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="198ef-111">Typ: **HICON \***</span><span class="sxs-lookup"><span data-stu-id="198ef-111">Type: **HICON\***</span></span>

<span data-ttu-id="198ef-112">Zeigt auf eine Speicherposition, die ein Handle für das Symbol für das Gerät erhält.</span><span class="sxs-lookup"><span data-stu-id="198ef-112">Points to a memory location that will receive a handle for the icon for the device.</span></span>

</dd> <dt>

<span data-ttu-id="198ef-113">*nSize* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="198ef-113">*nSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="198ef-114">Typ: **ULONG**</span><span class="sxs-lookup"><span data-stu-id="198ef-114">Type: **ULONG**</span></span>

<span data-ttu-id="198ef-115">Gibt die gewünschte Symbolgröße in Pixel an.</span><span class="sxs-lookup"><span data-stu-id="198ef-115">Specifies the desired icon size, in pixels.</span></span> <span data-ttu-id="198ef-116">Das Symbol wird als quadratisch angenommen, und nSize gibt sowohl die Breite als auch die Höhe des angeforderten Symbols an.</span><span class="sxs-lookup"><span data-stu-id="198ef-116">The icon is assumed to be square, and nSize specifies both the width and height of the requested icon.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="198ef-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="198ef-117">Return value</span></span>

<span data-ttu-id="198ef-118">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="198ef-118">Type: **HRESULT**</span></span>

<span data-ttu-id="198ef-119">Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="198ef-119">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="198ef-120">Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="198ef-120">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="198ef-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="198ef-121">Requirements</span></span>



| <span data-ttu-id="198ef-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="198ef-122">Requirement</span></span> | <span data-ttu-id="198ef-123">Wert</span><span class="sxs-lookup"><span data-stu-id="198ef-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="198ef-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="198ef-124">Minimum supported client</span></span><br/> | <span data-ttu-id="198ef-125">Nur Windows \[ XP-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="198ef-125">Windows XP \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="198ef-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="198ef-126">Minimum supported server</span></span><br/> | <span data-ttu-id="198ef-127">Nur Windows Server \[ 2003-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="198ef-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="198ef-128">Header</span><span class="sxs-lookup"><span data-stu-id="198ef-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="198ef-129"><dt>Wiadevd.h</dt></span><span class="sxs-lookup"><span data-stu-id="198ef-129"><dt>Wiadevd.h</dt></span></span> </dl> |



 

 




