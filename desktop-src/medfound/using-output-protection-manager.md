---
description: 'Weitere Informationen finden Sie unter: Verwenden von Output Protection Manager'
ms.assetid: 01edc17e-e71c-4772-a03c-09c9a2b8400f
title: Verwenden von Output Protection Manager
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57bf4def3b0575dd706ae5f0c62924b6f1375a05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345862"
---
# <a name="using-output-protection-manager"></a>Verwenden von Output Protection Manager

In diesem Thema wird beschrieben, wie Sie mit dem Output Protection Manager (OPM) Videoinhalte während der Übertragung über einen physischen Connector zu einem Anzeigegerät schützen. Dieses Thema enthält folgende Abschnitte:

-   [Video Ausgaben](#video-outputs)
-   [Initialisieren einer OPM-Sitzung](#initializing-an-opm-session)
-   [Senden von OPM-Status Anforderungen](#sending-opm-status-requests)
-   [Senden von OPM-Befehlen](#sending-opm-commands)
-   [Behandeln einer deaktivierten Video Ausgabe](#sending-opm-commands)
-   [Verwenden von HDCP zum Schützen von Inhalten](#using-hdcp-to-protect-content)

Premium-Videoinhalte werden normalerweise verschlüsselt, um Sie vor unbefugter Duplizierung zu schützen. Natürlich muss das Video entschlüsselt werden, bevor es angezeigt wird. Die entschlüsselten, nicht komprimierten Frames müssen dann über einen physischen Connector auf das Anzeigegerät übertragen werden. Bei Inhaltsanbietern ist es möglicherweise erforderlich, dass die Videorahmen an dieser Stelle geschützt werden, da Sie über den physischen Connector übertragen werden.

Zu diesem Zweck gibt es verschiedene Schutzmechanismen, einschließlich High-Bandwidth Digital Content Protection (HDCP) und DisplayPort Content Protection (dpcp) für digitale Ausgaben. und Copy Generation Management System-Analog (CGMS-A) für analoge Ausgaben. Diese Mechanismen beinhalten in der Regel das Verschlüsseln oder stören des Signals, das Sie an die Anzeige weitergibt.

OPM ermöglicht es einer Anwendung, Inhalts Schutzmechanismen für die Videoausgabe zu erzwingen. Mithilfe von OPM sendet die Anwendung Befehle und Status Anforderungen an den Grafiktreiber über einen vertrauenswürdigen, sicheren Kanal. OPM ermöglicht einer Anwendung Folgendes:

-   Überprüfen Sie, ob ein Grafiktreiber von Microsoft signiert wurde.
-   Richten Sie einen vertrauenswürdigen Kommunikationskanal mit dem Treiber ein.
-   Erzwingen von Mechanismen zum Schutz von Inhalten für die physische Ausgabe.

OPM ersetzt den zertifizierten Ausgabe Schutz-Protcol (COPP) und verwendet eine ähnliche API. Aus Gründen der Abwärtskompatibilität kann die OPM-Schnittstelle die COPP-Schnittstelle emulieren. Die Unterschiede zwischen OPM und COPP umfassen Folgendes:

-   OPM verwendet X. 509-Zertifikate, während COPP ein proprietäres Zertifikat Format verwendet.
-   OPM unterstützt HDCP-Repeater.
-   Anwendungen, die OPM verwenden, müssen keine HDCP-systemerneuungsopbarkeits-Meldungen (SRMs) analysieren.
-   OPM kann verwendet werden, wenn in der Grafik Anzeige der Klon Modus verwendet wird. Der Klon Modus wird von COPP nicht unterstützt.

Wenn Ihre Anwendung den geschützten Medien Pfad (PMP) zum Wiedergeben von Videoinhalten verwendet, müssen Sie die OPM-API nicht verwenden, da das PMP alle erforderlichen OPM-Aufrufe ausführt. Die OPM-API ist für Anwendungen verfügbar, die das PMP nicht verwenden.

OPM ist in Windows Vista und höher verfügbar, aber die API wurde bis Windows 7 nicht öffentlich gemacht. Um OPM in einer Anwendung verwenden zu können, müssen Sie über die Header-und Bibliotheksdateien aus dem Windows 7 SDK verfügen. Sie müssen keine DLLs neu verteilen, um OPM in Windows Vista oder Windows Server 2008 zu verwenden.

## <a name="video-outputs"></a>Video Ausgaben

Ein Grafikadapter kann über mehrere physische Ausgaben verfügen, die jeweils über eigene Funktionen verfügen. Bevor eine Anwendung geschützte Inhalte wieder gibt, muss Sie die entsprechenden Schutzmechanismen für jede Videoausgabe festlegen, die der Grafikkarte zugeordnet ist, auf der das Video angezeigt wird. Welche Schutzmechanismen angewendet werden sollen, hängt von den Verwendungs Regeln für den Inhalt ab.

Jede Videoausgabe wird durch eine Instanz der [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) -Schnittstelle dargestellt. Sie können ein Direct3D-Gerät oder Monitor Handles verwenden, um die Video Ausgaben zu erhalten.

Verwenden eines Direct3D-Geräts:

1.  Rufen Sie den **IDirect3DDevice9** -Zeiger für das Direct3D-Gerät ab, das Ihre Anwendung zum Erstellen von Oberflächen zum Speichern der Videorahmen verwendet.
2.  Ruft die [**OPMGetVideoOutputsFromIDirect3DDevice9Object**](/windows/desktop/api/opmapi/nf-opmapi-opmgetvideooutputsfromidirect3ddevice9object) -Funktion auf. Diese Funktion weist ein Array von [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) -Zeigern zu, eines für jede Ausgabe.

Verwenden von Monitor Handles:

1.  Geben Sie " **enumdisplaymonitors** " an, um die **Hmonitor** -Handles abzurufen, die dem Videofenster entsprechen. Dem gleichen Fenster können mehrere Monitore zugeordnet werden, sodass Sie möglicherweise mehrere **Hmonitor** -Handles erhalten.
2.  Aufrufen Sie für jedes Monitor Handle [**opmgetvideooutputsfromhmonitor**](/windows/desktop/api/opmapi/nf-opmapi-opmgetvideooutputsfromhmonitor). Diese Funktion weist ein Array von [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) -Zeigern zu, eines für jede Ausgabe.

## <a name="initializing-an-opm-session"></a>Initialisieren einer OPM-Sitzung

Bevor die Anwendung OPM-Befehle oder-Status Anforderungen sendet, muss Sie überprüfen, ob die Videoausgabe vertrauenswürdig ist, und einen Sitzungsschlüssel einrichten. Der Sitzungsschlüssel wird verwendet, um die zwischen der Anwendung und dem Grafiktreiber ausgetauschten Daten zu signieren.

Die OPM-API definiert einen Handshake, der Vertrauens Stellungen herstellt und den Sitzungsschlüssel festlegt. Sie müssen diesen Handshake für jede Instanz der [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) -Schnittstelle wie folgt ausführen:

1.  Aufrufen von [**IOPMVideoOutput:: startinitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-startinitialization). Diese Methode ruft zwei Datenelemente ab:
    -   Eine Zufallszahl, die vom Treiber generiert wurde. Sie verwenden diese Zahl, um den Handshake abzuschließen.
    -   Die X. 509-Zertifikat Kette des Treibers.
2.  Überprüfen Sie, ob die Zertifikat Kette von Microsoft signiert wurde.
    > [!Note]  
    > Die Zertifikat Sperrung liegt außerhalb des Gültigkeits Bereichs von OPM.

     

3.  Den öffentlichen Schlüssel des Treibers aus der Zertifikat Kette erhalten.
4.  Generieren Sie einen 128-Bit-AES-Sitzungsschlüssel.
5.  Generieren Sie zwei zufällige 32-Bit-Zahlen:

    -   Die Startsequenz Nummer für OPM-Status Anforderungen.
    -   Die Startsequenz Nummer für OPM-Befehle.

    Diese Zahlen müssen mithilfe eines kryptografisch sicheren Pseudozufallszahlen-Generators generiert werden, z. **b. cryptgenrandom**.

6.  Kopieren Sie die zufällige Nummer des Treibers (abgerufen in Schritt 1), den Sitzungsschlüssel und die beiden Sequenznummern in eine [**OPM- \_ verschlüsselte \_ Initialisierungs \_ Parameter**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_encrypted_initialization_parameters) -Struktur, wie in [**IOPMVideoOutput:: FinishInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-finishinitialization)beschrieben.
7.  Verschlüsseln Sie die Struktur der [**verschlüsselten OPM- \_ \_ Initialisierungs \_ Parameter**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_encrypted_initialization_parameters) mit rsaes-OAEP. verwenden Sie dazu den öffentlichen Schlüssel des Treibers, der im Zertifikat des Treibers enthalten ist.
8.  Aufrufen von [**IOPMVideoOutput:: FinishInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-finishinitialization).

## <a name="sending-opm-status-requests"></a>Senden von OPM-Status Anforderungen

OPM-Status Anforderungen geben Informationen über die Videoausgabe zurück, z. b. den Typ des physischen Connector und die aktuelle Schutz Ebene. Eine Liste der Anforderungs Typen finden Sie unter [OPM-Status Anforderungen](opm-status-requests.md).

Führen Sie die folgenden Schritte aus, um eine Status Anforderung zu senden.

1.  Initialisieren [**Sie eine OPM-Struktur \_ get \_ Info \_ Parameters**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters) , wie in der folgenden Tabelle gezeigt.

    | Member               | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                 |
    |----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | **OMAC**             | Dieses Feld jetzt überspringen.                                                                                                                                                                                                                                                                                                                                                    |
    | **rnrandomnumber**   | Eine kryptografisch sichere 128-Bit-Zufallszahl. Wenn Sie eine Status Anforderung erstellen, generieren Sie immer eine neue Zufallszahl, auch wenn Sie dieselbe Anforderung vornehmen. Speichern Sie die Nummer in einer Variablen, da Sie später darauf verweisen müssen.                                                                                                                             |
    | **guidinformation**  | Eine GUID, die die Status Anforderung identifiziert. Eine Liste der Status Anforderungen finden Sie unter [OPM-Status Anforderungen](opm-status-requests.md).                                                                                                                                                                                                                                               |
    | **ulsequencenumschlag** | Die Sequenznummer. Verwenden Sie für die erste Status Anforderung die Startsequenz Nummer, die Sie in der [**IOPMVideoOutput:: FinishInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-finishinitialization) -Methode angegeben haben (Schritt 5 der [Initialisierung einer OPM-Sitzung](#initializing-an-opm-session)). Jedes Mal, wenn Sie eine weitere Status Anforderung vornehmen, erhöhen Sie diese Zahl um 1. |
    | **abparameters**     | Ein Bytearray, das zusätzliche Eingabedaten für die Anforderung enthält. Das Format der Eingabedaten wird im Referenz Thema für jede Status Anforderung aufgeführt.                                                                                                                                                                                                                    |
    | **cbparameterssize** | Die Größe der gültigen Daten im **abparameters** -Array. Der Inhalt des restlichen Arrays ist nicht definiert.                                                                                                                                                                                                                                                              |

    

     

2.  Berechnen Sie den One-Key-CBC-MAC (OMAC-1), um einen Hash für den Datenblock zu berechnen, der nach dem **OMAC** -Member angezeigt wird, und legen Sie dann den **OMAC** -Member auf diesen Wert fest. Siehe [OPM-Beispiel Code](opm-example-code.md).
3.  Aufrufen der [**IOPMVideoOutput:: GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) -Methode. Übergibt einen Zeiger auf die [**OPM-Struktur \_ get \_ Info \_ Parameters**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters) und einen Zeiger auf eine von [**OPM \_ angeforderte \_ Informations**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_requested_information) Struktur. Die Antwort des Treibers wird in die von **OPM \_ angeforderte \_ Informations** Struktur geschrieben.
    -   Der **OMAC** -Member dieser Struktur enthält eine OMAC, die für die Daten berechnet wird, die diesem Element folgen.
    -   Der **abrequestedinformation** -Member ist ein Bytearray, das Ausgabedaten für die Antwort enthält. Das Format der Ausgabedaten wird im Referenz Thema für jede Status Anforderung aufgeführt.
4.  Berechnen eines OMAC für die von [**OPM \_ angeforderte \_ Informations**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_requested_information) Struktur, ohne den **OMAC** -Member. Vergewissern Sie sich, dass der OMAC mit dem Wert im **OMAC** -Member übereinstimmt.
5.  Stellen Sie sicher, dass der **cbrequestedinformationsize** -Member der von [**OPM \_ angeforderten \_ Informations**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_requested_information) Struktur die richtige Größe für die Ausgabedaten liefert. Beispielsweise handelt es sich bei den Ausgabedaten für die OPM-Abfrage " [**\_ get \_ Connector \_ Type**](opm-get-connector-type.md) " um eine [**OPM- \_ Standard \_ Informations**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) Struktur, daher sollte der Wert von " **cbrequestedinformationsize** " lauten `sizeof(OPM_STANDARD_INFORMATION)` .
6.  Wandeln Sie den **abrequestedinformation** -Member der von [**OPM \_ angeforderten \_ Informations**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_requested_information) Struktur in die richtige Ausgabedaten Struktur um. Wenn die Status Anforderung beispielsweise [**OPM \_ get \_ Connector \_ Type**](opm-get-connector-type.md)lautet, wandeln Sie **abrequestedinformation** in eine [**OPM- \_ Standard \_ Informations**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) Struktur um.
7.  Stellen Sie sicher, dass der **rnrandomnumber** -Member der Ausgabedaten Struktur mit dem Wert von **rnrandomnumber** aus Schritt 1 übereinstimmt.
8.  Überprüfen Sie den **ulstaturflags** -Member der Ausgabedaten Struktur, wie unter [Behandeln einer deaktivierten Video Ausgabe](#handling-a-disabled-video-output)beschrieben.

Wenn eine der Überprüfungen in den Schritten 5 – 8 fehlschlägt, muss die Anwendung den geschützten Inhalt nicht mehr angezeigt werden.

## <a name="sending-opm-commands"></a>Senden von OPM-Befehlen

OPM-Befehle werden verwendet, um die Schutz Ebene und andere Einstellungen für die Videoausgabe festzulegen. Das Senden eines OPM-Befehls ähnelt dem Senden einer Status Anforderung, mit dem Unterschied, dass keine Antwortdaten vom Treiber vorhanden sind. Eine Liste der Befehle finden Sie unter [OPM-Befehle](opm-commands.md).

Führen Sie die folgenden Schritte aus, um einen OPM-Befehl zu senden.

1.  Füllen Sie die Struktur von [**OPM- \_ Konfigurations \_ Parametern**](/windows/desktop/api/opmapi/ns-opmapi-opm_configure_parameters) aus, wie in der folgenden Tabelle gezeigt.

    | Member                | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                   |
    |-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | **OMAC**              | Dieses Feld jetzt überspringen.                                                                                                                                                                                                                                                                                                                                      |
    | **guidsetting**       | Eine GUID, die den Befehl identifiziert. Eine Liste der Befehle finden Sie unter [OPM-Befehle](opm-commands.md).                                                                                                                                                                                                                                                             |
    | **ulsequencenumschlag**  | Die Sequenznummer. Verwenden Sie für den ersten Befehl die Startsequenz Nummer, die Sie in der [**IOPMVideoOutput:: FinishInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-finishinitialization) -Methode angegeben haben (Schritt 5 der [Initialisierung einer OPM-Sitzung](#initializing-an-opm-session)). Jedes Mal, wenn Sie einen anderen Befehl senden, erhöhen Sie diese Zahl um 1. |
    | **abparameters**      | Ein Bytearray, das zusätzliche Eingabedaten für den Befehl enthält. Das Format der Eingabedaten wird im Referenz Thema für jeden Befehl aufgeführt.                                                                                                                                                                                                             |
    | **cbsettingdatasize** | Die Größe der gültigen Daten im **abparameters** -Array. Der Inhalt des restlichen Arrays ist nicht definiert.                                                                                                                                                                                                                                                |

    

     

2.  Berechnen Sie eine OMAC für den Datenblock, der nach dem **OMAC** -Member angezeigt wird, und legen Sie dann den **OMAC** -Member auf diesen Wert fest.
3.  Nennen Sie [**IOPMVideoOutput:: Configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure).

Bei den meisten Befehlen gibt es eine entsprechende Status Anforderung, mit der der Status des Befehls zurückgegeben wird. Der [**OPM-Befehl \_ \_ Schutz \_ Ebene festlegen**](opm-set-protection-level.md) legt z. b. die Schutz Ebene fest, und der Befehl [**OPM \_ get \_ Virtual \_ Protection \_ Level**](opm-get-virtual-protection-level.md) Ruft die aktuelle Schutz Ebene ab.

## <a name="handling-a-disabled-video-output"></a>Behandeln einer deaktivierten Video Ausgabe

Eine Videoausgabe kann jederzeit deaktiviert werden, um die nicht autorisierte Verwendung von Videoinhalten zu verhindern. Dies kann der Fall sein, weil ein Schutzmechanismus nicht mehr funktioniert, da der Treiber Manipulationen erkennt oder die Anzeige vom physischen Connector getrennt wurde. Während eine Videoausgabe deaktiviert ist, werden keine Video Frames angezeigt.

Während der Inhalts Schutz aktiviert ist, sollte eine Anwendung in regelmäßigen Abständen (mindestens einmal alle zwei Sekunden) die folgenden Schritte ausführen.

1.  Wenden Sie [**IOPMVideoOutput:: GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) an, um entweder die Status Anforderung " [**\_ \_ tatsächliche \_ Schutz \_ Ebene**](opm-get-actual-protection-level.md) abrufen" oder " [**OPM \_ get \_ Virtual \_ Protection \_ Level**](opm-get-virtual-protection-level.md) " zu senden. Die Rückgabe Daten für beide Befehle sind eine [**OPM- \_ Standard \_ Informations**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) Struktur.
2.  Überprüfen Sie den **ulinformation** -Member der [**OPM- \_ Standard \_ Informations**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) Struktur. Dieser Member enthält ein Flag, das angibt, ob der Inhalts Schutz weiterhin aktiviert ist. Wenn Content Protection deaktiviert ist, beenden Sie die Wiedergabe des Videos sofort.
3.  Wenn der Inhalts Schutz auf on ist, überprüfen Sie den **ulstatus-Flags** -Member der [**OPM- \_ Standard \_ Informations**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) Struktur. Wenn keine Flags festgelegt sind, funktioniert die Videoausgabe ordnungsgemäß. Andernfalls ist die Videoausgabe deaktiviert.

Die folgenden Flags sind für **ulstatus-Flags** definiert.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Flag</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>OPM_STATUS_LINK_LOST</strong></td>
<td>Der Ausgabe Schutz ist aus irgendeinem Grund nicht mehr Funktions intensiv. Beispielsweise kann das Anzeigegerät nicht aus dem Verbindungs Modul entfernt werden. Beenden Sie die Wiedergabe, und deaktivieren Sie alle Mechanismen des Ausgabe Schutzes.</td>
</tr>
<tr class="even">
<td><strong>OPM_STATUS_RENEGOTIATION_REQUIRED</strong></td>
<td>Die Anwendung muss die OPM-Sitzung wiederherstellen. Antworten Sie wie folgt:
<ol>
<li>Wiedergabe wird beendet.</li>
<li>Deaktivieren Sie alle Schutzmechanismen.</li>
<li>Geben Sie die <a href="/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput"><strong>IOPMVideoOutput</strong></a> -Schnittstelle frei.</li>
<li>Erstellen Sie alle Video Oberflächen neu.</li>
<li>Erstellen Sie ein neues OPM-Objekt, und versuchen Sie, den Inhalts Schutz wiederherzustellen. Wenn dies nicht möglich ist, wird dem Benutzer eine Fehlermeldung angezeigt. Spielen Sie keine weiteren Videoinhalte.</li>
</ol></td>
</tr>
<tr class="odd">
<td><strong>OPM_STATUS_REVOKED_HDCP_DEVICE_ATTACHED</strong></td>
<td>Dieses Flag gilt nur, wenn HDCP verwendet wird, und gibt an, dass ein gesperrtes HDCP-Gerät vorhanden ist. Beenden Sie die Wiedergabe, und deaktivieren Sie alle Schutzmechanismen für diese Videoausgabe. Wenn dieses Flag festgelegt ist, wird auch das <strong>OPM_STATUS_LINK_LOST</strong> -Flag festgelegt.</td>
</tr>
<tr class="even">
<td><strong>OPM_STATUS_REVOKED_HDCP_DEVICE_ATTACHED</strong></td>
<td>Der Treiber hat Manipulationen erkannt. Die Wiedergabe wird beendet, und es werden keine weiteren Videos mit dieser Videoausgabe abgespielt. Es ist auch eine gute Idee, andere Video Ausgaben nicht zu verwenden, da das System möglicherweise kompromittiert ist.</td>
</tr>
</tbody>
</table>



 

## <a name="using-hdcp-to-protect-content"></a>Verwenden von HDCP zum Schützen von Inhalten

In diesem Abschnitt wird beschrieben, wie Sie den HDCP-Ausgabe Schutz mithilfe von OPM aktivieren. Im folgenden finden Sie eine allgemeine Übersicht über die Schritte, die die Anwendung ausführen muss. Details finden Sie weiter unten in diesem Abschnitt.

1.  Die Anwendung muss möglicherweise einen SRM für die Videoausgabe bereitstellen. Der Mechanismus für den Empfang von SRMs liegt außerhalb des Gültigkeits Bereichs der OPM-Schnittstelle. Beispielsweise können SRMs als Teil eines Broadcast Datenstroms übermittelt werden.
2.  Die Anwendung aktiviert den HDCP-Ausgabe Schutz.
3.  Die Anwendung spielt den Videoinhalt. Die Anwendung fragt den Treiber in regelmäßigen Abständen ab, um sicherzustellen, dass HDCP eingeschaltet ist.
4.  Wenn die Wiedergabe beendet ist, wird HDCP von der Anwendung deaktiviert.

### <a name="setting-the-srm"></a>Festlegen des SRM

Führen Sie die folgenden Schritte aus, um den SRM festzulegen.

1.  Initialisieren Sie eine [**OPM- \_ festgelegte \_ HDCP- \_ SRM- \_ Parameter**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_hdcp_srm_parameters) Struktur mit der SRM-Versionsnummer.
2.  Speichern Sie den SRM in einer Variablen.
3.  Senden Sie einen [**OPM \_ Set \_ HDCP \_ SRM**](opm-set-hdcp-srm.md) -Befehl an die Videoausgabe. Verwenden Sie das unter [Senden von OPM-Befehlen](#sending-opm-commands)beschriebene Verfahren.
    -   Der **abparameters** -Member der [**OPM- \_ configure \_ Parameters**](/windows/desktop/api/opmapi/ns-opmapi-opm_configure_parameters) -Struktur enthält die [**OPM- \_ festgelegte \_ HDCP-SRM- \_ \_ Parameter**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_hdcp_srm_parameters) Struktur.
    -   Der *pbadditionalparameters* -Parameter der [**IOPMVideoOutput:: Configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure) -Methode verweist auf die Variable, die das SRM enthält.
4.  Hiermit wird eine OPM-Anforderung zum Status der [**\_ \_ aktuellen \_ HDCP- \_ SRM- \_ Version**](opm-get-current-hdcp-srm-version.md) an die Videoausgabe gesendet. Verwenden Sie das unter [Senden von OPM-Status Anforderungen](#sending-opm-status-requests)beschriebene Verfahren. Diese Status Anforderung enthält keine Eingabedaten, sodass der Inhalt des **abparameters** -Members der [**OPM-Struktur \_ get \_ Info \_ Parameters**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters) nicht definiert ist.
5.  Wenn die [**IOPMVideoOutput:: GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) -Methode zurückgegeben wird, enthält das **abrequestedinformation** -Array in der von [**OPM \_ angeforderten \_ Informations**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_requested_information) Struktur eine [**OPM- \_ Standard \_ Informations**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) Struktur. Der **ulinformation** -Member dieser Struktur enthält die Versionsnummer des aktuellen SRM. Dieser Wert muss mit dem Wert aus Schritt 2 übereinstimmen.

### <a name="enabling-hdcp"></a>Aktivieren von HDCP

Führen Sie die folgenden Schritte aus, um HDCP zu aktivieren.

1.  Initialisieren Sie eine OPM-Struktur vom Typ " [**\_ \_ Schutz \_ Ebenen- \_ Parameter festlegen**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_protection_level_parameters) " mit den folgenden Werten:
    -   **ulschutztyp**  =  **OPM \_ \_Schutztyp \_ HDCP**
    -   **ulschutzlevel**  =  **OPM \_ HDCP \_ auf**
    -   **Reserviert** = 0
    -   **"Reserved2"** = 0
2.  Senden Sie einen OPM-Befehl zum [**\_ Festlegen der \_ Schutz \_ Ebene**](opm-set-protection-level.md) . Bei den Eingabedaten im **abparameter** -Array handelt es sich um die OPM-Struktur zum [**\_ Festlegen der \_ Schutz \_ Ebenen \_**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_protection_level_parameters) .
3.  Senden Sie eine OPM-Anforderung zum Status der [**\_ \_ virtuellen \_ Schutz \_ Ebene**](opm-get-virtual-protection-level.md) , um zu überprüfen, ob HDCP aktiviert ist. Die ersten 4 Bytes des **abparameters** -Elements der [**OPM-Struktur \_ get \_ Info \_ Parameters**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters) enthalten den Wert **OPM \_ Protection \_ Type \_ HDCP**.

Wenn die [**GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) -Methode zurückgegeben wird, enthält das **abrequestedinformation** -Array in der von [**OPM \_ angeforderten \_ Informations**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_requested_information) Struktur eine [**OPM- \_ Standard \_ Informations**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) Struktur. Der **ulinformation** -Member dieser Struktur enthält einen Wert aus der Enumeration der [**OPM- \_ HDCP- \_ Schutz \_ Ebene**](/windows/desktop/api/opmapi/ne-opmapi-opm_hdcp_protection_level) . Wenn der Wert **OPM \_ HDCP \_ on** ist, bedeutet dies, dass HDCP aktiviert ist. Wiederholen Sie andernfalls die Schritte 1 – 2, bis HDCP aktiviert ist, andernfalls tritt ein Fehler auf. (Denken Sie daran, die Sequenznummer zu erhöhen und jedes Mal eine neue Zufallszahl zu generieren.)

Es dauert in der Regel zwischen 100 und 200 Millisekunden, um HDCP zu aktivieren, aber es kann länger dauern. Gehen Sie nicht davon aus, dass HDCP aktiviert ist, bis Sie es überprüft haben.

Deaktivieren Sie HDCP, wenn die Anwendung die Wiedergabe geschützter Inhalte beendet hat. Die Schritte sind identisch mit dem Aktivieren von HDCP, aber in Schritt 1 Legen Sie **ulschutzlevel** auf **OPM \_ HDCP \_ Off** fest.

> [!Note]  
> Aktivieren Sie HDCP nicht, wenn der Verbindungstyp **OPM- \_ Connector- \_ Typ \_ Display Port \_ Embedded** ist. (Siehe [**OPM-Connector-Typflags**](opm-connector-type-flags.md).)

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Output Protection Manager](output-protection-manager.md)
</dt> </dl>

 

 



