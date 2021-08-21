---
title: Grundlegendes zum Benutzeroberflächenautomatisierung Textobjektmodell
description: In diesem Thema wird beschrieben, Benutzeroberflächenautomatisierung Microsoft-Clientanwendungen auf den Textinhalt eines textbasierten Steuerelements zugreifen.
ms.assetid: 8545EBA3-6995-4336-A197-27CE3A3339EE
keywords:
- Clients,Grundlegendes Benutzeroberflächenautomatisierung Textobjektmodells
- Clients,textbasierte Steuerelemente
- Clients,Textbereiche
- Clients,Textsteuermuster
- clients,TextRange-Steuerelementmuster
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 655f291e9cc11d925f947617fe31be96ebd81a2dbff73506a0e474dcde9e4446
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118823892"
---
# <a name="understanding-the-ui-automation-text-object-model"></a>Grundlegendes zum Benutzeroberflächenautomatisierung Textobjektmodell

In diesem Thema wird beschrieben, Benutzeroberflächenautomatisierung Microsoft-Clientanwendungen auf den Textinhalt eines textbasierten Steuerelements zugreifen.

-   [Steuerelementspezifisches Objektmodell](#control-specific-object-model)
-   [Zugehörige Themen](#related-topics)

Textbasierte Steuerelemente machen Textinhalte für Benutzeroberflächenautomatisierung Clientanwendungen über ein einfaches Textobjektmodell verfügbar. Clientanwendungen haben Zugriff auf das Textobjektmodell über die [Text-](uiauto-about-text-and-textrange-patterns.md) und TextRange-Steuerelementmusterschnittstellen, einschließlich [**IUIAutomationTextPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextpattern) und [**IUIAutomationTextRange.**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextrange) Clientanwendungen können diese Schnittstellen verwenden, um Textinhalte, Textattribute und eingebettete Objekte wie Tabellen und Links aus textbasierten Steuerelementen abzurufen.

Steuerelementtypen, die das Benutzeroberflächenautomatisierung Textobjektmodell unterstützen, umfassen die [Steuerelementtypen Bearbeiten](uiauto-supporteditcontroltype.md) [und](uiauto-supportdocumentcontroltype.md) Dokument. Andere Steuerelementtypen wie [QuickInfo und](uiauto-supporttooltipcontroltype.md) [Text](uiauto-supporttextcontroltype.md) unterstützen möglicherweise auch das Textobjektmodell, dies ist jedoch nicht erforderlich.

> [!Note]  
> Das Benutzeroberflächenautomatisierung Textobjektmodell bietet keine Möglichkeit zum Einfügen oder Ändern von Text. Einige Steuerelemente ermöglichen jedoch das Einfügen oder Ändern von Text entweder über die [**IUIAutomationValuePattern-Schnittstelle**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationvaluepattern) oder über direkte Tastatureingaben.

 

## <a name="control-specific-object-model"></a>Steuerelementspezifisches Objektmodell

Ein textbasiertes Steuerelement, das ein eigenes Dokumentobjektmodell (DOM) implementiert, kann das DOM verfügbar machen, indem es das [ObjectModel-Steuerelementmuster](uiauto-implementingobjectmodel.md) implementiert. Durch das Verfügbar machen des DOM können Clientanwendungen besseren Zugriff auf den Inhalt eines textbasierten Steuerelements erhalten und diesen steuern.

Eine Clientanwendung kann ermitteln, ob ein bestimmtes textbasiertes Steuerelement ein DOM implementiert, indem die [**IUIAutomationElement-Schnittstelle**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) des Steuerelements abgerufen wird. Rufen Sie dann die [**IUIAutomationElement::GetCurrentPropertyValue-Methode**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue) auf, und geben Sie dabei den [**\_ UIA-Eigenschaftenbezeichner IsObjectModelPatternAvailablePropertyId**](uiauto-control-pattern-availability-propids.md) und eine Variante an, die TRUE empfängt, wenn das Steuerelement ein DOM implementiert.

Rufen Sie für den Zugriff auf das DOM die [**IUIAutomationElement::GetCurrentPattern-Methode**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpattern) auf, und geben Sie dabei den [**UIA \_ ObjectModelPatternId-Steuerelementmusterbezeichner**](uiauto-controlpattern-ids.md) und eine Variable an, die die [**IUIAutomationObjectModelPattern-Schnittstelle**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationobjectmodelpattern) empfängt. Rufen Sie [**die IUIAutomationObjectModelPattern::GetUnderlyingObjectModel-Methode**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationobjectmodelpattern-getunderlyingobjectmodel) auf, um die DOM-Schnittstelle abzurufen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Text- und TextRange-Steuerelementmuster](uiauto-implementingtextandtextrange.md)
</dt> <dt>

[Benutzeroberflächenautomatisierung Unterstützung für Textinhalte](uiauto-ui-automation-textpattern-overview.md)
</dt> <dt>

[Arbeiten mit textbasierten Steuerelementen](uiauto-workingwithtextbasedcontrols.md)
</dt> </dl>

 

 




