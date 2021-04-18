---
title: Auschecken unnötiger Objekte
description: Wenn Sie überprüfen verwenden, um ein einfaches Steuerelement zu untersuchen, z. b. eine Schaltfläche "OK" im Microsoft WordPad-Zubehör, sehen Sie, dass diese übergeordneten Fenster Objekte auch mehrere unsichtbare untergeordnete Objekte enthalten.
ms.assetid: 30884e11-cc73-4bb8-9d9e-b9f1b53c4193
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb341881ee2ea503b1f74643723a1f90c8e5d1d5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106340414"
---
# <a name="screening-out-unnecessary-objects"></a>Auschecken unnötiger Objekte

Wenn Sie über [prüfen](inspect-objects.md) verwenden, um ein einfaches Steuerelement zu untersuchen, z. b. eine Schaltfläche "OK" im Microsoft WordPad-Zubehör, sehen Sie, dass diese übergeordneten Fenster Objekte auch mehrere unsichtbare untergeordnete Objekte enthalten. Diese nicht sichtbaren Objekte haben denselben Fenster Klassennamen wie das Steuerelement, und die [State-Eigenschaft](state-property.md) des [**Zustands Systems ist \_ \_ unsichtbar**](object-state-constants.md). In der folgenden Tabelle sind die unsichtbaren untergeordneten Objekte aufgelistet, die von Active Accessibility Microsoft für das-Steuerelement erstellt werden.



| Name          | Role                                                                  | ChildCount |
|---------------|-----------------------------------------------------------------------|------------|
| Anlage      | [**Rollen \_ System- \_ Menüleiste**](object-roles.md)     | 0          |
| Keine          | [**Rollen \_ System- \_ TitleBar**](object-roles.md)   | 5          |
| Asyl | [**Rollen \_ System- \_ Menüleiste**](object-roles.md)     | 0          |
| Rechtes    | [**Rollen \_ System- \_ Scrollleiste**](object-roles.md) | 5          |
| Ales  | [**Rollen \_ System- \_ Scrollleiste**](object-roles.md) | 5          |
| "Size Box"    | [**Rollen System-Zieh Punkt \_ \_**](object-roles.md)           | 0          |



 

Client Entwickler müssen diese Objekte des übergeordneten Fensters und die untergeordneten Objekte identifizieren und herausfiltern, da Sie keinen sinnvollen Informationen für Endbenutzer bereitstellen.

 

 




