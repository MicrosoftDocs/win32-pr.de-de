---
title: Unterstützung mehrerer Sprachen
description: Unterstützung mehrerer Sprachen
ms.assetid: b0061de4-d725-455f-9d9b-5bd0dbe8ff53
keywords:
- Windows Medienformat-SDK, unterstützt mehrere Sprachen
- Windows Medienformat-SDK, Unterstützung mehrerer Sprachen
- Windows Medienformat-SDK, Sprachunterstützung
- Advanced Systems Format (ASF) mit Unterstützung mehrerer Sprachen
- ASF (Advanced Systems Format), unterstützung mehrerer Sprachen
- Advanced Systems Format (ASF), Unterstützung mehrerer Sprachen
- ASF (Advanced Systems Format), Unterstützung mehrerer Sprachen
- Advanced Systems Format (ASF), Sprachunterstützung
- ASF (Advanced Systems Format), Sprachunterstützung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa610d5a9b0c92fb205ecdc234a18d816190223b5bca843a542e7222695fa24f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118699101"
---
# <a name="to-support-multiple-languages"></a>Unterstützung mehrerer Sprachen

Sie können mehrere Sprachen sowohl in Streams als auch in Metadaten unterstützen. Der Kern der Unterstützung mehrerer Sprachen im Windows Media Format SDK ist die [**IWMLanguageList-Schnittstelle,**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlanguagelist) die eine Liste der unterstützten Sprachen verwaltet. Die Sprachliste gibt jeder unterstützten Sprache einen Index, der in verschiedenen Objekten im SDK verwendet wird, wenn es um die verschiedenen Sprachen geht.

Die [**IWMLanguageList::AddLanguageByRFC1766String-Methode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlanguagelist-addlanguagebyrfc1766string) fügt der Liste eine Sprache hinzu. Sie können die bereits in der Liste enthaltenen Sprachen ermitteln, indem Sie die Gesamtzahl der Sprachen mit [**IWMLanguageList::GetLanguageCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlanguagelist-getlanguagecount) abrufen und dann die Sprachen durchlaufen, die jeweils [**IWMLanguageList::GetLanguageDetails**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlanguagelist-getlanguagedetails) aufrufen. Der Sprachindex basiert auf 0 (null).

## <a name="to-configure-mutual-exclusion-by-language"></a>So konfigurieren Sie gegenseitigen Ausschluss nach Sprache

Das Konfigurieren eines einfachen gegenseitigen Ausschlussobjekts nach Sprache ist sehr einfach. Jeder Stream ist jetzt einer Sprache zugeordnet. Die einem Stream zugeordnete Sprache kann mithilfe von [**IWMStreamConfig3::SetLanguage**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig3-setlanguage)festgelegt werden. Nachdem alle sich gegenseitig ausschließenden Datenströme konfiguriert wurden, erstellen Sie einfach ein objekt für gegenseitigen Ausschluss wie bei jedem anderen Typ. Rufen Sie dann [**IWMMutualExclusion::SetType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-settype) auf, und übergeben Sie die CLSID \_ WMMUTEX-Sprache \_ für den Typ.

Streams, die sich durch die Sprache gegenseitig ausschließen, werden komplizierter, wenn sich die exklusiven Datenströme auch durch die Bitrate gegenseitig ausschließen. In diesem Fall müssen Sie sich gegenseitig ausschließende Datensätze verwenden, indem Sie die folgenden Schritte ausführen:

1.  Erstellen Sie ein objekt für gegenseitigen Ausschluss für die Datenströme unterschiedlicher Bitraten in jeder Sprache. Weitere Informationen zum Erstellen eines gegenseitigen Ausschlussobjekts nach Bitrate finden Sie unter [Using Multiple Bit Rate Mutual Exclusion](using-multiple-bit-rate-mutual-exclusion.md).
2.  Erstellen Sie ein objekt für gegenseitigen Ausschluss. Rufen Sie [**IWMMutualExclusion::SetType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-settype) auf, und übergeben Sie CLSID \_ WMMUTEX \_ Language, um Dies nach Sprache anzugeben.
3.  Rufen Sie einen Zeiger auf die [**IWMMutualExclusion2-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion2) des in Schritt 2 erstellten gegenseitigen Ausschlussobjekts ab, indem Sie die **QueryInterface-Methode** von [**IWMMutualExclusion**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion)aufrufen.
4.  Rufen Sie die [**IWMMutualExclusion2::AddRecord-Methode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion2-addrecord) einmal für jede Sprache auf, um Datenstromdatensätze zu erstellen, die sich gegenseitig ausschließen.
5.  Fügen Sie für jeden in Schritt 4 erstellten Datensatz die Streams der entsprechenden Sprache mit Aufrufen von [**IWMMutualExclusion2::AddStreamForRecord**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion2-addstreamforrecord)hinzu.

## <a name="to-read-files-with-multiple-languages"></a>So lesen Sie Dateien mit mehreren Sprachen

Das Readerobjekt stellt Methoden zum Identifizieren der verfügbaren Sprachen von Streams in einer Datei bereit. Sie können die Anzahl der unterstützten Sprachen für eine Ausgabe abrufen, indem Sie [**IWMReaderAdvanced4::GetLanguageCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced4-getlanguagecount)aufrufen. Sie können dann details zu jeder Sprache mit Aufrufen von [**IWMReaderAdvanced4::GetLanguage**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced4-getlanguage)abrufen.

Sie können die zu spielende Sprache angeben, indem Sie den Index dieser Sprache mit einem Aufruf von [**IWMReaderAdvanced2::SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting)an den Reader übergeben. Dadurch wird die angegebene Sprache ausgewählt, während die automatische Streamauswahl für alle anderen objekte für gegenseitigen Ausschluss in der Datei beibehalten wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Weiterführende Themen**](advanced-topics.md)
</dt> <dt>

[**IWMLanguageList-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlanguagelist)
</dt> <dt>

[**IWMMutualExclusion-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion)
</dt> <dt>

[**IWMMutualExclusion2-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion2)
</dt> <dt>

[**IWMReaderAdvanced2-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2)
</dt> <dt>

[**IWMReaderAdvanced4-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced4)
</dt> <dt>

[**IWMStreamConfig3-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig3)
</dt> </dl>

 

 




