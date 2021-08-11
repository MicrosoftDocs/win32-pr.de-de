---
title: Laden des Standardzeichens
description: Laden des Standardzeichens
ms.assetid: 4e91aef5-8402-401d-b09f-83be25011027
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f99d194843c6196f69e287857ce08097e849f328738c5f5d1a6e7feba0c53d18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118247607"
---
# <a name="loading-the-default-character"></a>Laden des Standardzeichens

\[Microsoft Agent ist ab Version Windows 7 veraltet und möglicherweise in nachfolgenden Versionen von Windows.\]

Anstatt nur ein bestimmtes Zeichen direkt durch Angabe des Dateinamens zu laden, können Sie das *Standardzeichen laden.* Das Standardzeichen ist ein Dienst, der einen freigegebenen, zentralen Windows, den der Benutzer auswählt, bereitstellen soll. Microsoft Agent enthält ein Eigenschaftenblatt als Teil des Standardzeichendiensts, der als Zeichen-Eigenschaftenfenster bezeichnet wird und es dem Benutzer ermöglicht, seine Auswahl des Standardzeichens zu ändern.

Die Auswahl des Standardzeichens ist auf ein Zeichen beschränkt, das den Standardanimationsatz unterstützt, um ein grundlegendes Maß an Konsistenz zwischen Zeichen sicherzustellen. Dies schließt nicht aus, dass ein Zeichen über zusätzliche Animationen verfügt.

Da das Standardzeichen jedoch für die allgemeine Verwendung vorgesehen ist und von anderen Anwendungen gleichzeitig freigegeben werden kann, vermeiden Sie das Laden des Standardzeichens, wenn Sie ein Zeichen ausschließlich für Ihre Anwendung wünschen.

Um das Standardzeichen zu laden, rufen Sie die [**Load-Methode**](load-method.md) auf, ohne einen Dateinamen oder Pfad anzugeben. Microsoft Agent lädt automatisch den aktuellen Zeichensatz als Standardzeichen. Wenn der Benutzer noch kein Standardzeichen ausgewählt hat, wählt der -Agent das erste Zeichen aus, das den Standardanimationsatz unterstützt. Wenn keine verfügbar ist, verursacht die Methode einen Fehler und gibt die Ursache zurück.

Obwohl eine Clientanwendung die Identität des Zeichens abfragen kann, kann nur ein Benutzer seine Einstellungen ändern. Sie können [**showDefaultCharacterProperties**](showdefaultcharacterproperties-method.md) verwenden, um die Zeichenzeichenfolge Eigenschaftenfenster.

Der Server benachrichtigt Clients, die das Standardzeichen geladen haben, wenn ein Benutzer eine Zeichenauswahl ändert, und überträgt die GUID des neuen Zeichens. Der Server entlädt das erste Zeichen automatisch und lädt das neue Zeichen erneut. Die Warteschlangen aller Clients, die das Standardzeichen geladen haben, werden angehalten und geleert. Die Warteschlangen von Clients, die das Zeichen explizit mithilfe des Dateinamens des Zeichens geladen haben, sind jedoch nicht betroffen. Bei Bedarf übernimmt der Server auch das automatische Zurücksetzen der TTS-Engine (Text-to-Speech) für das neue Zeichen.

 

 




