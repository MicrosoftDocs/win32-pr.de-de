---
title: Implementieren eines benutzerdefinierten audioendpunkt-Enumerators
description: Ab Windows Server 2008 R2 können Sie einen benutzerdefinierten remoteaudioendpunkt-Enumerator als Teil eines Remotedesktop Protokoll Anbieters implementieren.
ms.assetid: 684bd62e-1e28-4330-a3c5-6bce684d652d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 435ab2a572169f20a7f8f9db194449be5361e409
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/08/2020
ms.locfileid: "106340540"
---
# <a name="implementing-a-custom-audio-endpoint-enumerator"></a><span data-ttu-id="6be10-103">Implementieren eines benutzerdefinierten audioendpunkt-Enumerators</span><span class="sxs-lookup"><span data-stu-id="6be10-103">Implementing a Custom Audio Endpoint Enumerator</span></span>

<span data-ttu-id="6be10-104">Ab Windows Server 2008 R2 können Sie einen benutzerdefinierten remoteaudioendpunkt-Enumerator als Teil eines Remotedesktop Protokoll Anbieters implementieren.</span><span class="sxs-lookup"><span data-stu-id="6be10-104">Beginning with Windows Server 2008 R2, you can implement a custom remote audio endpoint enumerator as part of a Remote Desktop protocol provider.</span></span> <span data-ttu-id="6be10-105">Ein Remotedesktop-Protokoll Anbieter kann einen benutzerdefinierten audioendpunktenumerator zum Abrufen einer Auflistung von audioendpunkten verwenden, die über einen bestimmten Satz von Funktionen verfügen.</span><span class="sxs-lookup"><span data-stu-id="6be10-105">A Remote Desktop protocol provider can use a custom audio endpoint enumerator to retrieve a collection of audio endpoints that have a specific set of capabilities.</span></span>

<span data-ttu-id="6be10-106">**So implementieren Sie einen benutzerdefinierten remoteaudioendpunkt-Enumerator**</span><span class="sxs-lookup"><span data-stu-id="6be10-106">**To implement a custom remote audio endpoint enumerator**</span></span>

