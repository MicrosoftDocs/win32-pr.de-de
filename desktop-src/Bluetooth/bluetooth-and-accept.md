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
# <a name="bluetooth-and-accept"></a><span data-ttu-id="cdfc1-107">Bluetooth und Accept</span><span class="sxs-lookup"><span data-stu-id="cdfc1-107">Bluetooth and accept</span></span>

<span data-ttu-id="cdfc1-108">Bluetooth verwendet die [**Accept**](/windows/desktop/api/winsock2/nf-winsock2-accept) -Funktion, um eingehende Verbindungsversuche für einen Socket zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="cdfc1-108">Bluetooth uses the [**accept**](/windows/desktop/api/winsock2/nf-winsock2-accept) function to enable incoming connection attempts on a socket.</span></span> <span data-ttu-id="cdfc1-109">Die BTH- \_ addr der Client Anwendung wird durchlesen des Transport spezifischen Bluetooth-Abschnitts der zurückgegebenen [**sockaddr**](/windows/desktop/WinSock/sockaddr-2) -Struktur abgerufen.</span><span class="sxs-lookup"><span data-stu-id="cdfc1-109">The BTH\_ADDR of the client application is obtained by reading the Bluetooth transport-specific section of the returned [**sockaddr**](/windows/desktop/WinSock/sockaddr-2) structure.</span></span> <span data-ttu-id="cdfc1-110">Die Verwendung der **Accept** -Funktion mit Bluetooth weist das folgende Format auf:</span><span class="sxs-lookup"><span data-stu-id="cdfc1-110">Use of the **accept** function with Bluetooth has the following format:</span></span>

-   <span data-ttu-id="cdfc1-111">Der *addr* -Parameter der [**Accept**](/windows/desktop/api/winsock2/nf-winsock2-accept) -Funktion ist ein optionaler Zeiger auf einen Puffer, der die Adresse der verbundenen Entität empfängt, wie Sie der Kommunikationsschicht bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="cdfc1-111">The *addr* parameter of the [**accept**](/windows/desktop/api/winsock2/nf-winsock2-accept) function is an optional pointer to a buffer that receives the address of the connecting entity, as known to the communications layer.</span></span> <span data-ttu-id="cdfc1-112">Ein Zeiger auf eine [**sockaddr- \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) -Struktur mit der Remote-Bluetooth-Geräteadresse wird zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="cdfc1-112">A pointer to a [**SOCKADDR\_BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) structure with the remote Bluetooth device address is returned.</span></span>
-   <span data-ttu-id="cdfc1-113">Der *addrlen* -Parameter der [**Accept**](/windows/desktop/api/winsock2/nf-winsock2-accept) -Funktion ist ein optionaler Zeiger auf eine Ganzzahl, die die Länge von addr in Bytes enthält. Der ganzzahlige Wert muss größer als oder gleich dem Wert von **sizeof** ([**sockaddr \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)) sein.</span><span class="sxs-lookup"><span data-stu-id="cdfc1-113">The *addrlen* parameter of the [**accept**](/windows/desktop/api/winsock2/nf-winsock2-accept) function is an optional pointer to an integer that contains the length, in bytes, of addr. The integer must be greater or equal to the value of **sizeof** ([**SOCKADDR\_BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="cdfc1-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="cdfc1-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cdfc1-115">Windows-Sockets</span><span class="sxs-lookup"><span data-stu-id="cdfc1-115">Windows Sockets</span></span>](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[<span data-ttu-id="cdfc1-116">**erst**</span><span class="sxs-lookup"><span data-stu-id="cdfc1-116">**accept**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-accept)
</dt> </dl>

 

 