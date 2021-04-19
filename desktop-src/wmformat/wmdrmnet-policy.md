---
title: WMDRMNET_POLICY Struktur (wmdrmsdk. h)
description: Die wmdrmnet- \_ Richtlinien Struktur enthält die Richtlinie, die für Windows Media DRM für Netzwerkgeräte Vorgänge verwendet werden soll.
ms.assetid: 11eaaeb2-3470-4f58-ae1c-53ee0f60bdce
keywords:
- WMDRMNET_POLICY Struktur-Windows Media-Format
- Struktur des Windows-Medien Formats
topic_type:
- apiref
api_name:
- WMDRMNET_POLICY
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 574e37a8c5ee7f68291012b86cda3a89e25949ab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373611"
---
# <a name="wmdrmnet_policy-structure"></a>Wmdrmnet- \_ Richtlinien Struktur

Die **wmdrmnet- \_ Richtlinien** Struktur enthält die Richtlinie, die für Windows Media DRM für Netzwerkgeräte Vorgänge verwendet werden soll.

## <a name="syntax"></a>Syntax


```C++
typedef struct WMDRMNET_POLICY {
  WMDRMNET_POLICY_TYPE ePolicyType;
  BYTE                 *pbPolicy;
} ;
```



## <a name="members"></a>Member

<dl> <dt>

**epolicytype**
</dt> <dd>

Member der [**wmdrmnet- \_ \_ Richtlinientyp**](wmdrmnet-policy-type.md) -Enumeration, die den Richtlinientyp angibt.

</dd> <dt>

**pbpolicy**
</dt> <dd>

Puffer, der die Richtlinie enthält. Der einzige derzeit unterstützte Richtlinientyp ist der **wmdrmnet- \_ Richtlinientyp \_ \_ transryptplay**. Dieser Member ist ein Zeiger auf die **\_ \_ transryptplay-Struktur der wmdrmnet-Richtlinie** .

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Struktur wird als Parameter für die [**iwmdrmnettransmitter:: getleaflicenseresponse**](iwmdrmnettransmitter-getleaflicenseresponse.md) -Methode verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Strukturen**](drm-structures.md)
</dt> <dt>

[**globale Anforderungen für wmdrmnet- \_ Richtlinien \_ \_**](wmdrmnet-policy-global-requirements.md)
</dt> <dt>

[**minimale Umgebung der wmdrmnet- \_ Richtlinie \_ \_**](wmdrmnet-policy-minimum-environment.md)
</dt> <dt>

[**wmdrmnet- \_ Richtlinie \_ transryptplay**](wmdrmnet-policy-transcryptplay.md)
</dt> <dt>

[**wmdrmnet \_ - \_ Richtlinientyp**](wmdrmnet-policy-type.md)
</dt> </dl>

 

 





