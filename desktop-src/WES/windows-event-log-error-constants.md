---
title: Windows-Ereignisprotokoll-Fehler Konstanten (Winerror. h)
description: Im folgenden finden Sie die Fehlercodes, die vom Windows-Ereignisprotokoll definiert werden.
ms.assetid: 889ea4ae-dede-45d5-9293-cec85d81f010
topic_type:
- apiref
api_name:
- ERROR_EVT_INVALID_CHANNEL_PATH
- ERROR_EVT_INVALID_QUERY
- ERROR_EVT_PUBLISHER_METADATA_NOT_FOUND
- ERROR_EVT_EVENT_TEMPLATE_NOT_FOUND
- ERROR_EVT_INVALID_PUBLISHER_NAME
- ERROR_EVT_INVALID_EVENT_DATA
- ERROR_EVT_CHANNEL_NOT_FOUND
- ERROR_EVT_MALFORMED_XML_TEXT
- ERROR_EVT_SUBSCRIPTION_TO_DIRECT_CHANNEL
- ERROR_EVT_CONFIGURATION_ERROR
- ERROR_EVT_QUERY_RESULT_STALE
- ERROR_EVT_QUERY_RESULT_INVALID_POSITION
- ERROR_EVT_NON_VALIDATING_MSXML
- ERROR_EVT_FILTER_ALREADYSCOPED
- ERROR_EVT_FILTER_NOTELTSET
- ERROR_EVT_FILTER_INVARG
- ERROR_EVT_FILTER_INVTEST
- ERROR_EVT_FILTER_INVTYPE
- ERROR_EVT_FILTER_PARSEERR
- ERROR_EVT_FILTER_UNSUPPORTEDOP
- ERROR_EVT_FILTER_UNEXPECTEDTOKEN
- ERROR_EVT_INVALID_OPERATION_OVER_ENABLED_DIRECT_CHANNEL
- ERROR_EVT_INVALID_CHANNEL_PROPERTY_VALUE
- ERROR_EVT_INVALID_PUBLISHER_PROPERTY_VALUE
- ERROR_EVT_CHANNEL_CANNOT_ACTIVATE
- ERROR_EVT_FILTER_TOO_COMPLEX
- ERROR_EVT_MESSAGE_NOT_FOUND
- ERROR_EVT_MESSAGE_ID_NOT_FOUND
- ERROR_EVT_UNRESOLVED_VALUE_INSERT
- ERROR_EVT_UNRESOLVED_PARAMETER_INSERT
- ERROR_EVT_MAX_INSERTS_REACHED
- ERROR_EVT_EVENT_DEFINITION_NOT_FOUND
- ERROR_EVT_MESSAGE_LOCALE_NOT_FOUND
- ERROR_EVT_VERSION_TOO_OLD
- ERROR_EVT_VERSION_TOO_NEW
- ERROR_EVT_CANNOT_OPEN_CHANNEL_OF_QUERY
- ERROR_EVT_PUBLISHER_DISABLED
- ERROR_EVT_FILTER_OUT_OF_RANGE
api_location:
- WinError.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efa5443d98c53d6abedbe3a0027e8e2e524ae9df
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106343883"
---
# <a name="windows-event-log-error-constants"></a>Fehler Konstanten im Windows-Ereignisprotokoll

Im folgenden finden Sie die Fehlercodes, die vom Windows-Ereignisprotokoll definiert werden.

<dl> <dt>

<span id="ERROR_EVT_INVALID_CHANNEL_PATH"></span><span id="error_evt_invalid_channel_path"></span>**Fehler beim Auftreten eines \_ \_ ungültigen \_ Kanal \_ Pfads.**
</dt> <dd> <dl> <dt>

15000
</dt> <dt>



Der angegebene Kanalpfad ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_INVALID_QUERY"></span><span id="error_evt_invalid_query"></span>**Fehler beim Auftreten einer \_ \_ ungültigen \_ Abfrage**
</dt> <dd> <dl> <dt>

15001
</dt> <dt>



Die angegebene Abfrage ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_PUBLISHER_METADATA_NOT_FOUND"></span><span id="error_evt_publisher_metadata_not_found"></span>**Fehler beim Auftreten von \_ \_ Verleger \_ Metadaten \_ nicht \_ gefunden.**
</dt> <dd> <dl> <dt>

15002
</dt> <dt>



Die Anbieter Metadaten wurden in der Ressource nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_EVENT_TEMPLATE_NOT_FOUND"></span><span id="error_evt_event_template_not_found"></span>**Fehler \_ Ereignis Vorlage "Fehler Ereignis" wurde \_ \_ \_ nicht \_ gefunden.**
</dt> <dd> <dl> <dt>

