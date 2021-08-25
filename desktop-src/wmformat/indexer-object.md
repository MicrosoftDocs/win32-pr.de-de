---
title: Indexer-Objekt
description: Indexer-Objekt
ms.assetid: 652e04a5-ed6e-4e92-acf4-55ed82f77ef1
keywords:
- Windows Medienformat-SDK, Indexerobjekte
- Advanced Systems Format (ASF), Indexerobjekte
- ASF (Advanced Systems Format), Indexerobjekte
- Objekte,Indexerobjekte
- Indexerobjekte
- Indizes,Indexer-Objekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 795ef166f6b3ad46897305cbd3f6c38bbc7a219bb99df1dcf8b14dbfb1443577
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119839787"
---
# <a name="indexer-object"></a>Indexer-Objekt

Das Indexerobjekt erstellt einen Index in einer ASF-Datei. Ein Index ist ein Standardteil einer ASF-Datei, der Videobeispiele mit Zeit-, Framenummern- oder (falls zutreffend) SMPTE-Standardzeitstempeln (Society of Motion Picture and Tv Engineers) gleichzusetzen. Ohne Index kann weder das Readerobjekt noch das synchrone Readerobjekt bis zu einem Punkt in der Mitte einer Datei suchen.

Von diesem Objekt erstellte Indizes sind nur erforderlich, wenn die Datei einen oder mehrere Videostreams enthält. Dies liegt daran, dass Audiodaten nicht zeitlich komprimiert sind, was es einfach macht, eine bestimmte Zeit in einem Audiostream zu finden.

Das Indexerobjekt wird von der [**WMCreateIndexer-Funktion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateindexer) erstellt, die einen Zeiger auf eine **IWMIndexer-Schnittstelle** legt. Die anderen Schnittstellen des Indexerobjekts können durch Aufrufen der **QueryInterface-Methode ermittelt** werden.

Die folgenden Schnittstellen werden vom Indexerobjekt unterstützt.



| Schnittstelle                          | BESCHREIBUNG                                                                         |
|------------------------------------|-------------------------------------------------------------------------------------|
| [**IWMIndexer**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmindexer)   | Startet und beendet den Indizierungsprozess.                                              |
| [**IWMIndexer2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmindexer2) | Konfiguriert den Indexer und ermöglicht die Indizierung nach Frame, Zeit oder SMPTE-Zeitcode. |



 

Die folgende Rückrufschnittstelle muss von der Anwendung implementiert werden, um das Indexerobjekt verwenden zu können.



| Schnittstelle                                      | BESCHREIBUNG                                                                |
|------------------------------------------------|----------------------------------------------------------------------------|
| [**IWMStatusCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) | Empfängt Statusmeldungen von Prozessen, die in einem separaten Thread ausgeführt werden. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Objekte**](objects.md)
</dt> <dt>

[**Arbeiten mit Indizes**](working-with-indexes.md)
</dt> </dl>

 

 




