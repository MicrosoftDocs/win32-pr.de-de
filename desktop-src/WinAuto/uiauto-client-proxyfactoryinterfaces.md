---
title: Proxyfactory-Schnittstellen für Clients
description: In diesem Abschnitt werden die proxyfactory-Schnittstellen für nicht verwaltete Benutzeroberflächenautomatisierungs-Client Anwendungen beschrieben
ms.assetid: 46c6720a-19c2-4ddd-893c-1a46af0642fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fc1827ab36a221dcd7f27e5b2a05de91931b0ad
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037458"
---
# <a name="proxy-factory-interfaces-for-clients"></a>Proxyfactory-Schnittstellen für Clients

In diesem Abschnitt werden die proxyfactory-Schnittstellen für nicht verwaltete Benutzeroberflächenautomatisierungs-Client Anwendungen beschrieben

## <a name="in-this-section"></a>In diesem Abschnitt



| Schnittstelle                                                                                      | BESCHREIBUNG                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Iuiautomationproxyfactory**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactory)<br/>               | Macht Eigenschaften und Methoden eines Objekts verfügbar, das einen Microsoft-Benutzeroberflächenautomatisierungs-Anbieter für Benutzeroberflächen Elemente erstellt, die keine native Unterstützung für die Benutzeroberflächen Automatisierung aufweisen. Diese Schnittstelle wird von Proxys implementiert.<br/>                                                                          |
| [**Iuiautomationproxyfactoriyentry**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactoryentry)<br/>     | Stellt eine proxyfactory in der von der Benutzeroberflächen Automatisierung verwalteten Tabelle dar und macht Eigenschaften und Methoden verfügbar, die von Client Anwendungen für die Interaktion mit [**iuiautomationproxyfactory**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactory) -Objekten verwendet werden können.<br/>                                   |
| [**Iuiautomationproxyfactoriymapping**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactorymapping)<br/> | Macht Eigenschaften und Methoden für eine Tabelle von proxyfactorys verfügbar. Jeder Tabelleneintrag wird durch eine [**iuiautomationproxyfactor yentry**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactoryentry) -Schnittstelle dargestellt. Die Einträge werden in der Reihenfolge angezeigt, in der das System versucht, die Proxys zu verwenden.<br/> |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[UI-Automatisierungs Clients](uiauto-entry-uiautoclientsforwin32apps.md)
</dt> </dl>

 

 