1.  <span data-ttu-id="6be10-107">Die benutzerdefinierte Endpunkt-enumeratorlösung sollte vier Haupttypen von Objekten implementieren: Geräte Enumeratorobjekte, Geräte Sammlungsobjekte, Geräte Objekte und Eigenschaften Speicher Objekte.</span><span class="sxs-lookup"><span data-stu-id="6be10-107">Your custom endpoint enumerator solution should implement four main types of objects: device enumerator objects, device collection objects, device objects, and property store objects.</span></span>

    

    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="6be10-108">Objekttyp</span><span class="sxs-lookup"><span data-stu-id="6be10-108">Object type</span></span></th>
    <th><span data-ttu-id="6be10-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6be10-109">Description</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="6be10-110">Geräte-Enumeratorobjekt</span><span class="sxs-lookup"><span data-stu-id="6be10-110">Device enumerator object</span></span><br/></td>
    <td><span data-ttu-id="6be10-111">Ein geräteenumeratorobjekt stellt die Endpunkt-enumeratorfunktion bereit.</span><span class="sxs-lookup"><span data-stu-id="6be10-111">A device enumerator object provides the endpoint enumerator functionality.</span></span> <span data-ttu-id="6be10-112">Es macht Methoden verfügbar, die einen Standard Endpunkt und angegebene Auflistungen von Endpunkten zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="6be10-112">It exposes methods that return a default endpoint and specified collections of endpoints.</span></span> <span data-ttu-id="6be10-113">Abhängig von den angegebenen Kriterien kann der Enumerator z. b. Kommunikations Endpunkte, Wiedergabe Endpunkte oder Aufzeichnungs Endpunkte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="6be10-113">For example, depending on the criteria specified, the enumerator can return communication endpoints, playback endpoints, or capture endpoints.</span></span> <span data-ttu-id="6be10-114">Das geräteenumeratorobjekt muss die <a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator"><strong>immdeviceenumerator</strong></a> -Schnittstelle implementieren.</span><span class="sxs-lookup"><span data-stu-id="6be10-114">The device enumerator object must implement the <a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator"><strong>IMMDeviceEnumerator</strong></a> interface.</span></span><br/></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="6be10-115">Geräte Sammlungsobjekt</span><span class="sxs-lookup"><span data-stu-id="6be10-115">Device collection object</span></span><br/></td>
    <td><span data-ttu-id="6be10-116">Ein Geräte Sammlungsobjekt stellt eine Sammlung von Audiogeräten dar.</span><span class="sxs-lookup"><span data-stu-id="6be10-116">A device collection object represents a collection of audio devices.</span></span> <span data-ttu-id="6be10-117">Es muss die <a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdevicecollection"><strong>immdebug</strong></a> -Schnittstelle implementieren.</span><span class="sxs-lookup"><span data-stu-id="6be10-117">It must implement the <a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdevicecollection"><strong>IMMDeviceCollection</strong></a> interface.</span></span><br/></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="6be10-118">Geräteobjekt</span><span class="sxs-lookup"><span data-stu-id="6be10-118">Device object</span></span><br/></td>
    <td><span data-ttu-id="6be10-119">Ein Geräte Objekt stellt ein bestimmtes Audiogerät dar.</span><span class="sxs-lookup"><span data-stu-id="6be10-119">A device object represents a particular audio device.</span></span> <span data-ttu-id="6be10-120">Sie ermöglicht den Zugriff auf den Eigenschaften Speicher des Audiogeräts und macht die auf dem Gerät verfügbaren Audiowiedergabe-und Erfassungs Schnittstellen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6be10-120">It provides access to the audio device's property store and exposes the audio playback and capture interfaces available on the device.</span></span> <span data-ttu-id="6be10-121">Das Device-Objekt muss die <a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdevice"><strong>immdevice</strong></a> -und die <a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immendpoint"><strong>immendpoint</strong></a> -Schnittstelle implementieren.</span><span class="sxs-lookup"><span data-stu-id="6be10-121">The device object must implement the <a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdevice"><strong>IMMDevice</strong></a> and <a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immendpoint"><strong>IMMEndpoint</strong></a> interfaces.</span></span><br/></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="6be10-122">Eigenschaften Speicher Objekt</span><span class="sxs-lookup"><span data-stu-id="6be10-122">Property store object</span></span><br/></td>
    <td><span data-ttu-id="6be10-123">Ein Eigenschaften Speicher Objekt macht die einem Audiogerät zugeordneten Eigenschaften verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6be10-123">A property store object exposes the properties associated with an audio device.</span></span> <span data-ttu-id="6be10-124">Einige dieser Eigenschaften werden vom System verwendet, aber Anwendungen können auch beliebige Eigenschaften mit dem audioendpunkt speichern.</span><span class="sxs-lookup"><span data-stu-id="6be10-124">Some of these properties are used by the system, but applications can store arbitrary properties with the audio endpoint as well.</span></span><br/> <span data-ttu-id="6be10-125">Alle Audiogeräte verfügen über die folgenden drei Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="6be10-125">All audio devices have the following three properties:</span></span><br/>
    <ul>
    <li><span data-ttu-id="6be10-126"><a href="/windows/desktop/CoreAudio/pkey-deviceinterface-friendlyname"><strong>PKEY_DeviceInterface_FriendlyName</strong></a></span><span class="sxs-lookup"><span data-stu-id="6be10-126"><a href="/windows/desktop/CoreAudio/pkey-deviceinterface-friendlyname"><strong>PKEY_DeviceInterface_FriendlyName</strong></a></span></span></li>
    <li><span data-ttu-id="6be10-127"><a href="/windows/desktop/CoreAudio/pkey-device-devicedesc"><strong>PKEY_Device_DeviceDesc</strong></a></span><span class="sxs-lookup"><span data-stu-id="6be10-127"><a href="/windows/desktop/CoreAudio/pkey-device-devicedesc"><strong>PKEY_Device_DeviceDesc</strong></a></span></span></li>
    <li><span data-ttu-id="6be10-128"><a href="/windows/desktop/CoreAudio/pkey-device-friendlyname"><strong>PKEY_Device_FriendlyName</strong></a></span><span class="sxs-lookup"><span data-stu-id="6be10-128"><a href="/windows/desktop/CoreAudio/pkey-device-friendlyname"><strong>PKEY_Device_FriendlyName</strong></a></span></span></li>
    </ul>
