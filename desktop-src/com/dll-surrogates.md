---
title: DLL-Surrogates
description: DLL-Surrogates
ms.assetid: fe30c0ae-1d19-4a5f-8ee3-8a5337c79c44
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 313c3fcbd07b4c6317dfb6ac8ede772fc62035f0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106337186"
---
# <a name="dll-surrogates"></a>DLL-Surrogates

COM ermöglicht das Erstellen von DLL-Servern, die in einen Ersatz-exe-Prozess geladen werden können. Dadurch wird die einfache Erstellung von DLL-Servern mit den Vorteilen der Implementierung der ausführbaren Datei kombiniert. Entwicklungs Tools wie Microsoft Visual Studio vereinfachen das Schreiben von DLL-Servern, aber ein dll-Server in sich weist Grenzen auf. Das Ausführen des dll-Servers in einem Ersatzprozess bietet verschiedene Vorteile:

-   Fehler Isolation und die Möglichkeit, mehrere Clients gleichzeitig zu bedienen.
-   In einer verteilten Umgebung könnte eine DLL-Server Implementierung zum Dienst von Remote Clients verwendet werden.
-   Sie können es Clients ermöglichen, sich selbst vor nicht vertrauenswürdigem Servercode zu schützen, während Sie Ihnen den Zugriff auf die vom dll-Server bereitgestellten Dienste erlauben.
-   Durch das Ausführen eines dll-Servers in einem Ersatz Zeichen erhält die dll die Sicherheit des Ersatz Diensts.

COM stellt einen standardmäßigen Ersatzprozess bereit, oder Sie können ein benutzerdefiniertes Ersatz Zeichen schreiben, wenn Sie besondere Anforderungen haben.

Die folgenden Themen enthalten weitere Informationen zu dll-Surrogates:

-   [DLL-Server Anforderungen](dll-server-requirements.md)
-   [Verwenden des System-Supplied Ersatz Zeichens](using-the-system-supplied-surrogate.md)
-   [Schreiben eines benutzerdefinierten Ersatz Zeichens](writing-a-custom-surrogate.md)

 

 




