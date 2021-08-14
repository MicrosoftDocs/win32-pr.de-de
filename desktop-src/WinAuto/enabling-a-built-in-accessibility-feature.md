---
title: Aktivieren eines integrierten Barrierefreiheitsfeatures
ms.assetid: f97a445d-f93d-4462-bce5-d853f5076b9c
description: Weitere Informationen finden Sie unter Aktivieren eines integrierten Barrierefreiheitsfeatures.
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b733181e28e075f4590e858f576020a7bbd35a23b845778a940e909247f6d40
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118829153"
---
# <a name="enabling-a-built-in-accessibility-feature"></a>Aktivieren eines integrierten Barrierefreiheitsfeatures

Im folgenden Codefragment wird die [**Funktion SystemParametersInfo verwendet,**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) um das FilterKeys-Feature zu aktivieren:


```C++
FILTERKEYS fk; 
BOOL bSuccess; 
 
// Fill in the members of the FILTERKEYS structure.  
 
fk.cbSize = sizeof(FILTERKEYS); 
fk.dwFlags = (FKF_FILTERKEYSON | FKF_HOTKEYACTIVE | 
                       FKF_AVAILABLE | FKF_HOTKEYSOUND |
FKF_CLICKON); 
fk.iWaitMSec = 1000; 
fk.iDelayMSec = 1000; 
fk.iRepeatMSec = 500; 
fk.iBounceMSec = 0; 
 
// Call SystemParametersInfo with the SPI_SETFILTERKEYS flag.  
 
bSuccess = SystemParametersInfo(SPI_SETFILTERKEYS, 0, (LPVOID)
&fk, 0); 
```



 

 
