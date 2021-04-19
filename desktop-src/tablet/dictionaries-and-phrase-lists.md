---
description: Das Lexicon oder die Liste möglicher Wörter, die vom Sprachmodell einer bestimmten Erkennungsfunktion verwendet werden, ist in mindestens einem Wörterbuch enthalten.
ms.assetid: e975a75f-ab88-4164-afc8-3b817988504d
title: Wörterbücher und Ausdrucks Listen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1f88dc2f6b05eea322b6e88dda1f986b3c54b7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353898"
---
# <a name="dictionaries-and-phrase-lists"></a>Wörterbücher und Ausdrucks Listen

Das Lexicon oder die Liste möglicher Wörter, die vom Sprachmodell einer bestimmten Erkennungsfunktion verwendet werden, ist in mindestens einem Wörterbuch enthalten. Die Erkennung durchsucht alle im System verfügbaren Wörterbücher, wenn Erkennungs Übereinstimmungen kompiliert werden. Sie können die Microsoft Speech APIs (SAPI) verwenden, um einige dieser Wörterbücher zu ändern.

Eine Ausdrucks Liste stellt eine andere Möglichkeit zum Ändern des vokabularerkennungs-Vokabulars dar. Durch das Hinzufügen von Wörtern zu einer Ausdrucks Liste wird das Vokabular erweitert. durch das Hinzufügen von Wörtern und Einschränken der Erkennungsfunktion zur Verwendung nur der Ausdrucks Liste (im Gegensatz zur Ausdrucks Liste und den Wörterbüchern) wird das Vokabular eingeschränkt.

Frühere Versionen der Tablet PC-Technologie-APIs stützten sich auf das Konzept der Wortlisten. Word-Listen sind fast identisch mit den Ausdrucks Listen und werden für denselben Zweck verwendet, wenn Sie direkt mit einem [**erkenzercontext**](inkrecognizercontext-class.md) -Objekt in einer Anwendung arbeiten, für die frei Hand Eingaben aktiviert ist. Weitere Informationen dazu, wo und wann Wortlisten verwendet werden sollten, finden Sie unter [Setting Context for Ink-Enabled Controls](setting-context-for-ink-enabled-controls.md).

Wenn die Größe der Liste, mit der Sie das Lexikon erweitern möchten, 100.000 Wörter überschreitet, empfiehlt es sich, anstelle einer Wort Liste oder einer Ausdrucks Liste ein Wörterbuch zu verwenden.

 

 



