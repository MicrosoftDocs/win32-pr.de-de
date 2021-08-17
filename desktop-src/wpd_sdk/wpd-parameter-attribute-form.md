---
description: Beschreibt, wie ein -Parameter (Methode oder Ereignis) seinen Wert speichert.
ms.assetid: 066196af-7805-4823-8ab7-cb95c17bba2a
title: WpdParameterAttributeForm-Enumeration (PortableDevice.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WpdParameterAttributeForm
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: f50665768d62d8155bd0ac9001f4ae5029766d7d5b27a942941f8f41b9492e10
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119026748"
---
# <a name="wpdparameterattributeform-enumeration"></a>WpdParameterAttributeForm-Enumeration

Der [**WpdParameterAttributeForm-Enumerationstyp**](/previous-versions/windows/hardware/drivers/ff597895(v=vs.85)) beschreibt, wie ein -Parameter (Methode oder Ereignis) seinen Wert speichert.

## <a name="syntax"></a>Syntax


```C++
typedef enum tagWpdParameterAttributeForm { 
  WPD_PARAMETER_ATTRIBUTE_FORM_UNSPECIFIED         = 0,
  WPD_PARAMETER_ATTRIBUTE_FORM_RANGE               = 1,
  WPD_PARAMETER_ATTRIBUTE_FORM_ENUMERATION         = 2,
  WPD_PARAMETER_ATTRIBUTE_FORM_REGULAR_EXPRESSION  = 3,
  WPD_PARAMETER_ATTRIBUTE_OBJECT_IDENTIFIER        = 4
} WpdParameterAttributeForm;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="WPD_PARAMETER_ATTRIBUTE_FORM_UNSPECIFIED"></span><span id="wpd_parameter_attribute_form_unspecified"></span>**\_ \_ WPD-PARAMETERATTRIBUTFORMULAR \_ NICHT \_ ANGEGEBEN**
</dt> <dd>

Die Form des Parameters ist nicht angegeben.

</dd> <dt>

<span id="WPD_PARAMETER_ATTRIBUTE_FORM_RANGE"></span><span id="wpd_parameter_attribute_form_range"></span>**FORMULARBEREICH DES \_ \_ WPD-PARAMETERATTRIBUTS \_ \_**
</dt> <dd>

Der -Parameter gibt einen Bereich an.

</dd> <dt>

<span id="WPD_PARAMETER_ATTRIBUTE_FORM_ENUMERATION"></span><span id="wpd_parameter_attribute_form_enumeration"></span>**\_FORMULARENUMERATION DES WPD-PARAMETERATTRIBUTS \_ \_ \_**
</dt> <dd>

Der -Parameter ist eine Enumeration.

</dd> <dt>

<span id="WPD_PARAMETER_ATTRIBUTE_FORM_REGULAR_EXPRESSION"></span><span id="wpd_parameter_attribute_form_regular_expression"></span>**\_ \_ WPD-PARAMETERATTRIBUT \_ FORMULAR \_ REGULÄRER \_ AUSDRUCK**
</dt> <dd>

Der -Parameter ist ein regulärer Ausdruck.

</dd> <dt>

<span id="WPD_PARAMETER_ATTRIBUTE_OBJECT_IDENTIFIER"></span><span id="wpd_parameter_attribute_object_identifier"></span>**WPD \_ PARAMETER \_ ATTRIBUTE \_ OBJECT \_ IDENTIFIER**
</dt> <dd>

Der -Parameter ist ein Objektbezeichner.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



 

