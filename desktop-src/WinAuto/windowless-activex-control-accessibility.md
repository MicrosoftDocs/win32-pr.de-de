---
title: Barrierefreiheit für das fensterlose ActiveX-Steuerelement
description: In diesem Abschnitt wird beschrieben, wie Sie die Windows-Barrierefreiheits-API verwenden, um sicherzustellen, dass auf fensterlose Microsoft ActiveX-Steuerelemente
ms.assetid: 93CBCF20-DADF-4A63-BE60-F2A0D8810C62
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6eb0489cdd5de3ac34df361bfa3e7b3624ee18f3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390706"
---
# <a name="windowless-activex-control-accessibility"></a>Barrierefreiheit für das fensterlose ActiveX-Steuerelement

In diesem Abschnitt wird beschrieben, wie Sie die Windows-Barrierefreiheits-API verwenden, um sicherzustellen, dass auf fensterlose Microsoft ActiveX-Steuerelemente

Windows 8 enthält neue API-Schnittstellen für die Barrierefreiheit von Windows, die die Implementierung von Barrierefreiheit für fensterlose ActiveX-Steuerelemente vereinfachen. Die API enthält Schnittstellen, die auf einem fensterlosen Steuerelement und im Steuerelement Container implementiert werden, sodass das fensterlose Steuerelement und sein Container zusammenarbeiten können, um Barrierefreiheits Informationen über das fensterlose Steuerelement bereitzustellen. Die API unterstützt die folgenden Szenarien:

-   Microsoft Active Accessibility fensterlose Steuerelemente, die in einem Microsoft Active Accessibility Control-Container gehostet werden.
-   Microsoft Active Accessibility fensterlose Steuerelemente, die in einem Microsoft UI Automation Control-Container gehostet werden.
-   Benutzeroberflächen Automatisierung fensterlose Steuerelemente, die in einem Microsoft Active Accessibility Control-Container gehostet werden.
-   Benutzeroberflächenautomatisierungs-Steuerelemente, die in einem Benutzeroberflächenautomatisierungs-Steuerungs Container gehostet werden

In der folgenden Tabelle werden die Schnittstellen aufgelistet, die fensterlose ActiveX-Steuerelemente unterstützen und die Objekte identifizieren, die die Schnittstellen implementieren.



| Object              | MSAA                                                                             | Benutzeroberflächenautomatisierung                                                                                     |
|---------------------|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| Control-Objekt      | [**IAccessibleHandler**](/windows/desktop/api/oleacc/nn-oleacc-iaccessiblehandler)                                 |                                                                                                   |
| Steuerungs Website        | [**Iaccessiblewindowlesssite**](/windows/desktop/api/oleacc/nn-oleacc-iaccessiblewindowlesssite)        | [**Irawelementproviderwindowlesssite**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementproviderwindowlesssite)         |
| Stamm des Host Fensters | [**Iaccessiblehostingelementproviders**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessiblehostingelementproviders) | [**Irawelementproviderhostingaccessibles**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementproviderhostingaccessibles) |



 

## <a name="in-this-section"></a>In diesem Abschnitt

-   [Verwenden der Benutzeroberflächen Automatisierung zum Zugreifen auf ein fensterloses ActiveX-Steuerelement](use-ui-automation-to-make-an-windowless-activex-control-accessible.md)
-   [Verwenden von MSAA zum Zugreifen auf ein fensterloses ActiveX-Steuerelement](use-msaa-to-make-an-windowless-activex-control-accessible.md)
-   [Hosten eines fensterlosen ActiveX-Steuer Elements für die Benutzeroberflächen Automatisierung](host-a-ui-automation-windowless-activex-control.md)
-   [Hosten eines Windows-losen ActiveX-Steuer Elements mit MSAA](host-an-msaa-windowless-activex-control.md)

 

 