<span data-ttu-id="6be10-129">Das Eigenschaften Speicher Objekt muss die <a href="/windows/win32/api/propsys/nn-propsys-ipropertystore">IPropertyStore</a> -Schnittstelle implementieren.</span><span class="sxs-lookup"><span data-stu-id="6be10-129">The property store object must implement the <a href="/windows/win32/api/propsys/nn-propsys-ipropertystore">IPropertyStore</a> interface.</span></span><br/></td>
    </tr>
    </tbody>
    </table>

    

     

2.  <span data-ttu-id="6be10-130">Der benutzerdefinierte Endpunkt Enumerator muss in einer DLL implementiert werden, die in das Audiosystem und andere Anwendungen geladen werden kann.</span><span class="sxs-lookup"><span data-stu-id="6be10-130">The custom endpoint enumerator must be implemented in a DLL that can be loaded into the audio system and other applications.</span></span> <span data-ttu-id="6be10-131">Die dll muss signiert werden, damit Sie von sicheren Prozessen geladen werden kann.</span><span class="sxs-lookup"><span data-stu-id="6be10-131">The DLL must be signed so that secure processes can load it.</span></span> <span data-ttu-id="6be10-132">Die dll muss die [**gettsaudioendpointenumeratorforsession**](gettsaudioendpointenumeratorforsession.md) -Funktion implementieren und exportieren, die als Einstiegspunkt für den benutzerdefinierten Endpunkt Enumerator fungiert.</span><span class="sxs-lookup"><span data-stu-id="6be10-132">The DLL must implement and export the [**GetTSAudioEndpointEnumeratorForSession**](gettsaudioendpointenumeratorforsession.md) function, which acts as an entry point to the custom endpoint enumerator.</span></span>

<span data-ttu-id="6be10-133">Der Remotedesktopdienste-Dienst ruft die [**queryproperty**](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-queryproperty) -Methode auf und legt den *QueryType* -Parameter auf die **WTS- \_ Abfrage \_ audioenum- \_ dll** fest, um den Namen des Enumeratorobjekts abzurufen.</span><span class="sxs-lookup"><span data-stu-id="6be10-133">The Remote Desktop Services service calls the [**QueryProperty**](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-queryproperty) method and sets the *QueryType* parameter to **WTS\_QUERY\_AUDIOENUM\_DLL** to retrieve the name of the enumerator object.</span></span>

