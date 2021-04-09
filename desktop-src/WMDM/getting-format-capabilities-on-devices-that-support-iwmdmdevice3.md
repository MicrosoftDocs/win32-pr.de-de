---
title: Erhalten von Formatfunktionen über IWMDMDevice3
description: Erhalten von Format Funktionen auf Geräten, die IWMDMDevice3 unterstützen
ms.assetid: a431c3cb-e722-4d68-a82d-385fff067ea6
keywords:
- Windows Media Device Manager, Gerätefunktionen
- Device Manager, Gerätefunktionen
- Programmier Handbuch, Gerätefunktionen
- Desktop Anwendungen, Gerätefunktionen
- Erstellen von Windows Media Device Manager-Anwendungen, Gerätefunktionen
- Schreiben von Dateien auf Geräte, Gerätefunktionen
- IWMDMDevice3-Methode
- Windows Media Device Manager, IWMDMDevice3-Methode
- Device Manager, IWMDMDevice3-Methode
- Programmier Handbuch, IWMDMDevice3-Methode
- Desktop Anwendungen, IWMDMDevice3-Methode
- Erstellen von Windows Media Device Manager-Anwendungen, IWMDMDevice3-Methode
- Schreiben von Dateien auf Geräte, IWMDMDevice3-Methode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 734f674a5fc54aaec0df10d4db613fa067f9b505
ms.sourcegitcommit: b95a94ffffda33f9ebbdd41787c01866444b4cf4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/27/2019
ms.locfileid: "104038406"
---
# <a name="getting-format-capabilities-through-iwmdmdevice3"></a>Erhalten von Formatfunktionen über IWMDMDevice3

[**IWMDMDevice3:: getformatcapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability) ist die bevorzugte Methode, um ein Gerät zu Fragen, welche Formate unterstützt werden. Die folgenden Schritte zeigen, wie Sie mit dieser Methode ein Gerät für seine Formatfunktionen Abfragen können:

1.  Die Anwendung muss bestimmen, welche Formate von einem Gerät unterstützt werden und welche von Interesse sind. Zu diesem Zweck kann die Anwendung durch Aufrufen von [**IWMDMDevice3:: GetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty)eine Liste der vom Gerät unterstützten Formate anfordern.
2.  Die Anwendung durchläuft alle unterstützten Formate und fordert die Formatierungsfunktionen eines Geräts für ein bestimmtes Format (z. b. WMA oder WMV) an, indem **IWMDMDevice3:: getformatcapability** aufgerufen und ein Format mithilfe der [**WMDM- \_ Formatcode**](wmdm-formatcode.md) -Enumeration angegeben wird. Diese Methode ruft eine Funktionsstruktur für das [**WMDM- \_ Format \_**](wmdm-format-capability.md) ab.
3.  Durchlaufen Sie alle [**WMDM- \_ Prop- \_ Konfigurations**](wmdm-prop-config.md) Strukturen in der abgerufenen **WMDM- \_ formatfunktionsstruktur \_** . Jede **\_ \_ Konfigurations Struktur von WMDM-Prop** enthält eine Gruppe von Eigenschaften mit unterstützten Werten, die eine Konfiguration für dieses Format darstellen. Jede Konfiguration verfügt über eine bevorzugte Zahl, bei der eine niedrigere Zahl eine höhere Einstellung für das Gerät angibt.
4.  Durchlaufen aller [**WMDM- \_ Prop- \_ MASC**](wmdm-prop-desc.md) -Strukturen in der abgerufenen **WMDM- \_ Prop- \_ Konfiguration**. Jede **WMDM- \_ Prop- \_ Abteilung** enthält eine Liste der unterstützten Eigenschaft/Wert-Paare.
5.  Rufen Sie die Eigenschaftsnamen und-Werte aus der **WMDM- \_ Prop \_** -Debug-Struktur ab. Zu den Eigenschaften zählen Bitrate, Codec und Frame Größe. Eigenschaftsnamen werden in der Header Datei "mswap. h" definiert. eine Liste der meisten dieser Konstanten wird in den [metadatenkonstanten](metadata-constants.md)angegeben. Drei Typen von Eigenschafts Werten sind möglich:
    -   Ein einzelner Wert, WMDM-Enumeration, \_ \_ \_ gültige \_ Werte, die die \_ Unterstützung für alle Werte für diese Eigenschaft angeben.
    -   Ein Wertebereich, der durch einen maximalen Wert, einen minimalen Wert und ein Intervall definiert wird.
    -   Eine Liste von diskreten Werten.
