---
title: DCOMSCMRemoteCallFlags
description: Steuert das Verhalten von Aufrufen vom lokalen DCOM-Dienststeuerungs-Manager (DCOMSCM) an einen Remote-DCOMSCM.
ms.assetid: fb306da7-4b9a-4386-8525-7f78bd6bf728
keywords:
- DCOMSCMRemoteCallFlags-Registrierungswert COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81d658b80d347e684aa42aebad936a863b9bca2138b3118508849a730e11878d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119678830"
---
# <a name="dcomscmremotecallflags"></a>DCOMSCMRemoteCallFlags

Steuert das Verhalten von Aufrufen vom lokalen DCOM-Dienststeuerungs-Manager (DCOMSCM) an einen Remote-DCOMSCM.

## <a name="registry-entry"></a>Registrierungseintrag

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   DCOMSCMRemoteCallFlags = value
```

## <a name="remarks"></a>Hinweise

Dies ist ein **\_ REG-DWORD-Wert.**



| Wert | BESCHREIBUNG                                       |
|-------|---------------------------------------------------|
| 0x1   | **DCOMSCM \_ ACTIVATION \_ USE \_ ALL \_ AUTHNSERVICES**  |
| 0x2   | **DCOMSCM \_ ACTIVATION \_ DISALLOW \_ UNSECURE \_ CALL** |
| 0x4   | **DCOMSCM \_ RESOLVE \_ USE \_ ALL \_ AUTHNSERVICES**     |
| 0x8   | **DCOMSCM \_ RESOLVE \_ DISALLOW \_ UNSECURE \_ CALL**    |
| 0x10  | **\_DCOMSCM-PING \_ VERWENDEN MID \_ \_ AUTHNSERVICE**         |



 

## <a name="dcomscm_activation_use_all_authnservices-description"></a>DCOMSCM \_ ACTIVATION \_ USE \_ ALL \_ AUTHNSERVICES Description

Wenn der Client eine Aktivierungsanforderung aus gibt, die die Standardsicherheitseinstellungen verwendet, verwendet der lokale DCOMSCM den Negotiate-Authentifizierungsdienst, wenn der AKTIVIERUNGS-RPC-Aufruf an den Remote-DCOMSCM ausgeführt wird. Wenn der Aufruf fehlschlägt, wird der RPC-Aktivierungsaufruf vom lokalen DCOMSCM ohne Sicherheit ausgeführt.

**Windows Server 2003 und Windows XP/2000:** Wenn der RPC-Aktivierungsaufruf, der den Negotiate-Authentifizierungsdienst verwendet, fehlschlägt, wird der RPC-Aktivierungsaufruf vom lokalen DCOMSCM mit Kerberos, NTLM oder anderen konfigurierten Sicherheitsanbietern ausgeführt. Wenn keine Sicherheitsanbieter funktionieren, wird der RPC-Aktivierungsaufruf vom lokalen DCOMSCM ohne Sicherheit ausgeführt.

Durch Festlegen dieses Flags kann das lokale DCOMSCM auf Windows Vista oder höher so gemacht werden, dass es sich wie Systeme vor Vista verhält. Es wird nicht empfohlen, dieses Flag zu setzen, es sei denn, dies ist aus Kompatibilitätsgründen erforderlich.

## <a name="dcomscm_activation_disallow_unsecure_call-description"></a>DCOMSCM \_ ACTIVATION \_ DISALLOW \_ UNSECURE \_ CALL Description

Wenn das **Flag DCOMSCM \_ ACTIVATION \_ DISALLOW \_ UNSECURE \_ CALL** festgelegt ist, führt der lokale DCOMSCM keinen unsicheren RPC-Aktivierungsaufruf aus. Damit Clients Aktivierungsanforderungen mit nicht standardmäßigen Sicherheitseinstellungen vornehmen können, geben Sie beim Senden der Aktivierungsanforderung die [**COAUTHINFO-Struktur**](/windows/desktop/api/wtypesbase/ns-wtypesbase-coauthinfo) an. In diesem Fall werden die **Flags DCOMSCM \_ ACTIVATION USE ALL \_ \_ \_ AUTHNSERVICES** und **DCOMSCM \_ ACTIVATION \_ DISALLOW \_ UNSECURE \_ CALL** ignoriert.

Es wird nicht empfohlen, dieses Flag zu setzen, es sei denn, alle Clients und Server im Netzwerk sind vollständig authentifiziert.

## <a name="dcomscm_resolve_use_all_authnservices-description"></a>DCOMSCM \_ RESOLVE \_ USE \_ ALL \_ AUTHNSERVICES Description

Wenn der Client einen Objektverweis entmarshalsiert, verwendet der lokale DCOMSCM den Negotiate-Authentifizierungsdienst, wenn der RPC-Aufruf der AUTH-Auflösung an den Remote-DCOMSCM ausgeführt wird. Wenn der Aufruf fehlschlägt, stellt der lokale DCOMSCM den RPC-Aufruf der RPC-Auflösung ohne Sicherheit bereit.

**Windows Server 2003 und Windows XP/2000:** Wenn der RPC-Aufruf der AUTH-Auflösung mithilfe des Negotiate-Authentifizierungsdiensts fehlschlägt, wird der RPC-Aufruf durch den lokalen DCOMSCM mit Kerberos, NTLM oder anderen konfigurierten Sicherheitsanbietern vom lokalen DCOMSCM ausgeführt. Wenn keine Sicherheitsanbieter funktionieren, verwendet der lokale DCOMSCM den RPC-Aufruf der RPC-Auflösung ohne Sicherheit.

Durch Festlegen dieses Flags kann das lokale DCOMSCM auf Windows Vista oder höher so gemacht werden, dass es sich wie Systeme vor Vista verhält. Es wird nicht empfohlen, dieses Flag zu setzen, es sei denn, dies ist aus Kompatibilitätsgründen erforderlich.

## <a name="dcomscm_resolve_disallow_unsecure_call-description"></a>DCOMSCM \_ RESOLVE \_ DISALLOW \_ UNSECURE \_ CALL Description

Wenn das **Flag DCOMSCM \_ RESOLVE \_ DISALLOW \_ UNSECURE \_ CALL** festgelegt ist, führt der lokale DCOMSCM keinen unsicheren RPC-Aufruf der RPC-Auflösung durch. Darüber hinaus führt der lokale DCOMSCM keinen unsicheren Ping-RPC-Aufruf der Garbage Collection aus. Es wird nicht empfohlen, dieses Flag zu setzen, es sei denn, alle Clients und Server im Netzwerk sind vollständig authentifiziert.

## <a name="dcomscm_ping_use_mid_authnservice-description"></a>DCOMSCM \_ PING \_ USE \_ MID \_ AUTHNSERVICE Description

Der lokale DCOMSCM verwendet den Negotiate-Authentifizierungsdienst, wenn der Ping-RPC-Aufruf der Garbage Collection an den Remote-DCOMSCM ausgeführt wird. Wenn der Aufruf fehlschlägt, wird der Ping-RPC-Aufruf der Garbage Collection vom lokalen DCOMSCM ohne Sicherheit ausgeführt.

**Windows Server 2003 und Windows XP/2000:** Wenn beim Ping-RPC-Aufruf der Garbage Collection mithilfe des Negotiate-Authentifizierungsdiensts ein Fehler auftritt, wird der GARBAGE COLLECTION-Ping-RPC-Aufruf vom lokalen DCOMSCM mit Kerberos, NTLM und anderen konfigurierten Sicherheitsanbietern durchgeführt. Wenn keine Sicherheitsanbieter funktionieren, wird der Ping-RPC-Aufruf der Garbage Collection vom lokalen DCOMSCM ohne Sicherheit ausgeführt.

Durch Festlegen dieses Flags kann das lokale DCOMSCM auf Windows Vista oder höher so gemacht werden, dass es sich wie Systeme vor Vista verhält. Es wird nicht empfohlen, das **Flag DCOMSCM \_ PING \_ USE MID \_ \_ AUTHNSERVICE** solange nicht aus Kompatibilitätsgründen festgelegt zu werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Authentifizierung für Remoteverbindungen](/windows/desktop/WinRM/authentication-for-remote-connections)
</dt> <dt>

[EnableDCOM](enabledcom.md)
</dt> <dt>

[Registrieren von COM-Servern](registering-com-servers.md)
</dt> <dt>

[Sicherheit in COM](security-in-com.md)
</dt> </dl>

 

 