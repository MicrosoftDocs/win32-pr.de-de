---
title: Ausgabemedieneigenschaften-Objekt
description: Ausgabemedieneigenschaften-Objekt
ms.assetid: 96fa7c66-59a0-4eb3-ace4-a827b139f978
keywords:
- Windows Medienformat-SDK, Ausgabemedieneigenschaftenobjekte
- Advanced Systems Format (ASF), Ausgabemedieneigenschaftenobjekte
- ASF (Advanced Systems Format), Ausgabemedieneigenschaftenobjekte
- Objekte,Ausgabemedieneigenschaftenobjekte
- Ausgabemedieneigenschaftenobjekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6848270147a1a191faf93830f062cf7768a19ccd38a77598d15617197a1967a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119084632"
---
# <a name="output-media-properties-object"></a>Ausgabemedieneigenschaften-Objekt

Ein Ausgabemedieneigenschaftenobjekt wird verwendet, um eine Ausgabeeigenschaft abzurufen und zu festlegen. Ausgabemedieneigenschaftenobjekte werden für unterstützte Ausgabeformate von Streams in einer Datei erstellt, die in ein Readerobjekt geladen wird. Bei komprimierten Streams werden die Ausgabeeigenschaften durch die möglichen Ausgaben des dekomprimierten Codecs bestimmt.

Ein Ausgabemedieneigenschaftenobjekt wird von [**IWMReader::GetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputprops) erstellt. Diese Methode erstellt ein Ausgabemedieneigenschaftenobjekt, das die Eigenschaften des Standardausgabeformats enthält. Andere Formate können für eine Ausgabe unterstützt werden. Um zusätzliche Ausgabeformate zu erhalten, können Sie [**IWMReader::GetOutputFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformatcount) aufrufen, um die Anzahl der unterstützten Ausgabeformate zu erhalten, und diese dann mithilfe von Aufrufen von [**IWMReader::GetOutputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformat)durchschleifen. **GetOutputFormat erstellt** ein Ausgabemedieneigenschaftenobjekt, das mit den Daten für das ausgewählte Ausgabeformat aufgefüllt wird.

Ausgabemedieneigenschaftenobjekte können auch mit dem synchronen Reader erstellt werden. Alle Methodennamen sind mit denen im Reader identisch und werden alle von der [**IWMSyncReader-Schnittstelle verfügbar**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader) gemacht.

**GetOutputProps und** **GetOutputFormat** legen einen Zeiger auf eine [**IWMOutputMediaProps-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops) fest. Die anderen Schnittstellen des Ausgabemedieneigenschaftenobjekts können durch Aufrufen der **QueryInterface-Methode ermittelt** werden.

Die folgenden Schnittstellen werden von jedem Ausgabemedieneigenschaftenobjekt unterstützt.



| Schnittstelle                                          | BESCHREIBUNG                                                                                                |
|----------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [**IWMMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops)             | Wird als Basisschnittstelle für die anderen Medieneigenschaftsschnittstellen (Eingabe, Ausgabe und Video) verwendet.             |
| [**IWMOutputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops) | Ruft die Eigenschaften einer Ausgabe ab.                                                                     |
| [**IWMVideoMediaProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nn-wmsdkidl-iwmvideomediaprops)   | Verwaltet die Eigenschaften eines Videostreams. Dies ist eine optionale Schnittstelle, die nur für Videostreams verfügbar ist. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Objekte**](objects.md)
</dt> <dt>

[**Reader-Objekt**](reader-object.md)
</dt> </dl>

 

 




