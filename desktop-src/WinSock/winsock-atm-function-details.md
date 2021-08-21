---
description: Basierend auf der Taxonomie, die für Windows sockets 2-protokollunabhängige Multipoint-/Multicastschemas definiert ist, fällt ATM in die Kategorie der Stammdaten- und Stammkontrollebenen.
ms.assetid: 309afa65-2cc4-4b7b-9968-4c4efb2d10a3
title: Details zur Winsock ATM-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b089d02653ee996acc249f63144654c952ba724425fb208d9eb35cc9c2589e4a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051378"
---
# <a name="winsock-atm-function-details"></a>Details zur Winsock ATM-Funktion

Basierend auf der Taxonomie, die für Windows sockets 2-protokollunabhängige Multipoint-/Multicastschemas definiert ist, fällt ATM in die Kategorie der Stammdaten- und Stammkontrollebenen. (Weitere Informationen finden Sie in der Windows Sockets 2-API-Spezifikation, Anhang D.) Eine Anwendung, die als Stamm fungiert, erstellt \_ C-Stammsockets, und Entsprechungen, die auf Blattknoten ausgeführt werden, verwenden \_ C-Blattsockets. Die Stammanwendung verwendet [**WSAJoinLeaf,**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) um neue Blattknoten hinzuzufügen. Die entsprechenden Anwendungen auf den Blattknoten haben ihre \_ C-Blattsockets in den Lauschenmodus versetzt. **WSAJoinLeaf** mit einem \_ angegebenen c-Stammsocket wird der Q.2931 SETUP-Nachricht (für das erste Blatt) oder der ADD PARTY-Nachricht (für alle nachfolgenden Blätter) zugeordnet.

> [!Note]  
> Die QoS-Parameter, die in **WSAJoinLeaf** für alle nachfolgenden Blätter angegeben sind, sollten gemäß der UNI-Spezifikation des ATM-Forums ignoriert werden.

 

Der blattinitiierte Join ist nicht Teil von ATM UNI 3.1, wird aber in ATM UNI 4.0 unterstützt. Daher kann [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) mit einem \_ angegebenen C-Blattsocket der entsprechenden ATM UNI 4.0-Nachricht zugeordnet werden.

Der AAL-Parameter und die B-LLI-Aushandlung werden durch die Änderung der entsprechenden IEs im *lpSQOS-Parameter* beim Aufruf der bedingungsfunktion unterstützt, die in [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept)angegeben ist.

> [!Note]  
> Nur bestimmte Felder in diesen beiden IEs können geändert werden. Ausführliche Informationen finden Sie in den UNI-Spezifikationen des ATM-Forums Anhang C und Anhang F.

 

 

 



