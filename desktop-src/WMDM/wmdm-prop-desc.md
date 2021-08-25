---
title: WMDM_PROP_DESC-Struktur
description: Die WMDM \_ PROP \_ DESC-Struktur beschreibt gültige Werte einer Eigenschaft in einer bestimmten Eigenschaftenkonfiguration.
ms.assetid: e4766e1e-6c1b-4a2d-ad2e-c07035ca2be2
keywords:
- WMDM_PROP_DESC struktur windows media Geräte-Manager
topic_type:
- apiref
api_name:
- WMDM_PROP_DESC
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cad250745d51f00d3bb0492b6da8d3f9802bf87b78d65f4640324a68caa9ddf3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119903940"
---
# <a name="wmdm_prop_desc-structure"></a>WMDM \_ PROP \_ DESC-Struktur

Die **WMDM \_ PROP \_ DESC-Struktur** beschreibt gültige Werte einer Eigenschaft in einer bestimmten Eigenschaftenkonfiguration.

## <a name="syntax"></a>Syntax


```C++
typedef struct _WMDM_PROP_DESC {
  LPWSTR                           pwszPropName;
  WMDM_ENUM_PROP_VALID_VALUES_FORM ValidValuesForm;
  union  {
    WMDM_PROP_VALUES_RANGE ValidValuesRange;
    WMDM_PROP_VALUES_ENUM  EnumeratedValidValues;
  } ValidValues;
} WMDM_PROP_DESC;
```



## <a name="members"></a>Member

<dl> <dt>

**pwszPropName**
</dt> <dd>

Der Name der Eigenschaft. Die Anwendung muss diesen Arbeitsspeicher frei geben, wenn sie ihn nicht mehr verwendet.

</dd> <dt>

**ValidValuesForm**
</dt> <dd>

Ein [**WMDM \_ ENUM \_ PROP VALID VALUES \_ \_ \_ FORM-Enumerationswert,**](wmdm-enum-prop-valid-values-form.md) der den Typ von Werten beschreibt, z. B. einen Bereich oder eine Liste. Der Wert dieser Enumeration bestimmt, welche Membervariable verwendet wird.

</dd> <dt>

**ValidValues**
</dt> <dd>

Enthält die gültigen Werte der Eigenschaft in einer bestimmten Eigenschaftenkonfiguration. Dieser Member enthält eines von drei Elementen: den Enumerationswert WMDM ENUM PROP VALID VALUES ANY, den Member \_ \_ \_ \_ \_ **ValidValuesRange** oder den **Member EnumeratedValidValues**. Der Wert oder Member wird durch **ValidValuesForm angegeben.**

<dl> <dt>

**ValidValuesRange**
</dt> <dd>

Eine [**WMDM \_ PROP VALUES \_ \_ RANGE-Struktur,**](wmdm-prop-values-range.md) die einen Bereich gültiger Werte enthält. Dies ist nur vorhanden, **wenn ValidValuesForm** auf WMDM \_ ENUM \_ PROP VALID VALUES RANGE festgelegt \_ \_ \_ ist. Siehe Hinweise.

</dd> <dt>

**EnumeratedValidValues**
</dt> <dd>

Eine [**WMDM \_ PROP \_ \_ VALUES-ENUM-Struktur,**](wmdm-prop-values-enum.md) die einen aufzählten Satz gültiger Werte enthält. Dies ist nur vorhanden, **wenn ValidValuesForm** auf WMDM \_ ENUM \_ PROP VALID VALUES \_ \_ \_ ENUM festgelegt ist. Siehe Hinweise.

</dd> </dl> </dd> </dl>

## <a name="remarks"></a>Hinweise

Die **WMDM \_ PROP \_ DESC-Struktur** enthält eine Eigenschaftenbeschreibung, die aus einem Eigenschaftennamen und den gültigen Werten in einer bestimmten Konfiguration besteht.

Der Aufrufer ist erforderlich, um den von **ValidValuesRange oder** **EnumeratedValues** verwendeten Arbeitsspeicher frei zu geben. Ein Beispiel hierfür finden Sie unter [**WMDM \_ FORMAT \_ CAPABILITY**](wmdm-format-capability.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wmdm.idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IWMDMDevice3::GetFormatCapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability)
</dt> <dt>

[**WMDM \_ ENUM \_ PROP \_ VALID \_ VALUES \_ FORM**](wmdm-enum-prop-valid-values-form.md)
</dt> <dt>

[**\_WMDM-FORMATFUNKTION \_**](wmdm-format-capability.md)
</dt> <dt>

[**WMDM \_ PROP \_ CONFIG**](wmdm-prop-config.md)
</dt> <dt>

[**WMDM \_ PROP \_ VALUES \_ ENUM**](wmdm-prop-values-enum.md)
</dt> <dt>

[**WMDM \_ PROP \_ VALUES \_ RANGE**](wmdm-prop-values-range.md)
</dt> <dt>

[**Strukturen**](structures.md)
</dt> </dl>

 

 





