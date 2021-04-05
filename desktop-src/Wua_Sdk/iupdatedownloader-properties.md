---
description: Die iupdatedownloader-Schnittstelle definiert die folgenden Eigenschaften.
ms.assetid: b6a30356-f97d-408f-becd-a467e9f8e79f
title: Iupdatedownloader-Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99c16aa762bcc14dc1919ef91d162752652c327e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752081"
---
# <a name="iupdatedownloader-properties"></a>Iupdatedownloader-Eigenschaften

Die [**iupdatedownloader**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatedownloader) -Schnittstelle definiert die folgenden Eigenschaften.



| Eigenschaft                                                             | BESCHREIBUNG                                                                                                                                                                |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ClientApplicationID**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-get_clientapplicationid) | Ruft die aktuelle Client Anwendung ab und legt Sie fest.                                                                                                                              |
| [**Isforced**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-get_isforced)                       | Ruft einen booleschen Wert ab, der angibt, ob der Windows Update-Agent (WUA) das Herunterladen von Updates erzwingt, die bereits installiert sind oder nicht installiert werden können, oder legt diesen fest. |
| [**Priorität**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-get_priority)                       | Ruft die Prioritäts Ebene des Downloads ab und legt Sie fest.                                                                                                                          |
| [**Updates**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-get_updates)                         | Ruft eine Schnittstelle ab, die eine schreibgeschützte Auflistung der für den Download angegebenen Updates enthält, oder legt Sie fest.                                                            |



 

 

 



