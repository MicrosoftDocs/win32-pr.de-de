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
# <a name="getting-format-capabilities-through-iwmdmdevice3"></a><span data-ttu-id="d8632-116">Erhalten von Formatfunktionen über IWMDMDevice3</span><span class="sxs-lookup"><span data-stu-id="d8632-116">Getting format capabilities through IWMDMDevice3</span></span>

<span data-ttu-id="d8632-117">[**IWMDMDevice3:: getformatcapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability) ist die bevorzugte Methode, um ein Gerät zu Fragen, welche Formate unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="d8632-117">[**IWMDMDevice3::GetFormatCapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability) is the preferred method for asking a device what formats it supports.</span></span> <span data-ttu-id="d8632-118">Die folgenden Schritte zeigen, wie Sie mit dieser Methode ein Gerät für seine Formatfunktionen Abfragen können:</span><span class="sxs-lookup"><span data-stu-id="d8632-118">The following steps show how to use this method to query a device for its format capabilities:</span></span>

1.  <span data-ttu-id="d8632-119">Die Anwendung muss bestimmen, welche Formate von einem Gerät unterstützt werden und welche von Interesse sind.</span><span class="sxs-lookup"><span data-stu-id="d8632-119">The application must determine which formats a device supports and which are of interest.</span></span> <span data-ttu-id="d8632-120">Zu diesem Zweck kann die Anwendung durch Aufrufen von [**IWMDMDevice3:: GetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty)eine Liste der vom Gerät unterstützten Formate anfordern.</span><span class="sxs-lookup"><span data-stu-id="d8632-120">To do this, the application can request a list of formats supported by the device by calling [**IWMDMDevice3::GetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty).</span></span>
2.  <span data-ttu-id="d8632-121">Die Anwendung durchläuft alle unterstützten Formate und fordert die Formatierungsfunktionen eines Geräts für ein bestimmtes Format (z. b. WMA oder WMV) an, indem **IWMDMDevice3:: getformatcapability** aufgerufen und ein Format mithilfe der [**WMDM- \_ Formatcode**](wmdm-formatcode.md) -Enumeration angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="d8632-121">The application loops through all of the supported formats and requests a device's format capabilities for a specific format (such as WMA or WMV) by calling **IWMDMDevice3::GetFormatCapability** and specifying a format using the [**WMDM\_FORMATCODE**](wmdm-formatcode.md) enumeration.</span></span> <span data-ttu-id="d8632-122">Diese Methode ruft eine Funktionsstruktur für das [**WMDM- \_ Format \_**](wmdm-format-capability.md) ab.</span><span class="sxs-lookup"><span data-stu-id="d8632-122">This method retrieves a [**WMDM\_FORMAT\_CAPABILITY**](wmdm-format-capability.md) structure.</span></span>
3.  <span data-ttu-id="d8632-123">Durchlaufen Sie alle [**WMDM- \_ Prop- \_ Konfigurations**](wmdm-prop-config.md) Strukturen in der abgerufenen **WMDM- \_ formatfunktionsstruktur \_** .</span><span class="sxs-lookup"><span data-stu-id="d8632-123">Loop through all the [**WMDM\_PROP\_CONFIG**](wmdm-prop-config.md) structures in the retrieved **WMDM\_FORMAT\_CAPABILITY** structure.</span></span> <span data-ttu-id="d8632-124">Jede **\_ \_ Konfigurations Struktur von WMDM-Prop** enthält eine Gruppe von Eigenschaften mit unterstützten Werten, die eine Konfiguration für dieses Format darstellen.</span><span class="sxs-lookup"><span data-stu-id="d8632-124">Each **WMDM\_PROP\_CONFIG** structure holds a group of properties with supported values, representing one configuration for that format.</span></span> <span data-ttu-id="d8632-125">Jede Konfiguration verfügt über eine bevorzugte Zahl, bei der eine niedrigere Zahl eine höhere Einstellung für das Gerät angibt.</span><span class="sxs-lookup"><span data-stu-id="d8632-125">Each configuration has a preference number, where a lower number indicates a greater preference by the device.</span></span>
4.  <span data-ttu-id="d8632-126">Durchlaufen aller [**WMDM- \_ Prop- \_ MASC**](wmdm-prop-desc.md) -Strukturen in der abgerufenen **WMDM- \_ Prop- \_ Konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="d8632-126">Loop through all the [**WMDM\_PROP\_DESC**](wmdm-prop-desc.md) structures in the retrieved **WMDM\_PROP\_CONFIG**.</span></span> <span data-ttu-id="d8632-127">Jede **WMDM- \_ Prop- \_ Abteilung** enthält eine Liste der unterstützten Eigenschaft/Wert-Paare.</span><span class="sxs-lookup"><span data-stu-id="d8632-127">Each **WMDM\_PROP\_DESC** contains a list of supported property/value pairs.</span></span>
5.  <span data-ttu-id="d8632-128">Rufen Sie die Eigenschaftsnamen und-Werte aus der **WMDM- \_ Prop \_** -Debug-Struktur ab.</span><span class="sxs-lookup"><span data-stu-id="d8632-128">Retrieve the property names and values from the **WMDM\_PROP\_DESC** structure.</span></span> <span data-ttu-id="d8632-129">Zu den Eigenschaften zählen Bitrate, Codec und Frame Größe.</span><span class="sxs-lookup"><span data-stu-id="d8632-129">Properties include bit rate, codec, and frame size.</span></span> <span data-ttu-id="d8632-130">Eigenschaftsnamen werden in der Header Datei "mswap. h" definiert. eine Liste der meisten dieser Konstanten wird in den [metadatenkonstanten](metadata-constants.md)angegeben.</span><span class="sxs-lookup"><span data-stu-id="d8632-130">Property names are defined in the mswmdm.h header file; a list of most of these constants is given in [Metadata Constants](metadata-constants.md).</span></span> <span data-ttu-id="d8632-131">Drei Typen von Eigenschafts Werten sind möglich:</span><span class="sxs-lookup"><span data-stu-id="d8632-131">Three types of property values are possible:</span></span>
    -   <span data-ttu-id="d8632-132">Ein einzelner Wert, WMDM-Enumeration, \_ \_ \_ gültige \_ Werte, die die \_ Unterstützung für alle Werte für diese Eigenschaft angeben.</span><span class="sxs-lookup"><span data-stu-id="d8632-132">A single value, WMDM\_ENUM\_PROP\_VALID\_VALUES\_ANY, indicating support for any values for this property.</span></span>
    -   <span data-ttu-id="d8632-133">Ein Wertebereich, der durch einen maximalen Wert, einen minimalen Wert und ein Intervall definiert wird.</span><span class="sxs-lookup"><span data-stu-id="d8632-133">A range of values, defined by a maximum value, minimum value, and interval.</span></span>
    -   <span data-ttu-id="d8632-134">Eine Liste von diskreten Werten.</span><span class="sxs-lookup"><span data-stu-id="d8632-134">A list of discrete values.</span></span>
