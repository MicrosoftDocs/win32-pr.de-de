---
description: Gerätetopologien
ms.assetid: 5ac421e5-74a4-40e8-af6f-a99a05ebc3e0
title: Gerätetopologien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31e0af267bb4a0fa924ee23d36a2a615ac5ae7fa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524256"
---
# <a name="device-topologies"></a>Gerätetopologien

Die [devicetopology-API](devicetopology-api.md) ermöglicht Clients die Kontrolle über eine Vielzahl von internen Funktionen von audioadaptern, auf die Sie über die [mmdevice-API](mmdevice-api.md), die [WASAPI](wasapi.md)oder die [endpointvolume-API](endpointvolume-api.md)nicht zugreifen können.

Wie bereits erläutert, stellen die [mmdevice-API](mmdevice-api.md), [WASAPI](wasapi.md)und die [endpointvolume-API](endpointvolume-api.md) an Clients als [audioendpunktgeräte](audio-endpoint-devices.md)Mikrofon, Referenten, Kopfhörer und andere Audioeingabe-und-Ausgabegeräte zur Verfügung. Das Endpunkt Gerätemodell ermöglicht Clients den bequemen Zugriff auf die Volume-und stumm Steuerelemente in Audiogeräten. Clients, die nur diese einfachen Steuerelemente benötigen, können vermeiden, dass die internen Topologien von Hardware Geräten in audioadaptern durchlaufen werden.

In Windows Vista konfiguriert die Audioengine automatisch die Topologien von Audiogeräten für die Verwendung durch Audioanwendungen. Daher müssen Anwendungen selten, falls immer, die Debug-API-API zu diesem Zweck verwenden. Nehmen wir beispielsweise an, dass ein Audioadapter einen eingabemultiplexer enthält, der einen Stream aus einer Zeilen Eingabe oder einem Mikrofon erfassen kann, aber nicht gleichzeitig Datenströme von beiden Endpunkt Geräten erfassen kann. Angenommen, der Benutzer hat Anwendungen im exklusiven Modus aktiviert, um die Verwendung eines audioendpunktgeräts durch Anwendungen im freigegebenen Modus vorzuführen, wie in Daten [strömen im exklusiven Modus](exclusive-mode-streams.md)beschrieben. Wenn eine Anwendung im freigegebenen Modus einen Stream aus der Zeilen Eingabe abzeichnet, wenn eine Anwendung im exklusiven Modus beginnt, einen Stream vom Mikrofon aufzuzeichnen, schaltet die Audioengine den Multiplexer automatisch von der Zeilen Eingabe in das Mikrofon um. In früheren Versionen von Windows, einschließlich Windows XP, würde die Anwendung im exklusiven Modus in diesem Beispiel die **mixerxxx** -Funktionen in der Windows-Multimedia-API verwenden, um die Topologien der Adapter Geräte zu durchlaufen, den Multiplexer zu ermitteln und den Multiplexer so zu konfigurieren, dass die Mikrofon Eingabe ausgewählt wird. In Windows Vista sind diese Schritte nicht mehr erforderlich.

Einige Clients benötigen jedoch möglicherweise explizite Kontrolle über die Typen von audiohardwaresteuerelementen, auf die über die mmdevice-API, die WASAPI oder die endpointvolume-API nicht zugegriffen werden kann. Für diese Clients bietet die devicetopology-API die Möglichkeit, die Topologien von Adapter Geräten zu durchlaufen, um die Audiosteuerelemente in den Geräten zu ermitteln und zu verwalten. Anwendungen, die die devicetopology-API verwenden, müssen sorgfältig entworfen werden, um das stören der Windows-audiorichtlinie zu vermeiden und die internen Konfigurationen von Audiogeräten zu beeinträchtigen, die für andere Anwendungen freigegeben sind. Weitere Informationen zur Windows-audiorichtlinie finden Sie unter [benutzermodusaudiokomponenten](user-mode-audio-components.md).

