---
title: Bluetooth und Socket
description: Erstellt einen Socket für eingehende oder ausgehende Verbindungen.
ms.assetid: 21b9cf1f-1a85-4a4b-9557-faa4f32c3696
keywords:
- Bluetooth Bluetooth
- socket Bluetooth
- Bluetooth und Socket-Bluetooth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5afaf61e307ce8d5001c2ba5402607b63b1ad6d19317aee044d7a2cac31259b0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004300"
---
# <a name="bluetooth-and-socket"></a>Bluetooth und Socket

Die [**Socketfunktion**](/windows/desktop/api/winsock2/nf-winsock2-socket) erstellt einen Socket für eingehende oder ausgehende Verbindungen:

Verwenden Sie zum Erstellen eines Sockets mit Bluetooth die folgenden Einstellungen:

-   Der *af-Parameter* der [**Socketfunktion**](/windows/desktop/api/winsock2/nf-winsock2-socket) wird für Bluetooth Sockets immer auf **AF \_ BTH** festgelegt.
-   Der *Typparameter* der [**Socketfunktion**](/windows/desktop/api/winsock2/nf-winsock2-socket) ist immer **SOCK \_ STREAM**. **SOCK \_ DGRAM-Sockets** werden von Bluetooth nicht unterstützt.
-   Für den *Protokollparameter* ist **BTHPROTO \_ RFCOMM** das unterstützte Protokoll.

Weitere Informationen finden Sie unter [Windows Sockets.](/windows/desktop/WinSock/windows-sockets-start-page-2)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Windows-Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[**Socket**](/windows/desktop/api/winsock2/nf-winsock2-socket)
</dt> </dl>

 

 