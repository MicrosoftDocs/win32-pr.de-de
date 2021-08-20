---
description: Gerätetopologien
ms.assetid: 5ac421e5-74a4-40e8-af6f-a99a05ebc3e0
title: Gerätetopologien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb08221ac157738f8b13ff3dce68d70675b6e94ddc04d99514277d3f1b79b42c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119077618"
---
# <a name="device-topologies"></a>Gerätetopologien

Die [DeviceTopology-API](devicetopology-api.md) ermöglicht Clients die Kontrolle über eine Vielzahl interner Funktionen von Audioadaptern, auf die sie nicht über die [MMDevice-API,](mmdevice-api.md) [WASAPI](wasapi.md)oder die [EndpointVolume-API](endpointvolume-api.md)zugreifen können.

Wie bereits erläutert, stellen die [MMDevice-API,](mmdevice-api.md) [WASAPI](wasapi.md)und die [EndpointVolume-API Mikrofone,](endpointvolume-api.md) Lautsprecher, Lautsprecher und andere Audioeingabe- und -ausgabegeräte als [Audioendpunktgeräte](audio-endpoint-devices.md)für Clients bereit. Das Endpunktgerätemodell bietet Clients bequemen Zugriff auf Lautstärke- und Stummschaltungssteuerelemente auf Audiogeräten. Clients, die nur diese einfachen Steuerelemente benötigen, können das Durchlaufen der internen Topologien von Hardwaregeräten in Audioadaptern vermeiden.

In Windows Vista konfiguriert die Audio-Engine automatisch die Topologien von Audiogeräten für die Verwendung durch Audioanwendungen. Daher müssen Anwendungen die DeviceTopology-API nur selten zu diesem Zweck verwenden, falls überhaupt. Angenommen, ein Audioadapter enthält einen Eingabemultixer, der einen Datenstrom entweder aus einer Zeileneingabe oder einem Mikrofon erfassen kann, aber keine Datenströme von beiden Endpunktgeräten gleichzeitig erfassen kann. Angenommen, der Benutzer hat Anwendungen im exklusiven Modus aktiviert, um die Verwendung eines Audioendpunktgeräts durch Anwendungen im gemeinsam genutzten Modus zu verstellen, wie unter [Exklusiver Modus Streams](exclusive-mode-streams.md)beschrieben. Wenn eine Anwendung im gemeinsam genutzten Modus einen Datenstrom aus der Zeileneingabe erfasst, wenn eine Anwendung im exklusiven Modus mit der Aufzeichnung eines Streams über das Mikrofon beginnt, schaltet die Audio-Engine den Multiplexer automatisch von der Zeileneingabe in das Mikrofon um. In früheren Versionen von Windows, einschließlich Windows XP, verwendet die Anwendung im exklusiven Modus in diesem Beispiel die **mixerXxx-Funktionen** in der Windows Multimedia-API, um die Topologien der Adaptergeräte zu durchlaufen, den Multiplexer zu ermitteln und den Multiplexer zu konfigurieren, um die Mikrofoneingabe auszuwählen. In Windows Vista sind diese Schritte nicht mehr erforderlich.

Einige Clients erfordern jedoch möglicherweise eine explizite Kontrolle über Arten von Audiohardwaresteuerelementen, auf die nicht über die MMDevice-API, WASAPI oder die EndpointVolume-API zugegriffen werden kann. Für diese Clients bietet die DeviceTopology-API die Möglichkeit, die Topologien von Adaptergeräten zu durchlaufen, um die Audiosteuerelemente auf den Geräten zu ermitteln und zu verwalten. Anwendungen, die die DeviceTopology-API verwenden, müssen mit Vorsicht entworfen werden, um Windows Audiorichtlinie zu verhindern und die internen Konfigurationen von Audiogeräten zu beeinträchtigen, die für andere Anwendungen freigegeben werden. Weitere Informationen zu Windows Audiorichtlinie finden Sie unter [Benutzermodus-Audiokomponenten.](user-mode-audio-components.md)

