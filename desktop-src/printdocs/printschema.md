---
description: Das Druck Schema und zugehörige Technologien sind in Microsoft .NET Framework 3,0 und höheren Versionen von Microsoft .NET Framework sowie in Windows Vista und höheren Versionen von Windows verfügbar.
ms.assetid: 98d5f8ec-54bd-4e88-b632-ed427b599cb6
title: Druck Schema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae3ac50b9a2f2aba9cda7dc73f183e1f3571cc9d
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106371838"
---
# <a name="print-schema"></a>Druck Schema

Das Druck Schema und zugehörige Technologien sind in Microsoft .NET Framework 3,0 und höheren Versionen von Microsoft .NET Framework sowie in Windows Vista und höheren Versionen von Windows verfügbar. XPS-Dokumente und das XPS-Objektmodell können die Druck Ticket Objekte verwenden, die in der [Druck Schema Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)beschrieben werden, um die Druckeinstellungen eines Dokuments für Drucker und die Anzeige von Anwendungen anzugeben.

Die [Druck Schema Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip) ist ein herunterladbares Dokument, das Informationen über das Druck Schema und seine Verwendung in Dokumenten und Drucken enthält. Weitere Informationen werden nur dann online für Ihre Informationen bereitgestellt, und zwar in der [Legacy-Druck Schema Referenz](print-schema.md). Allerdings wird die aktuelle Version der [Druck Schema Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)möglicherweise nicht genau widerspiegelt. Die aktuellen Entwurfs Informationen finden Sie in der [Druck Schema Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip) .

## <a name="print-schema-overview"></a>Übersicht über das Druck Schema

Beim Druck Schema handelt es sich um ein hierarchisch strukturiertes XML-basiertes Schema, das zum organisieren und beschreiben der Eigenschaften eines Druckers oder Druckauftrags verwendet wird. Das Druck Schema umfasst zwei Komponenten: die Print-Schema Schlüsselwörter und das Print Schema-Framework. Die Schlüsselwörter des Druck Schemas sind ein Satz von Element Instanzen, die Drucker Attribute und die Formatierungs Absicht der Druckaufträge beschreiben. Das Print Schema-Framework definiert eine hierarchisch strukturierte Auflistung von XML-Elementtypen und wie diese Elementtypen verwendet werden können.

Die Druck Schema Technologien, die als *Print-Funktionen* und *PrintTicket* bezeichnet werden, werden mit den im Print Schema-Framework angegebenen Druck Schema Schlüsselwörtern erstellt. Die Print-Schema Spezifikation unterstützt Schema Erweiterungen durch Dritte, sodass Druck Schema Benutzer nicht auf die von den Schlüsselwörtern des Druck Schemas definierten Eigenschaften, Features, Optionen oder parameterinit-Instanzen beschränkt sind. Element Instanzen von Drittanbietern können Element Instanzen hinzugefügt werden, die von den Druck Schema Schlüsselwörtern definiert werden. Private Instanzen von Drittanbieter-Eigenschaften müssen jedoch zu einem Namespace gehören, der eindeutig mit dem Drittanbieter verknüpft ist, der den Namespace erstellt hat.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Druck Schema Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> <dt>

[Ältere Druck Schema Referenz](print-schema.md)
</dt> <dt>

[Bidirektionale Druckerkommunikation (Hardware dev Center)](/windows-hardware/drivers/print/bidirectional-communication)
</dt> </dl>

 

 
