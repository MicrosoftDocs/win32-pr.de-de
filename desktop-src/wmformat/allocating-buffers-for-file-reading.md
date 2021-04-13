---
title: Puffer für Datei Lesevorgänge werden zugewiesen.
description: Puffer für Datei Lesevorgänge werden zugewiesen.
ms.assetid: da66ef5b-ec92-445c-90ba-5ee89e0def36
keywords:
- Windows Media-Format-SDK, Lesen von ASF-Dateien
- Advanced Systems Format (ASF), Lesen von Dateien
- ASF (Advanced Systems Format), Lesen von Dateien
- Windows Media-Format-SDK, Zuordnen von Puffern
- Advanced Systems Format (ASF), Zuordnen von Puffern
- ASF (Advanced Systems Format), Zuordnen von Puffern
- Advanced Systems Format (ASF), Puffer Zuordnung
- ASF (Advanced Systems Format), Puffer Zuordnung
- Puffer Zuordnung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecdf9ba0a333bbe25c94ec087911237b68f38f74
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104389832"
---
# <a name="allocating-buffers-for-file-reading"></a>Puffer für Datei Lesevorgänge werden zugewiesen.

Im grundlegendsten Datei Lese Szenario werden die Puffer, die zum Übermitteln von Beispielen verwendet werden, vom Lese Objekt (dem Reader-Objekt oder dem synchronen Reader-Objekt) zugeordnet. Sie können Puffer jedoch selbst zuweisen. Weitere Informationen zu den Vorteilen der Zuordnung eigener Puffer finden Sie unter vom [Benutzer zugewiesene Beispiel Unterstützung](user-allocated-sample-support.md).

Führen Sie die folgenden Schritte aus, um Ihre eigenen Puffer zum Lesen von Dateien zu verwenden.

1.  Implementieren Sie einen Rückruf oder Rückrufe, die der Reader aufrufen soll, wenn er einen Puffer benötigt. Wenn Sie Ausgabe Beispiele lesen, verwenden Sie [**iwmreaderindecatorex:: depcateforoutputex**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderallocatorex-allocateforoutputex). Wenn Sie streambeispiele lesen, verwenden Sie " [**iwmreaderdepcatorex:: depcateforstreamex**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderallocatorex-allocateforstreamex)". Fügen Sie die Logik zum Verwalten von Puffern ein, die für Ihre Anwendung geeignet
2.  Weisen Sie einen Pufferpool zu, den Sie für das Lesen von Dateien verwenden werden.
    -   Suchen Sie die Größe, die für die Puffer erforderlich ist, indem Sie für jede Ausgabe und/oder jeden Stream, für die der Puffer verwendet wird, [**iwmreaderadvanced:: getmaxoutputsamplesize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getmaxoutputsamplesize) oder [**iwmreaderadvanced:: getmaxstreamsamplesize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getmaxstreamsamplesize) aufrufen. Wenn Sie den synchronen Reader verwenden, verwenden Sie stattdessen [**iwmsynkreader:: getmaxoutputsamplesize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getmaxoutputsamplesize) oder [**iwmsynkreader:: getmaxstreamsamplesize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getmaxstreamsamplesize) .
    -   Erstellen Sie jeden Puffer für den Pool.
3.  Einrichten des Readers oder des synchronen Readers zum Lesen. Weitere Informationen finden Sie unter [Lesen von Dateien mit dem asynchronen Reader](reading-files-with-the-asynchronous-reader.md) oder [Lesen von Dateien mit dem synchronen Reader](reading-files-with-the-synchronous-reader.md).
4.  Bevor Sie mit dem Schreiben beginnen, nennen Sie [**iwmreaderadvanced:: setallocateforoutput**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setallocateforoutput) oder [**iwmreaderadvanced:: setallocateforstream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setallocateforstream) für jede Ausgabe und jeden Datenstrom, für den Sie Puffer mithilfe des Reader-Objekts zuordnen. Für den synchronen Reader müssen Sie stattdessen [**IWMSyncReader2:: Log-locateforoutput**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader2-setallocateforoutput) bzw. [**IWMSyncReader2:: abslocateforstream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader2-setallocateforstream) abrufen.
5.  Beginnen Sie mit dem Lesen der Datei.

Das Lese Objekt ruft den entsprechenden zuordnerrückruf auf und ruft Beispiele von Ihrer Anwendung ab. Ihre Puffer Verwaltungs Logik muss eine Möglichkeit enthalten, um zu signalisieren, dass ein Puffer frei verwendet werden kann. In der Regel wird ein Puffer wieder im Pool abgelegt, wenn sein Inhalt gerendert wird. Abhängig von Ihrer Anwendung benötigen Sie möglicherweise nur wenige Puffer im Pool oder viele.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Lesen von ASF-Dateien**](reading-asf-files.md)
</dt> </dl>

 

 