Die DeviceTopology-API stellt Schnittstellen zum Ermitteln und Verwalten der folgenden Arten von Audiosteuerelementen in einer Gerätetopologie bereit:

-   Steuerung der automatischen Verstärkung
-   Steuerelement "Linden"
-   Eingabeselektor (Multiplexer)
-   Lautstärkesteuerung
-   Midrange-Steuerelement
-   Stummschalten des Steuerelements
-   Ausgabeselektor (Demultiplexer)
-   Spitzenzähler
-   Treble-Steuerelement
-   Volumesteuerung

Darüber hinaus ermöglicht die DeviceTopology-API Clients, Adaptergeräte nach Informationen zu den von ihnen unterstützten Streamformaten abzufragen. Die Headerdatei Devicetopology.h definiert die Schnittstellen in der DeviceTopology-API.

Das folgende Diagramm zeigt ein Beispiel für mehrere verbundene Gerätetopologien für den Teil eines PCI-Adapters, der Audiodaten von einem Mikrofon, einer Zeileneingabe und einem CD-Player erfasst.

![Beispiel für vier Topologien für verbundene Geräte](images/fig2.jpg)

Das obige Diagramm zeigt die Datenpfade, die von den analogen Eingaben zum Systembus führen. Jedes der folgenden Geräte wird als Gerätetopologieobjekt mit einer [**IDeviceTopology-Schnittstelle**](/windows/desktop/api/Devicetopology/nn-devicetopology-idevicetopology) dargestellt:

-   Wave capture device (Wellenerfassungsgerät)
-   Eingabe-Multiplexergerät
-   Endpunktgerät A
-   Endpunktgerät B

Beachten Sie, dass das Topologiediagramm Adaptergeräte (Die Wellenerfassungs- und Eingabemultixergeräte) mit Endpunktgeräten kombiniert. Über die Verbindungen zwischen Geräten werden Audiodaten von einem Gerät zum nächsten übertragen. Auf jeder Seite einer Verbindung befindet sich ein Connector (im Diagramm als Con bezeichnet), über den Daten in ein Gerät gelangen oder es verlassen.

Am linken Rand des Diagramms gelangen Signale von der Zeileneingabe und den Mikrofonbuchsen in die Endpunktgeräte.

Innerhalb des Wave Capture-Geräts und des Eingabe-Multiplexergeräts sind Streamverarbeitungsfunktionen, die in der Terminologie der DeviceTopology-API als Untereinheiten bezeichnet werden. Die folgenden Typen von Untereinheiten werden im vorherigen Diagramm angezeigt:

-   Volumesteuerelement (mit der Bezeichnung Vol bezeichnet)
-   Stummschaltungssteuerelement (mit der Bezeichnung Stummschalten bezeichnet)
-   Multiplexer (oder Eingabeselektor mit der Bezeichnung MUX)
-   Analog-digital-Konverter (bezeichnet als ADC)

Die Einstellungen in den Untereinheiten Volume, Stummschaltung und Multiplexer können von Clients gesteuert werden, und die DeviceTopology-API stellt Steuerungsschnittstellen für Clients bereit, um sie zu steuern. In diesem Beispiel verfügt die ADC-Untereinheit über keine Steuerungseinstellungen. Daher stellt die DeviceTopology-API keine Steuerungsschnittstelle für den ADC bereit.

In der Terminologie der DeviceTopology-API gehören Connectors und Untereinheiten zur gleichen allgemeinen Kategorie– Teile. Alle Teile stellen einen gemeinsamen Satz von Funktionen bereit, unabhängig davon, ob es sich um Connectors oder Untereinheiten handelt. Die DeviceTopology-API implementiert eine [**IPart-Schnittstelle,**](/windows/desktop/api/Devicetopology/nn-devicetopology-ipart) um die generischen Funktionen darzustellen, die Connectors und Untereinheiten gemeinsam sind. Die API implementiert die [**IConnector-**](/windows/desktop/api/Devicetopology/nn-devicetopology-iconnector) und [**ISubunit-Schnittstellen,**](/windows/win32/api/devicetopology/nn-devicetopology-isubunit) um die spezifischen Aspekte von Connectors und Untereinheiten darzustellen.

