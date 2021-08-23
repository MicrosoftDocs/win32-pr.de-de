---
title: DRM_INDIVIDUALIZATION_STATUS-Enumeration (Drmexternals.h)
description: Der DRM \_ INDIVIDUALIZATION \_ STATUS-Enumerationstyp definiert die gültigen Zustände für die DRM-Individualisierung. | DRM_INDIVIDUALIZATION_STATUS-Enumeration (Drmexternals.h)
ms.assetid: 76748fb3-340e-47e2-969d-5e857bb4e4d8
keywords:
- DRM_INDIVIDUALIZATION_STATUS enumeration windows Media Format
- Enumerationsfenster Medienformat
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
ms.openlocfilehash: 081a8714d29cb48236bdb9191c15e92db96b18a9f8c1d9c2388c5baee7783296
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119705650"
---
# <a name="drm_individualization_status-enumeration-drmexternalsh"></a>DRM_INDIVIDUALIZATION_STATUS-Enumeration (Drmexternals.h)

Der **DRM \_ INDIVIDUALIZATION STATUS-Enumerationstyp \_** definiert die gültigen Zustände für die DRM-Individualisierung. [](wmformat-glossary.md) Wenn eine Anwendung die Individualisierung mit einem Aufruf von [**IWMDRMReader::Individualize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-individualize)initiiert, wird der Fortschritt der Individualisierungsanforderung durch Aufrufe der [**IWMStatusCallback::OnStatus-Methode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) an die Anwendung übermittelt. Individualisierungsstatusmeldungen verwenden alle den WMT \_ INDIVIDUALIZE-Member des [**WMT STATUS-Enumerationstyps \_**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_status) als *Statusparameter.* Der Status der Individualisierung wird im *pValue-Parameter* an **OnStatus** übergeben.

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

Gibt den Beginn des Individualisierungsprozesses an.

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

Gibt an, dass der Individualisierungsprozess als Ergebnis eines Aufrufs von [**IWMDRMReader::CancelIndividualization**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-cancelindividualization)abgebrochen wurde.

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

Diese Enumeration wird von der [**WM \_ INDIVIDUALIZE \_ STATUS-Struktur**](wm-individualize-status.md) verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                      |
| Version<br/>                  | Windows Media Format 7 SDK oder höhere Versionen des SDK<br/>                       |
| Header<br/>                   | <dl> <dt>Drmexternals.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**\_DRM-HTTP-STATUS \_**](drm-http-status.md)
</dt> <dt>

[**Enumerationstypen**](enumeration-types.md)
</dt> </dl>

 

 





