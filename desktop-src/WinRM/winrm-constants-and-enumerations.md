---
title: WinRM-Konstanten und -Enumerationen
description: Windows Die Remoteverwaltung verfügt über Bitflags, die zum Erstellen von Sitzungen und Enumerationen sowie für Zugriffstypen und die Authentifizierung bei einem Proxyserver verwendet werden.
ms.assetid: 17e59245-26a3-4383-a741-4a09f3cfcec6
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73de8f418d5b0fb0bd7adebb8439ccbce67f0bcb6aacf72ed2665683c00e0076
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117742936"
---
# <a name="winrm-constants-and-enumerations"></a>WinRM-Konstanten und -Enumerationen

Windows Die Remoteverwaltung verfügt über Bitflags, die zum Erstellen von Sitzungen und Enumerationen sowie für Zugriffstypen und die Authentifizierung bei einem Proxyserver verwendet werden. In der folgenden Liste sind die verschiedenen Bitflags aufgeführt.

<dl> <dt>

<span id="Session_Constants"></span><span id="session_constants"></span><span id="SESSION_CONSTANTS"></span>[Sitzungskonstanten](session-constants.md)
</dt> <dd>

Flags, die im *flags-Parameter* der [**Methoden WSMan.CreateSession**](wsman-createsession.md) oder [**IWSMan::CreateSession**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsman-createsession) verwendet werden.

</dd> <dt>

<span id="Enumeration_Constants"></span><span id="enumeration_constants"></span><span id="ENUMERATION_CONSTANTS"></span>[**Enumerationskonstanten**](enumeration-constants.md)
</dt> <dd>

Flags, die im *flags-Parameter* des Aufrufs von [**Session.Enumerate**](session-enumerate.md) oder [**IWSManSession::Enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate)verwendet werden.

</dd> <dt>

<span id="WSManProxyAuthenticationFlags"></span><span id="wsmanproxyauthenticationflags"></span><span id="WSMANPROXYAUTHENTICATIONFLAGS"></span>[**WSManProxyAuthenticationFlags**](/windows/desktop/api/WSManDisp/ne-wsmandisp-wsmanproxyauthenticationflags)
</dt> <dd>

Flags, die im *authenticationMenowism-Parameter* des Aufrufs von [**IWSManConnectionOptionsEx2::SetProxy**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanconnectionoptionsex2-setproxy)verwendet werden.

</dd> <dt>

<span id="WSManProxyAccessTypeFlags"></span><span id="wsmanproxyaccesstypeflags"></span><span id="WSMANPROXYACCESSTYPEFLAGS"></span>[**WSManProxyAccessTypeFlags**](/windows/desktop/api/WSManDisp/ne-wsmandisp-wsmanproxyaccesstypeflags)
</dt> <dd>

Flags, die im *accessType-Parameter* des Aufrufs von [**IWSManConnectionOptionsEx2::SetProxy**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanconnectionoptionsex2-setproxy)verwendet werden.

</dd> </dl>

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Windows Referenz zur Remoteverwaltung](windows-remote-management-reference.md)
</dt> <dt>

[**WSMan.CreateSession**](wsman-createsession.md)
</dt> <dt>

[**IWSMan::CreateSession**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsman-createsession)
</dt> <dt>

[**IWSManConnectionOptionsEx2::SetProxy**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanconnectionoptionsex2-setproxy)
</dt> </dl>

 

 




