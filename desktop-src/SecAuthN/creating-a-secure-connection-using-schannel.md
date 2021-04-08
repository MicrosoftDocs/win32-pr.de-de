---
description: Erstellen einer sicheren Verbindung mithilfe von SChannel
ms.assetid: 94eb15c3-225b-4b6f-b29c-41e5d356a847
title: Erstellen einer sicheren Verbindung mithilfe von SChannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 335713a400804bc84fffa078496c53c9178e389b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757291"
---
# <a name="creating-a-secure-connection-using-schannel"></a>Erstellen einer sicheren Verbindung mithilfe von SChannel

Das SChannel- [*Sicherheitspaket*](/windows/desktop/SecGloss/s-gly) ermöglicht den Zugriff auf vier [*Sicherheitsprotokolle*](/windows/desktop/SecGloss/s-gly):

-   [Transport Layer Security (TLS 1,2)](transport-layer-security-protocol.md)
-   [Transport Layer Security (TLS 1,1)](transport-layer-security-protocol.md)
-   [Transport Layer Security (TLS 1,0)](transport-layer-security-protocol.md)
-   [Secure Sockets Layer (SSL 3,0)](secure-sockets-layer-protocol.md)
-   [Secure Sockets Layer (SSL 2,0)](secure-sockets-layer-protocol.md)

> [!Note]  
> Die PCT-und SSL 2,0-Protokolle wurden durch das TLS-Protokoll ersetzt und sollten nicht für die neue Entwicklung verwendet werden.

 

**So richten Sie eine sichere Verbindung zwischen einem Client und einem Server ein**

1.  Anfordern von SChannel-Anmelde Informationen (Abrufen von[SChannel-Anmelde](obtaining-schannel-credentials.md)Informationen)
2.  Erstellen eines SChannel-Sicherheits Kontexts ([Erstellen eines SChannel-Sicherheits Kontexts](creating-an-schannel-security-context.md)).

Nachdem eine Verbindung hergestellt wurde, können Sie Informationen zu ihren Attributen abrufen. Weitere Informationen finden Sie unter [Informationen zu SChannel-Verbindungen](getting-information-about-schannel-connections.md).

Wenn Sie nach dem Herstellen einer Verbindung die Sicherheitsanforderungen Ihrer Anwendung ändern oder die Verbindung verloren geht, können Sie die Verbindung erneut aushandeln. Weitere Informationen finden Sie unter [Aushandeln einer SChannel-Verbindung](renegotiating-an-schannel-connection.md).

Wenn Sie mit der Verwendung einer SChannel-Verbindung fertig sind, müssen Sie die erforderliche Bereinigung ausführen. Weitere Informationen finden Sie unter Herunterfahren [einer SChannel-Verbindung](shutting-down-an-schannel-connection.md).

Informationen zu den mit dem Platform Software Development Kit (SDK) gelieferten Beispielen, die das SChannel- [*Sicherheitspaket*](/windows/desktop/SecGloss/s-gly)veranschaulichen, finden Sie in den PSDK-Beispielen mithilfe von Schannel.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Angeben von SChannel-Chiffren und Verschlüsselungs stärken](specifying-schannel-ciphers-and-cipher-strengths.md)
</dt> </dl>

 

 
