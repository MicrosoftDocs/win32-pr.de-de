---
description: Die itaudiodevicecontrol-Schnittstelle macht Methoden verfügbar, mit denen eine Anwendung Parameter für die Steuerung eines Audiogeräts erhalten und festlegen kann.
ms.assetid: 9a557cb2-acad-406c-9a87-18cbe96e8a9f
title: Itaudiode vicecontrol-Schnittstelle (ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 589bf50ee219f200a81aed7057b7755f203b2275
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358729"
---
# <a name="itaudiodevicecontrol-interface"></a><span data-ttu-id="77f5f-103">Itaudiodebug econtrol-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="77f5f-103">ITAudioDeviceControl interface</span></span>

<span data-ttu-id="77f5f-104">\[ Diese Schnittstelle ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="77f5f-104">\[ This interface is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="77f5f-105">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="77f5f-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="77f5f-106">Die **itaudiodevicecontrol** -Schnittstelle macht Methoden verfügbar, mit denen eine Anwendung Parameter für die Steuerung eines Audiogeräts erhalten und festlegen kann.</span><span class="sxs-lookup"><span data-stu-id="77f5f-106">The **ITAudioDeviceControl** interface exposes methods that enable an application to get and set parameters for control of an audio device.</span></span>

<span data-ttu-id="77f5f-107">Diese Schnittstelle wird von [ipconf MSP](ipconf-msp.md) und [h323 MSP](h323-msp.md)implementiert.</span><span class="sxs-lookup"><span data-stu-id="77f5f-107">This interface is implemented by the [IPConf MSP](ipconf-msp.md) and the [H323 MSP](h323-msp.md).</span></span> <span data-ttu-id="77f5f-108">Es wird verfügbar gemacht, wenn ein-Rückruf diese Dienstanbieter oder einen Dienstanbieter von Drittanbietern verwendet, der diese Schnittstelle implementiert.</span><span class="sxs-lookup"><span data-stu-id="77f5f-108">It is exposed when a call uses these service providers or a third party service provider that implements this interface.</span></span> <span data-ttu-id="77f5f-109">Rufen Sie zum Abrufen eines Zeigers auf die **itaudiodevicecontrol** -Schnittstelle **QueryInterface** in der [**itstream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream) -Schnittstelle auf, die das Audiogerät steuert, das dem Stream entspricht.</span><span class="sxs-lookup"><span data-stu-id="77f5f-109">To obtain a pointer to the **ITAudioDeviceControl** interface, call **QueryInterface** on the [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream) interface that controls the audio device corresponding to the stream.</span></span> <span data-ttu-id="77f5f-110">Der Medientyp der **itstream** -Schnittstelle muss Audio sein, damit die **itaudiodevicecontrol** -Schnittstelle verfügbar gemacht wird.</span><span class="sxs-lookup"><span data-stu-id="77f5f-110">The media type of the **ITStream** interface must be audio for the **ITAudioDeviceControl** interface to be exposed.</span></span>

## <a name="members"></a><span data-ttu-id="77f5f-111">Member</span><span class="sxs-lookup"><span data-stu-id="77f5f-111">Members</span></span>

<span data-ttu-id="77f5f-112">Die **itaudiode vicecontrol** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="77f5f-112">The **ITAudioDeviceControl** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="77f5f-113">**Itaudiotovicecontrol** verfügt auch über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="77f5f-113">**ITAudioDeviceControl** also has these types of members:</span></span>

-   [<span data-ttu-id="77f5f-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="77f5f-114">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="77f5f-115">Methoden</span><span class="sxs-lookup"><span data-stu-id="77f5f-115">Methods</span></span>

<span data-ttu-id="77f5f-116">Die **itaudiodevicecontrol** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="77f5f-116">The **ITAudioDeviceControl** interface has these methods.</span></span>



| <span data-ttu-id="77f5f-117">Methode</span><span class="sxs-lookup"><span data-stu-id="77f5f-117">Method</span></span>                                              | <span data-ttu-id="77f5f-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="77f5f-118">Description</span></span>                                                                                             |
|:----------------------------------------------------|:--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="77f5f-119">**Erhalten**</span><span class="sxs-lookup"><span data-stu-id="77f5f-119">**Get**</span></span>](/windows/desktop/api/tapi3if/nf-tapi3if-itasrterminalevent-get_call)          | <span data-ttu-id="77f5f-120">Ruft den Wert einer angegebenen [audiogeräteeigenschaft](audiodeviceproperty.md)ab.</span><span class="sxs-lookup"><span data-stu-id="77f5f-120">Gets the value of a given [audio device property](audiodeviceproperty.md).</span></span><br/>                  |
| [<span data-ttu-id="77f5f-121">**GetRange**</span><span class="sxs-lookup"><span data-stu-id="77f5f-121">**GetRange**</span></span>](/windows/desktop/api/tapi3if/nf-tapi3if-itasrterminalevent-get_terminal) | <span data-ttu-id="77f5f-122">Ruft den Bereich der gültigen Werte für eine angegebene [audiogeräteeigenschaft](audiodeviceproperty.md)ab.</span><span class="sxs-lookup"><span data-stu-id="77f5f-122">Gets the range of valid values for a given [audio device property](audiodeviceproperty.md).</span></span><br/> |
| [<span data-ttu-id="77f5f-123">**Set**</span><span class="sxs-lookup"><span data-stu-id="77f5f-123">**Set**</span></span>](/windows/desktop/api/tapi3if/nf-tapi3if-itasrterminalevent-get_error)         | <span data-ttu-id="77f5f-124">Legt den Wert einer angegebenen [audiogeräteeigenschaft](audiodeviceproperty.md)fest.</span><span class="sxs-lookup"><span data-stu-id="77f5f-124">Sets the value of a given [audio device property](audiodeviceproperty.md).</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="77f5f-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="77f5f-125">Requirements</span></span>



| <span data-ttu-id="77f5f-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="77f5f-126">Requirement</span></span> | <span data-ttu-id="77f5f-127">Wert</span><span class="sxs-lookup"><span data-stu-id="77f5f-127">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="77f5f-128">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="77f5f-128">TAPI version</span></span><br/> | <span data-ttu-id="77f5f-129">Erfordert TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="77f5f-129">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="77f5f-130">Header</span><span class="sxs-lookup"><span data-stu-id="77f5f-130">Header</span></span><br/>       | <dl> <span data-ttu-id="77f5f-131"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="77f5f-131"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="77f5f-132">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="77f5f-132">Library</span></span><br/>      | <dl> <span data-ttu-id="77f5f-133"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="77f5f-133"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="77f5f-134">DLL</span><span class="sxs-lookup"><span data-stu-id="77f5f-134">DLL</span></span><br/>          | <dl> <span data-ttu-id="77f5f-135"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="77f5f-135"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="77f5f-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="77f5f-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77f5f-137">Ipconf-msp</span><span class="sxs-lookup"><span data-stu-id="77f5f-137">IPConf MSP</span></span>](ipconf-msp.md)
</dt> </dl>

 

