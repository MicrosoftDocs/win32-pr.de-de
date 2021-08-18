---
title: Drag & Drop
description: Drag & Drop bezieht sich auf Datenübertragungen, bei denen eine Maus oder ein anderes zeigendes Gerät verwendet wird, um sowohl die Datenquelle als auch das Ziel anzugeben.
ms.assetid: bba0ddf8-fcf9-4827-bf85-7ac597d33b4b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b388fc6c051fa73c72720d1f349cd50a4fa6902b8f880fbf5ccfb4cf263a4227
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119993160"
---
# <a name="drag-and-drop"></a>Drag & Drop

*Drag and drop* refers to data transfers in which a mouse or other pointing device is used to specify both the data source and its destination. In einem typischen Drag & Drop-Vorgang wählt ein Benutzer das zu übertragende Objekt aus, indem er den Mauszeiger darauf bewegt und entweder die linke Schaltfläche oder eine andere für diesen Zweck vorgesehene Schaltfläche gedrückt hält. Während der Benutzer weiterhin die Schaltfläche gedrückt hält, initiiert er die Übertragung, indem er das Objekt an das Ziel zieht, bei dem es sich um einen beliebigen OLE-Container befinden kann. Drag & Drop bietet genau die gleiche Funktionalität wie das Kopieren und Einfügen in der OLE-Zwischenablage, fügt aber visuelles Feedback hinzu und vermeidet die Notwendigkeit von Menüs. Wenn eine Anwendung das Kopieren und Einfügen in die Zwischenablage unterstützt, ist nur wenig Zusätzliches erforderlich, um Drag & Drop zu unterstützen.

Während eines OLE-Drag & Drop-Vorgangs werden die folgenden drei separaten Codeteile verwendet.



| Drag & Drop-Codequelle                               | Implementierung und Verwendung                                                                                                                                                                      |
|---------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IDropSource-Schnittstelle**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource)<br/> | Wird durch das -Objekt implementiert, das die gezogenen Daten enthält, die als *Ziehquelle* bezeichnet werden.<br/>                                                                                         |
| [**IDropTarget-Schnittstelle**](/windows/desktop/api/OleIdl/nn-oleidl-idroptarget)<br/> | Wird durch das -Objekt implementiert, das die Ablage akzeptieren soll, die als *Ablageziel* bezeichnet wird.<br/>                                                                                 |
| [**DoDragDrop-Funktion**](/windows/desktop/api/Ole2/nf-ole2-dodragdrop)<br/>    | Wird von OLE implementiert und zum Initiieren eines Drag & Drop-Vorgangs verwendet. Nachdem der Vorgang ausgeführt wird, erleichtert er die Kommunikation zwischen der Ziehquelle und dem Ablageziel.<br/> |



 

Die [**Schnittstellen IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource) und [**IDropTarget**](/windows/desktop/api/OleIdl/nn-oleidl-idroptarget) können entweder in einem Container oder in einer Objektanwendung implementiert werden. Die Rolle des Ziehquellen- oder Ablageziels ist nicht auf einen ole-Anwendungstyp beschränkt.

Die OLE-Funktion [**DoDragDrop**](/windows/desktop/api/Ole2/nf-ole2-dodragdrop) implementiert eine Schleife, die Maus- und Tastaturbewegungen verfolgt, bis der Ziehvorgang abgebrochen wird oder ein Ziehvorgang auftritt. **DoDragDrop** is the key function in the drag and drop process, facilitating communication between the drag source and drop target.

Während eines Drag & Drop-Vorgangs können dem Benutzer drei Arten von Feedback angezeigt werden.



| Art des Feedbacks            | Beschreibung                                                                                                                                                                                                                                                                                                                                                      |
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Feedback zur Quelle<br/>  | Das Von der Ziehquelle bereitgestellte Quellfeedback gibt an, dass die Daten gezogen werden und sich während des Ziehens nicht ändern. In der Regel werden die Daten hervorgehoben, um zu signalisieren, dass sie ausgewählt wurden.<br/>                                                                                                                                            |
| Zeigerfeedback<br/> | Das Zeigerfeedback, das von der Ziehquelle bereitgestellt wird, gibt an, was geschieht, wenn die Maus zu einem bestimmten Zeitpunkt losgelassen wird. Das Zeigerfeedback ändert sich ständig, wenn der Benutzer die Maus bewegt und/oder eine Modifizierertaste drückt. Wenn der Zeiger z. B. in ein Fenster verschoben wird, das keine Ablage akzeptieren kann, ändert sich der Zeiger in das Symbol "Nicht zulässig".<br/> |
| Zielfeedback<br/>  | Vom Ablageziel bereitgestellt, gibt das Zielfeedback an, wo der Abbruch erfolgen soll.<br/>                                                                                                                                                                                                                                                                    |



 

Weitere Informationen finden Sie unter [Drag Source Responsibilities](drag-source-responsibilities.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Datenübertragung](data-transfer.md)
</dt> </dl>

 

 





