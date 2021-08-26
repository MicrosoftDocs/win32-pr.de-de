---
title: Bluetooth und Akzeptieren
description: Bluetooth verwendet die accept-Funktion, um eingehende Verbindungsversuche für einen Socket zu ermöglichen.
ms.assetid: 79708118-2f70-4759-b5d6-cf5cfc33c27e
keywords:
- accept (Akzeptieren)
- Bluetooth
- Bluetooth
- Bluetooth und Akzeptieren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c5f12a7fd9fee508354dfcd9421f830e814eed09bb207cc6024b50705cc3566
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004610"
---
# <a name="bluetooth-and-accept"></a>Bluetooth und Akzeptieren

Bluetooth verwendet die [](/windows/desktop/api/winsock2/nf-winsock2-accept) accept-Funktion, um eingehende Verbindungsversuche für einen Socket zu aktivieren. Die \_ BTH-ADDR der Clientanwendung wird durch Lesen des Bluetooth transportspezifischen Abschnitts der [**zurückgegebenen Sockaddr-Struktur**](/windows/desktop/WinSock/sockaddr-2) abgerufen. Die Verwendung der **accept-Funktion** mit Bluetooth hat das folgende Format:

-   Der *addr-Parameter* der [**accept-Funktion**](/windows/desktop/api/winsock2/nf-winsock2-accept) ist ein optionaler Zeiger auf einen Puffer, der die Adresse der verbindenden Entität empfängt, wie es der Kommunikationsschicht bekannt ist. Ein Zeiger auf eine [**SOCKADDR-BTH-Struktur \_**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) mit der Remote-Bluetooth Geräteadresse wird zurückgegeben.
-   Der *addrlen-Parameter* der [**accept-Funktion**](/windows/desktop/api/winsock2/nf-winsock2-accept) ist ein optionaler Zeiger auf eine ganze Zahl, die die Länge des Addrs in Bytes enthält. Die ganze Zahl muss größer oder gleich dem Wert von **sizeof** ([**SOCKADDR \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)) sein.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Windows-Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[**Akzeptieren**](/windows/desktop/api/winsock2/nf-winsock2-accept)
</dt> </dl>

 

 