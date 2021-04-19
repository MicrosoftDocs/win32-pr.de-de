---
title: Speichern und Wiederherstellen von Sätzen von Zustandsvariablen
description: Sie können die Werte einer Auflistung von Zustandsvariablen in einem Attribut Stapel mit den Funktionen glpushatpub und glpopatpub speichern und wiederherstellen.
ms.assetid: 339de633-4158-4907-b985-2d75b465fb2a
keywords:
- OpenGL-Zustandsvariablen
- Speichern von Zustandsvariablen OpenGL
- Wiederherstellen von Zustandsvariablen OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b3192c228ea35005c5755802d3cd1b873f7b7fe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106338601"
---
# <a name="saving-and-restoring-sets-of-state-variables"></a>Speichern und Wiederherstellen von Sätzen von Zustandsvariablen

Sie können die Werte einer Auflistung von Zustandsvariablen in einem Attribut Stapel mit den Funktionen [**glpushatpub**](glpushattrib.md) und [**glpopatpub**](glpopattrib.md) speichern und wiederherstellen. Der Attribut Stapel hat eine Tiefe von mindestens 16. Um die tatsächliche Tiefe zu erhalten, verwenden Sie die maximale Speichergröße \_ \_ von GL \_ \_ . [](glgetintegerv.md) Durch das übertragen eines vollständigen Stapels oder das Pop einer leeren wird ein Fehler generiert.

Es ist in der Regel schneller, **glpushatpub** und **glpopatpub** zu verwenden, als die Werte selbst zu erhalten und wiederherzustellen. Einige Werte werden möglicherweise per pushübertragung in die Hardware übermittelt, und das Speichern und wiederherstellen kann ressourcenintensiv sein. Wenn Sie einen Remote Client verwenden, müssen alle Attributdaten bei der Speicherung und Wiederherstellung über die Netzwerkverbindung übertragen werden. Allerdings behält ihre OpenGL-Implementierung den Attribut Stapel auf dem Server bei, wodurch unnötige Netzwerkverzögerungen vermieden werden.

Der Prototyp von **glpushatpub** ist:

**void** **glpushattestb**(**GLbitfield** *Mask* );

Durch die Verwendung von [**glpushatpub**](glpushattrib.md) werden alle durch Bits in der *Maske* gekennzeichneten Attribute gespeichert, indem Sie auf den Attribut Stapel übertragen werden. Eine Liste der möglichen Masken Bits, die Sie logisch oder gemeinsam zum Speichern einer beliebigen Kombination von Attributen haben, finden Sie unter [Attribut Gruppen](attribute-groups.md). Jedes Bit entspricht einer Auflistung einzelner Zustandsvariablen. Das GL-Beleuchtungs Bit bezieht sich z. b. \_ \_ auf alle Zustandsvariablen im Zusammenhang mit der Beleuchtung, einschließlich der aktuellen Material Farbe, der Ambient-, diffuse, Glanz und ausgegebene Beleuchtung, einer Liste der aktivierten Lichter und der Richtungen der Schein Lichter. Wenn Sie [**glpopatzb**](glpopattrib.md)anrufen, werden alle diese Variablen wieder hergestellt. Informationen dazu, welche Attribute für bestimmte Masken Werte gespeichert werden, finden Sie unter [OpenGL State variables](opengl-state-variables.md).

 

 




