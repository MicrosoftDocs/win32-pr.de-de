---
title: Dcomscmremotecallflags
description: Steuert das Verhalten von Aufrufen vom lokalen DCOM-Dienststeuerungs-Manager (dcomscm) zu einem Remote-dcomscm.
ms.assetid: fb306da7-4b9a-4386-8525-7f78bd6bf728
keywords:
- Dcomscmremotecallflags-Registrierungs Wert com
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fda58975e40ac6ac1633db8aa78f2c7636f9103
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104039662"
---
# <a name="dcomscmremotecallflags"></a>Dcomscmremotecallflags

Steuert das Verhalten von Aufrufen vom lokalen DCOM-Dienststeuerungs-Manager (dcomscm) zu einem Remote-dcomscm.

## <a name="registry-entry"></a>Registrierungseintrag

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   DCOMSCMRemoteCallFlags = value
```

## <a name="remarks"></a>Bemerkungen

Dies ist ein **reg \_ DWORD** -Wert.



| Wert | BESCHREIBUNG                                       |
|-------|---------------------------------------------------|
| 0x1   | **dcomscm \_ - \_ Aktivierung \_ alle \_ authnservices verwenden**  |
| 0x2   | **nicht sicheren Rückruf durch dcomscm- \_ Aktivierung \_ \_ nicht zulassen \_** |
| 0x4   | **dcomscm \_ Auflösen der \_ Verwendung \_ aller \_ authnservices**     |
| 0x8   | **dcomscm \_ Auflösen \_ \_ unsichere Aufrufe nicht zulassen \_**    |
| 0x10  | **dcomscm- \_ ping \_ verwendet \_ Mid \_ authnservice.**         |



 

## <a name="dcomscm_activation_use_all_authnservices-description"></a>Dcomscm \_ - \_ Aktivierung \_ alle \_ authnservices-Beschreibungen verwenden

Wenn der Client eine Aktivierungs Anforderung ausgibt, bei der die Standard Sicherheitseinstellungen verwendet werden, verwendet der lokale dcomscm den Aushandlungs Authentifizierungsdienst, wenn der Remote-dcomscm aufgerufen wird. Wenn der Aufruf fehlschlägt, führt der lokale dcomscm den RPC-Aktivierungs Aufruf ohne Sicherheit aus.

**Windows Server 2003 und Windows XP/2000:** Wenn der RPC-Aktivierungs Aufruf, der den Aushandlungs Authentifizierungsdienst verwendet, fehlschlägt, führt der lokale dcomscm den RPC-Aktivierungs Aufruf mithilfe von Kerberos, NTLM oder anderen konfigurierten Sicherheitsanbietern aus. Wenn keine Sicherheitsanbieter funktionieren, stellt der lokale dcomscm den RPC-Aktivierungs Aufruf ohne Sicherheit dar.

Wenn Sie dieses Flag festlegen, kann der lokale dcomscm unter Windows Vista oder höher so gestaltet werden, dass es sich wie vor Vista-Systemen verhält. Es wird nicht empfohlen, dieses Flag festzulegen, sofern dies aus Kompatibilitätsgründen nicht erforderlich ist.

## <a name="dcomscm_activation_disallow_unsecure_call-description"></a>Dcomscm- \_ Aktivierung \_ \_ unsichere \_ aufrufsbeschreibung nicht zulassen

Wenn die **dcomscm- \_ Aktivierung \_ \_ unsicheres \_ Aufruf** Flag nicht zulassen festgelegt ist, führt der lokale dcomscm keinen nicht sicheren Aktivierungs-RPC-Aufruf aus. Wenn Sie zulassen möchten, dass Clients Aktivierungs Anforderungen mit nicht standardmäßigen Sicherheitseinstellungen herstellen, geben Sie die [**coauthinfo**](/windows/desktop/api/wtypesbase/ns-wtypesbase-coauthinfo) -Struktur beim Ausführen der Aktivierungs Anforderung an. In diesem Fall werden bei der **dcomscm- \_ Aktivierung \_ \_ alle \_ authnservices verwendet** , und die **dcomscm-Aktivierung verhindert, \_ \_ dass \_ unsichere \_ callflags** ignoriert werden.

Es wird nicht empfohlen, dieses Flag festzulegen, es sei denn, alle Clients und Server im Netzwerk sind vollständig authentifiziert.

## <a name="dcomscm_resolve_use_all_authnservices-description"></a>Dcomscm \_ - \_ Beschreibung "use \_ All \_ authnservices" auflösen

Wenn der Client einen Objekt Verweis aufnimmt, verwendet der lokale dcomscm den Aushandlungs Authentifizierungsdienst, wenn der RPC-Auflösungs-RPC-Aufruf an den Remote-dcomscm erfolgt. Wenn der Aufruf fehlschlägt, führt der lokale dcomscm den RPC-Aufruf der oxid Auflösung ohne Sicherheit aus.

**Windows Server 2003 und Windows XP/2000:** Wenn bei der RPC-Auflösung ein RPC-Aufruf mit dem Aushandlungs Authentifizierungsdienst fehlschlägt, führt der lokale dcomscm den RPC-Aufruf der oxid Auflösung mithilfe von Kerberos, NTLM oder anderen konfigurierten Sicherheitsanbietern aus. Wenn keine Sicherheitsanbieter funktionieren, führt der lokale dcomscm den RPC-Aufruf der oxid Auflösung ohne Sicherheit aus.

Wenn Sie dieses Flag festlegen, kann der lokale dcomscm unter Windows Vista oder höher so gestaltet werden, dass es sich wie vor Vista-Systemen verhält. Es wird nicht empfohlen, dieses Flag festzulegen, sofern dies aus Kompatibilitätsgründen nicht erforderlich ist.

## <a name="dcomscm_resolve_disallow_unsecure_call-description"></a>Dcomscm \_ Auflösen \_ \_ unsichere \_ aufrufsbeschreibung nicht zulassen

Wenn das Flag zum **\_ Auflösen von \_ \_ unsicherem \_ Aufruf durch dcomscm auflösen nicht zulassen** festgelegt ist, führt der lokale dcomscm keinen nicht sicheren RPC-Auflösungs Aufruf aus. Außerdem führt der lokale dcomscm keinen unsicheren Garbage Collection Ping-RPC-Aufruf aus. Es wird nicht empfohlen, dieses Flag festzulegen, es sei denn, alle Clients und Server im Netzwerk sind vollständig authentifiziert.

## <a name="dcomscm_ping_use_mid_authnservice-description"></a>Dcomscm \_ ping \_ use \_ Mid \_ authnservice Description

Der lokale dcomscm verwendet den Aushandlungs Authentifizierungsdienst, wenn der RPC-Aufruf der Garbage Collection an den Remote-dcomscm gesendet wird. Wenn der Aufruf fehlschlägt, führt der lokale dcomscm den RPC-Aufruf der Garbage Collection per Ping ohne Sicherheit aus.

**Windows Server 2003 und Windows XP/2000:** Wenn das Ping-RPC-Aufruf der Garbage Collection mithilfe des Aushandlungs Authentifizierungs Diensts fehlschlägt, führt der lokale dcomscm den Garbage Collection Ping-RPC-Aufruf mithilfe von Kerberos, NTLM und anderen konfigurierten Sicherheitsanbietern aus. Wenn keine Sicherheitsanbieter funktionieren, führt der lokale dcomscm den Garbage Collection Ping-RPC-Aufruf mithilfe von No Security aus.

Wenn Sie dieses Flag festlegen, kann der lokale dcomscm unter Windows Vista oder höher so gestaltet werden, dass es sich wie vor Vista-Systemen verhält. Es wird nicht empfohlen, das Flag " **dcomscm \_ ping \_ use \_ Mid \_ authnservice** " festzulegen, sofern dies aus Kompatibilitätsgründen nicht erforderlich ist.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Authentifizierung für Remote Verbindungen](/windows/desktop/WinRM/authentication-for-remote-connections)
</dt> <dt>

[EnableDCOM](enabledcom.md)
</dt> <dt>

[Registrieren von com-Servern](registering-com-servers.md)
</dt> <dt>

[Sicherheit in com](security-in-com.md)
</dt> </dl>

 

 