<span data-ttu-id="6be10-134">Benutzerdefinierte Enumeratorobjekte verwenden com-ähnliche Schnittstellen und einen com-ähnlichen Verweis Zählmechanismus, Sie sind jedoch keine echten com-Objekte.</span><span class="sxs-lookup"><span data-stu-id="6be10-134">Custom enumerator objects use COM-like interfaces and a COM-like reference counting mechanism, but they are not true COM objects.</span></span> <span data-ttu-id="6be10-135">Der benutzerdefinierte Endpunkt Enumerator muss mit älteren Audioschnittstellen arbeiten können, die von Anwendungen verwendet werden, die com nicht unterstützen.</span><span class="sxs-lookup"><span data-stu-id="6be10-135">The custom endpoint enumerator must have the ability to work with legacy audio interfaces used by applications that do not support COM.</span></span> <span data-ttu-id="6be10-136">Aus diesem Grund darf sich der benutzerdefinierte Endpunkt-Enumerator nicht auf den Verwaltungsmechanismus des Lebenszyklus von com verlassen.</span><span class="sxs-lookup"><span data-stu-id="6be10-136">For this reason, the custom endpoint enumerator must not rely on COM's life cycle management mechanism.</span></span> <span data-ttu-id="6be10-137">Consumer Ihres audioendpunktenumerators, wie z. b. MMDevAPI.dll, laden die benutzerdefinierte Endpunkt-enumeratordll, wenn Sie von Benutzer Anwendungen benötigt wird, und entladen den Enumerator nicht, während der Enumerator einen Verweis auf ein Geräte Enumeratorobjekt, ein Geräte Auflistungs Objekt, ein Geräte Objekt oder ein Eigenschafts Speicher Objekt enthält.</span><span class="sxs-lookup"><span data-stu-id="6be10-137">Consumers of your audio endpoint enumerator, such as MMDevAPI.dll, load the custom endpoint enumerator DLL when required by user applications, and they will not unload the enumerator while the enumerator holds a reference to a device enumerator object, device collection object, device object, or property store object.</span></span> <span data-ttu-id="6be10-138">Es ist jedoch nicht möglich, dass diese Consumer Verweise auf andere Typen von Objekten nachverfolgen, die im Besitz des benutzerdefinierten Endpunkt Enumerators sind.</span><span class="sxs-lookup"><span data-stu-id="6be10-138">It is not possible, however, for these consumers to track references to other types of objects owned by the custom endpoint enumerator.</span></span> <span data-ttu-id="6be10-139">Dementsprechend wird empfohlen, dass der benutzerdefinierte Endpunkt Enumerator keine Objekte erstellt, die diese vier Objekttypen überstehen könnten.</span><span class="sxs-lookup"><span data-stu-id="6be10-139">Accordingly, we recommend that your custom endpoint enumerator not create any objects that could outlive these four types of objects.</span></span>

## <a name="to-implement-a-custom-audio-endpoint"></a><span data-ttu-id="6be10-140">So implementieren Sie einen benutzerdefinierten audioendpunkt</span><span class="sxs-lookup"><span data-stu-id="6be10-140">To implement a custom audio endpoint</span></span>

<span data-ttu-id="6be10-141">Um einen benutzerdefinierten audiogeräteenumerator zu implementieren, müssen Sie einen benutzerdefinierten audioendpunkt implementieren.</span><span class="sxs-lookup"><span data-stu-id="6be10-141">To implement a custom audio device enumerator, you must implement a custom audio endpoint.</span></span> <span data-ttu-id="6be10-142">Die Verknüpfung Ihrer benutzerdefinierten Audiogeräte erfolgt mithilfe der folgenden beiden-Anweisungen:</span><span class="sxs-lookup"><span data-stu-id="6be10-142">The way that your custom audio devices are linked is by using the following two statements:</span></span>

-   `IMMDevice::Activate(IAudioOutputEndpointRT)`
-   `IMMDevice::Activate(IAudioInputEndpointRT)`

<span data-ttu-id="6be10-143">Es ist nicht zu erwarten, dass Sie die vollständige Liste der [**immdevice:: Aktivierungs**](/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-immdevice-activate) -Schnittstellen in Ihrem benutzerdefinierten Audiogeräte-Enumerator implementieren.</span><span class="sxs-lookup"><span data-stu-id="6be10-143">We do not expect you to implement the full list of [**IMMDevice::Activate**](/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-immdevice-activate) interfaces in your custom audio device enumerator.</span></span> <span data-ttu-id="6be10-144">Stattdessen sollten Sie [**iaudiooutputendpointrt**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudiooutputendpointrt) und [**iaudioinputendpointrt**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioinputendpointrt)implementieren.</span><span class="sxs-lookup"><span data-stu-id="6be10-144">Instead, you should implement [**IAudioOutputEndpointRT**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudiooutputendpointrt) and [**IAudioInputEndpointRT**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioinputendpointrt).</span></span> <span data-ttu-id="6be10-145">Optional können Sie einige weitere implementieren, z. b. [**iaudioendpointvolume**](/windows/desktop/api/endpointvolume/nn-endpointvolume-iaudioendpointvolume).</span><span class="sxs-lookup"><span data-stu-id="6be10-145">You can optionally implement a few more, such as [**IAudioEndpointVolume**](/windows/desktop/api/endpointvolume/nn-endpointvolume-iaudioendpointvolume).</span></span> <span data-ttu-id="6be10-146">Für jede Schnittstelle, die Sie nicht implementieren, sollten Sie **E \_ nointerface** zurückgeben (Sie müssen diesen spezifischen Fehlercode verwenden).</span><span class="sxs-lookup"><span data-stu-id="6be10-146">For any interface you do not implement, you should return **E\_NOINTERFACE** (you must use this specific failure code).</span></span> <span data-ttu-id="6be10-147">Windows greift dann auf eine Aktien Implementierung der-Schnittstelle zurück (z. b. [**IAudioClient2**](/windows/desktop/api/audioclient/nn-audioclient-iaudioclient2)).</span><span class="sxs-lookup"><span data-stu-id="6be10-147">Windows will then fall back to a stock implementation of the interface (for example, [**IAudioClient2**](/windows/desktop/api/audioclient/nn-audioclient-iaudioclient2)).</span></span>

