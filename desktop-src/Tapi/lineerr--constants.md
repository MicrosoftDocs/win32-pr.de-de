---
description: Im folgenden finden Sie eine Liste von Fehlercodes, die TAPI zurückgeben kann, wenn Vorgänge für Zeilen, Adressen oder Aufrufe aufgerufen werden.
ms.assetid: bdaf60d1-6ff2-4bd6-b246-8556d6cae644
title: LINEERR_ Konstanten (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ed7757377d26dbde832b7ef50f275b45e21760d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369292"
---
# <a name="lineerr_-constants"></a>Lineerr- \_ Konstanten

Im folgenden finden Sie eine Liste von Fehlercodes, die TAPI zurückgeben kann, wenn Vorgänge für Zeilen, Adressen oder Aufrufe aufgerufen werden. Weitere Informationen zum Bestimmen der Fehlercodes, die eine bestimmte Funktion zurückgeben kann, finden Sie in den Beschreibungen zu den einzelnen Funktionen.

<dl> <dt>

<span id="LINEERR_ADDRESSBLOCKED"></span><span id="lineerr_addressblocked"></span>**lineerr \_ adressiblockiert**
</dt> <dd> <dl> <dt>



Die angegebene Adresse wird für den angegebenen-Befehl nicht gewählt.


</dt> </dl> </dd> <dt>

<span id="LINEERR_ADDRESSBLOCKED"></span><span id="lineerr_addressblocked"></span>**lineerr \_ adressiblockiert**
</dt> <dd> <dl> <dt>



Für die Ziel-Telefon Adresse ist die aktivierte Sperre aktiviert.


</dt> </dl> </dd> <dt>

<span id="LINEERR_ALLOCATED"></span><span id="lineerr_allocated"></span>**lineerr \_ zugeordnet**
</dt> <dd> <dl> <dt>



Die Zeile kann aufgrund einer permanenten Bedingung nicht geöffnet werden, z. b. bei einem seriellen Anschluss, der exklusiv von einem anderen Prozess geöffnet wird.


</dt> </dl> </dd> <dt>

<span id="LINEERR_BADDEVICEID"></span><span id="lineerr_baddeviceid"></span>**lineerr \_ badde viceid**
</dt> <dd> <dl> <dt>



Der angegebene Geräte Bezeichner oder zeilige Geräte Bezeichner, z. b. in einem *dwenviceid* -Parameter, ist ungültig oder liegt außerhalb des gültigen Bereichs.


</dt> </dl> </dd> <dt>

<span id="LINEERR_BEARERMODEUNAVAIL"></span><span id="lineerr_bearermodeunavail"></span>**lineerr \_ bearermodeunnütz**
</dt> <dd> <dl> <dt>



Der bearermodusmember in [**linecallparameams**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) ist ungültig, der in **linecallparameams** angegebene bearermodus ist nicht verfügbar, oder der callbearermodus kann nicht in den angegebenen bearermodus geändert werden.


</dt> </dl> </dd> <dt>

<span id="LINEERR_BILLINGREJECTED"></span><span id="lineerr_billingrejected"></span>**lineerr \_ billingreworfene**
</dt> <dd> <dl> <dt>



Der Abrechnungsmodus des Aufrufes wurde zurückgewiesen.


</dt> </dl> </dd> <dt>

<span id="LINEERR_CALLUNAVAIL"></span><span id="lineerr_callunavail"></span>**lineerr \_ callunnütz**
</dt> <dd> <dl> <dt>



Alle Aufrufe für die angegebene Adresse werden zurzeit verwendet.


</dt> </dl> </dd> <dt>

<span id="LINEERR_COMPLETIONOVERRUN"></span><span id="lineerr_completionoverrun"></span>**"lineerr \_ completionüberlauf"**
</dt> <dd> <dl> <dt>



Die maximal zulässige Anzahl von ausstehenden Aufstellungen wurde überschritten.


</dt> </dl> </dd> <dt>

<span id="LINEERR_CONFERENCEFULL"></span><span id="lineerr_conferencefull"></span>**lineerr- \_ Konferenz Name**
</dt> <dd> <dl> <dt>



Die maximale Anzahl von Parteien für eine Konferenz wurde erreicht, oder die angeforderte Anzahl von Parteien kann nicht erfüllt werden.


</dt> </dl> </dd> <dt>

<span id="LINEERR_DIALBILLING"></span><span id="lineerr_dialbilling"></span>**lineerr- \_ dialabrechnung**
</dt> <dd> <dl> <dt>



Der Parameter für die dialable-Adresse enthält Wähl Bare Steuerzeichen, die nicht vom Dienstanbieter verarbeitet werden.


</dt> </dl> </dd> <dt>

<span id="LINEERR_DIALDIALTONE"></span><span id="lineerr_dialdialtone"></span>**lineerr- \_ dialdialtone**
</dt> <dd> <dl> <dt>



Der Parameter für die dialable-Adresse enthält Wähl Bare Steuerzeichen, die nicht vom Dienstanbieter verarbeitet werden.


</dt> </dl> </dd> <dt>

<span id="LINEERR_DIALPROMPT"></span><span id="lineerr_dialprompt"></span>**lineerr- \_ dialprompt**
</dt> <dd> <dl> <dt>



Der Parameter für die dialable-Adresse enthält Wähl Bare Steuerzeichen, die nicht vom Dienstanbieter verarbeitet werden.


</dt> </dl> </dd> <dt>

<span id="LINEERR_DIALQUIET"></span><span id="lineerr_dialquiet"></span>**lineerr- \_ dialquiet**
</dt> <dd> <dl> <dt>



Der Parameter für die dialable-Adresse enthält Wähl Bare Steuerzeichen, die nicht vom Dienstanbieter verarbeitet werden.


</dt> </dl> </dd> <dt>

<span id="LINEERR_DIALVOICEDETECT"></span><span id="lineerr_dialvoicedetect"></span>**lineerr- \_ dialvoicedetect**
</dt> <dd> <dl> <dt>



Verwendung des wählmodifizierers (:) wird nicht unterstützt. Dieser Wert ist nur für Anwendungen verfügbar, die eine TAPI-Version von 2,0 oder höher aushandeln.


</dt> </dl> </dd> <dt>

<span id="LINEERR_DISCONNECTED"></span><span id="lineerr_disconnected"></span>**lineerr \_ getrennt**
</dt> <dd> <dl> <dt>



Der-Rückruf wurde getrennt. Dieser Wert ist nur für Anwendungen verfügbar, die eine TAPI-Version von 2,2 oder höher aushandeln.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INCOMPATIBLEAPIVERSION"></span><span id="lineerr_incompatibleapiversion"></span>**lineerr \_ incompatibleapiversion**
</dt> <dd> <dl> <dt>



Die Anwendung hat eine TAPI-Version oder einen Versions Bereich angefordert, der entweder mit der telefonieimplementierung der Telefonie-API und dem entsprechenden Dienstanbieter kompatibel ist oder nicht von dieser unterstützt werden kann.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INCOMPATIBLEEXTVERSION"></span><span id="lineerr_incompatibleextversion"></span>**lineerr \_ incompatibleextversion**
</dt> <dd> <dl> <dt>



Die Anwendung hat einen Erweiterungs Versions Bereich angefordert, der entweder ungültig ist oder vom entsprechenden Dienstanbieter nicht unterstützt werden kann.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INIFILECORRUPT"></span><span id="lineerr_inifilecorrupt"></span>**lineerr \_ inifilebeschädigt**
</dt> <dd> <dl> <dt>



Die Telephon.ini Datei kann aufgrund interner Inkonsistenzen oder Formatierungs Probleme nicht ordnungsgemäß von TAPI gelesen oder verstanden werden. Beispielsweise kann der \[ Abschnitt "Standorte" \] , "Karten" oder " \[ Länder" \] \[ \] der Telephon.ini Datei beschädigt oder inkonsistent sein.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INUSE"></span><span id="lineerr_inuse"></span>**lineerr- \_ InUse**
</dt> <dd> <dl> <dt>



