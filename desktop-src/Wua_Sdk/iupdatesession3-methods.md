---
description: Die IUpdateSession3-Schnittstelle definiert die folgenden Methoden.
ms.assetid: 8015443a-e232-44ab-b53a-e8cc4acd4dd3
title: IUpdateSession3-Methoden
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bd4126d8bae9e1ba768e574fd9520bdb6cf3d45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128276"
---
# <a name="iupdatesession3-methods"></a>IUpdateSession3-Methoden

Die [**IUpdateSession3**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession3) -Schnittstelle definiert die folgenden Methoden.



| Methode                                                                           | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**"Kreateupdateservicemanager"**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesession3-createupdateservicemanager) | Gibt einen Zeiger auf eine [**IUpdateServiceManager2**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservicemanager2) -Schnittstelle für die Sitzung zurück.                                                                                                                                                                                                                |
| [**Queryhistory**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesession3-queryhistory)                             | Gibt einen Zeiger auf eine [**iupdatehistoryentrycollection**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatehistoryentrycollection) -Schnittstelle zurück. Die-Schnittstelle enthält übereinstimmende Ereignisdaten Sätze auf dem Computer. Dadurch wird der Computer von der [**queryhistory**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesession3-queryhistory) -Methode synchron nach dem Verlauf von Update Ereignissen abgefragt. |



 

Informationen zu den Membern, die von dieser Schnittstelle geerbt werden, finden Sie unter den folgenden Schnittstellen:

-   [**IUpdateSession2**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession2)
-   [**Iupdatesession**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession)

 

 



