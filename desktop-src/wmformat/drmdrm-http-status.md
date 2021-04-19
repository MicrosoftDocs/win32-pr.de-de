---
title: DRM_HTTP_STATUS-Enumeration (wmdrmsdk. h)
description: Der DRM- \_ http- \_ statusenumerationstyp definiert einen Bereich von http-Zuständen für eine DRM-Anforderung.
ms.assetid: 09183ef9-4832-4469-a960-dbeb67381949
keywords:
- DRM_HTTP_STATUS-Enumeration Windows Media-Format
- Enumeration Windows Media-Format
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
ms.openlocfilehash: 367c5a40af45fd573f7f5033b9be3b037079cb30
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356045"
---
# <a name="drm_http_status-enumeration-wmdrmsdkh"></a>DRM_HTTP_STATUS-Enumeration (wmdrmsdk. h)

Der **DRM- \_ http- \_ statusenumerationstyp** definiert einen Bereich von http-Zuständen für eine DRM-Anforderung.

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

Diese Enumeration wird von der [**WM \_ Individual \_ Status**](drmwm-individualize-status.md) -Struktur verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Enumerationstypen**](drm-enumeration-types.md)
</dt> </dl>

 

 