Die DeviceTopology-API erstellt die Topologien des Wave capture-Geräts und des Eingabe-Multiplexergeräts aus den Kernelstreamingfiltern (KS), die der Audiotreiber dem Betriebssystem zur Darstellung dieser Geräte verfügbar macht. (Der Audioadaptertreiber implementiert **IMiniportWaveXxx-** und **IMiniportTopology-Schnittstellen,** um die hardwareabhängigen Teile dieser Filter darzustellen. Weitere Informationen zu diesen Schnittstellen und zu KS-Filtern finden Sie in der Windows DDK-Dokumentation.)

Die DeviceTopology-API erstellt triviale Topologien, um die Endpunktgeräte A und B im vorherigen Diagramm darzustellen. Die Gerätetopologie eines Endpunktgeräts besteht aus einem einzelnen Connector. Diese Topologie ist lediglich ein Platzhalter für das Endpunktgerät und enthält keine Untereinheiten für die Verarbeitung von Audiodaten. Tatsächlich enthalten Adaptergeräte alle Untereinheiten, die Clientanwendungen zum Steuern der Audioverarbeitung verwenden. Die Gerätetopologie eines Endpunktgeräts dient in erster Linie als Ausgangspunkt für die Untersuchung der Gerätetopologien von Adaptergeräten.

Interne Verbindungen zwischen zwei Teilen in einer Gerätetopologie werden als Links bezeichnet. Die DeviceTopology-API stellt Methoden zum Durchlaufen von Links von einem Teil zum nächsten in einer Gerätetopologie bereit. Die API stellt auch Methoden zum Durchlaufen der Verbindungen zwischen Gerätetopologien bereit.

Um mit der Untersuchung eines Satzes verbundener Gerätetopologien zu beginnen, aktiviert eine Clientanwendung die **IDeviceTopology-Schnittstelle** eines Audioendpunktgeräts. Der Connector auf einem Endpunktgerät stellt entweder eine Verbindung mit einem Connector in einem Audioadapter oder mit einem Netzwerk her. Wenn der Endpunkt eine Verbindung mit einem Gerät auf einem Audioadapter herstellt, können die Methoden in der DeviceTopology-API der Anwendung ermöglichen, die Verbindung zwischen dem Endpunkt und dem Adapter schrittweise herzustellen, indem sie einen Verweis auf die **IDeviceTopology-Schnittstelle** des Adaptergeräts auf der anderen Seite der Verbindung erhält. Ein Netzwerk verfügt dagegen über keine Gerätetopologie. Eine Netzwerkverbindung überlässt einen Audiostream an einen Client, der remote auf das System zugreift.

Die DeviceTopology-API bietet nur Zugriff auf die Topologien der Hardwaregeräte in einem Audioadapter. Die externen Geräte am linken Rand des Diagramms und die Softwarekomponenten am rechten Rand liegen außerhalb des Bereichs der API. Die gestrichelten Linien auf beiden Seiten des Diagramms stellen die Grenzwerte der DeviceTopology-API dar. Der Client kann die API verwenden, um einen Datenpfad zu untersuchen, der sich von der Eingabebuchse bis zum Systembus erstreckt, aber die API kann diese Grenzen nicht überschreiten.

