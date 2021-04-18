---
title: WMDRMNET_POLICY_TYPE-Enumeration (wmdrmsdk. h)
description: Der Enumerationstyp wmdrmnet- \_ \_ Richtlinientyp listet die Typen von Richtlinien auf, die für Windows Media DRM für Netzwerkgeräte Vorgänge verfügbar sind.
ms.assetid: 83e9e247-3bd8-4857-97b6-95b3cd5ad25c
keywords:
- WMDRMNET_POLICY_TYPE-Enumeration Windows Media-Format
- Enumeration Windows Media-Format
topic_type:
- apiref
api_name:
- WMDRMNET_POLICY_TYPE
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 964a3e938caa312f02f21074f046f3cf88d72de6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365710"
---
# <a name="wmdrmnet_policy_type-enumeration"></a>Wmdrmnet \_ - \_ Richtlinientyp-Enumeration

Der Enumerationstyp **wmdrmnet- \_ \_ Richtlinientyp** listet die Typen von Richtlinien auf, die für Windows Media DRM für Netzwerkgeräte Vorgänge verfügbar sind.

## <a name="syntax"></a>Syntax


```C++
typedef enum WMDRMNET_POLICY_TYPE { 
  WMDRMNET_POLICY_TYPE_UNDEFINED       = 0x0000,
  WMDRMNET_POLICY_TYPE_TRANSCRYPTPLAY  = 0x0001
} ;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="WMDRMNET_POLICY_TYPE_UNDEFINED"></span><span id="wmdrmnet_policy_type_undefined"></span>**wmdrmnet \_ - \_ Richtlinientyp nicht \_ definiert**
</dt> <dd>

Nicht definierte Richtlinien Typen werden nicht unterstützt.

</dd> <dt>

<span id="WMDRMNET_POLICY_TYPE_TRANSCRYPTPLAY"></span><span id="wmdrmnet_policy_type_transcryptplay"></span>**wmdrmnet \_ - \_ Richtlinientyp \_ transryptplay**
</dt> <dd>

Die Richtlinie steuert die Fähigkeit zum Konvertieren von Inhalten, die von Windows Media DRM geschützt werden, in geschützte Windows Media DRM für Netzwerkgeräte Daten und die Wiedergabe auf einem vernetzten Gerät.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Keine.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Enumerationstypen**](drm-enumeration-types.md)
</dt> <dt>

[**wmdrmnet- \_ Richtlinie**](wmdrmnet-policy.md)
</dt> </dl>

 

 





