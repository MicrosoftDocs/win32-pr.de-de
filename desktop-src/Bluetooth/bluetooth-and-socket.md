---
title: Bluetooth und Socket
description: Erstellt einen Socket für eingehende oder ausgehende Verbindungen.
ms.assetid: 21b9cf1f-1a85-4a4b-9557-faa4f32c3696
keywords:
- Bluetooth Bluetooth
- Socket Bluetooth
- Bluetooth und Socket Bluetooth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c2c2085ee0c61941bab93ed25dd86f5c102d0d0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727649"
---
# <a name="bluetooth-and-socket"></a>Bluetooth und Socket

Die [**Socket**](/windows/desktop/api/winsock2/nf-winsock2-socket) -Funktion erstellt einen Socket für eingehende oder ausgehende Verbindungen:

Verwenden Sie die folgenden Einstellungen, um einen Socket mithilfe von Bluetooth zu erstellen:

-   Der *AF* -Parameter der [**Socket**](/windows/desktop/api/winsock2/nf-winsock2-socket) -Funktion ist für Bluetooth-Sockets immer auf " **AF \_ BTH** " festgelegt.
-   Der *Typparameter der Socketfunktion* ist immer ein **Sock- \_ Stream**. [](/windows/desktop/api/winsock2/nf-winsock2-socket) **Sock \_ Dgram** -Sockets werden von Bluetooth nicht unterstützt.
-   Für den *Protokoll* Parameter ist **bthproto \_ RFCOMM** das unterstützte Protokoll.

Weitere Informationen finden Sie unter [Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Windows-Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[**Glühbirne**](/windows/desktop/api/winsock2/nf-winsock2-socket)
</dt> </dl>

 

 