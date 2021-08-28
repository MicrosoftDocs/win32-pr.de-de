---
title: So erstellen Sie einen synchronen Reader und öffnen eine Datei
description: So erstellen Sie einen synchronen Reader und öffnen eine Datei
ms.assetid: 6349d05e-20db-4ce8-83fd-cad4cec666f2
keywords:
- Advanced Systems Format (ASF), Erstellen von Readern
- ASF (Advanced Systems Format), Erstellen von Readern
- Advanced Systems Format (ASF), Öffnen von Dateien
- ASF (Advanced Systems Format), Öffnen von Dateien
- Synchrone Reader,erstellen
- Synchrone Reader,Öffnen von Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52d1c6897c05bb0d843e5818f078df5235a5afac4a485d6a719ab86b8e4f8267
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807650"
---
# <a name="to-create-a-synchronous-reader-and-open-a-file"></a>So erstellen Sie einen synchronen Reader und öffnen eine Datei

Bevor Sie mit dem synchronen Reader arbeiten können, müssen Sie ein synchrones Readerobjekt erstellen und eine Datei zum Lesen laden. Führen Sie die folgenden Schritte aus, um den synchronen Reader zu initialisieren und eine Datei zu öffnen.

1.  Erstellen Sie ein synchrones Readerobjekt, indem Sie die [**WMCreateSyncReader-Funktion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatesyncreader) aufrufen. Sie müssen die gewünschte Rechteverwaltungsebene für das neue Readerobjekt angeben. Die verfügbaren Modi sind im **WMT \_ RIGHTS-Enumerationstyp** aufgeführt.
2.  Geben Sie eine zu lesende Datei an, indem [**Sie IWMSyncReader::Open aufrufen.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-open)

Der synchrone Reader unterstützt auch die Verwendung der **IStream** COM-Schnittstelle zum Öffnen von Dateien. Sie können die **IStream-Schnittstelle** auf beliebige Weise implementieren. Nachdem die gewünschte Datei in **IStream** geöffnet wurde, können Sie die oben aufgeführten Schritte ausführen, außer dass [**Sie IWMSyncReader::OpenStream**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmsyncreader-openstream) anstelle von **IWMSyncReader::Open** in Schritt 2 aufrufen müssen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IWMSyncReader-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[**Lesen von Dateien mit dem synchronen Reader**](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




