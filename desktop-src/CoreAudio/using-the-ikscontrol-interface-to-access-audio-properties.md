---
description: Verwenden der ikscontrol-Schnittstelle für den Zugriff auf Audioeigenschaften
ms.assetid: 72bf9164-96c6-4543-b858-19480b032fdb
title: Verwenden der ikscontrol-Schnittstelle für den Zugriff auf Audioeigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a67639a0e51334da80b7bff88293414a58bb204c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214204"
---
# <a name="using-the-ikscontrol-interface-to-access-audio-properties"></a>Verwenden der ikscontrol-Schnittstelle für den Zugriff auf Audioeigenschaften

In seltenen Fällen muss eine spezialisierte Audioanwendung möglicherweise die " [**ikscontrol**](/windows-hardware/drivers/ddi/ksproxy/nn-ksproxy-ikscontrol) "-Schnittstelle verwenden, um auf bestimmte Hardwarefunktionen eines audioadapters zuzugreifen, die nicht von der [devicetopology-API](devicetopology-api.md) oder der [mmdevice-API](mmdevice-api.md)verfügbar gemacht werden. Die " **ikscontrol** "-Schnittstelle macht die Eigenschaften, Ereignisse und Methoden von Kernel Streaming (ksstreaming)-Geräten für Benutzermodusanwendungen verfügbar. Hauptinteresse an Audioanwendungen sind die Eigenschaften von "". Die " **ikscontrol** "-Schnittstelle kann zusammen mit der devicetopology-API und der mmdevice-API verwendet werden, um auf die Eigenschaften von "die Eigenschaften von audioadaptern" zuzugreifen

Die " [**ikscontrol**](/windows-hardware/drivers/ddi/ksproxy/nn-ksproxy-ikscontrol) "-Schnittstelle ist hauptsächlich für die Verwendung durch Hardwarehersteller vorgesehen, die System Steuerungsanwendungen zum Verwalten Ihrer Audiohardware schreiben. " **Ikscontrol** " ist weniger nützlich für allgemeine Audioanwendungen, die nicht an bestimmte Hardware Geräte gebunden sind. Der Grund hierfür ist, dass Hardware Anbieter für den Zugriff auf die Audioeigenschaften Ihrer Geräte häufig proprietäre Mechanismen implementieren. Anders als bei der devicetopology-API, mit der Hardware spezifische Treiber-quirkselemente ausgeblendet werden und eine relativ einheitliche Schnittstelle für den Zugriff auf Audioeigenschaften bereitgestellt wird, verwenden Anwendungen " **ikscontrol** ", um direkt mit Treibern zu kommunizieren. Weitere Informationen zu " **ikscontrol**" finden Sie in der Windows-DDK-Dokumentation.

Wie in [Device Topologien](device-topologies.md)erläutert, unterstützt eine Untereinheit in der Topologie eines Adapter Geräts möglicherweise eine oder mehrere der Funktions spezifischen Steuerungs Schnittstellen, die in der linken Spalte der folgenden Tabelle angezeigt werden. Jeder Eintrag in der rechten Spalte der Tabelle ist die Eigenschaft "", die der Steuerelement Schnittstelle auf der linken Seite entspricht. Die Steuerelement Schnittstelle bietet bequemen Zugriff auf die-Eigenschaft. Die meisten Audiotreiber verwenden die Eigenschaften von "Eigenschaften", um die Funktions spezifischen Verarbeitungsfunktionen der untergeordneten Einheiten (auch als "-Knoten" bezeichnet) in den Topologien ihrer Audioadapter darzustellen. Weitere Informationen zu den Eigenschaften von "KS" und "KS" finden Sie in der Windows-DDK-Dokumentation.



