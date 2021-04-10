---
title: Eigenschaften Objekt für Ausgabemedien
description: Eigenschaften Objekt für Ausgabemedien
ms.assetid: 96fa7c66-59a0-4eb3-ace4-a827b139f978
keywords:
- Windows Media-Format-SDK, Objekte für Ausgabemedien Eigenschaften
- Advanced Systems Format (ASF), Ausgabemedien Eigenschaften Objekte
- ASF (Advanced Systems Format), Ausgabemedien Eigenschaften Objekte
- Objekte, Objekte für Ausgabemedien Eigenschaften
- Objekte der Ausgabemedien Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61490464381a0b4e58be7994dfaeb0dfec2baa76
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2020
ms.locfileid: "104038686"
---
# <a name="output-media-properties-object"></a>Eigenschaften Objekt für Ausgabemedien

Ein Ausgabemedien-Eigenschaften Objekt wird verwendet, um eine Ausgabe Eigenschaft abzurufen und festzulegen. Ausgabemedien Eigenschaften Objekte werden für unterstützte Ausgabeformate von Streams in einer Datei erstellt, die in ein Reader-Objekt geladen wird. Bei komprimierten Datenströmen werden die Ausgabe Eigenschaften durch die möglichen Ausgaben des Dekomprimierungs Codecs bestimmt.

Ein Ausgabemedien-Eigenschaften Objekt wird von [**iwmreader:: getOutputProperties**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputprops) erstellt. diese Methode erstellt ein Ausgabemedien-Eigenschaften Objekt, das die Eigenschaften des Standardausgabe Formats enthält. Andere Formate können für eine Ausgabe unterstützt werden. Zum Abrufen zusätzlicher Ausgabeformate können Sie [**iwmreader:: getoutputformatcount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformatcount) aufrufen, um die Anzahl der unterstützten Ausgabeformate abzurufen und Sie dann mithilfe von Aufrufen von [**iwmreader:: getoutputformat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformat)durchlaufen zu lassen. **Getoutputformat** erstellt ein Ausgabemedien Eigenschaften-Objekt, das mit den Daten für das ausgewählte Ausgabeformat aufgefüllt ist.

Objekte der Ausgabemedien Eigenschaften können auch mit dem synchronen Reader erstellt werden. Alle Methodennamen sind identisch mit denen im Reader und werden alle von der [**iwmsynkreader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader) -Schnittstelle verfügbar gemacht.

" **GetOutput-** Eigenschaften" und " **getoutputformat** " legen einen Zeiger auf eine [**iwmoutputmediarequicschnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops) fest. Die anderen Schnittstellen des Eigenschaften Objekts der Ausgabemedien können durch Aufrufen der **QueryInterface** -Methode abgerufen werden.

Die folgenden Schnittstellen werden von allen Ausgabemedien-Eigenschaften Objekten unterstützt.



| Schnittstelle                                          | BESCHREIBUNG                                                                                                |
|----------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [**Iwmmedia-Eigenschaften**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops)             | Wird als Basisschnittstelle für die anderen Schnittstellen der Medien Eigenschaft verwendet (Eingabe, Ausgabe und Video).             |
| [**Iwmoutputmedia-Eigenschaften**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops) | Ruft die Eigenschaften einer Ausgabe ab.                                                                     |
| [**Iwmvideomedia-Eigenschaften**](/previous-versions/windows/desktop/api/Wmsdkidl/nn-wmsdkidl-iwmvideomediaprops)   | Verwaltet die Eigenschaften eines Videostreams. Dies ist eine optionale Schnittstelle, die nur für Videostreams verfügbar ist. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Objekte**](objects.md)
</dt> <dt>

[**Reader-Objekt**](reader-object.md)
</dt> </dl>

 

 