Jeder Connector im obigen Diagramm verfügt über einen zugeordneten Verbindungstyp, der den Typ der Verbindung angibt, die vom Connector hergestellt wird. Daher verfügen die Connectors auf den beiden Seiten einer Verbindung immer über identische Verbindungstypen. Der Verbindungstyp wird durch einen [**ConnectorType-Enumerationswert**](/windows/win32/api/devicetopology/ne-devicetopology-connectortype) angegeben: Physisch \_ extern, physisch \_ intern, Software \_ fixed, \_ Software-E/A oder Netzwerk. Die Verbindungen zwischen dem Eingabe-Multiplexergerät und den Endpunktgeräten A und B sind vom Typ Physisch \_ extern. Dies bedeutet, dass die Verbindung eine physische Verbindung mit einem externen Gerät darstellt (d. h. eine vom Benutzer zugängliche Audiobuchse). Die Verbindung mit dem analogen Signal vom internen CD-Player ist vom Typ Physisch \_ intern, was auf eine physische Verbindung mit einem Hilfsgerät hinweist, das im Systemchassis installiert ist. Die Verbindung zwischen dem Wave capture-Gerät und dem Eingabe-Multiplexergerät ist vom Typ Software \_ Fixed. Dies gibt eine permanente Verbindung an, die behoben ist und nicht unter Softwaresteuerung konfiguriert werden kann. Schließlich ist die Verbindung mit dem Systembus auf der rechten Seite des Diagramms vom Typ \_ Software-E/A, der angibt, dass die Daten-E/A für die Verbindung von einer DMA-Engine unter Softwaresteuerung implementiert wird. (Das Diagramm enthält kein Beispiel für einen Netzwerkverbindungstyp.)

Der Client beginnt mit dem Durchlaufen eines Datenpfads auf dem Endpunktgerät. Zunächst ruft der Client eine [**IMMDevice-Schnittstelle**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) ab, die das Endpunktgerät darstellt, wie unter [Auflisten von Audiogeräten](enumerating-audio-devices.md)erläutert. Um die **IDeviceTopology-Schnittstelle** für das Endpunktgerät abzurufen, ruft der Client die [**IMMDevice::Activate-Methode**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) auf, wobei der Parameter *iid* auf REFIID IID \_ IDeviceTopology festgelegt ist.

Im Beispiel im vorherigen Diagramm enthält das Eingabe-Multiplexergerät alle Hardwaresteuerelemente (Lautstärke, Stummschaltung und Multiplexer) für die Erfassungsstreams aus den Zeileneingabe- und Mikrofonbuchsen. Das folgende Codebeispiel zeigt, wie Sie die **IDeviceTopology-Schnittstelle** für das Eingabemultixergerät von der **IMMDevice-Schnittstelle** für das Endpunktgerät für die Zeileneingabe oder das Mikrofon abrufen:


```C++
//-----------------------------------------------------------
// The input argument to this function is a pointer to the
// IMMDevice interface of an endpoint device. The function
// outputs a pointer (counted reference) to the
// IDeviceTopology interface of the adapter device that
// connects to the endpoint device.
//-----------------------------------------------------------
#define EXIT_ON_ERROR(hres)  \
              if (FAILED(hres)) { goto Exit; }
#define SAFE_RELEASE(punk)  \
              if ((punk) != NULL)  \
                { (punk)->Release(); (punk) = NULL; }

const IID IID_IDeviceTopology = __uuidof(IDeviceTopology);
const IID IID_IPart = __uuidof(IPart);

HRESULT GetHardwareDeviceTopology(
            IMMDevice *pEndptDev,
            IDeviceTopology **ppDevTopo)
{
    HRESULT hr = S_OK;
    IDeviceTopology *pDevTopoEndpt = NULL;
    IConnector *pConnEndpt = NULL;
    IConnector *pConnHWDev = NULL;
    IPart *pPartConn = NULL;

    // Get the endpoint device's IDeviceTopology interface.

    hr = pEndptDev->Activate(
                      IID_IDeviceTopology, CLSCTX_ALL,
                      NULL, (void**)&pDevTopoEndpt);
    EXIT_ON_ERROR(hr)

    // The device topology for an endpoint device always
    // contains just one connector (connector number 0).

    hr = pDevTopoEndpt->GetConnector(0, &pConnEndpt);
    EXIT_ON_ERROR(hr)

    // Use the connector in the endpoint device to get the
    // connector in the adapter device.

    hr = pConnEndpt->GetConnectedTo(&pConnHWDev);
    EXIT_ON_ERROR(hr)

    // Query the connector in the adapter device for
    // its IPart interface.

    hr = pConnHWDev->QueryInterface(
                         IID_IPart, (void**)&pPartConn);
    EXIT_ON_ERROR(hr)

    // Use the connector's IPart interface to get the
    // IDeviceTopology interface for the adapter device.

    hr = pPartConn->GetTopologyObject(ppDevTopo);

Exit:
    SAFE_RELEASE(pDevTopoEndpt)
    SAFE_RELEASE(pConnEndpt)
    SAFE_RELEASE(pConnHWDev)
    SAFE_RELEASE(pPartConn)

    return hr;
}
```



