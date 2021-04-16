---
description: Encoder-API
ms.assetid: 3d19152f-17a3-4576-a2a2-5b827d9ca8d1
title: Encoder-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 386b964f44dc4dc69896ead34bbe0d0177b198a1
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392773"
---
# <a name="encoder-api"></a><span data-ttu-id="e6804-103">Encoder-API</span><span class="sxs-lookup"><span data-stu-id="e6804-103">Encoder API</span></span>

<span data-ttu-id="e6804-104">Die Encoder-API bietet eine einheitliche Schnittstelle zum Konfigurieren von Software-und Hardware Encodern.</span><span class="sxs-lookup"><span data-stu-id="e6804-104">The Encoder API provides a uniform interface for configuring software and hardware encoders.</span></span> <span data-ttu-id="e6804-105">Anwendungen können die Encoder-API verwenden, um einen Encoder zu konfigurieren und die Konfigurationseinstellungen zu speichern.</span><span class="sxs-lookup"><span data-stu-id="e6804-105">Applications can use the Encoder API to configure an encoder and to store the configuration settings.</span></span> <span data-ttu-id="e6804-106">Encoder-Anbieter können die Encoder-API verwenden, um die Funktionen eines Encoders verfügbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="e6804-106">Encoder vendors can use the Encoder API to expose the capabilities of an encoder.</span></span> <span data-ttu-id="e6804-107">Obwohl die Encoder-API primär für Encoder entwickelt wurde, ist sie allgemein ausreichend, dass Decoder Sie auch unterstützen können.</span><span class="sxs-lookup"><span data-stu-id="e6804-107">Although the Encoder API is designed primarily for encoders, it is general enough that decoders can support it as well.</span></span>

<span data-ttu-id="e6804-108">Die Encoder-API wird für Anwendungen über die [**icodecapi**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) -Schnittstelle verfügbar gemacht, die durch den Encoder-Filter verfügbar gemacht wird.</span><span class="sxs-lookup"><span data-stu-id="e6804-108">The Encoder API is exposed to applications through the [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) interface, which is exposed by the encoder filter.</span></span> <span data-ttu-id="e6804-109">Der Encoder-Filter kann ein nativer DirectShow-Filter, ein Hardware Encoder oder ein DirectX Media Object (DMO) sein.</span><span class="sxs-lookup"><span data-stu-id="e6804-109">The encoder filter may be a native DirectShow filter, a hardware encoder, or a DirectX Media Object (DMO).</span></span>

-   <span data-ttu-id="e6804-110">Software Filter: ein Encoder, der als nativer DirectShow-Filter implementiert ist, sollte [**icodecapi**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) direkt verfügbar machen.</span><span class="sxs-lookup"><span data-stu-id="e6804-110">Software filters: An encoder that is implemented as a native DirectShow filter should expose the [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) directly.</span></span>
-   <span data-ttu-id="e6804-111">Hardware Encoder: das Codierungs Gerät wird durch einen oder mehrere AVStream-Mini Treiber bereitgestellt, die im Benutzermodus durch ksproxy dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="e6804-111">Hardware encoders: The encoding device is exposed through one or more AVStream minidrivers, which are represented in user mode by KSProxy.</span></span> <span data-ttu-id="e6804-112">Ksproxy übersetzt [**icodecapi**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) -Methodenaufrufe in KS-Eigenschaften Sätze.</span><span class="sxs-lookup"><span data-stu-id="e6804-112">KSProxy translates [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) method calls into KS property sets.</span></span> <span data-ttu-id="e6804-113">Weitere Informationen finden Sie in der DDK-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="e6804-113">For more information, see the DDK documentation.</span></span>
-   <span data-ttu-id="e6804-114">DMOS: der DMO sollte die [**icodecapi**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) -Schnittstelle verfügbar machen.</span><span class="sxs-lookup"><span data-stu-id="e6804-114">DMOs: The DMO should expose the [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) interface.</span></span> <span data-ttu-id="e6804-115">DirectShow-Anwendungen können den DMO-Wrapper Filter Abfragen, der die Schnittstelle durch aggregierten DMO verfügbar macht.</span><span class="sxs-lookup"><span data-stu-id="e6804-115">DirectShow applications can query the DMO Wrapper filter, which exposes the interface by aggregating the DMO.</span></span> <span data-ttu-id="e6804-116">Anwendungen, die nicht auf DirectShow basieren, können den DMO direkt abfragen.</span><span class="sxs-lookup"><span data-stu-id="e6804-116">Applications not based on DirectShow can query the DMO directly.</span></span>