15003
</dt> <dt>



Die Vorlage für eine Ereignis Definition wurde in der Ressource nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_INVALID_PUBLISHER_NAME"></span><span id="error_evt_invalid_publisher_name"></span>**\_ \_ ungültiger \_ Herausgeber \_ Name**
</dt> <dd> <dl> <dt>

15004
</dt> <dt>



Der angegebene Anbieter Name ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_INVALID_EVENT_DATA"></span><span id="error_evt_invalid_event_data"></span>**Fehler beim Auftreten von \_ \_ ungültigen \_ Ereignis \_ Daten.**
</dt> <dd> <dl> <dt>

15005
</dt> <dt>



Die Ereignisdaten, die vom Anbieter ausgelöst werden, sind nicht mit der Definition der Ereignis Vorlage im Manifest des Anbieters kompatibel.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_CHANNEL_NOT_FOUND"></span><span id="error_evt_channel_not_found"></span>**Fehler beim \_ EVT- \_ Kanal \_ nicht \_ gefunden.**
</dt> <dd> <dl> <dt>

15007
</dt> <dt>



Der angegebene Kanal wurde nicht gefunden. Überprüfen Sie die Kanal Konfiguration.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_MALFORMED_XML_TEXT"></span><span id="error_evt_malformed_xml_text"></span>**fehlerhafter \_ \_ XML- \_ \_ Text Fehler.**
</dt> <dd> <dl> <dt>

15008
</dt> <dt>



Der angegebene XML-Text war nicht wohl geformt. Weitere Informationen erhalten Sie, wenn Sie die [**evtgetextendedstatus**](/windows/desktop/api/WinEvt/nf-winevt-evtgetextendedstatus) -Funktion aufrufen.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_SUBSCRIPTION_TO_DIRECT_CHANNEL"></span><span id="error_evt_subscription_to_direct_channel"></span>**Fehler " \_ evt"- \_ Abonnement \_ für \_ direkten \_ Kanal**
</dt> <dd> <dl> <dt>

15009
</dt> <dt>



Sie können einen analytischen oder Debug-Kanal nicht abonnieren. die Ereignisse für einen Analyse-oder Debugkanal gelangen direkt in eine Protokolldatei und können nicht abonniert werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_CONFIGURATION_ERROR"></span><span id="error_evt_configuration_error"></span>**Fehler bei \_ EVT- \_ Konfigurations \_ Fehler**
</dt> <dd> <dl> <dt>

15010
</dt> <dt>



Konfigurationsfehler.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_QUERY_RESULT_STALE"></span><span id="error_evt_query_result_stale"></span>**Fehler beim auslassen der \_ \_ Abfrage \_ Ergebnisse \_**
</dt> <dd> <dl> <dt>

15011
</dt> <dt>



Das Abfrageergebnis ist ungültig. Dies kann darauf zurückzuführen sein, dass das Protokoll gelöscht oder ein Rollback ausgeführt wird, nachdem das Abfrageergebnis erstellt wurde. Geben Sie das Abfrageergebnis Objekt frei, und wiederholen Sie die Abfrage.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_QUERY_RESULT_INVALID_POSITION"></span><span id="error_evt_query_result_invalid_position"></span>**Fehler bei der \_ \_ Abfrage \_ Ergebnis \_ ungültige \_ Position**
</dt> <dd> <dl> <dt>

15012
</dt> <dt>



Der Cursor für das Abfrageergebnis verweist nicht auf eine gültige Position.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_NON_VALIDATING_MSXML"></span><span id="error_evt_non_validating_msxml"></span>**Fehler beim \_ \_ nicht \_ Validieren von \_ MSXML.**
</dt> <dd> <dl> <dt>

15013
</dt> <dt>



Der registrierte MSXML-Parser unterstützt keine Validierung.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_ALREADYSCOPED"></span><span id="error_evt_filter_alreadyscoped"></span>**Fehler beim Filtern von " \_ \_ \_ alread-scoped".**
</dt> <dd> <dl> <dt>

15014
</dt> <dt>



Auf einen Ausdruck kann nur dann eine Änderung des Bereichs Vorgangs angewendet werden, wenn der Ausdruck zu einer Knotengruppe ausgewertet wird und nicht bereits Teil einer anderen Änderung des Bereichs Vorgangs ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_NOTELTSET"></span><span id="error_evt_filter_noteltset"></span>**Fehler beim \_ \_ Filtern von \_ noteltset.**
</dt> <dd> <dl> <dt>

