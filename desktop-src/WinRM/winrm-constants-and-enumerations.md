---
title: WinRM-Konstanten und-Enumerationen
description: Windows-Remoteverwaltung verfügt über Bitflags, die zum Erstellen von Sitzungen und Enumerationen sowie für Zugriffs Typen und die Authentifizierung auf einem Proxy Server verwendet werden.
ms.assetid: 17e59245-26a3-4383-a741-4a09f3cfcec6
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0789d440ff0f88cc037e0dc9e544ca559c1af5b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037265"
---
# <a name="winrm-constants-and-enumerations"></a>WinRM-Konstanten und-Enumerationen

Windows-Remoteverwaltung verfügt über Bitflags, die zum Erstellen von Sitzungen und Enumerationen sowie für Zugriffs Typen und die Authentifizierung auf einem Proxy Server verwendet werden. In der folgenden Liste sind die verschiedenen Bitflags aufgeführt.

<dl> <dt>

<span id="Session_Constants"></span><span id="session_constants"></span><span id="SESSION_CONSTANTS"></span>[Sitzungs Konstanten](session-constants.md)
</dt> <dd>

Flags, die im *Flags* -Parameter der [**WSMAN. kreatesession**](wsman-createsession.md) -Methode oder der [**iwsman:: | atesession**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsman-createsession) -Methode verwendet werden.

</dd> <dt>

<span id="Enumeration_Constants"></span><span id="enumeration_constants"></span><span id="ENUMERATION_CONSTANTS"></span>[**Enumerationskonstanten**](enumeration-constants.md)
</dt> <dd>

Flags, die im *Flags* -Parameter des Aufrufes [**Session. Enumerate**](session-enumerate.md) oder [**iwsmansession:: Enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate)verwendet werden.

</dd> <dt>

<span id="WSManProxyAuthenticationFlags"></span><span id="wsmanproxyauthenticationflags"></span><span id="WSMANPROXYAUTHENTICATIONFLAGS"></span>[**Wsmanproxyauthenticationflags**](/windows/desktop/api/WSManDisp/ne-wsmandisp-wsmanproxyauthenticationflags)
</dt> <dd>

Flags, die im *authenticationmechanism* -Parameter des Aufrufes [**IWSManConnectionOptionsEx2:: SetProxy**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanconnectionoptionsex2-setproxy)verwendet werden.

</dd> <dt>

<span id="WSManProxyAccessTypeFlags"></span><span id="wsmanproxyaccesstypeflags"></span><span id="WSMANPROXYACCESSTYPEFLAGS"></span>[**Wsmanproxyaccesstypflags**](/windows/desktop/api/WSManDisp/ne-wsmandisp-wsmanproxyaccesstypeflags)
</dt> <dd>

Flags, die im *accessType* -Parameter des Aufrufes [**IWSManConnectionOptionsEx2:: SetProxy**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanconnectionoptionsex2-setproxy)verwendet werden.

</dd> </dl>

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Windows-Remoteverwaltung Referenz](windows-remote-management-reference.md)
</dt> <dt>

[**WSMAN. kreatesession**](wsman-createsession.md)
</dt> <dt>

[**Iwsman:: kreatesession**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsman-createsession)
</dt> <dt>

[**IWSManConnectionOptionsEx2:: SetProxy**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanconnectionoptionsex2-setproxy)
</dt> </dl>

 

 




