---
description: Basierend auf der Taxonomie, die für Protokoll unabhängige Multipoint-/Multicast Schemas von Windows Sockets 2 definiert ist, fällt ATM in die Kategorie der Stammdaten und der Stamm steuerungsflächen.
ms.assetid: 309afa65-2cc4-4b7b-9968-4c4efb2d10a3
title: Details der Winsock-ATM-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e82ca0531272490c2d3189467186535a63d6ba2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130405"
---
# <a name="winsock-atm-function-details"></a>Details der Winsock-ATM-Funktion

Basierend auf der Taxonomie, die für Protokoll unabhängige Multipoint-/Multicast Schemas von Windows Sockets 2 definiert ist, fällt ATM in die Kategorie der Stammdaten und der Stamm steuerungsflächen. (Weitere Informationen finden Sie in der API-Spezifikation von Windows Sockets 2 (Anhang D).) Eine Anwendung, die als Stamm fungiert, würde c \_ -stammsockets erstellen, und Gegenstücke, die auf Blattknoten ausgeführt werden, würden c- \_ Blatt Sockets verwenden. Die Stamm Anwendung verwendet [**wsajoinleaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) , um neue Blattknoten hinzuzufügen. Die entsprechenden Anwendungen auf den Blattknoten haben ihre c- \_ Blatt-Sockets in den Empfangsmodus festgelegt. **Wsajoinleaf** mit einem angegebenen c-Stamm- \_ Socket wird der Q. 2931-Setup Nachricht (für das erste Blatt) oder der Nachricht zum Hinzufügen von Parteien (für nachfolgende Blätter) zugeordnet.

> [!Note]  
> Die in **wsajoinleaf** angegebenen QoS-Parameter für nachfolgende Blätter sollten gemäß der Uni-Spezifikation des ATM-Forums ignoriert werden.

 

Der Blatt initiierte Join ist nicht Teil der ATM-Uni 3,1, wird jedoch in der ATM-Uni 4,0 unterstützt. Daher kann [**wsajoinleaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) mit einem \_ angegebenen c-Blatt Socket der entsprechenden ATM-Uni 4,0-Nachricht zugeordnet werden.

Der Aal-Parameter und die B-lli-Aushandlung werden durch die Änderung der entsprechenden IES im *lpsqos* -Parameter nach dem Aufruf der in [**wsaaccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept)angegebenen Bedingungs Funktion unterstützt.

> [!Note]  
> Nur bestimmte Felder in diesen beiden IES können geändert werden. Weitere Informationen finden Sie im ATM-Forum in der Uni-Spezifikation Anhang C und Anhang F.

 

 

 



