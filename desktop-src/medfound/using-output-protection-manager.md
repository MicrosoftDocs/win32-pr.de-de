---
description: Weitere Informationen finden Sie unter Verwenden des Ausgabeschutz-Managers.
ms.assetid: 01edc17e-e71c-4772-a03c-09c9a2b8400f
title: Verwenden des Ausgabeschutz-Managers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73e37dd548603a6f9d7769a9e724df3477e2fcde
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122475516"
---
# <a name="using-output-protection-manager"></a>Verwenden des Ausgabeschutz-Managers

In diesem Thema wird beschrieben, wie Sie den Ausgabeschutz-Manager (Output Protection Manager, OPM) verwenden, um Videoinhalte zu schützen, während sie über einen physischen Connector zu einem Anzeigegerät übertragen werden. Dieses Thema enthält folgende Abschnitte:

-   [Videoausgaben](#video-outputs)
-   [Initialisieren einer OPM-Sitzung](#initializing-an-opm-session)
-   [Senden von OPM-Statusanforderungen](#sending-opm-status-requests)
-   [Senden von OPM-Befehlen](#sending-opm-commands)
-   [Verarbeiten einer deaktivierten Videoausgabe](#sending-opm-commands)
-   [Verwenden von HDCP zum Schützen von Inhalten](#using-hdcp-to-protect-content)

Premium Videoinhalte werden in der Regel verschlüsselt, um sie vor nicht autorisierter Duplizierung zu schützen. Natürlich muss das Video entschlüsselt werden, bevor es angezeigt wird. Die entschlüsselten, unkomprimierten Frames müssen dann über einen physischen Connector zum Anzeigegerät übertragen werden. Inhaltsanbieter erfordern möglicherweise, dass die Videoframes an diesem Punkt geschützt werden, da sie über den physischen Connector gelangen.

Zu diesem Zweck gibt es verschiedene Schutzmechanismen, einschließlich High-Bandwidth Digital Content Protection (HDCP) und DisplayPort Content Protection (DPCP) für digitale Ausgaben. und Copy Generation Management System – Analog (CGMS-A) für analoge Ausgaben. Im Allgemeinen umfassen diese Mechanismen das Verschlüsseln oder Scrambling des Signals, bevor es zur Anzeige wechselt.

OPM ermöglicht einer Anwendung, Inhaltsschutzmechanismen für die Videoausgabe zu erzwingen. Mit OPM sendet die Anwendung Befehle und Statusanforderungen über einen vertrauenswürdigen, sicheren Kanal an den Grafiktreiber. OPM ermöglicht einer Anwendung:

-   Überprüfen Sie, ob ein Grafiktreiber von Microsoft signiert wurde.
-   Richten Sie einen vertrauenswürdigen Kommunikationskanal mit dem Treiber ein.
-   Erzwingen Sie Mechanismen zum Schutz von Inhalten für die physische Ausgabe.

OPM ersetzt Certified Output Protection Protcol (COPP) und verwendet eine ähnliche API. Aus Gründen der Abwärtskompatibilität kann die OPM-Schnittstelle die COPP-Schnittstelle emulieren. Die Unterschiede zwischen OPM und COPP umfassen Folgendes:

-   OPM verwendet X.509-Zertifikate, während COPP ein proprietäres Zertifikatformat verwendet.
-   OPM unterstützt HDCP-Repeater.
-   Anwendungen, die OPM verwenden, müssen HDCP-Systemerneuerbarkeitsmeldungen (SRMs) nicht analysieren.
-   OPM kann verwendet werden, wenn die Grafikanzeige den Klonmodus verwendet. COPP unterstützt den Klonmodus nicht.

Wenn Ihre Anwendung den Pfad für geschützte Medien (Protected Media Path, PMP) zum Wiedergeben von Videoinhalten verwendet, müssen Sie nicht die OPM-API verwenden, da der PMP alle erforderlichen OPM-Aufrufe vornimmt. Die OPM-API ist für Anwendungen verfügbar, die PMP nicht verwenden.

OPM ist in Windows Vista und höher verfügbar, aber die API wurde erst Windows 7 öffentlich gemacht. Um OPM in einer Anwendung verwenden zu können, benötigen Sie die Header und Bibliotheksdateien aus dem Windows 7 SDK. Sie müssen keine DLLs neu verteilen, um OPM in Windows Vista oder Windows Server 2008 zu verwenden.

## <a name="video-outputs"></a>Videoausgaben

Ein Grafikadapter kann mehrere physische Ausgaben mit jeweils eigenen Funktionen aufweisen. Bevor eine Anwendung geschützte Inhalte wiedergibt, muss sie die entsprechenden Schutzmechanismen für jede Videoausgabe festlegen, die der Grafikkarte zugeordnet ist, auf der das Video angezeigt wird. Welche Schutzmechanismen angewendet werden sollen, hängt von den Nutzungsregeln für den Inhalt ab.

Jede Videoausgabe wird durch eine Instanz der [**IOPMVideoOutput-Schnittstelle**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) dargestellt. Sie können ein Direct3D-Gerät oder Monitorhandles verwenden, um die Videoausgaben abzurufen.

Verwenden eines Direct3D-Geräts:

1.  Abrufen des **IDirect3DDevice9-Zeigers** für das Direct3D-Gerät, das ihre Anwendung zum Erstellen von Oberflächen zum Speichern der Videoframes verwendet.
2.  Rufen Sie die [**OPMGetVideoOutputsFromIDirect3DDevice9Object-Funktion**](/windows/desktop/api/opmapi/nf-opmapi-opmgetvideooutputsfromidirect3ddevice9object) auf. Diese Funktion ordnet ein Array von [**IOPMVideoOutput-Zeigern**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) zu, eines für jede Ausgabe.

Verwenden von Monitorhandles:

1.  Rufen Sie **EnumDisplayMonitors** auf, um die **HMONITOR-Handles** abzurufen, die dem Videofenster entsprechen. Mehrere Monitore können demselben Fenster zugeordnet werden, sodass Sie möglicherweise mehrere **HMONITOR-Handles** erhalten.
2.  Rufen Sie für jedes Monitorhandle [**OPMGetVideoOutputsFromHMONITOR**](/windows/desktop/api/opmapi/nf-opmapi-opmgetvideooutputsfromhmonitor)auf. Diese Funktion ordnet ein Array von [**IOPMVideoOutput-Zeigern**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) zu, eines für jede Ausgabe.

## <a name="initializing-an-opm-session"></a>Initialisieren einer OPM-Sitzung

Bevor die Anwendung OPM-Befehle oder Statusanforderungen sendet, muss sie überprüfen, ob die Videoausgabe vertrauenswürdig ist, und einen Sitzungsschlüssel einrichten. Der Sitzungsschlüssel wird verwendet, um die Daten zu signieren, die zwischen der Anwendung und dem Grafiktreiber ausgetauscht werden.

Die OPM-API definiert einen Handshake, der eine Vertrauensstellung herstellt und den Sitzungsschlüssel festlegt. Sie müssen diesen Handshake für jede Instanz der [**IOPMVideoOutput-Schnittstelle**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) wie folgt ausführen:

1.  Rufen Sie [**IOPMVideoOutput::StartInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-startinitialization)auf. Diese Methode ruft zwei Datenteile ab:
    -   Eine vom Treiber generierte Zufallszahl. Sie verwenden diese Nummer, um den Handshake abzuschließen.
    -   Die X.509-Zertifikatkette des Treibers.
2.  Überprüfen Sie, ob die Zertifikatkette von Microsoft signiert wurde.
    > [!Note]  
    > Die Zertifikatsperrung liegt außerhalb des OPM-Bereichs.

     

3.  Abrufen des öffentlichen Schlüssels des Treibers aus der Zertifikatkette.
4.  Generieren Sie einen 128-Bit-AES-Sitzungsschlüssel.
5.  Generieren Sie zwei zufällige 32-Bit-Zahlen:

    -   Die Startsequenznummer für OPM-Statusanforderungen.
    -   Die Startsequenznummer für OPM-Befehle.

    Diese Zahlen müssen mithilfe eines kryptografisch sicheren Pseudozufallszahlengenerators wie **CryptGenRandom** generiert werden.

6.  Kopieren Sie die Zufallszahl des Treibers (abgerufen in Schritt 1), den Sitzungsschlüssel und die beiden Sequenznummern in eine [**OPM \_ ENCRYPTED \_ INITIALIZATION \_ PARAMETERS-Struktur,**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_encrypted_initialization_parameters) wie unter [**IOPMVideoOutput::FinishInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-finishinitialization)beschrieben.
7.  Verschlüsseln Sie die [**OPM \_ ENCRYPTED \_ INITIALIZATION \_ PARAMETERS-Struktur**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_encrypted_initialization_parameters) mit RSAES-OAEP unter Verwendung des öffentlichen Schlüssels des Treibers, der sich im Zertifikat des Treibers befindet.
8.  Rufen Sie [**IOPMVideoOutput::FinishInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-finishinitialization)auf.

## <a name="sending-opm-status-requests"></a>Senden von OPM-Statusanforderungen

OPM-Statusanforderungen geben Informationen zur Videoausgabe zurück, z. B. den Typ des physischen Connectors und die aktuelle Schutzebene. Eine Liste der Anforderungstypen finden Sie unter [OPM-Statusanforderungen.](opm-status-requests.md)

Führen Sie die folgenden Schritte aus, um eine Statusanforderung zu senden.

1.  Initialisieren Sie eine [**OPM \_ GET INFO \_ \_ PARAMETERS-Struktur,**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters) wie in der folgenden Tabelle gezeigt.

    | Member               | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                 |
    |----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | **omac**             | Überspringen Sie dieses Feld vorerst.                                                                                                                                                                                                                                                                                                                                                    |
    | **rnRandomNumber**   | Eine kryptografisch sichere 128-Bit-Zufallszahl. Wenn Sie eine Statusanforderung stellen, generieren Sie immer eine neue Zufallszahl, auch wenn Sie dieselbe Anforderung stellen. Store die Zahl in einer Variablen, da Sie später darauf verweisen müssen.                                                                                                                             |
    | **guidInformation**  | Eine GUID, die die Statusanforderung identifiziert. Eine Liste der Statusanforderungen finden Sie unter [OPM-Statusanforderungen.](opm-status-requests.md)                                                                                                                                                                                                                                               |
    | **ulSequenceNumber** | Die Sequenznummer. Verwenden Sie für die erste Statusanforderung die Startsequenznummer, die Sie in der [**IOPMVideoOutput::FinishInitialization-Methode**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-finishinitialization) angegeben haben (Schritt 5 der [Initialisierung einer OPM-Sitzung](#initializing-an-opm-session)). Jedes Mal, wenn Sie eine weitere Statusanforderung stellen, erhöhen Sie diese Zahl um 1. |
    | **abParameters**     | Ein Bytearray, das zusätzliche Eingabedaten für die Anforderung enthält. Das Format der Eingabedaten ist im Referenzthema für jede Statusanforderung aufgeführt.                                                                                                                                                                                                                    |
    | **cbParametersSize** | Die Größe der gültigen Daten im **abParameters-Array.** Der Inhalt des restlichen Arrays ist nicht definiert.                                                                                                                                                                                                                                                              |

    

     

2.  Berechnen Sie den CBC-MAC mit einer Taste (OMAC-1), um einen Hash für den Datenblock zu berechnen, der nach dem **omac-Element** angezeigt wird, und legen Sie dann das **omac-Element** auf diesen Wert fest. Siehe [OPM-Beispielcode.](opm-example-code.md)
3.  Rufen Sie die [**IOPMVideoOutput::GetInformation-Methode**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) auf. Übergeben Sie einen Zeiger auf die [**OPM \_ GET INFO \_ \_ PARAMETERS-Struktur**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters) und einen Zeiger auf eine [**OPM REQUESTED \_ \_ INFORMATION-Struktur.**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_requested_information) Die Antwort des Treibers wird in die **OPM \_ REQUESTED \_ INFORMATION-Struktur** geschrieben.
    -   Der **omac-Member** dieser Struktur enthält einen OMAC, der für die Daten berechnet wird, die diesem Member folgen.
    -   Der **abRequestedInformation-Member** ist ein Bytearray, das Ausgabedaten für die Antwort enthält. Das Format der Ausgabedaten ist im Referenzthema für jede Statusanforderung aufgeführt.
4.  Berechnen Sie einen OMAC für die [**OPM \_ REQUESTED \_ INFORMATION-Struktur,**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_requested_information) ohne das **omac-Element.** Überprüfen Sie, ob der OMAC mit dem Wert im **omac-Element** übereinstimmt.
5.  Stellen Sie sicher, dass der **cbRequestedInformationSize-Member** der [**OPM \_ REQUESTED \_ INFORMATION-Struktur**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_requested_information) die richtige Größe für die Ausgabedaten angibt. Beispielsweise sind die Ausgabedaten für die [**OPM \_ GET CONNECTOR \_ \_ TYPE-Abfrage**](opm-get-connector-type.md) eine [**OPM STANDARD \_ \_ INFORMATION-Struktur,**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) daher sollte der Wert von **cbRequestedInformationSize** `sizeof(OPM_STANDARD_INFORMATION)` sein.
6.  Cast the abRequestedInformation member of the OPM REQUESTED INFORMATION structure to the correct output data structure. (Umwandlung des **abRequestedInformation-Elements** der [**OPM \_ REQUESTED \_ INFORMATION-Struktur**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_requested_information) in die richtige Ausgabedatenstruktur. Wenn die Statusanforderung beispielsweise [**OPM \_ GET CONNECTOR \_ \_ TYPE**](opm-get-connector-type.md)lautet, wird **abRequestedInformation** in eine [**OPM STANDARD \_ \_ INFORMATION-Struktur**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) umgecastet.
7.  Stellen Sie sicher, dass der **rnRandomNumber-Member** der Ausgabedatenstruktur mit dem Wert von **rnRandomNumber** aus Schritt 1 übereinstimmt.
8.  Überprüfen Sie den **ulStatusFlags-Member** der Ausgabedatenstruktur, wie unter [Behandeln einer deaktivierten Videoausgabe](#handling-a-disabled-video-output)beschrieben.

Wenn eine der Überprüfungen in den Schritten 5 bis 8 fehlschlägt, muss die Anwendung keine geschützten Inhalte mehr anzeigen.

## <a name="sending-opm-commands"></a>Senden von OPM-Befehlen

OPM-Befehle werden verwendet, um die Schutzebene und andere Einstellungen für die Videoausgabe festzulegen. Das Senden eines OPM-Befehls ähnelt dem Senden einer Statusanforderung, mit der Ausnahme, dass keine Antwortdaten vom Treiber vorhanden sind. Eine Liste der Befehle finden Sie unter [OPM-Befehle.](opm-commands.md)

Führen Sie die folgenden Schritte aus, um einen OPM-Befehl zu senden.

1.  Füllen Sie eine [**OPM \_ CONFIGURE \_ PARAMETERS-Struktur**](/windows/desktop/api/opmapi/ns-opmapi-opm_configure_parameters) aus, wie in der folgenden Tabelle dargestellt.

    | Member                | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                   |
    |-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | **omac**              | Überspringen Sie dieses Feld vorerst.                                                                                                                                                                                                                                                                                                                                      |
    | **guidSetting**       | Eine GUID, die den Befehl identifiziert. Eine Liste der Befehle finden Sie unter [OPM-Befehle.](opm-commands.md)                                                                                                                                                                                                                                                             |
    | **ulSequenceNumber**  | Die Sequenznummer. Verwenden Sie für den ersten Befehl die Startsequenznummer, die Sie in der [**IOPMVideoOutput::FinishInitialization-Methode**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-finishinitialization) angegeben haben (Schritt 5 der [Initialisierung einer OPM-Sitzung](#initializing-an-opm-session)). Jedes Mal, wenn Sie einen anderen Befehl senden, erhöhen Sie diese Zahl um 1. |
    | **abParameters**      | Ein Bytearray, das zusätzliche Eingabedaten für den Befehl enthält. Das Format der Eingabedaten ist im Referenzthema für jeden Befehl aufgeführt.                                                                                                                                                                                                             |
    | **cbSettingDataSize** | Die Größe der gültigen Daten im **abParameters-Array.** Der Inhalt des restlichen Arrays ist nicht definiert.                                                                                                                                                                                                                                                |

    

     

2.  Berechnen Sie einen OMAC für den Datenblock, der nach dem **omac-Element** angezeigt wird, und legen Sie dann das **omac-Element** auf diesen Wert fest.
3.  Rufen Sie [**IOPMVideoOutput::Configure auf.**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure)

Für die meisten Befehle gibt es eine entsprechende Statusanforderung, die den Status des Befehls zurückgibt. Beispielsweise legt der Befehl [**OPM \_ SET PROTECTION \_ \_ LEVEL**](opm-set-protection-level.md) die Schutzebene fest, und der Befehl [**OPM GET VIRTUAL PROTECTION \_ \_ \_ \_ LEVEL**](opm-get-virtual-protection-level.md) ruft die aktuelle Schutzebene ab.

## <a name="handling-a-disabled-video-output"></a>Verarbeiten einer deaktivierten Videoausgabe

Eine Videoausgabe kann sich jederzeit selbst deaktivieren, um die unbefugte Verwendung von Videoinhalten zu verhindern. Dies kann auftreten, weil ein Schutzmechanismus nicht mehr funktioniert, weil der Treiber Manipulationen erkennt oder weil die Anzeige vom physischen Connector getrennt wurde. Während eine Videoausgabe deaktiviert ist, werden keine Videoframes angezeigt.

Während der Inhaltsschutz aktiviert ist, sollte eine Anwendung in regelmäßigen Abständen (mindestens einmal alle 2 Sekunden) die folgenden Schritte ausführen.

1.  Rufen Sie [**IOPMVideoOutput::GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) auf, um entweder die Statusanforderung [**OPM \_ GET ACTUAL PROTECTION \_ \_ \_ LEVEL**](opm-get-actual-protection-level.md) oder [**OPM GET VIRTUAL PROTECTION \_ \_ \_ \_ LEVEL**](opm-get-virtual-protection-level.md) zu senden. Die Rückgabedaten für beide Befehle sind eine [**OPM \_ STANDARD \_ INFORMATION-Struktur.**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information)
2.  Überprüfen Sie den **ulInformation-Member** der [**OPM \_ STANDARD \_ INFORMATION-Struktur.**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) Dieser Member enthält ein Flag, das angibt, ob der Inhaltsschutz noch aktiviert ist. Wenn der Inhaltsschutz deaktiviert ist, beenden Sie die Wiedergabe des Videos sofort.
3.  Wenn der Inhaltsschutz aktiviert ist, überprüfen Sie den **ulStatusFlags-Member** der [**OPM \_ STANDARD \_ INFORMATION-Struktur.**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) Wenn keine Flags festgelegt sind, funktioniert die Videoausgabe ordnungsgemäß. Andernfalls ist die Videoausgabe deaktiviert.

Die folgenden Flags sind für **ulStatusFlags** definiert.




| Flag | Beschreibung | 
|------|-------------|
| <strong>OPM_STATUS_LINK_LOST</strong> | Der Ausgabeschutz funktioniert aus irgendeinem Grund nicht mehr. Beispielsweise kann das Anzeigegerät vom Konntector entfernt werden. Beenden Sie die Wiedergabe, und deaktivieren Sie alle Ausgabeschutzmechanismen. | 
| <strong>OPM_STATUS_RENEGOTIATION_REQUIRED</strong> | Die Anwendung muss die OPM-Sitzung wiederherstellen. Reagieren Sie wie folgt:<ol><li>Beenden Sie die Wiedergabe.</li><li>Deaktivieren Sie alle Schutzmechanismen.</li><li>Geben Sie die <a href="/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput"><strong>IOPMVideoOutput-Schnittstelle</strong></a> frei.</li><li>Erstellen Sie alle Videooberflächen neu.</li><li>Erstellen Sie ein neues OPM-Objekt, und versuchen Sie, den Inhaltsschutz wiederherzustellen. Wenn dies fehlschlägt, zeigen Sie dem Benutzer eine Fehlermeldung an. Geben Sie keine weiteren Videoinhalte wieder.</li></ol> | 
| <strong>OPM_STATUS_REVOKED_HDCP_DEVICE_ATTACHED</strong> | Dieses Flag gilt nur, wenn HDCP verwendet wird, und gibt an, dass ein gesperrtes HDCP-Gerät vorhanden ist. Beenden Sie die Wiedergabe, und deaktivieren Sie alle Schutzmechanismen für diese Videoausgabe. Wenn dieses Flag festgelegt ist, wird auch das <strong>OPM_STATUS_LINK_LOST-Flag</strong> festgelegt. | 
| <strong>OPM_STATUS_REVOKED_HDCP_DEVICE_ATTACHED</strong> | Der Treiber hat Manipulationen erkannt. Beenden Sie die Wiedergabe, und geben Sie keine weiteren Videos mithilfe dieser Videoausgabe wieder. Es empfiehlt sich auch, keine anderen Videoausgaben mehr zu verwenden, da das System möglicherweise kompromittiert ist. | 




 

## <a name="using-hdcp-to-protect-content"></a>Verwenden von HDCP zum Schützen von Inhalten

In diesem Abschnitt wird beschrieben, wie Sie den HDCP-Ausgabeschutz mit OPM aktivieren. Im Folgenden finden Sie eine allgemeine Übersicht über die Schritte, die die Anwendung ausführen muss. Details finden Sie weiter unten in diesem Abschnitt.

1.  Die Anwendung muss möglicherweise einen SRM für die Videoausgabe bereitstellen. Der Mechanismus zum Empfangen von SRMs liegt außerhalb des Bereichs der OPM-Schnittstelle. Beispielsweise können SRMs als Teil eines Broadcaststreams übermittelt werden.
2.  Die Anwendung aktiviert den HDCP-Ausgabeschutz.
3.  Die Anwendung gibt den Videoinhalt wieder. In regelmäßigen Abständen fragt die Anwendung den Treiber ab, um sicherzustellen, dass HDCP eingeschaltet ist.
4.  Wenn die Wiedergabe abgeschlossen ist, deaktiviert die Anwendung HDCP.

### <a name="setting-the-srm"></a>Festlegen des SRM

Führen Sie die folgenden Schritte aus, um den SRM festzulegen.

1.  Initialisieren Sie eine [**OPM \_ SET \_ HDCP \_ SRM \_ PARAMETERS-Struktur**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_hdcp_srm_parameters) mit der SRM-Versionsnummer.
2.  Store den SRM in einer Variablen.
3.  Senden Sie einen [**OPM \_ SET \_ HDCP \_ SRM-Befehl**](opm-set-hdcp-srm.md) an die Videoausgabe. Verwenden Sie das unter [Senden von OPM-Befehlen beschriebene](#sending-opm-commands)Verfahren.
    -   Der **abParameters-Member** der [**OPM \_ CONFIGURE \_ PARAMETERS-Struktur**](/windows/desktop/api/opmapi/ns-opmapi-opm_configure_parameters) enthält die [**OPM SET \_ \_ HDCP \_ SRM \_ PARAMETERS-Struktur.**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_hdcp_srm_parameters)
    -   Der *pbAdditionalParameters-Parameter* der [**IOPMVideoOutput::Configure-Methode**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure) verweist auf die Variable, die den SRM enthält.
4.  Senden Einer [**OPM \_ GET CURRENT \_ \_ HDCP \_ SRM \_ VERSION-Statusanforderung**](opm-get-current-hdcp-srm-version.md) an die Videoausgabe. Verwenden Sie das unter [Senden von OPM-Statusanforderungen beschriebene](#sending-opm-status-requests)Verfahren. Diese Statusanforderung enthält keine Eingabedaten, sodass der Inhalt des **abParameters-Members** der [**OPM \_ GET INFO \_ \_ PARAMETERS-Struktur**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters) nicht definiert ist.
5.  Wenn die [**IOPMVideoOutput::GetInformation-Methode**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) zurückgegeben wird, enthält das **abRequestedInformation-Array** in der [**OPM \_ REQUESTED \_ INFORMATION-Struktur**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_requested_information) eine [**OPM \_ STANDARD \_ INFORMATION-Struktur.**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) Der **ulInformation-Member** dieser Struktur enthält die Versionsnummer des aktuellen SRM. Dieser Wert muss dem Wert aus Schritt 2 entsprechen.

### <a name="enabling-hdcp"></a>Aktivieren von HDCP

Führen Sie die folgenden Schritte aus, um HDCP zu aktivieren.

1.  Initialisieren Sie eine [**OPM \_ SET PROTECTION \_ LEVEL \_ \_ PARAMETERS-Struktur**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_protection_level_parameters) mit den folgenden Werten:
    -   **ulProtectionType**  =  **OPM \_ SCHUTZTYP \_ \_ HDCP**
    -   **ulProtectionLevel**  =  **OPM \_ HDCP \_ ON**
    -   **Reserviert** = 0
    -   **Reserviert2** = 0
2.  Senden Sie einen [**OPM \_ SET PROTECTION \_ \_ LEVEL-Befehl.**](opm-set-protection-level.md) Die Eingabedaten im **abParameters-Array** sind die [**OPM \_ SET PROTECTION \_ LEVEL \_ \_ PARAMETERS-Struktur.**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_protection_level_parameters)
3.  Senden Sie eine [**OPM \_ GET VIRTUAL \_ PROTECTION \_ LEVEL-Statusanforderung, \_**](opm-get-virtual-protection-level.md) um zu überprüfen, ob HDCP aktiviert ist. Die ersten 4 Bytes des **abParameters-Members** der [**OPM \_ GET INFO \_ \_ PARAMETERS-Struktur**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters) enthalten den Wert **OPM PROTECTION TYPE \_ \_ \_ HDCP**.

Wenn die [**GetInformation-Methode**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) zurückgegeben wird, enthält das **abRequestedInformation-Array** in der [**OPM \_ REQUESTED \_ INFORMATION-Struktur**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_requested_information) eine [**OPM \_ STANDARD \_ INFORMATION-Struktur.**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) Der **ulInformation-Member** dieser Struktur enthält einen Wert aus der [**OPM \_ HDCP \_ PROTECTION \_ LEVEL-Enumeration.**](/windows/desktop/api/opmapi/ne-opmapi-opm_hdcp_protection_level) Wenn der Wert **OPM \_ HDCP \_ ON** entspricht, bedeutet dies, dass HDCP aktiviert ist. Wiederholen Sie andernfalls die Schritte 1 bis 2, bis HDCP aktiviert ist oder ein Fehler auftritt. (Denken Sie daran, die Sequenznummer zu erhöhen und jedes Mal eine neue Zufallszahl zu generieren.)

Die Aktivierung von HDCP dauert in der Regel zwischen 100 und 200 Millisekunden, kann aber länger dauern. Gehen Sie nicht davon aus, dass HDCP aktiviert ist, bis Sie es überprüft haben.

Wenn die Anwendung die Wiedergabe geschützter Inhalte beendet hat, deaktivieren Sie HDCP. Die Schritte sind identisch mit dem zum Aktivieren von HDCP, aber legen Sie in Schritt 1 **ulProtectionLevel** auf **OPM \_ HDCP \_ OFF fest.**

> [!Note]  
> Aktivieren Sie HDCP nicht, wenn der Connectortyp **OPM \_ CONNECTOR TYPE \_ \_ DISPLAYPORT \_ EMBEDDED** ist. (Siehe [**OPM-Connectortypflags.)**](opm-connector-type-flags.md)

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ausgabeschutz-Manager](output-protection-manager.md)
</dt> </dl>

 

 



