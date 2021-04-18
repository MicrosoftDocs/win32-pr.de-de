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
# <a name="wpd_device_types-enumeration"></a>WPD \_ - \_ Gerätetyp-Enumeration

Der Enumerationstyp " **WPD- \_ Geräte \_ Typen** " beschreibt die verschiedenen Windows Portable Device (WPD)-Typen, die häufig verwendet werden, um die grundlegende Klassifizierung und visuelle Darstellung eines tragbaren Geräts zu bestimmen.

## <a name="syntax"></a>Syntax


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



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="WPD_DEVICE_TYPE_GENERIC"></span><span id="wpd_device_type_generic"></span>**WPD \_ - \_ Gerätetyp \_ generisch**
</dt> <dd>

Ein generisches WPD, das Multifunktionsgeräte enthält, die nicht in einen der anderen Enumerationswerte für [**WPD- \_ Geräte \_ Typen**](wpd-device-types.md) fallen.

</dd> <dt>

<span id="WPD_DEVICE_TYPE_CAMERA"></span><span id="wpd_device_type_camera"></span>**WPD \_ - \_ Gerätetyp \_ Kamera**
</dt> <dd>

Ein Kamera Gerät, z. b. eine digitale Kamera.

</dd> <dt>

<span id="WPD_DEVICE_TYPE_MEDIA_PLAYER"></span><span id="wpd_device_type_media_player"></span>**WPD \_ - \_ Gerätetyp \_ Media \_ Player**
</dt> <dd>

Ein Media Player-Gerät, das das Abspielen von Audiodaten, Videos oder Anzeigen von Bildern unterstützt, wie z. b. ein portabler Musikplayer oder ein portables Nicht alle diese Funktionen werden als WPD- \_ \_ Gerätetyp \_ Media Player klassifiziert \_ . Beispielsweise werden Portable Music Player-Geräte als WPD- \_ \_ Gerätetyp \_ Media \_ Player klassifiziert.

</dd> <dt>

<span id="WPD_DEVICE_TYPE_PHONE"></span><span id="wpd_device_type_phone"></span>**WPD \_ - \_ Gerätetyp \_ Telefon**
</dt> <dd>

Ein Telefongerät, z. b. ein Mobiltelefon.

</dd> <dt>

<span id="WPD_DEVICE_TYPE_VIDEO"></span><span id="wpd_device_type_video"></span>**Video zum WPD- \_ \_ Gerätetyp \_**
</dt> <dd>

Ein Videogerät.

</dd> <dt>

<span id="WPD_DEVICE_TYPE_PERSONAL_INFORMATION_MANAGER"></span><span id="wpd_device_type_personal_information_manager"></span>**WPD \_ - \_ Gerätetyp \_ Personal \_ Information \_ Manager**
</dt> <dd>

Ein persönliches Informations-Manager-Gerät.

</dd> <dt>

<span id="WPD_DEVICE_TYPE_AUDIO_RECORDER"></span><span id="wpd_device_type_audio_recorder"></span>**WPD \_ \_ \_ -Gerätetyp \_ Audiorecorder**
</dt> <dd>

Ein audioaufzeichnungs Gerät.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

**WPD \_ Geräte \_ Typen** werden mithilfe der [**iportableendvicemanager**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager) -Schnittstelle gelesen. WPD-Anwendungen können diese Werte verwenden, um die generische visuelle Darstellung des Geräts zu bestimmen. Das heißt, ein Kamerabild wird für Kamera ähnliche Geräte angezeigt, ein Mobil telefonbild wird für Telefon ähnliche Geräte angezeigt usw.

> [!Note]  
> WPD-Anwendungen müssen die Funktionen des portablen Geräts verwenden, um funktionell und nicht den Wert der **WPD- \_ Geräte \_ Typen** zu bestimmen.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Portabledevice. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Strukturen und Enumerationstypen**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




