---
title: Schlüssel Erwerbs Funktionen
description: Standardmäßig stellt der SSP Verschlüsselungsschlüssel für Serverprogramme bereit, von denen diese angefordert werden. Jeder SSP implementiert sein eigenes System zum Erstellen von Schlüsseln. Das Format der vom SSP generierten Schlüssel ist spezifisch für den SSP.
ms.assetid: 0ba7212c-6ee8-4a92-94d0-f09f84b05bf3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36a8c8e8cfb2f3b4f8f241b2401878576cbe7f90
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856747"
---
# <a name="key-acquisition-functions"></a>Schlüssel Erwerbs Funktionen

Standardmäßig stellt der SSP Verschlüsselungsschlüssel für Serverprogramme bereit, von denen diese angefordert werden. Jeder SSP implementiert sein eigenes System zum Erstellen von Schlüsseln. Das Format der vom SSP generierten Schlüssel ist spezifisch für den SSP.

RPC bietet Ihnen die Möglichkeit, die Standardmethode zum Erstellen von Verschlüsselungsschlüsseln zu überschreiben. Die Anwendung kann die [**rpcserverregisterauthinfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterauthinfo) -Funktion aufrufen und ihr einen Zeiger auf eine Schlüssel Erwerbs Funktion übergeben. Sie können die Schlüssel Erwerbs Funktion so schreiben, dass Sie mit jeder gewählten Methode Schlüssel generiert. Der an das Serverprogramm übergebenen Schlüssel muss jedoch dem Format entsprechen, das für den SSP erforderlich ist.

> [!Note]  
> Die meisten Anwendungen müssen keine Schlüssel Erwerbs Funktionen verwenden und können einfach **null** für alle Parameter angeben, bei denen eine Schlüssel Erwerbs Funktion angefordert wird.

 

 

 




