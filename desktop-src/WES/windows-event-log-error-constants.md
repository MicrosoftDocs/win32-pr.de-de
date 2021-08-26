---
title: Windows Ereignisprotokollfehlerkonst constants (WinError.h)
description: Im Folgenden finden Sie die Fehlercodes, die Windows Ereignisprotokoll definiert.
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
ms.openlocfilehash: e0f6f0bd3e2805c02dad78c064b56a443bfbb596cf42f25e9b52ac7ba584f123
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120031940"
---
# <a name="windows-event-log-error-constants"></a>Windows Ereignisprotokollfehlerkonst constants

Im Folgenden finden Sie die Fehlercodes, die Windows Ereignisprotokoll definiert.

<dl> <dt>

<span id="ERROR_EVT_INVALID_CHANNEL_PATH"></span><span id="error_evt_invalid_channel_path"></span>**FEHLER \_ EVT \_ \_ UNGÜLTIGER \_ KANALPFAD**
</dt> <dd> <dl> <dt>

15000
</dt> <dt>



Der angegebene Kanalpfad ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_INVALID_QUERY"></span><span id="error_evt_invalid_query"></span>**FEHLER \_ EVT \_ UNGÜLTIGE \_ ABFRAGE**
</dt> <dd> <dl> <dt>

15001
</dt> <dt>



Die angegebene Abfrage ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_PUBLISHER_METADATA_NOT_FOUND"></span><span id="error_evt_publisher_metadata_not_found"></span>**FEHLER \_ EVT \_ PUBLISHER METADATA NOT \_ \_ \_ FOUND**
</dt> <dd> <dl> <dt>

15002
</dt> <dt>



Die Anbietermetadaten können in der Ressource nicht gefunden werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_EVENT_TEMPLATE_NOT_FOUND"></span><span id="error_evt_event_template_not_found"></span>**FEHLER \_ \_ EVT-EREIGNISVORLAGE \_ \_ NICHT \_ GEFUNDEN**
</dt> <dd> <dl> <dt>

15003
</dt> <dt>



Die Vorlage für eine Ereignisdefinition wurde in der Ressource nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_INVALID_PUBLISHER_NAME"></span><span id="error_evt_invalid_publisher_name"></span>**FEHLER \_ EVT \_ UNGÜLTIGER \_ \_ HERAUSGEBERNAME**
</dt> <dd> <dl> <dt>

15004
</dt> <dt>



Der angegebene Anbietername ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_INVALID_EVENT_DATA"></span><span id="error_evt_invalid_event_data"></span>**FEHLER \_ EVT \_ INVALID EVENT \_ \_ DATA**
</dt> <dd> <dl> <dt>

15005
</dt> <dt>



Die vom Anbieter ausgelösten Ereignisdaten sind nicht mit der Ereignisvorlagendefinition im Manifest des Anbieters kompatibel.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_CHANNEL_NOT_FOUND"></span><span id="error_evt_channel_not_found"></span>**FEHLER \_ \_ EVT-KANAL \_ NICHT \_ GEFUNDEN**
</dt> <dd> <dl> <dt>

15007
</dt> <dt>



Der angegebene Kanal wurde nicht gefunden. Überprüfen Sie die Kanalkonfiguration.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_MALFORMED_XML_TEXT"></span><span id="error_evt_malformed_xml_text"></span>**FEHLER \_ EVT \_ FALSCH FORMATIERTEN \_ \_ XML-TEXT**
</dt> <dd> <dl> <dt>

15008
</dt> <dt>



Der angegebene XML-Text war nicht wohlgeformt. Um weitere Informationen zu erhalten, rufen Sie die [**EvtGetExtendedStatus-Funktion**](/windows/desktop/api/WinEvt/nf-winevt-evtgetextendedstatus) auf.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_SUBSCRIPTION_TO_DIRECT_CHANNEL"></span><span id="error_evt_subscription_to_direct_channel"></span>**FEHLER BEIM \_ \_ EVT-ABONNEMENT \_ ZUM DIREKTEN \_ \_ KANAL**
</dt> <dd> <dl> <dt>

