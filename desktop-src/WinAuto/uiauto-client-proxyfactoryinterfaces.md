---
title: Proxy Factory-Schnittstellen für Clients
description: In diesem Abschnitt werden die Proxy factory-Schnittstellen für nicht verwaltete Benutzeroberflächenautomatisierung Clientanwendungen beschrieben.
ms.assetid: 46c6720a-19c2-4ddd-893c-1a46af0642fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e92264691c35cefe3ffaf246d2e73bac5ea7dc3363a4f220eb0ddecb9f15030
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119614359"
---
# <a name="proxy-factory-interfaces-for-clients"></a>Proxy Factory-Schnittstellen für Clients

In diesem Abschnitt werden die Proxy factory-Schnittstellen für nicht verwaltete Benutzeroberflächenautomatisierung Clientanwendungen beschrieben.

## <a name="in-this-section"></a>In diesem Abschnitt



| Schnittstelle                                                                                      | BESCHREIBUNG                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IUIAutomationProxyFactory**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactory)<br/>               | Macht Eigenschaften und Methoden eines Objekts verfügbar, das einen Microsoft Benutzeroberflächenautomatisierung-Anbieter für Benutzeroberflächenelemente erstellt, die keine native Unterstützung für Benutzeroberflächenautomatisierung. Diese Schnittstelle wird von Proxys implementiert.<br/>                                                                          |
| [**IUIAutomationProxyFactoryEntry**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactoryentry)<br/>     | Stellt eine Proxyfactory in der von Benutzeroberflächenautomatisierung verwalteten Tabelle dar und macht Eigenschaften und Methoden verfügbar, die von Clientanwendungen für die Interaktion mit [**IUIAutomationProxyFactory-Objekten verwendet werden**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactory) können.<br/>                                   |
| [**IUIAutomationProxyFactoryMapping**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactorymapping)<br/> | Macht Eigenschaften und Methoden für eine Tabelle von Proxy factorys verfügbar. Jeder Tabelleneintrag wird durch eine [**IUIAutomationProxyFactoryEntry-Schnittstelle**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactoryentry) dargestellt. Die Einträge befinden sich in der Reihenfolge, in der das System versucht, die Proxys zu verwenden.<br/> |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Benutzeroberflächenautomatisierung Clients](uiauto-entry-uiautoclientsforwin32apps.md)
</dt> </dl>

 

 





