---
title: Fensterloses ActiveX Barrierefreiheit
description: In diesem Abschnitt wird beschrieben, wie Sie die Windows Barrierefreiheits-API verwenden, um sicherzustellen, dass fensterlose Microsoft ActiveX-Steuerelemente zugänglich sind.
ms.assetid: 93CBCF20-DADF-4A63-BE60-F2A0D8810C62
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3842dd6b9ec18b745e043841936dd811afd1580779d276290057c2fe6d2194cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118563455"
---
# <a name="windowless-activex-control-accessibility"></a>Fensterloses ActiveX Barrierefreiheit

In diesem Abschnitt wird beschrieben, wie Sie die Windows Barrierefreiheits-API verwenden, um sicherzustellen, dass fensterlose Microsoft ActiveX-Steuerelemente zugänglich sind.

Windows 8 enthält neue Windows Barrierefreiheits-API, die die Implementierung der Barrierefreiheit für fensterlose steuerelemente ActiveX vereinfachen. Die API enthält Schnittstellen, die in einem fensterlosen Steuerelement und im Steuerelementcontainer implementiert werden, sodass das fensterlose Steuerelement und sein Container zusammenarbeiten können, um Barrierefreiheitsinformationen über das fensterlose Steuerelement zur Verfügung zu stellen. Die API unterstützt die folgenden Szenarien:

-   Microsoft Active Accessibility fensterlose Steuerelemente, die in einem Microsoft Active Accessibility-Steuerelementcontainer gehostet werden.
-   Microsoft Active Accessibility fensterlose Steuerelemente, die in einem Microsoft Benutzeroberflächenautomatisierung-Steuerelementcontainer gehostet werden.
-   Benutzeroberflächenautomatisierung fensterlose Steuerelemente, die in einem Microsoft Active Accessibility-Steuerelementcontainer gehostet werden.
-   Benutzeroberflächenautomatisierung fensterlose Steuerelemente, die in einem Benutzeroberflächenautomatisierung-Steuerelementcontainer gehostet werden.

In der folgenden Tabelle sind die Schnittstellen aufgeführt, die fensterlose Steuerelemente ActiveX und die Objekte identifizieren, die die Schnittstellen implementieren.



| Object              | MSAA                                                                             | Benutzeroberflächenautomatisierung                                                                                     |
|---------------------|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| Steuerelementobjekt      | [**Iaccessiblehandler**](/windows/desktop/api/oleacc/nn-oleacc-iaccessiblehandler)                                 |                                                                                                   |
| Steuerungsstandort        | [**IAccessibleWindowlessSite**](/windows/desktop/api/oleacc/nn-oleacc-iaccessiblewindowlesssite)        | [**IRawElementProviderWindowlessSite**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementproviderwindowlesssite)         |
| Stamm des Hostfensters | [**IAccessibleHostingElementProviders**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessiblehostingelementproviders) | [**IRawElementProviderHostingAccessibles**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementproviderhostingaccessibles) |



 

## <a name="in-this-section"></a>In diesem Abschnitt

-   [How to Use Benutzeroberflächenautomatisierung to Make a Windowless ActiveX Control Accessible](use-ui-automation-to-make-an-windowless-activex-control-accessible.md)
-   [How to Use MSAA to Make a Windowless ActiveX Control Accessible](use-msaa-to-make-an-windowless-activex-control-accessible.md)
-   [Hosten eines fensterlosen Benutzeroberflächenautomatisierung-Steuerelements ActiveX Hosten](host-a-ui-automation-windowless-activex-control.md)
-   [Hosten eines fensterlosen MSAA-steuerelements ActiveX](host-an-msaa-windowless-activex-control.md)

 

 