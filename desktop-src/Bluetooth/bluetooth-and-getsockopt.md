---
title: Bluetooth und getsockopt
description: Bluetooth verwendet die getsockopt-Funktion, um verschiedene Parameter abzufragen, die dem Serverchannel oder der Verbindung zugeordnet sind.
ms.assetid: 9593fd6c-b55d-45d8-a9d9-87ebcd09d1bd
keywords:
- Bluetooth
- getsockopt
- Bluetooth und getsockopt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dede19b27eea39b7d1e778b3e92312a5e148c0ec
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728361"
---
# <a name="bluetooth-and-getsockopt"></a>Bluetooth und getsockopt

Bluetooth verwendet die [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) -Funktion, um verschiedene Parameter abzufragen, die dem Serverchannel oder der Verbindung zugeordnet sind. Für die Verwendung von **getsockopt** mit Bluetooth gelten die folgenden Anforderungen:

-   Der *s* -Parameter von [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) muss ein gültiger Bluetooth-Socket sein.
-   Der *Level* -Parameter von [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) muss "Sol \_ RFCOMM" lauten.

Eine Liste der verfügbaren Bluetooth-Socketoptionen finden Sie unter [Optionen für Bluetooth und Socket](bluetooth-and-socket-options.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Windows-Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt)
</dt> </dl>

 

 