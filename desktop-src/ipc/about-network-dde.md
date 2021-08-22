---
description: Netzwerk-DDE wird verwendet, um die Netzwerkverbindungen zu initiieren und zu verwalten, die für DDE-Konversationen zwischen Anwendungen erforderlich sind, die auf verschiedenen Computern in einem Netzwerk ausgeführt werden.
ms.assetid: f9eee391-2b4a-4c17-bea5-72cda5124e1c
title: Informationen zu Netzwerk-DDE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eeb8f232dc10080a575a6afe500727435bed7913ae95364daf697844c3c65dc8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118756456"
---
# <a name="about-network-dde"></a>Informationen zu Netzwerk-DDE

\[Netzwerk-DDE wird nicht mehr unterstützt. Nddeapi.dll ist auf Windows Vista vorhanden, aber alle Funktionsaufrufe geben NDDE \_ NICHT \_ IMPLEMENTIERT zurück.\]

Netzwerk-DDE wird verwendet, um die Netzwerkverbindungen zu initiieren und zu verwalten, die für DDE-Konversationen zwischen Anwendungen erforderlich sind, die auf verschiedenen Computern in einem Netzwerk ausgeführt werden. Eine *DDE-Konversation* ist die Interaktion zwischen Client- und Serveranwendungen. Sie verwenden Netzwerk-DDE zusammen mit DDE und der DDE-Verwaltungsbibliothek (DDEML) in Ihrer Anwendung.

DDE ist eine Form der prozessübergreifenden Kommunikation, bei der freigegebener Arbeitsspeicher zum Austauschen von Daten zwischen Anwendungen verwendet wird. Anwendungen können DDE für einmalige Datenübertragungen oder für den fortlaufenden Austausch und die Aktualisierung von Daten verwenden. Weitere Informationen zu DDE finden Sie unter [dynamische Daten Exchange](../dataxchg/dynamic-data-exchange.md).

DDEML vereinfacht das Hinzufügen von DDE-Funktionen zu einer Anwendung. Anstatt DDE-Nachrichten direkt zu senden, zu posten und zu verarbeiten, verwendet eine Anwendung die von DDEML bereitgestellten Funktionen, um DDE-Konversationen zu verwalten. Weitere Informationen zu DDEML finden Sie unter [dynamische Daten Exchange Management Library](../dataxchg/dynamic-data-exchange-management-library.md).

## <a name="network-dde-files"></a>Netzwerk-DDE-Dateien

Um die API-Elemente von Netzwerk-DDE zu verwenden, müssen Sie die Headerdatei "NDDEApi.h" in Ihre Quelldateien und die Datei "NDDEApi.lib" in die Linkzeile hinzufügen. Sie müssen auch sicherstellen, dass die NDDEApi.dll geladen ist.

Weitere Informationen finden Sie in den folgenden Themen:

-   [Netzwerk-DDE-Agent](network-dde-agent.md)
-   [DDE-Freigaben](dde-shares.md)
-   [Vertrauenswürdige Freigaben und Sicherheit](trusted-shares-and-security.md)
-   [Verwalten von DDE-Freigaben](managing-dde-shares.md)

 

 
