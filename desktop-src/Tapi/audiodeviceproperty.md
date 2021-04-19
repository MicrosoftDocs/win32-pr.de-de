---
description: 'Die audiodeviceproperty-Enumeration wird von den Methoden itaudiodevicecontrol:: GetRange, itaudiodevicecontrol:: Get und itaudiodevicecontrol:: Set verwendet, um die Eigenschaft anzugeben, die adressiert wird.'
ms.assetid: 0ed9b75e-3c79-4e41-9883-63b85ebfae06
title: Audiodeviceproperty-Enumeration (ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab807759bfb316858be41ea9bb4b78d795ee1a1a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367053"
---
# <a name="audiodeviceproperty-enumeration"></a><span data-ttu-id="61817-103">Audiodeviceproperty-Enumeration</span><span class="sxs-lookup"><span data-stu-id="61817-103">AudioDeviceProperty enumeration</span></span>

<span data-ttu-id="61817-104">\[ Diese Enumeration ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="61817-104">\[ This enumeration is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="61817-105">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="61817-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="61817-106">Die **audiodeviceproperty** -Enumeration wird von den Methoden [**itaudiodevicecontrol:: GetRange**](itaudiodevicecontrol-getrange.md), [**itaudiodevicecontrol:: Get**](itaudiodevicecontrol-get.md)und [**itaudiodevicecontrol**](itaudiodevicecontrol-set.md) :: Set verwendet, um die Eigenschaft anzugeben, die adressiert wird.</span><span class="sxs-lookup"><span data-stu-id="61817-106">The **AudioDeviceProperty** enum is used by the [**ITAudioDeviceControl::GetRange**](itaudiodevicecontrol-getrange.md), [**ITAudioDeviceControl::Get**](itaudiodevicecontrol-get.md), and [**ITAudioDeviceControl::Set**](itaudiodevicecontrol-set.md) methods to indicate the property being addressed.</span></span>

## <a name="syntax"></a><span data-ttu-id="61817-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="61817-107">Syntax</span></span>


```C++
} AudioDeviceProperty;
```



## <a name="constants"></a><span data-ttu-id="61817-108">Konstanten</span><span class="sxs-lookup"><span data-stu-id="61817-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="61817-109"><span id="AudioDevice_DuplexMode"></span><span id="audiodevice_duplexmode"></span><span id="AUDIODEVICE_DUPLEXMODE"></span>**Audiodevice- \_ duplexmode**</span><span class="sxs-lookup"><span data-stu-id="61817-109"><span id="AudioDevice_DuplexMode"></span><span id="audiodevice_duplexmode"></span><span id="AUDIODEVICE_DUPLEXMODE"></span>**AudioDevice\_DuplexMode**</span></span>
</dt> <dd>

<span data-ttu-id="61817-110">Gibt an, dass der Duplex Modus des Geräts festgelegt oder abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="61817-110">Indicates that the duplex mode of the device is being set or retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="61817-111"><span id="AudioDevice_AutomaticGainControl"></span><span id="audiodevice_automaticgaincontrol"></span><span id="AUDIODEVICE_AUTOMATICGAINCONTROL"></span>**Audiodevice \_ automaticgaincontrol**</span><span class="sxs-lookup"><span data-stu-id="61817-111"><span id="AudioDevice_AutomaticGainControl"></span><span id="audiodevice_automaticgaincontrol"></span><span id="AUDIODEVICE_AUTOMATICGAINCONTROL"></span>**AudioDevice\_AutomaticGainControl**</span></span>
</dt> <dd>

<span data-ttu-id="61817-112">Gibt an, dass die automatische Erlangung der Steuerung des Geräts festgelegt oder abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="61817-112">Indicates that the automatic gain control of the device is being set or retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="61817-113"><span id="AudioDevice_AcousticEchoCancellation"></span><span id="audiodevice_acousticechocancellation"></span><span id="AUDIODEVICE_ACOUSTICECHOCANCELLATION"></span>**Audiodevice- \_ acousticechoabbruch**</span><span class="sxs-lookup"><span data-stu-id="61817-113"><span id="AudioDevice_AcousticEchoCancellation"></span><span id="audiodevice_acousticechocancellation"></span><span id="AUDIODEVICE_ACOUSTICECHOCANCELLATION"></span>**AudioDevice\_AcousticEchoCancellation**</span></span>
</dt> <dd>

<span data-ttu-id="61817-114">Gibt an, dass die Eigenschaften für den akustischen Echo Abbruch des Geräts festgelegt oder abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="61817-114">Indicates that the acoustic echo cancellation properties of the device are being set or retrieved.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="61817-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="61817-115">Requirements</span></span>



| <span data-ttu-id="61817-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="61817-116">Requirement</span></span> | <span data-ttu-id="61817-117">Wert</span><span class="sxs-lookup"><span data-stu-id="61817-117">Value</span></span> |
|-------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="61817-118">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="61817-118">TAPI version</span></span><br/> | <span data-ttu-id="61817-119">Erfordert TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="61817-119">Requires TAPI 3.1</span></span><br/>                                                       |
| <span data-ttu-id="61817-120">Header</span><span class="sxs-lookup"><span data-stu-id="61817-120">Header</span></span><br/>       | <dl> <span data-ttu-id="61817-121"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="61817-121"><dt>Ipmsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61817-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="61817-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61817-123">**Itaudiodebug econtrol:: GetRange**</span><span class="sxs-lookup"><span data-stu-id="61817-123">**ITAudioDeviceControl::GetRange**</span></span>](itaudiodevicecontrol-getrange.md)
</dt> <dt>

[<span data-ttu-id="61817-124">**Itaudiodebug econtrol:: Get**</span><span class="sxs-lookup"><span data-stu-id="61817-124">**ITAudioDeviceControl::Get**</span></span>](itaudiodevicecontrol-get.md)
</dt> <dt>

[<span data-ttu-id="61817-125">**Itaudiode vicecontrol:: Set**</span><span class="sxs-lookup"><span data-stu-id="61817-125">**ITAudioDeviceControl::Set**</span></span>](itaudiodevicecontrol-set.md)
</dt> </dl>

 

 




