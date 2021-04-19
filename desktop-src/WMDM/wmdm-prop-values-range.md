---
title: WMDM_PROP_VALUES_RANGE Struktur
description: Die Bereichs Struktur der WMDM- \_ Prop- \_ Werte \_ beschreibt einen Bereich gültiger Werte für eine bestimmte Eigenschaft in einer bestimmten Eigenschaften Konfiguration.
ms.assetid: fb823a66-cc9c-4632-a4f0-03c7255c3ccb
keywords:
- WMDM_PROP_VALUES_RANGE Struktur von Windows-Medien Device Manager
topic_type:
- apiref
api_name:
- WMDM_PROP_VALUES_RANGE
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ba82a1067db97e93fff2845e69e89f978548b73
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356351"
---
# <a name="wmdm_prop_values_range-structure"></a>Bereichs Struktur der WMDM- \_ Prop- \_ Werte \_

Die **Bereichs Struktur der WMDM- \_ Prop- \_ Werte \_** beschreibt einen Bereich gültiger Werte für eine bestimmte Eigenschaft in einer bestimmten Eigenschaften Konfiguration.

## <a name="syntax"></a>Syntax


```C++
typedef struct _WMDM_PROP_VALUES_RANGE {
  PROPVARIANT rangeMin;
  PROPVARIANT rangeMax;
  PROPVARIANT rangeStep;
} WMDM_PROP_VALUES_RANGE;
```



## <a name="members"></a>Member

<dl> <dt>

**rangeMin**
</dt> <dd>

Minimalwert im Bereich.

</dd> <dt>

**rangeMax**
</dt> <dd>

Maximalwert im Bereich.

</dd> <dt>

**rangestep**
</dt> <dd>

Die Schrittgröße, in der gültige Werte von dem Minimalwert auf den maximalen Wert erhöht werden. Dies ermöglicht die Angabe diskreter zulässiger Werte in einem Bereich.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Struktur wird in der-Struktur der [**WMDM- \_ Prop \_**](wmdm-prop-desc.md) -Struktur verwendet, um einen Bereich gültiger Werte zu beschreiben. Ein Bereich gültiger Werte ist anwendbar, wenn die Enumeration "gültige Werte für WMDM-Enumerationswerte" \_ \_ \_ \_ \_ aus der Enumeration "gültige Werte" der WMDM-Enumeration ausgewählt wird. [**\_ \_ \_ \_ \_**](wmdm-enum-prop-valid-values-form.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>WMDM. idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IWMDMDevice3:: getformatcapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability)
</dt> <dt>

[**\_ \_ \_ Formular für gültige \_ Werte \_ für WMDM-Enumeration**](wmdm-enum-prop-valid-values-form.md)
</dt> <dt>

[**WMDM- \_ Format \_ Funktion**](wmdm-format-capability.md)
</dt> <dt>

[**WMDM- \_ Prop- \_ Konfiguration**](wmdm-prop-config.md)
</dt> <dt>

[**WMDM- \_ Prop- \_ Abteilung**](wmdm-prop-desc.md)
</dt> <dt>

[**WMDM- \_ Prop \_ Values- \_ Enumeration**](wmdm-prop-values-enum.md)
</dt> <dt>

[**Strukturen**](structures.md)
</dt> </dl>

 

 