Das liniengerät wird derzeit verwendet und kann derzeit nicht konfiguriert werden, die Hinzufügung einer Partei, das zulassen eines Aufrufes zulassen, das Platzieren eines Aufrufes zulassen oder das übertragen eines Aufrufes erlauben.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALADDRESS"></span><span id="lineerr_invaladdress"></span>**lineerr- \_ invaladdress**
</dt> <dd> <dl> <dt>



Eine angegebene Adresse ist entweder ungültig oder nicht zulässig. Wenn der Wert ungültig ist, enthält die Adresse ungültige Zeichen oder Ziffern, oder die Zieladresse enthält Wähl Kontrollzeichen (W, @, $ oder?), die vom Dienstanbieter nicht unterstützt werden. Wenn dies nicht zulässig ist, wird die angegebene Adresse entweder nicht der angegebenen Zeile zugewiesen oder ist für die Adressumleitung ungültig.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALADDRESSID"></span><span id="lineerr_invaladdressid"></span>**lineerr \_ invaladressssid**
</dt> <dd> <dl> <dt>



Der angegebene Adress Bezeichner ist entweder ungültig oder liegt außerhalb des zulässigen Bereichs.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALADDRESSMODE"></span><span id="lineerr_invaladdressmode"></span>**lineerr \_ invaladdressmode**
</dt> <dd> <dl> <dt>



Der angegebene Adress Modus ist ungültig.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALADDRESSSTATE"></span><span id="lineerr_invaladdressstate"></span>**lineerr \_ invaladdressstate**
</dt> <dd> <dl> <dt>