| Steuerungs Schnittstelle                                          | Eigenschaft "Eigenschaften"                        |
|------------------------------------------------------------|------------------------------------|
| [**Iaudioautogaincontrol**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioautogaincontrol)     | ksproperty \_ \_ audioagc             |
| [**Iaudiobass**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiobass)                           | ksproperty \_ - \_ audiobass            |
| [**Iaudiochannelconfig**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiochannelconfig)         | ksproperty \_ - \_ \_ audiokanalkonfiguration |
| [**Iaudioinputselector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioinputselector)         | ksproperty \_ - \_ audiomux- \_ Quelle     |
| [**Iaudioloudness**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioloudness)                   | ksproperty \_ - \_ audiolaut Stärke        |
| [**Iaudiomidrange**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiomidrange)                   | ksproperty \_ - \_ audiomid             |
| [**Iaudiomute**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiomute)                           | ksproperty \_ - \_ audiostumm schalten            |
| [**Iaudiooutputselector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiooutputselector)       | ksproperty \_ - \_ audiodemux \_ dest     |
| [**Iaudiopeakmeter**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiopeakmeter)                 | ksproperty \_ - \_ audioakmeter       |
| [**Iaudiotreble**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiotreble)                       | ksproperty \_ \_ audiotreble          |
| [**Iaudiovolumelevel**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiovolumelevel)             | ksproperty \_ \_ audiovolumelevel     |
| [**Idevicespecificproperty**](/windows/desktop/api/Devicetopology/nn-devicetopology-idevicespecificproperty) | ksproperty \_ - \_ \_ audioentwicklungspezifischer   |



 

Die Topologien einiger Audioadapter können Untereinheiten enthalten, die über die in der obigen Tabelle nicht aufgelisteten Eigenschaften von "in der vorangehenden Tabelle" verfügen. Nehmen Sie beispielsweise an, dass ein Aufrufen der [**ipart:: getsubtype**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getsubtype) -Methode für eine bestimmte Teil Einheit den GUID-Wert ksnodetype-Ton abruft \_ . Diese Untertyp-GUID gibt an, dass die Untereinheit mindestens eine der folgenden Eigenschaften unterstützt:

-   ksproperty \_ - \_ audiobass
-   ksproperty \_ - \_ audiomid
-   ksproperty \_ \_ audiotreble
-   ksproperty \_ - \_ audiobass- \_ Boost

Der Zugriff auf die ersten drei Eigenschaften in dieser Liste ist über die Steuerelement Schnittstellen möglich, die in der obigen Tabelle angezeigt werden. die Eigenschaft "ksproperty \_ \_ audiobass Boost" verfügt jedoch nicht über die \_ entsprechende Steuerungs Schnittstelle in der devicetopology-API. Allerdings kann eine Anwendung die " [**ikscontrol**](/windows-hardware/drivers/ddi/ksproxy/nn-ksproxy-ikscontrol) "-Schnittstelle verwenden, um auf diese Eigenschaft zuzugreifen, wenn die Untereinheit die-Eigenschaft unterstützt.

Die folgenden Schritte sind erforderlich, um auf die Eigenschaft "ksproperty \_ \_ audiobass Boost" einer \_ Teil Einheit des unter Typs "ksnodetype Tone" zuzugreifen \_ :

1.  Rufen Sie die [**IConnector:: getdeviceidconnectedto**](/windows/desktop/api/Devicetopology/nf-devicetopology-iconnector-getdeviceidconnectedto) -Methode oder die [**idevicetopology:: getdeviceid**](/windows/desktop/api/Devicetopology/nf-devicetopology-idevicetopology-getdeviceid) -Methode auf, um die Geräte-ID-Zeichenfolge zu erhalten, die das Adapter Gerät identifiziert. Diese Zeichenfolge ähnelt einer [Endpunkt-ID-Zeichenfolge](endpoint-id-strings.md), mit der Ausnahme, dass Sie ein Adapter Gerät anstelle eines Endpunkt Geräts identifiziert. Weitere Informationen zu den Unterschieden zwischen einem Adapter Gerät und einem Endpunkt Gerät finden Sie unter [audioendpunktgeräte](audio-endpoint-devices.md).
2.  Rufen Sie die [**immdevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) -Schnittstelle des Adapter Geräts durch Aufrufen der [**immdeviceenumerator:: getdevice**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice) -Methode mit der Geräte-ID-Zeichenfolge ab. Diese **immdevice** -Schnittstelle ist mit der in der **immdevice-Schnitt** Stelle beschriebenen Schnittstelle identisch, stellt jedoch ein Adapter Gerät anstelle eines Endpunkt Geräts dar.
3.  Rufen Sie die " [**ikscontrol**](/windows-hardware/drivers/ddi/ksproxy/nn-ksproxy-ikscontrol) "-Schnittstelle für die untergeordnete Einheit ab, indem Sie die Methode " [**immdevice:: Aktivierungs**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) " mit dem Parameter " *IID* " aufrufen, der auf **refID** \_ IID Beachten Sie, dass sich die von dieser **Aktivierungs** Methode unterstützten Schnittstellen, die für ein Adapter Gerät vorgesehen sind, von den Schnittstellen unterscheiden, die von der **Aktivierungs** Methode für ein Endpunkt Gerät unterstützt werden. Insbesondere unterstützt die **Aktivierungs** Methode für ein Adapter Gerät " **ikscontrol**".
4.  Rufen Sie die [**ipart:: getlocalid-**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getlocalid) Methode auf, um die lokale ID der Untereinheit zu erhalten.
5.  Erstellen Sie eine Anforderung für eine Anforderungs Anforderung. Die für die Anforderung erforderliche ID-Knoten-ID ist in den 16 kleinsten signifikanten Bits der lokalen ID enthalten, die im vorherigen Schritt abgerufen wurden.
6.  Senden Sie die KS-Eigenschaften Anforderung an den Audiotreiber, indem Sie die Methode " [**ikscontrol:: ksproperty**](/windows-hardware/drivers/ddi/ksproxy/nf-ksproxy-ikscontrol-ksproperty) " aufrufen. Weitere Informationen zu dieser Methode finden Sie in der Windows-DDK-Dokumentation.

