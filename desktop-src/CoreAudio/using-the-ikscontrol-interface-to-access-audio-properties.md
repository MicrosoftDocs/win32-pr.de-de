---
description: Verwenden der IKsControl-Schnittstelle für den Zugriff auf Audioeigenschaften
ms.assetid: 72bf9164-96c6-4543-b858-19480b032fdb
title: Verwenden der IKsControl-Schnittstelle für den Zugriff auf Audioeigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b763b874730981907d61ed7d4d2f46f4a9b053705b2747064c2505b9c5e90b14
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088224"
---
# <a name="using-the-ikscontrol-interface-to-access-audio-properties"></a>Verwenden der IKsControl-Schnittstelle für den Zugriff auf Audioeigenschaften

In seltenen Fällen muss eine spezialisierte Audioanwendung möglicherweise die [**IKsControl-Schnittstelle**](/windows-hardware/drivers/ddi/ksproxy/nn-ksproxy-ikscontrol) verwenden, um auf bestimmte Hardwarefunktionen eines Audioadapters zuzugreifen, die nicht von der [DeviceTopology-API](devicetopology-api.md) oder der [MMDevice-API](mmdevice-api.md)verfügbar gemacht werden. Die **IKsControl-Schnittstelle** macht die Eigenschaften, Ereignisse und Methoden von Kernelstreaminggeräten (KS) für Benutzermodusanwendungen verfügbar. Von primärem Interesse für Audioanwendungen sind KS-Eigenschaften. Die **IKsControl-Schnittstelle** kann in Verbindung mit der DeviceTopology-API und der MMDevice-API verwendet werden, um auf die KS-Eigenschaften von Audioadaptern zuzugreifen.

Die [**IKsControl-Schnittstelle**](/windows-hardware/drivers/ddi/ksproxy/nn-ksproxy-ikscontrol) ist in erster Linie für die Verwendung durch Hardwarehersteller vorgesehen, die Systemsteuerungsanwendungen schreiben, um ihre Audiohardware zu verwalten. **IKsControl** ist weniger nützlich für allgemeine Audioanwendungen, die nicht an bestimmte Hardwaregeräte gebunden sind. Der Grund dafür ist, dass Hardwarehersteller häufig proprietäre Mechanismen implementieren, um auf die Audioeigenschaften ihrer Geräte zuzugreifen. Im Gegensatz zur DeviceTopology-API, die hardwarespezifische Treiberanforderungen ausblendet und eine relativ einheitliche Schnittstelle für den Zugriff auf Audioeigenschaften bereitstellt, verwenden Anwendungen **IKsControl,** um direkt mit Treibern zu kommunizieren. Weitere Informationen zu **IKsControl** finden Sie in der Windows DDK-Dokumentation.

Wie unter [Gerätetopologien](device-topologies.md)erläutert, kann eine Untereinheit in der Topologie eines Adaptergeräts eine oder mehrere der funktionsspezifischen Steuerungsschnittstellen unterstützen, die in der linken Spalte der folgenden Tabelle angezeigt werden. Jeder Eintrag in der rechten Spalte der Tabelle ist die KS-Eigenschaft, die der Steuerelementschnittstelle auf der linken Seite entspricht. Die Steuerelementschnittstelle ermöglicht den komfortablen Zugriff auf die -Eigenschaft. Die meisten Audiotreiber verwenden KS-Eigenschaften, um die funktionsspezifischen Verarbeitungsfunktionen der Untereinheiten (auch als KS-Knoten bezeichnet) in den Topologien ihrer Audioadapter darzustellen. Weitere Informationen zu KS-Eigenschaften und KS-Knoten finden Sie in der Windows DDK-Dokumentation.