Der angegebene Adress Zustand enthält mindestens ein Bit, das keine [**lineaddressstate- \_ Konstanten**](lineaddressstate--constants.md)ist.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALADDRESSTYPE"></span><span id="lineerr_invaladdresstype"></span>**lineerr \_ invaladresssstype**
</dt> <dd> <dl> <dt>



Die Anwendung hat auf einen ungültigen adrestyp verwiesen. Dieser Wert ist nur für Anwendungen verfügbar, die eine TAPI-Version von 3,0 oder höher aushandeln.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALAGENTACTIVITY"></span><span id="lineerr_invalagentactivity"></span>**lineerr \_ invalagentactivity**
</dt> <dd> <dl> <dt>



Die angegebene Agentaktivität ist ungültig.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALAGENTACTIVITY"></span><span id="lineerr_invalagentactivity"></span>**lineerr \_ invalagentactivity**
</dt> <dd> <dl> <dt>



Die Anwendung, die diesen Vorgang aufruft, ist das Ziel der indirekten Übergabe. Das heißt, TAPI hat festgestellt, dass die aufrufenden Anwendung auch die Anwendung mit der höchsten Priorität für den angegebenen Medientyp ist. Dieser Wert ist nur für Anwendungen verfügbar, die eine TAPI-Version von 2,0 oder höher aushandeln.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALAGENTGROUP"></span><span id="lineerr_invalagentgroup"></span>**lineerr \_ invalagentgroup**
</dt> <dd> <dl> <dt>



Die angegebenen agentgruppeninformationen sind ungültig oder enthalten Fehler. Die angeforderte Aktion wurde nicht ausgeführt.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALAGENTGROUP"></span><span id="lineerr_invalagentgroup"></span>**lineerr \_ invalagentgroup**
</dt> <dd> <dl> <dt>



Die Anwendung hat auf eine ungültige Agent-Gruppe verwiesen. Dieser Wert ist nur für Anwendungen verfügbar, die eine TAPI-Version von 2,0 oder höher aushandeln.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALAGENTID"></span><span id="lineerr_invalagentid"></span>**lineerr \_ invalagentid**
</dt> <dd> <dl> <dt>



Der angegebene Agent-Bezeichner ist ungültig.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALAGENTID"></span><span id="lineerr_invalagentid"></span>**lineerr \_ invalagentid**
</dt> <dd> <dl> <dt>



Es wurde ein ungültiger Agent-Bezeichner verwendet. Dieser Wert ist nur für Anwendungen verfügbar, die eine TAPI-Version von 2,0 oder höher aushandeln.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALAGENTSESSIONSTATE"></span><span id="lineerr_invalagentsessionstate"></span>**lineerr \_ invalagentsessionstate**
</dt> <dd> <dl> <dt>



Der agentsitzungsstatus ist ungültig. Dieser Wert ist nur für Anwendungen verfügbar, die eine TAPI-Version von 2,2 oder höher aushandeln.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALAGENTSTATE"></span><span id="lineerr_invalagentstate"></span>**lineerr \_ invalagentstate**
</dt> <dd> <dl> <dt>



Der angegebene Agentstatus ist ungültig oder enthält Fehler. Es wurden keine Änderungen am Agentstatus der angegebenen Adresse vorgenommen.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALAGENTSTATE"></span><span id="lineerr_invalagentstate"></span>**lineerr \_ invalagentstate**
</dt> <dd> <dl> <dt>



Die Anwendung hat auf einen ungültigen Agent-Status verwiesen. Dieser Wert ist nur für Anwendungen verfügbar, die eine TAPI-Version von 2,0 oder höher aushandeln.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALAPPHANDLE"></span><span id="lineerr_invalapphandle"></span>**lineerr \_ invalapphandle**
</dt> <dd> <dl> <dt>



Das Anwendungs handle (z. b. durch einen *hlineapp* -Parameter angegeben) oder das Anwendungs Registrierungs Handle ist ungültig.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALAPPNAME"></span><span id="lineerr_invalappname"></span>**lineerr \_ invalappname**
</dt> <dd> <dl> <dt>



Der angegebene Anwendungsname ist ungültig. Wenn ein Anwendungsname von der Anwendung angegeben wird, wird davon ausgegangen, dass die Zeichenfolge keine nicht anzeigbaren Zeichen enthält und mit 0 (null) beendet wird.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALBEARERMODE"></span><span id="lineerr_invalbearermode"></span>**lineerr \_ invalbearermode**
</dt> <dd> <dl> <dt>



Der angegebene bearermodus ist ungültig.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALCALLCOMPLMODE"></span><span id="lineerr_invalcallcomplmode"></span>**lineerr \_ invalcallcomplmode**
</dt> <dd> <dl> <dt>



Der angegebene Abschluss ist ungültig.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALCALLHANDLE"></span><span id="lineerr_invalcallhandle"></span>**lineerr \_ invalcallhandle**
</dt> <dd> <dl> <dt>



