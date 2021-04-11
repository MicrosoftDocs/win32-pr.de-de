---
title: Bluetooth und setsockopt
description: Bluetooth verwendet die Setsockopt-Funktion, um verschiedene Parameter festzulegen, die dem Serverchannel oder der Verbindung zugeordnet sind.
ms.assetid: ab78baed-5556-4d7b-88a6-e3ceb93afa8c
keywords:
- Bluetooth
- setsockopt
- Bluetooth und setsockopt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 943839a49788b76e597596aee9cba65fa4b8d30d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315344"
---
# <a name="bluetooth-and-setsockopt"></a>Bluetooth und setsockopt

Bluetooth verwendet die [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) -Funktion, um verschiedene Parameter festzulegen, die dem Serverchannel oder der Verbindung zugeordnet sind. Für die Verwendung von **setsockopt** mit Bluetooth gelten die folgenden Anforderungen:

-   Der *s* -Parameter von [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) muss ein gültiger Bluetooth-Socket sein.
-   Der *Level* -Parameter von [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) muss "Sol \_ RFCOMM" lauten.

Eine Liste der verfügbaren Bluetooth-Socketoptionen finden Sie unter [Optionen für Bluetooth und Socket](bluetooth-and-socket-options.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Windows-Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt)
</dt> </dl>

 

 