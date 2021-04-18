---
title: Ideviceicon Width-Methode
description: Ruft die Breite des Symbols in Pixel ab.
ms.assetid: 28ADA921-6808-43B8-966E-BA42B1B52931
keywords:
- Width-Methode Medien Streaming-API
- Width-Methode Medien Streaming-API, ideviceicon-Schnittstelle
- Ideviceicon Interface Medien Streaming-API, Width-Methode
topic_type:
- apiref
api_name:
- IDeviceIcon.Width
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4b04f8c40cc209ccf1261af0fc2f6cdfd329db88
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104315081"
---
# <a name="ideviceiconwidth-method"></a><span data-ttu-id="52446-106">Ideviceicon:: width-Methode</span><span class="sxs-lookup"><span data-stu-id="52446-106">IDeviceIcon::Width method</span></span>

<span data-ttu-id="52446-107">Ruft die Breite des Symbols in Pixel ab.</span><span class="sxs-lookup"><span data-stu-id="52446-107">Retrieves the width of the icon in pixels.</span></span>

## <a name="syntax"></a><span data-ttu-id="52446-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="52446-108">Syntax</span></span>


```C++
HRESULT Width(
  [out] UINT32 *value
);
```



## <a name="parameters"></a><span data-ttu-id="52446-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="52446-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="52446-110">*Wert* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="52446-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="52446-111">Empfängt einen Zeiger auf die Breite des Symbols in Pixel.</span><span class="sxs-lookup"><span data-stu-id="52446-111">Receives a pointer to the width of the icon in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="52446-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="52446-112">Return value</span></span>

<span data-ttu-id="52446-113">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="52446-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="52446-114">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="52446-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="52446-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="52446-115">Return code</span></span>                                                                          | <span data-ttu-id="52446-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="52446-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="52446-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="52446-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="52446-118">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="52446-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="52446-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="52446-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52446-120">**Ideviceicon**</span><span class="sxs-lookup"><span data-stu-id="52446-120">**IDeviceIcon**</span></span>](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon)
</dt> </dl>

 