Die GetHardwareDeviceTopology-Funktion im vorherigen Codebeispiel führt die folgenden Schritte aus, um die **IDeviceTopology-Schnittstelle** für das Eingabe-Multiplexergerät abzurufen:

1.  Rufen Sie die **IMMDevice::Activate-Methode** auf, um die **IDeviceTopology-Schnittstelle** für das Endpunktgerät abzurufen.
2.  Rufen Sie mit der **IDeviceTopology-Schnittstelle** aus dem vorherigen Schritt die [**IDeviceTopology::GetConnector-Methode**](/windows/desktop/api/Devicetopology/nf-devicetopology-idevicetopology-getconnector) auf, um die **IConnector-Schnittstelle** des einzelnen Connectors (Connectornummer 0) auf dem Endpunktgerät abzurufen.
3.  Rufen Sie mit der **IConnector-Schnittstelle** aus dem vorherigen Schritt die [**IConnector::GetConnectedTo-Methode**](/windows/desktop/api/Devicetopology/nf-devicetopology-iconnector-getconnectedto) auf, um die **IConnector-Schnittstelle** des Connectors im Eingabe-Multiplexergerät abzurufen.
4.  Fragen Sie die im vorherigen Schritt abgerufene **IConnector-Schnittstelle** nach ihrer **IPart-Schnittstelle** ab.
5.  Rufen Sie mit der im vorherigen Schritt abgerufenen **IPart-Schnittstelle** die [**IPart::GetTopologyObject-Methode**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-gettopologyobject) auf, um die **IDeviceTopology-Schnittstelle** für das Eingabe-Multiplexergerät abzurufen.

Bevor der Benutzer über das Mikrofon im vorherigen Diagramm aufzeichnen kann, muss die Clientanwendung sicherstellen, dass der Multiplexer die Mikrofoneingabe auswählt. Das folgende Codebeispiel zeigt, wie ein Client den Datenpfad vom Mikrofon durchlaufen kann, bis er den Multiplexer findet, den er dann programmiert, um die Mikrofoneingabe auszuwählen:


