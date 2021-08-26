---
description: Die IUpdateSession3-Schnittstelle definiert die folgenden Methoden.
ms.assetid: 8015443a-e232-44ab-b53a-e8cc4acd4dd3
title: IUpdateSession3-Methoden
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 845af7bc4858aa713a3c044562c91325d337e49da0f413a3b2536c0129a85bc6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119896740"
---
# <a name="iupdatesession3-methods"></a>IUpdateSession3-Methoden

Die [**IUpdateSession3-Schnittstelle**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession3) definiert die folgenden Methoden.



| Methode                                                                           | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateUpdateServiceManager**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesession3-createupdateservicemanager) | Gibt einen Zeiger auf eine [**IUpdateServiceManager2-Schnittstelle**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservicemanager2) für die Sitzung zurück.                                                                                                                                                                                                                |
| [**QueryHistory**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesession3-queryhistory)                             | Gibt einen Zeiger auf eine [**IUpdateHistoryEntryCollection-Schnittstelle**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatehistoryentrycollection) zurück. Die Schnittstelle enthält übereinstimmende Ereignisdatensätze auf dem Computer. Dies bewirkt, dass die [**QueryHistory-Methode**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesession3-queryhistory) den Computer synchron nach dem Verlauf von Updateereignissen abfragt. |



 

Informationen zu den Membern, die von dieser Schnittstelle geerbt werden, finden Sie in den folgenden Schnittstellen:

-   [**IUpdateSession2**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession2)
-   [**IUpdateSession**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession)

 

 



