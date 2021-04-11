---
title: Richtlinien für die Dateinamenerweiterung
description: Richtlinien für die Dateinamenerweiterung
ms.assetid: 71189ed8-4140-446f-a765-d72f35dd3d88
keywords:
- Windows Media-Format-SDK, Dateinamen Erweiterungen
- Advanced Systems Format (ASF), Dateinamen Erweiterungen
- ASF (Advanced Systems Format), Dateinamen Erweiterungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bed1fb59379644711a3954dc5eb82707e0e42f8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947670"
---
# <a name="file-name-extension-guidelines"></a>Richtlinien für die Dateinamenerweiterung

Eine Dateinamenerweiterung bietet einem unabhängigen Softwarehersteller Informationen zu den Renderinganforderungen einer Anwendung, die diese spezielle Erweiterung verwendet.

Die Dateinamenerweiterung, die Sie für eine Datei verwenden müssen, die von einer Anwendung basierend auf dem Windows Media Format SDK erstellt wurde, hängt vom Typ des Inhalts in der Datei ab. Verwenden Sie die folgende Logik, um die Dateinamenerweiterung zu bestimmen, die Sie verwenden müssen.

Wenn die Datei Datenströme enthält, die von Drittanbietern oder nicht unterstützten unkomprimierten Daten (einschließlich beliebiger Daten) codiert sind, muss die Datei die. asf-Erweiterung verwenden.

Wenn die Datei keine nicht unterstützten Streams enthält und mindestens einen Videostream enthält, der entweder unkomprimiert ist oder mit einem beliebigen Windows Media-Videocodec codiert ist, muss die Datei die Erweiterung. wmv verwenden. Diese Dateien können auch PCM-Audiostreams, Audiostreams enthalten, die mit beliebigen Windows Media-Audiocodecs, Skript Datenströmen und Webstreams codiert sind.

Wenn die Datei keine nicht unterstützten Streams und keine unterstützten Videostreams enthält und mindestens ein Audiodatenstrom entweder unkomprimiertes PCM oder codiert mit einem beliebigen Windows Media-Audiocodec enthält, muss die Datei die. wma-Erweiterung verwenden. Diese Dateien können auch Skript Datenströme und Webstreams enthalten.

Wenn die Datei nur Datenströme enthält, die weder Audiodaten noch Video enthalten, muss Sie die Erweiterung ". ASF" verwenden.

Unterstützte unkomprimierte Video Typen sind RGB8, RGB565, RGB555, RGB24, RGB32, I420, IYUV, YV12, im YUY2, UYVY, yvyu und YVU9.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Überlegungen zu Projekten**](project-considerations.md)
</dt> </dl>

 

 