```C++
//-----------------------------------------------------------
// The input argument to this function is a pointer to the
// IMMDevice interface for a capture endpoint device. The
// function traverses the data path that extends from the
// endpoint device to the system bus (for example, PCI)
// or external bus (USB). If the function discovers a MUX
// (input selector) in the path, it selects the MUX input
// that connects to the stream from the endpoint device.
//-----------------------------------------------------------
#define EXIT_ON_ERROR(hres)  \
              if (FAILED(hres)) { goto Exit; }
#define SAFE_RELEASE(punk)  \
              if ((punk) != NULL)  \
                { (punk)->Release(); (punk) = NULL; }

const IID IID_IDeviceTopology = __uuidof(IDeviceTopology);
const IID IID_IPart = __uuidof(IPart);
const IID IID_IConnector = __uuidof(IConnector);
const IID IID_IAudioInputSelector = __uuidof(IAudioInputSelector);

HRESULT SelectCaptureDevice(IMMDevice *pEndptDev)
{
    HRESULT hr = S_OK;
    DataFlow flow;
    IDeviceTopology *pDeviceTopology = NULL;
    IConnector *pConnFrom = NULL;
    IConnector *pConnTo = NULL;
    IPart *pPartPrev = NULL;
    IPart *pPartNext = NULL;
    IAudioInputSelector *pSelector = NULL;

    if (pEndptDev == NULL)
    {
        EXIT_ON_ERROR(hr = E_POINTER)
    }

    // Get the endpoint device's IDeviceTopology interface.
    hr = pEndptDev->Activate(
                      IID_IDeviceTopology, CLSCTX_ALL, NULL,
                      (void**)&pDeviceTopology);
    EXIT_ON_ERROR(hr)

    // The device topology for an endpoint device always
    // contains just one connector (connector number 0).
    hr = pDeviceTopology->GetConnector(0, &pConnFrom);
    SAFE_RELEASE(pDeviceTopology)
    EXIT_ON_ERROR(hr)

    // Make sure that this is a capture device.
    hr = pConnFrom->GetDataFlow(&flow);
    EXIT_ON_ERROR(hr)

    if (flow != Out)
    {
        // Error -- this is a rendering device.
        EXIT_ON_ERROR(hr = AUDCLNT_E_WRONG_ENDPOINT_TYPE)
    }

    // Outer loop: Each iteration traverses the data path
    // through a device topology starting at the input
    // connector and ending at the output connector.
    while (TRUE)
    {
        BOOL bConnected;
        hr = pConnFrom->IsConnected(&bConnected);
        EXIT_ON_ERROR(hr)

        // Does this connector connect to another device?
        if (bConnected == FALSE)
        {
            // This is the end of the data path that
            // stretches from the endpoint device to the
            // system bus or external bus. Verify that
            // the connection type is Software_IO.
            ConnectorType  connType;
            hr = pConnFrom->GetType(&connType);
            EXIT_ON_ERROR(hr)

            if (connType == Software_IO)
            {
                break;  // finished
            }
            EXIT_ON_ERROR(hr = E_FAIL)
        }

        // Get the connector in the next device topology,
        // which lies on the other side of the connection.
        hr = pConnFrom->GetConnectedTo(&pConnTo);
        EXIT_ON_ERROR(hr)
        SAFE_RELEASE(pConnFrom)

        // Get the connector's IPart interface.
        hr = pConnTo->QueryInterface(
                        IID_IPart, (void**)&pPartPrev);
        EXIT_ON_ERROR(hr)
        SAFE_RELEASE(pConnTo)

        // Inner loop: Each iteration traverses one link in a
        // device topology and looks for input multiplexers.
        while (TRUE)
        {
            PartType parttype;
            UINT localId;
            IPartsList *pParts;

            // Follow downstream link to next part.
            hr = pPartPrev->EnumPartsOutgoing(&pParts);
            EXIT_ON_ERROR(hr)

            hr = pParts->GetPart(0, &pPartNext);
            pParts->Release();
            EXIT_ON_ERROR(hr)

            hr = pPartNext->GetPartType(&parttype);
            EXIT_ON_ERROR(hr)

            if (parttype == Connector)
            {
                // We've reached the output connector that
                // lies at the end of this device topology.
                hr = pPartNext->QueryInterface(
                                  IID_IConnector,
                                  (void**)&pConnFrom);
                EXIT_ON_ERROR(hr)

                SAFE_RELEASE(pPartPrev)
                SAFE_RELEASE(pPartNext)
                break;
            }

            // Failure of the following call means only that
            // the part is not a MUX (input selector).
            hr = pPartNext->Activate(
                              CLSCTX_ALL,
                              IID_IAudioInputSelector,
                              (void**)&pSelector);
            if (hr == S_OK)
            {
                // We found a MUX (input selector), so select
                // the input from our endpoint device.
                hr = pPartPrev->GetLocalId(&localId);
                EXIT_ON_ERROR(hr)

                hr = pSelector->SetSelection(localId, NULL);
                EXIT_ON_ERROR(hr)

                SAFE_RELEASE(pSelector)
            }

            SAFE_RELEASE(pPartPrev)
            pPartPrev = pPartNext;
            pPartNext = NULL;
        }
    }

Exit:
    SAFE_RELEASE(pConnFrom)
    SAFE_RELEASE(pConnTo)
    SAFE_RELEASE(pPartPrev)
    SAFE_RELEASE(pPartNext)
    SAFE_RELEASE(pSelector)
    return hr;
}
```