### <a name="encoder-capabilties"></a><span data-ttu-id="e6804-117">Codierer</span><span class="sxs-lookup"><span data-stu-id="e6804-117">Encoder Capabilties</span></span>

<span data-ttu-id="e6804-118">Ein Encoder kann eine Liste der Funktionen auf hoher Ebene registrieren, indem er Sie in der Systemregistrierung speichert.</span><span class="sxs-lookup"><span data-stu-id="e6804-118">An encoder can register a list of high-level capabilities by storing them in the system registry.</span></span> <span data-ttu-id="e6804-119">Jede Funktion wird durch eine GUID identifiziert.</span><span class="sxs-lookup"><span data-stu-id="e6804-119">Each capability is identified by a GUID.</span></span> <span data-ttu-id="e6804-120">Gehen Sie folgendermaßen vor, um die Funktionen eines bestimmten Encoders aufzulisten:</span><span class="sxs-lookup"><span data-stu-id="e6804-120">To enumerate the capabilities of a particular encoder, do the following:</span></span>

1.  <span data-ttu-id="e6804-121">Erstellen Sie den Moniker, der den encoderfilter darstellt.</span><span class="sxs-lookup"><span data-stu-id="e6804-121">Create the moniker that represents the encoder filter.</span></span> <span data-ttu-id="e6804-122">(Weitere Informationen finden [Sie unter Verwenden des Enumerators für System Geräte](using-the-system-device-enumerator.md).)</span><span class="sxs-lookup"><span data-stu-id="e6804-122">(See [Using the System Device Enumerator](using-the-system-device-enumerator.md).)</span></span>
2.  <span data-ttu-id="e6804-123">Fragen Sie den Filter Moniker für die [**igetcapabilitieskey**](/windows/desktop/api/Strmif/nn-strmif-igetcapabilitieskey) -Schnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="e6804-123">Query the filter moniker for the [**IGetCapabilitiesKey**](/windows/desktop/api/Strmif/nn-strmif-igetcapabilitieskey) interface.</span></span>
3.  <span data-ttu-id="e6804-124">Nennen Sie [**igetcapabilitieskey:: getcapabilitieskey**](/windows/desktop/api/Strmif/nf-strmif-igetcapabilitieskey-getcapabilitieskey).</span><span class="sxs-lookup"><span data-stu-id="e6804-124">Call [**IGetCapabilitiesKey::GetCapabilitiesKey**](/windows/desktop/api/Strmif/nf-strmif-igetcapabilitieskey-getcapabilitieskey).</span></span> <span data-ttu-id="e6804-125">Die-Methode gibt ein Handle für den Registrierungsschlüssel zurück, der die Funktionsliste des Filters enthält.</span><span class="sxs-lookup"><span data-stu-id="e6804-125">The method returns a handle to the registry key that contains the filter's capabilities list.</span></span>
4.  <span data-ttu-id="e6804-126">Um die Werte für den zurückgegebenen Schlüssel aufzulisten, können Sie die Funktion " **RegEnumValue** " aufzählen.</span><span class="sxs-lookup"><span data-stu-id="e6804-126">Call the **RegEnumValue** function to enumerate the values for the returned key.</span></span>

