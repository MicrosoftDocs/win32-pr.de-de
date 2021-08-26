---
title: Schlüsselerfassungsfunktionen
description: Standardmäßig stellt der SSP Verschlüsselungsschlüssel für Serverprogramme zur Verfügung, die sie anfordern. Jeder SSP implementiert ein eigenes System zum Generieren von Schlüsseln. Das Format der Schlüssel, die der SSP generiert, ist spezifisch für den SSP.
ms.assetid: 0ba7212c-6ee8-4a92-94d0-f09f84b05bf3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 292926f53e5af0e75957f9b363d3917b1c5f68ef3a4e0a0acf7111c6b37b6518
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120020232"
---
# <a name="key-acquisition-functions"></a>Schlüsselerfassungsfunktionen

Standardmäßig stellt der SSP Verschlüsselungsschlüssel für Serverprogramme zur Verfügung, die sie anfordern. Jeder SSP implementiert ein eigenes System zum Generieren von Schlüsseln. Das Format der Schlüssel, die der SSP generiert, ist spezifisch für den SSP.

RPC bietet Ihnen die Möglichkeit, die Standardmethode zum Generieren von Verschlüsselungsschlüsseln zu überschreiben. Ihre Anwendung kann die [**RpcServerRegisterAuthInfo-Funktion**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterauthinfo) aufrufen und ihr einen Zeiger auf eine Schlüsselerwerbsfunktion übergeben. Sie können die Schlüsselerwerbsfunktion so schreiben, dass sie Schlüssel mit einer beliebigen Methode generiert, die Sie auswählen. Der Schlüssel, den er an das Serverprogramm übergibt, muss jedoch mit dem für den SSP benötigten Format übereinstimmen.

> [!Note]  
> Die meisten Anwendungen müssen keine Schlüsselerwerbsfunktionen verwenden und können einfach **NULL** für alle Parameter angeben, bei denen eine Schlüsselerwerbsfunktion angefordert wird.

 

 

 