Das angegebene-Rückruf Handle ist ungültig. Beispielsweise ist das Handle nicht **null** , gehört jedoch nicht zur angegebenen Zeile. In einigen Fällen ist das angegebene Handle-Geräte Handle ungültig.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALCALLPARAMS"></span><span id="lineerr_invalcallparams"></span>**lineerr \_ invalcallparametriams**
</dt> <dd> <dl> <dt>



Die angegebenen Parameter für den Rückruf sind ungültig.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALCALLPRIVILEGE"></span><span id="lineerr_invalcallprivilege"></span>**lineerr \_ invalcallprivilege**
</dt> <dd> <dl> <dt>



Der angegebene Parameter zum Aufrufen von Berechtigungen ist ungültig.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALCALLSELECT"></span><span id="lineerr_invalcallselect"></span>**lineerr \_ invalcallselect**
</dt> <dd> <dl> <dt>



Der angegebene Select-Parameter ist ungültig.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALCALLSTATE"></span><span id="lineerr_invalcallstate"></span>**lineerr \_ invalcallstate**
</dt> <dd> <dl> <dt>



Der aktuelle Zustand eines Aufrufens befindet sich nicht in einem gültigen Zustand für den angeforderten Vorgang.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALCALLSTATELIST"></span><span id="lineerr_invalcallstatelist"></span>**lineerr \_ invalcallstatuelist**
</dt> <dd> <dl> <dt>



Die angegebene aufrufstatusliste ist ungültig.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALCARD"></span><span id="lineerr_invalcard"></span>**lineerr- \_ invalcard**
</dt> <dd> <dl> <dt>



Der in *dwcard* angegebene permanente Karten Bezeichner konnte in keinem Eintrag im \[ Karten Abschnitt der Registrierung gefunden werden \] .


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALCOMPLETIONID"></span><span id="lineerr_invalcompletionid"></span>**lineerr \_ invalcompletionid**
</dt> <dd> <dl> <dt>



Der Vervollständigungs Bezeichner ist ungültig.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALCONFCALLHANDLE"></span><span id="lineerr_invalconfcallhandle"></span>**lineerr \_ invalconfcallhandle**
</dt> <dd> <dl> <dt>



Das angegebene Telefon Handle für den Konferenz Aufrufwert ist ungültig oder kein Handle für einen Konferenz Befehl.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALCONSULTCALLHANDLE"></span><span id="lineerr_invalconsultcallhandle"></span>**lineerr \_ invalberattcallhandle**
</dt> <dd> <dl> <dt>



Das angegebene Handle für den Beratungs Rückruf ist ungültig.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALCOUNTRYCODE"></span><span id="lineerr_invalcountrycode"></span>**lineerr \_ invalcountrycode**
</dt> <dd> <dl> <dt>



Der angegebene Code für Land oder Region ist ungültig.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALDEVICECLASS"></span><span id="lineerr_invaldeviceclass"></span>**lineerr \_ invalentviceclass**
</dt> <dd> <dl> <dt>



Das liniengerät weist kein zugeordnetes Gerät für die angegebene Geräteklasse auf, oder die angegebene Zeile unterstützt die angegebene Geräteklasse nicht.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALDEVICEHANDLE"></span><span id="lineerr_invaldevicehandle"></span>**lineerr \_ invaldebug-andle**
</dt> <dd> <dl> <dt>



Das Zeilen Geräte Handle ist ungültig.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALDIALPARAMS"></span><span id="lineerr_invaldialparams"></span>**lineerr \_ invaldialparametriams**
</dt> <dd> <dl> <dt>



Die Wähl Parameter sind ungültig.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALDIGITLIST"></span><span id="lineerr_invaldigitlist"></span>**lineerr \_ invaldigitlist**
</dt> <dd> <dl> <dt>



Die angegebene Ziffern Liste ist ungültig.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALDIGITMODE"></span><span id="lineerr_invaldigitmode"></span>**lineerr \_ invaldigitmode**
</dt> <dd> <dl> <dt>



Der angegebene Ziffern Modus ist ungültig.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALDIGITS"></span><span id="lineerr_invaldigits"></span>**lineerr- \_ invaldigits**
</dt> <dd> <dl> <dt>



Die angegebenen Beendigungs Ziffern sind ungültig.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALEXTVERSION"></span><span id="lineerr_invalextversion"></span>**lineerr \_ invalextversion**
</dt> <dd> <dl> <dt>



Die Versionsnummer der Dienstanbieter Erweiterung ist ungültig.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALFEATURE"></span><span id="lineerr_invalfeature"></span>**lineerr- \_ invalfeature**
</dt> <dd> <dl> <dt>



Der *dwfeature* -Parameter ist ungültig.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALFEATURE"></span><span id="lineerr_invalfeature"></span>**lineerr- \_ invalfeature**
</dt> <dd> <dl> <dt>



