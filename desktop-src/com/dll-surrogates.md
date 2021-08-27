---
title: DLL-Ersatzzeichen
description: DLL-Ersatzzeichen
ms.assetid: fe30c0ae-1d19-4a5f-8ee3-8a5337c79c44
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 808efe4a431a703282a705000d2fe18f6b4cfcde121d95c39fe65541b0260503
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119993250"
---
# <a name="dll-surrogates"></a>DLL-Ersatzzeichen

COM ermöglicht das Erstellen von DLL-Servern, die in einen Ersatz-EXE-Prozess geladen werden können. Dies kombiniert das einfache Schreiben von DLL-Servern mit den Vorteilen der ausführbaren Implementierung. Entwicklungstools wie Microsoft Visual Studio das Schreiben von DLL-Servern erleichtern, aber ein DLL-Server an sich hat Grenzen. Das Ausführen des DLL-Servers in einem Ersatzprozess bietet mehrere mögliche Vorteile:

-   Fehlerisolation und die Möglichkeit, mehrere Clients gleichzeitig zu bedienen.
-   In einer verteilten Umgebung kann eine DLL-Serverimplementierungen verwendet werden, um Remoteclients zu bedienen.
-   Es könnte Clients ermöglichen, sich vor nicht vertrauenswürdigem Servercode zu schützen, während sie gleichzeitig Zugriff auf die Dienste haben, die der DLL-Server bereitstellt.
-   Das Ausführen eines DLL-Servers in einem Ersatzzeichen stellt die Sicherheit des Ersatzzeichens für die DLL bereit.

COM stellt einen Standard-Ersatzprozess bereit, oder Sie können ein benutzerdefiniertes Ersatzzeichen schreiben, wenn Sie besondere Anforderungen haben.

Die folgenden Themen enthalten weitere Informationen zu DLL-Ersatzzeichen:

-   [DLL-Serveranforderungen](dll-server-requirements.md)
-   [Verwenden des System-Supplied Ersatzzeichens](using-the-system-supplied-surrogate.md)
-   [Schreiben eines benutzerdefinierten Ersatzzeichens](writing-a-custom-surrogate.md)

 

 




