---
title: Benutzeroberflächenautomatisierungs-Element Schnittstellen für Clients
description: In diesem Abschnitt werden die Schnittstellen beschrieben, die vom Microsoft UI Automation Client verwendet werden, um Benutzeroberflächenautomatisierungs-Elemente zu suchen, darauf zuzugreifen
ms.assetid: dd7cdcf1-3511-424f-b729-b71a7e11cdd8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a08859784d18905adbed463ac776bb2e717211f
ms.sourcegitcommit: 4c00910ed754d7d0a68c9a833751d714c06e3b39
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "103957693"
---
# <a name="ui-automation-element-interfaces-for-clients"></a>Benutzeroberflächenautomatisierungs-Element Schnittstellen für Clients

In diesem Abschnitt werden die Schnittstellen beschrieben, die vom Microsoft UI Automation Client verwendet werden, um Benutzeroberflächenautomatisierungs-Elemente zu suchen, darauf zuzugreifen

## <a name="in-this-section"></a>In diesem Abschnitt



| Schnittstelle                                                                        | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Iuiautomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation)<br/>                         | Macht Methoden verfügbar, mit denen Benutzeroberflächenautomatisierungs-Client Anwendungen Benutzeroberflächenautomatisierungs-Elemente erkennen, zugreifen und Filtern können. Die Benutzeroberflächen Automatisierung macht alle Elemente der Benutzeroberflächen Automatisierung als Objekt verfügbar, das von der [**iuiautomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) -Schnittstelle dargestellt wird. Die Member dieser Schnittstelle sind nicht spezifisch für ein bestimmtes Element.<br/> |
| [**IUIAutomation2**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation2)<br/>                       | Erweitert die [**iuiautomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) -Schnittstelle, um zusätzliche Methoden zum Steuern der Benutzeroberflächenautomatisierungs-Funktionalität bereitzustellen<br/>                                                                                                                                                                                                   |
| [**IUIAutomation3**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation3)<br/>                       | Erweitert die [**IUIAutomation2**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation2) -Schnittstelle, um zusätzliche Methoden zum Steuern der Benutzeroberflächenautomatisierungs-Funktionalität verfügbar<br/>                                                                                                                                                                                                 |
| [**IUIAutomation4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation4)<br/>                       | Erweitert die [**IUIAutomation3**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation3) -Schnittstelle, um zusätzliche Methoden zum Steuern der Benutzeroberflächenautomatisierungs-Funktionalität verfügbar<br/>                                                                                                                                                                                                 |
| [**IUIAutomation5**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation5)<br/>                       | Erweitert die [**IUIAutomation4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation4) -Schnittstelle, um zusätzliche Methoden zum Steuern der Benutzeroberflächenautomatisierungs-Funktionalität verfügbar<br/>                                                                                                                                                                                                 |
| [**IUIAutomation6**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation6)<br/>                       | Erweitert die [**IUIAutomation5**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation5) -Schnittstelle, um zusätzliche Methoden zum Steuern der Benutzeroberflächenautomatisierungs-Funktionalität verfügbar<br/>                                                                                                                                                                                                 |
| [**Iuiautomationcacherequest**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationcacherequest)<br/> | Macht Eigenschaften und Methoden einer Cache Anforderung verfügbar. Client Anwendungen verwenden diese Schnittstelle, um die Eigenschaften und Steuerelement Muster anzugeben, die zwischengespeichert werden, wenn ein Benutzeroberflächenautomatisierungs-Element abgerufen wird.<br/>                                                                                                                                                 |
| [**Iuiautomationelement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement)<br/>           | Macht Methoden und Eigenschaften für ein Benutzeroberflächenautomatisierungs-Element verfügbar, das ein Benutzeroberflächen Element darstellt. <br/>                                                                                                                                                                                                                                                        |
| [**IUIAutomationElement2**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement2)<br/>         | Erweitert die [**iuiautomationelement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) -Schnittstelle. <br/>                                                                                                                                                                                                                                                             |
| [**IUIAutomationElement3**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement3)<br/>         | Erweitert die [**IUIAutomationElement2**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement2) -Schnittstelle. <br/>                                                                                                                                                                                                                                                           |
| [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4)<br/>         | Erweitert die [**IUIAutomationElement3**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement3) -Schnittstelle. <br/>                                                                                                                                                                                                                                                           |
| [**IUIAutomationElement5**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement5)<br/>         | Erweitert die [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) -Schnittstelle, um Zugriff auf aktuelle und zwischengespeicherte Daten zu erstellen.<br/>                                                                                                                                                                                                      |
| [**IUIAutomationElement6**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement6)<br/>         | Erweitert die [**IUIAutomationElement5**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement5) -Schnittstelle, um Zugriff auf aktuelle und zwischengespeicherte vollständige Beschreibungen bereitzustellen.<br/>                                                                                                                                                                                                  |
| [**IUIAutomationElement7**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement7)<br/>         | Erweitert die [**IUIAutomationElement6**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement6) -Schnittstelle.<br/>                                                                                                                                                                                                                                                            |
| [**IUIAutomationElement8**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement8)<br/>         | Erweitert die [**IUIAutomationElement7**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement7) -Schnittstelle.<br/>                                                                                                                                                                                                                                                            |
| [**IUIAutomationElement9**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement9)<br/>         | Erweitert die [**IUIAutomationElement8**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement8) -Schnittstelle.<br/>                                                                                                                                                                                                                                                            |
| [**Iuiautomationelementarray**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelementarray)<br/> | Stellt eine Auflistung von Benutzeroberflächenautomatisierungs-Elementen dar.<br/>                                                                                                                                                                                                                                                                                              |
| [**Iuiautomationregistrar**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationregistrar)<br/>       | Macht Methoden zum Registrieren neuer Steuerelement Muster, Eigenschaften und Ereignisse verfügbar.<br/>                                                                                                                                                                                                                                                                   |
| [**Iuiautomationtreewalker**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtreewalker)<br/>     | Macht Eigenschaften und Methoden verfügbar, mit denen Benutzeroberflächenautomatisierungs-Client Anwendungen die Benutzeroberflächenautomatisierungs-Elemente auf dem Desktop anzeigen und navigieren. <br/>                                                                                                                                                                                                      |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[UI-Automatisierungs Clients](uiauto-entry-uiautoclientsforwin32apps.md)
</dt> </dl>

 

 





