---
title: Marker
description: Marker
ms.assetid: ba9bc93e-76a9-4a49-951f-c38dbcceef8c
keywords:
- Windows Media-Format-SDK, Marker
- Advanced Systems Format (ASF), Marker
- ASF (Advanced Systems Format), Marker
- Marker, Info
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d314b4e74aa05a08dfd4a297687662e10f045abc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856892"
---
# <a name="markers"></a>Marker

Marker sind benannte Stellen auf der Zeitachse einer ASF-Datei. Jeder Marker hat einen Namen und eine Präsentationszeit, die Sie zuweisen. Sie können so viele Marker angeben, wie Sie für eine Datei benötigen.

Marker sind nützlich, um große ASF-Dateien in logische Teile aufzuteilen. Eine Anwendung, die das Reader-Objekt zur Wiedergabe von ASF-Dateien verwendet, kann dem Benutzer die Möglichkeit bieten, von Marker zu Marker zu springen und die Navigation digitaler Medien zu vereinfachen. Wenn Sie z. b. eine ASF-Datei aus einer Präsentation erstellen, können Sie Marker für jedes wichtige Topic, das besprochen wird, in der Zeitachse platzieren. Bei der Wiedergabe kann ein Benutzer einfach ein Thema aus einer Liste auswählen und direkt zum entsprechenden Teil der Datei wechseln, anstatt eine lange Zeitachse zu erhalten, die sich an der Position befinden muss, an der gesucht werden soll.

Marker werden durch das Metadaten-Editor-Objekt manipuliert. Sie können die Marker in einer Datei jederzeit hinzufügen, entfernen und anzeigen, nachdem die Datei geschrieben wurde.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Funktionen der ASF-Datei**](asf-file-features.md)
</dt> <dt>

[**So suchen Sie Marker**](to-seek-to-markers.md)
</dt> <dt>

[**Verwenden von Markern**](using-markers.md)
</dt> </dl>

 

 




