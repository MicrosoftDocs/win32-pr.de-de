---
title: WMDM_PROP_CONFIG Struktur
description: Die WMDM- \_ Prop- \_ Konfigurations Struktur beschreibt eine Reihe kompatibler Eigenschaftswerte für alle Eigenschaften, die vom Gerät für ein bestimmtes Format unterstützt werden. Diese Struktur enthält eine Reihe von Eigenschafts Beschreibungen in einem Array von WMDM-untergeordneten \_ \_ Strukturen.
ms.assetid: cf116861-e31d-4561-b262-e271888afc24
keywords:
- WMDM_PROP_CONFIG Struktur von Windows-Medien Device Manager
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
ms.openlocfilehash: 0b19314b2f012d25fa2d97b44b9dc7524f9e3355
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369368"
---
# <a name="wmdm_prop_config-structure"></a>WMDM- \_ Prop- \_ Konfigurations Struktur

Die **WMDM- \_ Prop- \_ Konfigurations** Struktur beschreibt eine Reihe kompatibler Eigenschaftswerte für alle Eigenschaften, die vom Gerät für ein bestimmtes Format unterstützt werden. Diese Struktur enthält eine Reihe von Eigenschafts Beschreibungen in einem Array von [**WMDM-unter \_ \_**](wmdm-prop-desc.md) geordneten Strukturen.

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

**npreference**
</dt> <dd>

Die bevorzugte Ebene des Geräts für diese Konfiguration. Der niedrigste Wert gibt die bevorzugte Konfiguration an.

</dd> <dt>

**npropentsc**
</dt> <dd>

Anzahl der Eigenschafts Beschreibungen, die in dieser Konfiguration enthalten sind. Für jede Eigenschaft, die für das angegebene Format unterstützt wird, gibt es eine einzelne Eigenschafts Beschreibung.

</dd> <dt>

**ppropentsc**
</dt> <dd>

Zeiger auf ein Array von [**WMDM \_ \_**](wmdm-prop-desc.md) -untergeordneten Strukturen, die Eigenschafts Beschreibungen enthalten. Die Größe des Arrays ist gleich dem Wert von **npropde SC**. Die Anwendung muss diesen Arbeitsspeicher freigeben, wenn Sie damit fertig ist.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die von [**IWMDMDevice3:: getformatcapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability) für ein bestimmtes Format zurückgegebene [**WMDM- \_ Format \_**](wmdm-format-capability.md) Funktionsstruktur besteht aus einer Reihe von Eigenschafts Konfigurationen. **WMDM \_ Diese \_** Konfigurationen werden von der prop-Konfigurations Struktur beschrieben.

Eine Eigenschaften Konfiguration beschreibt Werte für alle Eigenschaften, die für ein bestimmtes Format unterstützt werden. Die Werte verschiedener Eigenschaften in einer einzelnen Konfiguration sind miteinander kompatibel. Beispielsweise enthält eine Konfiguration für eine Audiodatei gültige Werte der Samplingrate und gültige Werte der Bitrate, sodass alle Kombinationen dieser Stichproben-und Bitraten auf dem Gerät wiedergegeben werden können.

Der Aufrufer muss den von **ppropde** genutzten Arbeitsspeicher freigeben. Ein Beispiel hierfür finden Sie unter [**WMDM- \_ Format \_ Funktion**](wmdm-format-capability.md).

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

[**WMDM- \_ Prop- \_ Abteilung**](wmdm-prop-desc.md)
</dt> <dt>

[**WMDM- \_ Prop \_ Values- \_ Enumeration**](wmdm-prop-values-enum.md)
</dt> <dt>

[**Bereich der WMDM- \_ Prop- \_ Werte \_**](wmdm-prop-values-range.md)
</dt> <dt>

[**Strukturen**](structures.md)
</dt> </dl>

 

 





