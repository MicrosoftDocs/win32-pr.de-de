---
title: Abrufen von Formatfunktionen über IWMDMDevice3
description: Abrufen von Formatfunktionen auf Geräten, die IWMDMDevice3 unterstützen
ms.assetid: a431c3cb-e722-4d68-a82d-385fff067ea6
keywords:
- Windows Medien Geräte-Manager, Gerätefunktionen
- Geräte-Manager,Gerätefunktionen
- Programmierhandbuch, Gerätefunktionen
- Desktopanwendungen, Gerätefunktionen
- Erstellen von Windows Media Geräte-Manager-Anwendungen, Gerätefunktionen
- Schreiben von Dateien auf Geräte, Gerätefunktionen
- IWMDMDevice3-Methode
- Windows Media Geräte-Manager,IWMDMDevice3-Methode
- Geräte-Manager,IWMDMDevice3-Methode
- Programmierhandbuch,IWMDMDevice3-Methode
- Desktopanwendungen, IWMDMDevice3-Methode
- Erstellen Windows Media Geräte-Manager-Anwendungen, IWMDMDevice3-Methode
- Schreiben von Dateien auf Geräte, IWMDMDevice3-Methode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1eadde80f957573563468375ea06cd64b95cf83815491a3f21775fb1ebcefc7d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119957525"
---
# <a name="getting-format-capabilities-through-iwmdmdevice3"></a>Abrufen von Formatfunktionen über IWMDMDevice3

[**IWMDMDevice3::GetFormatCapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability) ist die bevorzugte Methode, um ein Gerät zu fragen, welche Formate es unterstützt. Die folgenden Schritte zeigen, wie Sie diese Methode verwenden, um ein Gerät nach seinen Formatfunktionen abzufragen:

1.  Die Anwendung muss bestimmen, welche Formate ein Gerät unterstützt und welche von Interesse sind. Hierzu kann die Anwendung eine Liste der vom Gerät unterstützten Formate anfordern, indem [**sie IWMDMDevice3::GetProperty aufruft.**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty)
2.  Die Anwendung durchläuft alle unterstützten Formate und fordert die Formatfunktionen eines Geräts für ein bestimmtes Format (z. B. WMA oder WMV) an, indem **sie IWMDMDevice3::GetFormatCapability** aufruft und ein Format mithilfe der [**WMDM \_ FORMATCODE-Enumeration**](wmdm-formatcode.md) angibt. Diese Methode ruft eine [**WMDM \_ FORMAT \_ CAPABILITY-Struktur**](wmdm-format-capability.md) ab.
3.  Durchlaufen Sie alle [**WMDM \_ PROP \_ CONFIG-Strukturen**](wmdm-prop-config.md) in der abgerufenen **WMDM \_ FORMAT \_ CAPABILITY-Struktur.** Jede **WMDM \_ PROP \_ CONFIG-Struktur** enthält eine Gruppe von Eigenschaften mit unterstützten Werten, die eine Konfiguration für dieses Format darstellen. Jede Konfiguration verfügt über eine Einstellungsnummer, wobei eine niedrigere Zahl eine höhere Einstellung durch das Gerät angibt.
4.  Durchlaufen Sie alle [**WMDM \_ PROP \_ DESC-Strukturen**](wmdm-prop-desc.md) in der abgerufenen **WMDM \_ PROP \_ CONFIG**. Jedes **WMDM \_ PROP \_ DESC** enthält eine Liste der unterstützten Eigenschaften-Wert-Paare.
5.  Rufen Sie die Eigenschaftennamen und -werte aus der **WMDM \_ PROP \_ DESC-Struktur** ab. Zu den Eigenschaften gehören Bitrate, Codec und Framegröße. Eigenschaftennamen werden in der Headerdatei mswmdm.h definiert. Eine Liste der meisten dieser Konstanten wird in [Metadatenkonstanten](metadata-constants.md)angegeben. Drei Typen von Eigenschaftswerten sind möglich:
    -   Ein einzelner Wert, WMDM \_ ENUM \_ PROP VALID VALUES \_ \_ \_ ANY, der die Unterstützung für alle Werte für diese Eigenschaft angibt.
    -   Ein Wertebereich, der durch einen Höchstwert, einen Mindestwert und ein Intervall definiert wird.
    -   Eine Liste diskreter Werte.
