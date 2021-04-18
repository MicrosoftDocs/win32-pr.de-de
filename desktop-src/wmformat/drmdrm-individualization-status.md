---
title: DRM_INDIVIDUALIZATION_STATUS-Enumeration (wmdrmsdk. h)
description: Der DRM- \_ Individualisierungs \_ Status-Enumerationstyp definiert die gültigen Zustände für die DRM-Individualisierung. | DRM_INDIVIDUALIZATION_STATUS-Enumeration (wmdrmsdk. h)
ms.assetid: 4e6712e2-3297-4636-9b0c-07269bd63d52
keywords:
- DRM_INDIVIDUALIZATION_STATUS-Enumeration Windows Media-Format
- Enumeration Windows Media-Format
topic_type:
- apiref
api_name:
- DRM_INDIVIDUALIZATION_STATUS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b395d3ad4271ccef9964f0d39c74a1e0ba158257
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361443"
---
# <a name="drm_individualization_status-enumeration-wmdrmsdkh"></a>DRM_INDIVIDUALIZATION_STATUS-Enumeration (wmdrmsdk. h)

Der **DRM- \_ Individualisierungs \_ Status** -Enumerationstyp definiert die gültigen Zustände für die DRM-Individualisierung.

## <a name="syntax"></a>Syntax


```C++
typedef enum DRM_INDIVIDUALIZATION_STATUS { 
  INDI_UNDEFINED  = 0x0000,
  INDI_BEGIN      = 0x0001,
  INDI_SUCCEED    = 0x0002,
  INDI_FAIL       = 0x0004,
  INDI_CANCEL     = 0x0008,
  INDI_DOWNLOAD   = 0x0010,
  INDI_INSTALL    = 0x0020
} ;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="INDI_UNDEFINED"></span><span id="indi_undefined"></span>**Indi nicht \_ definiert**
</dt> <dd>

Dieser Wert ist für die zukünftige Verwendung reserviert.

</dd> <dt>

<span id="INDI_BEGIN"></span><span id="indi_begin"></span>**Indi \_ Begin**
</dt> <dd>

Gibt den Beginn des Individualisierungs Vorgangs an.

</dd> <dt>

<span id="INDI_SUCCEED"></span><span id="indi_succeed"></span>**Indi \_ erfolgreich**
</dt> <dd>

Gibt an, dass der Individualisierungsprozess abgeschlossen wurde.

</dd> <dt>

<span id="INDI_FAIL"></span><span id="indi_fail"></span>**Indi \_ Fail**
</dt> <dd>

Gibt an, dass der Individualisierungsprozess fehlgeschlagen ist.

</dd> <dt>

<span id="INDI_CANCEL"></span><span id="indi_cancel"></span>**Indi \_ Abbrechen**
</dt> <dd>

Gibt an, dass der Individualisierungsprozess von der Anwendung abgebrochen wurde.

</dd> <dt>

<span id="INDI_DOWNLOAD"></span><span id="indi_download"></span>**Indi \_ herunterladen**
</dt> <dd>

Gibt an, dass das Sicherheits Upgrade heruntergeladen wird.

</dd> <dt>

<span id="INDI_INSTALL"></span><span id="indi_install"></span>**Indi- \_ Installation**
</dt> <dd>

Gibt an, dass das Sicherheits Upgrade installiert wird.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Enumeration wird von der [**WM \_ Individual \_ Status**](drmwm-individualize-status.md) -Struktur verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Enumerationstypen**](drm-enumeration-types.md)
</dt> </dl>

 

 





