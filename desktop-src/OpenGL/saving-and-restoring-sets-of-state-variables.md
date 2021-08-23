---
title: Speichern und Wiederherstellen von Sätzen von Zustandsvariablen
description: Sie können die Werte einer Auflistung von Zustandsvariablen in einem Attributstapel mit den Funktionen glPushAttrib und glPopAttrib speichern und wiederherstellen.
ms.assetid: 339de633-4158-4907-b985-2d75b465fb2a
keywords:
- OpenGL-Zustandsvariablen
- Speichern von Zustandsvariablen OpenGL
- Wiederherstellen von Zustandsvariablen OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 197a05d80e72479aecdade3323899464bf0b1f4afa2d9f2a8a1a1add6e56db78
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119553810"
---
# <a name="saving-and-restoring-sets-of-state-variables"></a>Speichern und Wiederherstellen von Sätzen von Zustandsvariablen

Sie können die Werte einer Auflistung von Zustandsvariablen in einem Attributstapel mit den Funktionen [**glPushAttrib**](glpushattrib.md) und [**glPopAttrib**](glpopattrib.md) speichern und wiederherstellen. Der Attributstapel hat eine Tiefe von mindestens 16. Um die tatsächliche Tiefe zu erhalten, verwenden Sie GL \_ MAX \_ ATTRIB \_ STACK DEPTH mit \_ [**glGetIntegerv**](glgetintegerv.md). Das Pushen eines vollständigen Stapels oder das Popen eines leeren Stapels führt zu einem Fehler.

Im Allgemeinen ist es schneller, **glPushAttrib** und **glPopAttrib** zu verwenden, als die Werte selbst abzurufen und wiederherzustellen. Einige Werte werden möglicherweise in die Hardware gepusht und per Pop übertragen, und das Speichern und Wiederherstellen dieser Werte kann ressourcenintensiv sein. Wenn Sie auf einem Remoteclient arbeiten, müssen außerdem alle Attributdaten über die Netzwerkverbindung und zurück übertragen werden, während sie gespeichert und wiederhergestellt werden. Ihre OpenGL-Implementierung behält jedoch den Attributstapel auf dem Server bei, um unnötige Netzwerkverzögerungen zu vermeiden.

Der Prototyp von **glPushAttrib** lautet:

**void** **glPushAttrib**(**GLbitfield** *mask* );

Mit [**glPushAttrib**](glpushattrib.md) werden alle attribute gespeichert, die durch Bits in *mask* angegeben werden, indem sie auf den Attributstapel gepusht werden. Eine Liste der möglichen Maskierungsbits, die Sie logisch OR zusammen erstellen können, um eine beliebige Kombination von Attributen zu speichern, finden Sie unter [Attributgruppen.](attribute-groups.md) Jedes Bit entspricht einer Auflistung einzelner Zustandsvariablen. GL LIGHTING BIT bezieht sich z. \_ \_ B. auf alle Zustandsvariablen im Zusammenhang mit der Beleuchtung, die die aktuelle Materialfarbe, die Umgebungsfarbe, die Diffuse, das Glanzlicht und das ausgegebene Licht, eine Liste der aktivierten Beleuchtungen und die Richtungen der Spotlights enthalten. Wenn Sie [**glPopAttrib**](glpopattrib.md)aufrufen, werden alle diese Variablen wiederhergestellt. Informationen dazu, welche Attribute genau für bestimmte Maskenwerte gespeichert werden, finden Sie unter [OpenGL State Variables](opengl-state-variables.md).

 

 




