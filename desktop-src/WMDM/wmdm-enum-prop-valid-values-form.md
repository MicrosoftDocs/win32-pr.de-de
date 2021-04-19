---
title: WMDM_ENUM_PROP_VALID_VALUES_FORM-Enumeration
description: Der Enumerationstyp "der WMDM- \_ \_ \_ \_ Enumerationswert für gültige Werte" \_ beschreibt mögliche Formen gültiger Werte für eine Eigenschaft.
ms.assetid: 49d174b4-c8a3-4c16-ad21-4b66dcf8088f
keywords:
- Device Manager der WMDM_ENUM_PROP_VALID_VALUES_FORM-Enumeration Windows Media
topic_type:
- apiref
api_name:
- WMDM_ENUM_PROP_VALID_VALUES_FORM
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d7db971f359a9cead2aae6083a934086d42c481
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367536"
---
# <a name="wmdm_enum_prop_valid_values_form-enumeration"></a>WMDM- \_ \_ \_ \_ Enumeration gültige Werte \_ Formular Enumeration

Der Enumerationstyp "der **WMDM-Enumerationswert für \_ \_ \_ gültige \_ Werte \_** " beschreibt mögliche Formen gültiger Werte für eine Eigenschaft.

## <a name="syntax"></a>Syntax


```C++
typedef enum _WMDM_ENUM_PROP_VALID_VALUES_FORM { 
  WMDM_ENUM_PROP_VALID_VALUES_ANY,
  WMDM_ENUM_PROP_VALID_VALUES_RANGE,
  WMDM_ENUM_PROP_VALID_VALUES_ENUM
} WMDM_ENUM_PROP_VALID_VALUES_FORM;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="WMDM_ENUM_PROP_VALID_VALUES_ANY"></span><span id="wmdm_enum_prop_valid_values_any"></span>**WMDM- \_ \_ enumerationsprop \_ gültige \_ Werte \_ beliebig**
</dt> <dd>

Alle Werte sind gültig.

</dd> <dt>

<span id="WMDM_ENUM_PROP_VALID_VALUES_RANGE"></span><span id="wmdm_enum_prop_valid_values_range"></span>**\_ \_ \_ Bereich der gültigen \_ Werte \_ für die WMDM-Enumeration**
</dt> <dd>

Gültige Werte werden als Bereich ausgedrückt. Ausführliche Informationen finden Sie in der Struktur von [**WMDM- \_ Prop- \_ Werten \_**](wmdm-prop-values-range.md) .

</dd> <dt>

<span id="WMDM_ENUM_PROP_VALID_VALUES_ENUM"></span><span id="wmdm_enum_prop_valid_values_enum"></span>**Enumeration \_ \_ \_ gültiger \_ Werte \_ für WMDM-Enumeration**
</dt> <dd>

Gültige Werte sind enumerationssätze. Ausführliche Informationen finden Sie in der enumerationsstruktur der [**WMDM- \_ Prop- \_ Werte \_**](wmdm-prop-values-enum.md) .

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Enumeration wird in der-Struktur der [**WMDM- \_ Prop \_**](wmdm-prop-desc.md) -Struktur verwendet, um die Form gültiger Werte für eine Eigenschaft anzugeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>WMDM. idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Enumerationstypen**](enumeration-types.md)
</dt> <dt>

[**IWMDMDevice3:: getformatcapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability)
</dt> <dt>

[**WMDM- \_ Format \_ Funktion**](wmdm-format-capability.md)
</dt> <dt>

[**WMDM- \_ Prop- \_ Konfiguration**](wmdm-prop-config.md)
</dt> <dt>

[**WMDM- \_ Prop- \_ Abteilung**](wmdm-prop-desc.md)
</dt> <dt>

[**WMDM- \_ Prop \_ Values- \_ Enumeration**](wmdm-prop-values-enum.md)
</dt> <dt>

[**Bereich der WMDM- \_ Prop- \_ Werte \_**](wmdm-prop-values-range.md)
</dt> </dl>

 

 





