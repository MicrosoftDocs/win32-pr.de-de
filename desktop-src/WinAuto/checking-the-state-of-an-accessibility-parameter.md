---
title: Überprüfen des Status eines Barrierefreiheits Parameters
description: Im folgenden Code Fragment wird die GetSystemMetrics-Funktion verwendet, um den ShowSounds-Parameter zu überprüfen. Wenn GetSystemMetrics true zurückgibt, sollte die Anwendung alle wichtigen Informationen in der visuellen Form darstellen.
ms.assetid: fb6a0adf-ca38-4e21-9edd-1abb2efd59e5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75409f5af96f83bf13f4834f83503579862caa97
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039081"
---
# <a name="checking-the-state-of-an-accessibility-parameter"></a>Überprüfen des Status eines Barrierefreiheits Parameters

Im folgenden Code Fragment wird die [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) -Funktion verwendet, um den ShowSounds-Parameter zu überprüfen. Wenn **GetSystemMetrics** **true** zurückgibt, sollte die Anwendung alle wichtigen Informationen in der visuellen Form darstellen.


```C++
BOOL fShowSounds; 
fShowSounds = GetSystemMetrics(SM_SHOWSOUNDS); 
```



 

 