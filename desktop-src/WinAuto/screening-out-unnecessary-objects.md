---
title: Aufsparen unnötiger Objekte
description: Wenn Sie überprüfen verwenden, um ein einfaches Steuerelement zu untersuchen, z. B. eine SCHALTFLÄCHE OK im Microsoft WordPad-Accessory, können Sie sehen, dass diese übergeordneten Fensterobjekte auch mehrere unsichtbare untergeordnete Objekte enthalten.
ms.assetid: 30884e11-cc73-4bb8-9d9e-b9f1b53c4193
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c52dc54f2c32be3aff3e535427668943cf1ee21423636e3be8c018f6e3257b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117745283"
---
# <a name="screening-out-unnecessary-objects"></a>Aufsparen unnötiger Objekte

Wenn Sie [](inspect-objects.md) überprüfen verwenden, um ein einfaches Steuerelement zu untersuchen, z. B. eine SCHALTFLÄCHE OK im Microsoft WordPad-Accessory, können Sie sehen, dass diese übergeordneten Fensterobjekte auch mehrere unsichtbare untergeordnete Objekte enthalten. Diese unsichtbaren Objekte haben den gleichen Fensterklassennamen wie das -Steuerelement und die [State-Eigenschaft](state-property.md) [**von STATE SYSTEM \_ \_ INVISIBLE**](object-state-constants.md). In der folgenden Tabelle sind die unsichtbaren untergeordneten Objekte aufgeführt, Microsoft Active Accessibility für das -Steuerelement erstellt werden.



| Name          | Role                                                                  | ChildCount |
|---------------|-----------------------------------------------------------------------|------------|
| "System"      | [**MENÜLEISTE \_ \_ "ROLLENSYSTEM"**](object-roles.md)     | 0          |
| Keine          | [**ROLE \_ SYSTEM \_ TITLEBAR**](object-roles.md)   | 5          |
| "Anwendung" | [**MENÜLEISTE \_ \_ "ROLLENSYSTEM"**](object-roles.md)     | 0          |
| "Vertikal"    | [**\_ \_ ROLLENSYSTEM-BILDLAUFLEISTE**](object-roles.md) | 5          |
| "Horizontal"  | [**\_ \_ ROLLENSYSTEM-BILDLAUFLEISTE**](object-roles.md) | 5          |
| "Size Box"    | [**ROLE \_ \_ SYSTEM-GREIFER**](object-roles.md)           | 0          |



 

Cliententwickler müssen diese übergeordneten Fensterobjekte und unsichtbaren untergeordneten Objekte identifizieren und herausfiltern, da sie endbenutzern keine aussagekräftigen Informationen bereitstellen.

 

 




