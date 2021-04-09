---
title: Unterstützung mehrerer Sprachen
description: Unterstützung mehrerer Sprachen
ms.assetid: b0061de4-d725-455f-9d9b-5bd0dbe8ff53
keywords:
- Windows Media-Format-SDK, Unterstützung für mehrere Sprachen
- Windows Media-Format-SDK, Unterstützung mehrerer Sprachen
- Windows Media-Format-SDK, Sprachunterstützung
- Advanced Systems Format (ASF), Unterstützung für mehrere Sprachen
- ASF (Advanced Systems Format), Unterstützung mehrerer Sprachen
- Advanced Systems Format (ASF), Unterstützung mehrerer Sprachen
- ASF (Advanced Systems Format), Unterstützung mehrerer Sprachen
- Advanced Systems Format (ASF), Sprachunterstützung
- ASF (Advanced Systems Format), Sprachunterstützung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bc070bda1cc25c6b7fd0fa583a8ac63a55fa603
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2020
ms.locfileid: "103948508"
---
# <a name="to-support-multiple-languages"></a>Unterstützung mehrerer Sprachen

Sie können mehrere Sprachen in Streams und Metadaten unterstützen. Der Kern der Unterstützung mehrerer Sprachen im Windows Media-Format-SDK ist die [**iwmlanguagelist**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlanguagelist) -Schnittstelle, die eine Liste der unterstützten Sprachen verwaltet. Die Sprachliste gibt jeder unterstützten Sprache einen Index, der in verschiedenen Objekten im SDK verwendet wird, wenn mehrere Sprachen verwendet werden.

Die [**iwmlanguagelist:: AddLanguageByRFC1766String**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlanguagelist-addlanguagebyrfc1766string) -Methode fügt der Liste eine Sprache hinzu. Sie können die Sprachen, die sich bereits in der Liste befinden, ermitteln, indem Sie die Gesamtzahl der Sprachen mit [**iwmlanguagelist:: getlanguagecount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlanguagelist-getlanguagecount) abrufen und dann die Sprachen, die [**iwmlanguagelist:: getlanguagedetails**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlanguagelist-getlanguagedetails) aufrufen, durchlaufen. Der sprach Index ist NULL basiert.

## <a name="to-configure-mutual-exclusion-by-language"></a>So konfigurieren Sie den gegenseitigen Ausschluss nach Sprache

Das Konfigurieren eines einfachen gegenseitigen Ausschluss Objekts nach Sprache ist sehr einfach. Jeder Stream ist nun einer Sprache zugeordnet. Die einem Stream zugeordnete Sprache kann mithilfe von [**IWMStreamConfig3:: setLanguage**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig3-setlanguage)festgelegt werden. Nachdem alle sich gegenseitig ausschließenden Streams konfiguriert wurden, erstellen Sie einfach ein gegenseitiges Ausschluss Objekt, wie es bei jedem anderen Typ der Fall wäre. Rufen Sie dann [**iwmmutualexclusion:: settype**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-settype) auf, und übergeben Sie die CLSID- \_ wmmutex- \_ Sprache für den-Typ.

Datenströme, die sich gegenseitig ausschließen, werden komplizierter, wenn die exklusiven Streams auch durch die Bitrate gegenseitig ausschließen. In diesem Fall müssen Sie die folgenden Schritte ausführen, um sich gegenseitig ausschließende Datensätze zu verwenden:

1.  Erstellen Sie ein gegenseitiges Ausschluss Objekt für die Streams unterschiedlicher Bitraten in jeder Sprache. Weitere Informationen zum Erstellen eines gegenseitigen Ausschluss Objekts per Bitrate finden [Sie unter Verwenden des gegenseitigen Ausschlusses mehrerer Bitrate](using-multiple-bit-rate-mutual-exclusion.md).
2.  Erstellen Sie ein gegenseitiges Ausschluss Objekt. Rufen Sie [**iwmmutualexclusion:: settype**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-settype) auf, und übergeben Sie die CLSID- \_ wmmutex- \_ Sprache, um die Exklusivität nach Sprache anzugeben.
3.  Rufen Sie einen Zeiger auf die [**IWMMutualExclusion2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion2) -Schnittstelle des gegenseitigen Ausschluss Objekts ab, das in Schritt 2 durch Aufrufen der **QueryInterface** -Methode von [**iwmmutualexclusion**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion)erstellt wurde.
4.  Rufen Sie die [**IWMMutualExclusion2:: addRecord**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion2-addrecord) -Methode einmal für jede Sprache auf, um Stream-Datensätze zu erstellen, die sich gegenseitig ausschließen.
5.  Fügen Sie für jeden Datensatz, der in Schritt 4 erstellt wurde, die Streams der entsprechenden Sprache mit Aufrufen von [**IWMMutualExclusion2:: addstreamforrecord**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion2-addstreamforrecord)hinzu.

## <a name="to-read-files-with-multiple-languages"></a>So lesen Sie Dateien mit mehreren Sprachen

Das Reader-Objekt stellt Methoden bereit, um die verfügbaren Sprachen von Streams in einer Datei zu identifizieren. Sie können die Anzahl der unterstützten Sprachen für eine Ausgabe abrufen, indem Sie [**IWMReaderAdvanced4:: getlanguagecount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced4-getlanguagecount)aufrufen. Anschließend können Sie Details zu jeder Sprache mit Aufrufen von [**IWMReaderAdvanced4:: GetLanguage**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced4-getlanguage)abrufen.

Sie können die zu Wiedergabe Ende Sprache angeben, indem Sie den Index dieser Sprache mit einem Aufrufen von [**IWMReaderAdvanced2:: setoutputsetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting)an den Reader übergeben. Dadurch wird die angegebene Sprache ausgewählt, während die automatische Datenstrom Auswahl für alle anderen gegenseitigen Ausschluss Objekte in der Datei beibehalten wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Erweiterte Themen**](advanced-topics.md)
</dt> <dt>

[**Iwmlanguagelist-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlanguagelist)
</dt> <dt>

[**Iwmmutualexclusion-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion)
</dt> <dt>

[**IWMMutualExclusion2-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion2)
</dt> <dt>

[**IWMReaderAdvanced2-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2)
</dt> <dt>

[**IWMReaderAdvanced4-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced4)
</dt> <dt>

[**IWMStreamConfig3-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig3)
</dt> </dl>

 

 




