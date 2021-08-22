---
description: Die IUpdateInstaller-Schnittstelle definiert die folgenden Eigenschaften.
ms.assetid: 876a2150-40a1-42a3-bc9a-05dec94fccd3
title: IUpdateInstaller-Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49c6076e395e98ef21cd54fbf45ffdc5e57bc29fa8ceffc78c16d9a9a0d2bc4a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119049148"
---
# <a name="iupdateinstaller-properties"></a>IUpdateInstaller-Eigenschaften

Die [**IUpdateInstaller-Schnittstelle**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateinstaller) definiert die folgenden Eigenschaften.



| Eigenschaft                                                                                      | Beschreibung                                                                                                                           |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [**AllowSourcePrompts**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_allowsourceprompts)                             | Ruft einen booleschen Wert ab, der angibt, ob dem Benutzer beim Installieren der Updates Quellaufforderungen angezeigt werden sollen, und legt diesen fest.                  |
| [**ClientApplicationID**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_clientapplicationid)                           | Ruft die aktuelle Clientanwendung ab und legt sie fest.                                                                                         |
| [**Isbusy**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_isbusy)                                                     | Ruft einen booleschen Wert ab, der angibt, ob eine Installation oder Deinstallation auf einem Computer zu einem bestimmten Zeitpunkt ausgeführt wird.        |
| [**IsForced**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_isforced)                                                 | Ruft einen booleschen Wert ab, der angibt, ob ein Update installiert oder deinstalliert werden soll, oder legt diesen fest.                                       |
| [**ParentHwnd**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_parenthwnd)                                             | Ruft ein Handle für das übergeordnete Fenster ab, das ein Dialogfeld enthalten kann, und legt dieses fest.                                                            |
| [**ParentWindow**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_parentwindow)                                         | Ruft die Schnittstelle ab, die das übergeordnete Fenster darstellt, das ein Dialogfeld enthalten kann, und legt diese fest.                                          |
| [**RebootRequiredBeforeInstallation**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_rebootrequiredbeforeinstallation) | Ruft einen booleschen Wert ab, der angibt, ob ein Systemneustart erforderlich ist, bevor Updates installiert oder deinstalliert werden.                   |
| [**Updates**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_updates)                                                   | Ruft eine Schnittstelle ab, die eine schreibgeschützte Auflistung der Updates enthält, die für die Installation oder Deinstallation angegeben sind, und legt diese fest. |



 

 

 