| Steuerungsschnittstelle                                          | KS-Eigenschaft                        |
|------------------------------------------------------------|------------------------------------|
| [**IAudioAutoGainControl**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioautogaincontrol)     | KSPROPERTY \_ AUDIO \_ AGC             |
| [**IAudioBass**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiobass)                           | KSPROPERTY \_ \_ AUDIOBASS            |
| [**IAudioChannelConfig**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiochannelconfig)         | \_KSPROPERTY-AUDIOKANALKONFIGURATION \_ \_ |
| [**IAudioInputSelector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioinputselector)         | KSPROPERTY \_ AUDIO \_ MUX \_ SOURCE     |
| [**IAudioLoudness**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioloudness)                   | KSPROPERTY \_ AUDIO \_ LAUTHEIT        |
| [**IAudioMidrange**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiomidrange)                   | KSPROPERTY \_ AUDIO \_ MID             |
| [**IAudioMute**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiomute)                           | KSPROPERTY \_ AUDIO \_ MUTE            |
| [**IAudioOutputSelector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiooutputselector)       | KSPROPERTY \_ AUDIO \_ DEMUX \_ DEST     |
| [**IAudioPeakMeter**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiopeakmeter)                 | KSPROPERTY \_ AUDIO \_ PEAKMETER       |
| [**IAudioTreble**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiotreble)                       | KSPROPERTY \_ AUDIO \_ TREBLE          |
| [**IAudioVolumeLevel**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiovolumelevel)             | KSPROPERTY \_ AUDIO \_ VOLUMELEVEL     |
| [**IDeviceSpecificProperty**](/windows/desktop/api/Devicetopology/nn-devicetopology-idevicespecificproperty) | KSPROPERTY \_ AUDIO \_ DEV \_ SPECIFIC   |



 

Die Topologien einiger Audioadapter können Untereinheiten mit KS-Eigenschaften enthalten, die in der obigen Tabelle nicht aufgeführt sind. Angenommen, ein Aufruf der [**IPart::GetSubType-Methode**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getsubtype) für eine bestimmte Untereinheit ruft den GUID-Wert KSNODETYPE \_ TONE ab. Diese Untertyp-GUID gibt an, dass die Untereinheit eine oder mehrere der folgenden KS-Eigenschaften unterstützt:

-   KSPROPERTY \_ \_ AUDIOBASS
-   KSPROPERTY \_ AUDIO \_ MID
-   KSPROPERTY \_ AUDIO \_ TREBLE
-   KSPROPERTY \_ AUDIO \_ SOUND \_ BOOST

Auf die ersten drei Eigenschaften in dieser Liste kann über die Steuerelementschnittstellen zugegriffen werden, die in der obigen Tabelle angezeigt werden, aber die KSPROPERTY \_ AUDIO \_ \_ BOOST-Eigenschaft verfügt über keine entsprechende Steuerelementschnittstelle in der DeviceTopology-API. Eine Anwendung kann jedoch die [**IKsControl-Schnittstelle**](/windows-hardware/drivers/ddi/ksproxy/nn-ksproxy-ikscontrol) verwenden, um auf diese Eigenschaft zuzugreifen, wenn die Untereinheit die -Eigenschaft unterstützt.

Die folgenden Schritte sind erforderlich, um auf die KSPROPERTY \_ AUDIO \_ \_ BOOST-Eigenschaft einer Untereinheit des Untertyps KSNODETYPE TONE zuzugreifen: \_

