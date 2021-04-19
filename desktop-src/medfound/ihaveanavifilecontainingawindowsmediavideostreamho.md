---
description: Ich verfüge über eine AVI-Datei, die einen Windows Media Video Stream enthält.
ms.assetid: 0b4c5bf2-caa6-4e14-be5f-9e25ec918cf0
title: Ich verfüge über eine AVI-Datei, die einen Windows Media Video Stream enthält. Wie kann ich Sie in eine WMV-Datei konvertieren?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08c770a8355e92c6cfe052d86a17c6638a7a9948
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106366543"
---
# <a name="i-have-an-avi-file-containing-a-windows-media-video-stream-how-can-i-convert-it-to-a-wmv-file"></a>Ich verfüge über eine AVI-Datei, die einen Windows Media Video Stream enthält. Wie kann ich Sie in eine WMV-Datei konvertieren?

Die Windows Media Audio-und Video-Codec-Schnittstellen bieten keine Methoden zum Erstellen von Dateien mit dem Advanced Systems-Format (ASF). Dies ist das Format, das für WMV-Dateien verwendet wird. Wenn Sie eine Datei (mit einem beliebigen Container) in eine ASF-Datei konvertieren möchten, müssen Sie die Objekte des Windows Media Format SDK verwenden.

Rufen Sie die komprimierten Windows Media-Beispiele aus der Quelldatei ab, und übergeben Sie Sie als streambeispiele an das Writer-Objekt. Weitere Informationen finden Sie in der SDK-Dokumentation für das Windows Media-Format 9.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Häufig gestellte Fragen](frequentlyaskedquestions.md)
</dt> </dl>

 

 



