---
description: Diese IXpsOMPrintTicketResource-Schnittstelle der XPS-Dokument-API bietet Zugriff auf ein vorhandenes Druckticket sowie die Möglichkeit, ein Druckticket in einer XPS OM zu erstellen.
ms.assetid: 53c95da0-1601-4945-83a1-e3266d251aee
title: XPS OM–Druckticketschnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f629e716db7098f8f6999df758fd3b73e3f82b83308a3dd68d5f247d6cd709a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117867756"
---
# <a name="xps-om-print-ticket-interfaces"></a>XPS OM–Druckticketschnittstellen

Diese [**IXpsOMPrintTicketResource-Schnittstelle**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomprintticketresource) der XPS-Dokument-API bietet Zugriff auf ein vorhandenes Druckticket sowie die Möglichkeit, ein Druckticket in einer XPS OM zu erstellen.

## <a name="print-ticket-resources"></a>Drucken von Ticketressourcen

Mit der [**IXpsOMPrintTicketResource-Schnittstelle**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomprintticketresource) kann ein Programm den Inhalt eines vorhandenen Drucktickets lesen, indem es die **GetPrintTicketResource-Methode** einer Schnittstelle aufruft, die ein Druckticket unterstützt. Neue Druckticketressourcen können einem Dokumentteil durch Aufrufen von **SetPrintTicketResource** hinzugefügt werden.

Es gibt drei Druckticketebenen, die den Bereich des Drucktickets angeben. Die Druckticketebenen sind: Auftrags- (oder Paketebene), Dokumentebene und Seitenebene. Die folgende Tabelle zeigt die Beziehung zwischen der Druckticketebene, der entsprechenden XPS OM-Schnittstelle und den Methoden für den Zugriff auf die Druckticketressource.

| Druckticketebene | Schnittstelle                                                | Get-Methode                                                                      | Set-Methode                                                                      |
|--------------------|----------------------------------------------------------|---------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| Auftrag                | [**IXpsOMDocumentSequence**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence) | [**GetPrintTicketResource**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomdocumentsequence-getprintticketresource) | [**SetPrintTicketResource**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomdocumentsequence-setprintticketresource) |
| Dokument           | [**IXpsOMDocument**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument)                 | [**GetPrintTicketResource**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomdocument-getprintticketresource)         | [**SetPrintTicketResource**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomdocument-setprintticketresource)         |
| Seite               | [**IXpsOMPageReference**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference)       | [**GetPrintTicketResource**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-getprintticketresource)    | [**SetPrintTicketResource**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-setprintticketresource)    |



 

## <a name="print-ticket-content"></a>Drucken von Ticketinhalten

Sie können auf den Inhalt einer vorhandenen Druckticketressource zugreifen, indem Sie aus dem Stream lesen, der der Ressource zugeordnet ist. Die [**GetStream-Methode**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomprintticketresource-getstream) der [**IXpsOMPrintTicketResource-Schnittstelle**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomprintticketresource) gibt den Zeiger auf einen schreibgeschützten Stream zurück, der den XML-formatierten Inhalt des Drucktickets enthält. Das Format des Druckticketinhalts wird in der [Druckschemaspezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)beschrieben.

Eine neue Druckticketressource kann durch Erstellen einer neuen [**IXpsOMPrintTicketResource-Schnittstelle**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomprintticketresource) erstellt werden. Ein gültiges, XML-formatiertes Druckticket wird in einen Stream geschrieben, und ein Teile-URI wird erstellt, um den Druckticketteil zu identifizieren. Weitere Informationen zum Inhalt eines gültigen Drucktickets finden Sie in der [Druckschemaspezifikation.](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip) Der Stream und der Part-URI werden als Parameter des [**SetContent-Aufrufs**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomprintticketresource-setcontent) übergeben, um die neue Druckticketressource festzulegen, und die Druckticketressource wird dem entsprechenden Dokumentteil hinzugefügt, indem die in der vorherigen Tabelle **gezeigte SetPrintTicketResource-Methode** aufgerufen wird.

## <a name="print-ticket-inheritance"></a>Vererbung von Drucktickets

Drucktickets erben die Eigenschaften von Drucktickets mit größerem Umfang. Beispielsweise erbt ein Druckticket auf Dokumentebene die Eigenschaften des Drucktickets auf Auftragsebene, das der Dokumentsequenz des Dokuments zugeordnet ist. Ebenso erbt ein Druckticket auf Seitenebene die Eigenschaften des Drucktickets auf Dokumentebene, das dem Dokument der Seite zugeordnet ist. Bei diesem Vererbungsprozess überschreiben Eigenschaften, die im Druckticket auf niedrigerer Ebene angegeben sind, die entsprechenden Eigenschaften, die andernfalls vom Übergeordneten Druckticket geerbt würden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Spezifikation des Druckschemas](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> <dt>

[**IXpsOMDocument**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument)
</dt> <dt>

[**IXpsOMDocumentSequence**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence)
</dt> <dt>

[**IXpsOMPageReference**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference)
</dt> <dt>

[**IXpsOMPrintTicketResource**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomprintticketresource)
</dt> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 