15009
</dt> <dt>



Sie können keinen Analyse- oder Debugkanal abonnieren. Die Ereignisse für einen Analyse- oder Debugkanal werden direkt an eine Protokolldatei übertragen und können nicht abonniert werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_CONFIGURATION_ERROR"></span><span id="error_evt_configuration_error"></span>**FEHLER \_ BEIM \_ EVT-KONFIGURATIONSFEHLER \_**
</dt> <dd> <dl> <dt>

15010
</dt> <dt>



Konfigurationsfehler.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_QUERY_RESULT_STALE"></span><span id="error_evt_query_result_stale"></span>**FEHLER \_ EVT \_ QUERY RESULT \_ \_ STALE**
</dt> <dd> <dl> <dt>

15011
</dt> <dt>



Das Abfrageergebnis ist ungültig. Dies kann daran liegt, dass das Protokoll nach dem Erstellen des Abfrageergebnisses bzw. rolliert wird. Geben Sie das Abfrageergebnisobjekt frei, und führen Sie die Abfrage erneut aus.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_QUERY_RESULT_INVALID_POSITION"></span><span id="error_evt_query_result_invalid_position"></span>**FEHLER \_ BEIM \_ EVT-ABFRAGEERGEBNIS \_ \_ UNGÜLTIGE \_ POSITION**
</dt> <dd> <dl> <dt>

15012
</dt> <dt>



Der Cursor für das Abfrageergebniszeigert nicht auf eine gültige Position.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_NON_VALIDATING_MSXML"></span><span id="error_evt_non_validating_msxml"></span>**FEHLER \_ EVT \_ NICHT ÜBERPRÜFEN \_ MSXML \_**
</dt> <dd> <dl> <dt>

15013
</dt> <dt>



Der registrierte MSXML Parser unterstützt keine Validierung.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_ALREADYSCOPED"></span><span id="error_evt_filter_alreadyscoped"></span>**FEHLER \_ EVT \_ FILTER \_ ALREADYSCOPED**
</dt> <dd> <dl> <dt>

15014
</dt> <dt>



Auf einen Ausdruck kann nur dann eine Änderung des Bereichsvorgang folgen, wenn der Ausdruck zu einem Knotensatz ausgewertet wird und nicht bereits Teil einer anderen Änderung des Bereichsvorgang ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_NOTELTSET"></span><span id="error_evt_filter_noteltset"></span>**FEHLER \_ EVT \_ FILTER \_ NOTELTSET**
</dt> <dd> <dl> <dt>

15015
</dt> <dt>



Ein Schrittvorgang kann nicht aus einem Begriff durchgeführt werden, der keinen Elementsatz repräsentiert.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_INVARG"></span><span id="error_evt_filter_invarg"></span>**FEHLER \_ BEIM \_ EVT-FILTER \_ INVARG**
</dt> <dd> <dl> <dt>

15016
</dt> <dt>



Die Argumente auf der linken Seite eines binären Operators müssen Attribute, Knoten oder Variablen sein, und die Argumente auf der rechten Seite müssen Konstanten sein.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_INVTEST"></span><span id="error_evt_filter_invtest"></span>**FEHLER \_ BEIM \_ EVT-FILTER \_ INVTEST**
</dt> <dd> <dl> <dt>

15017
</dt> <dt>



Ein Schrittvorgang muss entweder einen Knotentest oder im Fall eines Prädikats einen algebraischen Ausdruck umfassen, mit dem jeder Knoten in der Knotensatz, der durch die vorangehende Knotensatz identifiziert wird, überprüft werden kann.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_INVTYPE"></span><span id="error_evt_filter_invtype"></span>**FEHLER \_ BEIM \_ EVT-FILTER \_ INVTYPE**
</dt> <dd> <dl> <dt>

15018
</dt> <dt>



Dieser Datentyp wird nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_PARSEERR"></span><span id="error_evt_filter_parseerr"></span>**FEHLER \_ EVT \_ FILTER \_ PARSEERR**
</dt> <dd> <dl> <dt>

