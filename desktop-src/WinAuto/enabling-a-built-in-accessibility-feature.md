---
title: Aktivieren einer integrierten Barrierefreiheits Funktion
ms.assetid: f97a445d-f93d-4462-bce5-d853f5076b9c
description: 'Weitere Informationen finden Sie unter: Aktivieren einer integrierten Barrierefreiheits Funktion'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d860b1410e48f5824923b8b16babb6bcd1527ec9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218820"
---
# <a name="enabling-a-built-in-accessibility-feature"></a>Aktivieren einer integrierten Barrierefreiheits Funktion

Das folgende Code Fragment verwendet die [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) -Funktion, um die Funktion FilterKeys zu aktivieren:


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



 

 
