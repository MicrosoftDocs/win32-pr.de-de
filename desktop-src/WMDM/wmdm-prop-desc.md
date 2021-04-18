---
title: WMDM_PROP_DESC Struktur
description: Die WMDM- \_ Prop- \_ DESC-Struktur beschreibt gültige Werte einer Eigenschaft in einer bestimmten Eigenschaften Konfiguration.
ms.assetid: e4766e1e-6c1b-4a2d-ad2e-c07035ca2be2
keywords:
- WMDM_PROP_DESC Struktur von Windows-Medien Device Manager
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
ms.openlocfilehash: 98f6ea406a3d48d0ed65098d66721fcadbb98411
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354749"
---
# <a name="wmdm_prop_desc-structure"></a>WMDM- \_ Prop- \_ Struktur

Die **WMDM- \_ Prop- \_ DESC** -Struktur beschreibt gültige Werte einer Eigenschaft in einer bestimmten Eigenschaften Konfiguration.

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

**pwszpropname**
</dt> <dd>

Der Name der Eigenschaft. Die Anwendung muss diesen Arbeitsspeicher freigeben, wenn Sie verwendet wird.

</dd> <dt>

**Validvaluesform**
</dt> <dd>

Ein WMDM-Enumerationswert [**\_ \_ \_ gültige \_ Werte \_ Formular**](wmdm-enum-prop-valid-values-form.md) Enumerationswert, der den Typ der Werte beschreibt, z. b. einen Bereich oder eine Liste. Der Wert dieser Enumeration bestimmt, welche Member-Variable verwendet wird.

</dd> <dt>

**ValidValues**
</dt> <dd>

Enthält die gültigen Werte der-Eigenschaft in einer bestimmten Eigenschaften Konfiguration. Dieser Member enthält eines von drei Elementen: den Enumerationswert WMDM- \_ \_ \_ \_ \_ enumerationsprop gültige Werte any, den Member **validvaluesrange** oder den **enumeratedvalidvalues**-Member. Der Wert oder Member wird durch **validvaluesform** angegeben.

<dl> <dt>

**Validvaluesrange**
</dt> <dd>

Eine [**WMDM \_ - \_ Werte \_ Bereichs**](wmdm-prop-values-range.md) Struktur, die einen Bereich gültiger Werte enthält. Diese ist nur vorhanden, wenn **validvaluesform** auf den \_ \_ \_ gültigen \_ Werte \_ Bereich der WMDM-Enumeration festgelegt ist. Siehe Hinweise.

</dd> <dt>

**Enumeratedvalidvalues**
</dt> <dd>

Eine enumerationsstruktur mit [**WMDM- \_ Prop- \_ Werten \_**](wmdm-prop-values-enum.md) , die einen aufgelisteten Satz gültiger Werte enthält. Diese ist nur vorhanden, wenn für **validvaluesform** die Enumeration \_ \_ \_ gültige \_ Values-Enumeration festgelegt ist \_ . Siehe Hinweise.

</dd> </dl> </dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **WMDM- \_ Prop- \_ DESC** -Struktur enthält eine Eigenschafts Beschreibung, die aus einem Eigenschaftsnamen und den gültigen Werten in einer bestimmten Konfiguration besteht.

Der Aufrufer muss den von **validvaluesrange** oder **enumeratedvalues** genutzten Arbeitsspeicher freigeben. Ein Beispiel hierfür finden Sie unter [**WMDM- \_ Format \_ Funktion**](wmdm-format-capability.md).

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

[**WMDM- \_ Prop \_ Values- \_ Enumeration**](wmdm-prop-values-enum.md)
</dt> <dt>

[**Bereich der WMDM- \_ Prop- \_ Werte \_**](wmdm-prop-values-range.md)
</dt> <dt>

[**Strukturen**](structures.md)
</dt> </dl>

 

 





