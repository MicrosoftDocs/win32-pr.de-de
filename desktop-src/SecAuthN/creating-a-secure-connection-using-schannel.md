---
description: Erstellen einer sicheren Verbindung mit Schannel
ms.assetid: 94eb15c3-225b-4b6f-b29c-41e5d356a847
title: Erstellen einer sicheren Verbindung mit Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 374955b67bfa0026da5e8f8e9e88ce71da24231e218cb869cb532d05d4171bbf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008908"
---
# <a name="creating-a-secure-connection-using-schannel"></a>Erstellen einer sicheren Verbindung mit Schannel

Das Schannel-Sicherheitspaket [*bietet*](/windows/desktop/SecGloss/s-gly) Zugriff auf vier [*Sicherheitsprotokolle:*](/windows/desktop/SecGloss/s-gly)

-   [Transport Layer Security (TLS 1.2)](transport-layer-security-protocol.md)
-   [Transport Layer Security (TLS 1.1)](transport-layer-security-protocol.md)
-   [Transport Layer Security (TLS 1.0)](transport-layer-security-protocol.md)
-   [Secure Sockets Layer (SSL 3.0)](secure-sockets-layer-protocol.md)
-   [Secure Sockets Layer (SSL 2.0)](secure-sockets-layer-protocol.md)

> [!Note]  
> Die Protokolle PCT und SSL 2.0 wurden durch das TLS-Protokoll ersetzt und sollten nicht für neue Entwicklungen verwendet werden.

 

**So richten Sie eine sichere Verbindung zwischen einem Client und einem Server ein**

1.  Abrufen von Schannel-Anmeldeinformationen ([Abrufen von Schannel-Anmeldeinformationen](obtaining-schannel-credentials.md)).
2.  Erstellen eines Schannel-Sicherheitskontexts ([Erstellen eines Schannel-Sicherheitskontexts](creating-an-schannel-security-context.md)).

Nachdem eine Verbindung hergestellt wurde, können Sie Informationen zu ihren Attributen abrufen. Weitere Informationen finden Sie unter Getting Information About Schannel Connections (Abrufen von Informationen [zu Schannel-Verbindungen).](getting-information-about-schannel-connections.md)

Wenn sich nach dem Herstellen einer Verbindung die Sicherheitsanforderungen Ihrer Anwendung ändern oder die Verbindung verloren geht, können Sie die Verbindung erneut aushandeln. Weitere Informationen finden Sie unter [Neuverhandlung einer Schannel-Verbindung.](renegotiating-an-schannel-connection.md)

Wenn Sie die Verwendung einer Schannel-Verbindung abgeschlossen haben, müssen Sie die erforderliche Bereinigung durchführen. Weitere Informationen finden Sie unter [Herunterfahren einer Schannel-Verbindung.](shutting-down-an-schannel-connection.md)

Informationen zu Beispielen, die im Lieferumfang des Platform Software Development [](/windows/desktop/SecGloss/s-gly)Kit (SDK) enthalten sind und das Schannel-Sicherheitspaket veranschaulichen, finden Sie in den PSDK-Beispielen mit Schannel.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Angeben von Schannel-Verschlüsselungen und Verschlüsselungsstärken](specifying-schannel-ciphers-and-cipher-strengths.md)
</dt> </dl>

 

 