<span data-ttu-id="e6804-127">Wenn Sie einen Encoder entwickeln, erstellen Sie die Registrierungseinträge für die Funktionen, wenn der Filter registriert wird.</span><span class="sxs-lookup"><span data-stu-id="e6804-127">If you are devloping an encoder, create the registry entries for the capabilities when the filter is registered.</span></span> <span data-ttu-id="e6804-128">Erstellen Sie bei Software Filtern einen Schlüssel mit dem Namen " **Funktionen** ", der sich neben den Schlüsseln " **FilterData** " und " **FriendlyName** " befindet.</span><span class="sxs-lookup"><span data-stu-id="e6804-128">For software filters, create a key named **Capabilities** that is adjacent to the **FilterData** and **FriendlyName** keys.</span></span> <span data-ttu-id="e6804-129">Normalerweise würden Sie diese Informationen nach dem Aufrufen von [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) hinzufügen, um die Standardfilter Daten zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="e6804-129">Typically, you would add this information after calling [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) to register the standard filter data.</span></span> <span data-ttu-id="e6804-130">Weitere Informationen finden Sie unter Vorgehens [Weise beim Registrieren von DirectShow-Filtern](how-to-register-directshow-filters.md).</span><span class="sxs-lookup"><span data-stu-id="e6804-130">For more information, see [How to Register DirectShow Filters](how-to-register-directshow-filters.md).</span></span> <span data-ttu-id="e6804-131">Alternativ können Sie einen **capabilitieslocation** -Schlüssel erstellen, der eine Zeichenfolge enthält **, die den** Speicherort des Funktions Schlüssels in der Registrierung enthält.</span><span class="sxs-lookup"><span data-stu-id="e6804-131">Alternatively, you can create a **CapabilitiesLocation** key that contains a string giving the location of the **Capabilities** key in the registry.</span></span> <span data-ttu-id="e6804-132">Die Zeichenfolge sollte mit "HKLM \\ ", "HKCR \\ " oder "HKCU" beginnen, \\ um die Registrierungs Unterstruktur anzugeben.</span><span class="sxs-lookup"><span data-stu-id="e6804-132">The string should start with "HKLM\\", "HKCR\\", or "HKCU\\" to indicate the registry subtree.</span></span> <span data-ttu-id="e6804-133">Bei Plug & Play Geräten sollten die Setup Dateien des Treibers einen Funktions **Schlüssel erstellen** , der an den Schlüssel " **FriendlyName** " des Filters angrenzt, oder Sie können einen **capabilitieslocation** -Schlüssel verwenden, wie für Softwarefilter beschrieben.</span><span class="sxs-lookup"><span data-stu-id="e6804-133">For Plug and Play devices, the driver's setup files should create a **Capabilities** key adjacent to the filter's **FriendlyName** key, or it can use a **CapabilitiesLocation** key as described for software filters.</span></span>

<span data-ttu-id="e6804-134">Nachdem **Sie den Funktions** Schlüssel erstellt haben, erstellen Sie einen Wert für jede Funktions-GUID.</span><span class="sxs-lookup"><span data-stu-id="e6804-134">Once you have created the **Capabilities** key, create a value for each capability GUID.</span></span> <span data-ttu-id="e6804-135">Der Name des Werts muss die Zeichen folgen Form der GUID im Format sein `{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}` .</span><span class="sxs-lookup"><span data-stu-id="e6804-135">The name of the value should be the string form of the GUID, in the form `{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}`.</span></span> <span data-ttu-id="e6804-136">Jeder Werttyp muss einer der folgenden sein:</span><span class="sxs-lookup"><span data-stu-id="e6804-136">Each value type should be one of the following:</span></span>

-   <span data-ttu-id="e6804-137">Einzelner numerischer Wert.</span><span class="sxs-lookup"><span data-stu-id="e6804-137">Single numerical value.</span></span> <span data-ttu-id="e6804-138">Verwenden Sie einen **DWORD** -Wert.</span><span class="sxs-lookup"><span data-stu-id="e6804-138">Use a **DWORD** value.</span></span>
-   <span data-ttu-id="e6804-139">GUID.</span><span class="sxs-lookup"><span data-stu-id="e6804-139">GUID.</span></span> <span data-ttu-id="e6804-140">Verwenden Sie die Zeichen folgen Form der GUID.</span><span class="sxs-lookup"><span data-stu-id="e6804-140">Use the string form of the GUID.</span></span>
-   <span data-ttu-id="e6804-141">Numerische Paare.</span><span class="sxs-lookup"><span data-stu-id="e6804-141">Numeric pairs.</span></span> <span data-ttu-id="e6804-142">Verwenden Sie eine Zeichenfolge im Format "a, b", um Wertepaare darzustellen, z. b. Breite und Höhe, oder Zähler und Nenner für Bruchteile.</span><span class="sxs-lookup"><span data-stu-id="e6804-142">Use a string with the form "a,b" to represent pairs of values, such as width and height, or numerator and denominator for fractions.</span></span>
-   <span data-ttu-id="e6804-143">Arrays von-Werten.</span><span class="sxs-lookup"><span data-stu-id="e6804-143">Arrays of values.</span></span> <span data-ttu-id="e6804-144">Verwenden Sie mehrere Zeichen folgen (**reg \_ SZ \_ Multi**), um mehr als einen Wert darzustellen.</span><span class="sxs-lookup"><span data-stu-id="e6804-144">Use multi-strings (**REG\_SZ\_MULTI**) to represent more than one value.</span></span>

