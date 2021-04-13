---
description: Network DDE wird zum initiieren und Verwalten der Netzwerkverbindungen verwendet, die für DDE-Konversationen zwischen Anwendungen benötigt werden, die auf verschiedenen Computern in einem Netzwerk ausgeführt werden.
ms.assetid: f9eee391-2b4a-4c17-bea5-72cda5124e1c
title: Informationen zu Network DDE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 412971f6bef8d2782dce38b5aef413e4d073f6b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345088"
---
# <a name="about-network-dde"></a>Informationen zu Network DDE

\[Network DDE wird nicht mehr unterstützt. Nddeapi.dll ist unter Windows Vista vorhanden, aber alle Funktionsaufrufe geben "ndde" \_ nicht \_ implementiert zurück.\]

Network DDE wird zum initiieren und Verwalten der Netzwerkverbindungen verwendet, die für DDE-Konversationen zwischen Anwendungen benötigt werden, die auf verschiedenen Computern in einem Netzwerk ausgeführt werden. Eine DDE- *Konversation* ist die Interaktion zwischen Client-und Server Anwendungen. Sie verwenden Network DDE zusammen mit DDE und der DDE Management Library (Ddeml) in Ihrer Anwendung.

DDE ist eine Form der prozessübergreifenden Kommunikation, die gemeinsam genutzten Speicher zum Austauschen von Daten zwischen Anwendungen verwendet. Anwendungen können DDE für einen einmaligen Datentransfer oder für den laufenden Austausch und das Aktualisieren von Daten verwenden. Weitere Informationen zu DDE finden Sie unter [dynamischer Datenaustausch](../dataxchg/dynamic-data-exchange.md).

Ddeml vereinfacht das Hinzufügen von DDE-Funktionen zu einer Anwendung. Anstatt DDE-Nachrichten direkt zu senden, zu veröffentlichen und zu verarbeiten, verwendet eine Anwendung die von der Ddeml bereitgestellten Funktionen zum Verwalten von DDE-Konversationen. Weitere Informationen zu DDEML finden Sie unter [dynamischer Datenaustausch-Verwaltungs Bibliothek](../dataxchg/dynamic-data-exchange-management-library.md).

## <a name="network-dde-files"></a>Netzwerk-DDE-Dateien

Um die API-Elemente von Network DDE verwenden zu können, müssen Sie die Header Datei "nddeapi. h" in die Quelldateien einschließen und die Datei "nddeapi. lib" in die Linkzeile einschließen. Außerdem müssen Sie sicherstellen, dass die NDDEApi.dll-Datei geladen ist.

Weitere Informationen finden Sie unter den folgenden Themen:

-   [Netzwerk-DDE-Agent](network-dde-agent.md)
-   [DDE-Freigaben](dde-shares.md)
-   [Vertrauenswürdige Freigaben und Sicherheit](trusted-shares-and-security.md)
-   [Verwalten von DDE Shares](managing-dde-shares.md)

 

 