6.  Löschen Sie die gespeicherten Werte. Arbeitsspeicher für diese Werte wird von Windows Media Geräte-Manager zugeordnet. Ihr Gerät ist für das Freigeben des Arbeitsspeichers verantwortlich. Die Vorgehensweise wird am Ende dieses Themas beschrieben.

Wenn auf **GetFormatCapability** reagiert, kann ein Gerät WMDM \_ ENUM \_ PROP VALID VALUES ANY for \_ \_ \_ **WMDM \_ FORMAT \_ CAPABILITY melden. WMDM \_ PROP \_ CONFIG. WMDM \_ PROP \_ DESC. ValidValuesForm,** um Unterstützung für alle Werte für Bitrate, Kanäle usw. in Anspruch zu nehmen. Sie sollten diesen Anspruch jedoch mit Vorsicht behandeln, da Geräte manchmal Unterstützung für beliebige Werte melden können, wenn sie tatsächlich nicht alle Bitraten oder Bildgrößen unterstützen. Sie können erwägen, dass Ihre Anwendung extrem große oder Dateien mit hoher Bitrate in kleinere Versionen oder weniger speicher- und CPU-intensive Versionen transcodiert, wenn sie an Geräte gesendet werden, die diese Dateien wiedergeben sollen.

Die folgende C++-Funktion zeigt, wie Geräteformatunterstützung für ein bestimmtes Format angefordert wird.


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



**Löschen des belegten Arbeitsspeichers**

Nach dem Abrufen von Formatfunktionen von einem Gerät muss die Anwendung den zugeordneten Arbeitsspeicher freigeben, um die Beschreibung zu speichern. [**GetFormatSupport**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-getformatsupport) und [**GetFormatSupport2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice2-getformatsupport2) verfügen über Arrays einfacher Strukturen, die durch einfaches Aufrufen von **CoTaskMemFree** mit dem Array gelöscht werden können. **GetFormatCapability** verfügt jedoch über eine komplexere Datenstruktur mit dynamisch zugeordneten Arbeitsspeicher, die gelöscht werden muss, indem alle Elemente durchlaufen und einzeln freigegeben werden.

Der folgende C++-Code zeigt, wie eine Anwendung den Arbeitsspeicher freigeben kann, der einer **WMDM \_ FORMAT \_ CAPABILITY-Struktur** zugeordnet ist.


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



**Abfragen aller unterstützten Formate**

In der Regel fragt eine Anwendung ein Gerät nach einem bestimmten Format ab, da es daran interessiert ist, eine bestimmte Datei an das Gerät zu senden. Wenn Sie jedoch eine Anwendung nach allen unterstützten Formaten abfragen möchten, können Sie [**IWMDMDevice3::GetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty) aufrufen und g \_ wszWMDMFormatsSupported übergeben, um eine vollständige Liste abzurufen.

Wenn ein Gerät nur ein Element (WMDM \_ FORMATCODE \_ UNDEFINED) zurückgibt, bedeutet dies in der Regel, dass das Gerät keine Formatcodes unterstützt. Das Aufrufen von **GetFormatCapability** mit WMDM \_ FORMATCODE \_ UNDEFINED kann Funktionen abrufen, aber diese Eigenschaften können relativ generisch sein (z. B. Name, Dateigröße, Datum der letzten Änderung usw.).

Die folgenden Schritte zeigen, wie Sie eine Liste aller unterstützten Formate abfragen:

1.  Fordern Sie eine Liste aller Formatcodes an, die durch Aufrufen von **IWMDMDevice3::GetProperty** unterstützt werden, und übergeben Sie g \_ wszWMDMFormatsSupported. Dadurch wird ein **PROPVARIANT-Wert zurückgegeben,** der ein **SAFEARRAY-Format** mit unterstützten Formaten enthält.
2.  Durchlaufen Sie die Elemente, indem Sie **SafeArrayGetElement** aufrufen. Jedes Element ist eine **WMDM \_ FORMATCODE-Enumeration.**
3.  Fordern Sie die Funktionen für jedes Format an, und freigeben Sie anschließend den Arbeitsspeicher für jedes **WMDM \_ FORMAT \_ CAPABILITY-Element.**
4.  Löschen Sie das in Schritt 1 abgerufene **PROPVARIANT,** indem Sie **PropVariantClear** aufrufen.

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

[**Ermitteln von Geräteformatfunktionen**](discovering-device-format-capabilities.md)
</dt> </dl>

 

 