15015
</dt> <dt>



Ein Schritt Vorgang kann nicht von einem Begriff durchgeführt werden, der keinen Element Satz darstellt.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_INVARG"></span><span id="error_evt_filter_invarg"></span>**Fehler " \_ EVT Filter"- \_ Filter \_**
</dt> <dd> <dl> <dt>

15016
</dt> <dt>



Die Argumente auf der linken Seite eines binären Operators müssen entweder Attribute, Knoten oder Variablen sein, und die Argumente auf der rechten Seite müssen Konstanten sein.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_INVTEST"></span><span id="error_evt_filter_invtest"></span>**Fehler beim \_ \_ Filter zum Filtern \_ .**
</dt> <dd> <dl> <dt>

15017
</dt> <dt>



Ein Schritt Vorgang muss entweder einen Knoten Test oder, im Falle eines Prädikats, einen algebraischen Ausdruck einschließen, mit dem jeder Knoten in der Knotengruppe, der durch den vorherigen Knoten Satz identifiziert wird, getestet werden kann.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_INVTYPE"></span><span id="error_evt_filter_invtype"></span>**\_ \_ Fehlertyp \_ Filtertyp Filtern**
</dt> <dd> <dl> <dt>

15018
</dt> <dt>



Dieser Datentyp wird nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_PARSEERR"></span><span id="error_evt_filter_parseerr"></span>**Fehler beim \_ \_ Filtern der \_ parameterr**
</dt> <dd> <dl> <dt>

15019
</dt> <dt>



An der angegebenen Position ist ein Syntax Fehler aufgetreten.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_UNSUPPORTEDOP"></span><span id="error_evt_filter_unsupportedop"></span>**Fehler beim Filtern von " \_ \_ \_ unsupportedop".**
</dt> <dd> <dl> <dt>

15020
</dt> <dt>



Dieser Operator wird von dieser Implementierung des Filters nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_UNEXPECTEDTOKEN"></span><span id="error_evt_filter_unexpectedtoken"></span>**Fehler beim Filtern von " \_ \_ \_ unexpectedtoken".**
</dt> <dd> <dl> <dt>

15021
</dt> <dt>



Unerwartetes Token.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_INVALID_OPERATION_OVER_ENABLED_DIRECT_CHANNEL"></span><span id="error_evt_invalid_operation_over_enabled_direct_channel"></span>**Fehler durch \_ \_ ungültigen \_ Vorgang \_ über \_ aktiviertem \_ direkt \_ Kanal**
</dt> <dd> <dl> <dt>

15022
</dt> <dt>



Der angeforderte Vorgang kann nicht über einen aktivierten Analyse-oder Debugkanal ausgeführt werden. Sie müssen den Kanal deaktivieren, bevor Sie den angeforderten Vorgang ausführen.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_INVALID_CHANNEL_PROPERTY_VALUE"></span><span id="error_evt_invalid_channel_property_value"></span>**Error \_ EVT \_ ungültiger \_ \_ channeleigenschafts \_ Wert.**
</dt> <dd> <dl> <dt>

15023
</dt> <dt>



Die Channeleigenschaft enthält einen ungültigen Wert. Der Werttyp ist möglicherweise nicht gültig, der Wert liegt möglicherweise außerhalb des gültigen Bereichs, oder der Wert kann nicht aktualisiert werden oder wird für diesen Kanaltyp nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_INVALID_PUBLISHER_PROPERTY_VALUE"></span><span id="error_evt_invalid_publisher_property_value"></span>**Error \_ EVT \_ ungültiger \_ Verleger \_ Eigenschafts \_ Wert.**
</dt> <dd> <dl> <dt>

15024
</dt> <dt>



Die Provider-Eigenschaft enthält einen ungültigen Wert. Der Werttyp ist möglicherweise nicht gültig, der Wert liegt möglicherweise außerhalb des gültigen Bereichs, oder der Wert kann nicht aktualisiert werden oder wird für diesen Anbietertyp nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_CHANNEL_CANNOT_ACTIVATE"></span><span id="error_evt_channel_cannot_activate"></span>**\_fehlerevt- \_ Kanal \_ kann nicht \_ aktiviert werden.**
</dt> <dd> <dl> <dt>

15025
</dt> <dt>



Der Kanal konnte nicht aktiviert werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_TOO_COMPLEX"></span><span id="error_evt_filter_too_complex"></span>**Fehler beim \_ \_ Filter \_ zu \_ Komplex.**
</dt> <dd> <dl> <dt>

15026
</dt> <dt>



