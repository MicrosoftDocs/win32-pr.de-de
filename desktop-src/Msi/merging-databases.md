---
description: Sie können das Installationsprogramm verwenden, um die Informationen in einer Datenbank in einer anderen Datenbank hinzuzufügen, indem Sie eine Zusammenführung ausführen.
ms.assetid: c53ef3d2-b3dc-4cd1-bd98-a856a223917f
title: Daten Bank Zusammenführung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8212355f37a12aa3b92bc10e6e3e41abdcf361dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960345"
---
# <a name="merging-databases"></a>Daten Bank Zusammenführung

Sie können das Installationsprogramm verwenden, um die Informationen in einer Datenbank in einer anderen Datenbank hinzuzufügen, indem Sie eine Zusammenführung ausführen. Zusammenführungen [und Transformationen](merges-and-transforms.md) arbeiten mit einer gesamten Datenbank, und ein Merge kombiniert zwei Datenbanken zu einer Datenbank. Zusammenführungen sind für Entwicklungsteams nützlich, da Sie es ermöglichen, dass die Installations Datenbank der großen Anwendung in kleinere Teile aufgeteilt und anschließend später in der kompletten Installations Datenbank kombiniert werden kann.

**So führen Sie mehrere Komponenten Datenbanken zu einer einzelnen, kompletten Datenbank zusammen**

1.  Entwickeln Sie die partiellen Komponenten Datenbanken separat.
2.  Führen Sie die einzelnen Komponenten Datenbanken durch Aufrufen der Funktion [**msidatabasemerge**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea) in der Hauptprodukt Datenbank zusammen.

 

 



