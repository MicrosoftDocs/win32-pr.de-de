---
description: Beschreibt die Fehlercodes 1700-3999, die in der WinError.h-Headerdatei definiert sind und für Entwickler bestimmt sind.
ms.assetid: 7e57c087-53e4-443d-9227-21d9eb3cc71f
title: Systemfehlercodes (1700-3999) (WinError.h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: 707425f7714c84d92bf5bc001f57c1677183b9edbd9170236d1c629bc0aaf121
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118405601"
---
# <a name="system-error-codes-1700-3999"></a>Systemfehlercodes (1700-3999)

> [!NOTE]
> Diese Informationen sind für Entwickler gedacht, die Systemfehler debuggen. Für andere Fehler, z. B. Probleme mit Windows Update, finden Sie eine Liste der Ressourcen auf der [Seite Fehlercodes.](system-error-codes.md)

In der folgenden Liste werden [die Systemfehlercodes für](system-error-codes.md) die Fehler 1700 bis 3999 beschrieben. Sie werden von der [**GetLastError-Funktion zurückgegeben,**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) wenn viele Funktionen fehlschlagen. Verwenden Sie zum Abrufen des Beschreibungstexts für den Fehler in Ihrer Anwendung die [**Funktion FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) mit dem **Flag FORMAT MESSAGE FROM \_ \_ \_ SYSTEM.**

<dl> <dt>

<span id="RPC_S_INVALID_STRING_BINDING"></span><span id="rpc_s_invalid_string_binding"></span>**\_RPC-S \_ UNGÜLTIGE \_ \_ ZEICHENFOLGENBINDUNG**
</dt> <dd> <dl> <dt>

1700 (0x6A4)
</dt> <dt>



Die Zeichenfolgenbindung ist ungültig.


</dt> </dl> </dd> <dt>

<span id="RPC_S_WRONG_KIND_OF_BINDING"></span><span id="rpc_s_wrong_kind_of_binding"></span>**RPC \_ S \_ WRONG \_ KIND \_ OF \_ BINDING**
</dt> <dd> <dl> <dt>

1701 (0x6A5)
</dt> <dt>



Das Bindungshand handle ist nicht der richtige Typ.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INVALID_BINDING"></span><span id="rpc_s_invalid_binding"></span>**RPC \_ S \_ INVALID \_ BINDING**
</dt> <dd> <dl> <dt>

1702 (0x6A6)
</dt> <dt>



Das Bindungshand handle ist ungültig.


</dt> </dl> </dd> <dt>

<span id="RPC_S_PROTSEQ_NOT_SUPPORTED"></span><span id="rpc_s_protseq_not_supported"></span>**RPC \_ S \_ PROTSEQ \_ WIRD NICHT \_ UNTERSTÜTZT**
</dt> <dd> <dl> <dt>

1703 (0x6A7)
</dt> <dt>



Die RPC-Protokollsequenz wird nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INVALID_RPC_PROTSEQ"></span><span id="rpc_s_invalid_rpc_protseq"></span>**RPC \_ S \_ INVALID \_ RPC \_ PROTSEQ**
</dt> <dd> <dl> <dt>

1704 (0x6A8)
</dt> <dt>



Die RPC-Protokollsequenz ist ungültig.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INVALID_STRING_UUID"></span><span id="rpc_s_invalid_string_uuid"></span>**RPC \_ S \_ INVALID \_ STRING \_ UUID**
</dt> <dd> <dl> <dt>

1705 (0x6A9)
</dt> <dt>



Der UUID (Universal Unique Identifier) der Zeichenfolge ist ungültig.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INVALID_ENDPOINT_FORMAT"></span><span id="rpc_s_invalid_endpoint_format"></span>**RPC \_ S \_ UNGÜLTIGES \_ \_ ENDPUNKTFORMAT**
</dt> <dd> <dl> <dt>

1706 (0x6AA)
</dt> <dt>



Das Endpunktformat ist ungültig.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INVALID_NET_ADDR"></span><span id="rpc_s_invalid_net_addr"></span>**RPC \_ S \_ INVALID \_ NET \_ ADDR**
</dt> <dd> <dl> <dt>

1707 (0x6AB)
</dt> <dt>



Die Netzwerkadresse ist ungültig.


</dt> </dl> </dd> <dt>

<span id="RPC_S_NO_ENDPOINT_FOUND"></span><span id="rpc_s_no_endpoint_found"></span>**RPC \_ S KEIN ENDPUNKT \_ \_ \_ GEFUNDEN**
</dt> <dd> <dl> <dt>

1708 (0x6AC)
</dt> <dt>



Es wurde kein Endpunkt gefunden.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INVALID_TIMEOUT"></span><span id="rpc_s_invalid_timeout"></span>**RPC \_ S \_ INVALID \_ TIMEOUT**
</dt> <dd> <dl> <dt>

1709 (0x6AD)
</dt> <dt>



Der Timeoutwert ist ungültig.


</dt> </dl> </dd> <dt>

<span id="RPC_S_OBJECT_NOT_FOUND"></span><span id="rpc_s_object_not_found"></span>**\_ \_ RPC-S-OBJEKT \_ NICHT \_ GEFUNDEN**
</dt> <dd> <dl> <dt>

1710 (0x6AE)
</dt> <dt>



Der UUID (Universal Unique Identifier) des Objekts wurde nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="RPC_S_ALREADY_REGISTERED"></span><span id="rpc_s_already_registered"></span>**RPC \_ S \_ BEREITS \_ REGISTRIERT**
</dt> <dd> <dl> <dt>

1711 (0x6AF)
</dt> <dt>



Der UUID (Universal Unique Identifier) des Objekts wurde bereits registriert.


</dt> </dl> </dd> <dt>

<span id="RPC_S_TYPE_ALREADY_REGISTERED"></span><span id="rpc_s_type_already_registered"></span>**\_ \_ RPC-S-TYP \_ BEREITS \_ REGISTRIERT**
</dt> <dd> <dl> <dt>

1712 (0x6B0)
</dt> <dt>



Der Typ UUID (Universal Unique Identifier) wurde bereits registriert.


</dt> </dl> </dd> <dt>

<span id="RPC_S_ALREADY_LISTENING"></span><span id="rpc_s_already_listening"></span>**\_RPC-S, \_ DIE BEREITS \_ LAUSCHEN**
</dt> <dd> <dl> <dt>

1713 (0x6B1)
</dt> <dt>



Der RPC-Server lauset bereits.


</dt> </dl> </dd> <dt>

<span id="RPC_S_NO_PROTSEQS_REGISTERED"></span><span id="rpc_s_no_protseqs_registered"></span>**RPC \_ S \_ NO \_ PROTSEQS \_ REGISTERED**
</dt> <dd> <dl> <dt>

1714 (0x6B2)
</dt> <dt>



Es wurden keine Protokollsequenzen registriert.


</dt> </dl> </dd> <dt>

<span id="RPC_S_NOT_LISTENING"></span><span id="rpc_s_not_listening"></span>**\_RPC-S \_ \_ LAUSSING NICHT**
</dt> <dd> <dl> <dt>

1715 (0x6B3)
</dt> <dt>



Der RPC-Server lauset nicht.


</dt> </dl> </dd> <dt>

<span id="RPC_S_UNKNOWN_MGR_TYPE"></span><span id="rpc_s_unknown_mgr_type"></span>**RPC \_ S \_ UNBEKANNTER \_ MGR-TYP \_**
</dt> <dd> <dl> <dt>

1716 (0x6B4)
</dt> <dt>



Der Managertyp ist unbekannt.


</dt> </dl> </dd> <dt>

<span id="RPC_S_UNKNOWN_IF"></span><span id="rpc_s_unknown_if"></span>**RPC \_ S \_ UNKNOWN \_ IF**
</dt> <dd> <dl> <dt>

1717 (0x6B5)
</dt> <dt>



Die Schnittstelle ist unbekannt.


</dt> </dl> </dd> <dt>

<span id="RPC_S_NO_BINDINGS"></span><span id="rpc_s_no_bindings"></span>**RPC \_ S \_ NO \_ BINDINGS**
</dt> <dd> <dl> <dt>

1718 (0x6B6)
</dt> <dt>



Es gibt keine Bindungen.


</dt> </dl> </dd> <dt>

<span id="RPC_S_NO_PROTSEQS"></span><span id="rpc_s_no_protseqs"></span>**RPC \_ S \_ NO \_ PROTSEQS**
</dt> <dd> <dl> <dt>

1719 (0x6B7)
</dt> <dt>



Es gibt keine Protokollsequenzen.


</dt> </dl> </dd> <dt>

<span id="RPC_S_CANT_CREATE_ENDPOINT"></span><span id="rpc_s_cant_create_endpoint"></span>**RPC \_ S \_ CANT \_ CREATE \_ ENDPOINT**
</dt> <dd> <dl> <dt>

1720 (0x6B8)
</dt> <dt>



Der Endpunkt kann nicht erstellt werden.


</dt> </dl> </dd> <dt>

<span id="RPC_S_OUT_OF_RESOURCES"></span><span id="rpc_s_out_of_resources"></span>**RPC \_ S \_ OUT \_ OF \_ RESOURCES**
</dt> <dd> <dl> <dt>

1721 (0x6B9)
</dt> <dt>



Es sind nicht genügend Ressourcen verfügbar, um diesen Vorgang abschließen zu können.


</dt> </dl> </dd> <dt>

<span id="RPC_S_SERVER_UNAVAILABLE"></span><span id="rpc_s_server_unavailable"></span>**RPC \_ S SERVER NICHT \_ \_ VERFÜGBAR**
</dt> <dd> <dl> <dt>

1722 (0x6BA)
</dt> <dt>



Der RPC-Server ist nicht verfügbar.


</dt> </dl> </dd> <dt>

<span id="RPC_S_SERVER_TOO_BUSY"></span><span id="rpc_s_server_too_busy"></span>**\_ \_ RPC-S-SERVER \_ ZU \_ AUSGELASTET**
</dt> <dd> <dl> <dt>

1723 (0x6BB)
</dt> <dt>



Der RPC-Server ist zu ausgelastet, um diesen Vorgang abschließen zu können.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INVALID_NETWORK_OPTIONS"></span><span id="rpc_s_invalid_network_options"></span>**RPC \_ S \_ – \_ UNGÜLTIGE \_ NETZWERKOPTIONEN**
</dt> <dd> <dl> <dt>

1724 (0x6BC)
</dt> <dt>



Die Netzwerkoptionen sind ungültig.


</dt> </dl> </dd> <dt>

<span id="RPC_S_NO_CALL_ACTIVE"></span><span id="rpc_s_no_call_active"></span>**RPC \_ S \_ NO \_ CALL \_ ACTIVE**
</dt> <dd> <dl> <dt>

1725 (0x6BD)
</dt> <dt>



In diesem Thread sind keine Remoteprozeduraufrufe aktiv.


</dt> </dl> </dd> <dt>

<span id="RPC_S_CALL_FAILED"></span><span id="rpc_s_call_failed"></span>**FEHLER BEIM \_ RPC-S-AUFRUF \_ \_**
</dt> <dd> <dl> <dt>

1726 (0x6BE)
</dt> <dt>



Fehler beim Remoteprozeduraufruf.


</dt> </dl> </dd> <dt>

<span id="RPC_S_CALL_FAILED_DNE"></span><span id="rpc_s_call_failed_dne"></span>**FEHLER BEIM \_ \_ RPC-S-AUFRUF \_ \_ DES DNE**
</dt> <dd> <dl> <dt>

1727 (0x6BF)
</dt> <dt>



Der Remoteprozeduraufruf ist fehlgeschlagen und wurde nicht ausgeführt.


</dt> </dl> </dd> <dt>

<span id="RPC_S_PROTOCOL_ERROR"></span><span id="rpc_s_protocol_error"></span>**\_ \_ RPC-S-PROTOKOLLFEHLER \_**
</dt> <dd> <dl> <dt>

1728 (0x6C0)
</dt> <dt>



Ein RPC-Protokollfehler (Remote Procedure Call, Remoteprozeduraufruf) ist aufgetreten.


</dt> </dl> </dd> <dt>

<span id="RPC_S_PROXY_ACCESS_DENIED"></span><span id="rpc_s_proxy_access_denied"></span>**RPC \_ S PROXY ACCESS DENIED (RPC-S-PROXYZUGRIFF \_ \_ \_ VERWEIGERT)**
</dt> <dd> <dl> <dt>

1729 (0x6C1)
</dt> <dt>



Der Zugriff auf den HTTP-Proxy wird verweigert.


</dt> </dl> </dd> <dt>

<span id="RPC_S_UNSUPPORTED_TRANS_SYN"></span><span id="rpc_s_unsupported_trans_syn"></span>**RPC \_ S \_ UNSUPPORTED \_ TRANS \_ SYN**
</dt> <dd> <dl> <dt>

1730 (0x6C2)
</dt> <dt>



Die Übertragungssyntax wird vom RPC-Server nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="RPC_S_UNSUPPORTED_TYPE"></span><span id="rpc_s_unsupported_type"></span>**\_RPC S NICHT \_ UNTERSTÜTZTER \_ TYP**
</dt> <dd> <dl> <dt>

1732 (0x6C4)
</dt> <dt>



Der UUID-Typ (Universal Unique Identifier) wird nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INVALID_TAG"></span><span id="rpc_s_invalid_tag"></span>**RPC \_ S \_ UNGÜLTIGES \_ TAG**
</dt> <dd> <dl> <dt>

1733 (0x6C5)
</dt> <dt>



Das Tag ist ungültig.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INVALID_BOUND"></span><span id="rpc_s_invalid_bound"></span>**RPC \_ S \_ INVALID \_ BOUND**
</dt> <dd> <dl> <dt>

1734 (0x6C6)
</dt> <dt>



Die Arraygrenzen sind ungültig.


</dt> </dl> </dd> <dt>

<span id="RPC_S_NO_ENTRY_NAME"></span><span id="rpc_s_no_entry_name"></span>**RPC \_ S \_ KEIN \_ \_ EINTRAGSNAME**
</dt> <dd> <dl> <dt>

1735 (0x6C7)
</dt> <dt>



Die Bindung enthält keinen Eintragsnamen.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INVALID_NAME_SYNTAX"></span><span id="rpc_s_invalid_name_syntax"></span>**\_SYNTAX \_ FÜR UNGÜLTIGE \_ RPC S-NAMEN \_**
</dt> <dd> <dl> <dt>

1736 (0x6C8)
</dt> <dt>



Die Namenssyntax ist ungültig.


</dt> </dl> </dd> <dt>

<span id="RPC_S_UNSUPPORTED_NAME_SYNTAX"></span><span id="rpc_s_unsupported_name_syntax"></span>**RPC \_ \_ S– NICHT UNTERSTÜTZTE \_ \_ NAMENSSYNTAX**
</dt> <dd> <dl> <dt>

1737 (0x6C9)
</dt> <dt>



Die Namenssyntax wird nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="RPC_S_UUID_NO_ADDRESS"></span><span id="rpc_s_uuid_no_address"></span>**RPC \_ S \_ UUID \_ NO \_ ADDRESS**
</dt> <dd> <dl> <dt>

1739 (0x6CB)
</dt> <dt>



Es ist keine Netzwerkadresse verfügbar, mit der ein universeller eindeutiger Bezeichner (Universal Unique Identifier, UUID) erstellt werden kann.


</dt> </dl> </dd> <dt>

<span id="RPC_S_DUPLICATE_ENDPOINT"></span><span id="rpc_s_duplicate_endpoint"></span>**\_ \_ DOPPELTER \_ RPC-S-ENDPUNKT**
</dt> <dd> <dl> <dt>

1740 (0x6CC)
</dt> <dt>



Der Endpunkt ist ein Duplikat.


</dt> </dl> </dd> <dt>

<span id="RPC_S_UNKNOWN_AUTHN_TYPE"></span><span id="rpc_s_unknown_authn_type"></span>**UNBEKANNTER RPC \_ \_ \_ S-AUTHENTIFIZIERUNGSTYP \_**
</dt> <dd> <dl> <dt>

1741 (0x6CD)
</dt> <dt>



Der Authentifizierungstyp ist unbekannt.


</dt> </dl> </dd> <dt>

<span id="RPC_S_MAX_CALLS_TOO_SMALL"></span><span id="rpc_s_max_calls_too_small"></span>**RPC \_ S \_ MAX \_ CALLS \_ TOO \_ SMALL**
</dt> <dd> <dl> <dt>

1742 (0x6CE)
</dt> <dt>



Die maximale Anzahl von Aufrufen ist zu klein.


</dt> </dl> </dd> <dt>

<span id="RPC_S_STRING_TOO_LONG"></span><span id="rpc_s_string_too_long"></span>**\_ \_ RPC-S-ZEICHENFOLGE \_ ZU \_ LANG**
</dt> <dd> <dl> <dt>

1743 (0x6CF)
</dt> <dt>



Die Zeichenfolge ist zu lang.


</dt> </dl> </dd> <dt>

<span id="RPC_S_PROTSEQ_NOT_FOUND"></span><span id="rpc_s_protseq_not_found"></span>**RPC \_ S \_ PROTSEQ \_ NICHT \_ GEFUNDEN**
</dt> <dd> <dl> <dt>

1744 (0x6D0)
</dt> <dt>



Die RPC-Protokollsequenz wurde nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="RPC_S_PROCNUM_OUT_OF_RANGE"></span><span id="rpc_s_procnum_out_of_range"></span>**RPC \_ S \_ PROCNUM \_ AUßERHALB DES \_ \_ BEREICHS**
</dt> <dd> <dl> <dt>

1745 (0x6D1)
</dt> <dt>



Die Prozedurnummer liegt außerhalb des Bereichs.


</dt> </dl> </dd> <dt>

<span id="RPC_S_BINDING_HAS_NO_AUTH"></span><span id="rpc_s_binding_has_no_auth"></span>**RPC \_ S BINDING HAS NO AUTH (RPC-S-BINDUNG \_ VERFÜGT ÜBER KEINE \_ \_ \_ AUTHENTIFIZIERUNG)**
</dt> <dd> <dl> <dt>

1746 (0x6D2)
</dt> <dt>



Die Bindung enthält keine Authentifizierungsinformationen.


</dt> </dl> </dd> <dt>

<span id="RPC_S_UNKNOWN_AUTHN_SERVICE"></span><span id="rpc_s_unknown_authn_service"></span>**UNBEKANNTER RPC \_ \_ \_ S-AUTHENTIFIZIERUNGSDIENST \_**
</dt> <dd> <dl> <dt>

1747 (0x6D3)
</dt> <dt>



Der Authentifizierungsdienst ist unbekannt.


</dt> </dl> </dd> <dt>

<span id="RPC_S_UNKNOWN_AUTHN_LEVEL"></span><span id="rpc_s_unknown_authn_level"></span>**RPC \_ S \_ UNKNOWN \_ AUTHN \_ LEVEL**
</dt> <dd> <dl> <dt>

1748 (0x6D4)
</dt> <dt>



Die Authentifizierungsebene ist unbekannt.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INVALID_AUTH_IDENTITY"></span><span id="rpc_s_invalid_auth_identity"></span>**RPC \_ S \_ UNGÜLTIGE \_ \_ AUTHENTIFIZIERUNGSIDENTITÄT**
</dt> <dd> <dl> <dt>

1749 (0x6D5)
</dt> <dt>



Der Sicherheitskontext ist ungültig.


</dt> </dl> </dd> <dt>

<span id="RPC_S_UNKNOWN_AUTHZ_SERVICE"></span><span id="rpc_s_unknown_authz_service"></span>**RPC \_ S \_ UNKNOWN \_ \_ RPCHZ-DIENST**
</dt> <dd> <dl> <dt>

1750 (0x6D6)
</dt> <dt>



Der Autorisierungsdienst ist unbekannt.


</dt> </dl> </dd> <dt>

<span id="EPT_S_INVALID_ENTRY"></span><span id="ept_s_invalid_entry"></span>**EPT \_ S \_ UNGÜLTIGER \_ EINTRAG**
</dt> <dd> <dl> <dt>

1751 (0x6D7)
</dt> <dt>



Der Eintrag ist ungültig.


</dt> </dl> </dd> <dt>

<span id="EPT_S_CANT_PERFORM_OP"></span><span id="ept_s_cant_perform_op"></span>**EPT \_ S \_ CANT \_ PERFORM \_ OP**
</dt> <dd> <dl> <dt>

1752 (0x6D8)
</dt> <dt>



Der Serverendpunkt kann den Vorgang nicht ausführen.


</dt> </dl> </dd> <dt>

<span id="EPT_S_NOT_REGISTERED"></span><span id="ept_s_not_registered"></span>**EPT \_ S \_ NICHT \_ REGISTRIERT**
</dt> <dd> <dl> <dt>

1753 (0x6D9)
</dt> <dt>



Es sind keine Endpunkte mehr von der Endpunktzuordnung verfügbar.


</dt> </dl> </dd> <dt>

<span id="RPC_S_NOTHING_TO_EXPORT"></span><span id="rpc_s_nothing_to_export"></span>**RPC \_ S \_ NOTHING \_ TO \_ EXPORT**
</dt> <dd> <dl> <dt>

1754 (0x6DA)
</dt> <dt>



Es wurden keine Schnittstellen exportiert.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INCOMPLETE_NAME"></span><span id="rpc_s_incomplete_name"></span>**\_RPC S \_ UNVOLLSTÄNDIGER \_ NAME**
</dt> <dd> <dl> <dt>

1755 (0x6DB)
</dt> <dt>



Der Eintragsname ist unvollständig.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INVALID_VERS_OPTION"></span><span id="rpc_s_invalid_vers_option"></span>**RPC \_ S \_ INVALID \_ VERS \_ OPTION**
</dt> <dd> <dl> <dt>

1756 (0x6DC)
</dt> <dt>



Die Versionsoption ist ungültig.


</dt> </dl> </dd> <dt>

<span id="RPC_S_NO_MORE_MEMBERS"></span><span id="rpc_s_no_more_members"></span>**RPC \_ S \_ NO \_ MORE \_ MEMBERS**
</dt> <dd> <dl> <dt>

1757 (0x6DD)
</dt> <dt>



Es sind keine Member mehr vorhanden.


</dt> </dl> </dd> <dt>

<span id="RPC_S_NOT_ALL_OBJS_UNEXPORTED"></span><span id="rpc_s_not_all_objs_unexported"></span>**RPC \_ S \_ NOT \_ ALL \_ OBJS \_ UNEXPORTED**
</dt> <dd> <dl> <dt>

1758 (0x6DE)
</dt> <dt>



Es gibt nichts zu entpacken.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INTERFACE_NOT_FOUND"></span><span id="rpc_s_interface_not_found"></span>**\_ \_ RPC-S-SCHNITTSTELLE \_ NICHT \_ GEFUNDEN**
</dt> <dd> <dl> <dt>

1759 (0x6DF)
</dt> <dt>



Die Schnittstelle wurde nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="RPC_S_ENTRY_ALREADY_EXISTS"></span><span id="rpc_s_entry_already_exists"></span>**\_RPC-S-EINTRAG \_ \_ IST BEREITS \_ VORHANDEN**
</dt> <dd> <dl> <dt>

1760 (0x6E0)
</dt> <dt>



Der Eintrag ist bereits vorhanden.


</dt> </dl> </dd> <dt>

<span id="RPC_S_ENTRY_NOT_FOUND"></span><span id="rpc_s_entry_not_found"></span>**RPC \_ \_ S-EINTRAG \_ NICHT \_ GEFUNDEN**
</dt> <dd> <dl> <dt>

1761 (0x6E1)
</dt> <dt>



Der Eintrag wurde nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="RPC_S_NAME_SERVICE_UNAVAILABLE"></span><span id="rpc_s_name_service_unavailable"></span>**RPC \_ S NAME SERVICE NICHT \_ \_ \_ VERFÜGBAR**
</dt> <dd> <dl> <dt>

1762 (0x6E2)
</dt> <dt>



Der Name-Dienst ist nicht verfügbar.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INVALID_NAF_ID"></span><span id="rpc_s_invalid_naf_id"></span>**RPC \_ S \_ \_ INVALIDVAL \_ ID**
</dt> <dd> <dl> <dt>

1763 (0x6E3)
</dt> <dt>



Die Netzwerkadressfamilie ist ungültig.


</dt> </dl> </dd> <dt>

<span id="RPC_S_CANNOT_SUPPORT"></span><span id="rpc_s_cannot_support"></span>**RPC \_ S KANN NICHT UNTERSTÜTZT \_ \_ WERDEN**
</dt> <dd> <dl> <dt>

1764 (0x6E4)
</dt> <dt>



Der angeforderte Vorgang wird nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="RPC_S_NO_CONTEXT_AVAILABLE"></span><span id="rpc_s_no_context_available"></span>**RPC \_ S KEIN KONTEXT \_ \_ \_ VERFÜGBAR**
</dt> <dd> <dl> <dt>

1765 (0x6E5)
</dt> <dt>



Es ist kein Sicherheitskontext verfügbar, um den Identitätswechsel zuzulassen.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INTERNAL_ERROR"></span><span id="rpc_s_internal_error"></span>**INTERNER RPC \_ \_ \_ S-FEHLER**
</dt> <dd> <dl> <dt>

1766 (0x6E6)
</dt> <dt>



Interner Fehler bei einem Remoteprozeduraufruf (RPC).


</dt> </dl> </dd> <dt>

<span id="RPC_S_ZERO_DIVIDE"></span><span id="rpc_s_zero_divide"></span>**RPC \_ S \_ ZERO \_ DIVIDE**
</dt> <dd> <dl> <dt>

1767 (0x6E7)
</dt> <dt>



Der RPC-Server hat versucht, eine ganzzahlige Division durch 0 (null) zu erzielen.


</dt> </dl> </dd> <dt>

<span id="RPC_S_ADDRESS_ERROR"></span><span id="rpc_s_address_error"></span>**\_ \_ RPC-S-ADRESSFEHLER \_**
</dt> <dd> <dl> <dt>

1768 (0x6E8)
</dt> <dt>



Ein Adressierungsfehler ist auf dem RPC-Server aufgetreten.


</dt> </dl> </dd> <dt>

<span id="RPC_S_FP_DIV_ZERO"></span><span id="rpc_s_fp_div_zero"></span>**RPC \_ S \_ FP \_ DIV \_ ZERO**
</dt> <dd> <dl> <dt>

1769 (0x6E9)
</dt> <dt>



Ein Gleitkommavorgang auf dem RPC-Server hat eine Division durch 0 (null) verursacht.


</dt> </dl> </dd> <dt>

<span id="RPC_S_FP_UNDERFLOW"></span><span id="rpc_s_fp_underflow"></span>**RPC \_ S \_ FP \_ UNDERFLOW**
</dt> <dd> <dl> <dt>

1770 (0x6EA)
</dt> <dt>



Auf dem RPC-Server ist ein Gleitkommaunterlauf aufgetreten.


</dt> </dl> </dd> <dt>

<span id="RPC_S_FP_OVERFLOW"></span><span id="rpc_s_fp_overflow"></span>**RPC \_ S \_ FP \_ OVERFLOW**
</dt> <dd> <dl> <dt>

1771 (0x6EB)
</dt> <dt>



Auf dem RPC-Server ist ein Gleitkommaüberlauf aufgetreten.


</dt> </dl> </dd> <dt>

<span id="RPC_X_NO_MORE_ENTRIES"></span><span id="rpc_x_no_more_entries"></span>**RPC \_ X KEINE WEITEREN \_ \_ \_ EINTRÄGE**
</dt> <dd> <dl> <dt>

1772 (0x6EC)
</dt> <dt>



Die Liste der RPC-Server, die für die Bindung automatischer Handles verfügbar sind, ist erschöpft.


</dt> </dl> </dd> <dt>

<span id="RPC_X_SS_CHAR_TRANS_OPEN_FAIL"></span><span id="rpc_x_ss_char_trans_open_fail"></span>**RPC \_ X \_ SS \_ CHAR \_ TRANS \_ OPEN \_ FAIL**
</dt> <dd> <dl> <dt>

1773 (0x6ED)
</dt> <dt>



Die Zeichenübersetzungstabellendatei kann nicht geöffnet werden.


</dt> </dl> </dd> <dt>

<span id="RPC_X_SS_CHAR_TRANS_SHORT_FILE"></span><span id="rpc_x_ss_char_trans_short_file"></span>**RPC \_ X \_ SS \_ CHAR \_ TRANS \_ SHORT \_ FILE**
</dt> <dd> <dl> <dt>

1774 (0x6EE)
</dt> <dt>



Die Datei, die die Zeichenübersetzungstabelle enthält, hat weniger als 512 Bytes.


</dt> </dl> </dd> <dt>

<span id="RPC_X_SS_IN_NULL_CONTEXT"></span><span id="rpc_x_ss_in_null_context"></span>**RPC \_ X \_ SS IM \_ \_ \_ NULL-KONTEXT**
</dt> <dd> <dl> <dt>

1775 (0x6EF)
</dt> <dt>



Ein NULL-Kontexthandle wurde während eines Remoteprozeduraufrufs vom Client an den Host übergeben.


</dt> </dl> </dd> <dt>

<span id="RPC_X_SS_CONTEXT_DAMAGED"></span><span id="rpc_x_ss_context_damaged"></span>**RPC \_ \_ X-SS-KONTEXT \_ \_ BESCHÄDIGT**
</dt> <dd> <dl> <dt>

1777 (0x6F1)
</dt> <dt>



Das Kontexthandle wurde während eines Remoteprozeduraufrufs geändert.


</dt> </dl> </dd> <dt>

<span id="RPC_X_SS_HANDLES_MISMATCH"></span><span id="rpc_x_ss_handles_mismatch"></span>**RPC \_ X \_ SS \_ HANDLES \_ MISMATCH**
</dt> <dd> <dl> <dt>

1778 (0x6F2)
</dt> <dt>



Die bindungshandles, die an einen Remoteprozeduraufruf übergeben werden, stimmen nicht überein.


</dt> </dl> </dd> <dt>

<span id="RPC_X_SS_CANNOT_GET_CALL_HANDLE"></span><span id="rpc_x_ss_cannot_get_call_handle"></span>**RPC \_ X \_ SS KANN KEIN \_ \_ \_ \_ AUFRUFHANDLE ABRUFEN**
</dt> <dd> <dl> <dt>

1779 (0x6F3)
</dt> <dt>



Der Stub kann das Aufrufhandle der Remoteprozedur nicht abrufen.


</dt> </dl> </dd> <dt>

<span id="RPC_X_NULL_REF_POINTER"></span><span id="rpc_x_null_ref_pointer"></span>**RPC \_ X \_ NULL \_ REF \_ POINTER**
</dt> <dd> <dl> <dt>

1780 (0x6F4)
</dt> <dt>



Ein NULL-Verweiszeiger wurde an den Stub übergeben.


</dt> </dl> </dd> <dt>

<span id="RPC_X_ENUM_VALUE_OUT_OF_RANGE"></span><span id="rpc_x_enum_value_out_of_range"></span>**RPC \_ \_ X-ENUMERATIONSWERT \_ \_ AUßERHALB DES \_ \_ BEREICHS**
</dt> <dd> <dl> <dt>

1781 (0x6F5)
</dt> <dt>



Der Enumerationswert liegt außerhalb des Bereichs.


</dt> </dl> </dd> <dt>

<span id="RPC_X_BYTE_COUNT_TOO_SMALL"></span><span id="rpc_x_byte_count_too_small"></span>**RPC \_ X \_ \_ BYTEANZAHL ZU \_ \_ KLEIN**
</dt> <dd> <dl> <dt>

1782 (0x6F6)
</dt> <dt>



Die Byteanzahl ist zu klein.


</dt> </dl> </dd> <dt>

<span id="RPC_X_BAD_STUB_DATA"></span><span id="rpc_x_bad_stub_data"></span>**RPC \_ X \_ BAD \_ STUB \_ DATA**
</dt> <dd> <dl> <dt>

1783 (0x6F7)
</dt> <dt>



Der Stub hat ungültige Daten empfangen.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_USER_BUFFER"></span><span id="error_invalid_user_buffer"></span>**FEHLER: \_ UNGÜLTIGER \_ \_ BENUTZERPUFFER**
</dt> <dd> <dl> <dt>

1784 (0x6F8)
</dt> <dt>



Der angegebene Benutzerpuffer ist für den angeforderten Vorgang ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNRECOGNIZED_MEDIA"></span><span id="error_unrecognized_media"></span>**FEHLER \_ BEI NICHT ERKANNTEN \_ MEDIEN**
</dt> <dd> <dl> <dt>

1785 (0x6F9)
</dt> <dt>



Das Datenträgermedium wird nicht erkannt. Es ist möglicherweise nicht formatiert.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_TRUST_LSA_SECRET"></span><span id="error_no_trust_lsa_secret"></span>**\_FEHLER: \_ \_ LSA-GEHEIMNIS "NO TRUST" \_**
</dt> <dd> <dl> <dt>

1786 (0x6FA)
</dt> <dt>



Die Arbeitsstation verfügt nicht über ein Vertrauensgeheimnis.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_TRUST_SAM_ACCOUNT"></span><span id="error_no_trust_sam_account"></span>**FEHLER: \_ KEIN \_ \_ VERTRAUENSSTELLUNGS-SAM-KONTO \_**
</dt> <dd> <dl> <dt>

1787 (0x6FB)
</dt> <dt>



Die Sicherheitsdatenbank auf dem Server verfügt nicht über ein Computerkonto für diese Vertrauensstellung der Arbeitsstation.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRUSTED_DOMAIN_FAILURE"></span><span id="error_trusted_domain_failure"></span>**FEHLER: \_ FEHLER BEI VERTRAUENSWÜRDIGER \_ DOMÄNE \_**
</dt> <dd> <dl> <dt>

1788 (0x6FC)
</dt> <dt>



Fehler bei der Vertrauensstellung zwischen der primären Domäne und der vertrauenswürdigen Domäne.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRUSTED_RELATIONSHIP_FAILURE"></span><span id="error_trusted_relationship_failure"></span>**FEHLER: \_ FEHLER BEI \_ VERTRAUENSWÜRDIGER BEZIEHUNG \_**
</dt> <dd> <dl> <dt>

1789 (0x6FD)
</dt> <dt>



Bei der Vertrauensstellung zwischen der Arbeitsstation und der primären Domäne ist ein Fehler aufgetreten.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRUST_FAILURE"></span><span id="error_trust_failure"></span>**FEHLER \_ BEI \_ VERTRAUENSSTELLUNGSFEHLER**
</dt> <dd> <dl> <dt>

1790 (0x6FE)
</dt> <dt>



Fehler bei der Netzwerkanmeldung.


</dt> </dl> </dd> <dt>

<span id="RPC_S_CALL_IN_PROGRESS"></span><span id="rpc_s_call_in_progress"></span>**\_ \_ RPC-S-AUFRUF \_ WIRD \_ AUSGEFÜHRT**
</dt> <dd> <dl> <dt>

1791 (0x6FF)
</dt> <dt>



Für diesen Thread wird bereits ein Remoteprozeduraufruf ausgeführt.


</dt> </dl> </dd> <dt>

<span id="ERROR_NETLOGON_NOT_STARTED"></span><span id="error_netlogon_not_started"></span>**FEHLER \_ NETLOGON \_ NICHT \_ GESTARTET**
</dt> <dd> <dl> <dt>

1792 (0x700)
</dt> <dt>



Es wurde versucht, sich zu anmelden, aber der Netzwerkanmeldungsdienst wurde nicht gestartet.


</dt> </dl> </dd> <dt>

<span id="ERROR_ACCOUNT_EXPIRED"></span><span id="error_account_expired"></span>**FEHLERKONTO \_ \_ ABGELAUFEN**
</dt> <dd> <dl> <dt>

1793 (0x701)
</dt> <dt>



Das Konto des Benutzers ist abgelaufen.


</dt> </dl> </dd> <dt>

<span id="ERROR_REDIRECTOR_HAS_OPEN_HANDLES"></span><span id="error_redirector_has_open_handles"></span>**\_FEHLERUMLEITUNG \_ MIT \_ \_ GEÖFFNETEN HANDLES**
</dt> <dd> <dl> <dt>

1794 (0x702)
</dt> <dt>



Der Redirector wird verwendet und kann nicht entladen werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINTER_DRIVER_ALREADY_INSTALLED"></span><span id="error_printer_driver_already_installed"></span>**\_ \_ FEHLERDRUCKERTREIBER \_ BEREITS \_ INSTALLIERT**
</dt> <dd> <dl> <dt>

1795 (0x703)
</dt> <dt>



Der angegebene Druckertreiber ist bereits installiert.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNKNOWN_PORT"></span><span id="error_unknown_port"></span>**FEHLER \_ UNBEKANNTER \_ PORT**
</dt> <dd> <dl> <dt>

1796 (0x704)
</dt> <dt>



Der angegebene Port ist unbekannt.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNKNOWN_PRINTER_DRIVER"></span><span id="error_unknown_printer_driver"></span>**FEHLER \_ UNBEKANNTER \_ \_ DRUCKERTREIBER**
</dt> <dd> <dl> <dt>

1797 (0x705)
</dt> <dt>



Der Druckertreiber ist unbekannt.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNKNOWN_PRINTPROCESSOR"></span><span id="error_unknown_printprocessor"></span>**FEHLER \_ UNBEKANNTER \_ PRINTPROCESSOR**
</dt> <dd> <dl> <dt>

1798 (0x706)
</dt> <dt>



Der Druckprozessor ist unbekannt.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SEPARATOR_FILE"></span><span id="error_invalid_separator_file"></span>**FEHLER: \_ UNGÜLTIGE \_ \_ TRENNZEICHENDATEI**
</dt> <dd> <dl> <dt>

1799 (0x707)
</dt> <dt>



Die angegebene Trennzeichendatei ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PRIORITY"></span><span id="error_invalid_priority"></span>**FEHLER: \_ UNGÜLTIGE \_ PRIORITÄT**
</dt> <dd> <dl> <dt>

1800 (0x708)
</dt> <dt>



Die angegebene Priorität ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PRINTER_NAME"></span><span id="error_invalid_printer_name"></span>**FEHLER: \_ UNGÜLTIGER \_ \_ DRUCKERNAME**
</dt> <dd> <dl> <dt>

1801 (0x709)
</dt> <dt>



Der Druckername ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINTER_ALREADY_EXISTS"></span><span id="error_printer_already_exists"></span>**\_FEHLERDRUCKER \_ BEREITS \_ VORHANDEN**
</dt> <dd> <dl> <dt>

1802 (0x70A)
</dt> <dt>



Der Drucker ist bereits vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PRINTER_COMMAND"></span><span id="error_invalid_printer_command"></span>**FEHLER: \_ UNGÜLTIGER \_ \_ DRUCKERBEFEHL**
</dt> <dd> <dl> <dt>

1803 (0x70B)
</dt> <dt>



Der Druckerbefehl ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_DATATYPE"></span><span id="error_invalid_datatype"></span>**ERROR \_ INVALID \_ DATATYPE**
</dt> <dd> <dl> <dt>

1804 (0x70C)
</dt> <dt>



Der angegebene Datentyp ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_ENVIRONMENT"></span><span id="error_invalid_environment"></span>**FEHLER: \_ UNGÜLTIGE \_ UMGEBUNG**
</dt> <dd> <dl> <dt>

1805 (0x70D)
</dt> <dt>



Die angegebene Umgebung ist ungültig.


</dt> </dl> </dd> <dt>

<span id="RPC_S_NO_MORE_BINDINGS"></span><span id="rpc_s_no_more_bindings"></span>**RPC \_ S KEINE WEITEREN \_ \_ \_ BINDUNGEN**
</dt> <dd> <dl> <dt>

1806 (0x70E)
</dt> <dt>



Es gibt keine Bindungen mehr.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOLOGON_INTERDOMAIN_TRUST_ACCOUNT"></span><span id="error_nologon_interdomain_trust_account"></span>**FEHLER \_ NOLOGON \_ INTERDOMAIN \_ TRUST \_ ACCOUNT**
</dt> <dd> <dl> <dt>

1807 (0x70F)
</dt> <dt>



Das verwendete Konto ist ein Domänenübergreifendes Vertrauensstellungskonto. Verwenden Sie Ihr globales Benutzerkonto oder ihr lokales Benutzerkonto, um auf diesen Server zuzugreifen.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOLOGON_WORKSTATION_TRUST_ACCOUNT"></span><span id="error_nologon_workstation_trust_account"></span>**FEHLER \_ NOLOGON \_ WORKSTATION TRUST \_ \_ ACCOUNT**
</dt> <dd> <dl> <dt>

1808 (0x710)
</dt> <dt>



Das verwendete Konto ist ein Computerkonto. Verwenden Sie Ihr globales Benutzerkonto oder ihr lokales Benutzerkonto, um auf diesen Server zuzugreifen.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOLOGON_SERVER_TRUST_ACCOUNT"></span><span id="error_nologon_server_trust_account"></span>**FEHLER \_ NOLOGON \_ SERVER TRUST \_ \_ ACCOUNT**
</dt> <dd> <dl> <dt>

1809 (0x711)
</dt> <dt>



Das verwendete Konto ist ein Serververtrauenskonto. Verwenden Sie Ihr globales Benutzerkonto oder ihr lokales Benutzerkonto, um auf diesen Server zuzugreifen.


</dt> </dl> </dd> <dt>

<span id="ERROR_DOMAIN_TRUST_INCONSISTENT"></span><span id="error_domain_trust_inconsistent"></span>**\_ \_ FEHLERDOMÄNENVERTRAUEN \_ INKONSISTENT**
</dt> <dd> <dl> <dt>

1810 (0x712)
</dt> <dt>



Der Name oder die Sicherheits-ID (SID) der angegebenen Domäne stimmt nicht mit den Vertrauensinformationen für diese Domäne überein.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVER_HAS_OPEN_HANDLES"></span><span id="error_server_has_open_handles"></span>**FEHLERSERVER \_ \_ VERFÜGT ÜBER \_ \_ GEÖFFNETE HANDLES**
</dt> <dd> <dl> <dt>

1811 (0x713)
</dt> <dt>



Der Server wird verwendet und kann nicht entladen werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCE_DATA_NOT_FOUND"></span><span id="error_resource_data_not_found"></span>**FEHLER: \_ \_ RESSOURCENDATEN \_ NICHT \_ GEFUNDEN**
</dt> <dd> <dl> <dt>

1812 (0x714)
</dt> <dt>



Die angegebene Imagedatei enthielt keinen Ressourcenabschnitt.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCE_TYPE_NOT_FOUND"></span><span id="error_resource_type_not_found"></span>**FEHLER: \_ \_ RESSOURCENTYP \_ NICHT \_ GEFUNDEN**
</dt> <dd> <dl> <dt>

1813 (0x715)
</dt> <dt>



Der angegebene Ressourcentyp wurde in der Imagedatei nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCE_NAME_NOT_FOUND"></span><span id="error_resource_name_not_found"></span>**FEHLER: \_ \_ RESSOURCENNAME \_ NICHT \_ GEFUNDEN**
</dt> <dd> <dl> <dt>

1814 (0x716)
</dt> <dt>



Der angegebene Ressourcenname wurde in der Imagedatei nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCE_LANG_NOT_FOUND"></span><span id="error_resource_lang_not_found"></span>**\_FEHLERRESSOURCE \_ LANG NICHT \_ \_ GEFUNDEN**
</dt> <dd> <dl> <dt>

1815 (0x717)
</dt> <dt>



Die angegebene Ressourcensprach-ID wurde in der Imagedatei nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_ENOUGH_QUOTA"></span><span id="error_not_enough_quota"></span>**FEHLER: \_ NICHT \_ GENÜGEND \_ KONTINGENT**
</dt> <dd> <dl> <dt>

1816 (0x718)
</dt> <dt>



Das Kontingent reicht für die Verarbeitung dieses Befehls nicht aus.


</dt> </dl> </dd> <dt>

<span id="RPC_S_NO_INTERFACES"></span><span id="rpc_s_no_interfaces"></span>**RPC \_ S \_ KEINE \_ SCHNITTSTELLEN**
</dt> <dd> <dl> <dt>

1817 (0x719)
</dt> <dt>



Es wurden keine Schnittstellen registriert.


</dt> </dl> </dd> <dt>

<span id="RPC_S_CALL_CANCELLED"></span><span id="rpc_s_call_cancelled"></span>**RPC \_ S \_ CALL \_ CANCELLED**
</dt> <dd> <dl> <dt>

1818 (0x71A)
</dt> <dt>



Der Remoteprozeduraufruf wurde abgebrochen.


</dt> </dl> </dd> <dt>

<span id="RPC_S_BINDING_INCOMPLETE"></span><span id="rpc_s_binding_incomplete"></span>**\_ \_ RPC-S-BINDUNG \_ UNVOLLSTÄNDIG**
</dt> <dd> <dl> <dt>

1819 (0x71B)
</dt> <dt>



Das Bindungshandle enthält nicht alle erforderlichen Informationen.


</dt> </dl> </dd> <dt>

<span id="RPC_S_COMM_FAILURE"></span><span id="rpc_s_comm_failure"></span>**RPC \_ \_ S-COMM-FEHLER \_**
</dt> <dd> <dl> <dt>

1820 (0x71C)
</dt> <dt>



Während eines Remoteprozeduraufrufs ist ein Kommunikationsfehler aufgetreten.


</dt> </dl> </dd> <dt>

<span id="RPC_S_UNSUPPORTED_AUTHN_LEVEL"></span><span id="rpc_s_unsupported_authn_level"></span>**NICHT UNTERSTÜTZTE RPC \_ \_ \_ S-AUTHENTIFIZIERUNGSEBENE \_**
</dt> <dd> <dl> <dt>

1821 (0x71D)
</dt> <dt>



Die angeforderte Authentifizierungsebene wird nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="RPC_S_NO_PRINC_NAME"></span><span id="rpc_s_no_princ_name"></span>**RPC \_ S \_ NO \_ PRINC \_ NAME**
</dt> <dd> <dl> <dt>

1822 (0x71E)
</dt> <dt>



Kein Prinzipalname registriert.


</dt> </dl> </dd> <dt>

<span id="RPC_S_NOT_RPC_ERROR"></span><span id="rpc_s_not_rpc_error"></span>**RPC \_ S \_ NOT \_ RPC \_ ERROR**
</dt> <dd> <dl> <dt>

1823 (0x71F)
</dt> <dt>



Der angegebene Fehler ist kein gültiger Windows RPC-Fehlercode.


</dt> </dl> </dd> <dt>

<span id="RPC_S_UUID_LOCAL_ONLY"></span><span id="rpc_s_uuid_local_only"></span>**NUR RPC \_ S \_ UUID \_ LOCAL \_**
</dt> <dd> <dl> <dt>

1824 (0x720)
</dt> <dt>



Eine UUID, die nur auf diesem Computer gültig ist, wurde zugeordnet.


</dt> </dl> </dd> <dt>

<span id="RPC_S_SEC_PKG_ERROR"></span><span id="rpc_s_sec_pkg_error"></span>**\_RPC S SEC \_ \_ \_ PKG-FEHLER**
</dt> <dd> <dl> <dt>

1825 (0x721)
</dt> <dt>



Ein sicherheitspaketspezifischer Fehler ist aufgetreten.


</dt> </dl> </dd> <dt>

<span id="RPC_S_NOT_CANCELLED"></span><span id="rpc_s_not_cancelled"></span>**RPC \_ S \_ NICHT \_ ABGEBROCHEN**
</dt> <dd> <dl> <dt>

1826 (0x722)
</dt> <dt>



Der Thread wird nicht abgebrochen.


</dt> </dl> </dd> <dt>

<span id="RPC_X_INVALID_ES_ACTION"></span><span id="rpc_x_invalid_es_action"></span>**RPC \_ X \_ INVALID \_ ES \_ ACTION**
</dt> <dd> <dl> <dt>

1827 (0x723)
</dt> <dt>



Ungültiger Vorgang für das Codierungs-/Decodierungshandle.


</dt> </dl> </dd> <dt>

<span id="RPC_X_WRONG_ES_VERSION"></span><span id="rpc_x_wrong_es_version"></span>**RPC \_ X \_ FALSCHE \_ \_ ES-VERSION**
</dt> <dd> <dl> <dt>

1828 (0x724)
</dt> <dt>



Inkompatible Version des Serialisierungspakets.


</dt> </dl> </dd> <dt>

<span id="RPC_X_WRONG_STUB_VERSION"></span><span id="rpc_x_wrong_stub_version"></span>**\_RPC X FALSCHE \_ \_ \_ STUBVERSION**
</dt> <dd> <dl> <dt>

1829 (0x725)
</dt> <dt>



Inkompatible Version des RPC-Stubs.


</dt> </dl> </dd> <dt>

<span id="RPC_X_INVALID_PIPE_OBJECT"></span><span id="rpc_x_invalid_pipe_object"></span>**RPC \_ X \_ UNGÜLTIGES \_ \_ PIPEOBJEKT**
</dt> <dd> <dl> <dt>

1830 (0x726)
</dt> <dt>



Das RPC-Pipeobjekt ist ungültig oder beschädigt.


</dt> </dl> </dd> <dt>

<span id="RPC_X_WRONG_PIPE_ORDER"></span><span id="rpc_x_wrong_pipe_order"></span>**RPC \_ X \_ FALSCHE \_ \_ PIPEREIHENFOLGE**
</dt> <dd> <dl> <dt>

1831 (0x727)
</dt> <dt>



Ein ungültiger Vorgang wurde für ein RPC-Pipeobjekt versucht.


</dt> </dl> </dd> <dt>

<span id="RPC_X_WRONG_PIPE_VERSION"></span><span id="rpc_x_wrong_pipe_version"></span>**RPC \_ X \_ FALSCHE \_ \_ PIPEVERSION**
</dt> <dd> <dl> <dt>

1832 (0x728)
</dt> <dt>



Nicht unterstützte RPC-Pipeversion.


</dt> </dl> </dd> <dt>

<span id="RPC_S_COOKIE_AUTH_FAILED"></span><span id="rpc_s_cookie_auth_failed"></span>**FEHLER BEI \_ RPC-S-COOKIEAUTHENTIFIZIERUNG \_ \_ \_**
</dt> <dd> <dl> <dt>

1833 (0x729)
</dt> <dt>



Der HTTP-Proxyserver hat die Verbindung abgelehnt, weil die Cookieauthentifizierung fehlgeschlagen ist.


</dt> </dl> </dd> <dt>

<span id="RPC_S_GROUP_MEMBER_NOT_FOUND"></span><span id="rpc_s_group_member_not_found"></span>**\_ \_ RPC-S-GRUPPENMITGLIED \_ NICHT \_ \_ GEFUNDEN**
</dt> <dd> <dl> <dt>

1898 (0x76A)
</dt> <dt>



Das Gruppenmitglied wurde nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="EPT_S_CANT_CREATE"></span><span id="ept_s_cant_create"></span>**EPT \_ S \_ CANT \_ CREATE**
</dt> <dd> <dl> <dt>

1899 (0x76B)
</dt> <dt>



Der Endpunktzuordnungs-Datenbankeintrag konnte nicht erstellt werden.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INVALID_OBJECT"></span><span id="rpc_s_invalid_object"></span>**RPC \_ S \_ INVALID \_ OBJECT**
</dt> <dd> <dl> <dt>

1900 (0x76C)
</dt> <dt>



Der UUID (Universal Unique Identifier) des Objekts ist die NULL-UUID.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_TIME"></span><span id="error_invalid_time"></span>**FEHLER: \_ UNGÜLTIGE \_ ZEIT**
</dt> <dd> <dl> <dt>

1901 (0x76D)
</dt> <dt>



Die angegebene Zeit ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_FORM_NAME"></span><span id="error_invalid_form_name"></span>**FEHLER: \_ \_ UNGÜLTIGER \_ FORMULARNAME**
</dt> <dd> <dl> <dt>

1902 (0x76E)
</dt> <dt>



Der angegebene Formularname ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_FORM_SIZE"></span><span id="error_invalid_form_size"></span>**FEHLER \_ \_ UNGÜLTIGE \_ FORMULARGRÖßE**
</dt> <dd> <dl> <dt>

1903 (0x76F)
</dt> <dt>



Die angegebene Formulargröße ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_ALREADY_WAITING"></span><span id="error_already_waiting"></span>**FEHLER, \_ DER BEREITS \_ WARTET**
</dt> <dd> <dl> <dt>

1904 (0x770)
</dt> <dt>



Auf den angegebenen Druckerhandpunkt wird bereits gewartet.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINTER_DELETED"></span><span id="error_printer_deleted"></span>**\_ \_ FEHLERDRUCKER GELÖSCHT**
</dt> <dd> <dl> <dt>

1905 (0x771)
</dt> <dt>



Der angegebene Drucker wurde gelöscht.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PRINTER_STATE"></span><span id="error_invalid_printer_state"></span>**FEHLER: \_ \_ UNGÜLTIGER \_ DRUCKERSTATUS**
</dt> <dd> <dl> <dt>

1906 (0x772)
</dt> <dt>



Der Zustand des Druckers ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_PASSWORD_MUST_CHANGE"></span><span id="error_password_must_change"></span>**FEHLER: \_ \_ KENNWORT MUSS GEÄNDERT \_ WERDEN**
</dt> <dd> <dl> <dt>

1907 (0x773)
</dt> <dt>



Das Kennwort des Benutzers muss vor der Anmeldung geändert werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DOMAIN_CONTROLLER_NOT_FOUND"></span><span id="error_domain_controller_not_found"></span>**FEHLER: \_ \_ DOMÄNENCONTROLLER \_ WURDE NICHT \_ GEFUNDEN**
</dt> <dd> <dl> <dt>

1908 (0x774)
</dt> <dt>



Der Domänencontroller für diese Domäne wurde nicht finden.


</dt> </dl> </dd> <dt>

<span id="ERROR_ACCOUNT_LOCKED_OUT"></span><span id="error_account_locked_out"></span>**\_FEHLERKONTO \_ \_ GESPERRT**
</dt> <dd> <dl> <dt>

1909 (0x775)
</dt> <dt>



Das Konto, auf das verwiesen wird, ist derzeit gesperrt und möglicherweise nicht angemeldet.


</dt> </dl> </dd> <dt>

<span id="OR_INVALID_OXID"></span><span id="or_invalid_oxid"></span>**ODER \_ \_ UNGÜLTIGE ANTIE**
</dt> <dd> <dl> <dt>

1910 (0x776)
</dt> <dt>



Das angegebene Objektexporter wurde nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="OR_INVALID_OID"></span><span id="or_invalid_oid"></span>**ODER \_ UNGÜLTIGE \_ OID**
</dt> <dd> <dl> <dt>

1911 (0x777)
</dt> <dt>



Das angegebene Objekt wurde nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="OR_INVALID_SET"></span><span id="or_invalid_set"></span>**ODER \_ INVALID \_ SET**
</dt> <dd> <dl> <dt>

1912 (0x778)
</dt> <dt>



Der angegebene Objektrelösersatz wurde nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="RPC_S_SEND_INCOMPLETE"></span><span id="rpc_s_send_incomplete"></span>**RPC \_ S \_ SEND \_ INCOMPLETE**
</dt> <dd> <dl> <dt>

1913 (0x779)
</dt> <dt>



Einige Daten müssen noch im Anforderungspuffer gesendet werden.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INVALID_ASYNC_HANDLE"></span><span id="rpc_s_invalid_async_handle"></span>**RPC \_ S \_ INVALID \_ ASYNC \_ HANDLE**
</dt> <dd> <dl> <dt>

1914 (0x77A)
</dt> <dt>



Ungültiges asynchrones Remoteprozeduraufrufhand handle.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INVALID_ASYNC_CALL"></span><span id="rpc_s_invalid_async_call"></span>**RPC \_ S \_ INVALID \_ ASYNC \_ CALL**
</dt> <dd> <dl> <dt>

1915 (0x77B)
</dt> <dt>



Ungültiges asynchrones RPC-Aufrufhand handle für diesen Vorgang.


</dt> </dl> </dd> <dt>

<span id="RPC_X_PIPE_CLOSED"></span><span id="rpc_x_pipe_closed"></span>**RPC \_ X \_ PIPE \_ CLOSED**
</dt> <dd> <dl> <dt>

1916 (0x77C)
</dt> <dt>



Das RPC-Pipeobjekt wurde bereits geschlossen.


</dt> </dl> </dd> <dt>

<span id="RPC_X_PIPE_DISCIPLINE_ERROR"></span><span id="rpc_x_pipe_discipline_error"></span>**RPC X PIPE DISCIPLINE ERROR (RPC \_ X \_ \_ PIPE-DISZIPLINFEHLER) \_**
</dt> <dd> <dl> <dt>

1917 (0x77D)
</dt> <dt>



Der RPC-Aufruf wurde abgeschlossen, bevor alle Pipes verarbeitet wurden.


</dt> </dl> </dd> <dt>

<span id="RPC_X_PIPE_EMPTY"></span><span id="rpc_x_pipe_empty"></span>**RPC \_ X \_ PIPE \_ EMPTY**
</dt> <dd> <dl> <dt>

1918 (0x77E)
</dt> <dt>



Von der RPC-Pipe sind keine Daten mehr verfügbar.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SITENAME"></span><span id="error_no_sitename"></span>**FEHLER \_ NO \_ SITENAME**
</dt> <dd> <dl> <dt>

1919 (0x77F)
</dt> <dt>



Für diesen Computer ist kein Standortname verfügbar.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANT_ACCESS_FILE"></span><span id="error_cant_access_file"></span>**FEHLER: \_ CANT \_ ACCESS \_ FILE**
</dt> <dd> <dl> <dt>

1920 (0x780)
</dt> <dt>



Das System kann nicht auf die Datei zugreifen.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANT_RESOLVE_FILENAME"></span><span id="error_cant_resolve_filename"></span>**FEHLER: \_ CANT \_ RESOLVE \_ FILENAME**
</dt> <dd> <dl> <dt>

1921 (0x781)
</dt> <dt>



Der Name der Datei kann vom System nicht aufgelöst werden.


</dt> </dl> </dd> <dt>

<span id="RPC_S_ENTRY_TYPE_MISMATCH"></span><span id="rpc_s_entry_type_mismatch"></span>**KONFLIKT ZWISCHEN \_ RPC-S-EINTRAGSTYP \_ \_ \_**
</dt> <dd> <dl> <dt>

1922 (0x782)
</dt> <dt>



Der Eintrag ist nicht vom erwarteten Typ.


</dt> </dl> </dd> <dt>

<span id="RPC_S_NOT_ALL_OBJS_EXPORTED"></span><span id="rpc_s_not_all_objs_exported"></span>**RPC \_ S \_ NOT \_ ALL \_ OBJS \_ EXPORTED**
</dt> <dd> <dl> <dt>

1923 (0x783)
</dt> <dt>



Nicht alle Objekt-UUIDs konnten in den angegebenen Eintrag exportiert werden.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INTERFACE_NOT_EXPORTED"></span><span id="rpc_s_interface_not_exported"></span>**\_ \_ RPC-S-SCHNITTSTELLE \_ NICHT \_ EXPORTIERT**
</dt> <dd> <dl> <dt>

1924 (0x784)
</dt> <dt>



Die Schnittstelle konnte nicht in den angegebenen Eintrag exportiert werden.


</dt> </dl> </dd> <dt>

<span id="RPC_S_PROFILE_NOT_ADDED"></span><span id="rpc_s_profile_not_added"></span>**\_ \_ RPC-S-PROFIL \_ NICHT \_ HINZUGEFÜGT**
</dt> <dd> <dl> <dt>

1925 (0x785)
</dt> <dt>



Der angegebene Profileintrag konnte nicht hinzugefügt werden.


</dt> </dl> </dd> <dt>

<span id="RPC_S_PRF_ELT_NOT_ADDED"></span><span id="rpc_s_prf_elt_not_added"></span>**RPC \_ S \_ PRF \_ ELT NICHT \_ \_ HINZUGEFÜGT**
</dt> <dd> <dl> <dt>

1926 (0x786)
</dt> <dt>



Das angegebene Profilelement konnte nicht hinzugefügt werden.


</dt> </dl> </dd> <dt>

<span id="RPC_S_PRF_ELT_NOT_REMOVED"></span><span id="rpc_s_prf_elt_not_removed"></span>**RPC \_ S \_ PRF \_ ELT NICHT \_ \_ ENTFERNT**
</dt> <dd> <dl> <dt>

1927 (0x787)
</dt> <dt>



Das angegebene Profilelement konnte nicht entfernt werden.


</dt> </dl> </dd> <dt>

<span id="RPC_S_GRP_ELT_NOT_ADDED"></span><span id="rpc_s_grp_elt_not_added"></span>**RPC \_ S \_ GRP \_ ELT NICHT \_ \_ HINZUGEFÜGT**
</dt> <dd> <dl> <dt>

1928 (0x788)
</dt> <dt>



Das Group-Element konnte nicht hinzugefügt werden.


</dt> </dl> </dd> <dt>

<span id="RPC_S_GRP_ELT_NOT_REMOVED"></span><span id="rpc_s_grp_elt_not_removed"></span>**RPC \_ S \_ GRP \_ ELT NICHT \_ \_ ENTFERNT**
</dt> <dd> <dl> <dt>

1929 (0x789)
</dt> <dt>



Das Group-Element konnte nicht entfernt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_KM_DRIVER_BLOCKED"></span><span id="error_km_driver_blocked"></span>**FEHLER: \_ \_ KM-TREIBER \_ BLOCKIERT**
</dt> <dd> <dl> <dt>

1930 (0x78A)
</dt> <dt>



Der Druckertreiber ist nicht mit einer Richtlinie kompatibel, die auf Ihrem Computer aktiviert ist, die NT 4.0-Treiber blockiert.


</dt> </dl> </dd> <dt>

<span id="ERROR_CONTEXT_EXPIRED"></span><span id="error_context_expired"></span>**FEHLERKONTEXT \_ \_ ABGELAUFEN**
</dt> <dd> <dl> <dt>

1931 (0x78B)
</dt> <dt>



Der Kontext ist abgelaufen und kann nicht mehr verwendet werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_PER_USER_TRUST_QUOTA_EXCEEDED"></span><span id="error_per_user_trust_quota_exceeded"></span>**FEHLER \_ PRO \_ KONTINGENT FÜR \_ BENUTZERVERTRAUEN \_ \_ ÜBERSCHRITTEN**
</dt> <dd> <dl> <dt>

1932 (0x78C)
</dt> <dt>



Das Kontingent für die Erstellung delegierter Vertrauensstellungen des aktuellen Benutzers wurde überschritten.


</dt> </dl> </dd> <dt>

<span id="ERROR_ALL_USER_TRUST_QUOTA_EXCEEDED"></span><span id="error_all_user_trust_quota_exceeded"></span>**FEHLER: \_ ALLE \_ KONTINGENTE \_ FÜR DIE \_ BENUTZERVERTRAUENSSTELLUNG \_ ÜBERSCHRITTEN**
</dt> <dd> <dl> <dt>

1933 (0x78D)
</dt> <dt>



Das gesamt Kontingent für die Erstellung delegierter Vertrauensstellungen wurde überschritten.


</dt> </dl> </dd> <dt>

<span id="ERROR_USER_DELETE_TRUST_QUOTA_EXCEEDED"></span><span id="error_user_delete_trust_quota_exceeded"></span>**FEHLER: \_ \_ KONTINGENT FÜR \_ VERTRAUENSSTELLUNG \_ DURCH \_ BENUTZERLÖSCHUNG ÜBERSCHRITTEN**
</dt> <dd> <dl> <dt>

1934 (0x78E)
</dt> <dt>



Das Kontingent für das Löschen delegierter Vertrauensstellungen des aktuellen Benutzers wurde überschritten.


</dt> </dl> </dd> <dt>

<span id="ERROR_AUTHENTICATION_FIREWALL_FAILED"></span><span id="error_authentication_firewall_failed"></span>**FEHLER: \_ FEHLER BEI DER FIREWALL FÜR DIE \_ \_ AUTHENTIFIZIERUNG**
</dt> <dd> <dl> <dt>

1935 (0x78F)
</dt> <dt>



Der Computer, bei dem Sie sich anmelden, wird durch eine Authentifizierungsfirewall geschützt. Das angegebene Konto darf sich nicht beim Computer authentifizieren.


</dt> </dl> </dd> <dt>

<span id="ERROR_REMOTE_PRINT_CONNECTIONS_BLOCKED"></span><span id="error_remote_print_connections_blocked"></span>**FEHLER: \_ \_ \_ REMOTEDRUCKVERBINDUNGEN \_ BLOCKIERT**
</dt> <dd> <dl> <dt>

1936 (0x790)
</dt> <dt>



Remoteverbindungen mit dem Druckspooler werden durch eine Richtlinie blockiert, die auf Ihrem Computer festgelegt ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_NTLM_BLOCKED"></span><span id="error_ntlm_blocked"></span>**FEHLER \_ NTLM \_ BLOCKIERT**
</dt> <dd> <dl> <dt>

1937 (0x791)
</dt> <dt>



Fehler bei der Authentifizierung, weil die NTLM-Authentifizierung deaktiviert wurde.


</dt> </dl> </dd> <dt>

<span id="ERROR_PASSWORD_CHANGE_REQUIRED"></span><span id="error_password_change_required"></span>**FEHLER: \_ \_ KENNWORTÄNDERUNG \_ ERFORDERLICH**
</dt> <dd> <dl> <dt>

1938 (0x792)
</dt> <dt>



Anmeldefehler: Die EAS-Richtlinie erfordert, dass der Benutzer sein Kennwort ändert, bevor dieser Vorgang ausgeführt werden kann.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PIXEL_FORMAT"></span><span id="error_invalid_pixel_format"></span>**FEHLER: \_ \_ UNGÜLTIGES \_ PIXELFORMAT**
</dt> <dd> <dl> <dt>

2000 (0x7D0)
</dt> <dt>



Das Pixelformat ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_DRIVER"></span><span id="error_bad_driver"></span>**FEHLER: \_ \_ FEHLERHAFTER TREIBER**
</dt> <dd> <dl> <dt>

2001 (0x7D1)
</dt> <dt>



Der angegebene Treiber ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_WINDOW_STYLE"></span><span id="error_invalid_window_style"></span>**FEHLER: \_ \_ UNGÜLTIGER \_ FENSTERSTIL**
</dt> <dd> <dl> <dt>

2002 (0x7D2)
</dt> <dt>



Der Fensterstil oder das Klassenattribut ist für diesen Vorgang ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_METAFILE_NOT_SUPPORTED"></span><span id="error_metafile_not_supported"></span>**\_FEHLERMETADATEI \_ WIRD NICHT \_ UNTERSTÜTZT**
</dt> <dd> <dl> <dt>

2003 (0x7D3)
</dt> <dt>



Der angeforderte Metadateivorgang wird nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSFORM_NOT_SUPPORTED"></span><span id="error_transform_not_supported"></span>**\_FEHLERTRANSFORMATION \_ NICHT \_ UNTERSTÜTZT**
</dt> <dd> <dl> <dt>

2004 (0x7D4)
</dt> <dt>



Der angeforderte Transformationsvorgang wird nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLIPPING_NOT_SUPPORTED"></span><span id="error_clipping_not_supported"></span>**\_FEHLERBESCHNEIDUNG \_ WIRD NICHT \_ UNTERSTÜTZT**
</dt> <dd> <dl> <dt>

2005 (0x7D5)
</dt> <dt>



Der angeforderte Clippingvorgang wird nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_CMM"></span><span id="error_invalid_cmm"></span>**FEHLER \_ \_ UNGÜLTIGER CMM**
</dt> <dd> <dl> <dt>

2010 (0x7DA)
</dt> <dt>



Das angegebene Farbverwaltungsmodul ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PROFILE"></span><span id="error_invalid_profile"></span>**FEHLER: \_ UNGÜLTIGES \_ PROFIL**
</dt> <dd> <dl> <dt>

2011 (0x7DB)
</dt> <dt>



Das angegebene Farbprofil ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_TAG_NOT_FOUND"></span><span id="error_tag_not_found"></span>**FEHLERTAG \_ \_ NICHT \_ GEFUNDEN**
</dt> <dd> <dl> <dt>

2012 (0x7DC)
</dt> <dt>



Das angegebene Tag wurde nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_TAG_NOT_PRESENT"></span><span id="error_tag_not_present"></span>**FEHLERTAG \_ \_ NICHT \_ VORHANDEN**
</dt> <dd> <dl> <dt>

2013 (0x7DD)
</dt> <dt>



Ein erforderliches Tag ist nicht vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DUPLICATE_TAG"></span><span id="error_duplicate_tag"></span>**\_FEHLERDUPLIZIERTES \_ TAG**
</dt> <dd> <dl> <dt>

2014 (0x7DE)
</dt> <dt>



Das angegebene Tag ist bereits vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_PROFILE_NOT_ASSOCIATED_WITH_DEVICE"></span><span id="error_profile_not_associated_with_device"></span>**\_FEHLERPROFIL, DAS DEM GERÄT NICHT ZUGEORDNET \_ \_ \_ \_ IST**
</dt> <dd> <dl> <dt>

2015 (0x7DF)
</dt> <dt>



Das angegebene Farbprofil ist dem angegebenen Gerät nicht zugeordnet.


</dt> </dl> </dd> <dt>

<span id="ERROR_PROFILE_NOT_FOUND"></span><span id="error_profile_not_found"></span>**FEHLERPROFIL \_ \_ NICHT \_ GEFUNDEN**
</dt> <dd> <dl> <dt>

2016 (0x7E0)
</dt> <dt>



Das angegebene Farbprofil wurde nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_COLORSPACE"></span><span id="error_invalid_colorspace"></span>**FEHLER: \_ \_ UNGÜLTIGER COLORSPACE**
</dt> <dd> <dl> <dt>

2017 (0x7E1)
</dt> <dt>



Der angegebene Farbraum ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_ICM_NOT_ENABLED"></span><span id="error_icm_not_enabled"></span>**FEHLER \_ ICM \_ NICHT \_ AKTIVIERT**
</dt> <dd> <dl> <dt>

2018 (0x7E2)
</dt> <dt>



Die Bildfarbverwaltung ist nicht aktiviert.


</dt> </dl> </dd> <dt>

<span id="ERROR_DELETING_ICM_XFORM"></span><span id="error_deleting_icm_xform"></span>**FEHLER \_ BEIM LÖSCHEN ICM \_ \_ XFORM**
</dt> <dd> <dl> <dt>

2019 (0x7E3)
</dt> <dt>



Fehler beim Löschen der Farbtransformation.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_TRANSFORM"></span><span id="error_invalid_transform"></span>**FEHLER: \_ UNGÜLTIGE \_ TRANSFORMATION**
</dt> <dd> <dl> <dt>

2020 (0x7E4)
</dt> <dt>



Die angegebene Farbtransformation ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_COLORSPACE_MISMATCH"></span><span id="error_colorspace_mismatch"></span>**\_FEHLER: \_ FARBRAUMKONFLIKT**
</dt> <dd> <dl> <dt>

2021 (0x7E5)
</dt> <dt>



Die angegebene Transformation passt nicht zum Farbraum der Bitmap.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_COLORINDEX"></span><span id="error_invalid_colorindex"></span>**FEHLER \_ \_ UNGÜLTIGER COLORINDEX**
</dt> <dd> <dl> <dt>

2022 (0x7E6)
</dt> <dt>



Der angegebene benannte Farbindex ist im Profil nicht vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_PROFILE_DOES_NOT_MATCH_DEVICE"></span><span id="error_profile_does_not_match_device"></span>**FEHLERPROFIL \_ \_ NICHT MIT GERÄT \_ \_ \_ ÜBEREINSTIMMEN**
</dt> <dd> <dl> <dt>

2023 (0x7E7)
</dt> <dt>



Das angegebene Profil ist für ein Gerät vorgesehen, das einen anderen Typ als das angegebene Gerät hat.


</dt> </dl> </dd> <dt>

<span id="ERROR_CONNECTED_OTHER_PASSWORD"></span><span id="error_connected_other_password"></span>**FEHLER \_ : ANDERES KENNWORT \_ \_ VERBUNDEN**
</dt> <dd> <dl> <dt>

2108 (0x83C)
</dt> <dt>



Die Netzwerkverbindung wurde erfolgreich hergestellt, aber der Benutzer musste zur Eingabe eines anderen Kennworts aufgefordert werden als das ursprünglich angegebene.


</dt> </dl> </dd> <dt>

<span id="ERROR_CONNECTED_OTHER_PASSWORD_DEFAULT"></span><span id="error_connected_other_password_default"></span>**FEHLER \_ CONNECTED OTHER PASSWORD \_ \_ \_ DEFAULT**
</dt> <dd> <dl> <dt>

2109 (0x83D)
</dt> <dt>



Die Netzwerkverbindung wurde erfolgreich mithilfe der Standardanmeldeinformationen hergestellt.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_USERNAME"></span><span id="error_bad_username"></span>**FEHLER: \_ \_ FEHLERHAFTER BENUTZERNAME**
</dt> <dd> <dl> <dt>

2202 (0x89A)
</dt> <dt>



Der angegebene Benutzername ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_CONNECTED"></span><span id="error_not_connected"></span>**FEHLER \_ NICHT \_ VERBUNDEN**
</dt> <dd> <dl> <dt>

2250 (0x8CA)
</dt> <dt>



Diese Netzwerkverbindung ist nicht vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_OPEN_FILES"></span><span id="error_open_files"></span>**FEHLER \_ BEIM ÖFFNEN VON \_ DATEIEN**
</dt> <dd> <dl> <dt>

2401 (0x961)
</dt> <dt>



Diese Netzwerkverbindung verfügt über geöffnete Dateien oder ausstehende Anforderungen.


</dt> </dl> </dd> <dt>

<span id="ERROR_ACTIVE_CONNECTIONS"></span><span id="error_active_connections"></span>**FEHLER \_ AKTIVE \_ VERBINDUNGEN**
</dt> <dd> <dl> <dt>

2402 (0x962)
</dt> <dt>



Aktive Verbindungen sind weiterhin vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_IN_USE"></span><span id="error_device_in_use"></span>**FEHLER \_ \_ BEIM VERWENDEN DES \_ GERÄTS**
</dt> <dd> <dl> <dt>

2404 (0x964)
</dt> <dt>



Das Gerät wird von einem aktiven Prozess verwendet und kann nicht getrennt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNKNOWN_PRINT_MONITOR"></span><span id="error_unknown_print_monitor"></span>**FEHLER \_ UNBEKANNTER \_ \_ DRUCKMONITOR**
</dt> <dd> <dl> <dt>

3000 (0xBB8)
</dt> <dt>



Der angegebene Druckmonitor ist unbekannt.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINTER_DRIVER_IN_USE"></span><span id="error_printer_driver_in_use"></span>**VERWENDETER \_ \_ FEHLERDRUCKERTREIBER \_ \_**
</dt> <dd> <dl> <dt>

3001 (0xBB9)
</dt> <dt>



Der angegebene Druckertreiber wird derzeit verwendet.


</dt> </dl> </dd> <dt>

<span id="ERROR_SPOOL_FILE_NOT_FOUND"></span><span id="error_spool_file_not_found"></span>**\_FEHLER: \_ SPOOLDATEI NICHT \_ \_ GEFUNDEN**
</dt> <dd> <dl> <dt>

3002 (0xBBA)
</dt> <dt>



Die Spooldatei wurde nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_SPL_NO_STARTDOC"></span><span id="error_spl_no_startdoc"></span>**FEHLER \_ SPL \_ NO \_ STARTDOC**
</dt> <dd> <dl> <dt>

3003 (0xBBB)
</dt> <dt>



Es wurde kein StartDocPrinter-Aufruf ausgegeben.


</dt> </dl> </dd> <dt>

<span id="ERROR_SPL_NO_ADDJOB"></span><span id="error_spl_no_addjob"></span>**FEHLER \_ SPL \_ NO \_ ADDJOB**
</dt> <dd> <dl> <dt>

3004 (0xBBC)
</dt> <dt>



Ein AddJob-Aufruf wurde nicht ausgegeben.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINT_PROCESSOR_ALREADY_INSTALLED"></span><span id="error_print_processor_already_installed"></span>**\_ \_ FEHLERDRUCKPROZESSOR BEREITS \_ \_ INSTALLIERT**
</dt> <dd> <dl> <dt>

3005 (0xBBD)
</dt> <dt>



Der angegebene Druckprozessor wurde bereits installiert.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINT_MONITOR_ALREADY_INSTALLED"></span><span id="error_print_monitor_already_installed"></span>**\_ \_ FEHLERDRUCKMONITOR BEREITS \_ \_ INSTALLIERT**
</dt> <dd> <dl> <dt>

3006 (0xBBE)
</dt> <dt>



Der angegebene Druckmonitor wurde bereits installiert.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PRINT_MONITOR"></span><span id="error_invalid_print_monitor"></span>**FEHLER: \_ UNGÜLTIGER \_ \_ DRUCKMONITOR**
</dt> <dd> <dl> <dt>

3007 (0xBBF)
</dt> <dt>



Der angegebene Druckmonitor verfügt nicht über die erforderlichen Funktionen.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINT_MONITOR_IN_USE"></span><span id="error_print_monitor_in_use"></span>**VERWENDETER \_ \_ FEHLERDRUCKMONITOR \_ \_**
</dt> <dd> <dl> <dt>

3008 (0xBC0)
</dt> <dt>



Der angegebene Druckmonitor wird derzeit verwendet.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINTER_HAS_JOBS_QUEUED"></span><span id="error_printer_has_jobs_queued"></span>**\_FEHLERDRUCKER HAT AUFTRÄGE IN DIE \_ \_ \_ WARTESCHLANGE EINGEREIHT**
</dt> <dd> <dl> <dt>

3009 (0xBC1)
</dt> <dt>



Der angeforderte Vorgang ist nicht zulässig, wenn Aufträge in der Warteschlange des Druckers stehen.


</dt> </dl> </dd> <dt>

<span id="ERROR_SUCCESS_REBOOT_REQUIRED"></span><span id="error_success_reboot_required"></span>**FEHLER \_ BEI \_ ERFOLGREICHEM NEUSTART \_ ERFORDERLICH**
</dt> <dd> <dl> <dt>

3010 (0xBC2)
</dt> <dt>



Der angeforderte Vorgang ist erfolgreich. Änderungen sind erst wirksam, wenn das System neu gestartet wurde.


</dt> </dl> </dd> <dt>

<span id="ERROR_SUCCESS_RESTART_REQUIRED"></span><span id="error_success_restart_required"></span>**FEHLER \_ BEI \_ ERFOLGREICHEM NEUSTART \_ ERFORDERLICH**
</dt> <dd> <dl> <dt>

3011 (0xBC3)
</dt> <dt>



Der angeforderte Vorgang ist erfolgreich. Änderungen werden erst wirksam, wenn der Dienst neu gestartet wird.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINTER_NOT_FOUND"></span><span id="error_printer_not_found"></span>**\_ \_ FEHLERDRUCKER NICHT \_ GEFUNDEN**
</dt> <dd> <dl> <dt>

3012 (0xBC4)
</dt> <dt>



Es wurden keine Drucker gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINTER_DRIVER_WARNED"></span><span id="error_printer_driver_warned"></span>**\_ \_ FEHLERDRUCKERTREIBER \_ GEWARNT**
</dt> <dd> <dl> <dt>

3013 (0xBC5)
</dt> <dt>



Der Druckertreiber ist bekanntermaßen unzuverlässig.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINTER_DRIVER_BLOCKED"></span><span id="error_printer_driver_blocked"></span>**\_ \_ FEHLERDRUCKERTREIBER \_ BLOCKIERT**
</dt> <dd> <dl> <dt>

3014 (0xBC6)
</dt> <dt>



Es ist bekannt, dass der Druckertreiber das System beeinträchtigt.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINTER_DRIVER_PACKAGE_IN_USE"></span><span id="error_printer_driver_package_in_use"></span>**ERROR \_ PRINTER DRIVER PACKAGE IN USE (FEHLERDRUCKERTREIBERPAKET \_ IN \_ \_ \_ GEBRAUCH)**
</dt> <dd> <dl> <dt>

3015 (0xBC7)
</dt> <dt>



Das angegebene Druckertreiberpaket wird derzeit verwendet.


</dt> </dl> </dd> <dt>

<span id="ERROR_CORE_DRIVER_PACKAGE_NOT_FOUND"></span><span id="error_core_driver_package_not_found"></span>**\_ \_ FEHLERKERNTREIBERPAKET \_ NICHT \_ \_ GEFUNDEN**
</dt> <dd> <dl> <dt>

3016 (0xBC8)
</dt> <dt>



Es konnte kein Kerntreiberpaket gefunden werden, das für das Druckertreiberpaket erforderlich ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_FAIL_REBOOT_REQUIRED"></span><span id="error_fail_reboot_required"></span>**FEHLER: \_ \_ NEUSTARTFEHLER \_ ERFORDERLICH**
</dt> <dd> <dl> <dt>

3017 (0xBC9)
</dt> <dt>



Der angeforderte Vorgang ist fehlgeschlagen. Ein Systemneustart ist erforderlich, um die vorgenommenen Änderungen rückgängig zu machen.


</dt> </dl> </dd> <dt>

<span id="ERROR_FAIL_REBOOT_INITIATED"></span><span id="error_fail_reboot_initiated"></span>**\_FEHLER: \_ \_ NEUSTARTFEHLER INITIIERT**
</dt> <dd> <dl> <dt>

3018 (0xBCA)
</dt> <dt>



Der angeforderte Vorgang ist fehlgeschlagen. Ein Systemneustart wurde initiiert, um die vorgenommenen Änderungen rückgängig zu machen.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINTER_DRIVER_DOWNLOAD_NEEDED"></span><span id="error_printer_driver_download_needed"></span>**FEHLER \_ BEIM HERUNTERLADEN DES \_ \_ DRUCKERTREIBERS \_ ERFORDERLICH**
</dt> <dd> <dl> <dt>

3019 (0xBCB)
</dt> <dt>



Der angegebene Druckertreiber wurde auf dem System nicht gefunden und muss heruntergeladen werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINT_JOB_RESTART_REQUIRED"></span><span id="error_print_job_restart_required"></span>**FEHLER: NEUSTART DES \_ \_ \_ \_ DRUCKAUFTRAGS ERFORDERLICH**
</dt> <dd> <dl> <dt>

3020 (0xBCC)
</dt> <dt>



Der angeforderte Druckauftrag konnte nicht gedruckt werden. Für eine Aktualisierung des Drucksystems muss der Auftrag erneut übermittelt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PRINTER_DRIVER_MANIFEST"></span><span id="error_invalid_printer_driver_manifest"></span>**FEHLER: \_ UNGÜLTIGES \_ \_ \_ DRUCKERTREIBERMANIFEST**
</dt> <dd> <dl> <dt>

3021 (0xBCD)
</dt> <dt>



Der Druckertreiber enthält kein gültiges Manifest oder zu viele Manifeste.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINTER_NOT_SHAREABLE"></span><span id="error_printer_not_shareable"></span>**\_FEHLERDRUCKER KANN NICHT FREIGEGEBEN \_ \_ WERDEN**
</dt> <dd> <dl> <dt>

3022 (0xBCE)
</dt> <dt>



Der angegebene Drucker kann nicht freigegeben werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_REQUEST_PAUSED"></span><span id="error_request_paused"></span>**FEHLERANFORDERUNG \_ \_ ANGEHALTEN**
</dt> <dd> <dl> <dt>

3050 (0xBEA)
</dt> <dt>



Der Vorgang wurde angehalten.


</dt> </dl> </dd> <dt>

<span id="ERROR_IO_REISSUE_AS_CACHED"></span><span id="error_io_reissue_as_cached"></span>**FEHLER: \_ \_ E/A ERNEUT \_ ALS \_ ZWISCHENGESPEICHERT**
</dt> <dd> <dl> <dt>

3950 (0xF6E)
</dt> <dt>



Geben Sie den angegebenen Vorgang erneut als zwischengespeicherten E/A-Vorgang aus.


</dt> </dl> </dd> </dl>


## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>WinError.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Systemfehlercodes](system-error-codes.md)
</dt> </dl>

 

 




