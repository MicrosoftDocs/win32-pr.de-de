---
title: Bluetooth und getsockopt
description: Bluetooth die getsockopt-Funktion zum Abfragen verschiedener Parameter, die dem Serverkanal oder der Verbindung zugeordnet sind.
ms.assetid: 9593fd6c-b55d-45d8-a9d9-87ebcd09d1bd
keywords:
- Bluetooth
- getsockopt
- Bluetooth und getsockopt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ee63d8dc1665868023967dd88c5ba223cce538c1fa1d41dd151329f6bf52f7e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119081084"
---
# <a name="bluetooth-and-getsockopt"></a>Bluetooth und getsockopt

Bluetooth verwendet die [**getsockopt-Funktion,**](/windows/desktop/api/winsock/nf-winsock-getsockopt) um verschiedene Parameter abfragt, die dem Serverkanal oder der Verbindung zugeordnet sind. Die Verwendung **von getsockopt** mit Bluetooth erfüllt die folgenden Anforderungen:

-   Der *s-Parameter* [**von getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) muss ein gültiger Bluetooth sein.
-   Der *level-Parameter* [**von getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) muss SOL \_ RFCOMM sein.

Eine Liste der verfügbaren Socketoptionen Bluetooth finden Sie unter Bluetooth [und Socketoptionen.](bluetooth-and-socket-options.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Windows-Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt)
</dt> </dl>

 

 