15019
</dt> <dt>



An der angegebenen Position ist ein Syntaxfehler aufgetreten.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_UNSUPPORTEDOP"></span><span id="error_evt_filter_unsupportedop"></span>**FEHLER \_ EVT \_ FILTER \_ UNSUPPORTEDOP**
</dt> <dd> <dl> <dt>

15020
</dt> <dt>



Dieser Operator wird von dieser Implementierung des Filters nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_UNEXPECTEDTOKEN"></span><span id="error_evt_filter_unexpectedtoken"></span>**FEHLER \_ EVT \_ FILTER \_ UNEXPECTEDTOKEN**
</dt> <dd> <dl> <dt>

15021
</dt> <dt>



Das gefundene Token war unerwartet.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_INVALID_OPERATION_OVER_ENABLED_DIRECT_CHANNEL"></span><span id="error_evt_invalid_operation_over_enabled_direct_channel"></span>**FEHLER \_ EVT \_ \_ UNGÜLTIGER VORGANG \_ ÜBER \_ AKTIVIERTEN DIREKTEN \_ \_ KANAL**
</dt> <dd> <dl> <dt>

15022
</dt> <dt>



Der angeforderte Vorgang kann nicht über einen aktivierten Analyse- oder Debugkanal ausgeführt werden. Sie müssen den Kanal deaktivieren, bevor Sie den angeforderten Vorgang ausführen.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_INVALID_CHANNEL_PROPERTY_VALUE"></span><span id="error_evt_invalid_channel_property_value"></span>**FEHLER \_ EVT \_ UNGÜLTIGER \_ \_ \_ KANALEIGENSCHAFTSWERT**
</dt> <dd> <dl> <dt>

15023
</dt> <dt>



Die Channeleigenschaft enthält einen ungültigen Wert. Der Typ des Werts ist möglicherweise ungültig, der Wert liegt möglicherweise nicht im gültigen Bereich, oder der Wert kann nicht aktualisiert werden oder wird für diesen Kanaltyp nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_INVALID_PUBLISHER_PROPERTY_VALUE"></span><span id="error_evt_invalid_publisher_property_value"></span>**FEHLER \_ EVT \_ UNGÜLTIGER \_ \_ \_ VERLEGEREIGENSCHAFTSWERT**
</dt> <dd> <dl> <dt>

15024
</dt> <dt>



Die Anbietereigenschaft enthält einen ungültigen Wert. Der Typ des Werts ist möglicherweise ungültig, der Wert liegt möglicherweise nicht im gültigen Bereich, oder der Wert kann nicht aktualisiert werden oder wird für diesen Anbietertyp nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_CHANNEL_CANNOT_ACTIVATE"></span><span id="error_evt_channel_cannot_activate"></span>**\_FEHLER: \_ EVT-KANAL \_ KANN NICHT AKTIVIERT \_ WERDEN**
</dt> <dd> <dl> <dt>

15025
</dt> <dt>



Fehler beim Aktivieren des Kanals.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_TOO_COMPLEX"></span><span id="error_evt_filter_too_complex"></span>**FEHLER \_ BEIM \_ EVT-FILTER \_ ZU \_ KOMPLEX**
</dt> <dd> <dl> <dt>

15026
</dt> <dt>



Der XPath-Ausdruck hat die unterstützte Komplexität überschritten. Vereinfachen Sie den Ausdruck, oder teilen Sie ihn in zwei oder mehr einfache Ausdrücke auf.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_MESSAGE_NOT_FOUND"></span><span id="error_evt_message_not_found"></span>**FEHLER \_ EVT \_ MESSAGE NOT \_ \_ FOUND**
</dt> <dd> <dl> <dt>

15027
</dt> <dt>



Die Nachrichtenressource ist vorhanden, aber die Nachricht wurde in der Zeichenfolge oder Meldungstabelle nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_MESSAGE_ID_NOT_FOUND"></span><span id="error_evt_message_id_not_found"></span>**FEHLER \_ EVT \_ MESSAGE ID NOT \_ \_ \_ FOUND**
</dt> <dd> <dl> <dt>