Die DeviceTopology-API implementiert eine [**IAudioInputSelector-Schnittstelle,**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioinputselector) um einen Multiplexer zu kapseln, z. B. den im vorherigen Diagramm. (Eine [**IAudioOutputSelector-Schnittstelle**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiooutputselector) kapselt einen Demultiplexer.) Im vorherigen Codebeispiel fragt die innere Schleife der SelectCaptureDevice-Funktion jede gefundene Untereinheit ab, um zu ermitteln, ob die Untereinheit ein Multiplexer ist. Wenn die Untereinheit ein Multiplexer ist, ruft die Funktion die [**IAudioInputSelector::SetSelection-Methode**](/windows/desktop/api/Devicetopology/nf-devicetopology-iaudioinputselector-setselection) auf, um die Eingabe auszuwählen, die vom Endpunktgerät eine Verbindung mit dem Stream herstellt.

Im vorherigen Codebeispiel durchläuft jede Iteration der äußeren Schleife eine Gerätetopologie. Beim Durchlaufen der Gerätetopologien im vorherigen Diagramm durchläuft die erste Iteration das Eingabe-Multiplexergerät, und die zweite Iteration durchläuft das Wellenerfassungsgerät. Die Funktion wird beendet, wenn sie den Connector am rechten Rand des Diagramms erreicht. Die Beendigung tritt auf, wenn die Funktion einen Connector mit einem \_ Software-E/A-Verbindungstyp erkennt. Dieser Verbindungstyp identifiziert den Punkt, an dem das Adaptergerät eine Verbindung mit dem Systembus herstellt.

Der Aufruf der [**IPart::GetPartType-Methode**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getparttype) im vorherigen Codebeispiel ruft einen **IPartType-Enumerationswert** ab, der angibt, ob der aktuelle Teil ein Connector oder eine Audioverarbeitungsuntereinheit ist.

Die innere Schleife im vorherigen Codebeispiel durch Aufrufen der [**IPart::EnumPartsOutgoing-Methode**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-enumpartsoutgoing) über den Link von einem Teil zum nächsten. (Es gibt auch eine [**IPart::EnumPartsIncoming-Methode**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-enumpartsincoming) zum Schrittweisen in entgegengesetzter Richtung.) Diese Methode ruft ein [**IPartsList-Objekt**](/windows/desktop/api/Devicetopology/nn-devicetopology-ipartslist) ab, das eine Liste aller ausgehenden Teile enthält. Jeder Teil, den die SelectCaptureDevice-Funktion auf einem Erfassungsgerät erwartet, hat jedoch immer genau einen ausgehenden Teil. Daher fordert der nachfolgende Aufruf von [**IPartsList::GetPart**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipartslist-getpart) immer den ersten Teil in der Liste an, Teil 0, da die Funktion davon ausgeht, dass dies der einzige Teil in der Liste ist.

Wenn die SelectCaptureDevice-Funktion auf eine Topologie stößt, für die diese Annahme ungültig ist, kann die Funktion das Gerät möglicherweise nicht ordnungsgemäß konfigurieren. Um einen solchen Fehler zu vermeiden, kann eine allgemeinere Version der Funktion wie folgt funktionieren:

-   Rufen Sie die [**IPartsList::GetCount-Methode**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipartslist-getcount) auf, um die Anzahl ausgehender Teile zu bestimmen.
-   Rufen Sie für jeden ausgehenden Teil **IPartsList::GetPart** auf, um mit dem Durchlaufen des Datenpfads zu beginnen, der vom Teil führt.

