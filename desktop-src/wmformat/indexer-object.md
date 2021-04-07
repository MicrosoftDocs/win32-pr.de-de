---
title: Indexer-Objekt
description: Indexer-Objekt
ms.assetid: 652e04a5-ed6e-4e92-acf4-55ed82f77ef1
keywords:
- Windows Media-Format-SDK, Indexer-Objekte
- Advanced Systems Format (ASF), Indexer-Objekte
- ASF (Advanced Systems Format), Indexer-Objekte
- Objekte, Indexer-Objekte
- Indexer-Objekte
- Indizes, Indexer-Objekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71c9aa8c1c3ff694ae8e125e17dc0190451c7f21
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/21/2020
ms.locfileid: "104038667"
---
# <a name="indexer-object"></a>Indexer-Objekt

Das Indexer-Objekt erstellt einen Index in einer ASF-Datei. Ein Index ist ein Standard Teil einer ASF-Datei, der Videobeispiele mit Uhrzeiten, Frame Nummern oder (falls zutreffend) Struktur von Bewegungsbild-und Fernseh Technikern (SMPTE) Standardzeit Stempeln zuweist. Ohne einen Index kann weder das Reader-Objekt noch das synchrone Reader-Objekt zu einem Punkt in der Mitte einer Datei suchen.

Indizes, die von diesem-Objekt erstellt wurden, sind nur erforderlich, wenn die Datei mindestens einen Videostream enthält. Dies liegt daran, dass Audiodaten nicht temporlig komprimiert werden, sodass eine bestimmte Uhrzeit in einem Audiostream leicht zu finden ist.

Das Indexer-Objekt wird von der [**wmkreateindexer**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateindexer) -Funktion erstellt, mit der ein Zeiger auf eine **iwmindexer** -Schnittstelle festgelegt wird. Die anderen Schnittstellen des Indexer-Objekts können durch Aufrufen der **QueryInterface** -Methode abgerufen werden.

Die folgenden Schnittstellen werden vom Indexer-Objekt unterstützt.



| Schnittstelle                          | BESCHREIBUNG                                                                         |
|------------------------------------|-------------------------------------------------------------------------------------|
| [**Iwmindexer**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmindexer)   | Startet und beendet den Index Vorgang.                                              |
| [**IWMIndexer2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmindexer2) | Konfiguriert den Indexer, um die Indizierung nach Frame, Zeit oder SMPTE-Zeit Code zu ermöglichen. |



 

Die folgende Rückruf Schnittstelle muss von der Anwendung implementiert werden, damit das Indexer-Objekt verwendet werden soll.



| Schnittstelle                                      | BESCHREIBUNG                                                                |
|------------------------------------------------|----------------------------------------------------------------------------|
| [**Iwmstatus Callback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) | Empfängt Statusmeldungen von Prozessen, die in einem separaten Thread ausgeführt werden. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Objekte**](objects.md)
</dt> <dt>

[**Arbeiten mit Indizes**](working-with-indexes.md)
</dt> </dl>

 

 




