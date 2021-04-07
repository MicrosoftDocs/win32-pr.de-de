---
title: Speichern von Inhalt
description: Speichern von Inhalt
ms.assetid: 22f4e580-43a4-48b5-8eb3-90e1346a1093
keywords:
- Windows Media-Format-SDK, Speichern von Inhalten
- Windows Media-Format-SDK, schnelles Cache Streaming
- Advanced Systems Format (ASF), Speichern von Inhalten
- ASF (Advanced Systems Format), Speichern von Inhalten
- Advanced Systems Format (ASF), schnelles Cache Streaming
- ASF (Advanced Systems Format), schnelles Cache Streaming
- Streams, Speichern von Inhalten
- Schnelles Cache Streaming, Speichern von Inhalten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba6c215a81accef29f8943ed52ca24264f785d94
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2020
ms.locfileid: "103724083"
---
# <a name="saving-content"></a>Speichern von Inhalt

Mithilfe dieses SDK kann eine Anwendung heruntergeladenen oder gestreamt-Inhalt auf dem lokalen Computer des Benutzers speichern, indem die [**IWMReaderAdvanced2:: savefileas**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-savefileas) -Methode für das Reader-Objekt aufgerufen wird. Für gestreamt-Inhalte muss der Server schnelles Cache Streaming verwenden, das im Abschnitt [Aktivieren von schnellem Cache Streaming vom Client](enabling-fast-cache-streaming-from-the-client.md)beschrieben wird. Für gestreamt-Inhalte erstellt die **savefileas** -Methode eine ASX-Datei, die auf eine ASF-Datei verweist, die den gespeicherten Inhalt enthält. Wenn das Reader-Objekt eine serverseitige Wiedergabeliste gestreamt, wird jeder Eintrag als separate ASF-Datei gespeichert, und die Datei "ASX" verweist auf jede der ASF-Dateien. Für heruntergeladene Inhalte erstellt die **savefileas** -Methode einfach eine ASF-Datei.

Gehen Sie folgendermaßen vor, um Inhalt in einer lokalen Datei zu speichern:

1.  Nennen Sie [**iwmreader:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) mit der URL. **Open** ist ein asynchroner-Rückruf, und wird sofort zurückgegeben. Warten Sie, bis der Vorgang beendet wurde, wie in so [Erstellen Sie einen Reader und Öffnen einer Datei](to-create-a-reader-and-open-a-file.md)beschrieben.
2.  Fragen Sie das Reader-Objekt für die [**IWMReaderAdvanced4**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced4) -Schnittstelle ab.
3.  Überprüfen Sie, ob der Inhalt durch Aufrufen der [**IWMReaderAdvanced4:: cansavefileas**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced4-cansavefileas) -Methode gespeichert werden kann. Wenn die Methode false zurückgibt, kann der Inhalt nicht lokal gespeichert werden. Fahren Sie andernfalls mit Schritt 4 fort.
4.  Aufrufen der [**IWMReaderAdvanced4:: isusingfastcache**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced4-isusingfastcache) -Methode, um zu bestimmen, ob der Server schnelles Cache Streaming verwendet.
5.  Nennen Sie die Datei " [**IWMReaderAdvanced2:: savefileas**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-savefileas) " mit einem Dateinamen für die lokale Datei. Wenn die **isusingfastcache** -Methode "true" zurückgegeben hat, benennen Sie die Datei mit der Erweiterung ". asx". Andernfalls sollten Sie dem Dateinamen die Erweiterung. ASF,. WMA oder. wmv übergeben.

Die Anwendung kann den Speichervorgang abbrechen, während Sie ausgeführt wird, indem die [**IWMReaderAdvanced4:: cancelsavefileas**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced4-cancelsavefileas) -Methode aufgerufen wird.

Der gespeicherte Inhalt ist möglicherweise mit DRM geschützt, sodass es möglicherweise nicht möglich ist, die Datei auf einem anderen Computer wiederzugeben. Weitere Informationen zum Schutz von Inhalten finden Sie unter [Funktionen für digitale Rights Management](digital-rights-management-features.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Iwmreader-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[**IWMReaderAdvanced2-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2)
</dt> </dl>

 

 




