---
title: Sitzungs Konstanten
description: Die Sitzungs Konstanten in der \_ \_ wsmansessionflags-Enumeration geben die Authentifizierung und andere Informationen für die Aufrufe WSMAN. anatesession oder iwsman-Befehle an, die eine Verbindung mit einem Remote Computer herstellen.
ms.assetid: 5df52696-ac2c-42b7-8b0f-99a27b58575b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8417289a218203dbdaee288ff03096d894f4bd4d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106338160"
---
# <a name="session-constants"></a>Sitzungs Konstanten

Die Sitzungs Konstanten in der **\_ \_ wsmansessionflags** -Enumeration geben die Authentifizierung und andere Informationen für die Aufrufe [**WSMAN. foratesession**](wsman-createsession.md) oder [**iwsman:: foratesession**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsman-createsession) an, die eine Verbindung mit einem Remote Computer herstellen. Diese Konstanten sind auch eng mit den **WinRM** -Befehlszeilen Tool-Switches verknüpft.

## <a name="using-session-constants"></a>Verwenden von Sitzungs Konstanten

Sie können die Sitzungsflags für den Aufrufen von [**WSMAN. kreatesession**](wsman-createsession.md) auf zwei verschiedene Arten festlegen. Eine ist kürzer und einfacher. Die längere Methode, wie im folgenden Beispiel gezeigt, besteht darin, den Wert des Flags zu suchen, das Sie verwenden möchten, und eine Konstante in Ihrem Skript mit diesem Wert zu erstellen. Anschließend wird die Konstante verwendet, um den Wert des *IFlags* -Parameters festzulegen.

``` syntax
Const SessionFlagUseNegotiate = 131072
Const SessionFlagCredUserNamePassword = 4096
iFlags = SessionFlagUseNegotiate Or SessionFlagCredUserNamePassword
```

Die empfohlene Vorgehensweise, wie im folgenden Beispiel gezeigt, ist die Verwendung der [**WSMAN**](wsman.md) -Objektmethode, die mit dem-Flag verknüpft ist.

``` syntax
iFlags = Wsman.SessionFlagUseNegotiate Or Wsman.SessionFlagCredUserNamePassword
```

<dl> <dt>

<span id="Authentication_Constants"></span><span id="authentication_constants"></span><span id="AUTHENTICATION_CONSTANTS"></span>[**Authentifizierungs Konstanten**](authentication-constants.md)
</dt> <dd>

Geben Sie die Authentifizierungsmethode und die Vorgehensweise zum Behandeln von Zertifikat Servern an.

</dd> <dt>

<span id="Other_Session_Constants"></span><span id="other_session_constants"></span><span id="OTHER_SESSION_CONSTANTS"></span>[**Andere Sitzungs Konstanten**](other-session-constants.md)
</dt> <dd>

Geben Sie den Port für Codierung, Verschlüsselung und Dienst Prinzipal Name an.

</dd> </dl>

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[WinRM-Konstanten und-Enumerationen](winrm-constants-and-enumerations.md)
</dt> <dt>

[**WSMAN. kreatesession**](wsman-createsession.md)
</dt> <dt>

[Authentifizierung für Remote Verbindungen](authentication-for-remote-connections.md)
</dt> </dl>

 

 