Die devicetopology-API stellt Schnittstellen zum Ermitteln und Verwalten der folgenden Typen von Audiosteuer Elementen in einer Geräte Topologie bereit:

-   Automatisches erlangen von Steuerelementen
-   Bass-Steuerelement
-   Eingabeauswahl (Multiplexer)
-   Lautheit-Steuerelement
-   Midrange-Steuerelement
-   Steuerelement stumm schalten
-   Ausgabe Auswahl (Demultiplexer)
-   Spitzen Meter
-   Treble-Steuerelement
-   Volumesteuerung

Außerdem ermöglicht die devicetopology-API Clients, Adapter Geräte nach Informationen zu den von Ihnen unterstützten Streamingformaten abzufragen. In der Header Datei devicetopology. h sind die Schnittstellen in der devicetopology-API definiert.

Das folgende Diagramm zeigt ein Beispiel für mehrere verbundene gerätetopologien für den Teil eines PCI-Adapters, der Audiodaten von einem Mikrofon, einer Zeilen Eingabe und einem CD-Player aufzeichnet.

![Beispiel für vier Topologien mit verbundenen Geräten](images/fig2.jpg)

Das obige Diagramm zeigt die Daten Pfade, die von den analogen Eingaben zum Systembus geleitet werden. Jedes der folgenden Geräte wird als Geräte Topologieobjekt mit einer [**idevicetopology**](/windows/desktop/api/Devicetopology/nn-devicetopology-idevicetopology) -Schnittstelle dargestellt:

-   Wave Capture-Gerät
-   Eingabe-Multiplexer-Gerät
-   Endpunkt Gerät A
-   Endpunkt Gerät B

Beachten Sie, dass im Topologiediagramm Adapter Geräte (die Wellen Erfassung und die Eingabe-Multiplexer-Geräte) mit Endpunkt Geräten kombiniert werden. Über die Verbindungen zwischen Geräten werden Audiodaten von einem Gerät an das nächste weitergeleitet. Auf jeder Seite einer Verbindung befindet sich ein Connector (im Diagramm als "con" bezeichnet), über den Daten in ein Gerät eingegeben oder verlassen werden.

Am linken Rand des Diagramms geben Signale von den Zeilen-und Mikrofon-Buben die Endpunkt Geräte ein.

Innerhalb des Wave Capture-Geräts und des Eingabe-Multiplexer-Geräts handelt es sich um streamverarbeitungs Funktionen, die in der Terminologie der devicetopology-API als Untereinheiten bezeichnet werden. Die folgenden Typen von Untereinheiten werden im vorangehenden Diagramm angezeigt:

-   Volumesteuerelement (mit der Bezeichnung Vol)
-   Stumm Steuerelement (mit der Bezeichnung stumm)
-   Multiplexer (oder Eingabeauswahl; mit Bezeichnung MUX)
-   Analog zu Digital Converter (mit der Bezeichnung ADC)

Die Einstellungen in den Untereinheiten Volume, stumm und Multiplexer können von Clients gesteuert werden, und die devicetopology-API stellt Steuerungs Schnittstellen für Clients zur Steuerung bereit. In diesem Beispiel hat die ADC-Untereinheit keine Steuerungseinstellungen. Folglich bietet die API "de vicetopology" keine Steuerungs Schnittstelle für den ADC.

In der Terminologie der Debug-API-API Gehören Connectors und Untereinheiten zur gleichen allgemeinen Kategorie – Parts. Alle Teile, unabhängig davon, ob es sich um Connectors oder Untereinheiten handelt, stellen einen gemeinsamen Satz von Funktionen bereit. Die devicetopology-API implementiert eine [**ipart**](/windows/desktop/api/Devicetopology/nn-devicetopology-ipart) -Schnittstelle, die die generischen Funktionen darstellt, die von Connectors und Untereinheiten gemeinsam sind. Die API implementiert die [**IConnector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iconnector) -und [**isubunit**](/windows/win32/api/devicetopology/nn-devicetopology-isubunit) -Schnittstellen, um die spezifischen Aspekte von Connectors und Untereinheiten darzustellen.