Im folgenden Codebeispiel wird der Wert der Eigenschaft "ksproperty \_ \_ audiobass \_ Boost" aus einer Teil Einheit des unter Typs "ksnodetype Tone" abgerufen \_ :


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



Im vorangehenden Codebeispiel nimmt die getbassboost-Funktion die folgenden drei Parameter an:

-   `pEnumerator` verweist auf die [**immdeviceenumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) -Schnittstelle eines audioendpunkt-Enumerators.
-   `pPart` verweist auf die [**ipart**](/windows/desktop/api/Devicetopology/nn-devicetopology-ipart) -Schnittstelle einer Teil Einheit, die einen Untertyp des ksnodetype- \_ Tons aufweist.
-   `pbValue` verweist auf eine **boolesche** Variable, in die die-Funktion den Eigenschafts Wert schreibt.

Ein Programm ruft getbassboost erst auf, nachdem es [**ipart:: getsubtype**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getsubtype) aufgerufen hat, und legt fest, dass der Untertyp der untergeordneten Einheit ksnodetype \_ Tone ist. Der Eigenschafts Wert ist **true** , wenn der Bass Boost aktiviert ist. Der Wert ist **false** , wenn der Bass Boost deaktiviert ist.

Am Anfang der getbassboost-Funktion ruft der Aufruf der [**ipart:: gettopologyobject**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-gettopologyobject) -Methode die [**idevicetopology**](/windows/desktop/api/Devicetopology/nn-devicetopology-idevicetopology) -Schnittstelle des Adapter Geräts ab, das die "ksnodetype Tone"- \_ Untereinheit enthält. Der [**idevicetopology:: getdeviceid**](/windows/desktop/api/Devicetopology/nf-devicetopology-idevicetopology-getdeviceid) -Methodenaufruf Ruft die Geräte-ID-Zeichenfolge ab, die das Adapter Gerät identifiziert. Der [**immdeviceenumerator:: getdevice**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice) -Methodenaufrufe nimmt die Geräte-ID-Zeichenfolge als Eingabeparameter an und ruft die [**immdevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) -Schnittstelle des Adapter Geräts ab. Als Nächstes ruft der [**immdevice:: Aktivierungs**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) -Methodenaufrufe die " [**ikscontrol**](/windows-hardware/drivers/ddi/ksproxy/nn-ksproxy-ikscontrol) "-Schnittstelle der Teil Einheit ab. Weitere Informationen zur " **ikscontrol** "-Schnittstelle finden Sie in der Windows-DDK-Dokumentation.

