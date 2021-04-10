---
title: Schnittstellenregistrierungsflags (rpcdce. h)
description: Die folgenden Konstanten werden im flags-Parameter der RpcServerRegisterIf2-und RpcServerRegisterIfEx-Funktionen verwendet.
ms.assetid: 387311c0-13df-4497-a0ac-ce6aec0e726c
topic_type:
- apiref
api_name:
- RPC_IF_ALLOW_CALLBACKS_WITH_NO_AUTH
- RPC_IF_ALLOW_LOCAL_ONLY
- RPC_IF_AUTOLISTEN
- RPC_IF_OLE
- RPC_IF_ALLOW_UNKNOWN_AUTHORITY
- RPC_IF_ALLOW_SECURE_ONLY
- RPC_IF_SEC_NO_CACHE
api_location:
- Rpcdce.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8af938038d2bc7000d80268fb4cb00941f6b282b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105699"
---
# <a name="interface-registration-flags"></a>Schnittstellenregistrierungsflags

Die folgenden Konstanten werden im *Flags* -Parameter der [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2) -und [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex) -Funktionen verwendet.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Konstante</th>
<th style="text-align: left;">BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="0"></span><dl> <dt><strong>1,0</strong></dt> </dl></td>
<td style="text-align: left;">Standard Schnittstellen Semantik.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="RPC_IF_ALLOW_CALLBACKS_WITH_NO_AUTH"></span><span id="rpc_if_allow_callbacks_with_no_auth"></span><dl> <dt><strong>RPC_IF_ALLOW_CALLBACKS_WITH_NO_AUTH</strong></dt> </dl></td>
<td style="text-align: left;">Wenn dieses Schnittstellenflag registriert ist, ruft die RPC-Laufzeit den registrierten Sicherheits Rückruf für alle Aufrufe auf, unabhängig von der Identität, der Protokoll Sequenz oder der Authentifizierungs Ebene des Clients.<br/>
<blockquote>
[!Note]<br />
Dieses Flag ist ab Windows XP mit SP2 und Windows Server 2003 mit SP1 verfügbar. Wenn dieses Flag nicht festgelegt ist, filtert RPC automatisch alle nicht authentifizierten Aufrufe, bevor Sie den Sicherheits Rückruf erreichen.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="RPC_IF_ALLOW_LOCAL_ONLY"></span><span id="rpc_if_allow_local_only"></span><dl> <dt><strong>RPC_IF_ALLOW_LOCAL_ONLY</strong></dt> </dl></td>
<td style="text-align: left;">Wenn dieses Schnittstellenflag registriert ist, lehnt die RPC-Laufzeit Aufrufe von Remote Clients ab. Alle lokalen Aufrufe, die ncadg_ *-und ncacn_ *-Protokoll Sequenzen verwenden, werden ebenfalls abgelehnt, mit Ausnahme von ncacn_np. RPC lässt ncacn_NP Aufrufe nur zu, wenn der Aufruf nicht von SRV stammt. Aufrufe von Ncalrpc werden immer verarbeitet.<br/>
<blockquote>
[!Note]<br />
Dieses Flag ist ab Windows XP mit SP2 und Windows Server 2003 mit SP1 verfügbar.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="RPC_IF_AUTOLISTEN"></span><span id="rpc_if_autolisten"></span><dl> <dt><strong>RPC_IF_AUTOLISTEN</strong></dt> </dl></td>
<td style="text-align: left;">Dabei handelt es sich um eine Schnittstelle zum <strong>automatischen lauschen</strong> . Die Laufzeit beginnt mit dem lauschen auf Anrufe, sobald die erste autolistening-Schnittstelle registriert ist, und beendet die Überwachung, wenn die Registrierung der letzten autolistening-Schnittstelle aufgehoben wird.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="RPC_IF_OLE"></span><span id="rpc_if_ole"></span><dl> <dt><strong>RPC_IF_OLE</strong></dt> </dl></td>
<td style="text-align: left;">Für OLE reserviert. Verwenden Sie dieses Flag nicht.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="RPC_IF_ALLOW_UNKNOWN_AUTHORITY"></span><span id="rpc_if_allow_unknown_authority"></span><dl> <dt><strong>RPC_IF_ALLOW_UNKNOWN_AUTHORITY</strong></dt> </dl></td>
<td style="text-align: left;">Derzeit nicht implementiert.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="RPC_IF_ALLOW_SECURE_ONLY"></span><span id="rpc_if_allow_secure_only"></span><dl> <dt><strong>RPC_IF_ALLOW_SECURE_ONLY</strong></dt> </dl></td>
<td style="text-align: left;">Schränkt Verbindungen mit Clients ein, die eine Autorisierungs Ebene höher als RPC_C_AUTHN_LEVEL_NONE verwenden. Wenn dieses Flag angegeben wird, können Clients in der <strong>null</strong> -Sitzung durchlaufen werden. Unter Windows XP und Windows Server 2003 sind solche Clients nicht zulässig. Clients, bei denen der RPC_IF_ALLOW_SECURE_ONLY Test fehlschlägt, erhalten einen RPC_S_ACCESS_DENIED Fehler. Die Verwendung des RPC_IF_ALLOW_SECURE_ONLY-Flags impliziert oder garantiert keine hohe Berechtigungsebene für den Teil des aufrufenden Benutzers. RPC überprüft nur, ob der Benutzer über gültige Anmelde Informationen verfügt. der aufrufende Benutzer verwendet möglicherweise das Gastkonto oder andere Konten mit niedrigen Berechtigungen. Nehmen Sie bei Verwendung von RPC_IF_ALLOW_SECURE_ONLY keine hohen Berechtigungen an.<br/> <strong>Windows NT 4,0 und Windows Me/98/95:  </strong><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="RPC_IF_SEC_NO_CACHE"></span><span id="rpc_if_sec_no_cache"></span><dl> <dt><strong>RPC_IF_SEC_NO_CACHE</strong></dt> </dl></td>
<td style="text-align: left;">Deaktiviert das Zwischenspeichern des Sicherheits Rückrufs und erzwingt einen Sicherheits Rückruf für jeden RPC-Aufruf für eine bestimmte Schnittstelle.<br/>
<blockquote>
[!Note]<br />
Dieses Flag ist ab Windows XP mit SP2 und Windows Server 2003 mit SP1 verfügbar.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Rpcdce. h</dt> </dl> |



 

 





