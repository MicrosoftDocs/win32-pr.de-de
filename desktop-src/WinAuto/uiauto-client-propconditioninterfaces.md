---
title: Schnittstellen für Eigenschafts Bedingungen für Clients
description: In diesem Abschnitt werden Eigenschaften Bedingungs Schnittstellen für Benutzeroberflächenautomatisierungs-Clients für Microsoft Win32-Anwendungen beschrieben.
ms.assetid: cea34e47-03a9-4ff9-9019-427a2a3e13d6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00f840706d4f9e340cae86813a4992400791dccd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039079"
---
# <a name="property-condition-interfaces-for-clients"></a>Schnittstellen für Eigenschafts Bedingungen für Clients

In diesem Abschnitt werden Eigenschaften Bedingungs Schnittstellen für Benutzeroberflächenautomatisierungs-Clients für Microsoft Win32-Anwendungen beschrieben.

## <a name="in-this-section"></a>In diesem Abschnitt



| Schnittstelle                                                                                  | BESCHREIBUNG                                                                                                                                                        |
|--------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Iuiautomationandcondition**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationandcondition)<br/>           | Macht Eigenschaften und Methoden verfügbar, die Microsoft UI Automation-Client Anwendungen verwenden können, um Informationen über eine und eine-basierte Eigenschafts Bedingung abzurufen. <br/> |
| [**Iuiautomationboolcondition**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationboolcondition)<br/>         | Stellt eine Bedingung dar, die entweder **true** (alle Elemente auswählt) oder **false** (wählt keine Elemente) sein kann.<br/>                                           |
| [**Iuiautomationcondition**](/windows/win32/api/uiautomationclient/nn-uiautomationclient-iuiautomationcondition)<br/>                 | Dies ist die primäre Schnittstelle für Bedingungen, die beim Suchen nach Elementen in der Benutzeroberflächenautomatisierungs-Struktur beim Filtern verwendet werden.<br/>                                   |
| [**Iuiautomationnotcondition**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationnotcondition)<br/>           | Stellt eine Bedingung dar, die das negative einer anderen Bedingung ist.<br/>                                                                                       |
| [**Iuiautomationorcondition**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationorcondition)<br/>             | Stellt eine Bedingung dar, die aus mehreren Bedingungen besteht, von denen mindestens ein true sein muss.<br/>                                                              |
| [**Iuiautomationpropertycondition**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationpropertycondition)<br/> | Stellt eine Bedingung dar, die auf einem Eigenschafts Wert basiert, mit dem Benutzeroberflächenautomatisierungs-Elemente gesucht werden.<br/>                                                           |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[UI-Automatisierungs Clients](uiauto-entry-uiautoclientsforwin32apps.md)
</dt> </dl>

 

