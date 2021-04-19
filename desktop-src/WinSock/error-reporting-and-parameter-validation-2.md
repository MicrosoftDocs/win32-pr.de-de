---
description: Das Schema für die Fehlerberichterstattung unterscheidet sich zwischen den SPI-und API-Schnittstellen.
ms.assetid: f4a4b406-3e3a-444f-b75a-0cf51bded1bc
title: Fehlerberichterstattung und Parameter Validierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 291fa2ed950d916be39b1a696f5fe8ad6f07280c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346942"
---
# <a name="error-reporting-and-parameter-validation"></a>Fehlerberichterstattung und Parameter Validierung

Das Schema für die Fehlerberichterstattung unterscheidet sich zwischen den SPI-und API-Schnittstellen. Windows Sockets Service-Anbieter melden Fehler zusammen mit der Funktion, die zurückgibt, im Gegensatz zu dem Thread basierten Ansatz, der in der API verwendet wird. Der Ws2 \_ -32.dll verwendet den Funktions spezifischen Fehlercode des Dienstanbieters, um den Fehlerwert pro Thread zu aktualisieren, der über die [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) -API-Funktion abgerufen wird. Dienstanbieter sind jedoch weiterhin erforderlich, um den pro-Socket-basierten Fehler beizubehalten, der über die Option "so Error Socket" abgerufen werden kann \_ .

Der Ws2- \_32.dll führt die Parameter Validierung nur bei Funktionsaufrufen aus, die vollständig in sich selbst implementiert werden. Dienstanbieter sind für die Durchführung ihrer eigenen Parameter Validierung verantwortlich.

 

 



