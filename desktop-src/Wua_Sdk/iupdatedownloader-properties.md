---
description: Die IUpdateDownloader-Schnittstelle definiert die folgenden Eigenschaften.
ms.assetid: b6a30356-f97d-408f-becd-a467e9f8e79f
title: IUpdateDownloader-Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf66fbdad678ef6a78d0fa049ecb59c34be2ca9d08c873e24e82c35c9d1eb1c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117738289"
---
# <a name="iupdatedownloader-properties"></a>IUpdateDownloader-Eigenschaften

Die [**IUpdateDownloader-Schnittstelle**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatedownloader) definiert die folgenden Eigenschaften.



| Eigenschaft                                                             | BESCHREIBUNG                                                                                                                                                                |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ClientApplicationID**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-get_clientapplicationid) | Ruft die aktuelle Clientanwendung ab und legt sie fest.                                                                                                                              |
| [**IsForced**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-get_isforced)                       | Ruft einen booleschen Wert ab, der angibt, ob der Windows Update-Agent (WUA) das Herunterladen von Updates erzwingt, die bereits installiert sind oder nicht installiert werden können, und legt diesen fest. |
| [**Priorität**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-get_priority)                       | Ruft die Prioritätsstufe des Downloads ab und legt sie fest.                                                                                                                          |
| [**Updates**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-get_updates)                         | Ruft eine Schnittstelle ab, die eine schreibgeschützte Auflistung der Updates enthält, die für den Download angegeben sind, und legt diese fest.                                                            |



 

 

 



