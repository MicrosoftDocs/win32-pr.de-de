---
title: Sitzungskonstanten
description: Die Sitzungskonstanten in der \_ \_ WSManSessionFlags-Enumeration geben die Authentifizierung und andere Informationen für WSMan.CreateSession- oder IWSMan CreateSession-Aufrufe an, die eine Verbindung mit einem Remotecomputer herstellen.
ms.assetid: 5df52696-ac2c-42b7-8b0f-99a27b58575b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 584eb15c4b235a006b52551de8f9999ddb65459412af68db81f0500a0828888b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117743226"
---
# <a name="session-constants"></a>Sitzungskonstanten

Die Sitzungskonstanten in der **\_ \_ WSManSessionFlags-Enumeration** geben die Authentifizierung und andere Informationen für [**WSMan.CreateSession-**](wsman-createsession.md) oder [**IWSMan::CreateSession-Aufrufe**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsman-createsession) an, die eine Verbindung mit einem Remotecomputer herstellen. Diese Konstanten sind auch  eng mit Winrm-Befehlszeilentoolschaltern verknüpft.

## <a name="using-session-constants"></a>Verwenden von Sitzungskonstanten

Sie können die Sitzungsflags für den Aufruf von [**WSMan.CreateSession**](wsman-createsession.md) auf zwei verschiedene Arten festlegen. Eine ist kürzer und einfacher. Der längere Weg, wie im folgenden Beispiel gezeigt, besteht darin, den Wert des Flags zu suchen, das Sie verwenden möchten, und eine Konstante in Ihrem Skript mit diesem Wert zu erstellen. Anschließend wird die Konstante verwendet, um den Wert des *iFlags-Parameters* festzulegen.

``` syntax
Const SessionFlagUseNegotiate = 131072
Const SessionFlagCredUserNamePassword = 4096
iFlags = SessionFlagUseNegotiate Or SessionFlagCredUserNamePassword
```

Die empfohlene Methode, wie im folgenden Beispiel gezeigt, ist die Verwendung der [**WSMan-Objektmethode,**](wsman.md) die dem Flag zugeordnet ist.

``` syntax
iFlags = Wsman.SessionFlagUseNegotiate Or Wsman.SessionFlagCredUserNamePassword
```

<dl> <dt>

<span id="Authentication_Constants"></span><span id="authentication_constants"></span><span id="AUTHENTICATION_CONSTANTS"></span>[**Authentifizierungskonstanten**](authentication-constants.md)
</dt> <dd>

Geben Sie die Authentifizierungsmethode und die Behandlung von Zertifikatservern an.

</dd> <dt>

<span id="Other_Session_Constants"></span><span id="other_session_constants"></span><span id="OTHER_SESSION_CONSTANTS"></span>[**Andere Sitzungskonstanten**](other-session-constants.md)
</dt> <dd>

Geben Sie den Port für Codierung, Verschlüsselung und Dienstprinzipalnamen an.

</dd> </dl>

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[WinRM-Konstanten und -Enumerationen](winrm-constants-and-enumerations.md)
</dt> <dt>

[**WSMan.CreateSession**](wsman-createsession.md)
</dt> <dt>

[Authentifizierung für Remoteverbindungen](authentication-for-remote-connections.md)
</dt> </dl>

 

 




