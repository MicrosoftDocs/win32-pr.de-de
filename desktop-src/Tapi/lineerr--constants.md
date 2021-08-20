---
description: Im Folgenden finden Sie eine Liste der Fehlercodes, die TAPI beim Aufrufen von Vorgängen für Zeilen, Adressen oder Aufrufe zurückgeben kann.
ms.assetid: bdaf60d1-6ff2-4bd6-b246-8556d6cae644
title: LINEERR_ Konstanten (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de8e362e942f7819b0e15fcd7e8359c308e931868d57cc9da84acd62fe9e531d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119254634"
---
# <a name="lineerr_-constants"></a>\_LINEERR-Konstanten

Im Folgenden finden Sie eine Liste der Fehlercodes, die TAPI beim Aufrufen von Vorgängen für Zeilen, Adressen oder Aufrufe zurückgeben kann. Weitere Informationen dazu, wie Sie bestimmen können, welche dieser Fehlercodes eine bestimmte Funktion zurückgeben kann, finden Sie in den Beschreibungen der einzelnen Funktionen.

<dl> <dt>

<span id="LINEERR_ADDRESSBLOCKED"></span><span id="lineerr_addressblocked"></span>**LINEERR \_ ADDRESSBLOCKED**
</dt> <dd> <dl> <dt>



Das Wählen der angegebenen Adresse bei dem angegebenen Anruf wird blockiert.


</dt> </dl> </dd> <dt>

<span id="LINEERR_ADDRESSBLOCKED"></span><span id="lineerr_addressblocked"></span>**LINEERR \_ ADDRESSBLOCKED**
</dt> <dd> <dl> <dt>



Für die Zielaufrufadresse ist die Anrufblockierung aktiviert.


</dt> </dl> </dd> <dt>

<span id="LINEERR_ALLOCATED"></span><span id="lineerr_allocated"></span>**LINEERR \_ ZUGEORDNET**
</dt> <dd> <dl> <dt>



Die Zeile kann aufgrund einer permanenten Bedingung nicht geöffnet werden, z. B. der eines seriellen Ports, der ausschließlich von einem anderen Prozess geöffnet wird.


</dt> </dl> </dd> <dt>

<span id="LINEERR_BADDEVICEID"></span><span id="lineerr_baddeviceid"></span>**LINEERR \_ BADDEVICEID**
</dt> <dd> <dl> <dt>



Der angegebene Gerätebezeichner oder Zeilengerätebezeichner, z. B. in einem *dwDeviceID-Parameter,* ist ungültig oder liegt außerhalb des zulässigen Bereichs.


</dt> </dl> </dd> <dt>

<span id="LINEERR_BEARERMODEUNAVAIL"></span><span id="lineerr_bearermodeunavail"></span>**LINEERR \_ BEARERMODEUNAVAIL**
</dt> <dd> <dl> <dt>



Der Bearermodusmember in [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) ist ungültig, der in **LINECALLPARAMS** angegebene Bearermodus ist nicht verfügbar, oder der Aufruf-Bearermodus kann nicht in den angegebenen Bearermodus geändert werden.


</dt> </dl> </dd> <dt>

<span id="LINEERR_BILLINGREJECTED"></span><span id="lineerr_billingrejected"></span>**LINEERR \_ BILLINGREJECTED**
</dt> <dd> <dl> <dt>



Der Abrechnungsmodus des Anrufs wurde abgelehnt.


</dt> </dl> </dd> <dt>

<span id="LINEERR_CALLUNAVAIL"></span><span id="lineerr_callunavail"></span>**LINEERR \_ CALLUNAVAIL**
</dt> <dd> <dl> <dt>



Alle Aufrufdarstellungen für die angegebene Adresse werden derzeit verwendet.


</dt> </dl> </dd> <dt>

<span id="LINEERR_COMPLETIONOVERRUN"></span><span id="lineerr_completionoverrun"></span>**LINEERR \_ COMPLETIONOVERRUN**
</dt> <dd> <dl> <dt>



Die maximale Anzahl ausstehender Aufrufabschlusse wurde überschritten.


</dt> </dl> </dd> <dt>

<span id="LINEERR_CONFERENCEFULL"></span><span id="lineerr_conferencefull"></span>**LINEERR \_ CONFERENCEFULL**
</dt> <dd> <dl> <dt>



Die maximale Anzahl von Parteien für eine Konferenz wurde erreicht, oder die angeforderte Anzahl von Parteien kann nicht erfüllt werden.


</dt> </dl> </dd> <dt>

<span id="LINEERR_DIALBILLING"></span><span id="lineerr_dialbilling"></span>**LINEERR \_ DIALBILLING**
</dt> <dd> <dl> <dt>



Der DFÜ-Adressparameter enthält DFÜ-Steuerzeichen, die vom Dienstanbieter nicht verarbeitet werden.


</dt> </dl> </dd> <dt>

<span id="LINEERR_DIALDIALTONE"></span><span id="lineerr_dialdialtone"></span>**LINEERR \_ DIALDIALTONE**
</dt> <dd> <dl> <dt>



Der DFÜ-Adressparameter enthält DFÜ-Steuerzeichen, die vom Dienstanbieter nicht verarbeitet werden.


</dt> </dl> </dd> <dt>

<span id="LINEERR_DIALPROMPT"></span><span id="lineerr_dialprompt"></span>**LINEERR \_ DIALPROMPT**
</dt> <dd> <dl> <dt>



Der DFÜ-Adressparameter enthält DFÜ-Steuerzeichen, die vom Dienstanbieter nicht verarbeitet werden.


</dt> </dl> </dd> <dt>

<span id="LINEERR_DIALQUIET"></span><span id="lineerr_dialquiet"></span>**LINEERR \_ DIALQUIET**
</dt> <dd> <dl> <dt>



Der DFÜ-Adressparameter enthält DFÜ-Steuerzeichen, die vom Dienstanbieter nicht verarbeitet werden.


</dt> </dl> </dd> <dt>

<span id="LINEERR_DIALVOICEDETECT"></span><span id="lineerr_dialvoicedetect"></span>**LINEERR \_ DIALVOICEDETECT**
</dt> <dd> <dl> <dt>



Verwendung des Wählmodifizierer (:) wird nicht unterstützt. Dieser Wert wird nur für Anwendungen verfügbar gemacht, die eine TAPI-Version von 2.0 oder höher aushandeln.


</dt> </dl> </dd> <dt>

<span id="LINEERR_DISCONNECTED"></span><span id="lineerr_disconnected"></span>**LINEERR \_ GETRENNT**
</dt> <dd> <dl> <dt>



Der Aufruf wurde getrennt. Dieser Wert wird nur für Anwendungen verfügbar gemacht, die eine TAPI-Version von 2.2 oder höher aushandeln.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INCOMPATIBLEAPIVERSION"></span><span id="lineerr_incompatibleapiversion"></span>**LINEERR \_ INCOMPATIBLEAPIVERSION**
</dt> <dd> <dl> <dt>



Die Anwendung hat eine TAPI-Version oder einen Versionsbereich angefordert, die mit der Implementierung der Telefonie-API und dem entsprechenden Dienstanbieter entweder nicht kompatibel ist oder von dieser nicht unterstützt werden kann.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INCOMPATIBLEEXTVERSION"></span><span id="lineerr_incompatibleextversion"></span>**LINEERR \_ INCOMPATIBLEEXTVERSION**
</dt> <dd> <dl> <dt>



Die Anwendung hat einen Erweiterungsversionsbereich angefordert, der entweder ungültig ist oder vom entsprechenden Dienstanbieter nicht unterstützt werden kann.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INIFILECORRUPT"></span><span id="lineerr_inifilecorrupt"></span>**LINEERR \_ INIFILECORRUPT**
</dt> <dd> <dl> <dt>



Die Telephon.ini Datei kann aufgrund interner Inkonsistenzen oder Formatierungsprobleme von TAPI nicht richtig gelesen oder verstanden werden. Beispielsweise kann der \[ Abschnitt \] Speicherorte, Karten oder Länder der Telephon.ini Datei beschädigt oder \[ \] \[ \] inkonsistent sein.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INUSE"></span><span id="lineerr_inuse"></span>**LINEERR \_ INUSE**
</dt> <dd> <dl> <dt>



Das Leitungsgerät wird verwendet und kann derzeit nicht konfiguriert werden, eine Partei kann hinzugefügt werden, ein Anruf kann beantwortet werden, ein Anruf kann nicht platziert werden, oder ein Anruf kann übertragen werden.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALADDRESS"></span><span id="lineerr_invaladdress"></span>**LINEERR \_ INVALADDRESS**
</dt> <dd> <dl> <dt>



Eine angegebene Adresse ist entweder ungültig oder nicht zulässig. Wenn ungültig, enthält die Adresse ungültige Zeichen oder Ziffern, oder die Zieladresse enthält Steuerzeichen (W, @, $oder ?), die vom Dienstanbieter nicht unterstützt werden. Wenn dies nicht zulässig ist, wird die angegebene Adresse entweder nicht der angegebenen Zeile zugewiesen oder ist für die Adressumleitung ungültig.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALADDRESSID"></span><span id="lineerr_invaladdressid"></span>**LINEERR \_ INVALADDRESSID**
</dt> <dd> <dl> <dt>



Der angegebene Adressbezeichner ist entweder ungültig oder liegt außerhalb des zulässigen Bereichs.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALADDRESSMODE"></span><span id="lineerr_invaladdressmode"></span>**LINEERR \_ INVALADDRESSMODE**
</dt> <dd> <dl> <dt>



Der angegebene Adressmodus ist ungültig.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALADDRESSSTATE"></span><span id="lineerr_invaladdressstate"></span>**LINEERR \_ INVALADDRESSSTATE**
</dt> <dd> <dl> <dt>



Der angegebene Adresszustand enthält ein oder mehrere Bits, die keine [**LINEADDRESSSTATE-Konstanten \_**](lineaddressstate--constants.md)sind.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALADDRESSTYPE"></span><span id="lineerr_invaladdresstype"></span>**LINEERR \_ INVALADDRESSTYPE**
</dt> <dd> <dl> <dt>



Die Anwendung hat auf einen ungültigen Adresstyp verwiesen. Dieser Wert wird nur für Anwendungen verfügbar gemacht, die eine TAPI-Version von 3.0 oder höher aushandeln.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALAGENTACTIVITY"></span><span id="lineerr_invalagentactivity"></span>**LINEERR \_ INVALAGENTACTIVITY**
</dt> <dd> <dl> <dt>



Die angegebene Agentaktivität ist ungültig.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALAGENTACTIVITY"></span><span id="lineerr_invalagentactivity"></span>**LINEERR \_ INVALAGENTACTIVITY**
</dt> <dd> <dl> <dt>



Die Anwendung, die diesen Vorgang aufruft, ist das Ziel der indirekten Übergabe. Das heißt, TAPI hat ermittelt, dass die aufrufende Anwendung auch die Anwendung mit der höchsten Priorität für den angegebenen Medientyp ist. Dieser Wert wird nur für Anwendungen verfügbar gemacht, die eine TAPI-Version von 2.0 oder höher aushandeln.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALAGENTGROUP"></span><span id="lineerr_invalagentgroup"></span>**LINEERR \_ INVALAGENTGROUP**
</dt> <dd> <dl> <dt>



Die angegebenen Agentgruppeninformationen sind ungültig oder enthalten Fehler. Die angeforderte Aktion wurde nicht ausgeführt.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALAGENTGROUP"></span><span id="lineerr_invalagentgroup"></span>**LINEERR \_ INVALAGENTGROUP**
</dt> <dd> <dl> <dt>



Die Anwendung hat auf eine ungültige Agentgruppe verwiesen. Dieser Wert wird nur für Anwendungen verfügbar gemacht, die eine TAPI-Version von 2.0 oder höher aushandeln.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALAGENTID"></span><span id="lineerr_invalagentid"></span>**LINEERR \_ INVALAGENTID**
</dt> <dd> <dl> <dt>



Der angegebene Agent-Bezeichner ist ungültig.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALAGENTID"></span><span id="lineerr_invalagentid"></span>**LINEERR \_ INVALAGENTID**
</dt> <dd> <dl> <dt>



Ein ungültiger Agentbezeichner wurde verwendet. Dieser Wert wird nur für Anwendungen verfügbar gemacht, die eine TAPI-Version von 2.0 oder höher aushandeln.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALAGENTSESSIONSTATE"></span><span id="lineerr_invalagentsessionstate"></span>**LINEERR \_ INVALAGENTSESSIONSTATE**
</dt> <dd> <dl> <dt>



Der Agent-Sitzungszustand ist ungültig. Dieser Wert wird nur für Anwendungen verfügbar gemacht, die eine TAPI-Version von 2.2 oder höher aushandeln.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALAGENTSTATE"></span><span id="lineerr_invalagentstate"></span>**LINEERR \_ INVALAGENTSTATE**
</dt> <dd> <dl> <dt>



Der angegebene Agent-Zustand ist ungültig oder enthält Fehler. Es wurden keine Änderungen am Agentstatus der angegebenen Adresse vorgenommen.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALAGENTSTATE"></span><span id="lineerr_invalagentstate"></span>**LINEERR \_ INVALAGENTSTATE**
</dt> <dd> <dl> <dt>



Die Anwendung hat auf einen ungültigen Agentzustand verwiesen. Dieser Wert wird nur für Anwendungen verfügbar gemacht, die eine TAPI-Version von 2.0 oder höher aushandeln.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALAPPHANDLE"></span><span id="lineerr_invalapphandle"></span>**LINEERR \_ INVALAPPHANDLE**
</dt> <dd> <dl> <dt>



Das Anwendungshandle (z. B. durch einen *hLineApp-Parameter* angegeben) oder das Anwendungsregistrierungshandle ist ungültig.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALAPPNAME"></span><span id="lineerr_invalappname"></span>**LINEERR \_ INVALAPPNAME**
</dt> <dd> <dl> <dt>



Der angegebene Anwendungsname ist ungültig. Wenn ein Anwendungsname von der Anwendung angegeben wird, wird davon ausgegangen, dass die Zeichenfolge keine nicht darstellbaren Zeichen enthält und null endet.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALBEARERMODE"></span><span id="lineerr_invalbearermode"></span>**LINEERR \_ INVALBEARERMODE**
</dt> <dd> <dl> <dt>



Der angegebene Bearermodus ist ungültig.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALCALLCOMPLMODE"></span><span id="lineerr_invalcallcomplmode"></span>**LINEERR \_ INVALCALLCOMPLMODE**
</dt> <dd> <dl> <dt>



Die angegebene Vervollständigung ist ungültig.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALCALLHANDLE"></span><span id="lineerr_invalcallhandle"></span>**LINEERR \_ INVALCALLHANDLE**
</dt> <dd> <dl> <dt>



Das angegebene Aufrufhandle ist ungültig. Beispielsweise ist das Handle nicht **NULL,** gehört jedoch nicht zur angegebenen Zeile. In einigen Fällen ist das angegebene Anrufgerätehandle ungültig.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALCALLPARAMS"></span><span id="lineerr_invalcallparams"></span>**LINEERR \_ INVALCALLPARAMS**
</dt> <dd> <dl> <dt>



Die angegebenen Aufrufparameter sind ungültig.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALCALLPRIVILEGE"></span><span id="lineerr_invalcallprivilege"></span>**LINEERR \_ INVALCALLPRIVILEGE**
</dt> <dd> <dl> <dt>



Der angegebene Parameter für Aufrufberechtigungen ist ungültig.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALCALLSELECT"></span><span id="lineerr_invalcallselect"></span>**LINEERR \_ INVALCALLSELECT**
</dt> <dd> <dl> <dt>



Der angegebene select-Parameter ist ungültig.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALCALLSTATE"></span><span id="lineerr_invalcallstate"></span>**LINEERR \_ INVALCALLSTATE**
</dt> <dd> <dl> <dt>



Der aktuelle Zustand eines Aufrufs befindet sich für den angeforderten Vorgang nicht in einem gültigen Zustand.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALCALLSTATELIST"></span><span id="lineerr_invalcallstatelist"></span>**LINEERR \_ INVALCALLSTATELIST**
</dt> <dd> <dl> <dt>



Die angegebene Aufrufzustandsliste ist ungültig.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALCARD"></span><span id="lineerr_invalcard"></span>**LINEERR \_ INVALCARD**
</dt> <dd> <dl> <dt>



Der in *dwCard* angegebene permanente Kartenbezeichner wurde in keinen Einträgen im Abschnitt \[ Karten in der Registrierung \] gefunden.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALCOMPLETIONID"></span><span id="lineerr_invalcompletionid"></span>**LINEERR \_ INVALCOMPLETIONID**
</dt> <dd> <dl> <dt>



Der Vervollständigungsbezeichner ist ungültig.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALCONFCALLHANDLE"></span><span id="lineerr_invalconfcallhandle"></span>**LINEERR \_ INVALCONFCALLHANDLE**
</dt> <dd> <dl> <dt>



Das angegebene Aufrufhand handle für den Konferenzaufruf ist ungültig oder kein Handle für einen Konferenzaufruf.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALCONSULTCALLHANDLE"></span><span id="lineerr_invalconsultcallhandle"></span>**LINEERR \_ INVALCONSULTCALLHANDLE**
</dt> <dd> <dl> <dt>



Das angegebene Anrufhand handle für die Beratung ist ungültig.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALCOUNTRYCODE"></span><span id="lineerr_invalcountrycode"></span>**LINEERR \_ INVALCOUNTRYCODE**
</dt> <dd> <dl> <dt>



Der angegebene Länder- oder Regioncode ist ungültig.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALDEVICECLASS"></span><span id="lineerr_invaldeviceclass"></span>**LINEERR \_ INVALDEVICECLASS**
</dt> <dd> <dl> <dt>



Dem Liniengerät ist kein Gerät für die angegebene Geräteklasse zugeordnet, oder die angegebene Zeile unterstützt die angegebene Geräteklasse nicht.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALDEVICEHANDLE"></span><span id="lineerr_invaldevicehandle"></span>**LINEERR \_ INVALDEVICEHANDLE**
</dt> <dd> <dl> <dt>



Das Zeilengerätehandy ist ungültig.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALDIALPARAMS"></span><span id="lineerr_invaldialparams"></span>**LINEERR \_ INVALDIALPARAMS**
</dt> <dd> <dl> <dt>



Die Wählparameter sind ungültig.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALDIGITLIST"></span><span id="lineerr_invaldigitlist"></span>**LINEERR \_ INVALDIGITLIST**
</dt> <dd> <dl> <dt>



Die angegebene Ziffernliste ist ungültig.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALDIGITMODE"></span><span id="lineerr_invaldigitmode"></span>**LINEERR \_ INVALDIGITMODE**
</dt> <dd> <dl> <dt>



Der angegebene Ziffernmodus ist ungültig.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALDIGITS"></span><span id="lineerr_invaldigits"></span>**LINEERR \_ INVALDIGITS**
</dt> <dd> <dl> <dt>



Die angegebenen Beendigungsziffern sind ungültig.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALEXTVERSION"></span><span id="lineerr_invalextversion"></span>**LINEERR \_ INVALEXTVERSION**
</dt> <dd> <dl> <dt>



Die Versionsnummer der Dienstanbietererweiterung ist ungültig.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALFEATURE"></span><span id="lineerr_invalfeature"></span>**\_LINEERR-INVALFEATURE**
</dt> <dd> <dl> <dt>



Der *dwFeature-Parameter* ist ungültig.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALFEATURE"></span><span id="lineerr_invalfeature"></span>**\_LINEERR-INVALFEATURE**
</dt> <dd> <dl> <dt>



Die Anwendung hat ein Feature aufgerufen, das in dieser Zeile nicht verfügbar ist.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALGROUPID"></span><span id="lineerr_invalgroupid"></span>**LINEERR \_ INVALGROUPID**
</dt> <dd> <dl> <dt>



Der angegebene Gruppenbezeichner ist ungültig.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALLINEHANDLE"></span><span id="lineerr_invallinehandle"></span>**LINEERR \_ INVALLINEHANDLE**
</dt> <dd> <dl> <dt>



Der angegebene Aufruf, das angegebene Gerät, das Zeilengerät oder das Zeilenhand handle ist ungültig.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALLINESTATE"></span><span id="lineerr_invallinestate"></span>**LINEERR \_ INVALLINESTATE**
</dt> <dd> <dl> <dt>



Die Gerätekonfiguration kann im aktuellen Zeilenzustand nicht geändert werden. Die Zeile kann von einer anderen Anwendung verwendet werden, oder ein *dwLineStates-Parameter* enthält mindestens ein Bits, bei dem es sich nicht um [LINEDEVSTATE-Konstanten \_ handelt.](linedevstate--constants.md) Der **LINEERR \_ INVALLINESTATE-Wert** kann auch darauf hindeuten, dass das Gerät getrennt oder außer Dienst ist. Diese Zustände werden angegeben, indem die Bits, die den *LINEDEVSTATUSFLAGS \_ CONNECTED-* und *LINEDEVSTATUSFLAGS \_ INSERVICE-Werten* entspricht, im **dwDevStatusFlags-Member** der [**LINEDEVSTATUS-Struktur,**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) die von der [**lineGetLineDevStatus-Funktion**](/windows/desktop/api/Tapi/nf-tapi-linegetlinedevstatus) zurückgegeben wird, auf 0 festgelegt werden.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALLOCATION"></span><span id="lineerr_invallocation"></span>**\_LINEERR-INVALLOCATION**
</dt> <dd> <dl> <dt>



Der in *dwLocation* angegebene permanente Standortbezeichner wurde in den Einträgen im Abschnitt \[ \] Speicherorte der Registrierung nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALMEDIALIST"></span><span id="lineerr_invalmedialist"></span>**LINEERR \_ INVALMEDIALIST**
</dt> <dd> <dl> <dt>



Die angegebene Medienliste ist ungültig.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALMEDIAMODE"></span><span id="lineerr_invalmediamode"></span>**LINEERR \_ INVALMEDIAMODE**
</dt> <dd> <dl> <dt>



Die Liste der zu überwachenden Medientypen (Modi) enthält ungültige Informationen, der angegebene Medientypparameter ist ungültig, oder der Dienstanbieter unterstützt den angegebenen Medientyp nicht. Die in der Zeile unterstützten Medientypen werden im **dwMediaModes-Member** in der [**LINEDEVCAPS-Struktur**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) aufgeführt.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALMESSAGEID"></span><span id="lineerr_invalmessageid"></span>**LINEERR \_ INVALMESSAGEID**
</dt> <dd> <dl> <dt>



Die in *dwMessageID angegebene* Zahl liegt außerhalb des Bereichs, der vom **dwNumCompletionMessages-Member** in der [**LINEADDRESSCAPS-Struktur angegeben**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) wird.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALPARAM"></span><span id="lineerr_invalparam"></span>**LINEERR \_ INVALPARAM**
</dt> <dd> <dl> <dt>



Ein Parameter oder eine Struktur, auf die ein Parameter verweist, enthält ungültige Informationen, ein Länder- oder Regioncode ist ungültig, ein Fensterhand handle ist ungültig, oder der angegebene Vorwärtslistenparameter enthält ungültige Informationen.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALPARKID"></span><span id="lineerr_invalparkid"></span>**LINEERR \_ INVALPARKID**
</dt> <dd> <dl> <dt>



Die Park-ID ist ungültig.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALPARKMODE"></span><span id="lineerr_invalparkmode"></span>**LINEERR \_ INVALPARKMODE**
</dt> <dd> <dl> <dt>



Der angegebene Parkmodus ist ungültig.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALPASSWORD"></span><span id="lineerr_invalpassword"></span>**LINEERR \_ INVALPASSWORD**
</dt> <dd> <dl> <dt>



Das angegebene Kennwort ist nicht korrekt, und die angeforderte Aktion wurde nicht ausgeführt.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALPASSWORD"></span><span id="lineerr_invalpassword"></span>**LINEERR \_ INVALPASSWORD**
</dt> <dd> <dl> <dt>



Die Anwendung hat ein ungültiges Kennwort verwendet. Dieser Wert wird nur für Anwendungen verfügbar gemacht, die eine TAPI-Version von 2.0 oder höher aushandeln.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALPOINTER"></span><span id="lineerr_invalpointer"></span>**LINEERR \_ INVALPOINTER**
</dt> <dd> <dl> <dt>



Mindestens einer der angegebenen Zeigerparameter (z. B. *lpCallList,* *lpdwAPIVersion,* *lpExtensionID,* *lpdwExtVersion,* *lphIcon,* *lpLineDevCaps* und *lpToneList)* sind ungültig, oder ein erforderlicher Zeiger auf einen Ausgabeparameter ist **NULL.**


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALPRIVSELECT"></span><span id="lineerr_invalprivselect"></span>**LINEERR \_ INVALPRIVSELECT**
</dt> <dd> <dl> <dt>



Für den *dwPrivileges-Parameter* wurde ein ungültiges Flag oder eine Kombination von Flags festgelegt.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALRATE"></span><span id="lineerr_invalrate"></span>**\_LINEERR-INVALRATE**
</dt> <dd> <dl> <dt>



Die angegebene Rate ist ungültig.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALREQUESTMODE"></span><span id="lineerr_invalrequestmode"></span>**LINEERR \_ INVALREQUESTMODE**
</dt> <dd> <dl> <dt>



Der [**LINEREQUESTMODE-Indikator**](linerequestmode--constants.md) ist ungültig.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALTERMINALID"></span><span id="lineerr_invalterminalid"></span>**LINEERR \_ INVALTERMINALID**
</dt> <dd> <dl> <dt>



Der angegebene Terminalbezeichner ist ungültig.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALTERMINALMODE"></span><span id="lineerr_invalterminalmode"></span>**LINEERR \_ INVALTERMINALMODE**
</dt> <dd> <dl> <dt>



Der angegebene Terminalmodiparameter ist ungültig.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALTIMEOUT"></span><span id="lineerr_invaltimeout"></span>**LINEERR \_ INVALTIMEOUT**
</dt> <dd> <dl> <dt>



Timeouts werden nicht unterstützt, oder ein Wert liegt außerhalb des gültigen Bereichs, der in [**LINEDEVCAPS angegeben ist.**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps)


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALTONE"></span><span id="lineerr_invaltone"></span>**LINEERR \_ INVALTONE**
</dt> <dd> <dl> <dt>



Der angegebene benutzerdefinierte Ton stellt keinen gültigen Ton dar oder besteht aus zu vielen Frequenzen, oder die angegebene Tonstruktur beschreibt keinen gültigen Ton.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALTONELIST"></span><span id="lineerr_invaltonelist"></span>**LINEERR \_ INVALTONELIST**
</dt> <dd> <dl> <dt>



Die angegebene Tonliste ist ungültig.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALTONEMODE"></span><span id="lineerr_invaltonemode"></span>**LINEERR \_ INVALTONEMODE**
</dt> <dd> <dl> <dt>



Der angegebene Tonmodusparameter ist ungültig.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALTRANSFERMODE"></span><span id="lineerr_invaltransfermode"></span>**LINEERR \_ INVALTRANSFERMODE**
</dt> <dd> <dl> <dt>



Der angegebene Übertragungsmodusparameter ist ungültig.


</dt> </dl> </dd> <dt>

<span id="LINEERR_LINEMAPPERFAILED"></span><span id="lineerr_linemapperfailed"></span>**LINEERR \_ LINEMAPPERFAILED**
</dt> <dd> <dl> <dt>



LINEMAPPER war der Wert, der im *dwDeviceID-Parameter* übergeben wurde, aber es wurden keine Zeilen gefunden, die den im *lpCallParams-Parameter angegebenen Anforderungen* entsprechen.


</dt> </dl> </dd> <dt>

<span id="LINEERR_NOCONFERENCE"></span><span id="lineerr_noconference"></span>**LINEERR \_ NOCONFERENCE**
</dt> <dd> <dl> <dt>



Der angegebene Aufruf ist weder ein Telefonanrufhandy noch ein Teilnehmeraufruf.


</dt> </dl> </dd> <dt>

<span id="LINEERR_NODEVICE"></span><span id="lineerr_nodevice"></span>**LINEERR \_ NODEVICE**
</dt> <dd> <dl> <dt>



Der angegebene Gerätebezeichner, der zuvor gültig war, wird nicht mehr akzeptiert, da das zugeordnete Gerät seit der letzten Initialisierung von TAPI aus dem System entfernt wurde. Alternativ verfügt das Liniengerät über kein zugeordnetes Gerät für die gegebene Geräteklasse.


</dt> </dl> </dd> <dt>

<span id="LINEERR_NODRIVER"></span><span id="lineerr_nodriver"></span>**LINEERR \_ NODRIVER**
</dt> <dd> <dl> <dt>



Entweder Tapiaddr.dll nicht gefunden werden, oder der Telefondienstanbieter für das angegebene Gerät hat festgestellt, dass eine seiner Komponenten fehlt oder beschädigt ist, und zwar auf eine Weise, die zum Zeitpunkt der Initialisierung nicht erkannt wurde. Dem Benutzer sollte empfohlen werden, die Telefonie-Systemsteuerung zu verwenden, um das Problem zu beheben.


</dt> </dl> </dd> <dt>

<span id="LINEERR_NOMEM"></span><span id="lineerr_nomem"></span>**LINEERR \_ NOMEM**
</dt> <dd> <dl> <dt>



Nicht genügend Arbeitsspeicher, um den Vorgang durchzuführen, oder Speicher kann nicht gesperrt werden.


</dt> </dl> </dd> <dt>

<span id="LINEERR_NOMULTIPLEINSTANCE"></span><span id="lineerr_nomultipleinstance"></span>**LINEERR \_ NOMULTIPLEINSTANCE**
</dt> <dd> <dl> <dt>



Ein Telefoniedienstanbieter, der nicht mehrere Instanzen unterstützt, wird mehrmals im Abschnitt \[ Anbieter in der Registrierung \] aufgeführt. Die Anwendung sollte dem Benutzer empfehlen, die Telefonie-Systemsteuerung, um den duplizierten Treiber zu entfernen.


</dt> </dl> </dd> <dt>

<span id="LINEERR_NOMULTIPLEINSTANCE"></span><span id="lineerr_nomultipleinstance"></span>**LINEERR \_ NOMULTIPLEINSTANCE**
</dt> <dd> <dl> <dt>



Mehrere Instanzen dieses Dienstanbieters sind nicht zulässig.


</dt> </dl> </dd> <dt>

<span id="LINEERR_NOREQUEST"></span><span id="lineerr_norequest"></span>**LINEERR \_ NOREQUEST**
</dt> <dd> <dl> <dt>



Derzeit steht keine Anforderung des angegebenen Modus aus, oder die Anwendung ist nicht mehr die Anwendung mit der höchsten Priorität für den angegebenen Anforderungsmodus.


</dt> </dl> </dd> <dt>

<span id="LINEERR_NOTOWNER"></span><span id="lineerr_notowner"></span>**LINEERR \_ NO-LINEER**
</dt> <dd> <dl> <dt>



Die Anwendung verfügt über keine Besitzerberechtigung für den angegebenen Aufruf.


</dt> </dl> </dd> <dt>

<span id="LINEERR_NOTREGISTERED"></span><span id="lineerr_notregistered"></span>**LINEERR \_ NOTREGISTERED**
</dt> <dd> <dl> <dt>



Die Anwendung ist nicht als Anforderungsempfänger für den angegebenen Anforderungsmodus registriert.


</dt> </dl> </dd> <dt>

<span id="LINEERR_OPERATIONFAILED"></span><span id="lineerr_operationfailed"></span>**LINEERR \_ OPERATIONFAILED**
</dt> <dd> <dl> <dt>



Der Vorgang ist aus einem nicht angegebenen oder unbekannten Grund fehlgeschlagen.


</dt> </dl> </dd> <dt>

<span id="LINEERR_OPERATIONUNAVAIL"></span><span id="lineerr_operationunavail"></span>**LINEERR \_ OPERATIONUNAVAIL**
</dt> <dd> <dl> <dt>



Der Vorgang ist nicht verfügbar, z. B. für das angegebene Gerät oder die angegebene Zeile.


</dt> </dl> </dd> <dt>

<span id="LINEERR_RATEUNAVAIL"></span><span id="lineerr_rateunavail"></span>**LINEERR \_ RATEUNAVAIL**
</dt> <dd> <dl> <dt>



Der Dienstanbieter verfügt derzeit nicht über genügend Bandbreite für die angegebene Rate.


</dt> </dl> </dd> <dt>

<span id="LINEERR_REINIT"></span><span id="lineerr_reinit"></span>**LINEERR \_ REINIT**
</dt> <dd> <dl> <dt>



Wenn die TAPI-Neuinitialisierung angefordert wurde, z. B. als Ergebnis des Hinzufügens oder Entfernens eines Telefoniedienstanbieters, werden [**lineInitialize-,**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize) [**lineInitializeEx-**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa)oder [**lineOpen-Anforderungen**](/windows/desktop/api/Tapi/nf-tapi-lineopen) mit diesem Fehler abgelehnt, bis die letzte Anwendung ihre Nutzung der API heruntergefahren hat (mit [**lineShutdown).**](/windows/desktop/api/Tapi/nf-tapi-lineshutdown)Zu diesem Zeitpunkt wird die neue Konfiguration wirksam, und Anwendungen dürfen erneut **lineInitialize** oder **lineInitializeEx** aufrufen.


</dt> </dl> </dd> <dt>

<span id="LINEERR_REINIT"></span><span id="lineerr_reinit"></span>**LINEERR \_ REINIT**
</dt> <dd> <dl> <dt>



Die Anwendung hat zweimal versucht, TAPI zu initialisieren.


</dt> </dl> </dd> <dt>

<span id="LINEERR_REQUESTOVERRUN"></span><span id="lineerr_requestoverrun"></span>**LINEERR \_ REQUESTOVERRUN**
</dt> <dd> <dl> <dt>



Es stehen mehr Anforderungen aus, als das Gerät verarbeiten kann.


</dt> </dl> </dd> <dt>

<span id="LINEERR_RESOURCEUNAVAIL"></span><span id="lineerr_resourceunavail"></span>**LINEERR \_ RESOURCEUNAVAIL**
</dt> <dd> <dl> <dt>



Nicht genügend Ressourcen zum Abschließen des Vorgangs. Beispielsweise kann eine Zeile aufgrund einer dynamischen Ressourcenüberbelegung nicht geöffnet werden.


</dt> </dl> </dd> <dt>

<span id="LINEERR_STRUCTURETOOSMALL"></span><span id="lineerr_structuretoosmall"></span>**LINEERR \_ STRUCTURETOOSMALL**
</dt> <dd> <dl> <dt>



Der **dwTotalSize-Member** einer -Struktur gibt nicht genügend Arbeitsspeicher an, um den festen Teil der angegebenen Struktur zu enthalten.


</dt> </dl> </dd> <dt>

<span id="LINEERR_TARGETNOTFOUND"></span><span id="lineerr_targetnotfound"></span>**LINEERR \_ TARGETNOTFOUND**
</dt> <dd> <dl> <dt>



Ein Ziel für die Übergabe des Anrufs wurde nicht gefunden. Dies kann auftreten, wenn die benannte Anwendung nicht dieselbe Zeile mit dem LINECALLPRIVILEGE OWNER-Bit im \_ *dwPrivileges-Parameter* von [**lineOpen geöffnet hat.**](/windows/desktop/api/Tapi/nf-tapi-lineopen) Im Falle der Übergabe im Medienmodus hat keine Anwendung dieselbe Zeile mit dem LINECALLPRIVILEGE OWNER-Bit im \_ *dwPrivileges-Parameter* von [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen) geöffnet, und der im *dwMediaMode-Parameter* angegebene Medientyp wurde im *parameter dwMediaModes* von [**lineOpen angegeben.**](/windows/desktop/api/Tapi/nf-tapi-lineopen)


</dt> </dl> </dd> <dt>

<span id="LINEERR_TARGETSELF"></span><span id="lineerr_targetself"></span>**LINEERR \_ TARGETSELF**
</dt> <dd> <dl> <dt>



Die Anwendung, die diesen Vorgang aufruft, ist das Ziel der indirekten Übergabe. Das heißt, TAPI hat ermittelt, dass die aufrufende Anwendung auch die Anwendung mit der höchsten Priorität für den angegebenen Medientyp ist.


</dt> </dl> </dd> <dt>

<span id="LINEERR_UNINITIALIZED"></span><span id="lineerr_uninitialized"></span>**LINEERR \_ NICHT INITIALISIERT**
</dt> <dd> <dl> <dt>



Der Vorgang wurde vor jeder Anwendung namens [**lineInitialize oder**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize) [**lineInitializeEx aufgerufen.**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa)


</dt> </dl> </dd> <dt>

<span id="LINEERR_USERCANCELLED"></span><span id="lineerr_usercancelled"></span>**LINEERR \_ USERCANCELLED**
</dt> <dd> <dl> <dt>



Der Benutzer hat den Aufruf abgebrochen. Dieser Wert wird nur für Anwendungen verfügbar gemacht, die eine TAPI-Version von 2.2 oder höher aushandeln.


</dt> </dl> </dd> <dt>

<span id="LINEERR_USERUSERINFOTOOBIG"></span><span id="lineerr_useruserinfotoobig"></span>**LINEERR \_ USERUSRINFOTOOBIG**
</dt> <dd> <dl> <dt>



Die Zeichenfolge, die Benutzer-Benutzer-Informationen enthält, überschreitet die maximale Anzahl von Bytes, die im **dwUUIAcceptSize-,** **dwUUIAnswerSize-,** **dwUUIDropSize-,** **dwUUIMakeCallSize-** oder **dwUUISendUserUserInfoSize-Member** von [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps)angegeben sind, oder die Zeichenfolge, die Benutzerinformationen enthält, ist zu lang.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Hinweise

Die Werte 0xC0000000 bis 0xFFFFFFFF sind für gerätespezifische Erweiterungen verfügbar. Die Werte 0x80000000 durch 0xBFFFFFFF werden reserviert, während 0x00000000 bis 0x7FFFFFFF als Anforderungsbezeichner verwendet werden.

Wenn eine Anwendung eine Fehler-Rückgabe erhält, die sie nicht speziell behandelt (z. B. ein von einer gerätespezifischen Erweiterung definierter Fehler), sollte sie den Fehler als LINEERR OPERATIONFAILED behandeln (aus einem nicht angegebenen \_ Grund).

Beim Aufrufen der LINEERR-Konstanten, die mit TAPI 3.0 neu sind, muss die Tapierr.mc-Datei mit neuen \_ Nachrichten aktualisiert werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2.0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)
</dt> <dt>

[**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps)
</dt> <dt>

[**LINEDEVSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus)
</dt> <dt>

[**lineGetLineDevStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetlinedevstatus)
</dt> <dt>

[**lineInitialize**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize)
</dt> <dt>

[**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa)
</dt> <dt>

[**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen)
</dt> <dt>

[**lineShutdown**](/windows/desktop/api/Tapi/nf-tapi-lineshutdown)
</dt> </dl>

 

 




