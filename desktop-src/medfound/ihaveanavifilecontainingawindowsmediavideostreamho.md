---
description: Ich habe eine AVI-Datei, die einen Windows Medienvideostream enthält.
ms.assetid: 0b4c5bf2-caa6-4e14-be5f-9e25ec918cf0
title: Ich habe eine AVI-Datei, die einen Windows Medienvideostream enthält. Wie kann ich sie in eine WMV-Datei konvertieren?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74dfc2a5980533487c7a1c8716806fcedda1c7147bdacaf3ea0c887acbff0f83
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119777140"
---
# <a name="i-have-an-avi-file-containing-a-windows-media-video-stream-how-can-i-convert-it-to-a-wmv-file"></a>Ich habe eine AVI-Datei, die einen Windows Medienvideostream enthält. Wie kann ich sie in eine WMV-Datei konvertieren?

Die Windows Medienaudio- und Videocodec-Schnittstellen bieten keine Methoden zum Erstellen von Dateien mit dem Advanced Systems Format (ASF), dem Format, das für WMV-Dateien verwendet wird. Wenn Sie eine Datei (mit einem beliebigen Container) in eine ASF-Datei konvertieren möchten, müssen Sie die Objekte des Windows Media Format SDK verwenden.

Rufen Sie die komprimierten Windows Medienbeispiele aus der Quelldatei ab, und übergeben Sie sie als Streambeispiele an das Writer-Objekt. Weitere Informationen finden Sie in der Dokumentation Windows Media Format 9 Series SDK.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Häufig gestellte Fragen](frequentlyaskedquestions.md)
</dt> </dl>

 

 



