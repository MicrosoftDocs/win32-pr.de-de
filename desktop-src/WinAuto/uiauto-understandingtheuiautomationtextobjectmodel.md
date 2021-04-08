---
title: Grundlegendes zum Text Objektmodell für die Benutzeroberflächen Automatisierung
description: In diesem Thema wird beschrieben, wie Microsoft UI Automation-Client Anwendungen auf den Text Inhalt eines textbasierten Steuer Elements zugreifen.
ms.assetid: 8545EBA3-6995-4336-A197-27CE3A3339EE
keywords:
- Clients, Grundlegendes zum Textobjekt Modell der Benutzeroberflächen Automatisierung
- Clients, textbasierte Steuerelemente
- Clients, Textbereiche
- Clients, Text-Steuerelement Muster
- Clients, TextRange-Steuerelement Muster
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f6dae1fc5ca02af69ab3d5386461e6bd7a864d4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709341"
---
# <a name="understanding-the-ui-automation-text-object-model"></a>Grundlegendes zum Text Objektmodell für die Benutzeroberflächen Automatisierung

In diesem Thema wird beschrieben, wie Microsoft UI Automation-Client Anwendungen auf den Text Inhalt eines textbasierten Steuer Elements zugreifen.

-   [Steuerelement spezifisches Objektmodell](#control-specific-object-model)
-   [Zugehörige Themen](#related-topics)

Text basierte Steuerelemente machen Textinhalte für Benutzeroberflächenautomatisierungs-Client Anwendungen über ein einfaches Textobjekt Modell verfügbar. Client Anwendungen können über die [Text-und TextRange](uiauto-about-text-and-textrange-patterns.md) -Steuerelement Muster-Schnittstellen auf das Textobjekt Modell zugreifen, einschließlich [**iuiautomationtextpattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextpattern) und [**iuiautomationtextrange**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextrange). Client Anwendungen können diese Schnittstellen verwenden, um Textinhalte, Text Attribute und eingebettete Objekte wie Tabellen und Hyperlinks aus textbasierten Steuerelementen abzurufen.

Steuerelement Typen, die das Objektmodell für die Benutzeroberflächen Automatisierung unterstützen, enthalten die Steuerelement Typen [Bearbeiten](uiauto-supporteditcontroltype.md) und [Dokument](uiauto-supportdocumentcontroltype.md) . Andere Steuerelement Typen, [](uiauto-supporttooltipcontroltype.md) z. b. QuickInfo und [Text](uiauto-supporttextcontroltype.md) , unterstützen möglicherweise auch das Text Objektmodell, sind jedoch nicht erforderlich.

> [!Note]  
> Das Benutzeroberflächen Automatisierungs-Textobjekt Modell bietet keine Möglichkeit, Text einzufügen oder zu ändern. Einige Steuerelemente ermöglichen es jedoch, Text entweder über die [**iuiautomationvaluepattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationvaluepattern) -Schnittstelle oder durch direkte Tastatureingaben einzufügen oder zu ändern.

 

## <a name="control-specific-object-model"></a>Steuerelement spezifisches Objektmodell

Ein textbasiertes Steuerelement, das seinen eigenen Dokumentobjektmodell (DOM) implementiert, kann das DOM durch Implementieren des [ObjectModel](uiauto-implementingobjectmodel.md) -Steuerelement Musters verfügbar machen. Wenn Sie das DOM verfügbar machen, können Client Anwendungen den Inhalt eines textbasierten Steuer Elements besser aufrufen und steuern.

Eine Client Anwendung kann ermitteln, ob ein bestimmtes textbasiertes Steuerelement ein DOM durch Abrufen der [**iuiautomationelement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) -Schnittstelle des Steuer Elements implementiert. Anschließend können Sie die [**iuiautomationelement:: GetCurrentPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue) -Methode aufrufen und dabei den [**UIA- \_ isobjectmodelpatternavailablepropertyid**](uiauto-control-pattern-availability-propids.md) -Eigenschafts Bezeichner angeben und einen Variant-Wert, der true erhält, wenn das Steuerelement ein DOM implementiert.

Um auf das DOM zuzugreifen, müssen Sie die [**iuiautomationelement:: GetCurrentPattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpattern) -Methode aufrufen und dabei den [**UIA \_ objectmodelpatternid**](uiauto-controlpattern-ids.md) -Steuerelement Muster Bezeichner und eine Variable, die die [**iuiautomationobjectmodelpattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationobjectmodelpattern) -Schnittstelle empfängt, angeben. Rufen Sie die [**iuiautomationobjectmodelpattern:: getunderlyingobjectmodel**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationobjectmodelpattern-getunderlyingobjectmodel) -Methode auf, um die DOM-Schnittstelle abzurufen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Text-und TextRange-Steuerelement Muster](uiauto-implementingtextandtextrange.md)
</dt> <dt>

[Benutzeroberflächenautomatisierungs-Unterstützung für Textinhalte](uiauto-ui-automation-textpattern-overview.md)
</dt> <dt>

[Arbeiten mit Text basierten Steuerelementen](uiauto-workingwithtextbasedcontrols.md)
</dt> </dl>

 

 