Die Anwendung hat eine Funktion aufgerufen, die in dieser Zeile nicht verfügbar ist.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALGROUPID"></span><span id="lineerr_invalgroupid"></span>**lineerr \_ invalgroupid**
</dt> <dd> <dl> <dt>



Der angegebene Gruppen Bezeichner ist ungültig.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALLINEHANDLE"></span><span id="lineerr_invallinehandle"></span>**lineerr- \_ invallinehandle**
</dt> <dd> <dl> <dt>



Der angegebene Rückruf, das Gerät, das Zeilen Gerät oder das Zeilen Handle ist ungültig.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALLINESTATE"></span><span id="lineerr_invallinestate"></span>**lineerr- \_ invallinestate**
</dt> <dd> <dl> <dt>



Die Gerätekonfiguration kann im aktuellen Zeilen Status nicht geändert werden. Die Zeile wird möglicherweise von einer anderen Anwendung verwendet, oder ein *dwlinestates* -Parameter enthält mindestens ein Bit, das keine [linedevstate- \_ Konstanten](linedevstate--constants.md)ist. Der **lineerr-Wert " \_ invallinestate** " kann auch darauf hinweisen, dass das Gerät getrennt oder außer Betrieb genommen wird. Diese Zustände werden angegeben, indem die Bits, die den *\_ verbundenen linedevstatusflags* -und *linedevstatusflags- \_ INService* -Werten entsprechen, im **dwdevstatusflags** -Member der [**linedevstatus**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) -Struktur, die von der [**linegetlinedevstatus**](/windows/desktop/api/Tapi/nf-tapi-linegetlinedevstatus) -Funktion zurückgegeben wird, auf 0 festgelegt werden.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALLOCATION"></span><span id="lineerr_invallocation"></span>**lineerr \_ invallocation**
</dt> <dd> <dl> <dt>



Der in *dwlocation* angegebene Bezeichner für die permanente Position konnte in keinem Eintrag im Abschnitt "Speicher \[ Orte" \] in der Registrierung gefunden werden.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALMEDIALIST"></span><span id="lineerr_invalmedialist"></span>**lineerr \_ invalmedialist**
</dt> <dd> <dl> <dt>



Die angegebene Medien Liste ist ungültig.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALMEDIAMODE"></span><span id="lineerr_invalmediamode"></span>**lineerr \_ invalmediamode**
</dt> <dd> <dl> <dt>



Die Liste der zu überwachenden Medientypen (Modi) enthält ungültige Informationen, der angegebene Medientyp-Parameter ist ungültig, oder der angegebene Medientyp wird vom Dienstanbieter nicht unterstützt. Die in der Zeile unterstützten Medientypen werden im **dwmediamodes** -Member in der [**linedevcaps**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) -Struktur aufgeführt.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALMESSAGEID"></span><span id="lineerr_invalmessageid"></span>**lineerr \_ invalmessageid**
</dt> <dd> <dl> <dt>



Die in *dwMessageId* angegebene Zahl liegt außerhalb des Bereichs, der vom **dwnumcompletionmessages** -Member in der [**lineaddresscaps**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) -Struktur angegeben wird.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALPARAM"></span><span id="lineerr_invalparam"></span>**lineerr \_ invalparam**
</dt> <dd> <dl> <dt>



Ein Parameter oder eine Struktur, auf den ein Parameter zeigt, enthält ungültige Informationen, ein Länder-oder Regions Code ist ungültig, ein Fenster Handle ist ungültig, oder der angegebene forward-Listen Parameter enthält ungültige Informationen.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALPARKID"></span><span id="lineerr_invalparkid"></span>**lineerr \_ invalpark ID**
</dt> <dd> <dl> <dt>



Der Park Bezeichner ist ungültig.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALPARKMODE"></span><span id="lineerr_invalparkmode"></span>**lineerr \_ invalparkmode**
</dt> <dd> <dl> <dt>



Der angegebene Park Modus ist ungültig.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALPASSWORD"></span><span id="lineerr_invalpassword"></span>**lineerr \_ invalpassword**
</dt> <dd> <dl> <dt>



Das angegebene Kennwort ist nicht korrekt, und die angeforderte Aktion wurde nicht ausgeführt.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALPASSWORD"></span><span id="lineerr_invalpassword"></span>**lineerr \_ invalpassword**
</dt> <dd> <dl> <dt>



Die Anwendung hat ein ungültiges Kennwort verwendet. Dieser Wert ist nur für Anwendungen verfügbar, die eine TAPI-Version von 2,0 oder höher aushandeln.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALPOINTER"></span><span id="lineerr_invalpointer"></span>**lineerr- \_ invalpointer**
</dt> <dd> <dl> <dt>



