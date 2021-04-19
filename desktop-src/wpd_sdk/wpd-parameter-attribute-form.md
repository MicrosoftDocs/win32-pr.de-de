---
description: Beschreibt, wie ein-Parameter (Methode oder Ereignis) seinen Wert speichert.
ms.assetid: 066196af-7805-4823-8ab7-cb95c17bba2a
title: Wpdparameterattributeform-Enumeration (portabledevice. h)
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
ms.openlocfilehash: 528008edbb74d5eda626b9868814ad621e676fa9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369592"
---
# <a name="wpdparameterattributeform-enumeration"></a>Wpdparameterattributeform-Enumeration

Der [**wpdparameterattributeform**](/previous-versions/windows/hardware/drivers/ff597895(v=vs.85)) -Enumerationstyp beschreibt, wie ein (Methode-oder Ereignis)-Parameter seinen Wert speichert.

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

<span id="WPD_PARAMETER_ATTRIBUTE_FORM_UNSPECIFIED"></span><span id="wpd_parameter_attribute_form_unspecified"></span>**Das WPD- \_ Parameter \_ Attribut ist \_ \_ nicht angegeben.**
</dt> <dd>

Die Form des-Parameters ist nicht angegeben.

</dd> <dt>

<span id="WPD_PARAMETER_ATTRIBUTE_FORM_RANGE"></span><span id="wpd_parameter_attribute_form_range"></span>**Formular Bereich des WPD- \_ Parameter \_ Attributs \_ \_**
</dt> <dd>

Der-Parameter gibt einen Bereich an.

</dd> <dt>

<span id="WPD_PARAMETER_ATTRIBUTE_FORM_ENUMERATION"></span><span id="wpd_parameter_attribute_form_enumeration"></span>**\_ \_ Attribut \_ Formular- \_ Enumeration für WPD-Parameter**
</dt> <dd>

Der-Parameter ist eine Enumeration.

</dd> <dt>

<span id="WPD_PARAMETER_ATTRIBUTE_FORM_REGULAR_EXPRESSION"></span><span id="wpd_parameter_attribute_form_regular_expression"></span>**\_ \_ \_ \_ regulärer \_ Ausdruck des WPD-Parameter Attributs**
</dt> <dd>

Der-Parameter ist ein regulärer Ausdruck.

</dd> <dt>

<span id="WPD_PARAMETER_ATTRIBUTE_OBJECT_IDENTIFIER"></span><span id="wpd_parameter_attribute_object_identifier"></span>**Objekt-ID des WPD- \_ Parameter \_ Attributs \_ \_**
</dt> <dd>

Der-Parameter ist ein Objekt Bezeichner.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Portabledevice. h</dt> </dl> |



 

