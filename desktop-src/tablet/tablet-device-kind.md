---
description: Gibt den Typ des Tablettgeräts an, z. B. einen Stift, eine Maus oder einen touchabhängigen Digitizer.
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
ms.openlocfilehash: 784e2393f5470f8abd966ca6dbdce3ac9d9bff734f1245ebd0ef169180c62d79
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119820180"
---
# <a name="tablet_device_kind-enumeration"></a>TABLET \_ DEVICE \_ KIND-Enumeration

Gibt den Typ des Tablettgeräts an, z. B. einen Stift, eine Maus oder einen touchabhängigen Digitizer.

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

<span id="TABLET_DEVICE_MOUSE"></span><span id="tablet_device_mouse"></span>**MAUS \_ DES TABLET-GERÄTS \_**
</dt> <dd>

Das Tablet ist eine Maus. Dies schließt Touchpads ein, die auf vielen Laptopcomputern gefunden werden.

</dd> <dt>

<span id="TABLET_DEVICE_PEN"></span><span id="tablet_device_pen"></span>**TABLET \_ DEVICE \_ PEN**
</dt> <dd>

Das Tablet verwendet einen Stift und einen Digitizer.

</dd> <dt>

<span id="TABLET_DEVICE_TOUCH"></span><span id="tablet_device_touch"></span>**TABLET \_ DEVICE \_ TOUCH**
</dt> <dd>

Das Tablet verwendet einen touchabhängigen Digitizer.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ITablet2::GetDeviceKind-Methode**](itablet2-getdevicekind.md)
</dt> </dl>

 

 