Mindestens ein angegebener Zeiger Parameter (z. b. *lpcalllist*, *lpdwapiversion*, *lpextensionid*, *lpdwextversion*, *lphicon*, *lplinedevcaps* und *lptonelist*) ist ungültig, oder ein erforderlicher Zeiger auf einen Output-Parameter ist **null**.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALPRIVSELECT"></span><span id="lineerr_invalprivselect"></span>**lineerr \_ invalprivselect**
</dt> <dd> <dl> <dt>



Für den *dwprivileges* -Parameter wurde ein ungültiges Flag oder eine ungültige Kombination von Flags festgelegt.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALRATE"></span><span id="lineerr_invalrate"></span>**lineerr- \_ invalate**
</dt> <dd> <dl> <dt>



Die angegebene Rate ist ungültig.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALREQUESTMODE"></span><span id="lineerr_invalrequestmode"></span>**lineerr \_ invalrequestmode**
</dt> <dd> <dl> <dt>



Der [**linerequestmode**](linerequestmode--constants.md) -Indikator ist ungültig.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALTERMINALID"></span><span id="lineerr_invalterminalid"></span>**lineerr \_ invalterminalid**
</dt> <dd> <dl> <dt>



Der angegebene Terminal Bezeichner ist ungültig.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALTERMINALMODE"></span><span id="lineerr_invalterminalmode"></span>**lineerr \_ invalterminalmode**
</dt> <dd> <dl> <dt>



Der angegebene terminalmodusparameter ist ungültig.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALTIMEOUT"></span><span id="lineerr_invaltimeout"></span>**lineerr \_ invaltimeout**
</dt> <dd> <dl> <dt>



Timeouts werden nicht unterstützt, oder ein Wert liegt außerhalb des gültigen Bereichs, der in [**linedevcaps**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps)angegeben ist.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALTONE"></span><span id="lineerr_invaltone"></span>**lineerr \_ invaltone**
</dt> <dd> <dl> <dt>



Der angegebene benutzerdefinierte Farbton stellt keinen gültigen Ton dar oder besteht aus zu vielen Frequenzen, oder die angegebene Tonstruktur beschreibt keinen gültigen Ton.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALTONELIST"></span><span id="lineerr_invaltonelist"></span>**lineerr \_ invaltonelist**
</dt> <dd> <dl> <dt>



Die angegebene Tonliste ist ungültig.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALTONEMODE"></span><span id="lineerr_invaltonemode"></span>**lineerr \_ invaltonemode**
</dt> <dd> <dl> <dt>



Der angegebene Tone Mode-Parameter ist ungültig.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALTRANSFERMODE"></span><span id="lineerr_invaltransfermode"></span>**lineerr \_ invaltransfermode**
</dt> <dd> <dl> <dt>



Der angegebene Übertragungsmodus-Parameter ist ungültig.


</dt> </dl> </dd> <dt>

<span id="LINEERR_LINEMAPPERFAILED"></span><span id="lineerr_linemapperfailed"></span>**lineerr \_ linemapperfailed**
</dt> <dd> <dl> <dt>



Linemapper war der Wert, der im *dwdeviceid* -Parameter übergeben wurde, aber es wurden keine Zeilen gefunden, die den im *lpcallparameams* -Parameter angegebenen Anforderungen entsprechen.


</dt> </dl> </dd> <dt>

<span id="LINEERR_NOCONFERENCE"></span><span id="lineerr_noconference"></span>**lineerr \_ noconference**
</dt> <dd> <dl> <dt>



Der angegebene-Befehl ist kein Konferenz-oder Teilnehmer aufrufshandle.


</dt> </dl> </dd> <dt>

<span id="LINEERR_NODEVICE"></span><span id="lineerr_nodevice"></span>**lineerr- \_ nodevice**
</dt> <dd> <dl> <dt>



Der angegebene Geräte Bezeichner, der zuvor gültig war, wird nicht mehr akzeptiert, weil das zugehörige Gerät seit der letzten Initialisierung von TAPI aus dem System entfernt wurde. Alternativ weist das liniengerät kein zugeordnetes Gerät für die angegebene Geräteklasse auf.


</dt> </dl> </dd> <dt>

<span id="LINEERR_NODRIVER"></span><span id="lineerr_nodriver"></span>**lineerr- \_ nodriver**
</dt> <dd> <dl> <dt>



Entweder wurde Tapiaddr.dll nicht gefunden, oder der Telefon Dienstanbieter für das angegebene Gerät hat erkannt, dass eine der Komponenten fehlt oder beschädigt ist, weil Sie nicht während der Initialisierung erkannt wurde. Der Benutzer sollte aufgefordert werden, das Problem mithilfe der Telefonie-Systemsteuerung zu beheben.


</dt> </dl> </dd> <dt>

<span id="LINEERR_NOMEM"></span><span id="lineerr_nomem"></span>**lineerr \_ NOMEM**
</dt> <dd> <dl> <dt>



