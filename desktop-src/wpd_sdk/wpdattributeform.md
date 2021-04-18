---
description: Der wpdattributeform-Enumerationstyp beschreibt, wie eine Eigenschaft ihre Werte speichert.
ms.assetid: 3ad8d1f9-1b74-4f34-9af5-1acdd588b650
title: Wpdattributeform-Enumeration (portabledevice. h)
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
ms.openlocfilehash: 4c70f68dc04adcb454fcc7c5ae301f0dabf60c28
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365413"
---
# <a name="wpdattributeform-enumeration"></a>Wpdattributeform-Enumeration

Der **wpdattributeform** -Enumerationstyp beschreibt, wie eine Eigenschaft ihre Werte speichert.

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

<span id="WPD_PROPERTY_ATTRIBUTE_FORM_UNSPECIFIED"></span><span id="wpd_property_attribute_form_unspecified"></span>**Das WPD- \_ Eigenschafts \_ Attribut ist \_ \_ nicht angegeben.**
</dt> <dd>

Die Form der Eigenschaften Daten ist nicht angegeben.

</dd> <dt>

<span id="WPD_PROPERTY_ATTRIBUTE_FORM_RANGE"></span><span id="wpd_property_attribute_form_range"></span>**WPD- \_ Eigenschafts \_ Attribut- \_ Formular \_ Bereich**
</dt> <dd>

Der Wert wird als Wertebereich mit einem minimal-und Maximalwert ausgedrückt.

</dd> <dt>

<span id="WPD_PROPERTY_ATTRIBUTE_FORM_ENUMERATION"></span><span id="wpd_property_attribute_form_enumeration"></span>**WPD- \_ Eigenschafts \_ Attribut- \_ Formular \_ Enumeration**
</dt> <dd>

Die-Eigenschaft verfügt über eine Reihe einzelner Werte.

</dd> <dt>

<span id="WPD_PROPERTY_ATTRIBUTE_FORM_REGULAR_EXPRESSION"></span><span id="wpd_property_attribute_form_regular_expression"></span>**\_ \_ \_ \_ regulärer \_ Ausdruck für WPD-Eigenschafts Attribut**
</dt> <dd>

Der Eigenschafts Wert ist ein regulärer Ausdruck und kein literaler Ausdruck.

</dd> <dt>

<span id="WPD_PROPERTY_ATTRIBUTE_FORM_OJBECT_IDENTIFIER"></span><span id="wpd_property_attribute_form_ojbect_identifier"></span>**WPD- \_ Eigenschafts \_ Attribut ( \_ \_ Ojbect- \_ Bezeichner)**
</dt> <dd>

Der Eigenschafts Wert stellt einen Objekt Bezeichner dar.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Enumeration wird von der Eigenschaft " [WPD \_ Property \_ Attribute \_ Form](attributes.md) " verwendet, um zu beschreiben, wie die Daten einer Eigenschaft gespeichert werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Portabledevice. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Strukturen und Enumerationstypen**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




