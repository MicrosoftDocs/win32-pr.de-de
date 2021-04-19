---
description: Diese ixpsomprintticketresource-Schnittstelle der XPS-Dokument-API ermöglicht den Zugriff auf ein vorhandenes Druck Ticket sowie die Möglichkeit, in einem XPS-OM ein Druck Ticket zu erstellen.
ms.assetid: 53c95da0-1601-4945-83a1-e3266d251aee
title: Schnittstellen für XPS-OM-Druck Tickets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 646089455e7106b1be3716c0ccf0774be361f130
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106353282"
---
# <a name="xps-om-print-ticket-interfaces"></a>Schnittstellen für XPS-OM-Druck Tickets

Diese [**ixpsomprintticketresource**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomprintticketresource) -Schnittstelle der XPS-Dokument-API ermöglicht den Zugriff auf ein vorhandenes Druck Ticket sowie die Möglichkeit, in einem XPS-OM ein Druck Ticket zu erstellen.

## <a name="print-ticket-resources"></a>Drucken von Ticket Ressourcen

Die [**ixpsomprintticketresource**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomprintticketresource) -Schnittstelle ermöglicht einem Programm das Lesen des Inhalts eines vorhandenen Druck Tickets durch Aufrufen der **getprintticketresource** -Methode einer Schnittstelle, die ein Druck Ticket unterstützt. Neue Druck Ticket Ressourcen können einem Dokument Teil hinzugefügt werden, indem **setprintticketresource** aufgerufen wird.

Es gibt drei Druck Ticket Ebenen, die den Bereich des Druck Tickets angeben. Die Druck Ticket Stufen lauten wie folgt: die Ebene des Auftrags (oder Pakets), die Dokument Ebene und die Seitenebene. Die folgende Tabelle zeigt die Beziehung zwischen der Druck Ticket Ebene, der entsprechenden XPS OM-Schnittstelle und den Methoden, die für den Zugriff auf die Ressource "Print Ticket" verwendet werden.

| Druck Ticket Ebene | Schnittstelle                                                | Get-Methode                                                                      | Set-Methode                                                                      |
|--------------------|----------------------------------------------------------|---------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| Auftrag                | [**Ixpsomdocumentsequence**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence) | [**Getprintticketresource**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomdocumentsequence-getprintticketresource) | [**Setprintticketresource**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomdocumentsequence-setprintticketresource) |
| Dokument           | [**Ixpsomdocument**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument)                 | [**Getprintticketresource**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomdocument-getprintticketresource)         | [**Setprintticketresource**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomdocument-setprintticketresource)         |
| Seite               | [**Ixpsompagereferenzierung**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference)       | [**Getprintticketresource**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-getprintticketresource)    | [**Setprintticketresource**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-setprintticketresource)    |



 

## <a name="print-ticket-content"></a>Ticket Inhalt drucken

Der Zugriff auf den Inhalt einer vorhandenen Ressource "Print Ticket" kann durchlesen aus dem Stream erfolgen, der der Ressource zugeordnet ist. Die [**GetStream**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomprintticketresource-getstream) -Methode der [**ixpsomprintticketresource**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomprintticketresource) -Schnittstelle gibt den Zeiger auf einen schreibgeschützten Datenstrom zurück, der den XML-formatierten Inhalt des Druck Tickets enthält. Das Format des Druck Ticket Inhalts wird in der [Druck Schema Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)beschrieben.

Eine neue Druck Ticket Ressource kann erstellt werden, indem Sie eine neue [**ixpsomprintticketresource**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomprintticketresource) -Schnittstelle erstellen. Ein gültiges, XML-formatiertes Druck Ticket wird in einen Stream geschrieben, und es wird ein Teil-URI erstellt, um den Druck Ticket Teil zu identifizieren. Weitere Informationen zum Inhalt eines gültigen Druck Tickets finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip). Der Stream und der Teil-URI werden als Parameter des [**setContent**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomprintticketresource-setcontent) -Aufrufs zur Festlegung der neuen Ressource "Print Ticket" und der Ressource "Print Ticket" durch Aufrufen der **setprintticketresource** -Methode, die in der obigen Tabelle angezeigt wird, hinzugefügt.

## <a name="print-ticket-inheritance"></a>Druck Ticket Vererbung

Druck Tickets erben die Eigenschaften von Druck Tickets mit größerem Bereich. Ein Druck Ticket auf Dokument Ebene erbt z. b. die Eigenschaften des Druck Tickets auf Auftrags Ebene, das mit der Dokument Sequenz des Dokuments verknüpft ist. Ebenso erbt ein Druck Ticket auf Seitenebene die Eigenschaften des Druck Tickets auf Dokument Ebene, das dem Dokument der Seite zugeordnet ist. In diesem Vererbungs Prozess überschreiben Eigenschaften, die im Druck Ticket auf niedrigerer Ebene angegeben werden, die entsprechenden Eigenschaften, die andernfalls von dem höheren Druck Ticket geerbt werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Druck Schema Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> <dt>

[**Ixpsomdocument**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument)
</dt> <dt>

[**Ixpsomdocumentsequence**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence)
</dt> <dt>

[**Ixpsompagereferenzierung**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference)
</dt> <dt>

[**Ixpsomprintticketresource**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomprintticketresource)
</dt> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 



