---
description: Die meisten Get-und Set-Vorgänge behandeln nur eine Komponente von Informationen. Die phonegetstatus-Funktion gibt umfassende Statusinformationen zu einem Telefongerät an eine Anwendung zurück.
ms.assetid: ca38396c-6f97-4c1c-99fb-2bd64c74c626
title: Status (telefonieapi)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44a9a93fdd97d32b477545ba0fb9f73f10b45021
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864999"
---
# <a name="status-telephony-api"></a>Status (telefonieapi)

Die meisten Get-und Set-Vorgänge behandeln nur eine Komponente von Informationen. Die [**phonegetstatus**](/windows/desktop/api/Tapi/nf-tapi-phonegetstatus) -Funktion gibt umfassende Statusinformationen zu einem Telefongerät an eine Anwendung zurück.

Wie bereits erwähnt, wird bei jeder Änderung eines Status Elements auf dem Telefongerät eine [**Telefon \_ Zustands**](phone-state.md) Meldung an die Anwendungsfunktion gesendet. Zu den Parametern dieser Nachricht gehören ein Handle für das Telefongerät und ein Hinweis auf das geänderte Status Element.

Eine Anwendung kann [**phonesetstatusmessages**](/windows/desktop/api/Tapi/nf-tapi-phonesetstatusmessages) verwenden, um die spezifischen Statusänderungen auszuwählen, für die Sie benachrichtigt werden möchten. Dementsprechend gibt [**phonegetstatusmessages**](/windows/desktop/api/Tapi/nf-tapi-phonegetstatusmessages) die Statusänderungen zurück, für die die Anwendung benachrichtigt werden soll.

 

 



