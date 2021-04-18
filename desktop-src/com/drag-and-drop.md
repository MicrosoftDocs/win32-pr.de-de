---
title: Drag & Drop
description: Drag & Drop bezieht sich auf Datenübertragungen, bei denen eine Maus oder ein anderes Zeigegerät verwendet wird, um sowohl die Datenquelle als auch das Ziel anzugeben.
ms.assetid: bba0ddf8-fcf9-4827-bf85-7ac597d33b4b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5dc4b425637432024d097acb8afdc5e169467c6a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106337167"
---
# <a name="drag-and-drop"></a>Drag & Drop

*Drag & Drop* bezieht sich auf Datenübertragungen, bei denen eine Maus oder ein anderes Zeigegerät verwendet wird, um sowohl die Datenquelle als auch das Ziel anzugeben. Bei einem typischen Drag & Drop-Vorgang wählt ein Benutzer das zu übertragende Objekt aus, indem der Mauszeiger darauf bewegt und entweder die linke Schaltfläche oder eine andere für diesen Zweck festgelegte Schaltfläche gedrückt wird. Wenn Sie die Schaltfläche weiterhin gedrückt halten, initiiert der Benutzer die Übertragung, indem er das Objekt auf das Ziel, das beliebige OLE-Container sein kann, zieht. Drag & Drop bietet genau die gleiche Funktionalität wie das Kopieren und Einfügen der OLE-Zwischenablage, fügt aber visuelles Feedback hinzu und entfällt die Notwendigkeit von Menüs. Wenn eine Anwendung das Kopieren und Einfügen von Zwischenablage unterstützt, ist ein wenig zusätzlicher Aufwand erforderlich, um Drag & Drop zu unterstützen.

Während eines OLE-Drag & Drop-Vorgangs werden die folgenden drei separaten Code Elemente verwendet.



| Drag & Drop-Code Quelle                               | Implementierung und Verwendung                                                                                                                                                                      |
|---------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource) -Schnittstelle<br/> | Wird von dem Objekt implementiert, das die gezogenen Daten enthält, die als Zieh *Quelle* bezeichnet werden.<br/>                                                                                         |
| [**IDropTarget**](/windows/desktop/api/OleIdl/nn-oleidl-idroptarget) -Schnittstelle<br/> | Wird von dem Objekt implementiert, das den Löschvorgang akzeptieren soll, der als Ablage *Ziel* bezeichnet wird.<br/>                                                                                 |
| [**DoDragDrop**](/windows/desktop/api/Ole2/nf-ole2-dodragdrop) -Funktion<br/>    | Wird von OLE implementiert und zum Initiieren eines Drag & Drop-Vorgangs verwendet. Nachdem der Vorgang ausgeführt wurde, wird die Kommunikation zwischen der Zieh Quelle und dem Ablage Ziel erleichtert.<br/> |



 

Die [**IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource) -Schnittstelle und die [**IDropTarget**](/windows/desktop/api/OleIdl/nn-oleidl-idroptarget) -Schnittstelle können entweder in einem Container oder in einer Objekt Anwendung implementiert werden. Die Rolle von "Drag Source" oder "Drop Target" ist nicht auf einen Typ von OLE-Anwendungen beschränkt.

Die OLE-Funktion [**DoDragDrop**](/windows/desktop/api/Ole2/nf-ole2-dodragdrop) implementiert eine Schleife, mit der die Maus-und Tastatur Bewegung nachverfolgt wird, bis der Zieh Vorgang abgebrochen oder eine Ablage auftritt. **DoDragDrop** ist die Schlüsselfunktion im Drag & Drop-Prozess und ermöglicht so die Kommunikation zwischen der Zieh Quelle und dem Ablage Ziel.

Während eines Drag & Drop-Vorgangs können dem Benutzer drei Feedback Typen angezeigt werden.



| Art des Feedbacks            | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                      |
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Quellen Feedback<br/>  | Das Feedback der Quelle wird von der Zieh Quelle bereitgestellt und zeigt an, dass die Daten gezogen und während des Zieh Vorgangs nicht geändert werden. Normalerweise werden die Daten hervorgehoben, um zu signalisieren, dass Sie ausgewählt wurde.<br/>                                                                                                                                            |
| Zeiger Feedback<br/> | Der von der Zieh Quelle bereitgestellte Zeiger gibt an, was geschieht, wenn die Maus zu einem beliebigen Zeitpunkt freigegeben wird. Zeiger Feedback werden fortlaufend geändert, wenn der Benutzer die Maus bewegt und/oder eine Modifizierertaste drückt. Wenn der Zeiger z. b. in ein Fenster verschoben wird, das keinen Löschvorgang akzeptieren kann, wird der Zeiger in das Symbol "nicht zulässig" geändert.<br/> |
| Ziel Feedback<br/>  | Das vom Ablage Ziel bereitgestellte Ziel Feedback gibt an, wo der Ablage Vorgang erfolgen soll.<br/>                                                                                                                                                                                                                                                                    |



 

Weitere Informationen finden Sie unter über [tragen von Quell Zuständigkeiten](drag-source-responsibilities.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Datenübertragung](data-transfer.md)
</dt> </dl>

 

 





