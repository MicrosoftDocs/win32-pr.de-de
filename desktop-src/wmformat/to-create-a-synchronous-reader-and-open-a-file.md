---
title: So erstellen Sie einen synchronen Reader und öffnen eine Datei
description: So erstellen Sie einen synchronen Reader und öffnen eine Datei
ms.assetid: 6349d05e-20db-4ce8-83fd-cad4cec666f2
keywords:
- Advanced Systems Format (ASF), Erstellen von Lesern
- ASF (Advanced Systems Format), Erstellen von Lesern
- Advanced Systems Format (ASF), Öffnen von Dateien
- ASF (Advanced Systems Format), Öffnen von Dateien
- synchrone Leser, erstellen
- synchrone Leser, Öffnen von Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e222c046a685885fa9e17baa52d0161176551ff3
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2020
ms.locfileid: "106341509"
---
# <a name="to-create-a-synchronous-reader-and-open-a-file"></a>So erstellen Sie einen synchronen Reader und öffnen eine Datei

Bevor Sie mit dem synchronen Reader arbeiten können, müssen Sie ein synchrones Reader-Objekt erstellen und eine Datei zum Lesen laden. Führen Sie die folgenden Schritte aus, um den synchronen Reader zu initialisieren und eine Datei zu öffnen.

1.  Erstellen Sie ein synchrones Reader-Objekt, indem Sie die [**wmcreatesyncreader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatesyncreader) -Funktion aufrufen. Sie müssen die gewünschte Ebene der Rechteverwaltung für das neue Reader-Objekt angeben. Die verfügbaren Modi sind im Enumerationstyp **WMT- \_ Rechte** aufgeführt.
2.  Geben Sie eine Datei an, die Sie lesen möchten, indem Sie [**iwmsyncreader:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-open)aufrufen.

Der synchrone Reader unterstützt auch die Verwendung der **IStream** -com-Schnittstelle zum Öffnen von Dateien. Sie können die **IStream** -Schnittstelle beliebig implementieren. Nachdem die gewünschte Datei in **IStream** geöffnet wurde, können Sie die oben aufgeführten Schritte ausführen, mit dem Unterschied, dass Sie in Schritt 2 iwmsynkreader:: [**OpenStream**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmsyncreader-openstream) anstelle von **iwmsynanader:: Open** aufrufen müssen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Iwmsynkreader-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[**Lesen von Dateien mit dem synchronen Reader**](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




