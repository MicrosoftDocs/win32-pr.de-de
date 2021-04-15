---
title: DRM_INDIVIDUALIZATION_STATUS-Enumeration (drmexternals. h)
description: Der DRM- \_ Individualisierungs \_ Status-Enumerationstyp definiert die gültigen Zustände für die DRM-Individualisierung. | DRM_INDIVIDUALIZATION_STATUS-Enumeration (drmexternals. h)
ms.assetid: 76748fb3-340e-47e2-969d-5e857bb4e4d8
keywords:
- DRM_INDIVIDUALIZATION_STATUS-Enumeration Windows Media-Format
- Enumeration Windows Media-Format
topic_type:
- apiref
api_name:
- DRM_INDIVIDUALIZATION_STATUS
api_location:
- Drmexternals.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8d59a19c58c775ee22d78e17bc09add2825948e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104394025"
---
# <a name="drm_individualization_status-enumeration-drmexternalsh"></a>DRM_INDIVIDUALIZATION_STATUS-Enumeration (drmexternals. h)

Der **DRM- \_ Individualisierungs \_ Status** -Enumerationstyp definiert die gültigen Zustände für die DRM- [*Individualisierung*](wmformat-glossary.md). Wenn eine Anwendung mit einem Aufruf von [**iwmdrmreader:: Individual**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-individualize)eine Individualisierung initiiert, wird der Fortschritt der Individualisierungs Anforderung durch Aufrufe der [**iwmstatuscallback:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) -Methode an die Anwendung übermittelt. In den Individualisierungs Statusmeldungen wird das WMT-Element \_ Individual des Enumerationstyps [**WMT \_**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_status) als *Status* Parameter verwendet. Der Status der Individualisierung wird im *pValue* -Parameter an **OnStatus** übergeben.

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

Gibt an, dass der Individualisierungsprozess aufgrund eines Aufrufes von [**iwmdrmreader:: cancelindividualization**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-cancelindividualization)abgebrochen wurde.

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

Diese Enumeration wird von der [**WM \_ Individual \_ Status**](wm-individualize-status.md) -Struktur verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                      |
| Version<br/>                  | SDK für Windows Media-Format 7 oder höhere Versionen des SDKs<br/>                       |
| Header<br/>                   | <dl> <dt>Drmexternals. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**DRM- \_ http- \_ Status**](drm-http-status.md)
</dt> <dt>

[**Enumerationstypen**](enumeration-types.md)
</dt> </dl>

 

 





