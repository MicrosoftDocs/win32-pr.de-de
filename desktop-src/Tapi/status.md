---
description: Die meisten Get- und Set-Vorgänge befassen sich nur mit einer Informationskomponente. Die phoneGetStatus-Funktion gibt vollständige Statusinformationen zu einem Telefongerät an eine Anwendung zurück.
ms.assetid: ca38396c-6f97-4c1c-99fb-2bd64c74c626
title: Status (Telefonie-API)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32fd9191d4b1808ca2dc5ff20ce509b58ad27a78a354aeca4ca83f8aa60dafa1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118861827"
---
# <a name="status-telephony-api"></a>Status (Telefonie-API)

Die meisten Get- und Set-Vorgänge befassen sich nur mit einer Informationskomponente. Die [**phoneGetStatus-Funktion**](/windows/desktop/api/Tapi/nf-tapi-phonegetstatus) gibt vollständige Statusinformationen zu einem Telefongerät an eine Anwendung zurück.

Wie bereits erwähnt, wird bei jeder Änderung eines Statuselements auf dem Telefongerät eine [**PHONE \_ STATE-Nachricht**](phone-state.md) an die Anwendungsfunktion gesendet. Zu den Parametern dieser Nachricht gehören ein Handle für das Telefongerät und ein Hinweis auf das geänderte Statuselement.

Eine Anwendung kann [**phoneSetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-phonesetstatusmessages) verwenden, um die spezifischen Statusänderungen auszuwählen, für die sie benachrichtigt werden möchte. Entsprechend gibt [**phoneGetStatusMessages die**](/windows/desktop/api/Tapi/nf-tapi-phonegetstatusmessages) Statusänderungen zurück, über die die Anwendung benachrichtigt werden möchte.

 

 



