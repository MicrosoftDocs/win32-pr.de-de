---
title: DRM_HTTP_STATUS-Enumeration (Wmdrmsdk.h)
description: Der \_ \_ DRM-HTTP-STATUS-Enumerationstyp definiert einen Bereich von HTTP-Zuständen für eine DRM-Anforderung.
ms.assetid: 09183ef9-4832-4469-a960-dbeb67381949
keywords:
- DRM_HTTP_STATUS-Enumerationsfenster Media Format
- Enumerationsfenster Medienformat
topic_type:
- apiref
api_name:
- DRM_HTTP_STATUS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 385a52811cc8deb7e1c221737bd97391122160de065ca28111132ee6c5e4a859
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119447760"
---
# <a name="drm_http_status-enumeration-wmdrmsdkh"></a>DRM_HTTP_STATUS-Enumeration (Wmdrmsdk.h)

Der **\_ DRM-HTTP-STATUS-Enumerationstyp \_** definiert einen Bereich von HTTP-Zuständen für eine DRM-Anforderung.

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

<span id="HTTP_NOTINITIATED"></span><span id="http_notinitiated"></span>**HTTP \_ NICHT INITIIERT**
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

<span id="HTTP_COMPLETED"></span><span id="http_completed"></span>**HTTP \_ ABGESCHLOSSEN**
</dt> <dd>

Die HTTP-Vorgänge sind abgeschlossen.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Diese Enumeration wird von der [**WM \_ INDIVIDUALIZE \_ STATUS-Struktur**](drmwm-individualize-status.md) verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[**Enumerationstypen**](drm-enumeration-types.md)
</dt> </dl>

 

 