6.  <span data-ttu-id="d8632-135">Löschen Sie die gespeicherten Werte.</span><span class="sxs-lookup"><span data-stu-id="d8632-135">Clear the stored values.</span></span> <span data-ttu-id="d8632-136">Der Arbeitsspeicher für diese Werte wird von Windows Media Device Manager zugeordnet. Ihr Gerät ist für die Freigabe des Arbeitsspeichers verantwortlich.</span><span class="sxs-lookup"><span data-stu-id="d8632-136">Memory for these values is allocated by Windows Media Device Manager; your device is responsible for freeing the memory.</span></span> <span data-ttu-id="d8632-137">Diese Vorgehensweise wird am Ende dieses Themas beschrieben.</span><span class="sxs-lookup"><span data-stu-id="d8632-137">How to do this is described at the end of this topic.</span></span>

<span data-ttu-id="d8632-138">Bei der Reaktion auf **getformatcapability** können von einem Gerät WMDM-Enumerationswerte \_ \_ \_ \_ für gültige Werte für die \_ **WMDM- \_ Format \_ Funktion gemeldet werden. WMDM- \_ Prop- \_ Konfiguration. WMDM- \_ Prop- \_ Abteilung. Validvaluesform** , um die Unterstützung für alle Werte für Bitrate, Kanäle usw. zu beanspruchen.</span><span class="sxs-lookup"><span data-stu-id="d8632-138">When responding to **GetFormatCapability**, a device can report WMDM\_ENUM\_PROP\_VALID\_VALUES\_ANY for **WMDM\_FORMAT\_CAPABILITY.WMDM\_PROP\_CONFIG.WMDM\_PROP\_DESC.ValidValuesForm** to claim support for any values for bit rate, channels, and so on.</span></span> <span data-ttu-id="d8632-139">Sie sollten diesen Anspruch jedoch mit Vorsicht behandeln, da Geräte manchmal Unterstützung für beliebige Werte melden können, wenn Sie nicht alle Bitraten oder Bildgrößen unterstützen.</span><span class="sxs-lookup"><span data-stu-id="d8632-139">However, you should treat this claim with caution, because devices can sometimes report support for any values when in fact they do not support all bit rates or image sizes.</span></span> <span data-ttu-id="d8632-140">Sie sollten in Erwägung gezogen werden, dass Ihre Anwendung extrem große Dateien oder High-Bit-Rate-Dateien in kleinere Versionen oder weniger speicherintensive und CPU-intensive Versionen umwandelt, wenn Sie Sie an Geräte senden, die diese Dateien wiedergeben sollen.</span><span class="sxs-lookup"><span data-stu-id="d8632-140">You might consider having your application transcode extremely large or high-bit-rate files to smaller versions or less memory-intensive and CPU-intensive versions when sending them to devices that are intended to play these files.</span></span>

