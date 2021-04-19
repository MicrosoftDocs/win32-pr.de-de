---
title: WMDM_FORMAT_CAPABILITY Struktur
description: Die Funktionsstruktur des WMDM- \_ Formats \_ beschreibt die Funktionen eines Geräts für ein bestimmtes Format.
ms.assetid: 9672173D-B11E-4DCB-BCAE-38B94FCC8B99
keywords:
- WMDM_FORMAT_CAPABILITY Struktur von Windows-Medien Device Manager
topic_type:
- apiref
api_name:
- WMDM_FORMAT_CAPABILITY
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14f8dbdd81aff63a819624cdb1c778cb9bec712b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367558"
---
# <a name="wmdm_format_capability-structure"></a>Struktur der WMDM- \_ Format \_ Funktion

Die Funktionsstruktur des **WMDM- \_ Formats \_** beschreibt die Funktionen eines Geräts für ein bestimmtes Format. Diese Struktur enthält eine Reihe von Eigenschaften Konfigurationen in einem Array von **WMDM- \_ Prop- \_ Konfigurations** Strukturen. Jede Eigenschaften Konfiguration stellt einen Satz kompatibler Eigenschaftswerte für alle Eigenschaften dar, die für ein bestimmtes Format unterstützt werden. Die Anwendung kann diese Struktur abrufen, indem Sie die **IWMDMDevice3:: getformatcapability** -Methode aufruft und den Format Code übergibt. Eine Liste der Formatcodes finden Sie unter [**WMDM \_ Formatcode**](wmdm-formatcode.md).

## <a name="syntax"></a>Syntax


```C++
typedef struct _WMDM_FORMAT_CAPABILITY {
  UINT              nPropConfig;
  WMDM_PROP_CONFIG  *pConfigs;
} WMDM_FORMAT_CAPABILITY;
```



## <a name="members"></a>Member

<dl> <dt>

**npropconfig**
</dt> <dd>

Anzahl der Eigenschafts Konfigurationen im **pconfigs** -Array.

</dd> <dt>

**pconfigs**
</dt> <dd>

Zeiger auf ein Array von [**WMDM- \_ Prop- \_ Konfigurations**](wmdm-prop-config.md) Strukturen. Die Größe des Arrays ist gleich dem Wert von **npropconfig**.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die Struktur der **WMDM- \_ Format \_ Funktionen** bietet einen flexiblen Mechanismus zum Ausdrücken der Funktionen des Geräts für ein bestimmtes Format.

Wenn der Inhalt vom Gerät gerendert werden soll (z. b. eine Audiodatei, die vom Gerät abgespielt werden soll), müssen die Eigenschaften des Inhalts einer der Eigenschafts Konfigurationen entsprechen, die von [**IWMDMDevice3:: getformatcapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability) in der Funktionsstruktur des **WMDM- \_ Formats \_** zurückgegeben werden. Beispielsweise müssen für eine Audiodatei die Bitrate und die Samplingrate eine der zurückgegebenen Eigenschafts Konfigurationen erfüllen.

Der Aufrufer ist dafür verantwortlich, den für diese Struktur zugeordneten Arbeitsspeicher freizugeben. Die folgende Funktion veranschaulicht, wie Sie eine Funktionsstruktur des **WMDM- \_ Formats \_** löschen.


```C++
void FreeFormatCapability(WMDM_FORMAT_CAPABILITY formatCap)
{
    // Loop through all configurations.
    for (UINT i=0; i < formatCap.nPropConfig; i++) 
    {
        // Loop through all descriptions of a configuration and delete
        // the values particular to that description type.
        for (UINT j=0; j < formatCap.pConfigs[i].nPropDesc; j++) 
        {
            switch (formatCap.pConfigs[i].pPropDesc[j].ValidValuesForm)
            {
                case WMDM_ENUM_PROP_VALID_VALUES_ENUM:
                    for (UINT k=0; k < formatCap.pConfigs[i].pPropDesc[j].ValidValues.EnumeratedValidValues.cEnumValues; k++)
                    {
                        PropVariantClear (&(formatCap.pConfigs[i].pPropDesc[j].ValidValues.EnumeratedValidValues.pValues[k]));
                    }
                    CoTaskMemFree(formatCap.pConfigs[i].pPropDesc[j].ValidValues.EnumeratedValidValues.pValues);
                    break;
                case WMDM_ENUM_PROP_VALID_VALUES_RANGE:
                    PropVariantClear (&(formatCap.pConfigs[i].pPropDesc[j].ValidValues.ValidValuesRange.rangeMin));
                    PropVariantClear (&(formatCap.pConfigs[i].pPropDesc[j].ValidValues.ValidValuesRange.rangeMax));
                    PropVariantClear (&(formatCap.pConfigs[i].pPropDesc[j].ValidValues.ValidValuesRange.rangeStep));
                    break;
                case WMDM_ENUM_PROP_VALID_VALUES_ANY:
                    // No dynamically allocated memory for this value.
                default:
                    break;
            }

            // Free the memory for the description name.
            CoTaskMemFree(formatCap.pConfigs[i].pPropDesc[j].pwszPropName);
        }
        // Free the memory holding the array of description items for this configuration.
        CoTaskMemFree(formatCap.pConfigs[i].pPropDesc);
    }

    // Free the memory pointing to the array of configurations.
    CoTaskMemFree(formatCap.pConfigs);
    formatCap.nPropConfig = 0;
}
```



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

[**WMDM- \_ Prop- \_ Konfiguration**](wmdm-prop-config.md)
</dt> <dt>

[**WMDM- \_ Prop- \_ Abteilung**](wmdm-prop-desc.md)
</dt> <dt>

[**WMDM- \_ Prop \_ Values- \_ Enumeration**](wmdm-prop-values-enum.md)
</dt> <dt>

[**Bereich der WMDM- \_ Prop- \_ Werte \_**](wmdm-prop-values-range.md)
</dt> <dt>

[**Strukturen**](structures.md)
</dt> </dl>

 

 





