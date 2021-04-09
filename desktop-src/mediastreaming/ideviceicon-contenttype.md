---
title: Ideviceicon-ContentType-Methode
description: Ruft den Inhaltstyp des Symbols ab.
ms.assetid: 01928A98-B7D0-4523-9259-81FEB33F052E
keywords:
- ContentType-Methode Medien Streaming-API
- ContentType-Methode Medien Streaming-API, ideviceicon-Schnittstelle
- Ideviceicon Interface Medien Streaming-API, ContentType-Methode
topic_type:
- apiref
api_name:
- IDeviceIcon.ContentType
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: af48aabb2a64f4c4b8fbd40a3859acc82496a399
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103858177"
---
# <a name="ideviceiconcontenttype-method"></a><span data-ttu-id="83d3c-106">Ideviceicon:: ContentType-Methode</span><span class="sxs-lookup"><span data-stu-id="83d3c-106">IDeviceIcon::ContentType method</span></span>

<span data-ttu-id="83d3c-107">Ruft den Inhaltstyp des Symbols ab.</span><span class="sxs-lookup"><span data-stu-id="83d3c-107">Retrieves the content type of the icon.</span></span>

## <a name="syntax"></a><span data-ttu-id="83d3c-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="83d3c-108">Syntax</span></span>


```C++
HRESULT ContentType(
  [out] HSTRING *value
);
```



## <a name="parameters"></a><span data-ttu-id="83d3c-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="83d3c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83d3c-110">*Wert* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="83d3c-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="83d3c-111">Empfängt einen Zeiger auf den Inhaltstyp des Symbols.</span><span class="sxs-lookup"><span data-stu-id="83d3c-111">Receives a pointer to the content type of the icon.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83d3c-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="83d3c-112">Return value</span></span>

<span data-ttu-id="83d3c-113">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="83d3c-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="83d3c-114">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="83d3c-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="83d3c-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="83d3c-115">Return code</span></span>                                                                          | <span data-ttu-id="83d3c-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="83d3c-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="83d3c-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="83d3c-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="83d3c-118">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="83d3c-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="83d3c-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="83d3c-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83d3c-120">**Ideviceicon**</span><span class="sxs-lookup"><span data-stu-id="83d3c-120">**IDeviceIcon**</span></span>](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon)
</dt> </dl>

 

