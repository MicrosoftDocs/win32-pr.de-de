---
title: Attribut Bereichs Abruf
description: Ein mehr wertiges Attribut kann fast eine beliebige Anzahl von Werten aufweisen. In vielen Fällen kann es vorteilhaft oder sogar notwendig sein, den Wertebereich einzuschränken, der von einer Abfrage abgerufen wird.
ms.assetid: 3a0eb764-fca9-4ca6-9991-b85f293961af
ms.tgt_platform: multiple
keywords:
- Attribut Bereichs Abruf ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47f8787eb0b2aba30d1926b4d9cbb7e566e0f59c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947359"
---
# <a name="attribute-range-retrieval"></a>Attribut Bereichs Abruf

Ein mehr wertiges Attribut kann fast eine beliebige Anzahl von Werten aufweisen. In vielen Fällen kann es vorteilhaft oder sogar notwendig sein, den Wertebereich einzuschränken, der von einer Abfrage abgerufen wird.

Der Bereichs Abruf umfasst das Anfordern einer begrenzten Anzahl von Attributwerten in einer einzelnen Abfrage. Die Anzahl der angeforderten Werte muss kleiner oder gleich der maximalen Anzahl von Werten sein, die vom Server unterstützt werden. Um die Häufigkeit zu verringern, mit der die Abfrage den Server kontaktieren muss, sollte die Anzahl der angeforderten Werte so nah wie möglich an diesem Maximum liegen. Damit eine Anwendung ordnungsgemäß mit allen Windows-Servern funktioniert, sollte eine maximale Anzahl von 1000 verwendet werden.

Die bereichsspezifier für eine Eigenschaften Abfrage muss folgende Form haben:


```C++
range=<low range>-<high range>
```



dabei &lt; ist "Low Range &gt; " der null basierte Index des ersten Eigenschafts Werts, der abgerufen werden soll, und " &lt; High Range &gt; " ist der null basierte Index des letzten Eigenschafts Werts, der abgerufen werden soll. NULL wird für " &lt; niedriger Bereich &gt; " verwendet, um den ersten Eintrag anzugeben. Das Platzhalter Zeichen ( \* ) kann für " &lt; High Range" verwendet werden &gt; , um alle verbleibenden Einträge anzugeben.

In der folgenden Tabelle sind Beispiele für Bereichs Bearbeiter aufgeführt.



| Beispiel      | BESCHREIBUNG                                                                                   |
|--------------|-----------------------------------------------------------------------------------------------|
| Bereich = 0-\*   | Ruft alle Eigenschaftswerte ab. Dies unterliegt den vom Server vorgegebenen Grenzwerten.                |
| Bereich = 0-500  | Abrufen von 1. bis 501st-Werten.                                                |
| Bereich = 2-3    | Abrufen von 3-und 4-Werten.                                                                  |
| Bereich = 501-\* | Rufen Sie das 502nd und alle verbleibenden Werte ab. Dies unterliegt den vom Server vorgegebenen Grenzwerten. |



 

Es gibt verschiedene Möglichkeiten zum Abrufen eines Bereichs von Eigenschafts Werten. Die [**IADs. GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) -Methode kann entweder in einer Automatisierungs Sprache oder in C++ verwendet werden. Die **IADs. GetInfoEx** -Methode ist die bevorzugte Methode zur Durchführung des Bereichs Abrufs. Weitere Informationen zur Verwendung von **IADs. GetInfoEx** für den Bereichs Abruf finden Sie unter [using IADs:: GetInfoEx for Range Abruf](using-iads--getinfoex-for-range-retrieval.md).

Wenn eine Automatisierungs Sprache verwendet wird, können die ActiveX-Verzeichnisobjekte (ADO) zum Abrufen eines Bereichs von Eigenschafts Werten verwendet werden. Weitere Informationen zur Verwendung von ADO für den Bereichs Abruf finden Sie unter [Verwenden von ADO für den Bereichs Abruf](using-ado-for-range-retrieval.md).

Wenn C++ verwendet wird, können die Schnittstellen [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) und [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) zum Abrufen eines Bereichs von Eigenschafts Werten verwendet werden. Weitere Informationen zur Verwendung von **IDirectorySearch** und **IDirectoryObject** für den Bereichs Abruf finden [Sie unter Verwenden von IDirectorySearch und IDirectoryObject für den Bereichs Abruf](using-idirectorysearch-and-idirectoryobject-for-range-retrieval.md).

 

 