<span data-ttu-id="d8632-141">Die folgende C++-Funktion zeigt, wie Sie die Unterstützung von Geräte Formaten für ein bestimmtes Format anfordern.</span><span class="sxs-lookup"><span data-stu-id="d8632-141">The following C++ function shows how to request device format support for a specific format.</span></span>


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



<span data-ttu-id="d8632-142">**Löschen von zugewiesener Speicher**</span><span class="sxs-lookup"><span data-stu-id="d8632-142">**Clearing allocated memory**</span></span>

<span data-ttu-id="d8632-143">Nachdem Sie die Formatierungsfunktionen von einem Gerät abgerufen haben, muss die Anwendung den Arbeitsspeicher freigeben, der der Beschreibung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="d8632-143">After retrieving format capabilities from a device, the application must free the memory allocated to hold the description.</span></span> <span data-ttu-id="d8632-144">[**Getformatsupport**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-getformatsupport) und [**GetFormatSupport2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice2-getformatsupport2) verfügen über Arrays von einfachen Strukturen, die durch einfaches Aufrufen von **CoTaskMemFree** mit dem Array gelöscht werden können.</span><span class="sxs-lookup"><span data-stu-id="d8632-144">[**GetFormatSupport**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-getformatsupport) and [**GetFormatSupport2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice2-getformatsupport2) have arrays of simple structures that can be cleared by simply calling **CoTaskMemFree** with the array.</span></span> <span data-ttu-id="d8632-145">Allerdings verfügt **getformatcapability** über eine komplexere Datenstruktur mit dynamisch zugewiesener Arbeitsspeicher, die durch Schleifen durch alle Elemente gelöscht und einzeln freigegeben werden muss.</span><span class="sxs-lookup"><span data-stu-id="d8632-145">However, **GetFormatCapability** has a more complex data structure with dynamically allocated memory that must be cleared by looping through all the elements and freeing them individually.</span></span>

<span data-ttu-id="d8632-146">Der folgende C++-Code zeigt, wie eine Anwendung den für eine **WMDM- \_ Format \_** Funktionsstruktur zugeordneten Arbeitsspeicher freigeben kann.</span><span class="sxs-lookup"><span data-stu-id="d8632-146">The following C++ code shows how an application can free the memory allocated for a **WMDM\_FORMAT\_CAPABILITY** structure.</span></span>


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



<span data-ttu-id="d8632-147">**Abfragen für alle unterstützten Formate**</span><span class="sxs-lookup"><span data-stu-id="d8632-147">**Querying for all supported formats**</span></span>

<span data-ttu-id="d8632-148">In der Regel fragt eine Anwendung ein Gerät nach einem bestimmten Format ab, da es daran interessiert ist, eine bestimmte Datei an das Gerät zu senden.</span><span class="sxs-lookup"><span data-stu-id="d8632-148">Typically, an application queries a device for a specific format, because it is interested in sending a specific file to the device.</span></span> <span data-ttu-id="d8632-149">Wenn Sie jedoch eine Anwendung für alle unterstützten Formate Abfragen möchten, können Sie [**IWMDMDevice3:: GetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty) aufrufen und g \_ wszwmdmformatssupported übergeben, um eine vollständige Liste abzurufen.</span><span class="sxs-lookup"><span data-stu-id="d8632-149">However, if you want to query an application for all its supported formats, you can call [**IWMDMDevice3::GetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty) and pass in g\_wszWMDMFormatsSupported to retrieve a full list.</span></span>

