---
title: WMDRMNET_POLICY -Struktur (Wmdrmsdk.h)
description: Die WMDRMNET POLICY-Struktur enthält die Richtlinie, die für Windows \_ Media DRM für Netzwerkgerätevorgänge verwendet werden soll.
ms.assetid: 11eaaeb2-3470-4f58-ae1c-53ee0f60bdce
keywords:
- WMDRMNET_POLICY struktur windows media format
- Strukturfenster Medienformat
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
ms.openlocfilehash: bf648ef5e300fa9fef1cf12fd4698f4ec196f62130bf75a02f263cd96931f0bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117653423"
---
# <a name="wmdrmnet_policy-structure"></a>WMDRMNET \_ POLICY-Struktur

Die **WMDRMNET \_ POLICY-Struktur** enthält die Richtlinie, die für vorgänge Windows Medien-DRM für Netzwerkgeräte verwendet werden soll.

## <a name="syntax"></a>Syntax


```C++
typedef struct WMDRMNET_POLICY {
  WMDRMNET_POLICY_TYPE ePolicyType;
  BYTE                 *pbPolicy;
} ;
```



## <a name="members"></a>Member

<dl> <dt>

**ePolicyType**
</dt> <dd>

Member der [**WMDRMNET \_ POLICY \_ TYPE-Enumeration,**](wmdrmnet-policy-type.md) die den Typ der Richtlinie angibt.

</dd> <dt>

**pbPolicy**
</dt> <dd>

Puffer, der die Richtlinie enthält. Der einzige derzeit unterstützte Richtlinientyp ist **WMDRMNET \_ POLICY \_ TYPE \_ TRANSCRYPTPLAY.** Dieser Member ist ein Zeiger auf eine **WMDRMNET \_ POLICY \_ TRANSCRYPTPLAY-Struktur.**

</dd> </dl>

## <a name="remarks"></a>Hinweise

Diese Struktur wird als Parameter für die [**IWMDRMNetTransmitter::GetLeafLicenseResponse-Methode**](iwmdrmnettransmitter-getleaflicenseresponse.md) verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Strukturen**](drm-structures.md)
</dt> <dt>

[**GLOBALE ANFORDERUNGEN FÜR \_ WMDRMNET-RICHTLINIEN \_ \_**](wmdrmnet-policy-global-requirements.md)
</dt> <dt>

[**MINDESTUMGEBUNG FÜR \_ \_ WMDRMNET-RICHTLINIEN \_**](wmdrmnet-policy-minimum-environment.md)
</dt> <dt>

[**WMDRMNET \_ POLICY \_ TRANSCRYPTPLAY**](wmdrmnet-policy-transcryptplay.md)
</dt> <dt>

[**WMDRMNET-RICHTLINIENTYP \_ \_**](wmdrmnet-policy-type.md)
</dt> </dl>

 

 