Die devicetopology-API erstellt die Topologien des Wave Capture-Geräts und des Eingabe-Multiplexer-Geräts aus den kernelstreamingfiltern, die der Audiotreiber für das Betriebssystem zur Darstellung dieser Geräte verfügbar macht. (Der audioadaptertreiber implementiert **iminiportwavexxx** -und **iminiporttopology** -Schnittstellen, um die Hardware abhängigen Teile dieser Filter darzustellen. Weitere Informationen zu diesen Schnittstellen und zu KS-Filtern finden Sie in der Windows-DDK-Dokumentation.)

Die Debug-API erstellt triviale Topologien zur Darstellung der Endpunkt Geräte A und B im vorangehenden Diagramm. Die Geräte Topologie eines Endpunkt Geräts besteht aus einem einzelnen Connector. Bei dieser Topologie handelt es sich lediglich um einen Platzhalter für das Endpunktgerät, der keine Untereinheiten für die Verarbeitung von Audiodaten enthält. In der Tat enthalten Adapter Geräte alle Untereinheiten, die von Client Anwendungen zum Steuern der Audioverarbeitung verwendet werden. Die Geräte Topologie eines Endpunkt Geräts dient hauptsächlich als Ausgangspunkt für die Untersuchung der gerätetopologien von Adapter Geräten.

Interne Verbindungen zwischen zwei Teilen in einer Geräte Topologie werden als Verknüpfungen bezeichnet. Die devicetopology-API stellt Methoden zum Durchlaufen von Links von einem Teil zum nächsten in einer Geräte Topologie bereit. Die API bietet auch Methoden zum Durchlaufen der Verbindungen zwischen gerätetopologien.

Um mit der Untersuchung eines Satzes von Topologien verbundener Geräte zu beginnen, aktiviert eine Client Anwendung die **idevicetopology** -Schnittstelle eines audioendpunktgeräts. Der Connector in einem Endpunkt Gerät stellt eine Verbindung mit einem Connector in einem Audioadapter oder einem Netzwerk her. Wenn der Endpunkt eine Verbindung mit einem Gerät auf einem Audioadapter herstellt, ermöglichen die Methoden in der devicetopology-API der Anwendung, über die Verbindung zwischen dem Endpunkt und dem Adapter zu wechseln, indem Sie einen Verweis auf die **idevicetopology** -Schnittstelle des Adapter Geräts auf der anderen Seite der Verbindung erhalten. Ein Netzwerk hat dagegen keine Geräte Topologie. Eine Netzwerkverbindung leitet einen Audiostream an einen Client, der Remote auf das System zugreift.

Die devicetopology-API ermöglicht nur den Zugriff auf die Topologien der Hardware Geräte in einem Audioadapter. Die externen Geräte am linken Rand des Diagramms und die Softwarekomponenten am rechten Rand überschreiten den Geltungsbereich der API. Die gestrichelten Linien auf beiden Seiten des Diagramms stellen die Grenzen der devicetopology-API dar. Der Client kann die API verwenden, um einen Dateipfad zu untersuchen, der vom Eingabe-Jack zum Systembus reicht, aber die API kann nicht über diese Grenzen hinweg durchdringen.

