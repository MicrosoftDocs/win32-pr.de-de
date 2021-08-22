---
description: Der WPD DEVICE TYPES-Enumerationstyp beschreibt die verschiedenen Windows \_ Portable Device (WPD)-Typen, die häufig verwendet werden, um die grundlegende Klassifizierung und visuelle Darstellung eines portablen \_ Geräts zu bestimmen.
ms.assetid: 51714e0f-e9b7-4474-a8bb-da3875ef5399
title: WPD_DEVICE_TYPES -Enumeration (PortableDevice.h)
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
ms.openlocfilehash: 747c4631bc2c24a6550904e36e58a6fc02547bc010da7fa1d08b896c6c17489c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119657460"
---
# <a name="wpd_device_types-enumeration"></a>WPD \_ DEVICE \_ TYPES-Enumeration

Der **WPD \_ DEVICE TYPES-Enumerationstyp \_** beschreibt die verschiedenen Windows Portable Device (WPD)-Typen, die häufig verwendet werden, um die grundlegende Klassifizierung und visuelle Darstellung eines portablen Geräts zu bestimmen.

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

<span id="WPD_DEVICE_TYPE_GENERIC"></span><span id="wpd_device_type_generic"></span>**\_WPD-GERÄTETYP \_ \_ GENERISCH**
</dt> <dd>

Ein generisches WPD, das Multifunktionsgeräte enthält, die nicht in einen der anderen [**WPD \_ DEVICE \_ TYPES-Enumerationswerte**](wpd-device-types.md) fallen.

</dd> <dt>

<span id="WPD_DEVICE_TYPE_CAMERA"></span><span id="wpd_device_type_camera"></span>**\_ \_ WPD-GERÄTETYPKAMERA \_**
</dt> <dd>

Ein Kameragerät, z. B. eine digitale Stillkamera.

</dd> <dt>

<span id="WPD_DEVICE_TYPE_MEDIA_PLAYER"></span><span id="wpd_device_type_media_player"></span>**\_ \_ WPD-GERÄTETYP \_ MEDIA \_ PLAYER**
</dt> <dd>

Ein Medienplayergerät, das die Wiedergabe von Audio, Video oder das Anzeigen von Bildern unterstützt, z. B. einen portablen Musikplayer oder ein portables Mediencenter. Nicht all dies ist funktional als WPD \_ DEVICE TYPE MEDIA PLAYER \_ \_ \_ klassifiziert. Beispielsweise werden portable Musikplayergeräte als WPD \_ DEVICE TYPE MEDIA PLAYER \_ \_ \_ klassifiziert.

</dd> <dt>

<span id="WPD_DEVICE_TYPE_PHONE"></span><span id="wpd_device_type_phone"></span>**\_ \_ WPD-GERÄTETYP \_ TELEFON**
</dt> <dd>

Ein Telefongerät, z. B. ein Mobiltelefon.

</dd> <dt>

<span id="WPD_DEVICE_TYPE_VIDEO"></span><span id="wpd_device_type_video"></span>**VIDEO ZUM \_ \_ WPD-GERÄTETYP \_**
</dt> <dd>

Ein Videogerät.

</dd> <dt>

<span id="WPD_DEVICE_TYPE_PERSONAL_INFORMATION_MANAGER"></span><span id="wpd_device_type_personal_information_manager"></span>**\_ \_ WPD-GERÄTETYP \_ PERSONAL INFORMATION \_ \_ MANAGER**
</dt> <dd>

Ein Persönliches Informations-Manager-Gerät.

</dd> <dt>

<span id="WPD_DEVICE_TYPE_AUDIO_RECORDER"></span><span id="wpd_device_type_audio_recorder"></span>**WPD \_ DEVICE \_ TYPE \_ AUDIO \_ RECORDER**
</dt> <dd>

Ein Audioaufzeichnungsgerät.

</dd> </dl>

## <a name="remarks"></a>Hinweise

**WPD \_ \_GERÄTETYPEN** werden mithilfe der [**IPortableDeviceManager-Schnittstelle**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager) gelesen. WPD-Anwendungen können diese Werte verwenden, um die generische visuelle Darstellung des Geräts zu bestimmen. Das heißt, ein Kamerabild wird für kamerabasierte Geräte angezeigt, ein Mobiltelefonbild für telefonbasierte Geräte und so weiter.

> [!Note]  
> WPD-Anwendungen müssen die Funktionen des portablen Geräts verwenden, um die Funktionsfähigkeit zu bestimmen, nicht den **WpD \_ DEVICE \_ TYPES-Wert.**

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Strukturen und Enumerationstypen**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




