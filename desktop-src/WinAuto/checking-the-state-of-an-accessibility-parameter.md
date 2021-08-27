---
title: Überprüfen des Status eines Barrierefreiheitsparameters
description: Das folgende Codefragment verwendet die GetSystemMetrics-Funktion, um den ShowSounds-Parameter zu überprüfen. Wenn GetSystemMetrics TRUE zurückgibt, sollte die Anwendung alle wichtigen Informationen in visueller Form anzeigen.
ms.assetid: fb6a0adf-ca38-4e21-9edd-1abb2efd59e5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 374520612ce96522edc1b879a49f5f30a9c7a857f9bb46a562a4ab48effebe9e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120122250"
---
# <a name="checking-the-state-of-an-accessibility-parameter"></a>Überprüfen des Status eines Barrierefreiheitsparameters

Das folgende Codefragment verwendet die [**GetSystemMetrics-Funktion,**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) um den ShowSounds-Parameter zu überprüfen. Wenn **GetSystemMetrics** **TRUE zurückgibt,** sollte die Anwendung alle wichtigen Informationen in visueller Form anzeigen.


```C++
BOOL fShowSounds; 
fShowSounds = GetSystemMetrics(SM_SHOWSOUNDS); 
```



 

 