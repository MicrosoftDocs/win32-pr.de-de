---
title: So bearbeiten Sie Metadaten mit dem Writer
description: So bearbeiten Sie Metadaten mit dem Writer
ms.assetid: 86badfe3-64bc-4285-a231-f6c0ebf4f262
keywords:
- Windows Medienformat-SDK,Bearbeiten von Metadaten mit dem Writer
- Windows Medienformat-SDK, Metadatenbearbeitung
- Advanced Systems Format (ASF), Bearbeiten von Metadaten mit dem Writer
- ASF (Advanced Systems Format), Bearbeiten von Metadaten mit dem Writer
- Advanced Systems Format (ASF), Metadatenbearbeitung
- ASF (Advanced Systems Format), Metadatenbearbeitung
- Metadaten, Bearbeiten mit dem Writer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d09db09a2cd7dbc50130243e322085ab2113e76f71d8b6760bd602d16f29d3a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118197070"
---
# <a name="to-edit-metadata-with-the-writer"></a>So bearbeiten Sie Metadaten mit dem Writer

Sie können direkt über den Writer auf die Metadaten zugreifen, die in den Header der Datei gelangen. Rufen Sie die **QueryInterface-Methode** einer beliebigen Schnittstelle im Writer-Objekt auf, um einen Zeiger auf die [**IWMHeaderInfo-**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) oder [**IWMHeaderInfo2-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2) abzurufen. Nachdem Sie über einen Zeiger auf die entsprechende Schnittstelle verfügen, können Sie die Metadaten so bearbeiten, wie Sie die Datei in das Metadaten-Editor-Objekt geladen hätten. Weitere Informationen zum Bearbeiten von Metadaten finden Sie unter [Arbeiten mit Metadaten.](working-with-metadata.md)

Sie müssen alle Änderungen an den Metadaten vornehmen, bevor [**Sie IWMWriter::BeginWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting)aufrufen.

> [!Note]  
> Wenn Sie Metadaten für eine Datei festlegen, die Datei schreiben und dann das Schreiben einer neuen Datei vorbereiten, ohne den Writer freizugeben, bleiben einige Metadaten, die für die erste Datei festgelegt wurden, festgelegt und werden in den nachfolgenden Dateien enthalten sein. Wenn Sie mehrere Dateien mit derselben Instanz des Writer-Objekts schreiben, haben Sie zwei Möglichkeiten: Überprüfen Sie alle Metadaten, bevor Sie jede Datei schreiben, oder schreiben Sie nur die Writermetadaten, die für alle dateien gelten, die Sie schreiben.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Schreiben von ASF-Dateien**](writing-asf-files.md)
</dt> </dl>

 

 




