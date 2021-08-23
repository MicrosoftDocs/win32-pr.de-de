---
title: DRM_HTTP_STATUS -Enumeration (Drmexternals.h)
description: Der DRM \_ HTTP \_ STATUS-Enumerationstyp definiert einen Bereich von Status für eine DRM-Anforderung.
ms.assetid: 9e0fb060-3fbf-45d0-872b-4d666ea9a88d
keywords:
- DRM_HTTP_STATUS enumeration windows Media Format
- Windows Media-Enumerationsformat
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
ms.openlocfilehash: e222cbf24e6333c7105e8564a5ad255693340749aeea32d98bd013bcb40995d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119586300"
---
# <a name="drm_http_status-enumeration-drmexternalsh"></a>DRM_HTTP_STATUS -Enumeration (Drmexternals.h)

Der **DRM \_ HTTP \_ STATUS-Enumerationstyp** definiert einen Bereich von Status für eine [*DRM-Anforderung.*](wmformat-glossary.md)

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

<span id="HTTP_NOTINITIATED"></span><span id="http_notinitiated"></span>**HTTP \_ NOTINITIATED**
</dt> <dd>

Die HTTP-Vorgänge wurden nicht initiiert.

</dd> <dt>

<span id="HTTP_CONNECTING"></span><span id="http_connecting"></span>**\_HTTP-VERBINDUNG**
</dt> <dd>

Die Verbindung wird hergestellt.

</dd> <dt>

<span id="HTTP_REQUESTING"></span><span id="http_requesting"></span>**\_HTTP-ANFORDERUNG**
</dt> <dd>

Daten werden angefordert.

</dd> <dt>

<span id="HTTP_RECEIVING"></span><span id="http_receiving"></span>**\_HTTP-EMPFANG**
</dt> <dd>

Daten werden empfangen.

</dd> <dt>

<span id="HTTP_COMPLETED"></span><span id="http_completed"></span>**HTTP \_ COMPLETED**
</dt> <dd>

Die HTTP-Vorgänge sind abgeschlossen.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Diese Enumeration wird von der [**WM \_ INDIVIDUALIZE \_ STATUS-Struktur**](wm-individualize-status.md) verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                      |
| Version<br/>                  | Windows Media Format 7 SDK oder neuere Versionen des SDK<br/>                       |
| Header<br/>                   | <dl> <dt>Drmexternals.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_DRM-INDIVIDUALISIERUNGSSTATUS \_**](drm-individualization-status.md)
</dt> <dt>

[**Enumerationstypen**](enumeration-types.md)
</dt> </dl>

 

 