15028
</dt> <dt>



Der Nachrichtenbezeichner wurde nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_UNRESOLVED_VALUE_INSERT"></span><span id="error_evt_unresolved_value_insert"></span>**FEHLER \_ BEIM EINFÜGEN EINES NICHT \_ \_ AUFGELÖSTEN \_ WERTS**
</dt> <dd> <dl> <dt>

15029
</dt> <dt>



Die Ersetzungszeichenfolge für den Einfügeindex wurde nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_UNRESOLVED_PARAMETER_INSERT"></span><span id="error_evt_unresolved_parameter_insert"></span>**FEHLER \_ BEIM EINFÜGEN DES NICHT \_ \_ AUFGELÖSTEN PARAMETERS \_ EVT**
</dt> <dd> <dl> <dt>

15030
</dt> <dt>



Die Beschreibungszeichenfolge für den Parameterverweis (%1) wurde nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_MAX_INSERTS_REACHED"></span><span id="error_evt_max_inserts_reached"></span>**FEHLER \_ EVT \_ MAX \_ INSERTS \_ ERREICHT**
</dt> <dd> <dl> <dt>

15031
</dt> <dt>



Die maximale Anzahl von Ersetzungen wurde erreicht.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_EVENT_DEFINITION_NOT_FOUND"></span><span id="error_evt_event_definition_not_found"></span>**FEHLER \_ \_ EVT-EREIGNISDEFINITION \_ \_ NICHT \_ GEFUNDEN**
</dt> <dd> <dl> <dt>

15032
</dt> <dt>



Die Ereignisdefinition für den Ereignisbezeichner wurde nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_MESSAGE_LOCALE_NOT_FOUND"></span><span id="error_evt_message_locale_not_found"></span>**FEHLER \_ EVT \_ MESSAGE \_ LOCALE NOT \_ \_ FOUND**
</dt> <dd> <dl> <dt>

15033
</dt> <dt>



Die lokale Ressource für die gewünschte Nachricht ist nicht vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_VERSION_TOO_OLD"></span><span id="error_evt_version_too_old"></span>**FEHLER \_ \_ EVT-VERSION \_ ZU \_ ALT**
</dt> <dd> <dl> <dt>

15034
</dt> <dt>



Die Ressource ist zu alt, um kompatibel zu sein.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_VERSION_TOO_NEW"></span><span id="error_evt_version_too_new"></span>**FEHLER \_ \_ EVT-VERSION \_ ZU \_ NEU**
</dt> <dd> <dl> <dt>

15035
</dt> <dt>



Die Ressource ist zu neu, um kompatibel zu sein.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_CANNOT_OPEN_CHANNEL_OF_QUERY"></span><span id="error_evt_cannot_open_channel_of_query"></span>**FEHLER \_ BEIM ÖFFNEN DES \_ \_ \_ ABFRAGEKANALS \_ DURCH \_ EVT**
</dt> <dd> <dl> <dt>

15036
</dt> <dt>



Der Kanal am angegebenen Index der Abfrage kann nicht geöffnet werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_PUBLISHER_DISABLED"></span><span id="error_evt_publisher_disabled"></span>**FEHLER \_ EVT \_ PUBLISHER \_ DISABLED**
</dt> <dd> <dl> <dt>

15037
</dt> <dt>



Der Anbieter wurde deaktiviert, und seine Ressourcen sind nicht verfügbar. Dies kann auftreten, wenn der Anbieter deinstalliert oder aktualisiert wird.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_OUT_OF_RANGE"></span><span id="error_evt_filter_out_of_range"></span>**FEHLER \_ EVT \_ FILTER OUT OF \_ \_ \_ RANGE**
</dt> <dd> <dl> <dt>

15038
</dt> <dt>



Es wurde versucht, einen numerischen Typ zu erstellen, der sich außerhalb seines gültigen Bereichs befindet.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>WinError.h</dt> </dl> |



 

 