Jeder Connector im vorangehenden Diagramm verfügt über einen zugeordneten Verbindungstyp, der den Verbindungstyp angibt, der vom Connector hergestellt wird. Daher verfügen die Connectors auf den beiden Seiten einer Verbindung immer über identische Verbindungstypen. Der Verbindungstyp wird durch einen [**ConnectorType**](/windows/win32/api/devicetopology/ne-devicetopology-connectortype) -Enumerationswert angegeben – physischer \_ externer, physischer interner, Software-Fixed, Software-e/a \_ \_ \_ oder Netzwerk. Die Verbindungen zwischen dem Eingabe-Multiplexer-Gerät und den Endpunkt Geräten A und B sind physischer \_ extern, d. h. die Verbindung stellt eine physische Verbindung mit einem externen Gerät dar (d. h. einen AudioJack, der vom Benutzer aufgerufen werden kann). Die Verbindung mit dem analogen Signal vom internen CD-Player ist vom Typ Physical \_ internal, was eine physische Verbindung mit einem zusätzlichen Gerät angibt, das im System Chassis installiert ist. Die Verbindung zwischen dem Wave Capture-Gerät und dem Eingabe-Multiplexer-Gerät ist vom Typ "Software \_ Fixed", was auf eine permanente Verbindung hinweist, die fest ist und nicht unter der Software Steuerung konfiguriert werden kann. Zum Schluss ist die Verbindung mit dem Systembus auf der rechten Seite des Diagramms vom Typ Software-e \_ /a, was darauf hinweist, dass die Daten-e/a für die Verbindung von einem DMA-Modul unter Software Steuerung implementiert wird. (Das Diagramm enthält kein Beispiel für einen Netzwerk Verbindungstyp.)

Der Client beginnt mit dem Durchlaufen eines Daten Pfads auf dem Endpunkt Gerät. Zuerst erhält der Client eine [**immdevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) -Schnittstelle, die das Endpunkt Gerät darstellt, wie in Auflisten von [Audiogeräten](enumerating-audio-devices.md)erläutert. Um die **idevicetopology** -Schnittstelle für das Endpunkt Gerät abzurufen, ruft der Client die Methode " [**immdevice:: Aktivierungs**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) " mit dem Parameter " *IID* " auf, der auf refi IID \_ idevicetopology festgelegt ist.

Im Beispiel im vorangehenden Diagramm enthält das Eingabe-Multiplexer-Gerät alle Hardware Steuerelemente (Volume, stumm und Multiplexer) für die Erfassungsdaten Ströme von den Zeilen-und Mikrofon-Buben. Im folgenden Codebeispiel wird veranschaulicht, wie Sie die **idevicetopology** -Schnittstelle für das Eingabe-Multiplexer-Gerät von der **immdevice** -Schnittstelle für das Endpunkt Gerät für die Zeilen Eingabe oder das Mikrofon abrufen:


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



Die Funktion "gethardwaredevicetopology" im vorangehenden Codebeispiel führt die folgenden Schritte aus, um die **idevicetopology** -Schnittstelle für das Eingabe-Multiplexer-Gerät abzurufen:

1.  Wenden Sie die **immdevice:: Aktivierungs** -Methode an, um die **idevicetopology** -Schnittstelle für das Endpunkt Gerät abzurufen.
2.  Mit der im vorherigen Schritt erhaltenen **idevicetopology** -Schnittstelle können Sie die [**idevicetopology:: getconnector**](/windows/desktop/api/Devicetopology/nf-devicetopology-idevicetopology-getconnector) -Methode aufrufen, um die **IConnector** -Schnittstelle des einzelnen Connector (Connector-Nummer 0) im Endpunkt Gerät abzurufen.
3.  Mit der **IConnector** -Schnittstelle, die Sie im vorherigen Schritt abgerufen haben, können Sie die [**IConnector:: getconnectedto**](/windows/desktop/api/Devicetopology/nf-devicetopology-iconnector-getconnectedto) -Methode aufrufen, um die **IConnector** -Schnittstelle des Konnektors im Eingabe-Multiplexer-Gerät abzurufen.
4.  Fragen Sie die **IConnector** -Schnittstelle ab, die im vorherigen Schritt für die **ipart** -Schnittstelle abgerufen wurde
5.  Mit der im vorherigen Schritt abzurufenden **ipart** -Schnittstelle können Sie die [**ipart:: gettopologyobject**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-gettopologyobject) -Methode aufrufen, um die **idevicetopology** -Schnittstelle für das eingabemultiplexer-Gerät abzurufen.

Bevor der Benutzer aus dem Mikrofon im vorangehenden Diagramm aufzeichnen kann, muss die Client Anwendung sicherstellen, dass der Multiplexer die Mikrofon Eingabe auswählt. Im folgenden Codebeispiel wird gezeigt, wie ein Client den Dateipfad vom Mikrofon durchlaufen kann, bis der Multiplexer gefunden wird, der dann die Mikrofon Eingabe auswählen kann:


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



