---
description: Verwenden paralleler Assemblys als Ressource
ms.assetid: f7963d37-93c4-49d6-af7d-fc692f632894
title: Verwenden paralleler Assemblys als Ressource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b97265b48f4ce8f3c87a87ec4ca9ea2b8252819
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958844"
---
# <a name="using-side-by-side-assemblies-as-a-resource"></a>Verwenden paralleler Assemblys als Ressource

Sie können einer-Anwendung ein Manifest als Ressource in der binären ausführbaren Header Datei der Anwendung hinzufügen. Der Wert der \_ manifestressourcenid bestimmt, wie die parallelen Assemblyabhängigkeiten, die \_ im Manifest beschrieben werden, vom Lade Modul verwendet werden.

Wenn Sie die \_ manifestressourcenid \_ auf 1 festlegen, verwendet das Lade Modul die parallelen Assemblyabhängigkeiten, die im Manifest als ProzessStandard angegeben sind. Alle Plug-Ins verwenden auch diesen ProzessStandard.

In der folgenden Tabelle wird zusammengefasst, wie das Lade Modul das Manifest für verschiedene Werte der manifestressourcenid verwendet, \_ \_ Wenn die Anwendung mit dem \_ aktivierten Flag-disolations \_ fähig ist. Beachten Sie, dass die Werte 1-16 für die Verwendung durch Windows XP reserviert sind. Entwickler können andere Werte verwenden, wenn Sie die Aktivierungs Kontexte mithilfe der Funktionen verwalten möchten, die im [Aktivierungs Kontext Verweis](activation-context-reference.md)beschrieben werden.



| Wert der \_ manifestressourcenid \_ | Das Manifest gibt den Prozessstandard an? | Verwenden Sie für statische Importe? | Verwenden Sie für eine exe-Anwendung? | Verwenden Sie für eine dll? | Wird eine parallele Version der Assemblys verwendet, wenn die Kompilierung mit-disolations-Unterstützung \_ \_ aktiviert ist? |
|---------------------------------|-----------------------------------------|-------------------------|-----------------|----------------|---------------------------------------------------------------------------------------|
| 1                               | Ja                                     | Ja                     | Ja             | Nein             | Ja                                                                                   |
| 2                               | Nein                                      | Ja                     | Ja             | Ja            | Ja                                                                                   |
| 3                               | Nein                                      | Nein                      | Ja             | Ja            | Ja                                                                                   |



 

\_ \_ Die manifestressourcenid 1 sollte für Anwendungen verwendet werden, die keine Plug-Ins hosten. Verwenden Sie \_ \_ die manifestressourcenid 1, wenn alle Teile der Anwendung die Version der parallelen Assembly verwenden sollen, die im Manifest angegeben ist. Weitere Informationen finden Sie unter [Aktivieren einer Assembly in einer Anwendung ohne Erweiterungen](enabling-an-assembly-in-an-application-without-extensions.md).

\_Manifestressourcenid \_ 2 sollte für Anwendungen verwendet werden, die Steuerelemente oder Plug-ins von Drittanbietern hosten. In diesem Fall wirkt sich das Manifest auf alle parallelen Assemblys aus, die durch statisches Laden geladen werden, DllMain-Aufrufe und Aufrufe, die von-disolations-Unterstützung \_ \_ aktiviert wurden. Weitere Informationen finden Sie unter [Aktivieren einer Assembly in einer Anwendung, die eine DLL, Erweiterung oder Systemsteuerung gehostet](enabling-an-assembly-in-an-application-hosting-a-dll-extension-or-control-panel.md).

\_Manifestressourcenid \_ 3 sollte zum Umleiten von Aufrufen durch-disolations Unterstützung verwendet werden \_ \_ . Das Laden von anderen Methoden ist nicht betroffen.

 

 



