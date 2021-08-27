---
title: WMDM_PROP_VALUES_ENUM Struktur
description: Die WMDM PROP VALUES ENUM-Struktur enthält einen aufzählten Satz gültiger Werte für eine bestimmte Eigenschaft \_ \_ in einer \_ bestimmten Eigenschaftenkonfiguration.
ms.assetid: 8094f3c0-a7ed-4e63-8503-aaac3fd9c012
keywords:
- WMDM_PROP_VALUES_ENUM Struktur von Windows Media Geräte-Manager
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
ms.openlocfilehash: 35766ed71b864c5eb7f0bbbebf5eda384a25e174501aa2a56e790840a4c636c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004790"
---
# <a name="wmdm_prop_values_enum-structure"></a>WMDM \_ PROP \_ VALUES \_ ENUM-Struktur

Die **WMDM \_ PROP VALUES \_ \_ ENUM-Struktur** enthält einen aufzählten Satz gültiger Werte für eine bestimmte Eigenschaft in einer bestimmten Eigenschaftenkonfiguration.

## <a name="syntax"></a>Syntax


```C++
typedef struct _WMDM_PROP_VALUES_ENUM {
  UINT        cEnumValues;
  PROPVARIANT *pValues;
} WMDM_PROP_VALUES_ENUM;
```



## <a name="members"></a>Member

<dl> <dt>

**cEnumValues**
</dt> <dd>

Anzahl der aufgezählten Werte.

</dd> <dt>

**pValues**
</dt> <dd>

Zeiger auf ein Array von Werten. Die Größe des Arrays entspricht dem Wert von **cEnumValues**.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Diese Struktur wird in der **WMDM \_ PROP \_ DESC-Struktur** verwendet, um einen enumerierten Satz gültiger Werte zu beschreiben. Ein aufzählter Satz gültiger Werte ist anwendbar, wenn WMDM \_ ENUM PROP VALID VALUES ENUM aus der \_ \_ \_ \_ **WMDM \_ ENUM \_ PROP VALID VALUES \_ \_ \_ FORM-Enumeration ausgewählt** wird.

Der Aufrufer ist erforderlich, um den von **pValues** verwendeten Arbeitsspeicher frei zu geben. Ein Beispiel hierfür finden Sie unter [**WMDM \_ FORMAT \_ CAPABILITY**](wmdm-format-capability.md).

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

[**WMDM \_ PROP \_ VALUES \_ RANGE**](wmdm-prop-values-range.md)
</dt> <dt>

[**Strukturen**](structures.md)
</dt> </dl>

 

 





