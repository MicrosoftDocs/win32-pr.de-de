---
title: Abfragebereich
description: Der Bereich einer Abfrage wird durch das Objekt bestimmt, an das Sie binden.
ms.assetid: 7ece8599-8a4b-45a1-95f4-a4180052f245
ms.tgt_platform: multiple
keywords:
- Bereich der Abfrage ADSI
- abfragen ADSI , Bereich
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45a31ebe378502dd9b4ddda6dce83e3547dab580360a8d1ec07516d1e3347cf0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023252"
---
# <a name="scope-of-query"></a>Abfragebereich

Der Bereich einer Abfrage wird durch das Objekt bestimmt, an das Sie binden. Wenn Sie sich nicht sicher sind, wo sich das Objekt innerhalb des Unternehmens befindet, müssen Sie so weit wie möglich eine Suche unternehmen. Wenn Sie jedoch wissen, dass das Objekt in einer bestimmten Domäne enthalten ist, z. B. in der Domäne, mit der der Benutzer verbunden ist, oder in einer bestimmten Gruppe, z. B. in der Gruppe Manager, sollten Sie den Bereich der Suche entsprechend den Umständen festlegen. Um die beste Leistung zu erzielen, sollten Sie versuchen, den Bereich als Ziel zu verwenden, um die geringst mögliche Anzahl von Objekten zu durchsuchen.

Wenn Sie nicht sicher sind, wo sich ein Objekt im Unternehmen befindet, können Sie eine Bindung an den globalen Katalogdienst erstellen. Der globale Katalogdienst enthält eine Liste aller Objekte im Verzeichnis und eine kleine Teilmenge der Attribute jedes Objekts. Nachdem Sie das Objekt im globalen Katalog finden, können Sie seinen Distinguished Name aus dem globalen Katalog abrufen und zum Binden an das Objekt verwenden, um andere Vorgänge durchzuführen.

Nachdem Sie entschieden haben, an welches Objekt sie gebunden werden soll, können Sie die Abfrage weiter auf einen der folgenden Bereiche beschränken: eine Basisabfrage, eine Abfrage auf einer Ebene oder eine Teilstruktursuche, wie in der folgenden Abbildung dargestellt.

![-Objekte im Stamm einer Suche nach einer Basis-, Einer-Ebene- oder Unterstruktursuche](images/netds6.png)

## <a name="base"></a>Basis

Eine Basisabfrage beschränkt die Suche auf das Basisobjekt. Die maximale Anzahl der zurückgegebenen Objekte ist immer 1. Diese Suche kann verwendet werden, um das Vorhandensein eines Objekts zu überprüfen. Wenn Sie beispielsweise über den Distinguished Name eines Objekts verfügen und das Vorhandensein des Objekts anhand des Pfads überprüfen müssen, können Sie eine Suche auf einer Ebene verwenden. Wenn bei der Suche ein Fehler auftritt, können Sie davon ausgehen, dass das Objekt umbenannt oder an einen anderen Speicherort verschoben wurde oder dass Falsche Daten zum Objekt angegeben wurden. Beachten Sie, dass Sie die GUID anstelle des Distinguished Name speichern sollten, wenn Sie ein Objekt erneut besuchen möchten. Dadurch kann das Objekt umbenannt oder in der Verzeichnishierarchie verschoben werden, ohne die persistente Verknüpfung zu unterbricht.

## <a name="one-level"></a>Eine Ebene

Eine Suche auf einer Ebene ist auf die unmittelbaren unteren Objekte eines Basisobjekts beschränkt, schließt jedoch das Basisobjekt selbst aus. Diese Einstellung kann eine gezielte Suche nach unmittelbar untergeordneten Objekten eines übergeordneten Objekts ausführen. Wenn Sie beispielsweise über ein übergeordnetes Objekt mit dem Namen P1 verfügen und dessen unmittelbar übergeordnete Objekte C1, C2, C3 sind, sollten C1, C2 und C3 bei der Auswertung der Kriterien in eine Ein-Ebene-Suche eingeschlossen werden, P1 wäre jedoch nicht Teil der Suche. Eine Suche auf einer Ebene kann verwendet werden, um alle unteren Objekte eines Objekts aufzählen. In einigen ADSI-Anbietern wird die [**IADsContainer-Enumeration**](/windows/desktop/api/Iads/nn-iads-iadscontainer) in eine Suche auf einer Ebene übersetzt.

## <a name="subtree"></a>Unterstruktur

Eine Unterstruktursuche, die auch als tiefe Suche bezeichnet wird, umfasst alle Objekte unter dem Basisobjekt, mit Ausnahme des Basisobjekts selbst. Diese Suche kann Verweise auf andere Server generieren. Diese Suche hat den größten Umfang und kann ein großes Resultset zurückgeben. Suchen Sie nach Möglichkeit nach mindestens einem indizierten Attribut, und legen Sie die Empfehlungseinstellungen fest (weitere Informationen finden Sie unter Leistung und Behandlung großer [Result Sets),](performance-and-handling-large-result-sets.md)um Ihre Suchanforderungen zu erfüllen. Es wird auch empfohlen, die Ergebnisse einer Teilstruktursuche asynchron durchzuführen und auspagen, um den Serveraufwand und die Netzwerkeffizienz zu reduzieren. Eine Unterstruktursuche wird normalerweise verwendet, um Objekte für einen bestimmten Bereich zu durchsuchen. Suchen Sie beispielsweise nach allen Benutzern mit Konten, die in 30 Tagen oder weniger ablaufen.

 

 