Nicht genügend Arbeitsspeicher zum Ausführen des Vorgangs, oder der Arbeitsspeicher kann nicht gesperrt werden.


</dt> </dl> </dd> <dt>

<span id="LINEERR_NOMULTIPLEINSTANCE"></span><span id="lineerr_nomultipleinstance"></span>**lineerr \_ nomultiplin Stance**
</dt> <dd> <dl> <dt>



Ein Telefoniedienstanbieter, der mehrere Instanzen nicht unterstützt, ist mehrmals im \[ Abschnitt "Anbieter" \] in der Registrierung aufgeführt. Die Anwendung sollte dem Benutzer die Verwendung der Telefonie-Systemsteuerung zum Entfernen des duplizierten Treibers empfehlen.


</dt> </dl> </dd> <dt>

<span id="LINEERR_NOMULTIPLEINSTANCE"></span><span id="lineerr_nomultipleinstance"></span>**lineerr \_ nomultiplin Stance**
</dt> <dd> <dl> <dt>



Mehrere Instanzen dieses Dienstanbieters sind nicht zulässig.


</dt> </dl> </dd> <dt>

<span id="LINEERR_NOREQUEST"></span><span id="lineerr_norequest"></span>**lineerr \_ norequest**
</dt> <dd> <dl> <dt>



Zurzeit steht keine Anforderung aus dem angegebenen Modus aus, oder die Anwendung ist nicht mehr die Anwendung mit der höchsten Priorität für den angegebenen Anforderungs Modus.


</dt> </dl> </dd> <dt>

<span id="LINEERR_NOTOWNER"></span><span id="lineerr_notowner"></span>**lineerr- \_ notowner**
</dt> <dd> <dl> <dt>



Die Anwendung verfügt nicht über die Berechtigung "Besitzer" für den angegebenen-Befehl.


</dt> </dl> </dd> <dt>

<span id="LINEERR_NOTREGISTERED"></span><span id="lineerr_notregistered"></span>**lineerr \_ notregistered**
</dt> <dd> <dl> <dt>



Die Anwendung ist nicht als Anforderungs Empfänger für den angezeigtem Anforderungs Modus registriert.


</dt> </dl> </dd> <dt>

<span id="LINEERR_OPERATIONFAILED"></span><span id="lineerr_operationfailed"></span>**lineerr- \_ operationfailed**
</dt> <dd> <dl> <dt>



Der Vorgang ist aus einem nicht angegebenen oder unbekannten Grund fehlgeschlagen.


</dt> </dl> </dd> <dt>

<span id="LINEERR_OPERATIONUNAVAIL"></span><span id="lineerr_operationunavail"></span>**lineerr \_ operationunnütz**
</dt> <dd> <dl> <dt>



Der Vorgang ist nicht verfügbar, z. b. für das angegebene Gerät oder die angegebene Zeile.


</dt> </dl> </dd> <dt>

<span id="LINEERR_RATEUNAVAIL"></span><span id="lineerr_rateunavail"></span>**lineerr \_ rateun-Anspruch**
</dt> <dd> <dl> <dt>



Der Dienstanbieter verfügt derzeit nicht über genügend Bandbreite für die angegebene Rate.


</dt> </dl> </dd> <dt>

<span id="LINEERR_REINIT"></span><span id="lineerr_reinit"></span>**lineerr \_ Reit**
</dt> <dd> <dl> <dt>



Wenn die TAPI-Neuinitialisierung angefordert wurde, z. b. aufgrund des Hinzufügens oder Entfernens eines Telefoniedienstanbieters, anschließend werden [**lineinitialize**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize)-, [**lineinitializeex**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa)-oder [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen) -Anforderungen mit diesem Fehler zurückgewiesen, bis die letzte Anwendung die Verwendung der API herunterfährt (mit [**LineShutdown**](/windows/desktop/api/Tapi/nf-tapi-lineshutdown)). zu diesem Zeitpunkt wird die neue Konfiguration wirksam, und Anwendungen können **lineinitialize** oder **lineinitializeex** aufrufen.


</dt> </dl> </dd> <dt>

<span id="LINEERR_REINIT"></span><span id="lineerr_reinit"></span>**lineerr \_ Reit**
</dt> <dd> <dl> <dt>



Die Anwendung hat versucht, TAPI zweimal zu initialisieren.


</dt> </dl> </dd> <dt>

<span id="LINEERR_REQUESTOVERRUN"></span><span id="lineerr_requestoverrun"></span>**lineerr \_ requestüberlauf**
</dt> <dd> <dl> <dt>



Es stehen weitere Anforderungen aus, die vom Gerät verarbeitet werden können.


</dt> </dl> </dd> <dt>

<span id="LINEERR_RESOURCEUNAVAIL"></span><span id="lineerr_resourceunavail"></span>**lineerr \_ resourceunnütz**
</dt> <dd> <dl> <dt>



