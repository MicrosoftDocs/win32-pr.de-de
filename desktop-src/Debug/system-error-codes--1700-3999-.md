---
description: Beschreibt die in der Header Datei "Winerror. h" definierten Fehlercodes 1700-3999 und ist für Entwickler bestimmt.
ms.assetid: 7e57c087-53e4-443d-9227-21d9eb3cc71f
title: System Fehler Codes (1700-3999) (Winerror. h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: 23b90db71a6e2e84b28f4aafc94475e9e82e3e7a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860672"
---
# <a name="system-error-codes-1700-3999"></a>System Fehler Codes (1700-3999)

> [!NOTE]
> Diese Informationen sind für Entwickler gedacht, die Systemfehler Debuggen. Bei anderen Fehlern, wie z. b. Problemen mit Windows Update, finden Sie eine Liste der Ressourcen auf der Seite [Fehlercodes](system-error-codes.md) .

In der folgenden Liste werden die [Systemfehler Codes](system-error-codes.md) für die Fehler 1700 bis 3999 beschrieben. Sie werden von der [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) -Funktion zurückgegeben, wenn viele Funktionen fehlschlagen. Um den Beschreibungstext für den Fehler in Ihrer Anwendung abzurufen, verwenden Sie die [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) -Funktion mit dem Flag " **Format \_ Message \_ from \_ System** ".

<dl> <dt>

<span id="RPC_S_INVALID_STRING_BINDING"></span><span id="rpc_s_invalid_string_binding"></span>**\_ \_ ungültige \_ Zeichen folgen \_ Bindung für RPC S**
</dt> <dd> <dl> <dt>

1700 (0x6a4)
</dt> <dt>



Die Zeichen folgen Bindung ist ungültig.


</dt> </dl> </dd> <dt>

<span id="RPC_S_WRONG_KIND_OF_BINDING"></span><span id="rpc_s_wrong_kind_of_binding"></span>**\_falsche RPC \_ - \_ Art \_ der \_ Bindung**
</dt> <dd> <dl> <dt>

1701 (0x6a5)
</dt> <dt>



Das Bindungs Handle ist nicht der richtige Typ.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INVALID_BINDING"></span><span id="rpc_s_invalid_binding"></span>**\_ungültige RPC S- \_ \_ Bindung**
</dt> <dd> <dl> <dt>

1702 (0x6a6)
</dt> <dt>



Das Bindungs Handle ist ungültig.


</dt> </dl> </dd> <dt>

<span id="RPC_S_PROTSEQ_NOT_SUPPORTED"></span><span id="rpc_s_protseq_not_supported"></span>**"RPC \_ S \_ Prot* \_ " \_ wird nicht unterstützt.**
</dt> <dd> <dl> <dt>

1703 (0x6a7)
</dt> <dt>



Die RPC-Protokoll Sequenz wird nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INVALID_RPC_PROTSEQ"></span><span id="rpc_s_invalid_rpc_protseq"></span>**RPC- \_ S- \_ ungültige \_ RPC- \_ protsek.**
</dt> <dd> <dl> <dt>

1704 (0x6a8)
</dt> <dt>



Die RPC-Protokoll Sequenz ist ungültig.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INVALID_STRING_UUID"></span><span id="rpc_s_invalid_string_uuid"></span>**\_ \_ ungültige RPC- \_ Zeichenfolge ( \_ UUID)**
</dt> <dd> <dl> <dt>

1705 (0x6a9)
</dt> <dt>



Der Zeichen folgen-Universal Unique Identifier (UUID) ist ungültig.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INVALID_ENDPOINT_FORMAT"></span><span id="rpc_s_invalid_endpoint_format"></span>**\_ \_ ungültiges \_ Endpunkt \_ Format für RPC-S**
</dt> <dd> <dl> <dt>

1706 (0x6aa)
</dt> <dt>



Das Endpunkt Format ist ungültig.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INVALID_NET_ADDR"></span><span id="rpc_s_invalid_net_addr"></span>**\_Netzwerk- \_ \_ \_ addr ist ungültig.**
</dt> <dd> <dl> <dt>

1707 (0x6ab)
</dt> <dt>



Die Netzwerkadresse ist ungültig.


</dt> </dl> </dd> <dt>

<span id="RPC_S_NO_ENDPOINT_FOUND"></span><span id="rpc_s_no_endpoint_found"></span>**RPC \_ S \_ kein \_ Endpunkt \_ gefunden.**
</dt> <dd> <dl> <dt>

1708 (0x6ac)
</dt> <dt>



Es wurde kein Endpunkt gefunden.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INVALID_TIMEOUT"></span><span id="rpc_s_invalid_timeout"></span>**\_Ungültiges RPC S- \_ \_ Timeout**
</dt> <dd> <dl> <dt>

1709 (0x6ad)
</dt> <dt>



Der Timeout Wert ist ungültig.


</dt> </dl> </dd> <dt>

<span id="RPC_S_OBJECT_NOT_FOUND"></span><span id="rpc_s_object_not_found"></span>**RPC \_ S- \_ Objekt \_ nicht \_ gefunden**
</dt> <dd> <dl> <dt>

1710 (0x6ae)
</dt> <dt>



Der Universal Unique Identifier (UUID) des Objekts wurde nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="RPC_S_ALREADY_REGISTERED"></span><span id="rpc_s_already_registered"></span>**RPC \_ S \_ bereits \_ registriert**
</dt> <dd> <dl> <dt>

1711 (0x6af)
</dt> <dt>



Der Universal Unique Identifier (UUID) für das Objekt wurde bereits registriert.


</dt> </dl> </dd> <dt>

<span id="RPC_S_TYPE_ALREADY_REGISTERED"></span><span id="rpc_s_type_already_registered"></span>**der RPC- \_ \_ Typ ist \_ bereits \_ registriert.**
</dt> <dd> <dl> <dt>

1712 (0x6b0)
</dt> <dt>



Der typuniversal Unique Identifier (UUID) wurde bereits registriert.


</dt> </dl> </dd> <dt>

<span id="RPC_S_ALREADY_LISTENING"></span><span id="rpc_s_already_listening"></span>**RPC-S, die \_ \_ bereits \_ lauschen**
</dt> <dd> <dl> <dt>

1713 (0x6b1)
</dt> <dt>



Der RPC-Server lauscht bereits.


</dt> </dl> </dd> <dt>

<span id="RPC_S_NO_PROTSEQS_REGISTERED"></span><span id="rpc_s_no_protseqs_registered"></span>**RPC \_ S ist \_ kein " \_ protabqs" \_ registriert**
</dt> <dd> <dl> <dt>

1714 (0x6b2)
</dt> <dt>



Es wurden keine Protokoll Sequenzen registriert.


</dt> </dl> </dd> <dt>

<span id="RPC_S_NOT_LISTENING"></span><span id="rpc_s_not_listening"></span>**RPC \_ S \_ nicht \_ lauscht**
</dt> <dd> <dl> <dt>

1715 (0x6b3)
</dt> <dt>



Der RPC-Server lauscht nicht.


</dt> </dl> </dd> <dt>

<span id="RPC_S_UNKNOWN_MGR_TYPE"></span><span id="rpc_s_unknown_mgr_type"></span>**\_ \_ unbekannter Mgr- \_ \_ Typ "RPC S"**
</dt> <dd> <dl> <dt>

1716 (0x6b4)
</dt> <dt>



Der Manager-Typ ist unbekannt.


</dt> </dl> </dd> <dt>

<span id="RPC_S_UNKNOWN_IF"></span><span id="rpc_s_unknown_if"></span>**RPC \_ S \_ unbekannt, \_ Wenn**
</dt> <dd> <dl> <dt>

1717 (0x6b5)
</dt> <dt>



Die Schnittstelle ist unbekannt.


</dt> </dl> </dd> <dt>

<span id="RPC_S_NO_BINDINGS"></span><span id="rpc_s_no_bindings"></span>**RPC \_ S \_ keine \_ Bindungen**
</dt> <dd> <dl> <dt>

1718 (0x6b6)
</dt> <dt>



Es sind keine Bindungen vorhanden.


</dt> </dl> </dd> <dt>

<span id="RPC_S_NO_PROTSEQS"></span><span id="rpc_s_no_protseqs"></span>**RPC \_ S ist \_ nicht \_ Prot/QS**
</dt> <dd> <dl> <dt>

1719 (0x6b7)
</dt> <dt>



Es sind keine Protokoll Sequenzen vorhanden.


</dt> </dl> </dd> <dt>

<span id="RPC_S_CANT_CREATE_ENDPOINT"></span><span id="rpc_s_cant_create_endpoint"></span>**RPC \_ S \_ - \_ \_ Endpunkt erstellen**
</dt> <dd> <dl> <dt>

1720 (0x6b8)
</dt> <dt>



Der Endpunkt kann nicht erstellt werden.


</dt> </dl> </dd> <dt>

<span id="RPC_S_OUT_OF_RESOURCES"></span><span id="rpc_s_out_of_resources"></span>**ausgehenden RPC- \_ \_ \_ \_ Ressourcen**
</dt> <dd> <dl> <dt>

1721 (0x6b9)
</dt> <dt>



Zum Ausführen dieses Vorgangs sind nicht genügend Ressourcen verfügbar.


</dt> </dl> </dd> <dt>

<span id="RPC_S_SERVER_UNAVAILABLE"></span><span id="rpc_s_server_unavailable"></span>**RPC \_ S- \_ Server nicht \_ verfügbar**
</dt> <dd> <dl> <dt>

1722 (0x6ba)
</dt> <dt>



Der RPC-Server ist nicht verfügbar.


</dt> </dl> </dd> <dt>

<span id="RPC_S_SERVER_TOO_BUSY"></span><span id="rpc_s_server_too_busy"></span>**RPC- \_ S- \_ Server ist \_ \_ ausgelastet.**
</dt> <dd> <dl> <dt>

1723 (0x6BB)
</dt> <dt>



Der RPC-Server ist zu stark ausgelastet, um diesen Vorgang abzuschließen.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INVALID_NETWORK_OPTIONS"></span><span id="rpc_s_invalid_network_options"></span>**\_ \_ ungültige \_ Netzwerk \_ Optionen für RPC S**
</dt> <dd> <dl> <dt>

1724 (0x6bc)
</dt> <dt>



Die Netzwerkoptionen sind ungültig.


</dt> </dl> </dd> <dt>

<span id="RPC_S_NO_CALL_ACTIVE"></span><span id="rpc_s_no_call_active"></span>**RPC \_ S \_ kein \_ Aufruf \_ aktiv**
</dt> <dd> <dl> <dt>

1725 (0x6bd)
</dt> <dt>



Für diesen Thread sind keine Remote Prozedur Aufrufe aktiv.


</dt> </dl> </dd> <dt>

<span id="RPC_S_CALL_FAILED"></span><span id="rpc_s_call_failed"></span>**Fehler beim RPC \_ S- \_ Aufruf. \_**
</dt> <dd> <dl> <dt>

1726 (0x6be)
</dt> <dt>



Fehler beim Remote Prozedur Rückruf.


</dt> </dl> </dd> <dt>

<span id="RPC_S_CALL_FAILED_DNE"></span><span id="rpc_s_call_failed_dne"></span>**dne-Fehler bei RPC \_ S- \_ Aufruf. \_ \_**
</dt> <dd> <dl> <dt>

1727 (0x6bf)
</dt> <dt>



Der Remote Prozedur Rückruf ist fehlgeschlagen und wurde nicht ausgeführt.


</dt> </dl> </dd> <dt>

<span id="RPC_S_PROTOCOL_ERROR"></span><span id="rpc_s_protocol_error"></span>**RPC \_ - \_ Protokoll \_ Fehler**
</dt> <dd> <dl> <dt>

1728 (0x6c0)
</dt> <dt>



RPC-Protokollfehler (Remote Procedure Aufruf).


</dt> </dl> </dd> <dt>

<span id="RPC_S_PROXY_ACCESS_DENIED"></span><span id="rpc_s_proxy_access_denied"></span>**RPC- \_ e- \_ Proxy \_ Zugriff \_ verweigert**
</dt> <dd> <dl> <dt>

1729 (0x6c1)
</dt> <dt>



Der Zugriff auf den HTTP-Proxy wird verweigert.


</dt> </dl> </dd> <dt>

<span id="RPC_S_UNSUPPORTED_TRANS_SYN"></span><span id="rpc_s_unsupported_trans_syn"></span>**transaktionale \_ \_ nicht unterstützte \_ transaktionssyn \_**
</dt> <dd> <dl> <dt>

1730 (0x6c2)
</dt> <dt>



Die Übertragungs Syntax wird vom RPC-Server nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="RPC_S_UNSUPPORTED_TYPE"></span><span id="rpc_s_unsupported_type"></span>**\_ \_ nicht unterstützter RPC S- \_ Typ**
</dt> <dd> <dl> <dt>

1732 (0x6c4)
</dt> <dt>



Der Universal Unique Identifier (UUID)-Typ wird nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INVALID_TAG"></span><span id="rpc_s_invalid_tag"></span>**\_Ungültiges RPC S- \_ \_ Tag**
</dt> <dd> <dl> <dt>

1733 (0x6c5)
</dt> <dt>



Das Tag ist ungültig.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INVALID_BOUND"></span><span id="rpc_s_invalid_bound"></span>**\_ungültige RPC S- \_ \_ Bindung**
</dt> <dd> <dl> <dt>

1734 (0x6c6)
</dt> <dt>



Die Array Begrenzungen sind ungültig.


</dt> </dl> </dd> <dt>

<span id="RPC_S_NO_ENTRY_NAME"></span><span id="rpc_s_no_entry_name"></span>**RPC \_ S \_ No \_ Entry \_ Name**
</dt> <dd> <dl> <dt>

1735 (0x6c7)
</dt> <dt>



Die Bindung enthält keinen Eintrags Namen.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INVALID_NAME_SYNTAX"></span><span id="rpc_s_invalid_name_syntax"></span>**\_Syntax für \_ ungültigen RPC S- \_ Namen \_**
</dt> <dd> <dl> <dt>

1736 (0x6c8)
</dt> <dt>



Die namens Syntax ist ungültig.


</dt> </dl> </dd> <dt>

<span id="RPC_S_UNSUPPORTED_NAME_SYNTAX"></span><span id="rpc_s_unsupported_name_syntax"></span>**\_ \_ nicht unterstützte \_ Name- \_ Syntax für RPC S**
</dt> <dd> <dl> <dt>

1737 (0x6c9)
</dt> <dt>



Die namens Syntax wird nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="RPC_S_UUID_NO_ADDRESS"></span><span id="rpc_s_uuid_no_address"></span>**RPC \_ S \_ UUID \_ keine \_ Adresse**
</dt> <dd> <dl> <dt>

1739 (0x6cb)
</dt> <dt>



Es ist keine Netzwerkadresse zum Erstellen eines Universal Unique Identifier (UUID) verfügbar.


</dt> </dl> </dd> <dt>

<span id="RPC_S_DUPLICATE_ENDPOINT"></span><span id="rpc_s_duplicate_endpoint"></span>**\_doppelter RPC \_ - \_ Endpunkt**
</dt> <dd> <dl> <dt>

1740 (0x6cc)
</dt> <dt>



Der Endpunkt ist ein Duplikat.


</dt> </dl> </dd> <dt>

<span id="RPC_S_UNKNOWN_AUTHN_TYPE"></span><span id="rpc_s_unknown_authn_type"></span>**\_ \_ unbekannter \_ authentifiztyp "RPC S" \_**
</dt> <dd> <dl> <dt>

1741 (0x6cd)
</dt> <dt>



Der Authentifizierungstyp ist unbekannt.


</dt> </dl> </dd> <dt>

<span id="RPC_S_MAX_CALLS_TOO_SMALL"></span><span id="rpc_s_max_calls_too_small"></span>**maximale Anzahl von RPC- \_ \_ \_ aufrufen \_ zu \_ klein**
</dt> <dd> <dl> <dt>

1742 (0x6ce)
</dt> <dt>



Die maximale Anzahl von Aufrufen ist zu klein.


</dt> </dl> </dd> <dt>

<span id="RPC_S_STRING_TOO_LONG"></span><span id="rpc_s_string_too_long"></span>**RPC- \_ S- \_ Zeichenfolge \_ zu \_ lang**
</dt> <dd> <dl> <dt>

1743 (0x6cf)
</dt> <dt>



Die Zeichenfolge ist zu lang.


</dt> </dl> </dd> <dt>

<span id="RPC_S_PROTSEQ_NOT_FOUND"></span><span id="rpc_s_protseq_not_found"></span>**"RPC \_ S \_ Prot*" wurde \_ nicht \_ gefunden.**
</dt> <dd> <dl> <dt>

1744 (0x6d0)
</dt> <dt>



Die RPC-Protokoll Sequenz wurde nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="RPC_S_PROCNUM_OUT_OF_RANGE"></span><span id="rpc_s_procnum_out_of_range"></span>**RPC \_ S \_ procnum liegt \_ außerhalb \_ des zulässigen \_ Bereichs.**
</dt> <dd> <dl> <dt>

1745 (0x6d1)
</dt> <dt>



Die Prozedur Nummer liegt außerhalb des zulässigen Bereichs.


</dt> </dl> </dd> <dt>

<span id="RPC_S_BINDING_HAS_NO_AUTH"></span><span id="rpc_s_binding_has_no_auth"></span>**die RPC \_ S- \_ Bindung \_ hat keine Authentifizierung \_ \_ .**
</dt> <dd> <dl> <dt>

1746 (0x6d2)
</dt> <dt>



Die Bindung enthält keine Authentifizierungsinformationen.


</dt> </dl> </dd> <dt>

<span id="RPC_S_UNKNOWN_AUTHN_SERVICE"></span><span id="rpc_s_unknown_authn_service"></span>**\_unbekannter RPC S- \_ \_ authn- \_ Dienst**
</dt> <dd> <dl> <dt>

1747 (0x6d3)
</dt> <dt>



Der Authentifizierungsdienst ist unbekannt.


</dt> </dl> </dd> <dt>

<span id="RPC_S_UNKNOWN_AUTHN_LEVEL"></span><span id="rpc_s_unknown_authn_level"></span>**nicht auf RPC- \_ \_ \_ Ebene unbekannte authn- \_ Ebene**
</dt> <dd> <dl> <dt>

1748 (0x6d4)
</dt> <dt>



Die Authentifizierungs Ebene ist unbekannt.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INVALID_AUTH_IDENTITY"></span><span id="rpc_s_invalid_auth_identity"></span>**\_ \_ ungültige Authentifizierungs \_ \_ Identität für RPC-S**
</dt> <dd> <dl> <dt>

1749 (0x6d5)
</dt> <dt>



Der Sicherheitskontext ist ungültig.


</dt> </dl> </dd> <dt>

<span id="RPC_S_UNKNOWN_AUTHZ_SERVICE"></span><span id="rpc_s_unknown_authz_service"></span>**\_unbekannter RPC S- \_ \_ Authz- \_ Dienst**
</dt> <dd> <dl> <dt>

1750 (0x6d6)
</dt> <dt>



Der Autorisierungs Dienst ist unbekannt.


</dt> </dl> </dd> <dt>

<span id="EPT_S_INVALID_ENTRY"></span><span id="ept_s_invalid_entry"></span>**\_ \_ Ungültiger Eintrag für EPT S \_**
</dt> <dd> <dl> <dt>

1751 (0x6d7)
</dt> <dt>



Der Eintrag ist ungültig.


</dt> </dl> </dd> <dt>

<span id="EPT_S_CANT_PERFORM_OP"></span><span id="ept_s_cant_perform_op"></span>**EPT \_ S \_ nicht \_ Ausführen \_**
</dt> <dd> <dl> <dt>

1752 (0x6d8)
</dt> <dt>



Der Server Endpunkt kann den Vorgang nicht durchführen.


</dt> </dl> </dd> <dt>

<span id="EPT_S_NOT_REGISTERED"></span><span id="ept_s_not_registered"></span>**EPT \_ S \_ nicht \_ registriert**
</dt> <dd> <dl> <dt>

1753 (0x6d9)
</dt> <dt>



Es sind keine Endpunkte mehr von der Endpunktzuordnung verfügbar.


</dt> </dl> </dd> <dt>

<span id="RPC_S_NOTHING_TO_EXPORT"></span><span id="rpc_s_nothing_to_export"></span>**RPC \_ S \_ Nothing \_ zum \_ exportieren**
</dt> <dd> <dl> <dt>

1754 (0x6da)
</dt> <dt>



Es wurden keine Schnittstellen exportiert.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INCOMPLETE_NAME"></span><span id="rpc_s_incomplete_name"></span>**\_ \_ unvollständiger RPC- \_ Name**
</dt> <dd> <dl> <dt>

1755 (0x6db)
</dt> <dt>



Der Eintrags Name ist unvollständig.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INVALID_VERS_OPTION"></span><span id="rpc_s_invalid_vers_option"></span>**\_Option " \_ ungültige RPC S" \_ \_**
</dt> <dd> <dl> <dt>

1756 (0x6dc)
</dt> <dt>



Die Versions Option ist ungültig.


</dt> </dl> </dd> <dt>

<span id="RPC_S_NO_MORE_MEMBERS"></span><span id="rpc_s_no_more_members"></span>**RPC \_ S \_ nicht \_ mehr \_ Mitglieder**
</dt> <dd> <dl> <dt>

1757 (0x6dd)
</dt> <dt>



Es sind keine weiteren Mitglieder vorhanden.


</dt> </dl> </dd> <dt>

<span id="RPC_S_NOT_ALL_OBJS_UNEXPORTED"></span><span id="rpc_s_not_all_objs_unexported"></span>**RPC \_ S \_ nicht \_ alle " \_ OBJS" nicht \_ exportiert**
</dt> <dd> <dl> <dt>

1758 (0x6de)
</dt> <dt>



Der Export ist nicht durchgängig.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INTERFACE_NOT_FOUND"></span><span id="rpc_s_interface_not_found"></span>**RPC \_ S- \_ Schnittstelle \_ nicht \_ gefunden**
</dt> <dd> <dl> <dt>

1759 (0x6df)
</dt> <dt>



Die Schnittstelle wurde nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="RPC_S_ENTRY_ALREADY_EXISTS"></span><span id="rpc_s_entry_already_exists"></span>**RPC \_ S- \_ Eintrag ist \_ bereits \_ vorhanden.**
</dt> <dd> <dl> <dt>

1760 (0x6e0)
</dt> <dt>



Der Eintrag ist bereits vorhanden.


</dt> </dl> </dd> <dt>

<span id="RPC_S_ENTRY_NOT_FOUND"></span><span id="rpc_s_entry_not_found"></span>**RPC \_ S- \_ Eintrag \_ nicht \_ gefunden**
</dt> <dd> <dl> <dt>

1761 (0x6e1)
</dt> <dt>



Der Eintrag wurde nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="RPC_S_NAME_SERVICE_UNAVAILABLE"></span><span id="rpc_s_name_service_unavailable"></span>**RPC- \_ S- \_ Namensdienst nicht \_ \_ verfügbar**
</dt> <dd> <dl> <dt>

1762 (0x6e2)
</dt> <dt>



Der Namensdienst ist nicht verfügbar.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INVALID_NAF_ID"></span><span id="rpc_s_invalid_naf_id"></span>**\_ \_ ungültige \_ NAF- \_ ID für RPC-S**
</dt> <dd> <dl> <dt>

1763 (0x6e3)
</dt> <dt>



Die Netzwerk Adressfamilie ist ungültig.


</dt> </dl> </dd> <dt>

<span id="RPC_S_CANNOT_SUPPORT"></span><span id="rpc_s_cannot_support"></span>**RPC \_ S \_ \_ unterstützt nicht**
</dt> <dd> <dl> <dt>

1764 (0x6e4)
</dt> <dt>



Der angeforderte Vorgang wird nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="RPC_S_NO_CONTEXT_AVAILABLE"></span><span id="rpc_s_no_context_available"></span>**RPC \_ S ist \_ kein \_ Kontext \_ verfügbar.**
</dt> <dd> <dl> <dt>

1765 (0x6e5)
</dt> <dt>



Es ist kein Sicherheitskontext verfügbar, um den Identitätswechsel zuzulassen.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INTERNAL_ERROR"></span><span id="rpc_s_internal_error"></span>**\_interner RPC \_ - \_ Fehler**
</dt> <dd> <dl> <dt>

1766 (0x6e6)
</dt> <dt>



Interner Fehler bei einem Remote Prozedur Aufruf (RPC).


</dt> </dl> </dd> <dt>

<span id="RPC_S_ZERO_DIVIDE"></span><span id="rpc_s_zero_divide"></span>**RPC \_ S \_ NULL- \_ Teilung**
</dt> <dd> <dl> <dt>

1767 (0x6e7)
</dt> <dt>



Der RPC-Server hat eine ganzzahlige Division durch Null versucht.


</dt> </dl> </dd> <dt>

<span id="RPC_S_ADDRESS_ERROR"></span><span id="rpc_s_address_error"></span>**RPC- \_ S- \_ Adress \_ Fehler**
</dt> <dd> <dl> <dt>

1768 (0x6e8)
</dt> <dt>



Beim RPC-Server ist ein Adressierungs Fehler aufgetreten.


</dt> </dl> </dd> <dt>

<span id="RPC_S_FP_DIV_ZERO"></span><span id="rpc_s_fp_div_zero"></span>**RPC-S (FP), \_ \_ \_ \_ 0**
</dt> <dd> <dl> <dt>

1769 (0x6e9)
</dt> <dt>



Ein Gleit Komma Vorgang auf dem RPC-Server verursachte eine Division durch 0 (null).


</dt> </dl> </dd> <dt>

<span id="RPC_S_FP_UNDERFLOW"></span><span id="rpc_s_fp_underflow"></span>**\_LFP \_ - \_ Unterlauf in RPC**
</dt> <dd> <dl> <dt>

1770 (0x6ea)
</dt> <dt>



Auf dem RPC-Server ist ein Gleit Komma Unterlauf aufgetreten.


</dt> </dl> </dd> <dt>

<span id="RPC_S_FP_OVERFLOW"></span><span id="rpc_s_fp_overflow"></span>**RPC- \_ S- \_ FP- \_ Überlauf**
</dt> <dd> <dl> <dt>

1771 (0x6eb)
</dt> <dt>



Auf dem RPC-Server ist ein Gleit Komma Überlauf aufgetreten.


</dt> </dl> </dd> <dt>

<span id="RPC_X_NO_MORE_ENTRIES"></span><span id="rpc_x_no_more_entries"></span>**RPC \_ X \_ keine \_ \_ Einträge mehr**
</dt> <dd> <dl> <dt>

1772 (0x6ec)
</dt> <dt>



Die Liste der RPC-Server, die für die Bindung von automatischen Handles verfügbar sind, ist erschöpft.


</dt> </dl> </dd> <dt>

<span id="RPC_X_SS_CHAR_TRANS_OPEN_FAIL"></span><span id="rpc_x_ss_char_trans_open_fail"></span>**RPC \_ X \_ SS \_ Char \_ Trans \_ Open \_ Fail**
</dt> <dd> <dl> <dt>

1773 (0x6ed)
</dt> <dt>



Die Zeichen Übersetzungs-Tabellen Datei kann nicht geöffnet werden.


</dt> </dl> </dd> <dt>

<span id="RPC_X_SS_CHAR_TRANS_SHORT_FILE"></span><span id="rpc_x_ss_char_trans_short_file"></span>**RPC \_ X \_ SS \_ Char \_ Trans \_ - \_ kurzdatei**
</dt> <dd> <dl> <dt>

1774 (0x6ee)
</dt> <dt>



Die Datei, die die Zeichen Übersetzungstabelle enthält, weist weniger als 512 Bytes auf.


</dt> </dl> </dd> <dt>

<span id="RPC_X_SS_IN_NULL_CONTEXT"></span><span id="rpc_x_ss_in_null_context"></span>**RPC \_ X \_ SS \_ in \_ NULL- \_ Kontext**
</dt> <dd> <dl> <dt>

1775 (0x6ef)
</dt> <dt>



Während eines Remote Prozedur Aufrufes wurde ein NULL-Kontext Handle vom Client an den Host übermittelt.


</dt> </dl> </dd> <dt>

<span id="RPC_X_SS_CONTEXT_DAMAGED"></span><span id="rpc_x_ss_context_damaged"></span>**RPC \_ X \_ SS- \_ Kontext \_ beschädigt**
</dt> <dd> <dl> <dt>

1777 (0x6F 1)
</dt> <dt>



Das Kontext Handle wurde während eines Remote Prozedur Aufrufes geändert.


</dt> </dl> </dd> <dt>

<span id="RPC_X_SS_HANDLES_MISMATCH"></span><span id="rpc_x_ss_handles_mismatch"></span>**RPC \_ X \_ SS- \_ Handles \_ stimmen nicht überein.**
</dt> <dd> <dl> <dt>

1778 (0x6F 2)
</dt> <dt>



Die an einen Remote Prozedur Befehl übergebenen Bindungs Handles stimmen nicht ab.


</dt> </dl> </dd> <dt>

<span id="RPC_X_SS_CANNOT_GET_CALL_HANDLE"></span><span id="rpc_x_ss_cannot_get_call_handle"></span>**RPC \_ X \_ SS \_ kann \_ kein \_ Aufruf \_ handle abrufen**
</dt> <dd> <dl> <dt>

1779 (0x6F 3)
</dt> <dt>



Der Stub kann das Remote Prozedur-Rückruf Handle nicht abrufen.


</dt> </dl> </dd> <dt>

<span id="RPC_X_NULL_REF_POINTER"></span><span id="rpc_x_null_ref_pointer"></span>**RPC \_ X \_ NULL \_ ref- \_ Zeiger**
</dt> <dd> <dl> <dt>

1780 (0x6F 4)
</dt> <dt>



Ein NULL-Verweis Zeiger wurde an den Stub übermittelt.


</dt> </dl> </dd> <dt>

<span id="RPC_X_ENUM_VALUE_OUT_OF_RANGE"></span><span id="rpc_x_enum_value_out_of_range"></span>**RPC- \_ X- \_ \_ \_ Enumerationswert außerhalb \_ des zulässigen \_ Bereichs**
</dt> <dd> <dl> <dt>

1781 (0x6F 5)
</dt> <dt>



Der Enumerationswert liegt außerhalb des Bereichs.


</dt> </dl> </dd> <dt>

<span id="RPC_X_BYTE_COUNT_TOO_SMALL"></span><span id="rpc_x_byte_count_too_small"></span>**RPC- \_ X- \_ Byte- \_ Anzahl \_ zu \_ klein**
</dt> <dd> <dl> <dt>

1782 (0x6F 6)
</dt> <dt>



Die Byte Anzahl ist zu klein.


</dt> </dl> </dd> <dt>

<span id="RPC_X_BAD_STUB_DATA"></span><span id="rpc_x_bad_stub_data"></span>**RPC-X-fehlerhafte \_ \_ \_ Stub- \_ Daten**
</dt> <dd> <dl> <dt>

1783 (0x6F 7)
</dt> <dt>



Der Stub hat ungültige Daten empfangen.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_USER_BUFFER"></span><span id="error_invalid_user_buffer"></span>**Fehler bei \_ ungültigem \_ Benutzer \_ Puffer.**
</dt> <dd> <dl> <dt>

1784 (0x6F 8)
</dt> <dt>



Der angegebene Benutzer Puffer ist für den angeforderten Vorgang nicht gültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNRECOGNIZED_MEDIA"></span><span id="error_unrecognized_media"></span>**Unbekannter Fehler. \_ \_**
</dt> <dd> <dl> <dt>

1785 (0x6F 9)
</dt> <dt>



Das Datenträger Medium wird nicht erkannt. Sie ist möglicherweise nicht formatiert.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_TRUST_LSA_SECRET"></span><span id="error_no_trust_lsa_secret"></span>**Fehler " \_ kein \_ vertrauenswürdiges \_ LSA- \_ Geheimnis"**
</dt> <dd> <dl> <dt>

1786 (0x6fa)
</dt> <dt>



Die Arbeitsstation hat keinen geheimen Vertrauens Schlüssel.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_TRUST_SAM_ACCOUNT"></span><span id="error_no_trust_sam_account"></span>**Fehler " \_ kein \_ vertrauenswürdiges Sam- \_ \_ Konto**
</dt> <dd> <dl> <dt>

1787 (0x6fb)
</dt> <dt>



Die Sicherheitsdatenbank auf dem Server hat kein Computer Konto für diese Arbeitsstations-Vertrauensstellung.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRUSTED_DOMAIN_FAILURE"></span><span id="error_trusted_domain_failure"></span>**Fehler \_ vertrauenswürdiger \_ Domäne \_**
</dt> <dd> <dl> <dt>

1788 (0x6fc)
</dt> <dt>



Die Vertrauensstellung zwischen der primären Domäne und der vertrauenswürdigen Domäne ist fehlgeschlagen.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRUSTED_RELATIONSHIP_FAILURE"></span><span id="error_trusted_relationship_failure"></span>**Fehler bei \_ vertrauenswürdiger \_ Beziehung \_**
</dt> <dd> <dl> <dt>

1789 (0x6fd)
</dt> <dt>



Bei der Vertrauensstellung zwischen der Arbeitsstation und der primären Domäne ist ein Fehler aufgetreten.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRUST_FAILURE"></span><span id="error_trust_failure"></span>**Fehler bei \_ Vertrauensstellung \_**
</dt> <dd> <dl> <dt>

1790 (0x6fe)
</dt> <dt>



Die Netzwerk Anmeldung ist fehlgeschlagen.


</dt> </dl> </dd> <dt>

<span id="RPC_S_CALL_IN_PROGRESS"></span><span id="rpc_s_call_in_progress"></span>**RPC \_ S- \_ Aufruf wird \_ ausgeführt. \_**
</dt> <dd> <dl> <dt>

1791 (0x6ff)
</dt> <dt>



Für diesen Thread wird bereits ein Remote Prozedur Aufrufvorgang ausgeführt.


</dt> </dl> </dd> <dt>

<span id="ERROR_NETLOGON_NOT_STARTED"></span><span id="error_netlogon_not_started"></span>**Fehler \_ Netlogon wurde \_ nicht \_ gestartet.**
</dt> <dd> <dl> <dt>

1792 (0x700)
</dt> <dt>



Es wurde versucht, sich anzumelden, aber der Netzwerk Anmeldedienst wurde nicht gestartet.


</dt> </dl> </dd> <dt>

<span id="ERROR_ACCOUNT_EXPIRED"></span><span id="error_account_expired"></span>**Fehler \_ Konto ist \_ abgelaufen.**
</dt> <dd> <dl> <dt>

1793 (0x701)
</dt> <dt>



Das Konto des Benutzers ist abgelaufen.


</dt> </dl> </dd> <dt>

<span id="ERROR_REDIRECTOR_HAS_OPEN_HANDLES"></span><span id="error_redirector_has_open_handles"></span>**Fehler \_ Redirector \_ hat \_ geöffnete \_ Handles**
</dt> <dd> <dl> <dt>

1794 (0x702)
</dt> <dt>



Der Redirector wird verwendet und kann nicht entladen werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINTER_DRIVER_ALREADY_INSTALLED"></span><span id="error_printer_driver_already_installed"></span>**der Fehler \_ Drucker \_ Treiber ist \_ bereits \_ installiert.**
</dt> <dd> <dl> <dt>

1795 (0x703)
</dt> <dt>



Der angegebene Druckertreiber ist bereits installiert.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNKNOWN_PORT"></span><span id="error_unknown_port"></span>**\_unbekannter \_ Port für Fehler**
</dt> <dd> <dl> <dt>

1796 (0x704)
</dt> <dt>



Der angegebene Port ist unbekannt.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNKNOWN_PRINTER_DRIVER"></span><span id="error_unknown_printer_driver"></span>**Fehler \_ unbekannter \_ Drucker \_ Treiber**
</dt> <dd> <dl> <dt>

1797 (0x705)
</dt> <dt>



Der Druckertreiber ist unbekannt.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNKNOWN_PRINTPROCESSOR"></span><span id="error_unknown_printprocessor"></span>**Unbekannter Fehler in \_ \_ PrintProcessor.**
</dt> <dd> <dl> <dt>

1798 (0x706)
</dt> <dt>



Der Druck Prozessor ist unbekannt.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SEPARATOR_FILE"></span><span id="error_invalid_separator_file"></span>**Fehler bei \_ ungültiger \_ Trenn \_ Datei.**
</dt> <dd> <dl> <dt>

1799 (0x707)
</dt> <dt>



Die angegebene Trenn Datei ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PRIORITY"></span><span id="error_invalid_priority"></span>**Fehler \_ ungültige \_ Priorität.**
</dt> <dd> <dl> <dt>

1800 (0x708)
</dt> <dt>



Die angegebene Priorität ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PRINTER_NAME"></span><span id="error_invalid_printer_name"></span>**Fehler \_ ungültiger \_ Drucker \_ Name**
</dt> <dd> <dl> <dt>

1801 (0x709)
</dt> <dt>



Der Druckername ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINTER_ALREADY_EXISTS"></span><span id="error_printer_already_exists"></span>**der Fehler \_ Drucker ist \_ bereits \_ vorhanden.**
</dt> <dd> <dl> <dt>

1802 (0x70a)
</dt> <dt>



Der Drucker ist bereits vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PRINTER_COMMAND"></span><span id="error_invalid_printer_command"></span>**Fehler bei \_ ungültigem \_ Drucker \_ Befehl.**
</dt> <dd> <dl> <dt>

1803 (0x70b)
</dt> <dt>



Der Drucker Befehl ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_DATATYPE"></span><span id="error_invalid_datatype"></span>**\_ungültiger \_ Datentyp.**
</dt> <dd> <dl> <dt>

1804 (0x70c)
</dt> <dt>



Der angegebene Datentyp ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_ENVIRONMENT"></span><span id="error_invalid_environment"></span>**\_ungültige \_ Umgebung**
</dt> <dd> <dl> <dt>

1805 (0x70d)
</dt> <dt>



Die angegebene Umgebung ist ungültig.


</dt> </dl> </dd> <dt>

<span id="RPC_S_NO_MORE_BINDINGS"></span><span id="rpc_s_no_more_bindings"></span>**RPC \_ S \_ keine \_ \_ Bindungen**
</dt> <dd> <dl> <dt>

1806 (0x70e)
</dt> <dt>



Es sind keine weiteren Bindungen vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOLOGON_INTERDOMAIN_TRUST_ACCOUNT"></span><span id="error_nologon_interdomain_trust_account"></span>**Fehler \_ nologon- \_ Domänen \_ Vertrauensstellungs \_ Konto**
</dt> <dd> <dl> <dt>

1807 (0x70f)
</dt> <dt>



Das verwendete Konto ist ein Domänen Vertrauensstellungs Konto. Verwenden Sie Ihr globales Benutzerkonto oder lokales Benutzerkonto, um auf diesen Server zuzugreifen.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOLOGON_WORKSTATION_TRUST_ACCOUNT"></span><span id="error_nologon_workstation_trust_account"></span>**Fehler \_ nologon \_ - \_ Vertrauensstellungs \_ Konto**
</dt> <dd> <dl> <dt>

1808 (0x710)
</dt> <dt>



Das verwendete Konto ist ein Computer Konto. Verwenden Sie Ihr globales Benutzerkonto oder lokales Benutzerkonto, um auf diesen Server zuzugreifen.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOLOGON_SERVER_TRUST_ACCOUNT"></span><span id="error_nologon_server_trust_account"></span>**Fehler \_ nologon \_ Server \_ Vertrauensstellungs \_ Konto**
</dt> <dd> <dl> <dt>

1809 (0x711)
</dt> <dt>



Das verwendete Konto ist ein Server Vertrauensstellungs Konto. Verwenden Sie Ihr globales Benutzerkonto oder lokales Benutzerkonto, um auf diesen Server zuzugreifen.


</dt> </dl> </dd> <dt>

<span id="ERROR_DOMAIN_TRUST_INCONSISTENT"></span><span id="error_domain_trust_inconsistent"></span>**Fehler \_ Domänen \_ Vertrauensstellung \_ inkonsistent**
</dt> <dd> <dl> <dt>

1810 (0x712)
</dt> <dt>



Der Name oder die Sicherheits-ID (SID) der angegebenen Domäne ist mit den Vertrauensstellungs Informationen für diese Domäne nicht konsistent.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVER_HAS_OPEN_HANDLES"></span><span id="error_server_has_open_handles"></span>**Fehler \_ Server \_ hat \_ geöffnete \_ Handles**
</dt> <dd> <dl> <dt>

1811 (0x713)
</dt> <dt>



Der Server wird verwendet und kann nicht entladen werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCE_DATA_NOT_FOUND"></span><span id="error_resource_data_not_found"></span>**Fehler \_ Ressourcen \_ Daten \_ \_ wurden nicht gefunden.**
</dt> <dd> <dl> <dt>

1812 (0x714)
</dt> <dt>



Die angegebene Bilddatei enthielt keinen Ressourcenabschnitt.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCE_TYPE_NOT_FOUND"></span><span id="error_resource_type_not_found"></span>**Fehler \_ beim \_ Ressourcentyp \_ nicht \_ gefunden.**
</dt> <dd> <dl> <dt>

1813 (0x715)
</dt> <dt>



Der angegebene Ressourcentyp wurde in der Bilddatei nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCE_NAME_NOT_FOUND"></span><span id="error_resource_name_not_found"></span>**der Fehler \_ Ressourcen \_ Name wurde \_ nicht \_ gefunden.**
</dt> <dd> <dl> <dt>

1814 (0x716)
</dt> <dt>



Der angegebene Ressourcen Name wurde in der Bilddatei nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCE_LANG_NOT_FOUND"></span><span id="error_resource_lang_not_found"></span>**Fehler \_ Ressource \_ lang \_ nicht \_ gefunden**
</dt> <dd> <dl> <dt>

1815 (0x717)
</dt> <dt>



Die angegebene Ressourcen Sprachen-ID wurde in der Bilddatei nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_ENOUGH_QUOTA"></span><span id="error_not_enough_quota"></span>**Fehler bei \_ nicht \_ ausreichendem \_ Kontingent.**
</dt> <dd> <dl> <dt>

1816 (0x718)
</dt> <dt>



Das Kontingent reicht für die Verarbeitung dieses Befehls nicht aus.


</dt> </dl> </dd> <dt>

<span id="RPC_S_NO_INTERFACES"></span><span id="rpc_s_no_interfaces"></span>**RPC \_ S \_ keine \_ Schnittstellen**
</dt> <dd> <dl> <dt>

1817 (0x719)
</dt> <dt>



Es wurden keine Schnittstellen registriert.


</dt> </dl> </dd> <dt>

<span id="RPC_S_CALL_CANCELLED"></span><span id="rpc_s_call_cancelled"></span>**RPC \_ S- \_ Aufruf \_ abgebrochen**
</dt> <dd> <dl> <dt>

1818 (0x71a)
</dt> <dt>



Der Remote Prozedur Aufrufvorgang wurde abgebrochen.


</dt> </dl> </dd> <dt>

<span id="RPC_S_BINDING_INCOMPLETE"></span><span id="rpc_s_binding_incomplete"></span>**RPC \_ S- \_ Bindung \_ unvollständig**
</dt> <dd> <dl> <dt>

1819 (0x71b)
</dt> <dt>



Das Bindungs Handle enthält nicht alle erforderlichen Informationen.


</dt> </dl> </dd> <dt>

<span id="RPC_S_COMM_FAILURE"></span><span id="rpc_s_comm_failure"></span>**RPC- \_ S- \_ comm- \_ Fehler**
</dt> <dd> <dl> <dt>

1820 (0x71c)
</dt> <dt>



Während eines Remote Prozedur Aufrufes ist ein Kommunikationsfehler aufgetreten.


</dt> </dl> </dd> <dt>

<span id="RPC_S_UNSUPPORTED_AUTHN_LEVEL"></span><span id="rpc_s_unsupported_authn_level"></span>**\_ \_ nicht unterstützte \_ authn- \_ Ebene für RPC S**
</dt> <dd> <dl> <dt>

1821 (0x71d)
</dt> <dt>



Die angeforderte Authentifizierungs Ebene wird nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="RPC_S_NO_PRINC_NAME"></span><span id="rpc_s_no_princ_name"></span>**RPC \_ S \_ kein \_ princ- \_ Name**
</dt> <dd> <dl> <dt>

1822 (0x71e)
</dt> <dt>



Es ist kein Prinzipal Name registriert.


</dt> </dl> </dd> <dt>

<span id="RPC_S_NOT_RPC_ERROR"></span><span id="rpc_s_not_rpc_error"></span>**RPC \_ - \_ \_ \_ Fehler**
</dt> <dd> <dl> <dt>

1823 (0x71f)
</dt> <dt>



Der angegebene Fehler ist kein gültiger Windows-RPC-Fehlercode.


</dt> </dl> </dd> <dt>

<span id="RPC_S_UUID_LOCAL_ONLY"></span><span id="rpc_s_uuid_local_only"></span>**RPC \_ S \_ UUID \_ lokal \_**
</dt> <dd> <dl> <dt>

1824 (0x720)
</dt> <dt>



Eine UUID, die nur auf diesem Computer gültig ist, wurde zugeordnet.


</dt> </dl> </dd> <dt>

<span id="RPC_S_SEC_PKG_ERROR"></span><span id="rpc_s_sec_pkg_error"></span>**RPC \_ S S- \_ \_ pkg- \_ Fehler**
</dt> <dd> <dl> <dt>

1825 (0x721)
</dt> <dt>



Ein Sicherheitspaket spezifischer Fehler ist aufgetreten.


</dt> </dl> </dd> <dt>

<span id="RPC_S_NOT_CANCELLED"></span><span id="rpc_s_not_cancelled"></span>**RPC- \_ S \_ nicht \_ abgebrochen**
</dt> <dd> <dl> <dt>

1826 (0x722)
</dt> <dt>



Der Thread wird nicht abgebrochen.


</dt> </dl> </dd> <dt>

<span id="RPC_X_INVALID_ES_ACTION"></span><span id="rpc_x_invalid_es_action"></span>**\_ungültige RPC X- \_ \_ \_ Aktion**
</dt> <dd> <dl> <dt>

1827 (0x723)
</dt> <dt>



Ungültiger Vorgang für das Codierungs-/decodierungshandle.


</dt> </dl> </dd> <dt>

<span id="RPC_X_WRONG_ES_VERSION"></span><span id="rpc_x_wrong_es_version"></span>**RPC \_ X \_ falsche \_ es- \_ Version**
</dt> <dd> <dl> <dt>

1828 (0x724)
</dt> <dt>



Nicht kompatible Version des serialisierungspakets.


</dt> </dl> </dd> <dt>

<span id="RPC_X_WRONG_STUB_VERSION"></span><span id="rpc_x_wrong_stub_version"></span>**\_falsche RPC X- \_ \_ Stub- \_ Version**
</dt> <dd> <dl> <dt>

1829 (0x725)
</dt> <dt>



Inkompatible Version des RPC-Stubs.


</dt> </dl> </dd> <dt>

<span id="RPC_X_INVALID_PIPE_OBJECT"></span><span id="rpc_x_invalid_pipe_object"></span>**\_Ungültiges RPC X- \_ Pipe- \_ \_ Objekt**
</dt> <dd> <dl> <dt>

1830 (0x726)
</dt> <dt>



Das RPC-Pipe-Objekt ist ungültig oder beschädigt.


</dt> </dl> </dd> <dt>

<span id="RPC_X_WRONG_PIPE_ORDER"></span><span id="rpc_x_wrong_pipe_order"></span>**RPC \_ X \_ falsche \_ Pipe- \_ Reihenfolge**
</dt> <dd> <dl> <dt>

1831 (0x727)
</dt> <dt>



Es wurde versucht, für ein RPC-Pipeobjekt einen ungültigen Vorgang auszuführen.


</dt> </dl> </dd> <dt>

<span id="RPC_X_WRONG_PIPE_VERSION"></span><span id="rpc_x_wrong_pipe_version"></span>**RPC \_ X \_ falsche \_ Pipe- \_ Version**
</dt> <dd> <dl> <dt>

1832 (0x728)
</dt> <dt>



Nicht unterstützte RPC-Pipe-Version.


</dt> </dl> </dd> <dt>

<span id="RPC_S_COOKIE_AUTH_FAILED"></span><span id="rpc_s_cookie_auth_failed"></span>**Fehler bei RPC-e-Cookie-Authentifizierung \_ \_ \_ . \_**
</dt> <dd> <dl> <dt>

1833 (0x729)
</dt> <dt>



Der HTTP-Proxy Server hat die Verbindung abgelehnt, weil die Cookie-Authentifizierung fehlgeschlagen ist


</dt> </dl> </dd> <dt>

<span id="RPC_S_GROUP_MEMBER_NOT_FOUND"></span><span id="rpc_s_group_member_not_found"></span>**das RPC \_ S- \_ Gruppenmitglied wurde \_ \_ nicht \_ gefunden.**
</dt> <dd> <dl> <dt>

1898 (0x76a)
</dt> <dt>



Das Gruppenmitglied wurde nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="EPT_S_CANT_CREATE"></span><span id="ept_s_cant_create"></span>**EPT \_ S \_ nicht \_ Erstellen**
</dt> <dd> <dl> <dt>

1899 (0x76b)
</dt> <dt>



Der Endpunkt Mapper-Datenbankeintrag konnte nicht erstellt werden.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INVALID_OBJECT"></span><span id="rpc_s_invalid_object"></span>**\_Ungültiges RPC S- \_ \_ Objekt**
</dt> <dd> <dl> <dt>

1900 (0x76c)
</dt> <dt>



Der Universal Unique Identifier (UUID) des Objekts ist die Nil-UUID.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_TIME"></span><span id="error_invalid_time"></span>**\_ungültige \_ Zeit**
</dt> <dd> <dl> <dt>

1901 (0x76d)
</dt> <dt>



Die angegebene Zeit ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_FORM_NAME"></span><span id="error_invalid_form_name"></span>**\_ungültiger \_ Formular \_ Name.**
</dt> <dd> <dl> <dt>

1902 (0x76e)
</dt> <dt>



Der angegebene Formular Name ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_FORM_SIZE"></span><span id="error_invalid_form_size"></span>**Fehler bei \_ ungültiger \_ Formular \_ Größe**
</dt> <dd> <dl> <dt>

1903 (0x76f)
</dt> <dt>



Die angegebene Formular Größe ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_ALREADY_WAITING"></span><span id="error_already_waiting"></span>**Fehler \_ beim \_ warten bereits**
</dt> <dd> <dl> <dt>

1904 (0x770)
</dt> <dt>



Auf das angegebene Drucker Handle wird bereits gewartet.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINTER_DELETED"></span><span id="error_printer_deleted"></span>**Fehler \_ Drucker \_ gelöscht**
</dt> <dd> <dl> <dt>

1905 (0x771)
</dt> <dt>



Der angegebene Drucker wurde gelöscht.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PRINTER_STATE"></span><span id="error_invalid_printer_state"></span>**Fehler \_ beim \_ Drucker \_ Zustand.**
</dt> <dd> <dl> <dt>

1906 (0x772)
</dt> <dt>



Der Drucker Zustand ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_PASSWORD_MUST_CHANGE"></span><span id="error_password_must_change"></span>**Fehler \_ Kennwort \_ muss \_ geändert werden**
</dt> <dd> <dl> <dt>

1907 (0x773)
</dt> <dt>



Das Kennwort des Benutzers muss vor der Anmeldung geändert werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DOMAIN_CONTROLLER_NOT_FOUND"></span><span id="error_domain_controller_not_found"></span>**Fehler \_ Domänen \_ Controller \_ nicht \_ gefunden**
</dt> <dd> <dl> <dt>

1908 (0x774)
</dt> <dt>



Der Domänen Controller für diese Domäne konnte nicht gefunden werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_ACCOUNT_LOCKED_OUT"></span><span id="error_account_locked_out"></span>**Fehler \_ Konto \_ gesperrt \_**
</dt> <dd> <dl> <dt>

1909 (0x775)
</dt> <dt>



Das Konto, auf das verwiesen wird, ist zurzeit gesperrt und darf nicht bei angemeldet sein.


</dt> </dl> </dd> <dt>

<span id="OR_INVALID_OXID"></span><span id="or_invalid_oxid"></span>**oder \_ ungültiges \_ oxid**
</dt> <dd> <dl> <dt>

1910 (0x776)
</dt> <dt>



Das angegebene Objekt Exportprogramm wurde nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="OR_INVALID_OID"></span><span id="or_invalid_oid"></span>**oder \_ ungültige \_ OID.**
</dt> <dd> <dl> <dt>

1911 (0x777)
</dt> <dt>



Das angegebene Objekt wurde nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="OR_INVALID_SET"></span><span id="or_invalid_set"></span>**oder \_ ungültiger \_ Satz**
</dt> <dd> <dl> <dt>

1912 (0x778)
</dt> <dt>



Der angegebene objektresolersatz wurde nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="RPC_S_SEND_INCOMPLETE"></span><span id="rpc_s_send_incomplete"></span>**RPC- \_ e- \_ Sendevorgang \_ unvollständig**
</dt> <dd> <dl> <dt>

1913 (0x779)
</dt> <dt>



Einige Daten werden weiterhin im Anforderungs Puffer gesendet.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INVALID_ASYNC_HANDLE"></span><span id="rpc_s_invalid_async_handle"></span>**Ungültiges asynchrones Handle für RPC \_ S \_ \_ \_**
</dt> <dd> <dl> <dt>

1914 (0x77a)
</dt> <dt>



Ungültiges asynchrones Remote Prozedur-Rückruf handle.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INVALID_ASYNC_CALL"></span><span id="rpc_s_invalid_async_call"></span>**\_Ungültiger asynchroner \_ \_ \_ Aufruf von RPC S**
</dt> <dd> <dl> <dt>

1915 (0x77b)
</dt> <dt>



Ungültiges asynchrones RPC-Aufruf Handle für diesen Vorgang.


</dt> </dl> </dd> <dt>

<span id="RPC_X_PIPE_CLOSED"></span><span id="rpc_x_pipe_closed"></span>**RPC- \_ X- \_ Pipe \_ geschlossen**
</dt> <dd> <dl> <dt>

1916 (0x77c)
</dt> <dt>



Das RPC-Pipe-Objekt wurde bereits geschlossen.


</dt> </dl> </dd> <dt>

<span id="RPC_X_PIPE_DISCIPLINE_ERROR"></span><span id="rpc_x_pipe_discipline_error"></span>**RPC \_ X \_ Pipe- \_ Disziplin- \_ Fehler**
</dt> <dd> <dl> <dt>

1917 (0x77d)
</dt> <dt>



Der RPC-Aufruf wurde abgeschlossen, bevor alle Pipes verarbeitet wurden.


</dt> </dl> </dd> <dt>

<span id="RPC_X_PIPE_EMPTY"></span><span id="rpc_x_pipe_empty"></span>**RPC- \_ X- \_ Pipe \_ leer**
</dt> <dd> <dl> <dt>

1918 (0x77e)
</dt> <dt>



Von der RPC-Pipe sind keine weiteren Daten verfügbar.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SITENAME"></span><span id="error_no_sitename"></span>**Fehler " \_ kein \_ Sitename"**
</dt> <dd> <dl> <dt>

1919 (0x77f)
</dt> <dt>



Für diesen Computer ist kein Website Name verfügbar.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANT_ACCESS_FILE"></span><span id="error_cant_access_file"></span>**Fehler beim Zugriff auf die \_ \_ \_ Datei.**
</dt> <dd> <dl> <dt>

1920 (0x780)
</dt> <dt>



Auf die Datei kann nicht vom System zugegriffen werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANT_RESOLVE_FILENAME"></span><span id="error_cant_resolve_filename"></span>**Fehler \_ beim \_ Auflösen des \_ Datei namens.**
</dt> <dd> <dl> <dt>

1921 (0x781)
</dt> <dt>



Der Name der Datei kann nicht vom System aufgelöst werden.


</dt> </dl> </dd> <dt>

<span id="RPC_S_ENTRY_TYPE_MISMATCH"></span><span id="rpc_s_entry_type_mismatch"></span>**nicht übereinstimmender RPC \_ S- \_ \_ Eintragstyp \_**
</dt> <dd> <dl> <dt>

1922 (0x782)
</dt> <dt>



Der Eintrag weist nicht den erwarteten Typ auf.


</dt> </dl> </dd> <dt>

<span id="RPC_S_NOT_ALL_OBJS_EXPORTED"></span><span id="rpc_s_not_all_objs_exported"></span>**RPC \_ S \_ nicht \_ alle \_ OBJS- \_ exportierten**
</dt> <dd> <dl> <dt>

1923 (0x783)
</dt> <dt>



Nicht alle Objekt-UUIDs konnten in den angegebenen Eintrag exportiert werden.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INTERFACE_NOT_EXPORTED"></span><span id="rpc_s_interface_not_exported"></span>**RPC \_ S- \_ Schnittstelle \_ nicht \_ exportiert**
</dt> <dd> <dl> <dt>

1924 (0x784)
</dt> <dt>



Die Schnittstelle konnte nicht in den angegebenen Eintrag exportiert werden.


</dt> </dl> </dd> <dt>

<span id="RPC_S_PROFILE_NOT_ADDED"></span><span id="rpc_s_profile_not_added"></span>**RPC- \_ S- \_ Profil \_ nicht \_ hinzugefügt**
</dt> <dd> <dl> <dt>

1925 (0x785)
</dt> <dt>



Der angegebene Profil Eintrag konnte nicht hinzugefügt werden.


</dt> </dl> </dd> <dt>

<span id="RPC_S_PRF_ELT_NOT_ADDED"></span><span id="rpc_s_prf_elt_not_added"></span>**RPC \_ S \_ PRF \_ ELT wurde \_ nicht \_ hinzugefügt.**
</dt> <dd> <dl> <dt>

1926 (0x786)
</dt> <dt>



Das angegebene Profil Element konnte nicht hinzugefügt werden.


</dt> </dl> </dd> <dt>

<span id="RPC_S_PRF_ELT_NOT_REMOVED"></span><span id="rpc_s_prf_elt_not_removed"></span>**RPC \_ S \_ PRF \_ ELT \_ nicht \_ entfernt**
</dt> <dd> <dl> <dt>

1927 (0x787)
</dt> <dt>



Das angegebene Profil Element konnte nicht entfernt werden.


</dt> </dl> </dd> <dt>

<span id="RPC_S_GRP_ELT_NOT_ADDED"></span><span id="rpc_s_grp_elt_not_added"></span>**RPC- \_ e- \_ GRP wird \_ \_ nicht \_ hinzugefügt.**
</dt> <dd> <dl> <dt>

1928 (0x788)
</dt> <dt>



Das Gruppenelement konnte nicht hinzugefügt werden.


</dt> </dl> </dd> <dt>

<span id="RPC_S_GRP_ELT_NOT_REMOVED"></span><span id="rpc_s_grp_elt_not_removed"></span>**RPC- \_ S \_ GRP \_ ELT \_ nicht \_ entfernt**
</dt> <dd> <dl> <dt>

1929 (0x789)
</dt> <dt>



Das Gruppenelement konnte nicht entfernt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_KM_DRIVER_BLOCKED"></span><span id="error_km_driver_blocked"></span>**Fehler- \_ km- \_ Treiber \_ blockiert**
</dt> <dd> <dl> <dt>

1930 (0x78a)
</dt> <dt>



Der Druckertreiber ist nicht kompatibel mit einer Richtlinie, die auf Ihrem Computer aktiviert ist und NT 4,0-Treiber blockiert.


</dt> </dl> </dd> <dt>

<span id="ERROR_CONTEXT_EXPIRED"></span><span id="error_context_expired"></span>**Fehler \_ Kontext ist \_ abgelaufen.**
</dt> <dd> <dl> <dt>

1931 (0x78b)
</dt> <dt>



Der Kontext ist abgelaufen und kann nicht mehr verwendet werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_PER_USER_TRUST_QUOTA_EXCEEDED"></span><span id="error_per_user_trust_quota_exceeded"></span>**Fehler \_ pro \_ Benutzer \_ Vertrauensstellungs \_ Kontingent \_ überschritten**
</dt> <dd> <dl> <dt>

1932 (0x78c)
</dt> <dt>



Das Kontingent für die Delegierte Vertrauensstellung des aktuellen Benutzers wurde überschritten.


</dt> </dl> </dd> <dt>

<span id="ERROR_ALL_USER_TRUST_QUOTA_EXCEEDED"></span><span id="error_all_user_trust_quota_exceeded"></span>**Fehler \_ alle \_ Benutzer \_ Vertrauensstellungs \_ Kontingente \_ überschritten.**
</dt> <dd> <dl> <dt>

1933 (0x78d)
</dt> <dt>



Das Kontingent für die Gesamt Erstellung Delegierter Vertrauens Stellungen wurde überschritten.


</dt> </dl> </dd> <dt>

<span id="ERROR_USER_DELETE_TRUST_QUOTA_EXCEEDED"></span><span id="error_user_delete_trust_quota_exceeded"></span>**Fehler \_ beim \_ Löschen der \_ Vertrauens \_ Quote \_ für den Benutzer.**
</dt> <dd> <dl> <dt>

1934 (0x78e)
</dt> <dt>



Das Kontingent für den Delegierten Vertrauens Löschvorgang des aktuellen Benutzers wurde überschritten.


</dt> </dl> </dd> <dt>

<span id="ERROR_AUTHENTICATION_FIREWALL_FAILED"></span><span id="error_authentication_firewall_failed"></span>**Fehler bei der \_ \_ firewallfirewall. \_**
</dt> <dd> <dl> <dt>

1935 (0x78f)
</dt> <dt>



Der Computer, bei dem Sie sich anmelden, wird durch eine Authentifizierungs Firewall geschützt. Das angegebene Konto darf sich nicht bei dem Computer authentifizieren.


</dt> </dl> </dd> <dt>

<span id="ERROR_REMOTE_PRINT_CONNECTIONS_BLOCKED"></span><span id="error_remote_print_connections_blocked"></span>**Fehler beim \_ Blockieren von Remote \_ Druck \_ Verbindungen \_ .**
</dt> <dd> <dl> <dt>

1936 (0x790)
</dt> <dt>



Remote Verbindungen mit dem Druck Spooler werden durch eine auf Ihrem Computer festgelegte Richtlinie blockiert.


</dt> </dl> </dd> <dt>

<span id="ERROR_NTLM_BLOCKED"></span><span id="error_ntlm_blocked"></span>**Fehler \_ NTLM \_ blockiert**
</dt> <dd> <dl> <dt>

1937 (0x791)
</dt> <dt>



Die Authentifizierung ist fehlgeschlagen, weil die NTLM-Authentifizierung deaktiviert wurde.


</dt> </dl> </dd> <dt>

<span id="ERROR_PASSWORD_CHANGE_REQUIRED"></span><span id="error_password_change_required"></span>**Fehler \_ Kennwort- \_ Änderung \_ erforderlich**
</dt> <dd> <dl> <dt>

1938 (0x792)
</dt> <dt>



Anmeldefehler: Die EAS-Richtlinie erfordert, dass der Benutzer sein Kennwort ändert, bevor dieser Vorgang ausgeführt werden kann.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PIXEL_FORMAT"></span><span id="error_invalid_pixel_format"></span>**Fehler \_ ungültiges \_ Pixel \_ Format.**
</dt> <dd> <dl> <dt>

2000 (0x7d0)
</dt> <dt>



Das Pixel Format ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_DRIVER"></span><span id="error_bad_driver"></span>**fehlerhafter \_ \_ Treiber Fehler**
</dt> <dd> <dl> <dt>

2001 (0x7d1)
</dt> <dt>



Der angegebene Treiber ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_WINDOW_STYLE"></span><span id="error_invalid_window_style"></span>**Fehler bei \_ ungültigem \_ Fenster \_ Stil.**
</dt> <dd> <dl> <dt>

2002 (0x7d2)
</dt> <dt>



Der Fenster Stil oder das Klassen Attribut ist für diesen Vorgang ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_METAFILE_NOT_SUPPORTED"></span><span id="error_metafile_not_supported"></span>**\_fehlermetadatendatei \_ \_ wird nicht unterstützt**
</dt> <dd> <dl> <dt>

2003 (0x7d3)
</dt> <dt>



Der angeforderte Metadatei-Vorgang wird nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSFORM_NOT_SUPPORTED"></span><span id="error_transform_not_supported"></span>**Fehler \_ Transformation \_ \_ wird nicht unterstützt.**
</dt> <dd> <dl> <dt>

2004 (0x7d4)
</dt> <dt>



Der angeforderte Transformations Vorgang wird nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLIPPING_NOT_SUPPORTED"></span><span id="error_clipping_not_supported"></span>**Fehler \_ Clipping \_ \_ wird nicht unterstützt.**
</dt> <dd> <dl> <dt>

2005 (0x7d5)
</dt> <dt>



Der angeforderte Clippingvorgang wird nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_CMM"></span><span id="error_invalid_cmm"></span>**\_ungültiger \_ CMM-Fehler.**
</dt> <dd> <dl> <dt>

2010 (0x7da)
</dt> <dt>



Das angegebene Farb Verwaltungsmodul ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PROFILE"></span><span id="error_invalid_profile"></span>**Fehler \_ ungültiges \_ Profil.**
</dt> <dd> <dl> <dt>

2011 (0x7db)
</dt> <dt>



Das angegebene Farbprofil ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_TAG_NOT_FOUND"></span><span id="error_tag_not_found"></span>**\_Fehlertag \_ nicht \_ gefunden.**
</dt> <dd> <dl> <dt>

2012 (0x7dc)
</dt> <dt>



Das angegebene Tag wurde nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_TAG_NOT_PRESENT"></span><span id="error_tag_not_present"></span>**\_Fehlertag \_ nicht \_ vorhanden**
</dt> <dd> <dl> <dt>

2013 (0x7dd)
</dt> <dt>



Ein erforderliches Tag ist nicht vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DUPLICATE_TAG"></span><span id="error_duplicate_tag"></span>**Fehler \_ doppeltes \_ Tag**
</dt> <dd> <dl> <dt>

2014 (0x7de)
</dt> <dt>



Das angegebene Tag ist bereits vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_PROFILE_NOT_ASSOCIATED_WITH_DEVICE"></span><span id="error_profile_not_associated_with_device"></span>**das Fehler \_ Profil ist \_ nicht \_ \_ mit dem \_ Gerät verknüpft.**
</dt> <dd> <dl> <dt>

2015 (0x7df)
</dt> <dt>



Das angegebene Farbprofil ist dem angegebenen Gerät nicht zugeordnet.


</dt> </dl> </dd> <dt>

<span id="ERROR_PROFILE_NOT_FOUND"></span><span id="error_profile_not_found"></span>**Fehler \_ Profil wurde \_ nicht \_ gefunden.**
</dt> <dd> <dl> <dt>

2016 (0x7e0)
</dt> <dt>



Das angegebene Farbprofil wurde nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_COLORSPACE"></span><span id="error_invalid_colorspace"></span>**\_ungültiger \_ colorspace-Fehler.**
</dt> <dd> <dl> <dt>

2017 (0x7e1)
</dt> <dt>



Der angegebene Farbraum ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_ICM_NOT_ENABLED"></span><span id="error_icm_not_enabled"></span>**ICM-Fehler ist \_ \_ nicht \_ aktiviert.**
</dt> <dd> <dl> <dt>

2018 (0x7e2)
</dt> <dt>



Die Bild Farbverwaltung ist nicht aktiviert.


</dt> </dl> </dd> <dt>

<span id="ERROR_DELETING_ICM_XFORM"></span><span id="error_deleting_icm_xform"></span>**Fehler beim \_ Löschen von \_ ICM \_ XForm.**
</dt> <dd> <dl> <dt>

2019 (0x7e3)
</dt> <dt>



Beim Löschen der Farb Transformation ist ein Fehler aufgetreten.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_TRANSFORM"></span><span id="error_invalid_transform"></span>**Fehler \_ ungültige \_ Transformation**
</dt> <dd> <dl> <dt>

2020 (0x7e4)
</dt> <dt>



Die angegebene Farb Transformation ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_COLORSPACE_MISMATCH"></span><span id="error_colorspace_mismatch"></span>**Fehler bei colorspace-Konflikt. \_ \_**
</dt> <dd> <dl> <dt>

2021 (0x7e5)
</dt> <dt>



Die angegebene Transformation entspricht nicht dem Farbraum der Bitmap.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_COLORINDEX"></span><span id="error_invalid_colorindex"></span>**Fehler \_ ungültiger \_ ColorIndex.**
</dt> <dd> <dl> <dt>

2022 (0x7e6)
</dt> <dt>



Der angegebene benannte Farb Index ist nicht im Profil vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_PROFILE_DOES_NOT_MATCH_DEVICE"></span><span id="error_profile_does_not_match_device"></span>**Fehler \_ Profil \_ entspricht \_ \_ Gerät nicht \_**
</dt> <dd> <dl> <dt>

2023 (0x7e7)
</dt> <dt>



Das angegebene Profil ist für ein Gerät mit einem anderen Typ als dem angegebenen Gerät vorgesehen.


</dt> </dl> </dd> <dt>

<span id="ERROR_CONNECTED_OTHER_PASSWORD"></span><span id="error_connected_other_password"></span>**Fehler beim \_ verbundenen \_ anderen \_ Kennwort**
</dt> <dd> <dl> <dt>

2108 (0x83c)
</dt> <dt>



Die Netzwerkverbindung wurde erfolgreich hergestellt, aber der Benutzer musste aufgefordert werden, ein anderes Kennwort als das ursprünglich angegebene Kennwort einzugeben.


</dt> </dl> </dd> <dt>

<span id="ERROR_CONNECTED_OTHER_PASSWORD_DEFAULT"></span><span id="error_connected_other_password_default"></span>**Fehler beim \_ verbundenen \_ anderen \_ Kennwort- \_ Standard**
</dt> <dd> <dl> <dt>

2109 (0x83d)
</dt> <dt>



Die Netzwerkverbindung wurde mithilfe der Standard Anmelde Informationen erfolgreich hergestellt.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_USERNAME"></span><span id="error_bad_username"></span>**Ungültiger \_ \_ Benutzername**
</dt> <dd> <dl> <dt>

2202 (0x89a)
</dt> <dt>



Der angegebene Benutzername ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_CONNECTED"></span><span id="error_not_connected"></span>**Fehler \_ nicht \_ verbunden**
</dt> <dd> <dl> <dt>

2250 (0x8ca)
</dt> <dt>



Diese Netzwerkverbindung ist nicht vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_OPEN_FILES"></span><span id="error_open_files"></span>**Fehler beim \_ Öffnen von \_ Dateien**
</dt> <dd> <dl> <dt>

2401 (0x961)
</dt> <dt>



Für diese Netzwerkverbindung sind Dateien geöffnet oder ausstehende Anforderungen.


</dt> </dl> </dd> <dt>

<span id="ERROR_ACTIVE_CONNECTIONS"></span><span id="error_active_connections"></span>**\_aktive \_ Verbindungsfehler**
</dt> <dd> <dl> <dt>

2402 (0x962)
</dt> <dt>



Aktive Verbindungen sind immer noch vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_IN_USE"></span><span id="error_device_in_use"></span>**\_fehlergerät \_ wird \_ verwendet**
</dt> <dd> <dl> <dt>

2404 (0x964)
</dt> <dt>



Das Gerät wird von einem aktiven Prozess verwendet und kann nicht getrennt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNKNOWN_PRINT_MONITOR"></span><span id="error_unknown_print_monitor"></span>**\_unbekannter Fehler \_ \_ Monitor.**
</dt> <dd> <dl> <dt>

3000 (0xBB8)
</dt> <dt>



Der angegebene Druckmonitor ist unbekannt.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINTER_DRIVER_IN_USE"></span><span id="error_printer_driver_in_use"></span>**Fehler \_ Drucker \_ Treiber \_ wird \_ verwendet**
</dt> <dd> <dl> <dt>

3001 (0xbb9)
</dt> <dt>



Der angegebene Druckertreiber wird zurzeit verwendet.


</dt> </dl> </dd> <dt>

<span id="ERROR_SPOOL_FILE_NOT_FOUND"></span><span id="error_spool_file_not_found"></span>**Fehler \_ \_ Spooldatei \_ nicht \_ gefunden.**
</dt> <dd> <dl> <dt>

3002 (0xBBA)
</dt> <dt>



Die Spooldatei wurde nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_SPL_NO_STARTDOC"></span><span id="error_spl_no_startdoc"></span>**Fehler \_ SPL \_ Nein \_ StartDoc**
</dt> <dd> <dl> <dt>

3003 (0xbbb)
</dt> <dt>



Es wurde kein StartDocPrinter-Befehl ausgegeben.


</dt> </dl> </dd> <dt>

<span id="ERROR_SPL_NO_ADDJOB"></span><span id="error_spl_no_addjob"></span>**Fehler- \_ SPL \_ Nein, \_ AddJob**
</dt> <dd> <dl> <dt>

3004 (0xbbc)
</dt> <dt>



Es wurde kein AddJob-Befehl ausgegeben.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINT_PROCESSOR_ALREADY_INSTALLED"></span><span id="error_print_processor_already_installed"></span>**der Fehler \_ Druck \_ Prozessor ist \_ bereits \_ installiert.**
</dt> <dd> <dl> <dt>

3005 (0xbbd)
</dt> <dt>



Der angegebene Druck Prozessor wurde bereits installiert.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINT_MONITOR_ALREADY_INSTALLED"></span><span id="error_print_monitor_already_installed"></span>**der Fehler \_ Druck \_ Monitor ist \_ bereits \_ installiert.**
</dt> <dd> <dl> <dt>

3006 (0xbbe)
</dt> <dt>



Der angegebene Druckmonitor wurde bereits installiert.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PRINT_MONITOR"></span><span id="error_invalid_print_monitor"></span>**Fehler \_ beim \_ Druck \_ Monitor.**
</dt> <dd> <dl> <dt>

3007 (0xbbf)
</dt> <dt>



Der angegebene Druckmonitor verfügt nicht über die erforderlichen Funktionen.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINT_MONITOR_IN_USE"></span><span id="error_print_monitor_in_use"></span>**Fehler \_ Druck \_ Monitor \_ wird \_ verwendet**
</dt> <dd> <dl> <dt>

3008 (0xbc0)
</dt> <dt>



Der angegebene Druckmonitor wird zurzeit verwendet.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINTER_HAS_JOBS_QUEUED"></span><span id="error_printer_has_jobs_queued"></span>**Fehler \_ Drucker \_ hat \_ Aufträge in \_ Warteschlange eingereiht**
</dt> <dd> <dl> <dt>

3009 (0xbc1)
</dt> <dt>



Der angeforderte Vorgang ist nicht zulässig, wenn Aufträge in die Warteschlange eingereiht wurden.


</dt> </dl> </dd> <dt>

<span id="ERROR_SUCCESS_REBOOT_REQUIRED"></span><span id="error_success_reboot_required"></span>**Fehler \_ beim \_ Neustart \_ erforderlich.**
</dt> <dd> <dl> <dt>

3010 (0xbc2)
</dt> <dt>



Der angeforderte Vorgang ist erfolgreich. Änderungen werden erst wirksam, wenn das System neu gestartet wird.


</dt> </dl> </dd> <dt>

<span id="ERROR_SUCCESS_RESTART_REQUIRED"></span><span id="error_success_restart_required"></span>**Fehler \_ beim \_ Neustart \_ erforderlich.**
</dt> <dd> <dl> <dt>

3011 (0xbc3)
</dt> <dt>



Der angeforderte Vorgang ist erfolgreich. Änderungen werden erst wirksam, wenn der Dienst neu gestartet wird.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINTER_NOT_FOUND"></span><span id="error_printer_not_found"></span>**Fehler \_ Drucker wurde \_ nicht \_ gefunden.**
</dt> <dd> <dl> <dt>

3012 (0xbc4)
</dt> <dt>



Es wurden keine Drucker gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINTER_DRIVER_WARNED"></span><span id="error_printer_driver_warned"></span>**Fehler \_ Drucker \_ Treiber \_ gewarnt**
</dt> <dd> <dl> <dt>

3013 (0xbc5)
</dt> <dt>



Der Druckertreiber ist bekanntermaßen unzuverlässig.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINTER_DRIVER_BLOCKED"></span><span id="error_printer_driver_blocked"></span>**Fehler \_ Drucker \_ Treiber \_ blockiert**
</dt> <dd> <dl> <dt>

3014 (0xbc6)
</dt> <dt>



Der Druckertreiber ist bekannt, dass er das System beeinträchtigt.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINTER_DRIVER_PACKAGE_IN_USE"></span><span id="error_printer_driver_package_in_use"></span>**Fehler \_ Drucker- \_ Treiber \_ Paket wird \_ \_ verwendet**
</dt> <dd> <dl> <dt>

3015 (0xbc7)
</dt> <dt>



Das angegebene Druckertreiber Paket wird zurzeit verwendet.


</dt> </dl> </dd> <dt>

<span id="ERROR_CORE_DRIVER_PACKAGE_NOT_FOUND"></span><span id="error_core_driver_package_not_found"></span>**Fehler beim \_ Core- \_ Treiber \_ Paket \_ nicht \_ gefunden.**
</dt> <dd> <dl> <dt>

3016 (0xbc8)
</dt> <dt>



Es wurde kein Core-Treiber Paket gefunden, das für das Druckertreiber Paket erforderlich ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_FAIL_REBOOT_REQUIRED"></span><span id="error_fail_reboot_required"></span>**Fehler \_ beim \_ Neustart \_ erforderlich.**
</dt> <dd> <dl> <dt>

3017 (0xbc9)
</dt> <dt>



Der angeforderte Vorgang ist fehlgeschlagen. Ein Systemneustart ist erforderlich, um ein Rollback der vorgenommenen Änderungen auszuführen.


</dt> </dl> </dd> <dt>

<span id="ERROR_FAIL_REBOOT_INITIATED"></span><span id="error_fail_reboot_initiated"></span>**Fehler \_ beim \_ Neustart \_ wurde initiiert.**
</dt> <dd> <dl> <dt>

3018 (0xbca)
</dt> <dt>



Der angeforderte Vorgang ist fehlgeschlagen. Ein Systemneustart wurde initiiert, um ein Rollback der vorgenommenen Änderungen auszuführen.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINTER_DRIVER_DOWNLOAD_NEEDED"></span><span id="error_printer_driver_download_needed"></span>**Fehler \_ Drucker- \_ Treiber \_ Download \_ erforderlich**
</dt> <dd> <dl> <dt>

3019 (0xbcb)
</dt> <dt>



Der angegebene Druckertreiber wurde im System nicht gefunden und muss heruntergeladen werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINT_JOB_RESTART_REQUIRED"></span><span id="error_print_job_restart_required"></span>**Fehler \_ beim \_ Neustart des Auftrags \_ \_ erforderlich.**
</dt> <dd> <dl> <dt>

3020 (0xbcc)
</dt> <dt>



Fehler beim Drucken des angeforderten Druckauftrags. Ein Drucksystem Update erfordert, dass der Auftrag erneut übermittelt wird.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PRINTER_DRIVER_MANIFEST"></span><span id="error_invalid_printer_driver_manifest"></span>**Fehler \_ beim \_ Drucker \_ Treiber \_ Manifest.**
</dt> <dd> <dl> <dt>

3021 (0xbcd)
</dt> <dt>



Der Druckertreiber enthält kein gültiges Manifest oder enthält zu viele Manifeste.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINTER_NOT_SHAREABLE"></span><span id="error_printer_not_shareable"></span>**Fehler \_ Drucker \_ nicht \_ share fähig**
</dt> <dd> <dl> <dt>

3022 (0xbce)
</dt> <dt>



Der angegebene Drucker kann nicht freigegeben werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_REQUEST_PAUSED"></span><span id="error_request_paused"></span>**Fehler \_ Anforderung \_ angehalten**
</dt> <dd> <dl> <dt>

3050 (0xbea)
</dt> <dt>



Der Vorgang wurde angehalten.


</dt> </dl> </dd> <dt>

<span id="ERROR_IO_REISSUE_AS_CACHED"></span><span id="error_io_reissue_as_cached"></span>**Fehler \_ - \_ e/a neu ausgestellt \_ als \_ zwischengespeichert**
</dt> <dd> <dl> <dt>

3950 (0xF 6E)
</dt> <dt>



Wiederholen Sie den angegebenen Vorgang als zwischengespeicherten e/a-Vorgang.


</dt> </dl> </dd> </dl>


## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Winerror. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[System Fehler Codes](system-error-codes.md)
</dt> </dl>

 

 




