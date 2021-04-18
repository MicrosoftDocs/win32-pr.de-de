---
title: Bluetooth und Accept
description: Bluetooth verwendet die Accept-Funktion, um eingehende Verbindungsversuche für einen Socket zu aktivieren.
ms.assetid: 79708118-2f70-4759-b5d6-cf5cfc33c27e
keywords:
- accept (Akzeptieren)
- Bluetooth
- Bluetooth
- Bluetooth und Accept
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28dff84ec05429411614e64a08ab159a5ee134b6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106337248"
---
# <a name="bluetooth-and-accept"></a>Bluetooth und Accept

Bluetooth verwendet die [**Accept**](/windows/desktop/api/winsock2/nf-winsock2-accept) -Funktion, um eingehende Verbindungsversuche für einen Socket zu aktivieren. Die BTH- \_ addr der Client Anwendung wird durchlesen des Transport spezifischen Bluetooth-Abschnitts der zurückgegebenen [**sockaddr**](/windows/desktop/WinSock/sockaddr-2) -Struktur abgerufen. Die Verwendung der **Accept** -Funktion mit Bluetooth weist das folgende Format auf:

-   Der *addr* -Parameter der [**Accept**](/windows/desktop/api/winsock2/nf-winsock2-accept) -Funktion ist ein optionaler Zeiger auf einen Puffer, der die Adresse der verbundenen Entität empfängt, wie Sie der Kommunikationsschicht bekannt ist. Ein Zeiger auf eine [**sockaddr- \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) -Struktur mit der Remote-Bluetooth-Geräteadresse wird zurückgegeben.
-   Der *addrlen* -Parameter der [**Accept**](/windows/desktop/api/winsock2/nf-winsock2-accept) -Funktion ist ein optionaler Zeiger auf eine Ganzzahl, die die Länge von addr in Bytes enthält. Der ganzzahlige Wert muss größer als oder gleich dem Wert von **sizeof** ([**sockaddr \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)) sein.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Windows-Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[**erst**](/windows/desktop/api/winsock2/nf-winsock2-accept)
</dt> </dl>

 

 