1.  Rufen Sie die [**IConnector::GetDeviceIdConnectedTo-**](/windows/desktop/api/Devicetopology/nf-devicetopology-iconnector-getdeviceidconnectedto) oder [**IDeviceTopology::GetDeviceId-Methode**](/windows/desktop/api/Devicetopology/nf-devicetopology-idevicetopology-getdeviceid) auf, um die Geräte-ID-Zeichenfolge abzurufen, die das Adaptergerät identifiziert. Diese Zeichenfolge ähnelt einer [Endpunkt-ID-Zeichenfolge,](endpoint-id-strings.md)mit der Ausnahme, dass sie ein Adaptergerät anstelle eines Endpunktgeräts identifiziert. Weitere Informationen zum Unterschied zwischen einem Adaptergerät und einem Endpunktgerät finden Sie unter [Audioendpunktgeräte.](audio-endpoint-devices.md)
2.  Rufen Sie die [**IMMDevice-Schnittstelle**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) des Adaptergeräts ab, indem Sie die [**IMMDeviceEnumerator::GetDevice-Methode**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice) mit der Geräte-ID-Zeichenfolge aufrufen. Diese **IMMDevice-Schnittstelle entspricht** der in **IMMDevice-Schnittstelle beschriebenen** Schnittstelle, stellt jedoch ein Adaptergerät anstelle eines Endpunktgeräts dar.
3.  Rufen Sie die [**IKsControl-Schnittstelle**](/windows-hardware/drivers/ddi/ksproxy/nn-ksproxy-ikscontrol) für die Untereinheit ab, indem Sie die [**IMMDevice::Activate-Methode**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) aufrufen, wobei der Parameter *iid* auf **REFIID** IID \_ IKsControl festgelegt ist. Beachten Sie, dass sich die von dieser **Activate-Methode** unterstützten Schnittstellen, die für ein Adaptergerät verwendet werden, von den Schnittstellen unterscheiden, die von der **Activate-Methode** für ein Endpunktgerät unterstützt werden. Insbesondere unterstützt die **Activate-Methode** für ein Adaptergerät **IKsControl.**
4.  Rufen Sie die [**IPart::GetLocalId-Methode**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getlocalid) auf, um die lokale ID der Untereinheit abzurufen.
5.  Erstellen Sie eine KS-Eigenschaftsanforderung. Die für die Anforderung erforderliche KS-Knoten-ID ist in den 16 am wenigsten signifikanten Bits der lokalen ID enthalten, die im vorherigen Schritt abgerufen wurden.
6.  Senden Sie die KS-Eigenschaftsanforderung an den Audiotreiber, indem Sie die [**IKsControl::KsProperty-Methode**](/windows-hardware/drivers/ddi/ksproxy/nf-ksproxy-ikscontrol-ksproperty) aufrufen. Weitere Informationen zu dieser Methode finden Sie in der Windows DDK-Dokumentation.

Im folgenden Codebeispiel wird der Wert der KSPROPERTY \_ AUDIO \_ SOUND \_ BOOST-Eigenschaft aus einer Untereinheit des Untertyps KSNODETYPE \_ TONE abgerufen:


```C++
//-----------------------------------------------------------
// This function calls the IKsControl::Property method to get
// the value of the KSPROPERTY_AUDIO_BASS_BOOST property of
// a subunit. Parameter pPart should point to a part that is
// a subunit with a subtype GUID value of KSNODETYPE_TONE.
//-----------------------------------------------------------
#define PARTID_MASK 0x0000ffff
#define EXIT_ON_ERROR(hres)  \
              if (FAILED(hres)) { goto Exit; }
#define SAFE_RELEASE(punk)  \
              if ((punk) != NULL)  \
                { (punk)->Release(); (punk) = NULL; }

const IID IID_IKsControl = __uuidof(IKsControl);

HRESULT GetBassBoost(IMMDeviceEnumerator *pEnumerator,
                     IPart *pPart, BOOL *pbValue)
{
    HRESULT hr;
    IDeviceTopology *pTopology = NULL;
    IMMDevice *pPnpDevice = NULL;
    IKsControl *pKsControl = NULL;
    LPWSTR pwszDeviceId = NULL;

    if (pEnumerator == NULL || pPart == NULL || pbValue == NULL)
    {
        return E_INVALIDARG;
    }

    // Get the topology object for the adapter device that contains
    // the subunit represented by the IPart interface.
    hr = pPart->GetTopologyObject(&pTopology);
    EXIT_ON_ERROR(hr)

    // Get the device ID string that identifies the adapter device.
    hr = pTopology->GetDeviceId(&pwszDeviceId);
    EXIT_ON_ERROR(hr)

    // Get the IMMDevice interface of the adapter device object.
    hr = pEnumerator->GetDevice(pwszDeviceId, &pPnpDevice);
    EXIT_ON_ERROR(hr)

    // Activate an IKsControl interface on the adapter device object.
    hr = pPnpDevice->Activate(IID_IKsControl, CLSCTX_ALL, NULL, (void**)&pKsControl);
    EXIT_ON_ERROR(hr)

    // Get the local ID of the subunit (contains the KS node ID).
    UINT localId = 0;
    hr = pPart->GetLocalId(&localId);
    EXIT_ON_ERROR(hr)

    KSNODEPROPERTY_AUDIO_CHANNEL ksprop;
    ZeroMemory(&ksprop, sizeof(ksprop));
    ksprop.NodeProperty.Property.Set = KSPROPSETID_Audio;
    ksprop.NodeProperty.Property.Id = KSPROPERTY_AUDIO_BASS_BOOST;
    ksprop.NodeProperty.Property.Flags = KSPROPERTY_TYPE_GET | KSPROPERTY_TYPE_TOPOLOGY;
    ksprop.NodeProperty.NodeId = localId & PARTID_MASK;
    ksprop.Channel = 0;

    // Send the property request.to the device driver.
    BOOL bValue = FALSE;
    ULONG valueSize;
    hr = pKsControl->KsProperty(
                         &ksprop.NodeProperty.Property, sizeof(ksprop),
                         &bValue, sizeof(bValue), &valueSize);
    EXIT_ON_ERROR(hr)

    *pbValue = bValue;

Exit:
    SAFE_RELEASE(pTopology)
    SAFE_RELEASE(pPnpDevice)
    SAFE_RELEASE(pKsControl)
    CoTaskMemFree(pwszDeviceId);
    return hr;
}

```



