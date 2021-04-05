---
title: Abfrage Bereich
description: Der Gültigkeitsbereich einer Abfrage wird durch das Objekt bestimmt, an das die Bindung erfolgen soll.
ms.assetid: 7ece8599-8a4b-45a1-95f4-a4180052f245
ms.tgt_platform: multiple
keywords:
- Bereich der Abfrage-ADSI
- Abfragen von ADSI, Bereich
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dac51fc261cb418db0018acd996c248766896a25
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707386"
---
# <a name="scope-of-query"></a>Abfrage Bereich

Der Gültigkeitsbereich einer Abfrage wird durch das Objekt bestimmt, an das die Bindung erfolgen soll. Wenn Sie nicht sicher sind, wo sich das Objekt im Unternehmen befindet, müssen Sie so weit wie möglich eine Suche durchführen. Wenn Sie jedoch wissen, dass das Objekt in einer bestimmten Domäne enthalten ist, z. b. in der Domäne, mit der der Benutzer verbunden ist, oder in einer bestimmten Gruppe (z. b. in der Gruppe "Manager"), sollten Sie den Suchbereich so festlegen, dass er die Umstände widerspiegelt. Um die optimale Leistung zu erzielen, sollten Sie versuchen, den Bereich als Ziel für die kleinste Anzahl möglicher Objekte zu suchen.

Wenn Sie nicht sicher sind, wo sich ein Objekt im Unternehmen befinden wird, können Sie eine Bindung an den globalen Katalog Dienst herstellen. Der globale Katalog Dienst enthält eine Liste aller Objekte im Verzeichnis und eine kleine Teilmenge der Attribute jedes Objekts. Nachdem Sie das Objekt im globalen Katalog gefunden haben, können Sie seinen Distinguished Name aus dem globalen Katalog abrufen und zum Binden an das-Objekt verwenden, um andere Vorgänge auszuführen.

Nachdem Sie entschieden haben, an welches Objekt die Bindung erfolgen soll, können Sie die Abfrage auf einen der folgenden Bereiche beschränken: eine Basis Abfrage, eine Abfrage auf einer einzelnen Ebene oder eine Unterstruktur Suche, wie in der folgenden Abbildung dargestellt.

![Objekte im Stammverzeichnis einer Suche nach einer Basis-, einer-oder Unterstruktur Suche](images/netds6.png)

## <a name="base"></a>Basis

Eine Basis Abfrage beschränkt die Suche auf das Basisobjekt. Die maximale Anzahl von zurückgegebenen Objekten ist immer 1. Diese Suche kann verwendet werden, um zu überprüfen, ob ein Objekt vorhanden ist. Wenn Sie z. b. über den Distinguished Name eines Objekts verfügen und das vorhanden sein des Objekts basierend auf dem Pfad überprüfen müssen, können Sie eine Suche auf einer einzelnen Ebene verwenden. Wenn die Suche fehlschlägt, können Sie davon ausgehen, dass das Objekt möglicherweise umbenannt oder an einen anderen Speicherort verschoben wurde oder dass ihnen falsche Daten über das Objekt übergeben wurden. Beachten Sie, dass Sie die GUID anstelle des Distinguished Name speichern sollten, wenn Sie ein Objekt überprüfen möchten. Dadurch kann das Objekt in der Verzeichnishierarchie umbenannt oder verschoben werden, ohne den beibehaltenen Link zu unterbrechen.

## <a name="one-level"></a>Eine Ebene

Eine einstufige Suche ist auf die unmittelbaren untergeordneten Elemente eines Basis Objekts beschränkt, schließt jedoch das Basisobjekt selbst aus. Mit dieser Einstellung kann eine gezielte Suche nach unmittelbar untergeordneten Objekten eines übergeordneten Objekts durchgeführt werden. Wenn Sie z. b. über ein übergeordnetes Objekt mit dem Namen P1 verfügen und seine unmittelbaren untergeordneten Elemente: C1, C2, C3 sind, sollten Sie bei der Auswertung der Kriterien in einer einstufigen Suche, C1, C2 und C3 enthalten sein, aber P1 wäre nicht Teil der Suche. Eine einstufige Suche kann verwendet werden, um alle untergeordneten Elemente eines Objekts aufzulisten. Tatsächlich übersetzt die [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) -Enumeration bei manchen ADSI-Anbietern in eine Suche auf einer Ebene.

## <a name="subtree"></a>Unterstruktur

Eine Unterstruktur Suche, auch als Deep Search bezeichnet, umfasst alle Objekte unterhalb des Basis Objekts, ausgenommen das Basisobjekt selbst. Diese Suche kann Verweise auf andere Server generieren. Diese Suche hat den größten Bereich und gibt möglicherweise ein großes Resultset zurück. Suchen Sie nach Möglichkeit nach mindestens einem indizierten Attribut, und legen Sie die Einstellungen für den Verweis fest (Weitere Informationen finden Sie unter [Leistung und Verarbeitung großer Resultsets](performance-and-handling-large-result-sets.md)), um die Suchanforderungen zu erfüllen. Außerdem wird empfohlen, dass die Ergebnisse einer Unterstruktur Suche asynchron und per Pager ausgeführt werden, um den Server Mehraufwand und die Effektivität des Netzwerks zu verringern. Eine Unterstruktur Suche wird normalerweise verwendet, um Objekte für einen bestimmten Bereich zu durchsuchen. Suchen Sie beispielsweise nach allen Benutzern mit Konten, die innerhalb von 30 Tagen oder weniger abläuft.

 

 




