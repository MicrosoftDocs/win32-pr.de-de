---
title: Angegebener Benutzer
description: Angegebener Benutzer
ms.assetid: ec7684fb-a9f1-4ef2-a7d4-07caf24b6023
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acce63aa502a8966cd0eb53c90dcca3c4454e80b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106340204"
---
# <a name="specified-user"></a>Angegebener Benutzer

Die Angabe eines bestimmten Benutzers (und des Benutzer Kennworts) ist die bevorzugte Identität für com-Server. Der Grund für die bevorzugte Identität ist, dass auf dem Computer, auf dem der Server ausgeführt wird, auf dem Server ausgeführt werden muss, auf dem der Server ausgeführt wird, und jeder Client mit derselben Instanz des Servers kommuniziert, wenn der Server seine Klassenfactory als Mehrfachverwendung registriert. Wenn der Server über eine grafische Benutzeroberfläche verfügt, sollten Sie diese Identität nicht auswählen. Wenn Sie dies tun, wird der Benutzer nicht in der Lage sein, die Benutzeroberfläche anzuzeigen.

Diese Art von Server verfügt über ein primäres Token und kann auf Remote Ressourcen zugreifen, bei denen ein Server mit der Start-Benutzer-Identität möglicherweise nicht in der Lage ist. Weitere Informationen zu Identitäts [Wechsel-und](cloaking.md)Zugriffs Token finden Sie unter Identitätswechsel [Ebenen](impersonation-levels.md) und-Verschleierung.

Das Ausführen von als festes Benutzerkonto ist sicherer als die interaktive Benutzeridentität, da diese Identität der Anwendung nur von einem Benutzer mit dem Kennwort eines bestimmten Benutzers zugewiesen werden kann.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Anwendungs Identität](application-identity.md)
</dt> <dt>

[Interaktiver Benutzer](interactive-user.md)
</dt> <dt>

[Benutzer wird gestartet](launching-user.md)
</dt> <dt>

[Dienst Identität](service-identity.md)
</dt> </dl>

 

 




