---
title: So erstellen Sie einen Reader und öffnen eine Datei
description: So erstellen Sie einen Reader und öffnen eine Datei
ms.assetid: 82b194d6-7cb7-4b88-9ed7-944b8b43bc29
keywords:
- Advanced Systems Format (ASF), Erstellen von Lesern
- ASF (Advanced Systems Format), Erstellen von Lesern
- Advanced Systems Format (ASF), Öffnen von Dateien
- ASF (Advanced Systems Format), Öffnen von Dateien
- asynchrone Leser, erstellen
- asynchrone Leser, Öffnen von Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8e714f51b56a7d9f3b18a774cd3b8c74bf05352
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2020
ms.locfileid: "103724091"
---
# <a name="to-create-a-reader-and-open-a-file"></a>So erstellen Sie einen Reader und öffnen eine Datei

Bevor Sie mit dem Reader arbeiten können, müssen Sie ein Reader-Objekt erstellen und eine Datei zum Lesen laden. Führen Sie die folgenden Schritte aus, um den Reader zu initialisieren und eine Datei zu öffnen.

1.  Erstellen Sie ein Reader-Objekt, indem Sie die [**wmcreatereader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatereader) -Funktion aufrufen. Sie müssen die gewünschte Ebene der Rechteverwaltung für das neue Reader-Objekt angeben. Die verfügbaren Modi sind im Enumerationstyp [**WMT- \_ Rechte**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_rights) aufgeführt.
2.  Geben Sie eine zu lesende Datei an, indem Sie [**iwmreader:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open)aufrufen. Sie müssen eine Reader-Rückruf Schnittstelle angeben, die der Reader verwenden soll. Weitere Informationen zum readerrückruf finden [Sie unter So implementieren Sie Reader-Meldungen im OnStatus-Rückruf](to-implement-reader-messages-in-the-onstatus-callback.md).
3.  Warten Sie, bis der Reader die Datei öffnet. Wenn Sie **Öffnen** zum Laden einer Datei aufzurufen, wird fast sofort zurückgegeben und die Verarbeitung in einem anderen Thread fortgesetzt. Sie sollten auf den Abschluss von Vorgängen warten, indem Sie ein Ereignis signalisieren, wenn der **OnStatus** -Rückruf die geöffnete WMT- \_ Statusmeldung empfängt.

Der Reader unterstützt auch die Verwendung der **IStream** -com-Schnittstelle zum Öffnen von Dateien. Sie können die **IStream** -Schnittstelle beliebig implementieren. Nachdem die gewünschte Datei in **IStream** geöffnet wurde, können Sie die oben aufgeführten Schritte ausführen, mit dem Unterschied, dass Sie [**IWMReaderAdvanced2:: OpenStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-openstream) anstelle von **iwmreader:: Open** in Schritt 2 aufgerufen haben müssen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Iwmreader-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[**IWMReaderAdvanced2-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2)
</dt> <dt>

[**Iwmstatus Callback-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback)
</dt> <dt>

[**Lesen von Dateien mit dem asynchronen Reader**](reading-files-with-the-asynchronous-reader.md)
</dt> <dt>

[**Verwenden der Rückruf Methoden**](using-the-callback-methods.md)
</dt> </dl>

 

 




