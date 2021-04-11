---
title: Ideviceicon-streammethode
description: Ruft das Symbol als Datenstrom ab.
ms.assetid: 0B9E852F-4F72-4721-8F88-24A850A088C4
keywords:
- Stream-Methode Medien Streaming-API
- Stream-Methode Medien Streaming-API, ideviceicon-Schnittstelle
- Ideviceicon-Schnittstelle Medien Streaming-API, Stream-Methode
topic_type:
- apiref
api_name:
- IDeviceIcon.Stream
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fd00d757fceb90cf5ee7199256b003464063abcb
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104315086"
---
# <a name="ideviceiconstream-method"></a><span data-ttu-id="ce07a-106">Ideviceicon:: Stream-Methode</span><span class="sxs-lookup"><span data-stu-id="ce07a-106">IDeviceIcon::Stream method</span></span>

<span data-ttu-id="ce07a-107">Ruft das Symbol als Datenstrom ab.</span><span class="sxs-lookup"><span data-stu-id="ce07a-107">Retrieves the icon as a stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce07a-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="ce07a-108">Syntax</span></span>


```C++
HRESULT Stream(
  [out] IRandomAccessStreamWithContentType **value
);
```



## <a name="parameters"></a><span data-ttu-id="ce07a-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="ce07a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce07a-110">*Wert* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="ce07a-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ce07a-111">Empfängt einen Verweis auf einen " [**tyandomaccessstreamwithcontenttype**](/uwp/api/Windows.Storage.Streams.IRandomAccessStreamWithContentType) ", der zum Abrufen der Bilddaten verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="ce07a-111">Receives a reference to a [**IRandomAccessStreamWithContentType**](/uwp/api/Windows.Storage.Streams.IRandomAccessStreamWithContentType) that can be used to retrieve the image data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce07a-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ce07a-112">Return value</span></span>

<span data-ttu-id="ce07a-113">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="ce07a-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="ce07a-114">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="ce07a-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="ce07a-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="ce07a-115">Return code</span></span>                                                                          | <span data-ttu-id="ce07a-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ce07a-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="ce07a-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ce07a-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="ce07a-118">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ce07a-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="ce07a-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ce07a-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce07a-120">**Ideviceicon**</span><span class="sxs-lookup"><span data-stu-id="ce07a-120">**IDeviceIcon**</span></span>](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon)
</dt> </dl>

 