Anschließend wird im vorangehenden Codebeispiel eine [**ksnodeproperty \_ - \_ audiokanalstruktur**](/windows-hardware/drivers/ddi/ksmedia/ns-ksmedia-ksnodeproperty_audio_channel) erstellt, die die Eigenschaft "Bass-Boost" beschreibt. Das Codebeispiel übergibt einen Zeiger an die-Struktur an die Methode " [**ikscontrol:: ksproperty**](/windows-hardware/drivers/ddi/ksproxy/nf-ksproxy-ikscontrol-ksproperty) ", die die Informationen in der-Struktur verwendet, um den Eigenschafts Wert abzurufen. Weitere Informationen zur **ksnodeproperty \_ - \_ audiokanalstruktur** und zur Methode " **ikscontrol:: ksproperty** " finden Sie in der Windows-DDK-Dokumentation.

Audiohardware weist den einzelnen Kanälen in einem Audiostream in der Regel einen separaten Bass-Boost-Zustand zu. Im Prinzip kann die Bass Verstärkung für einige Kanäle aktiviert und für andere Benutzer deaktiviert werden. Die [**ksnodebug Property \_ - \_ audiokanalstruktur**](/windows-hardware/drivers/ddi/ksmedia/ns-ksmedia-ksnodeproperty_audio_channel) enthält einen **kanalmember** , der die Kanalnummer angibt. Wenn ein Stream *N* Kanäle enthält, werden die Kanäle von 0 bis *N*– 1 nummeriert. Im vorangehenden Codebeispiel wird nur der Wert der Eigenschaft "Bass-Boost" für Channel 0 abgerufen. Diese Implementierung geht implizit davon aus, dass die Eigenschaften für das Bass-Boost für alle Kanäle einheitlich auf denselben Zustand festgelegt sind. Daher ist das Lesen der Eigenschaft "Bass-Boost" für Channel 0 ausreichend, um den Wert der Eigenschaft "Bass-Boost" für den Stream zu ermitteln. Damit diese Annahme konsistent ist, würde eine entsprechende Funktion zum Festlegen der Eigenschaft "Bass-Boost" alle Kanäle auf denselben Wert für die Eigenschaft "Bass-Boost" festlegen. Dies sind sinnvolle Konventionen, aber nicht alle Hardware Anbieter befolgen Sie unbedingt. Ein Hersteller könnte z. b. eine System Steuerungsanwendung bereitstellen, die eine Bass Verstärkung nur für Kanäle ermöglicht, die Lautsprecher mit vollständigem Bereich sorgen. (Ein Volltext-Redner ist in der Lage, Klänge über den vollen Bereich von Bass bis Treble zu spielen.) In diesem Fall stellt der Eigenschafts Wert, der im vorangehenden Codebeispiel abgerufen wurde, den Bass-Boost-Zustand des Streams möglicherweise nicht genau dar.

Clients, die die in der obigen Tabelle aufgeführten Steuerungs Schnittstellen verwenden, können die [**ipart:: registercontrolchangecallback**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-registercontrolchangecallback) -Methode aufrufen, um sich für Benachrichtigungen zu registrieren, wenn der Wert eines Steuerelement Parameters geändert wird. Beachten Sie, dass die " [**ikscontrol**](/windows-hardware/drivers/ddi/ksproxy/nn-ksproxy-ikscontrol) "-Schnittstelle keine ähnliche Methode für Clients zur Registrierung für Benachrichtigungen bereitstellt, wenn sich ein Eigenschafts Wert ändert. Wenn " **ikscontrol** " Eigenschaften Änderungs Benachrichtigungen unterstützt hat, könnte eine Anwendung informiert werden, wenn ein Eigenschafts Wert von einer anderen Anwendung geändert wurde. Im Gegensatz zu den am häufigsten verwendeten Steuerelementen, die über [**ipart**](/windows/desktop/api/Devicetopology/nn-devicetopology-ipart) -Benachrichtigungen überwacht werden, sind die von " **ikscontrol** " verwalteten Eigenschaften hauptsächlich für die Verwendung durch Hardwarehersteller gedacht, und diese Eigenschaften werden wahrscheinlich nur von System Steuerungsanwendungen geändert, die von den Anbietern geschrieben wurden. Wenn eine Anwendung von einer anderen Anwendung vorgenommene Eigenschafts Änderungen erkennen muss, kann Sie die Änderungen erkennen, indem Sie den Eigenschafts Wert regelmäßig über " **ikscontrol**" abfragt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Programmierhandbuch](programming-guide.md)
</dt> </dl>

 

 