<span data-ttu-id="e6804-145">Das folgende Beispiel zeigt das Registrierungs Layout für einen Softwarefilter:</span><span class="sxs-lookup"><span data-stu-id="e6804-145">The following example shows the registry layout for a software filter:</span></span>


```C++
\HKCR\CLSID\Filter Category\Instance\Filter CLSID\Capabilities\
    
Values: 
    
    guid1: 1234 (REG_DWORD)   
    
    guid2: "{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}" (REG_SZ)
    
    guid3: "2","4","6" (REG_SZ_MULTI)
    
    guid4: "720,480" (REG_SZ) 
```



### <a name="encoder-profiles"></a><span data-ttu-id="e6804-146">Codierprofile</span><span class="sxs-lookup"><span data-stu-id="e6804-146">Encoder Profiles</span></span>

<span data-ttu-id="e6804-147">Bei einem *Codierungs Profil* handelt es sich um eine Liste fester Konfigurationseinstellungen, die zur Laufzeit auf einen Encoder angewendet werden können.</span><span class="sxs-lookup"><span data-stu-id="e6804-147">An *encoder profile* is a fixed list of configuration settings that can be applied to an encoder at run time.</span></span> <span data-ttu-id="e6804-148">Profile sind unabhängig vom Encoder. eine Anwendung kann einen Encoder auswählen und dann ein Profil auswählen und die Profileinstellungen auf den Encoder anwenden.</span><span class="sxs-lookup"><span data-stu-id="e6804-148">Profiles are independent of the encoder; an application can select an encoder, then select a profile and apply the profile settings to the encoder.</span></span> <span data-ttu-id="e6804-149">Profile werden anhand der GUID identifiziert und sollten an folgendem Speicherort in der Registrierung gespeichert werden:</span><span class="sxs-lookup"><span data-stu-id="e6804-149">Profiles are identified by GUID and should be stored in the following location in the registry:</span></span>


```C++
\HKLM\Software\Microsoft\EncoderProfiles\Profile GUID\
```



<span data-ttu-id="e6804-150">*Profil-GUID*</span><span class="sxs-lookup"><span data-stu-id="e6804-150">where *Profile GUID*</span></span>

<span data-ttu-id="e6804-151">die Zeichen folgen Form der GUID, die das Profil identifiziert.</span><span class="sxs-lookup"><span data-stu-id="e6804-151">is the string form of the GUID that identifies the profile.</span></span> <span data-ttu-id="e6804-152">Erstellen Sie Werte für jede Einstellung.</span><span class="sxs-lookup"><span data-stu-id="e6804-152">Create values for each setting.</span></span> <span data-ttu-id="e6804-153">Erstellen Sie außerdem einen Zeichen folgen Wert mit dem Namen "FriendlyName", dessen Daten das Profil identifizieren (z. b. "lowbandwidthvideo").</span><span class="sxs-lookup"><span data-stu-id="e6804-153">Also create a string value named "FriendlyName" whose data identifies the profile (such as "LowBandwidthVideo").</span></span>

## <a name="related-topics"></a><span data-ttu-id="e6804-154">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e6804-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e6804-155">Encoder-und decoderentwicklung</span><span class="sxs-lookup"><span data-stu-id="e6804-155">Encoder and Decoder Development</span></span>](encoder-and-decoder-development.md)
</dt> </dl>

 

 



