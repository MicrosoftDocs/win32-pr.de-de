---
title: Ideviceicon Height-Methode
description: Ruft die Höhe des Symbols in Pixel ab.
ms.assetid: 06E1B3AD-FF49-4BC9-AC67-E2E00954475F
keywords:
- Height-Methode Medien Streaming-API
- Height-Methode Medien Streaming-API, ideviceicon-Schnittstelle
- Ideviceicon Interface Medien Streaming-API, Height-Methode
topic_type:
- apiref
api_name:
- IDeviceIcon.Height
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bdba8d107cc844a29d215e5da49949595a8cd27a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104038979"
---
# <a name="ideviceiconheight-method"></a><span data-ttu-id="8b0dd-106">Ideviceicon:: Height-Methode</span><span class="sxs-lookup"><span data-stu-id="8b0dd-106">IDeviceIcon::Height method</span></span>

<span data-ttu-id="8b0dd-107">Ruft die Höhe des Symbols in Pixel ab.</span><span class="sxs-lookup"><span data-stu-id="8b0dd-107">Retrieves the height of the icon in pixels.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b0dd-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="8b0dd-108">Syntax</span></span>


```C++
HRESULT Height(
  [out] UINT32 *value
);
```



## <a name="parameters"></a><span data-ttu-id="8b0dd-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="8b0dd-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b0dd-110">*Wert* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="8b0dd-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8b0dd-111">Empfängt einen Zeiger auf die Höhe des Symbols in Pixel.</span><span class="sxs-lookup"><span data-stu-id="8b0dd-111">Receives a pointer to the height of the icon in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b0dd-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8b0dd-112">Return value</span></span>

<span data-ttu-id="8b0dd-113">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="8b0dd-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="8b0dd-114">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="8b0dd-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="8b0dd-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="8b0dd-115">Return code</span></span>                                                                          | <span data-ttu-id="8b0dd-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8b0dd-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="8b0dd-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="8b0dd-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="8b0dd-118">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8b0dd-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="8b0dd-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8b0dd-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b0dd-120">**Ideviceicon**</span><span class="sxs-lookup"><span data-stu-id="8b0dd-120">**IDeviceIcon**</span></span>](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon)
</dt> </dl>

 

