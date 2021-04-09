---
description: Die iupdateingestaller-Schnittstelle definiert die folgenden Eigenschaften.
ms.assetid: 876a2150-40a1-42a3-bc9a-05dec94fccd3
title: Iupdateingestaller-Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77df235c49e7b6f27b0f93ec3b0c4def12135065
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862795"
---
# <a name="iupdateinstaller-properties"></a>Iupdateingestaller-Eigenschaften

Die [**iupdateingestaller**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateinstaller) -Schnittstelle definiert die folgenden Eigenschaften.



| Eigenschaft                                                                                      | BESCHREIBUNG                                                                                                                           |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [**Allowsourceaufforderungen**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_allowsourceprompts)                             | Ruft einen booleschen Wert ab, der angibt, ob beim Installieren der Updates Quell Aufforderungen für den Benutzer angezeigt werden sollen, oder legt diesen fest.                  |
| [**ClientApplicationID**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_clientapplicationid)                           | Ruft die aktuelle Client Anwendung ab und legt Sie fest.                                                                                         |
| [**IsBusy**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_isbusy)                                                     | Ruft einen booleschen Wert ab, der angibt, ob auf einem Computer zu einem bestimmten Zeitpunkt eine Installation oder eine Deinstallation ausgeführt wird.        |
| [**Isforced**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_isforced)                                                 | Ruft einen booleschen Wert ab, der angibt, ob ein Update zwangsweise installiert oder deinstalliert wird, oder legt ihn fest.                                       |
| [**Klammer**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_parenthwnd)                                             | Ruft ein Handle für das übergeordnete Fenster ab, das ein Dialogfeld enthalten kann, oder legt dieses fest.                                                            |
| [**Fenster Fenster**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_parentwindow)                                         | Dient zum Abrufen und Festlegen der-Schnittstelle, die das übergeordnete Fenster darstellt, das ein Dialogfeld enthalten kann.                                          |
| [**Rebootrequiredbeforeingestallations**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_rebootrequiredbeforeinstallation) | Ruft einen booleschen Wert ab, der angibt, ob vor dem Installieren oder Deinstallieren von Updates ein Systemneustart erforderlich ist.                   |
| [**Updates**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_updates)                                                   | Ruft eine Schnittstelle ab, die eine schreibgeschützte Auflistung der für die Installation oder die Installation angegebenen Updates enthält, oder legt Sie fest. |



 

 

 



