---
title: Elementmoniker
description: Eine andere OLE-implementierte Monikerklasse ist der elementmoniker, der zum Identifizieren eines Objekts verwendet werden kann, das in einem anderen Objekt enthalten ist.
ms.assetid: ddcf3669-4ad0-4a4e-80a6-eb78058cff09
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57b692502ba44519a2c51a661ef62a51e133ac04
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106340398"
---
# <a name="item-monikers"></a>Elementmoniker

Eine andere OLE-implementierte Monikerklasse ist der *elementmoniker*, der zum Identifizieren eines Objekts verwendet werden kann, das in einem anderen Objekt enthalten ist. Ein Typ eines enthaltenen Objekts ist ein OLE-Objekt, das in einem Verbund Dokument eingebettet ist. In einem Verbund Dokument können die eingebetteten Objekte identifiziert werden, die darin enthalten sind, indem jeder ein beliebiger Name zugewiesen wird, z. b. "embedobj1", "embedobj2" usw. Ein anderer Typ eines eigenständigen Objekts ist eine Benutzer Auswahl in einem Dokument, z. b. ein Bereich von Zellen in einer Kalkulations Tabelle oder ein Zeichenbereich in einem Textdokument. Ein Objekt, das aus einer Auswahl besteht, wird als *Pseudo Objekt* bezeichnet, da es nicht als eindeutiges Objekt behandelt wird, bis ein Benutzer die Auswahl markiert. Ein Arbeitsblatt identifiziert möglicherweise einen Zellbereich unter Verwendung eines Namens wie "1a: 7F", während ein Textverarbeitungsdokument einen Zeichenbereich mithilfe des Namens eines Lesezeichens identifizieren kann.

Ein elementmoniker ist vor allem dann hilfreich, wenn er mit einem anderen Moniker verkettet oder zusammen *gesetzt* wird, der den Container identifiziert. In der Regel wird ein elementmoniker erstellt und dann auf (z. b.) einen dateimoniker verfasst, um das Äquivalent eines kompletten Pfads zum Objekt zu erstellen. Beispielsweise können Sie den dateimoniker "c: \\ work \\report.doc" (der das Container Objekt identifiziert) mit dem elementmoniker "embedobj1" (der ein Objekt innerhalb des Containers identifiziert) verfassen, um den Moniker "c: \\ workreport.docembedobj1" zu bilden \\ \\ , der ein bestimmtes Objekt innerhalb einer bestimmten Datei eindeutig identifiziert. Sie können auch zusätzliche elementmoniker verketten, um tief geschachtelte Objekte zu identifizieren. Wenn "embedobj1" z. b. der Name eines Tabellen Kalkulations Objekts ist, können Sie einen bestimmten Zellen Bereich in diesem Tabellenobjekt anfügen, um einen anderen elementmoniker anzufügen, um einen Moniker zu erstellen, der das Äquivalent zu "c: \\ work \\report.doc\\ embedobj1 \\ 1a: 7F" wäre.

In Kombination mit einem dateimoniker bildet ein elementmoniker einen kompletten Pfad. Elementmoniker erweitern das Konzept von Pfadnamen über das Dateisystem hinaus und definieren dabei Pfadnamen, um einzelne Objekte und nicht nur Dateien zu identifizieren.

Es gibt einen signifikanten Unterschied zwischen einem elementmoniker und einem dateimoniker. Der in einem dateimoniker enthaltene Pfad ist für jeden Benutzer aussagekräftig, der das Dateisystem versteht, während der in einem elementmoniker enthaltene partielle Pfad nur für einen bestimmten Container sinnvoll ist. Jeder weiß, auf welche "c: \\ work \\report.doc" verweist, aber nur ein bestimmtes Container Objekt weiß, auf welches "1a: 7F" verwiesen wird. Ein von einer anderen Anwendung erstellter elementmoniker kann von einem Container nicht interpretiert werden. der einzige Container, der weiß, auf welches Objekt von einem elementmoniker verwiesen wird, ist der Container, der den elementmoniker dem Objekt an erster Stelle zugewiesen hat. Aus diesem Grund darf die Quelle des Objekts, das durch die Kombination aus Datei-und elementmoniker benannt ist, nicht nur [**IPersistFile**](/windows/desktop/api/ObjIdl/nn-objidl-ipersistfile)implementieren, um die Bindung des dateimonikers zu vereinfachen, sondern auch [**ioleitemcontainer**](/windows/desktop/api/OleIdl/nn-oleidl-ioleitemcontainer) , um das Auflösen des Namens des elementmonikers in das entsprechende Objekt im Kontext einer Datei zu vereinfachen.

Der Vorteil von Monikern besteht darin, dass jemand, der einen Moniker zum Auffinden eines Objekts verwendet, nicht den im elementmoniker enthaltenen Namen verstehen muss, solange der elementmoniker Teil eines zusammengesetzten ist. Im allgemeinen wäre es nicht sinnvoll, einen elementmoniker eigenständig zu existieren. Stattdessen würden Sie einen elementmoniker auf einem dateimoniker verfassen. Anschließend wird [**IMoniker:: BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) für den zusammengesetzten aufgerufen, der die einzelnen Moniker darin bindet und die Namen interpretiert.

Zum Erstellen eines elementmonikerobjekts und Zurückgeben des Zeigers auf den monikeranbieter stellt OLE die Hilfsfunktion " [**feateitemmoniker**](/windows/desktop/api/Objbase/nf-objbase-createitemmoniker)" bereit. Diese Funktion erstellt ein elementmonikerobjekt und gibt seinen Zeiger auf den Anbieter zurück.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Anti-Moniker](anti-monikers.md)
</dt> <dt>

[Klassenmoniker](class-monikers.md)
</dt> <dt>

[Zusammengesetzte Moniker](composite-monikers.md)
</dt> <dt>

[Dateimoniker](file-monikers.md)
</dt> <dt>

[Zeigermoniker](pointer-monikers.md)
</dt> </dl>

 

 