6.  Löschen Sie die gespeicherten Werte. Der Arbeitsspeicher für diese Werte wird von Windows Media Device Manager zugeordnet. Ihr Gerät ist für die Freigabe des Arbeitsspeichers verantwortlich. Diese Vorgehensweise wird am Ende dieses Themas beschrieben.

Bei der Reaktion auf **getformatcapability** können von einem Gerät WMDM-Enumerationswerte \_ \_ \_ \_ für gültige Werte für die \_ **WMDM- \_ Format \_ Funktion gemeldet werden. WMDM- \_ Prop- \_ Konfiguration. WMDM- \_ Prop- \_ Abteilung. Validvaluesform** , um die Unterstützung für alle Werte für Bitrate, Kanäle usw. zu beanspruchen. Sie sollten diesen Anspruch jedoch mit Vorsicht behandeln, da Geräte manchmal Unterstützung für beliebige Werte melden können, wenn Sie nicht alle Bitraten oder Bildgrößen unterstützen. Sie sollten in Erwägung gezogen werden, dass Ihre Anwendung extrem große Dateien oder High-Bit-Rate-Dateien in kleinere Versionen oder weniger speicherintensive und CPU-intensive Versionen umwandelt, wenn Sie Sie an Geräte senden, die diese Dateien wiedergeben sollen.

Die folgende C++-Funktion zeigt, wie Sie die Unterstützung von Geräte Formaten für ein bestimmtes Format anfordern.


```C++
HRESULT GetFormatCaps(WMDM_FORMATCODE formatCode, IWMDMDevice3* pDevice)
{
    HRESULT hr = S_OK;

    // Get a list of supported configurations for the format.
    WMDM_FORMAT_CAPABILITY formatCapList;
    hr = pDevice->GetFormatCapability(formatCode, &formatCapList);
    if (FAILED(hr)) return E_FAIL;

    // TODO: Display the format name.
    // Loop through the configurations and examine each one.
    for (UINT iConfig = 0; iConfig < formatCapList.nPropConfig; iConfig++)
    {
        WMDM_PROP_CONFIG formatConfig = formatCapList.pConfigs[iConfig];

        // Preference level for this configuration (lower number means more preferred).
        // TODO: Display the preference level for this format configuration.

        // Loop through all properties for this configuration and get supported
        // values for the property. Values can be a single value, a range, 
        // or a list of enumerated values.
        for (UINT iDesc = 0; iDesc < formatConfig.nPropDesc; iDesc++)
        {
            WMDM_PROP_DESC propDesc = formatConfig.pPropDesc[iDesc];
            // TODO: Display the property name.

            // Three ways a value can be represented: any, a range, or a list.
            switch (propDesc.ValidValuesForm)
            {
                case WMDM_ENUM_PROP_VALID_VALUES_ANY:
                    // TODO: Display a message indicating that all values are valid.
                    break;
                case WMDM_ENUM_PROP_VALID_VALUES_RANGE:
                    {
                        // List these in the docs as the propvariants set.
                        WMDM_PROP_VALUES_RANGE rng = 
                            propDesc.ValidValues.ValidValuesRange;
                        // TODO: Display the min, max, and step values.
                    }
                    break;
                case WMDM_ENUM_PROP_VALID_VALUES_ENUM:
                    {
                        // TODO: Display a banner for the list of valid values.
                        WMDM_PROP_VALUES_ENUM list = propDesc.ValidValues.EnumeratedValidValues;
                        PROPVARIANT pVal;
                        for (UINT iValue = 0; iValue < list.cEnumValues; iValue++)
                        {
                            pVal = list.pValues[iValue];
                            // TODO: Display each valid value.
                            PropVariantClear(&pVal);
                            PropVariantInit(&pVal);
                        }
                    }

                    break;
                default:
                    return E_FAIL,
                    break;
            }
        }
    }
    // Now clear the memory used by WMDM_FORMAT_CAPABILITY.
    FreeFormatCapability(formatCapList);
    return hr;
}
```



**Löschen von zugewiesener Speicher**

