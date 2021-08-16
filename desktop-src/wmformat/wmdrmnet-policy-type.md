---
title: WMDRMNET_POLICY_TYPE-Enumeration (Wmdrmsdk.h)
description: Der WMDRMNET \_ POLICY \_ TYPE-Enumerationstyp listet die Typen von Richtlinien auf, die für Windows Medien-DRM für Netzwerkgerätevorgänge verfügbar sind.
ms.assetid: 83e9e247-3bd8-4857-97b6-95b3cd5ad25c
keywords:
- WMDRMNET_POLICY_TYPE-Enumerationsfenster Media Format
- Enumerationsfenster Medienformat
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
ms.openlocfilehash: 8aec574717abb51117b142b8450ad7548d84766b4138f76a4296982422462fbc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118697812"
---
# <a name="wmdrmnet_policy_type-enumeration"></a>WMDRMNET \_ POLICY \_ TYPE-Enumeration

Der **WMDRMNET \_ POLICY TYPE-Enumerationstyp \_** listet die Typen von Richtlinien auf, die für Windows Medien-DRM für Netzwerkgerätevorgänge verfügbar sind.

## <a name="syntax"></a>Syntax


```C++
typedef enum WMDRMNET_POLICY_TYPE { 
  WMDRMNET_POLICY_TYPE_UNDEFINED       = 0x0000,
  WMDRMNET_POLICY_TYPE_TRANSCRYPTPLAY  = 0x0001
} ;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="WMDRMNET_POLICY_TYPE_UNDEFINED"></span><span id="wmdrmnet_policy_type_undefined"></span>**\_WMDRMNET-RICHTLINIENTYP \_ \_ UNDEFINED**
</dt> <dd>

Nicht definierte Richtlinientypen werden nicht unterstützt.

</dd> <dt>

<span id="WMDRMNET_POLICY_TYPE_TRANSCRYPTPLAY"></span><span id="wmdrmnet_policy_type_transcryptplay"></span>**\_WMDRMNET-RICHTLINIENTYP \_ \_ TRANSCRYPTPLAY**
</dt> <dd>

Die Richtlinie steuert die Möglichkeit, durch Windows Medien-DRM geschützte Inhalte in geschützte Windows Medien-DRM für Netzwerkgerätedaten zu konvertieren und auf einem Netzwerkgerät wiederzuspielen.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Keine.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Enumerationstypen**](drm-enumeration-types.md)
</dt> <dt>

[**\_WMDRMNET-RICHTLINIE**](wmdrmnet-policy.md)
</dt> </dl>

 

 





