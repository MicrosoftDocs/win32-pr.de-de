---
title: Remotedesktopdienste audioendpoint-Schnittstellen
description: Die folgenden Schnittstellen werden mit der audioendpoint-API verwendet.
ms.assetid: 615c2d03-c2fb-46f8-aa78-064f8e7b6064
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de520571c99bf84472760e8a1ca28a52a1d6c32e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106337774"
---
# <a name="remote-desktop-services-audioendpoint-interfaces"></a><span data-ttu-id="baec9-103">Remotedesktopdienste audioendpoint-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="baec9-103">Remote Desktop Services AudioEndpoint Interfaces</span></span>

<span data-ttu-id="baec9-104">Die folgenden Schnittstellen werden mit der audioendpoint-API verwendet.</span><span class="sxs-lookup"><span data-stu-id="baec9-104">The following interfaces are used with the AudioEndpoint API.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="baec9-105">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="baec9-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="baec9-106">**Iaudiodeviceendpoint**</span><span class="sxs-lookup"><span data-stu-id="baec9-106">**IAudioDeviceEndpoint**</span></span>](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudiodeviceendpoint)
</dt> <dd>

<span data-ttu-id="baec9-107">Initialisiert ein Geräte Endpunkt Objekt und ruft die Funktionen des Geräts ab, das es darstellt.</span><span class="sxs-lookup"><span data-stu-id="baec9-107">Initializes a device endpoint object and gets the capabilities of the device that it represents.</span></span>

</dd> <dt>

[<span data-ttu-id="baec9-108">**Iaudioendpoint**</span><span class="sxs-lookup"><span data-stu-id="baec9-108">**IAudioEndpoint**</span></span>](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioendpoint)
</dt> <dd>

<span data-ttu-id="baec9-109">Stellt Informationen für die Audioengine über einen audioendpunkt bereit.</span><span class="sxs-lookup"><span data-stu-id="baec9-109">Provides information to the audio engine about an audio endpoint.</span></span> <span data-ttu-id="baec9-110">Diese Schnittstelle wird von einem audioendpunkt implementiert.</span><span class="sxs-lookup"><span data-stu-id="baec9-110">This interface is implemented by an audio endpoint.</span></span>

</dd> <dt>

[<span data-ttu-id="baec9-111">**Iaudioendpointcontrol**</span><span class="sxs-lookup"><span data-stu-id="baec9-111">**IAudioEndpointControl**</span></span>](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioendpointcontrol)
</dt> <dd>

<span data-ttu-id="baec9-112">Steuert den streamstatus eines Endpunkts.</span><span class="sxs-lookup"><span data-stu-id="baec9-112">Controls the stream state of an endpoint.</span></span>

</dd> <dt>

[<span data-ttu-id="baec9-113">**Iaudioendpointrt**</span><span class="sxs-lookup"><span data-stu-id="baec9-113">**IAudioEndpointRT**</span></span>](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioendpointrt)
</dt> <dd>

<span data-ttu-id="baec9-114">Ruft den Unterschied zwischen den aktuellen Lese-und Schreib Positionen im Endpunkt Puffer ab.</span><span class="sxs-lookup"><span data-stu-id="baec9-114">Gets the difference between the current read and write positions in the endpoint buffer.</span></span>

</dd> <dt>

[<span data-ttu-id="baec9-115">**Iaudioinputendpointrt**</span><span class="sxs-lookup"><span data-stu-id="baec9-115">**IAudioInputEndpointRT**</span></span>](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioinputendpointrt)
</dt> <dd>

<span data-ttu-id="baec9-116">Ruft den Eingabepuffer für jeden Verarbeitungs Durchlauf ab.</span><span class="sxs-lookup"><span data-stu-id="baec9-116">Gets the input buffer for each processing pass.</span></span>

</dd> <dt>

[<span data-ttu-id="baec9-117">**Iaudiooutputendpointrt**</span><span class="sxs-lookup"><span data-stu-id="baec9-117">**IAudioOutputEndpointRT**</span></span>](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudiooutputendpointrt)
</dt> <dd>

<span data-ttu-id="baec9-118">Ruft den Ausgabepuffer für jeden Verarbeitungs Durchlauf ab.</span><span class="sxs-lookup"><span data-stu-id="baec9-118">Gets the output buffer for each processing pass.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="baec9-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="baec9-119">Remarks</span></span>

<span data-ttu-id="baec9-120">Die Remotedesktopdienste audioendpoint-API ist für die Verwendung in Remotedesktop Szenarien vorgesehen. Es handelt sich nicht um Client Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="baec9-120">The Remote Desktop Services AudioEndpoint API is for use in Remote Desktop scenarios; it is not for client applications.</span></span>

 

 