<span data-ttu-id="d8632-150">Wenn ein Gerät nur ein Element zurückgibt, WMDM- \_ Formatcode \_ nicht definiert ist, bedeutet dies in der Regel, dass das Gerät keine Formatcodes unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d8632-150">If a device only returns one element, WMDM\_FORMATCODE\_UNDEFINED, this usually means that the device does not support format codes.</span></span> <span data-ttu-id="d8632-151">Wenn **getformatcapability** mit nicht definiertem WMDM- \_ Format Code aufgerufen wird \_ , werden möglicherweise Funktionen abgerufen. diese Eigenschaften sind jedoch möglicherweise recht generisch (z. b. Name, Dateigröße, Datum der letzten Änderung usw.).</span><span class="sxs-lookup"><span data-stu-id="d8632-151">Calling **GetFormatCapability** with WMDM\_FORMATCODE\_UNDEFINED might retrieve capabilities, but these properties might be fairly generic (such as name, file size, last modified date, and so on).</span></span>

<span data-ttu-id="d8632-152">Die folgenden Schritte zeigen, wie Sie eine Liste aller unterstützten Formate Abfragen:</span><span class="sxs-lookup"><span data-stu-id="d8632-152">The following steps show how to query for a list of all supported formats:</span></span>

1.  <span data-ttu-id="d8632-153">Fordern Sie eine Liste aller durch den Aufruf von **IWMDMDevice3:: GetProperty** unterstützten Formatcodes an, und übergeben Sie g \_ wszwmdmformatssupported.</span><span class="sxs-lookup"><span data-stu-id="d8632-153">Request a list of all format codes supported by calling **IWMDMDevice3::GetProperty** and passing in g\_wszWMDMFormatsSupported.</span></span> <span data-ttu-id="d8632-154">Dadurch wird eine **PROPVARIANT** zurückgegeben, die ein **SAFEARRAY** unterstützter Formate enthält.</span><span class="sxs-lookup"><span data-stu-id="d8632-154">This returns a **PROPVARIANT** containing a **SAFEARRAY** of supported formats.</span></span>
2.  <span data-ttu-id="d8632-155">Durchlaufen Sie die Elemente durch den Aufruf von **safearraygetelements**.</span><span class="sxs-lookup"><span data-stu-id="d8632-155">Loop through the elements by calling **SafeArrayGetElement**.</span></span> <span data-ttu-id="d8632-156">Jedes Element ist eine **WMDM- \_ Formatcode** -Enumeration.</span><span class="sxs-lookup"><span data-stu-id="d8632-156">Each element is a **WMDM\_FORMATCODE** enumeration.</span></span>
3.  <span data-ttu-id="d8632-157">Fordern Sie die Funktionen für jedes Format an, und machen Sie den Arbeitsspeicher für jedes der **WMDM- \_ Formatierungs \_** Elemente frei</span><span class="sxs-lookup"><span data-stu-id="d8632-157">Request the capabilities for each format, freeing the memory for each **WMDM\_FORMAT\_CAPABILITY** element once done with it.</span></span>
4.  <span data-ttu-id="d8632-158">Löschen Sie die in Schritt 1 abgerufene **PROPVARIANT** durch Aufrufen von **propvariantclear**.</span><span class="sxs-lookup"><span data-stu-id="d8632-158">Clear the **PROPVARIANT** retrieved in step 1 by calling **PropVariantClear**.</span></span>

<span data-ttu-id="d8632-159">Der folgende C++-Beispielcode ruft eine Liste der unterstützten Formate für ein Gerät ab.</span><span class="sxs-lookup"><span data-stu-id="d8632-159">The following C++ example code retrieves a list of supported formats for a device.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="d8632-160">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d8632-160">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d8632-161">**Ermitteln der Funktionen des Geräte Formats**</span><span class="sxs-lookup"><span data-stu-id="d8632-161">**Discovering Device Format Capabilities**</span></span>](discovering-device-format-capabilities.md)
</dt> </dl>

 

 




