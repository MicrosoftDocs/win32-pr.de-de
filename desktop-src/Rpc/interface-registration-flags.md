---
title: Schnittstellenregistrierungsflags (Rpcdce.h)
description: Die folgenden Konstanten werden im Flags-Parameter der RpcServerRegisterIf2- und RpcServerRegisterIfEx-Funktionen verwendet.
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
ms.openlocfilehash: f33111bc7dc1acdf5ec12ba81b91b9ec37d7b9994c1af3821c0997562f49e81a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118928896"
---
# <a name="interface-registration-flags"></a>Schnittstellenregistrierungsflags

Die folgenden Konstanten werden im *Flags-Parameter* der [**RpcServerRegisterIf2-**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2) und [**RpcServerRegisterIfEx-Funktionen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex) verwendet.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Konstante</th>
<th style="text-align: left;">Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="0"></span><dl> <dt><strong>0</strong></dt> </dl></td>
<td style="text-align: left;">Standardschnittstellensemantik.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="RPC_IF_ALLOW_CALLBACKS_WITH_NO_AUTH"></span><span id="rpc_if_allow_callbacks_with_no_auth"></span><dl> <dt><strong>RPC_IF_ALLOW_CALLBACKS_WITH_NO_AUTH</strong></dt> </dl></td>
<td style="text-align: left;">Wenn dieses Schnittstellenflag registriert ist, ruft die RPC-Laufzeit den registrierten Sicherheitsrückruf für alle Aufrufe auf, unabhängig von der Identität, Protokollsequenz oder Authentifizierungsebene des Clients.<br/>
<blockquote>
[!Note]<br />
Dieses Flag ist ab Windows XP mit SP2 und Windows Server 2003 mit SP1 verfügbar. Wenn dieses Flag nicht festgelegt ist, filtert RPC automatisch alle nicht authentifizierten Aufrufe, bevor sie den Sicherheitsrückruf erreichen.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="RPC_IF_ALLOW_LOCAL_ONLY"></span><span id="rpc_if_allow_local_only"></span><dl> <dt><strong>RPC_IF_ALLOW_LOCAL_ONLY</strong></dt> </dl></td>
<td style="text-align: left;">Wenn dieses Schnittstellenflag registriert ist, lehnt die RPC-Laufzeit Aufrufe von Remoteclients ab. Alle lokalen Aufrufe, die ncadg_* und ncacn_*-Protokollsequenzen verwenden, werden ebenfalls abgelehnt, mit Ausnahme ncacn_np. RPC lässt ncacn_NP Aufrufe nur zu, wenn der Aufruf nicht von SRV kommt. Aufrufe von ncalrpc werden immer verarbeitet.<br/>
<blockquote>
[!Note]<br />
Dieses Flag ist ab Windows XP mit SP2 und Windows Server 2003 mit SP1 verfügbar.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="RPC_IF_AUTOLISTEN"></span><span id="rpc_if_autolisten"></span><dl> <dt><strong>RPC_IF_AUTOLISTEN</strong></dt> </dl></td>
<td style="text-align: left;">Dies ist <strong>eine Schnittstelle für automatisches Lauschen.</strong> Die Laufzeit beginnt mit dem Lauschen auf Aufrufe, sobald die erste Autolisten-Schnittstelle registriert ist, und beendet das Lauschen, wenn die Registrierung der letzten Autolisten-Schnittstelle aufgehoben wird.<br/></td>
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
<td style="text-align: left;">Beschränkt Verbindungen auf Clients, die eine Autorisierungsebene verwenden, die höher als RPC_C_AUTHN_LEVEL_NONE. Wenn Sie dieses Flag angeben, können Clients in der <strong>NULL-Sitzung durchkommen.</strong> Auf Windows XP und Windows Server 2003 sind solche Clients nicht zulässig. Clients, bei denen der RPC_IF_ALLOW_SECURE_ONLY fehlschlägt, erhalten einen RPC_S_ACCESS_DENIED Fehler. Die Verwendung RPC_IF_ALLOW_SECURE_ONLY Flags impliziert oder garantiert keine hohe Berechtigungsstufe des aufrufenden Benutzers. RPC überprüft nur, ob der Benutzer über gültige Anmeldeinformationen verfügt. Der aufrufende Benutzer verwendet möglicherweise das Gastkonto oder andere Konten mit geringen Berechtigungen. Gehen Sie nicht von hohen Rechten aus, wenn RPC_IF_ALLOW_SECURE_ONLY verwendet wird.<br/> <strong>Windows NT 4.0 und Windows Me/98/95:</strong><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="RPC_IF_SEC_NO_CACHE"></span><span id="rpc_if_sec_no_cache"></span><dl> <dt><strong>RPC_IF_SEC_NO_CACHE</strong></dt> </dl></td>
<td style="text-align: left;">Deaktiviert das Zwischenspeichern von Sicherheitsrückrufen und erzwingt einen Sicherheitsrückruf für jeden RPC-Aufruf auf einer bestimmten Schnittstelle.<br/>
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
| Header<br/>                   | <dl> <dt>Rpcdce.h</dt> </dl> |



 

 