Nicht genügend Ressourcen, um den Vorgang abzuschließen. Beispielsweise kann eine Zeile aufgrund einer dynamischen Ressourcen Übereinstimmung nicht geöffnet werden.


</dt> </dl> </dd> <dt>

<span id="LINEERR_STRUCTURETOOSMALL"></span><span id="lineerr_structuretoosmall"></span>**lineerr \_ structureumosmall**
</dt> <dd> <dl> <dt>



Der **dwtotalsize** -Member einer-Struktur gibt nicht genügend Arbeitsspeicher an, um den festgelegten Teil der angegebenen-Struktur zu enthalten.


</dt> </dl> </dd> <dt>

<span id="LINEERR_TARGETNOTFOUND"></span><span id="lineerr_targetnotfound"></span>**lineerr \_ targetnotfound**
</dt> <dd> <dl> <dt>



Es wurde kein Ziel für den calloff gefunden. Dies kann vorkommen, wenn die benannte Anwendung nicht dieselbe Zeile mit dem Besitzer des linecallprivilege- \_ Besitzers im *dwprivileges* -Parameter von [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen)geöffnet hat. Im Fall der Medien Modus-Übergabe hat keine Anwendung dieselbe Zeile mit dem Besitzer des linecallprivilege \_ -Besitzers im *dwprivileges* -Parameter von [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen) geöffnet, und der im *dwmediamode* -Parameter angegebene Medientyp wurde im *dwmediamodes* -Parameter von [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen)angegeben.


</dt> </dl> </dd> <dt>

<span id="LINEERR_TARGETSELF"></span><span id="lineerr_targetself"></span>**lineerr \_ targetSelf**
</dt> <dd> <dl> <dt>



Die Anwendung, die diesen Vorgang aufruft, ist das Ziel der indirekten Übergabe. Das heißt, TAPI hat festgestellt, dass die aufrufenden Anwendung auch die Anwendung mit der höchsten Priorität für den angegebenen Medientyp ist.


</dt> </dl> </dd> <dt>

<span id="LINEERR_UNINITIALIZED"></span><span id="lineerr_uninitialized"></span>**lineerr \_ nicht initialisiert**
</dt> <dd> <dl> <dt>



Der Vorgang wurde vor einer Anwendung mit dem Namen [**lineinitialize**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize) oder [**lineinitializeex**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa)aufgerufen.


</dt> </dl> </dd> <dt>

<span id="LINEERR_USERCANCELLED"></span><span id="lineerr_usercancelled"></span>**lineerr- \_ Benutzer abgebrochen**
</dt> <dd> <dl> <dt>



Der Benutzer hat den-Befehl abgebrochen. Dieser Wert ist nur für Anwendungen verfügbar, die eine TAPI-Version von 2,2 oder höher aushandeln.


</dt> </dl> </dd> <dt>

<span id="LINEERR_USERUSERINFOTOOBIG"></span><span id="lineerr_useruserinfotoobig"></span>**lineerr \_ useruserinfotoobig**
</dt> <dd> <dl> <dt>



Die Zeichenfolge, die Benutzer Benutzerinformationen enthält, überschreitet die maximale Anzahl von Bytes, die in den Elementen **dwuuiakzeptsize**, **dwuuibeantworsize**, **dwuuidropsize**, **dwuuimakecallsize** oder **dwuuisenduseruserinfosize** von [**linedevcaps**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps)angegeben sind, oder die Zeichenfolge, die Benutzer Benutzerinformationen enthält.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die Werte 0xC0000000 bis 0xffffffff sind für gerätespezifische Erweiterungen verfügbar. Die Werte 0x80000000 bis 0xBFFFFFFF sind reserviert, während 0x00000000 bis 0x7FFFFFFF als Anforderungs Bezeichner verwendet werden.

Wenn eine Anwendung eine Fehlermeldung erhält, die Sie nicht speziell behandelt (z. b. einen Fehler, der durch eine gerätespezifische Erweiterung definiert wurde), sollte Sie den Fehler als lineerr \_ operationfailed (aus einem nicht angegebenen Grund) behandeln.

Beim Aufrufen der lineerr- \_ Konstanten, die neu bei TAPI 3,0 sind, muss die Datei Tapierr.MC mit neuen Nachrichten aktualisiert werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2,0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Lineaddresscaps**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)
</dt> <dt>

[**Linedevcaps**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps)
</dt> <dt>

[**Linedevstatus**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus)
</dt> <dt>

[**linegetlinedevstatus**](/windows/desktop/api/Tapi/nf-tapi-linegetlinedevstatus)
</dt> <dt>

[**lineinitialize**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize)
</dt> <dt>

[**lineinitializeex**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa)
</dt> <dt>

[**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen)
</dt> <dt>

[**LineShutdown**](/windows/desktop/api/Tapi/nf-tapi-lineshutdown)
</dt> </dl>

 

 