Einige, aber nicht unbedingt alle Teile verfügen über zugeordnete Hardwaresteuerelemente, die Clients festlegen oder abrufen können. Ein bestimmter Teil kann über 0 (null), eine oder mehrere Hardwaresteuerelemente verfügen. Ein Hardwaresteuerelement wird durch das folgende Schnittstellenpaar dargestellt:

-   Eine generische Steuerelementschnittstelle, [**IControlInterface,**](/windows/desktop/api/Devicetopology/nn-devicetopology-icontrolinterface)mit Methoden, die allen Hardwaresteuerelementen gemeinsam sind.
-   Eine funktionsspezifische Schnittstelle (z. [**B. IAudioVolumeLevel),**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiovolumelevel)die die Steuerungsparameter für einen bestimmten Typ von Hardwaresteuerelement (z. B. ein Volumesteuerelement) verfügbar macht.

Um die Hardwaresteuerelemente für einen Teil aufzulisten, ruft der Client zuerst die [**IPart::GetControlInterfaceCount-Methode**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getcontrolinterfacecount) auf, um die Anzahl der Hardwaresteuerelemente zu bestimmen, die dem Teil zugeordnet sind. Als Nächstes ruft der Client die [**IPart::GetControlInterface-Methode**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getcontrolinterface) auf, um die **IControlInterface-Schnittstelle** für jedes Hardwaresteuerelement abzurufen. Schließlich ruft der Client die funktionsspezifische Schnittstelle für jedes Hardwaresteuerelement ab, indem er die [**IControlInterface::GetIID-Methode**](/windows/desktop/api/Devicetopology/nf-devicetopology-icontrolinterface-getiid) aufruft, um die Schnittstellen-ID abzurufen. Der Client ruft die [**IPart::Activate-Methode**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-activate) mit dieser ID auf, um die funktionsspezifische Schnittstelle abzurufen.

Ein Teil, der ein Connector ist, unterstützt möglicherweise eine der folgenden funktionsspezifischen Steuerelementschnittstellen:

-   [**IKsFormatSupport**](/windows/desktop/api/Devicetopology/nn-devicetopology-iksformatsupport)
-   [**IKsJackDescription**](/windows/desktop/api/Devicetopology/nn-devicetopology-iksjackdescription)

Ein Teil, der eine Untereinheit ist, kann eine oder mehrere der folgenden funktionsspezifischen Steuerelementschnittstellen unterstützen:

-   [**IAudioAutoGainControl**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioautogaincontrol)
-   [**IAudioBass**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiobass)
-   [**IAudioChannelConfig**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiochannelconfig)
-   [**IAudioInputSelector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioinputselector)
-   [**IAudioLoudness**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioloudness)
-   [**IAudioMidrange**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiomidrange)
-   [**IAudioMute**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiomute)
-   [**IAudioOutputSelector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiooutputselector)
-   [**IAudioPeakMeter**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiopeakmeter)
-   [**IAudioTreble**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiotreble)
-   [**IAudioVolumeLevel**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiovolumelevel)
-   [**IDeviceSpecificProperty**](/windows/desktop/api/Devicetopology/nn-devicetopology-idevicespecificproperty)

Ein Teil unterstützt die **IDeviceSpecificProperty-Schnittstelle** nur, wenn das zugrunde liegende Hardwaresteuerelement über einen gerätespezifischen Steuerelementwert verfügt und das Steuerelement nicht angemessen durch eine andere funktionsspezifische Schnittstelle in der vorherigen Liste dargestellt werden kann. In der Regel ist eine gerätespezifische Eigenschaft nur für einen Client nützlich, der die Bedeutung des Eigenschaftswerts aus Informationen wie dem Teiltyp, Teiluntertyp und Teilnamen ableiten kann. Der Client kann diese Informationen abrufen, indem er die Methoden [**IPart::GetPartType,**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getparttype) [**IPart::GetSubType**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getsubtype)und [**IPart::GetName aufruft.**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getname)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Programmierhandbuch](programming-guide.md)
</dt> </dl>

 

 
