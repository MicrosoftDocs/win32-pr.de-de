---
title: WMDM_PROP_VALUES_RANGE Struktur
description: Die WMDM \_ PROP \_ VALUES \_ RANGE-Struktur beschreibt einen Bereich gültiger Werte für eine bestimmte Eigenschaft in einer bestimmten Eigenschaftenkonfiguration.
ms.assetid: fb823a66-cc9c-4632-a4f0-03c7255c3ccb
keywords:
- WMDM_PROP_VALUES_RANGE struktur windows Media Geräte-Manager
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
ms.openlocfilehash: a668b5acd8427df5b4bc163788c225f4eaee9a16b70af25312ae8ec94cb2bb63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004780"
---
# <a name="wmdm_prop_values_range-structure"></a>WMDM \_ PROP \_ VALUES \_ RANGE-Struktur

Die **WMDM \_ PROP VALUES \_ \_ RANGE-Struktur** beschreibt einen Bereich gültiger Werte für eine bestimmte Eigenschaft in einer bestimmten Eigenschaftenkonfiguration.

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

Mindestwert im Bereich.

</dd> <dt>

**rangeMax**
</dt> <dd>

Maximalwert im Bereich.

</dd> <dt>

**rangeStep**
</dt> <dd>

Die Schrittgröße, in der gültige Werte vom Minimalwert zum Höchstwert inkrementiert werden. Dies ermöglicht die Angabe diskreter zulässiger Werte in einem Bereich.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Diese Struktur wird in der [**WMDM \_ PROP \_ DESC-Struktur**](wmdm-prop-desc.md) verwendet, um einen Bereich gültiger Werte zu beschreiben. Ein Bereich gültiger Werte ist anwendbar, wenn WMDM \_ ENUM \_ PROP VALID VALUES \_ \_ \_ ENUM aus der [**WMDM \_ ENUM \_ PROP VALID VALUES \_ \_ \_ FORM-Enumeration**](wmdm-enum-prop-valid-values-form.md) ausgewählt wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wmdm.idl</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IWMDMDevice3::GetFormatCapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability)
</dt> <dt>

[**WMDM \_ ENUM \_ PROP \_ VALID \_ VALUES \_ FORM**](wmdm-enum-prop-valid-values-form.md)
</dt> <dt>

[**\_WMDM-FORMATFUNKTION \_**](wmdm-format-capability.md)
</dt> <dt>

[**WMDM \_ PROP \_ CONFIG**](wmdm-prop-config.md)
</dt> <dt>

[**WMDM \_ PROP \_ DESC**](wmdm-prop-desc.md)
</dt> <dt>

[**WMDM \_ PROP \_ VALUES \_ ENUM**](wmdm-prop-values-enum.md)
</dt> <dt>

[**Strukturen**](structures.md)
</dt> </dl>

 

 





