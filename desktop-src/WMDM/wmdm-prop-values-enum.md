---
title: WMDM_PROP_VALUES_ENUM Struktur
description: Die Enum-Struktur der WMDM- \_ Prop- \_ Werte \_ enthält einen Aufzählungs Satz gültiger Werte für eine bestimmte Eigenschaft in einer bestimmten Eigenschaften Konfiguration.
ms.assetid: 8094f3c0-a7ed-4e63-8503-aaac3fd9c012
keywords:
- WMDM_PROP_VALUES_ENUM Struktur von Windows-Medien Device Manager
topic_type:
- apiref
api_name:
- WMDM_PROP_VALUES_ENUM
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1c70088d57189dd36d360bc8910a15717d964ea
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352864"
---
# <a name="wmdm_prop_values_enum-structure"></a>Enumerationsstruktur der WMDM- \_ Prop- \_ Werte \_

Die **\_ \_ \_ enum-Struktur der WMDM-Prop-Werte** enthält einen Aufzählungs Satz gültiger Werte für eine bestimmte Eigenschaft in einer bestimmten Eigenschaften Konfiguration.

## <a name="syntax"></a>Syntax


```C++
typedef struct _WMDM_PROP_VALUES_ENUM {
  UINT        cEnumValues;
  PROPVARIANT *pValues;
} WMDM_PROP_VALUES_ENUM;
```



## <a name="members"></a>Member

<dl> <dt>

**cenum Values**
</dt> <dd>

Anzahl von Enumerationswerten.

</dd> <dt>

**pvalues**
</dt> <dd>

Zeiger auf ein Array von-Werten. Die Größe des Arrays ist gleich dem Wert von " **cenum Values**".

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Struktur wird in der-Struktur der **WMDM- \_ Prop \_** -Struktur verwendet, um einen enumerierten Satz gültiger Werte zu beschreiben. Ein aufgelisteter Satz gültiger Werte ist anwendbar, wenn \_ \_ \_ \_ \_ die Enumeration für die Enumeration der Werte für die WMDM-Enumeration gültige Werte aus der WMDM-Enumeration gültig ist. **\_ \_ \_ \_ \_**

Der Aufrufer muss den von **pvalues** verwendeten Arbeitsspeicher freigeben. Ein Beispiel hierfür finden Sie unter [**WMDM- \_ Format \_ Funktion**](wmdm-format-capability.md).

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

[**Bereich der WMDM- \_ Prop- \_ Werte \_**](wmdm-prop-values-range.md)
</dt> <dt>

[**Strukturen**](structures.md)
</dt> </dl>

 

 





