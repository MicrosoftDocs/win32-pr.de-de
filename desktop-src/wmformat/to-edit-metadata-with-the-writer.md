---
title: So bearbeiten Sie Metadaten mit dem Writer
description: So bearbeiten Sie Metadaten mit dem Writer
ms.assetid: 86badfe3-64bc-4285-a231-f6c0ebf4f262
keywords:
- Windows Media-Format-SDK, Bearbeiten von Metadaten mit dem Writer
- Windows Media-Format-SDK, Metadatenbearbeitung
- Advanced Systems Format (ASF), Bearbeiten von Metadaten mit dem Writer
- ASF (Advanced Systems Format), Bearbeiten von Metadaten mit dem Writer
- Advanced Systems Format (ASF), Metadatenbearbeitung
- ASF (Advanced Systems Format), Metadatenbearbeitung
- Metadaten, bearbeiten mit dem Writer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f2823b266b51da366683ac0b5cf65e10debf1ad
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2020
ms.locfileid: "104390060"
---
# <a name="to-edit-metadata-with-the-writer"></a>So bearbeiten Sie Metadaten mit dem Writer

Sie können direkt vom Writer aus auf die Metadaten, die in den Header der Datei gelangen, zugreifen. Rufen Sie die **QueryInterface** -Methode einer beliebigen Schnittstelle im Writer-Objekt auf, um einen Zeiger auf die [**iwmheaderinfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) -oder [**IWMHeaderInfo2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2) -Schnittstelle zu erhalten. Nachdem Sie über einen Zeiger auf die entsprechende Schnittstelle verfügen, können Sie die Metadaten genauso bearbeiten, wie Sie dies tun würden, wenn Sie die Datei im Metadateneditor-Objekt geladen hätten. Weitere Informationen zum Bearbeiten von Metadaten finden Sie unter [Arbeiten mit Metadaten](working-with-metadata.md).

Sie müssen vor dem Aufrufen von [**iwmwriter:: BeginWrite**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting)alle Änderungen an den Metadaten vornehmen.

> [!Note]  
> Wenn Sie Metadaten für eine Datei festlegen, die Datei schreiben und dann vorbereiten, eine neue Datei zu schreiben, ohne den Writer freizugeben, bleiben einige Metadaten, die für die erste Datei festgelegt wurden, festgelegt und werden in nachfolgende Dateien eingeschlossen. Wenn Sie mehrere Dateien mit derselben Instanz des Writer-Objekts schreiben, haben Sie zwei Möglichkeiten: Überprüfen Sie alle Metadaten, bevor Sie jede Datei schreiben, oder schreiben Sie nur in die Writer-Metadaten, die für alle Dateien gelten, die Sie schreiben.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Schreiben von ASF-Dateien**](writing-asf-files.md)
</dt> </dl>

 

 