Nachdem Sie die Formatierungsfunktionen von einem Gerät abgerufen haben, muss die Anwendung den Arbeitsspeicher freigeben, der der Beschreibung zugeordnet ist. [**Getformatsupport**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-getformatsupport) und [**GetFormatSupport2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice2-getformatsupport2) verfügen über Arrays von einfachen Strukturen, die durch einfaches Aufrufen von **CoTaskMemFree** mit dem Array gelöscht werden können. Allerdings verfügt **getformatcapability** über eine komplexere Datenstruktur mit dynamisch zugewiesener Arbeitsspeicher, die durch Schleifen durch alle Elemente gelöscht und einzeln freigegeben werden muss.

Der folgende C++-Code zeigt, wie eine Anwendung den für eine **WMDM- \_ Format \_** Funktionsstruktur zugeordneten Arbeitsspeicher freigeben kann.


```C++
void CWMDMController::FreeFormatCapability(WMDM_FORMAT_CAPABILITY formatCap)
{
    // Loop through all configurations.
    for (UINT i = 0; i < formatCap.nPropConfig; i++) 
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



**Abfragen für alle unterstützten Formate**

In der Regel fragt eine Anwendung ein Gerät nach einem bestimmten Format ab, da es daran interessiert ist, eine bestimmte Datei an das Gerät zu senden. Wenn Sie jedoch eine Anwendung für alle unterstützten Formate Abfragen möchten, können Sie [**IWMDMDevice3:: GetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty) aufrufen und g \_ wszwmdmformatssupported übergeben, um eine vollständige Liste abzurufen.

Wenn ein Gerät nur ein Element zurückgibt, WMDM- \_ Formatcode \_ nicht definiert ist, bedeutet dies in der Regel, dass das Gerät keine Formatcodes unterstützt. Wenn **getformatcapability** mit nicht definiertem WMDM- \_ Format Code aufgerufen wird \_ , werden möglicherweise Funktionen abgerufen. diese Eigenschaften sind jedoch möglicherweise recht generisch (z. b. Name, Dateigröße, Datum der letzten Änderung usw.).

Die folgenden Schritte zeigen, wie Sie eine Liste aller unterstützten Formate Abfragen:

1.  Fordern Sie eine Liste aller durch den Aufruf von **IWMDMDevice3:: GetProperty** unterstützten Formatcodes an, und übergeben Sie g \_ wszwmdmformatssupported. Dadurch wird eine **PROPVARIANT** zurückgegeben, die ein **SAFEARRAY** unterstützter Formate enthält.
2.  Durchlaufen Sie die Elemente durch den Aufruf von **safearraygetelements**. Jedes Element ist eine **WMDM- \_ Formatcode** -Enumeration.
3.  Fordern Sie die Funktionen für jedes Format an, und machen Sie den Arbeitsspeicher für jedes der **WMDM- \_ Formatierungs \_** Elemente frei
4.  Löschen Sie die in Schritt 1 abgerufene **PROPVARIANT** durch Aufrufen von **propvariantclear**.

Der folgende C++-Beispielcode ruft eine Liste der unterstützten Formate für ein Gerät ab.


```C++
// Query a device for supported configurations for each media or format type. 
HRESULT CWMDMController::GetCaps(IWMDMDevice3* pDevice)
{
    HRESULT hr = S_OK;

    // Request the "formats supported" property to get a list of supported formats.
    PROPVARIANT pvFormatsSupported;
    PropVariantInit(&pvFormatsSupported);
    hr = pDevice->GetProperty(g_wszWMDMFormatsSupported, &pvFormatsSupported);
    HANDLE_HR(hr, "Got a property list in GetCaps", "Couldn't get a property list in GetCaps.");

    // Loop through the retrieved format list.
    // For each format, get a list of format configurations.
    SAFEARRAY* formatList = pvFormatsSupported.parray;
    WMDM_FORMATCODE formatCode = WMDM_FORMATCODE_NOTUSED;
    for (LONG iCap = 0; iCap < formatList->rgsabound[0].cElements; iCap++)
    { 
        // Get a format from the SAFEARRAY of retrieved formats.
        SafeArrayGetElement(formatList, &iCap, &formatCode);

        // Call a custom function to request the format capabilities.
        if (formatCode != WMDM_FORMATCODE_NOTUSED)
            myGetFormatCaps(formatCode, pDevice);
    }

e_Exit:
    // Clear out the memory we used.
    PropVariantClear(&pvFormatsSupported);
    return hr;
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Ermitteln der Funktionen des Geräte Formats**](discovering-device-format-capabilities.md)
</dt> </dl>

 

 




