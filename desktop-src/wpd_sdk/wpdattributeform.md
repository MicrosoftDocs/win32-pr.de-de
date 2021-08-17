---
description: Der WpdAttributeForm-Enumerationstyp beschreibt, wie eine Eigenschaft ihre Werte speichert.
ms.assetid: 3ad8d1f9-1b74-4f34-9af5-1acdd588b650
title: WpdAttributeForm-Enumeration (PortableDevice.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WpdAttributeForm
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 8366f90fe41eaa92d826f4d761fe8cdf58304f54e1f57cb074ae94d6fd9f1ea9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118696278"
---
# <a name="wpdattributeform-enumeration"></a>WpdAttributeForm-Enumeration

Der **WpdAttributeForm-Enumerationstyp** beschreibt, wie eine Eigenschaft ihre Werte speichert.

## <a name="syntax"></a>Syntax


```C++
typedef enum WpdAttributeForm { 
  WPD_PROPERTY_ATTRIBUTE_FORM_UNSPECIFIED         = 0,
  WPD_PROPERTY_ATTRIBUTE_FORM_RANGE               = 1,
  WPD_PROPERTY_ATTRIBUTE_FORM_ENUMERATION         = 2,
  WPD_PROPERTY_ATTRIBUTE_FORM_REGULAR_EXPRESSION  = 3,
  WPD_PROPERTY_ATTRIBUTE_FORM_OJBECT_IDENTIFIER   = 4
} ;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="WPD_PROPERTY_ATTRIBUTE_FORM_UNSPECIFIED"></span><span id="wpd_property_attribute_form_unspecified"></span>**\_ \_ WPD-EIGENSCHAFTENATTRIBUTFORMULAR \_ \_ NICHT ANGEGEBEN**
</dt> <dd>

Die Form der Daten der Eigenschaft ist nicht angegeben.

</dd> <dt>

<span id="WPD_PROPERTY_ATTRIBUTE_FORM_RANGE"></span><span id="wpd_property_attribute_form_range"></span>**FORMULARBEREICH DES \_ \_ WPD-EIGENSCHAFTSATTRIBUTS \_ \_**
</dt> <dd>

Der Wert wird als Wertebereich mit einem Minimum und einem Maximum ausgedrückt.

</dd> <dt>

<span id="WPD_PROPERTY_ATTRIBUTE_FORM_ENUMERATION"></span><span id="wpd_property_attribute_form_enumeration"></span>**\_ \_ WPD-EIGENSCHAFTENATTRIBUT \_ FORMULARENUMERATION \_**
</dt> <dd>

Die -Eigenschaft verfügt über eine Reihe einzelner Werte.

</dd> <dt>

<span id="WPD_PROPERTY_ATTRIBUTE_FORM_REGULAR_EXPRESSION"></span><span id="wpd_property_attribute_form_regular_expression"></span>**\_ \_ WPD-EIGENSCHAFTENATTRIBUT \_ FORMULAR \_ REGULÄRER \_ AUSDRUCK**
</dt> <dd>

Der Eigenschaftswert ist ein regulärer Ausdruck, kein Literalausdruck.

</dd> <dt>

<span id="WPD_PROPERTY_ATTRIBUTE_FORM_OJBECT_IDENTIFIER"></span><span id="wpd_property_attribute_form_ojbect_identifier"></span>**WPD \_ PROPERTY \_ ATTRIBUTE \_ FORM \_ OJBECT \_ IDENTIFIER**
</dt> <dd>

Der Eigenschaftswert stellt einen Objektbezeichner dar.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Diese Enumeration wird von der [WPD \_ PROPERTY ATTRIBUTE \_ \_ FORM-Eigenschaft verwendet,](attributes.md) um zu beschreiben, wie die Daten einer Eigenschaft gespeichert werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Strukturen und Enumerationstypen**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