Die devicetopology-API implementiert eine [**iaudioinputselector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioinputselector) -Schnittstelle, um einen Multiplexer (z. b. den im vorangehenden Diagramm) zu kapseln. (Eine [**iaudiooutputselector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiooutputselector) -Schnittstelle kapselt einen Demultiplexer.) Im vorangehenden Codebeispiel fragt die innere Schleife der selectcapturedevice-Funktion jede gefundene Untereinheit ab, um zu ermitteln, ob die Untereinheit ein Multiplexer ist. Wenn es sich bei der Teil Einheit um einen Multiplexer handelt, ruft die Funktion die [**iaudioinputselector:: setSelection**](/windows/desktop/api/Devicetopology/nf-devicetopology-iaudioinputselector-setselection) -Methode auf, um die Eingabe auszuwählen, die vom Endpunkt Gerät aus eine Verbindung mit dem Stream herstellt.

Im vorangehenden Codebeispiel durchläuft jede Iterationen der äußeren Schleife eine Geräte Topologie. Beim Durchlaufen der gerätetopologien im vorangehenden Diagramm durchläuft die erste Iteration das Eingabe-Multiplexer-Gerät, und die zweite Iteration durchläuft das Wave Capture-Gerät. Die Funktion wird beendet, wenn Sie den Connector am rechten Rand des Diagramms erreicht. Die Beendigung tritt auf, wenn die Funktion einen Connector mit einem Software- \_ IO-Verbindungstyp erkennt. Dieser Verbindungstyp gibt den Punkt an, an dem sich das Adapter Gerät mit dem Systembus verbindet.

Durch den Aufrufen der [**ipart:: getParser Type**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getparttype) -Methode im vorangehenden Codebeispiel wird ein **iparser Type** -Enumerationswert abgerufen, der angibt, ob es sich bei dem aktuellen Teil um einen Connector oder eine Audioverarbeitungs-Untereinheit handelt.

In der inneren-Schleife im vorangehenden Codebeispiel wird durch Aufrufen der [**ipart:: enumpartsoutgoing**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-enumpartsoutgoing) -Methode die Verknüpfung zwischen einem Teil und dem nächsten Schritt überschritten. (Es gibt auch eine [**ipart:: enumpartsincoming**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-enumpartsincoming) -Methode, die in umgekehrter Richtung verläuft.) Diese Methode ruft ein [**ipartslist**](/windows/desktop/api/Devicetopology/nn-devicetopology-ipartslist) -Objekt ab, das eine Liste aller ausgehenden Teile enthält. Alle Teile, die von der selectcapturedevice-Funktion in einem Erfassungsgerät erwartet werden, haben jedoch immer genau einen ausgehenden Teil. Folglich fordert der nachfolgende Aufrufe von [**ipartslist:: GetPart**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipartslist-getpart) immer den ersten Teil in der Liste an, Teil Nummer 0, da die Funktion annimmt, dass dies der einzige Teil in der Liste ist.

Wenn die selectcapturedevice-Funktion auf eine Topologie stößt, für die diese Annahme nicht gültig ist, kann die Funktion das Gerät möglicherweise nicht ordnungsgemäß konfigurieren. Um einen solchen Fehler zu vermeiden, kann eine allgemeinere Version der-Funktion folgende Aktionen ausführen:

-   Aufrufen der [**ipartslist:: GetCount**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipartslist-getcount) -Methode, um die Anzahl der ausgehenden Teile zu bestimmen.
-   Für jeden ausgehenden Teil muss **ipartslist:: GetPart** aufgerufen werden, um zu beginnen, den Daten Pfad zu durchlaufen, der aus dem Teil resultiert.

