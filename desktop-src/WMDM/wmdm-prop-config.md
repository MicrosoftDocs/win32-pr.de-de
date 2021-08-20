---
title: WMDM_PROP_CONFIG-Struktur
description: Die WMDM \_ PROP \_ CONFIG-Struktur beschreibt einen Satz kompatibler Eigenschaftswerte für alle Eigenschaften, die vom Gerät für ein bestimmtes Format unterstützt werden. Diese Struktur enthält eine Reihe von Eigenschaftenbeschreibungen in einem Array von WMDM \_ PROP \_ DESC-Strukturen.
ms.assetid: cf116861-e31d-4561-b262-e271888afc24
keywords:
- WMDM_PROP_CONFIG struktur windows Media Geräte-Manager
topic_type:
- apiref
api_name:
- WMDM_PROP_CONFIG
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e50cd18f5b7646934a6add71674f93ebaae700ab39e57f833e555ea3688ecb6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119862820"
---
# <a name="wmdm_prop_config-structure"></a>WMDM \_ PROP \_ CONFIG-Struktur

Die **WMDM \_ PROP \_ CONFIG-Struktur** beschreibt einen Satz kompatibler Eigenschaftswerte für alle Eigenschaften, die vom Gerät für ein bestimmtes Format unterstützt werden. Diese Struktur enthält eine Reihe von Eigenschaftenbeschreibungen in einem Array von [**WMDM \_ PROP \_ DESC-Strukturen.**](wmdm-prop-desc.md)

## <a name="syntax"></a>Syntax


```C++
typedef struct _WMDM_PROP_CONFIG {
  UINT           nPreference;
  UINT           nPropDesc;
  WMDM_PROP_DESC *pPropDesc;
} WMDM_PROP_CONFIG;
```



## <a name="members"></a>Member

<dl> <dt>

**nPreference**
</dt> <dd>

Gerätepräferenz für diese Konfiguration. Der niedrigste Wert gibt die bevorzugte Konfiguration an.

</dd> <dt>

**nPropDesc**
</dt> <dd>

Anzahl der in dieser Konfiguration enthaltenen Eigenschaftenbeschreibungen. Es gibt eine einzelne Eigenschaftenbeschreibung für jede Eigenschaft, die für das angegebene Format unterstützt wird.

</dd> <dt>

**pPropDesc**
</dt> <dd>

Zeiger auf ein Array von [**WMDM \_ PROP \_ DESC-Strukturen,**](wmdm-prop-desc.md) die Eigenschaftenbeschreibungen enthalten. Die Größe des Arrays entspricht dem Wert von **nPropDesc.** Die Anwendung muss diesen Arbeitsspeicher freigeben, wenn sie fertig ist.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die [**WMDM \_ FORMAT \_ CAPABILITY-Struktur,**](wmdm-format-capability.md) die von [**IWMDMDevice3::GetFormatCapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability) für ein bestimmtes Format zurückgegeben wird, besteht aus einer Reihe von Eigenschaftenkonfigurationen. **WMDM \_ PROP \_ CONFIG-Strukturen** beschreiben diese Konfigurationen.

Eine Eigenschaftenkonfiguration beschreibt Werte für alle Eigenschaften, die für ein bestimmtes Format unterstützt werden. Die Werte verschiedener Eigenschaften in einer einzelnen Konfiguration sind miteinander kompatibel. Beispielsweise enthält eine Konfiguration für eine Audiodatei gültige Werte der Abtastrate und gültige Werte der Bitrate, sodass alle Kombinationen dieser Stichproben- und Bitraten auf dem Gerät wiedergegeben werden können.

Der Aufrufer ist erforderlich, um den von **pPropDesc** verwendeten Arbeitsspeicher freizugeben. Ein Beispiel hierfür finden Sie unter [**WMDM \_ FORMAT \_ CAPABILITY**](wmdm-format-capability.md).

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

[**WMDM \_ PROP \_ DESC**](wmdm-prop-desc.md)
</dt> <dt>

[**WMDM \_ PROP \_ VALUES \_ ENUM**](wmdm-prop-values-enum.md)
</dt> <dt>

[**\_ \_ WMDM-PROP-WERTEBEREICH \_**](wmdm-prop-values-range.md)
</dt> <dt>

[**Strukturen**](structures.md)
</dt> </dl>

 

 