<span data-ttu-id="6be10-148">Eine weitere Referenz Dokumentation zum Implementieren und Registrieren von audioendpunkten finden Sie unter [**iaudioinputendpointrt**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioinputendpointrt).</span><span class="sxs-lookup"><span data-stu-id="6be10-148">For additional reference documentation about how to implement and register audio endpoints, see [**IAudioInputEndpointRT**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioinputendpointrt).</span></span> <span data-ttu-id="6be10-149">Ein Diagramm, das die Funktionsweise von WASAPI zeigt, finden Sie unter [benutzermodusaudiokomponenten](/windows/desktop/CoreAudio/user-mode-audio-components).</span><span class="sxs-lookup"><span data-stu-id="6be10-149">For a diagram that shows how WASAPI works, see [User-Mode Audio Components](/windows/desktop/CoreAudio/user-mode-audio-components).</span></span> <span data-ttu-id="6be10-150">Beachten Sie, dass alle Benutzermodus-Audiodaten ab Windows Server 2008 neu sind.</span><span class="sxs-lookup"><span data-stu-id="6be10-150">Note that all of user-mode audio is new beginning with Windows Server 2008.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6be10-151">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6be10-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6be10-152">Erstellen eines Remotedesktopprotokoll Anbieters</span><span class="sxs-lookup"><span data-stu-id="6be10-152">Creating a Remote Desktop Protocol Provider</span></span>](creating-a-custom-remote-protocol.md)
</dt> <dt>

[<span data-ttu-id="6be10-153">**Gettsaudioendpointenreeratorforsession**</span><span class="sxs-lookup"><span data-stu-id="6be10-153">**GetTSAudioEndpointEnumeratorForSession**</span></span>](gettsaudioendpointenumeratorforsession.md)
</dt> <dt>

[<span data-ttu-id="6be10-154">**Immdevice**</span><span class="sxs-lookup"><span data-stu-id="6be10-154">**IMMDevice**</span></span>](/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdevice)
</dt> <dt>

[<span data-ttu-id="6be10-155">**Immde vicecollection**</span><span class="sxs-lookup"><span data-stu-id="6be10-155">**IMMDeviceCollection**</span></span>](/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdevicecollection)
</dt> <dt>

[<span data-ttu-id="6be10-156">**Immdeviceenumerator**</span><span class="sxs-lookup"><span data-stu-id="6be10-156">**IMMDeviceEnumerator**</span></span>](/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator)
</dt> <dt>

[<span data-ttu-id="6be10-157">**Immendpoint**</span><span class="sxs-lookup"><span data-stu-id="6be10-157">**IMMEndpoint**</span></span>](/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immendpoint)
</dt> <dt>

[<span data-ttu-id="6be10-158">IPropertyStore</span><span class="sxs-lookup"><span data-stu-id="6be10-158">IPropertyStore</span></span>](/windows/win32/api/propsys/nn-propsys-ipropertystore)
</dt> </dl>