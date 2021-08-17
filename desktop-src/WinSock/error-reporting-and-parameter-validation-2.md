---
description: Das Schema für die Fehlerberichterstattung unterscheidet sich zwischen spi- und API-Schnittstellen.
ms.assetid: f4a4b406-3e3a-444f-b75a-0cf51bded1bc
title: Fehlerberichterstattung und Parameterüberprüfung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5fdec1ee6a4cd7d052ba9f94cdf62ce7de70969a521a7023a5ca41e37f6a931
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132613"
---
# <a name="error-reporting-and-parameter-validation"></a>Fehlerberichterstattung und Parameterüberprüfung

Das Schema für die Fehlerberichterstattung unterscheidet sich zwischen spi- und API-Schnittstellen. Windows Sockets-Dienstanbieter melden Fehler zusammen mit der zurückgegebenen Funktion im Gegensatz zum threadbasierten Ansatz, der in der API verwendet wird. Der Ws2-32.dll verwendet den Fehlercode pro \_ Funktion des Dienstanbieters, um den Fehlerwert pro Thread zu aktualisieren, der über die [**WSAGetLastError-API-Funktion**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) abgerufen wird. Dienstanbieter sind jedoch weiterhin erforderlich, um den socketbasierten Fehler beizubehalten, der über die SO ERROR-Socketoption abgerufen werden \_ kann.

Der \_ Ws2-32.dll führt die Parameterüberprüfung nur für Funktionsaufrufe durch, die vollständig in sich selbst implementiert sind. Dienstanbieter sind für die Durchführung ihrer gesamten eigenen Parametervalidierung verantwortlich.

 

 