Einige, aber nicht unbedingt alle Teile verfügen über zugeordnete Hardware Steuerelemente, die von Clients festgelegt oder festgelegt werden können. Ein bestimmter Teil kann keine, eine oder mehrere Hardware Steuerelemente enthalten. Ein Hardware Steuerelement wird durch das folgende Schnittstellen Paar dargestellt:

-   Eine generische Steuerungs Schnittstelle ( [**icontrolinterface**](/windows/desktop/api/Devicetopology/nn-devicetopology-icontrolinterface)), die über Methoden verfügt, die allen Hardware Steuerelementen gemeinsam sind.
-   Eine Funktions spezifische Schnittstelle (z. b. [**iaudiovolumelevel**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiovolumelevel)), die die Steuerelement Parameter für einen bestimmten Typ von Hardware Steuerung (z. b. ein volumesteuerelement) verfügbar macht.

Zum Auflisten der Hardware Steuerelemente für einen Teil ruft der Client zuerst die [**ipart:: getcontrolinterfacecount**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getcontrolinterfacecount) -Methode auf, um die Anzahl der Hardware Steuerelemente zu ermitteln, die mit dem Teil verknüpft sind. Als Nächstes führt der Client eine Reihe von Aufrufen der [**ipart:: getcontrolinterface**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getcontrolinterface) -Methode aus, um die **icontrolinterface** -Schnittstelle für jedes Hardware Steuerelement abzurufen. Schließlich ruft der Client die Funktions spezifische Schnittstelle für jedes Hardware Steuerelement ab, indem er die [**icontrolinterface:: getiid**](/windows/desktop/api/Devicetopology/nf-devicetopology-icontrolinterface-getiid) -Methode zum Abrufen der Schnittstellen-ID anfordert. Der Client ruft die [**ipart:: Aktivierungs**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-activate) -Methode mit dieser ID auf, um die Funktions spezifische Schnittstelle abzurufen.

Ein Teil, bei dem es sich um einen Connector handelt, kann eine der folgenden Funktions spezifischen Steuerungs Schnittstellen unterstützen:

-   [**"Iksformatsupport"**](/windows/desktop/api/Devicetopology/nn-devicetopology-iksformatsupport)
-   [**"Iksjackdescription"**](/windows/desktop/api/Devicetopology/nn-devicetopology-iksjackdescription)

Ein Teil, bei dem es sich um eine Untereinheit handelt, kann eine oder mehrere der folgenden Funktions spezifischen Steuerungs Schnittstellen unterstützen:

-   [**Iaudioautogaincontrol**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioautogaincontrol)
-   [**Iaudiobass**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiobass)
-   [**Iaudiochannelconfig**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiochannelconfig)
-   [**Iaudioinputselector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioinputselector)
-   [**Iaudioloudness**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioloudness)
-   [**Iaudiomidrange**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiomidrange)
-   [**Iaudiomute**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiomute)
-   [**Iaudiooutputselector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiooutputselector)
-   [**Iaudiopeakmeter**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiopeakmeter)
-   [**Iaudiotreble**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiotreble)
-   [**Iaudiovolumelevel**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiovolumelevel)
-   [**Idevicespecificproperty**](/windows/desktop/api/Devicetopology/nn-devicetopology-idevicespecificproperty)

Ein Teil unterstützt die **idevicespecificproperty** -Schnittstelle nur dann, wenn das zugrunde liegende Hardware Steuerelement über einen gerätespezifischen Steuerelement Wert verfügt und das Steuerelement nicht durch eine andere Funktions spezifische Schnittstelle in der vorangehenden Liste dargestellt werden kann. In der Regel ist eine gerätespezifische Eigenschaft nur für einen Client nützlich, der die Bedeutung des Eigenschafts Werts aus Informationen wie z. b. dem Teiltyp, dem Part-Untertyp und dem Teilnamen ableiten kann. Der Client kann diese Informationen abrufen, indem er die Methoden [**ipart:: getparamettype**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getparttype), [**ipart:: getsubtype**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getsubtype)und [**ipart:: GetName**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getname) anruft.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Programmierhandbuch](programming-guide.md)
</dt> </dl>

 

 
