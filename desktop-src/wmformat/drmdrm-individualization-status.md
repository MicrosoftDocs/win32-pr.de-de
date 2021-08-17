---
title: DRM_INDIVIDUALIZATION_STATUS -Enumeration (Wmdrmsdk.h)
description: Der DRM \_ INDIVIDUALIZATION \_ STATUS-Enumerationstyp definiert die gültigen Zustände für die DRM-Individualisierung. | DRM_INDIVIDUALIZATION_STATUS -Enumeration (Wmdrmsdk.h)
ms.assetid: 4e6712e2-3297-4636-9b0c-07269bd63d52
keywords:
- DRM_INDIVIDUALIZATION_STATUS enumeration windows Media Format
- Windows Media-Enumerationsformat
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
ms.openlocfilehash: 47e339fda95ccf7408ad2f218179cfb591da217b16fbbce9c9870eabd7437eaf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117848226"
---
# <a name="drm_individualization_status-enumeration-wmdrmsdkh"></a>DRM_INDIVIDUALIZATION_STATUS -Enumeration (Wmdrmsdk.h)

Der **DRM \_ INDIVIDUALIZATION \_ STATUS-Enumerationstyp** definiert die gültigen Zustände für die DRM-Individualisierung.

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

<span id="INDI_UNDEFINED"></span><span id="indi_undefined"></span>**INDI \_ UNDEFINED**
</dt> <dd>

Dieser Wert ist für die zukünftige Verwendung reserviert.

</dd> <dt>

<span id="INDI_BEGIN"></span><span id="indi_begin"></span>**INDI \_ BEGIN**
</dt> <dd>

Gibt den Anfang des Individualisierungsprozesses an.

</dd> <dt>

<span id="INDI_SUCCEED"></span><span id="indi_succeed"></span>**INDI \_ SUCCEED**
</dt> <dd>

Gibt an, dass der Individualisierungsprozess abgeschlossen wurde.

</dd> <dt>

<span id="INDI_FAIL"></span><span id="indi_fail"></span>**INDI \_ FAIL**
</dt> <dd>

Gibt an, dass der Individualisierungsprozess fehlgeschlagen ist.

</dd> <dt>

<span id="INDI_CANCEL"></span><span id="indi_cancel"></span>**INDI \_ CANCEL**
</dt> <dd>

Gibt an, dass der Individualisierungsprozess von der Anwendung abgebrochen wurde.

</dd> <dt>

<span id="INDI_DOWNLOAD"></span><span id="indi_download"></span>**\_INDI-DOWNLOAD**
</dt> <dd>

Gibt an, dass das Sicherheitsupgrade heruntergeladen wird.

</dd> <dt>

<span id="INDI_INSTALL"></span><span id="indi_install"></span>**\_INDI-INSTALLATION**
</dt> <dd>

Gibt an, dass das Sicherheitsupgrade installiert wird.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Diese Enumeration wird von der [**WM \_ INDIVIDUALIZE \_ STATUS-Struktur**](drmwm-individualize-status.md) verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Enumerationstypen**](drm-enumeration-types.md)
</dt> </dl>

 

 





