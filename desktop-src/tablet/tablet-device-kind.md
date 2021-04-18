---
description: Gibt den Typ des Tablettgeräts an, z. b. einen Stift, eine Maus oder einen Fingerabdruck-Digitalisierungs
ms.assetid: 4cca1e09-99c0-4357-a6ef-159bc8d17d57
title: TABLET_DEVICE_KIND-Enumeration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TABLET_DEVICE_KIND
api_type:
- NA
api_location: ''
ms.openlocfilehash: 18f691a2fa909ef28059a4788f4f8b4e184a61ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351129"
---
# <a name="tablet_device_kind-enumeration"></a>Tablet \_ Device \_ Kind-Enumeration

Gibt den Typ des Tablettgeräts an, z. b. einen Stift, eine Maus oder einen Fingerabdruck-Digitalisierungs

## <a name="syntax"></a>Syntax


```C++
typedef enum _TABLET_DEVICE_KIND { 
  TABLET_DEVICE_MOUSE  = 0,
  TABLET_DEVICE_PEN,
  TABLET_DEVICE_TOUCH
} TABLET_DEVICE_KIND;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="TABLET_DEVICE_MOUSE"></span><span id="tablet_device_mouse"></span>**\_Tablettgerät- \_ Maus**
</dt> <dd>

Das Tablet ist eine Maus. Dies schließt Touchpads ein, die auf vielen Laptop Computern gefunden wurden.

</dd> <dt>

<span id="TABLET_DEVICE_PEN"></span><span id="tablet_device_pen"></span>**\_Tablettgerät \_ Stift**
</dt> <dd>

Das Tablet verwendet einen elektromagnetischen Stift und Digitalisierer.

</dd> <dt>

<span id="TABLET_DEVICE_TOUCH"></span><span id="tablet_device_touch"></span>**Tablet \_ Gerät \_ berühren**
</dt> <dd>

Das Tablet verwendet einen Fingerabdruck der Fingereingabe.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ITablet2:: getdevicekind-Methode**](itablet2-getdevicekind.md)
</dt> </dl>

 

 




