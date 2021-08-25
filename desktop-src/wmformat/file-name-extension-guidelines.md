---
title: Richtlinien für die Dateinamenerweiterung
description: Richtlinien für die Dateinamenerweiterung
ms.assetid: 71189ed8-4140-446f-a765-d72f35dd3d88
keywords:
- Windows Medienformat-SDK, Dateinamenerweiterungen
- Advanced Systems Format (ASF), Dateinamenerweiterungen
- ASF (Advanced Systems Format), Dateinamenerweiterungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ccd8c3b1b4ba27aa7360296fc336625cb0f51c4374bb77c06d349cb70a987c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118704003"
---
# <a name="file-name-extension-guidelines"></a>Richtlinien für die Dateinamenerweiterung

Eine Dateinamenerweiterung stellt einem unabhängigen Softwarehersteller Informationen zu den Renderinganforderungen einer Anwendung bereit, die diese bestimmte Erweiterung verwendet.

Die Dateinamenerweiterung, die Sie für eine Datei verwenden müssen, die von einer Anwendung basierend auf dem Windows Media Format SDK erstellt wurde, wird durch den Typ des Inhalts in der Datei bestimmt. Verwenden Sie die folgende Logik, um die Dateinamenerweiterung zu bestimmen, die Sie verwenden müssen.

Wenn die Datei Streams enthält, die mit Codecs von Drittanbietern oder nicht unterstützten nicht komprimierten Daten (einschließlich beliebiger Daten) codiert sind, muss die Datei die Erweiterung .asf verwenden.

Wenn die Datei keine nicht unterstützten Streams enthält und einen oder mehrere Videostreams enthält, die entweder unkomprimiert oder mit einem Windows Media-Videocodec codiert sind, muss die Datei die Erweiterung WMV verwenden. Diese Dateien können auch PCM-Audiostreams, Audiostreams, die mit einem beliebigen Windows Media-Audiocodec codiert sind, Skriptstreams und Webstreams enthalten.

Wenn die Datei keine nicht unterstützten Streams und keine unterstützten Videostreams enthält und einen oder mehrere Audiostreams enthält, die entweder nicht komprimiertes PCM oder mit einem beliebigen Windows Media-Audiocodec codiert sind, muss die Datei die WMA-Erweiterung verwenden. Diese Dateien können auch Skriptstreams und Webstreams enthalten.

Wenn die Datei nur Streams enthält, die weder Audio noch Video sind, muss sie die Erweiterung .asf verwenden.

Zu den unterstützten nicht komprimierten Videotypen zählen RGB8, RGB565, RGB555, RGB24, RGB32, I420, IYUV, YV12, YUY2, UYVY, YV MSI und YVU9.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Project Überlegungen**](project-considerations.md)
</dt> </dl>

 

 




