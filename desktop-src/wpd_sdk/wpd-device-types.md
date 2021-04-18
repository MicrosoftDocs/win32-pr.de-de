---
description: Der \_ \_ Enumerationstyp "WPD-Gerätetypen" beschreibt die verschiedenen Windows Portable Device (WPD)-Typen, die häufig verwendet werden, um die grundlegende Klassifizierung und visuelle Darstellung eines tragbaren Geräts zu bestimmen.
ms.assetid: 51714e0f-e9b7-4474-a8bb-da3875ef5399
title: WPD_DEVICE_TYPES-Enumeration (portabledevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_DEVICE_TYPES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 3e71acf200a95bba05b7298a5824bfa353e4a90b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358204"
---
# <a name="wpd_device_types-enumeration"></a><span data-ttu-id="7d35c-103">WPD \_ - \_ Gerätetyp-Enumeration</span><span class="sxs-lookup"><span data-stu-id="7d35c-103">WPD\_DEVICE\_TYPES enumeration</span></span>

<span data-ttu-id="7d35c-104">Der Enumerationstyp " **WPD- \_ Geräte \_ Typen** " beschreibt die verschiedenen Windows Portable Device (WPD)-Typen, die häufig verwendet werden, um die grundlegende Klassifizierung und visuelle Darstellung eines tragbaren Geräts zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="7d35c-104">The **WPD\_DEVICE\_TYPES** enumeration type describes the different Windows Portable Device (WPD) types commonly used to determine the basic classification and visual appearance of a portable device.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d35c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7d35c-105">Syntax</span></span>


```C++
typedef enum tagWPD_DEVICE_TYPES { 
  WPD_DEVICE_TYPE_GENERIC                       = 0,
  WPD_DEVICE_TYPE_CAMERA                        = 1,
  WPD_DEVICE_TYPE_MEDIA_PLAYER                  = 2,
  WPD_DEVICE_TYPE_PHONE                         = 3,
  WPD_DEVICE_TYPE_VIDEO                         = 4,
  WPD_DEVICE_TYPE_PERSONAL_INFORMATION_MANAGER  = 5,
  WPD_DEVICE_TYPE_AUDIO_RECORDER                = 6
} WPD_DEVICE_TYPES;
```



## <a name="constants"></a><span data-ttu-id="7d35c-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="7d35c-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="7d35c-107"><span id="WPD_DEVICE_TYPE_GENERIC"></span><span id="wpd_device_type_generic"></span>**WPD \_ - \_ Gerätetyp \_ generisch**</span><span class="sxs-lookup"><span data-stu-id="7d35c-107"><span id="WPD_DEVICE_TYPE_GENERIC"></span><span id="wpd_device_type_generic"></span>**WPD\_DEVICE\_TYPE\_GENERIC**</span></span>
</dt> <dd>

<span data-ttu-id="7d35c-108">Ein generisches WPD, das Multifunktionsgeräte enthält, die nicht in einen der anderen Enumerationswerte für [**WPD- \_ Geräte \_ Typen**](wpd-device-types.md) fallen.</span><span class="sxs-lookup"><span data-stu-id="7d35c-108">A generic WPD that includes multifunction devices that do not fall into one of the other [**WPD\_DEVICE\_TYPES**](wpd-device-types.md) enumeration values.</span></span>

</dd> <dt>

<span data-ttu-id="7d35c-109"><span id="WPD_DEVICE_TYPE_CAMERA"></span><span id="wpd_device_type_camera"></span>**WPD \_ - \_ Gerätetyp \_ Kamera**</span><span class="sxs-lookup"><span data-stu-id="7d35c-109"><span id="WPD_DEVICE_TYPE_CAMERA"></span><span id="wpd_device_type_camera"></span>**WPD\_DEVICE\_TYPE\_CAMERA**</span></span>
</dt> <dd>

<span data-ttu-id="7d35c-110">Ein Kamera Gerät, z. b. eine digitale Kamera.</span><span class="sxs-lookup"><span data-stu-id="7d35c-110">A camera device, such as a digital still camera.</span></span>

</dd> <dt>

<span data-ttu-id="7d35c-111"><span id="WPD_DEVICE_TYPE_MEDIA_PLAYER"></span><span id="wpd_device_type_media_player"></span>**WPD \_ - \_ Gerätetyp \_ Media \_ Player**</span><span class="sxs-lookup"><span data-stu-id="7d35c-111"><span id="WPD_DEVICE_TYPE_MEDIA_PLAYER"></span><span id="wpd_device_type_media_player"></span>**WPD\_DEVICE\_TYPE\_MEDIA\_PLAYER**</span></span>
</dt> <dd>

<span data-ttu-id="7d35c-112">Ein Media Player-Gerät, das das Abspielen von Audiodaten, Videos oder Anzeigen von Bildern unterstützt, wie z. b. ein portabler Musikplayer oder ein portables</span><span class="sxs-lookup"><span data-stu-id="7d35c-112">A media player device that supports playing audio, video, or viewing pictures, such as a portable music player or portable media center.</span></span> <span data-ttu-id="7d35c-113">Nicht alle diese Funktionen werden als WPD- \_ \_ Gerätetyp \_ Media Player klassifiziert \_ .</span><span class="sxs-lookup"><span data-stu-id="7d35c-113">Not all of this functionally is classified as a WPD\_DEVICE\_TYPE\_MEDIA\_PLAYER.</span></span> <span data-ttu-id="7d35c-114">Beispielsweise werden Portable Music Player-Geräte als WPD- \_ \_ Gerätetyp \_ Media \_ Player klassifiziert.</span><span class="sxs-lookup"><span data-stu-id="7d35c-114">For example, portable music player devices are classified as WPD\_DEVICE\_TYPE\_MEDIA\_PLAYER.</span></span>

</dd> <dt>

<span data-ttu-id="7d35c-115"><span id="WPD_DEVICE_TYPE_PHONE"></span><span id="wpd_device_type_phone"></span>**WPD \_ - \_ Gerätetyp \_ Telefon**</span><span class="sxs-lookup"><span data-stu-id="7d35c-115"><span id="WPD_DEVICE_TYPE_PHONE"></span><span id="wpd_device_type_phone"></span>**WPD\_DEVICE\_TYPE\_PHONE**</span></span>
</dt> <dd>

<span data-ttu-id="7d35c-116">Ein Telefongerät, z. b. ein Mobiltelefon.</span><span class="sxs-lookup"><span data-stu-id="7d35c-116">A phone device, such as a mobile phone.</span></span>

</dd> <dt>

<span data-ttu-id="7d35c-117"><span id="WPD_DEVICE_TYPE_VIDEO"></span><span id="wpd_device_type_video"></span>**Video zum WPD- \_ \_ Gerätetyp \_**</span><span class="sxs-lookup"><span data-stu-id="7d35c-117"><span id="WPD_DEVICE_TYPE_VIDEO"></span><span id="wpd_device_type_video"></span>**WPD\_DEVICE\_TYPE\_VIDEO**</span></span>
</dt> <dd>

<span data-ttu-id="7d35c-118">Ein Videogerät.</span><span class="sxs-lookup"><span data-stu-id="7d35c-118">A video device.</span></span>

</dd> <dt>

<span data-ttu-id="7d35c-119"><span id="WPD_DEVICE_TYPE_PERSONAL_INFORMATION_MANAGER"></span><span id="wpd_device_type_personal_information_manager"></span>**WPD \_ - \_ Gerätetyp \_ Personal \_ Information \_ Manager**</span><span class="sxs-lookup"><span data-stu-id="7d35c-119"><span id="WPD_DEVICE_TYPE_PERSONAL_INFORMATION_MANAGER"></span><span id="wpd_device_type_personal_information_manager"></span>**WPD\_DEVICE\_TYPE\_PERSONAL\_INFORMATION\_MANAGER**</span></span>
</dt> <dd>

<span data-ttu-id="7d35c-120">Ein persönliches Informations-Manager-Gerät.</span><span class="sxs-lookup"><span data-stu-id="7d35c-120">A personal information manager device.</span></span>

</dd> <dt>

<span data-ttu-id="7d35c-121"><span id="WPD_DEVICE_TYPE_AUDIO_RECORDER"></span><span id="wpd_device_type_audio_recorder"></span>**WPD \_ \_ \_ -Gerätetyp \_ Audiorecorder**</span><span class="sxs-lookup"><span data-stu-id="7d35c-121"><span id="WPD_DEVICE_TYPE_AUDIO_RECORDER"></span><span id="wpd_device_type_audio_recorder"></span>**WPD\_DEVICE\_TYPE\_AUDIO\_RECORDER**</span></span>
</dt> <dd>

<span data-ttu-id="7d35c-122">Ein audioaufzeichnungs Gerät.</span><span class="sxs-lookup"><span data-stu-id="7d35c-122">An audio recorder device.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7d35c-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7d35c-123">Remarks</span></span>

<span data-ttu-id="7d35c-124">**WPD \_ Geräte \_ Typen** werden mithilfe der [**iportableendvicemanager**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager) -Schnittstelle gelesen.</span><span class="sxs-lookup"><span data-stu-id="7d35c-124">**WPD\_DEVICE\_TYPES** are read using the [**IPortableDeviceManager**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager) interface.</span></span> <span data-ttu-id="7d35c-125">WPD-Anwendungen können diese Werte verwenden, um die generische visuelle Darstellung des Geräts zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="7d35c-125">WPD applications may use these values to determine the generic visual appearance of the device.</span></span> <span data-ttu-id="7d35c-126">Das heißt, ein Kamerabild wird für Kamera ähnliche Geräte angezeigt, ein Mobil telefonbild wird für Telefon ähnliche Geräte angezeigt usw.</span><span class="sxs-lookup"><span data-stu-id="7d35c-126">That is, a camera picture is displayed for camera-like devices, a mobile phone picture is displayed for phone-like devices, and so on.</span></span>

> [!Note]  
> <span data-ttu-id="7d35c-127">WPD-Anwendungen müssen die Funktionen des portablen Geräts verwenden, um funktionell und nicht den Wert der **WPD- \_ Geräte \_ Typen** zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="7d35c-127">WPD applications must use the capabilities of the portable device to determine functionally, not the **WPD\_DEVICE\_TYPES** value.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="7d35c-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7d35c-128">Requirements</span></span>



| <span data-ttu-id="7d35c-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7d35c-129">Requirement</span></span> | <span data-ttu-id="7d35c-130">Wert</span><span class="sxs-lookup"><span data-stu-id="7d35c-130">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d35c-131">Header</span><span class="sxs-lookup"><span data-stu-id="7d35c-131">Header</span></span><br/> | <dl> <span data-ttu-id="7d35c-132"><dt>Portabledevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="7d35c-132"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7d35c-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7d35c-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d35c-134">**Strukturen und Enumerationstypen**</span><span class="sxs-lookup"><span data-stu-id="7d35c-134">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




