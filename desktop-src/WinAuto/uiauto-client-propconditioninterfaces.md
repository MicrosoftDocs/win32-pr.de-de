---
title: Eigenschaftenbedingungsschnittstellen für Clients
description: In diesem Abschnitt werden Eigenschaftenbedingungsschnittstellen für Benutzeroberflächenautomatisierung für Microsoft Win32-Anwendungen beschrieben.
ms.assetid: cea34e47-03a9-4ff9-9019-427a2a3e13d6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 447c2bf9a67a5fc9cbd303e86599502e2b6154f53485af5a57bf13a6268fa930
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119133483"
---
# <a name="property-condition-interfaces-for-clients"></a>Eigenschaftenbedingungsschnittstellen für Clients

In diesem Abschnitt werden Eigenschaftenbedingungsschnittstellen für Benutzeroberflächenautomatisierung für Microsoft Win32-Anwendungen beschrieben.

## <a name="in-this-section"></a>In diesem Abschnitt



| Schnittstelle                                                                                  | BESCHREIBUNG                                                                                                                                                        |
|--------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IUIAutomationAndCondition**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationandcondition)<br/>           | Macht Eigenschaften und Methoden verfügbar, die Microsoft Benutzeroberflächenautomatisierung Clientanwendungen verwenden können, um Informationen zu einer AND-basierten Eigenschaftenbedingung abzurufen. <br/> |
| [**IUIAutomationBoolCondition**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationboolcondition)<br/>         | Stellt eine Bedingung dar, die entweder **TRUE** (wählt alle Elemente aus) oder **FALSE** (keine Elemente auswählt) sein kann.<br/>                                           |
| [**IUIAutomationCondition**](/windows/win32/api/uiautomationclient/nn-uiautomationclient-iuiautomationcondition)<br/>                 | Dies ist die primäre Schnittstelle für Bedingungen, die beim Filtern bei der Suche nach Elementen in der Benutzeroberflächenautomatisierung werden.<br/>                                   |
| [**IUIAutomationNotCondition**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationnotcondition)<br/>           | Stellt eine Bedingung dar, die negativ einer anderen Bedingung ist.<br/>                                                                                       |
| [**IUIAutomationOrCondition**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationorcondition)<br/>             | Stellt eine Bedingung dar, die aus mehreren Bedingungen besteht, von denen mindestens eine erfüllt sein muss.<br/>                                                              |
| [**IUIAutomationPropertyCondition**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationpropertycondition)<br/> | Stellt eine Bedingung dar, die auf einem Eigenschaftswert basiert, der zum Suchen nach Benutzeroberflächenautomatisierung wird.<br/>                                                           |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Benutzeroberflächenautomatisierung Clients](uiauto-entry-uiautoclientsforwin32apps.md)
</dt> </dl>

 