Im vorherigen Codebeispiel verwendet die GetBassBoost-Funktion die folgenden drei Parameter:

-   `pEnumerator` verweist auf die [**IMMDeviceEnumerator-Schnittstelle**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) eines Audioendpunkt-Enumerators.
-   `pPart` zeigt auf die [**IPart-Schnittstelle**](/windows/desktop/api/Devicetopology/nn-devicetopology-ipart) einer Untereinheit, die über den Untertyp KSNODETYPE \_ TONE verfügt.
-   `pbValue` zeigt auf eine **BOOL-Variable,** in die die Funktion den Eigenschaftswert schreibt.

Ein Programm ruft GetBassBoost erst nach dem Aufruf von [**IPart::GetSubType**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getsubtype) auf und ermittelt, dass der Untertyp der Untereinheit KSNODETYPE \_ TONE ist. Der Eigenschaftswert ist **TRUE,** wenn die Verstärkung aktiviert ist. Der Wert ist **FALSE,** wenn die Verstärkung deaktiviert ist.

Am Anfang der GetBassBoost-Funktion ruft der Aufruf der [**IPart::GetTopologyObject-Methode**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-gettopologyobject) die [**IDeviceTopology-Schnittstelle**](/windows/desktop/api/Devicetopology/nn-devicetopology-idevicetopology) des Adaptergeräts ab, das die KSNODETYPE \_ TONE-Untereinheit enthält. Der [**IDeviceTopology::GetDeviceId-Methodenaufruf**](/windows/desktop/api/Devicetopology/nf-devicetopology-idevicetopology-getdeviceid) ruft die Geräte-ID-Zeichenfolge ab, die das Adaptergerät identifiziert. Der [**IMMDeviceEnumerator::GetDevice-Methodenaufruf**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice) verwendet die Geräte-ID-Zeichenfolge als Eingabeparameter und ruft die [**IMMDevice-Schnittstelle**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) des Adaptergeräts ab. Als Nächstes ruft der [**IMMDevice::Activate-Methodenaufruf**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) die [**IKsControl-Schnittstelle**](/windows-hardware/drivers/ddi/ksproxy/nn-ksproxy-ikscontrol) der Untereinheit ab. Weitere Informationen zur **IKsControl-Schnittstelle** finden Sie in der Windows DDK-Dokumentation.

Als Nächstes wird im vorherigen Codebeispiel eine [**KSNODEPROPERTY \_ AUDIO \_ CHANNEL-Struktur**](/windows-hardware/drivers/ddi/ksmedia/ns-ksmedia-ksnodeproperty_audio_channel) erstellt, die die Eigenschaft "sound-boost" beschreibt. Im Codebeispiel wird ein Zeiger auf die -Struktur an die [**IKsControl::KsProperty-Methode**](/windows-hardware/drivers/ddi/ksproxy/nf-ksproxy-ikscontrol-ksproperty) übergeben, die die Informationen in der -Struktur verwendet, um den Eigenschaftswert abzurufen. Weitere Informationen zur **KSNODEPROPERTY \_ AUDIO \_ CHANNEL-Struktur** und zur **IKsControl::KsProperty-Methode** finden Sie in der Windows DDK-Dokumentation.

