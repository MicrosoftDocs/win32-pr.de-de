---
title: Rendering von Absichten
description: Das International Color Consortium (ICC) hat vier verschiedene Werte definiert, die als renderintents bezeichnet werden.
ms.assetid: c980f3ea-daff-491a-a10a-03ba446d383e
keywords:
- Windows Color System (WCS), renderintents
- WCS (Windows Color System), renderintents
- Bild Farbverwaltung, renderintents
- Farbverwaltung, renderintents
- Farben, renderintents
- renderintents
- International Color Consortium (ICC)
- IIC (International Color Consortium)
- Bild Absicht
- Grafische Absicht
- Nachweis Absicht
- Ziel Übereinstimmung
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72df148cf4c439c8081e41f3eb8089c5588e7fe2
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106357170"
---
# <a name="rendering-intents"></a>Rendering von Absichten

Das International Color Consortium (ICC) hat vier verschiedene Werte definiert, die als *renderintents* bezeichnet werden. Diese stellen vier verschiedene Ansätze zum Erstellen eines Farb Rendering dar. Diese vier Intents und die Konstanten, die verwendet werden, um Sie im Code zu verweisen, lauten wie folgt.



| Intent                            | Name des ICC              | BESCHREIBUNG                    |
|-----------------------------------|-----------------------|--------------------------------|
| Picture | Wahrnehmungs            | beabsichtigte \_ Absicht             |
| Graphic | Sättigung            | beabsichtigte \_ Sättigung             |
| Proof     | Relative farbige Metrik | beabsichtigte \_ relative \_ farbige Metrik |
| Match     | Absolute farbige Metrik | beabsichtigte \_ absolute \_ farbige Metrik |




 

Die Version 3,4, in der diese Intents beschrieben werden, kann von Color.org heruntergeladen werden.

## <a name="picture-intent"></a>Bild Absicht

Eine Bild Absicht, die als perzeptive Absicht in der ICC-Spezifikations Klausel 4,9 bezeichnet wird, bewirkt, dass [die vollständige](./g.md) Spiel Größe des Bilds komprimiert oder erweitert wird, um die Größe des Zielgeräts zu füllen, sodass das graue Gleichgewicht beibehalten wird, die farbige metrikgenauigkeit jedoch möglicherweise nicht beibehalten wird.

Anders ausgedrückt: Wenn bestimmte Farben in einem Bild außerhalb des Bereichs von Farben liegen, die das Ausgabegerät rendern kann, bewirkt die Bild Absicht, dass alle Farben im Bild so angepasst werden, dass jede Farbe im Bild innerhalb des Bereichs liegt, der gerendert werden kann, sodass die Beziehung zwischen Farben so weit wie möglich beibehalten wird.

Diese Absicht eignet sich am besten für die Anzeige von Fotos und Bildern und ist in der Regel die Standard Absicht.

## <a name="graphic-intent"></a>Grafische Absicht

Die Klausel der ICC-Spezifikation 4,12 Ruft die Absicht einer [Sättigung](s.md) der Absicht auf. Es behält den Chroma der Farben im Bild bei möglichen Ausgaben von [Hue](h.md) und [Helligkeit](l.md)bei.

Die Implementierung dieser Absicht bleibt etwas problematisch, und der IStGH arbeitet immer noch an Methoden, um die gewünschten Effekte zu erzielen.

Diese Absicht eignet sich am besten für Unternehmens Grafiken, wie z. b. Diagramme, bei denen es wichtiger ist, dass die Farben lebhaft sind und einander gegenseitig und nicht eine bestimmte Farbe vergleichen.

## <a name="proof-intent"></a>Nachweis Absicht

Die Nachweis Absicht, die als farbige Metrik in der Bezeichnung "ICC" bezeichnet wird, ist so definiert, dass alle Farben, die außerhalb des Bereichs liegen, den das Ausgabegerät rendern kann, an die nächstgelegene Farbe angepasst werden, die gerendert werden kann, während alle anderen Farben unverändert bleiben.

Die Nachweis Absicht behält den [weißen Punkt](w.md)nicht bei.

Beispielsweise ist das weiß eines Whitepapers mit einem Whitepaper besser gelb als das whitetestweiß eines Computermonitors. Ein Bild, das mithilfe relativer farbige metrikabsicht in die Spiel Palette konvertiert wurde, würde dazu führen, dass alle Farben Gelb werden. Der weiße Punkt des Bilds wird so verschoben, dass er dem weißen Punkt des Druckers entspricht. Alle anderen Farben im Bild behalten ihre Position relativ zum weißen Punkt bei. Dadurch wird ein Bild erzeugt, das das Aussehen des gedruckten Bilds genauer widerspiegelt. Der Benutzer kann es jedoch visuell disconcerting finden.

## <a name="match-intent"></a>Ziel Übereinstimmung

In einer Übereinstimmungs Absicht werden alle Farben, die außerhalb des Bereichs liegen, den das Ausgabegerät rendern kann, an die nächstgelegene Farbe angepasst, die gerendert werden kann, während alle anderen Farben unverändert bleiben. Die Spezifikation "ICC" Ruft die Absicht "Match Intent absolute colormetric" auf.

Die Übereinstimmungs Absicht behält den weißen Punkt bei.

Beispielsweise ist das weiß eines Whitepapers mit einem Whitepaper besser gelb als das whitetestweiß eines Computermonitors. Ein Bild, das mit der Übereinstimmungs Absicht in den [Farbskala](./g.md) des Druckers konvertiert wurde, würde dazu führen, dass alle Farben konvertiert und mit dem Spiel des Druckers verglichen werden. Der weiße Punkt des Bilds wird nicht so verschoben, dass er dem weißen Punkt des Druckers entspricht. Daher kann sich der Abstand der Farben zum weißen Punkt ändern. Dies erzeugt ein Bild, das weniger visuell mit dem Benutzer disconceriert, aber auch eine weniger genaue Darstellung der Druckerausgabe ist.

 

 