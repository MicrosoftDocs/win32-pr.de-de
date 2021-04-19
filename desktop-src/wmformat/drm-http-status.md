---
title: DRM_HTTP_STATUS-Enumeration (drmexternals. h)
description: Der DRM- \_ http- \_ statusenumerationstyp definiert einen Bereich von Zuständen für eine DRM-Anforderung.
ms.assetid: 9e0fb060-3fbf-45d0-872b-4d666ea9a88d
keywords:
- DRM_HTTP_STATUS-Enumeration Windows Media-Format
- Enumeration Windows Media-Format
topic_type:
- apiref
api_name:
- DRM_HTTP_STATUS
api_location:
- Drmexternals.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93d61803cab6cb80932402e429e77228a1611fd9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339997"
---
# <a name="drm_http_status-enumeration-drmexternalsh"></a>DRM_HTTP_STATUS-Enumeration (drmexternals. h)

Der **DRM- \_ http- \_ statusenumerationstyp** definiert einen Bereich von Zuständen für eine [*DRM*](wmformat-glossary.md) -Anforderung.

## <a name="syntax"></a>Syntax


```C++
typedef enum DRM_HTTP_STATUS { 
  HTTP_NOTINITIATED  = 0,
  HTTP_CONNECTING    = 1,
  HTTP_REQUESTING    = 2,
  HTTP_RECEIVING     = 3,
  HTTP_COMPLETED     = 4
} ;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="HTTP_NOTINITIATED"></span><span id="http_notinitiated"></span>**HTTP \_ notinitiierte**
</dt> <dd>

Die http-Vorgänge wurden nicht initiiert.

</dd> <dt>

<span id="HTTP_CONNECTING"></span><span id="http_connecting"></span>**HTTP- \_ Verbindung**
</dt> <dd>

Die Verbindung wird hergestellt.

</dd> <dt>

<span id="HTTP_REQUESTING"></span><span id="http_requesting"></span>**HTTP- \_ Anforderung**
</dt> <dd>

Es werden Daten angefordert.

</dd> <dt>

<span id="HTTP_RECEIVING"></span><span id="http_receiving"></span>**HTTP- \_ Empfang**
</dt> <dd>

Daten werden empfangen.

</dd> <dt>

<span id="HTTP_COMPLETED"></span><span id="http_completed"></span>**HTTP \_ abgeschlossen**
</dt> <dd>

Die http-Vorgänge sind fertiggestellt.

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

[**DRM- \_ Individualisierungs \_ Status**](drm-individualization-status.md)
</dt> <dt>

[**Enumerationstypen**](enumeration-types.md)
</dt> </dl>

 

 





