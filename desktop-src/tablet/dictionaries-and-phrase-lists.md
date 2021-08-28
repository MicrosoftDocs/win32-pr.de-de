---
description: Das Lexikon oder eine Liste möglicher Wörter, die vom Sprachmodell einer bestimmten Erkennung verwendet werden, ist in einem oder mehreren Wörterbüchern enthalten.
ms.assetid: e975a75f-ab88-4164-afc8-3b817988504d
title: Wörterbücher und Ausdruckslisten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0cc5b97918e1fed384494e887b604f1d08856e27232ed82f09bceff3ce14fe2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120110960"
---
# <a name="dictionaries-and-phrase-lists"></a>Wörterbücher und Ausdruckslisten

Das Lexikon oder eine Liste möglicher Wörter, die vom Sprachmodell einer bestimmten Erkennung verwendet werden, ist in einem oder mehreren Wörterbüchern enthalten. Die Erkennung durchsucht beim Kompilieren von Erkennungsabstimmungen alle wörterbücher, die im System verfügbar sind. Sie können die Microsoft Speech-APIs (SAPI) verwenden, um einige dieser Wörterbücher zu ändern.

Eine Ausdrucksliste bietet eine weitere Möglichkeit, das Vokabular der Erkennung zu ändern. Das Hinzufügen von Wörtern zu einer Ausdrucksliste erweitert das Vokabular. Das Hinzufügen von Wörtern und das anschließende Einschränken der Erkennung auf die Verwendung nur der Ausdrucksliste (im Gegensatz zur Ausdrucksliste und den Wörterbüchern) schränkt das Vokabular ein.

Frühere Versionen der Tablet PC Technology-APIs beruhten auf dem Konzept von Wortlisten. Wortlisten sind fast identisch mit Begriffslisten und werden für den gleichen Zweck verwendet, wenn sie direkt mit einem [**RecognizerContext-Objekt**](inkrecognizercontext-class.md) in einer Anwendung arbeiten, für die Ink aktiviert ist. Weitere Informationen dazu, wo und wann Wortlisten verwendet werden sollten, finden Sie unter [Festlegen des Kontexts für Ink-Enabled-Steuerelemente.](setting-context-for-ink-enabled-controls.md)

Wenn die Größe der Liste, mit der Sie das Lexikon erweitern möchten, 100.000 Wörter überschreitet, wird empfohlen, anstelle einer Wortliste oder Ausdrucksliste ein Wörterbuch zu verwenden.

 

 