Audiohardware weist jedem Kanal in einem Audiostream in der Regel einen separaten Sound-Boost-Zustand zu. Im Prinzip kann die Boost-Verstärkung für einige Kanäle aktiviert und für andere deaktiviert werden. Die [**KSNODEPROPERTY \_ AUDIO \_ CHANNEL-Struktur**](/windows-hardware/drivers/ddi/ksmedia/ns-ksmedia-ksnodeproperty_audio_channel) enthält einen **Channelmember,** der die Kanalnummer angibt. Wenn ein Stream *N* Kanäle enthält, werden die Kanäle von 0 bis *N*– 1 nummeriert. Im vorangehenden Codebeispiel wird nur der Wert der Eigenschaft "wirr-boost" für Kanal 0 (0) abgelangt. Bei dieser Implementierung wird implizit davon ausgegangen, dass die Eigenschaften der Verstärkung für alle Kanäle einheitlich auf denselben Zustand festgelegt sind. Daher reicht es aus, die Eigenschaft "musik-boost" für Kanal 0 zu lesen, um den Wert der Eigenschaft "mess-boost" für den Stream zu bestimmen. Um mit dieser Annahme konsistent zu sein, würde eine entsprechende Funktion zum Festlegen der Eigenschaft "geleer-boost" alle Kanäle auf denselben Wert der Eigenschaft "geleer-boost" festlegen. Dies sind sinnvolle Konventionen, aber nicht alle Hardwareanbieter befolgen sie notwendigerweise. Beispielsweise kann ein Anbieter eine Systemsteuerungsanwendung bereitstellen, die die Verstärkung nur für Kanäle ermöglicht, die Vollbereichslautler steuern. (Ein Full-Range-Lautsprecher kann Sounds über den gesamten Bereich von Dern bis treble wiedergeben.) In diesem Fall stellt der im vorherigen Codebeispiel abgerufene Eigenschaftswert möglicherweise nicht genau den Zustand des Streams dar.

Clients, die die in der obigen Tabelle aufgeführten Steuerelementschnittstellen verwenden, können die [**IPart::RegisterControlChangeCallback-Methode**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-registercontrolchangecallback) aufrufen, um sich für Benachrichtigungen zu registrieren, wenn sich der Wert eines Steuerelementparameters ändert. Beachten Sie, dass die [**IKsControl-Schnittstelle**](/windows-hardware/drivers/ddi/ksproxy/nn-ksproxy-ikscontrol) keine ähnliche Möglichkeit für Clients bietet, sich für Benachrichtigungen zu registrieren, wenn sich ein Eigenschaftswert ändert. Wenn **IKsControl** Eigenschaftenänderungsbenachrichtigungen unterstützt, kann es eine Anwendung informieren, wenn eine andere Anwendung einen Eigenschaftswert geändert hat. Im Gegensatz zu den häufiger verwendeten Steuerelementen, die über [**IPart-Benachrichtigungen**](/windows/desktop/api/Devicetopology/nn-devicetopology-ipart) überwacht werden, sind die von **IKsControl** verwalteten Eigenschaften jedoch in erster Linie für die Verwendung durch Hardwarehersteller vorgesehen, und diese Eigenschaften werden wahrscheinlich nur von Systemsteuerungsanwendungen geändert, die von den Anbietern geschrieben wurden. Wenn eine Anwendung Eigenschaftenänderungen erkennen muss, die von einer anderen Anwendung vorgenommen wurden, kann sie die Änderungen erkennen, indem sie den Eigenschaftswert in regelmäßigen Abständen über **IKsControl** abruft.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Programmierhandbuch](programming-guide.md)
</dt> </dl>

 

 