Der XPath-Ausdruck hat unterstützte Komplexität überschritten. Vereinfachen Sie den Ausdruck, oder Teilen Sie ihn in zwei oder mehr einfache Ausdrücke auf.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_MESSAGE_NOT_FOUND"></span><span id="error_evt_message_not_found"></span>**Fehler \_ Meldung "evt" wurde \_ \_ nicht \_ gefunden.**
</dt> <dd> <dl> <dt>

15027
</dt> <dt>



Die Nachrichten Ressource ist vorhanden, aber die Nachricht wurde nicht in der Zeichenfolge oder in der Nachrichten Tabelle gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_MESSAGE_ID_NOT_FOUND"></span><span id="error_evt_message_id_not_found"></span>**Fehler- \_ EVT-nach \_ richten- \_ ID \_ nicht \_ gefunden.**
</dt> <dd> <dl> <dt>

15028
</dt> <dt>



Die Nachrichten-ID wurde nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_UNRESOLVED_VALUE_INSERT"></span><span id="error_evt_unresolved_value_insert"></span>**Fehler beim Einfügen von nicht aufgelösten \_ \_ \_ Werten. \_**
</dt> <dd> <dl> <dt>

15029
</dt> <dt>



Die Ersetzungs Zeichenfolge für den Einfügeindex wurde nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_UNRESOLVED_PARAMETER_INSERT"></span><span id="error_evt_unresolved_parameter_insert"></span>**Fehler beim \_ Einfügen nicht \_ aufgelöster \_ Parameter \_ .**
</dt> <dd> <dl> <dt>

15030
</dt> <dt>



Die Beschreibungs Zeichenfolge für den Parameter Verweis (%1) wurde nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_MAX_INSERTS_REACHED"></span><span id="error_evt_max_inserts_reached"></span>**\_Maximale Anzahl von \_ \_ Einfügungen des \_ Fehlers**
</dt> <dd> <dl> <dt>

15031
</dt> <dt>



Die maximal zulässige Anzahl von Ersetzungen wurde erreicht.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_EVENT_DEFINITION_NOT_FOUND"></span><span id="error_evt_event_definition_not_found"></span>**Fehler \_ Ereignis- \_ Ereignis \_ Definition \_ nicht \_ gefunden.**
</dt> <dd> <dl> <dt>

15032
</dt> <dt>



Die Ereignis Definition für den Ereignis Bezeichner wurde nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_MESSAGE_LOCALE_NOT_FOUND"></span><span id="error_evt_message_locale_not_found"></span>**Fehler beim \_ EVT-Nachrichten Gebiets Schema \_ \_ \_ nicht \_ gefunden.**
</dt> <dd> <dl> <dt>

15033
</dt> <dt>



Die Gebiets Schema spezifische Ressource für die gewünschte Nachricht ist nicht vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_VERSION_TOO_OLD"></span><span id="error_evt_version_too_old"></span>**Fehler- \_ EVT- \_ Version \_ zu \_ alt**
</dt> <dd> <dl> <dt>

15034
</dt> <dt>



Die Ressource ist zu alt, um kompatibel zu sein.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_VERSION_TOO_NEW"></span><span id="error_evt_version_too_new"></span>**Fehler- \_ EVT- \_ Version \_ zu \_ neu**
</dt> <dd> <dl> <dt>

15035
</dt> <dt>



Die Ressource ist zu neu, um kompatibel zu sein.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_CANNOT_OPEN_CHANNEL_OF_QUERY"></span><span id="error_evt_cannot_open_channel_of_query"></span>**Fehler \_ EVT \_ kann \_ den \_ Kanal \_ der \_ Abfrage nicht öffnen.**
</dt> <dd> <dl> <dt>

15036
</dt> <dt>



Der Kanal am angegebenen Index der Abfrage kann nicht geöffnet werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_PUBLISHER_DISABLED"></span><span id="error_evt_publisher_disabled"></span>**Fehler beim \_ Deaktivieren des \_ Verlegers \_**
</dt> <dd> <dl> <dt>

15037
</dt> <dt>



Der Anbieter wurde deaktiviert, und die zugehörigen Ressourcen sind nicht verfügbar. Dies kann vorkommen, wenn der Anbieter deinstalliert oder aktualisiert wird.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_OUT_OF_RANGE"></span><span id="error_evt_filter_out_of_range"></span>**Fehler beim \_ \_ Filtern \_ \_ im \_ Bereich.**
</dt> <dd> <dl> <dt>

15038
</dt> <dt>



Es wurde versucht, einen numerischen Typ zu erstellen, der außerhalb des gültigen Bereichs liegt.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Winerror. h</dt> </dl> |



 

 





