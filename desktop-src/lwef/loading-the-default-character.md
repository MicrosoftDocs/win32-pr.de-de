---
title: Laden des Standard Zeichens
description: Laden des Standard Zeichens
ms.assetid: 4e91aef5-8402-401d-b09f-83be25011027
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 387715b5078c4ec875c9abce47039898e4998cf7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106339812"
---
# <a name="loading-the-default-character"></a>Laden des Standard Zeichens

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

Anstatt nur ein bestimmtes Zeichen direkt durch Angabe des Datei namens zu laden, können Sie das *Standard Zeichen* laden. Das Standard Zeichen ist ein Dienst, der einen freigegebenen, zentralen Windows-Assistenten bereitstellen soll, den der Benutzer auswählt. Der Microsoft-Agent enthält ein Eigenschaften Blatt als Teil des Standard-Zeichen diensdienstanders, das als Zeichen Eigenschaftenfenster bezeichnet wird, das es dem Benutzer ermöglicht, die Auswahl des Standard Zeichens zu ändern.

Die Auswahl des Standard Zeichens ist auf ein Zeichen beschränkt, das den Standard Animations Satz unterstützt. Dadurch wird ein grundlegendes Maß an Konsistenz zwischen Zeichen sichergestellt. Dadurch wird kein Zeichen von zusätzlichen Animationen ausgeschlossen.

Da das Standard Zeichen jedoch für die Verwendung durch allgemeine Zwecke vorgesehen ist und von anderen Anwendungen gleichzeitig gemeinsam genutzt werden kann, sollten Sie das Standard Zeichen nicht laden, wenn Sie ein Zeichen exklusiv für Ihre Anwendung verwenden möchten.

Um das Standard Zeichen zu laden, müssen Sie die [**Load**](load-method.md) -Methode ohne Angabe eines Datei namens oder Pfads aufzurufen. Der Microsoft-Agent lädt den aktuellen Zeichensatz automatisch als Standard Zeichen. Wenn der Benutzer noch kein Standard Zeichen ausgewählt hat, wählt der-Agent das erste Zeichen aus, das den Standard Animations Satz unterstützt. Wenn keine verfügbar ist, schlägt die Methode fehl, und die Ursache wird gemeldet.

Obwohl eine Client Anwendung die Identität des Zeichens untersuchen kann, kann nur ein Benutzer seine Einstellungen ändern. Mithilfe der [**showdefaultcharacters-Eigenschaften**](showdefaultcharacterproperties-method.md) können Sie das Zeichen Eigenschaftenfenster anzeigen.

Der Server benachrichtigt Clients, die das Standard Zeichen geladen haben, wenn ein Benutzer eine Zeichenauswahl ändert, und übergibt die GUID des neuen Zeichens. Der Server entlädt automatisch das erste Zeichen und lädt das neue Zeichen erneut. Die Warteschlangen aller Clients, die das Standard Zeichen geladen haben, werden angehalten und geleert. Die Warteschlangen von Clients, die das Zeichen explizit mit dem Dateinamen des Zeichens geladen haben, sind jedoch nicht betroffen. Der Server übernimmt bei Bedarf auch das automatische Zurücksetzen des Text-zu-Sprache-Moduls (TTS) für das neue Zeichen.

 

 




