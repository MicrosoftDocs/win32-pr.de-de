---
description: Beim Hinzufügen der Unterstützung für IPv6 müssen Sie sicherstellen, dass Ihre Anwendung Datenstrukturen mit ordnungsgemäßer Größen Definition definiert.
ms.assetid: 2bf353e2-38d5-462c-9e6c-65886b617215
title: Ändern von Datenstrukturen für IPv6-Winsock-Appications
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2c91e19ed733d111bd4e12d824da6ee1a988e9e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343300"
---
# <a name="changing-data-structures-for-ipv6-winsock-appications"></a>Ändern von Datenstrukturen für IPv6-Winsock-Appications

Beim Hinzufügen der Unterstützung für IPv6 müssen Sie sicherstellen, dass Ihre Anwendung Datenstrukturen mit ordnungsgemäßer Größen Definition definiert. Die Größe einer IPv6-Adresse ist weitaus größer als eine IPv4-Adresse. Strukturen, die hart codiert sind, um die Größe einer IPv4-Adresse beim Speichern einer IP-Adresse zu verarbeiten, verursachen Probleme in der Anwendung und müssen geändert werden.

Bewährte Methode

Der beste Ansatz, um sicherzustellen, dass ihre Strukturen ordnungsgemäß skaliert sind, ist die Verwendung der [**sockaddr- \_ Speicher**](/previous-versions/windows/desktop/legacy/ms740504(v=vs.85)) Struktur. Die **sockaddr- \_ Speicher** Struktur ist für die IP-Adress Version agnostisch. Wenn die **sockaddr- \_ Speicher** Struktur zum Speichern von IP-Adressen verwendet wird, können IPv4-und IPv6-Adressen ordnungsgemäß mit einer Codebasis behandelt werden.

Das folgende Beispiel, bei dem es sich um einen Auszug aus der Datei "Server. c" in Anhang B handelt, identifiziert eine angemessene Verwendung der **sockaddr- \_ Speicher** Struktur. Beachten Sie, dass die-Struktur, die in diesem Beispiel ordnungsgemäß verwendet wird, entweder eine IPv4-oder eine IPv6-Adresse ordnungsgemäß verarbeitet.


```C++
#include <winsock2.h>
#include <ws2tcpip.h>
#include <stdio.h>

#pragma comment(lib, "Ws2_32.lib")

#define BUFFER_SIZE 512
#define DEFAULT_PORT "27015"

int main(int argc, char **argv)
{
    char Buffer[BUFFER_SIZE] = {0};
    char *Hostname;
    int Family = AF_UNSPEC;
    int SocketType = SOCK_STREAM;
    char *Port = DEFAULT_PORT;
    char *Address = NULL;
    int i = 0;
    DWORD dwRetval = 0;
    int iResult = 0;
    int FromLen = 0;
    int AmountRead = 0;

    SOCKADDR_STORAGE From;

    WSADATA wsaData;

    ADDRINFO *AddrInfo = NULL;
    ADDRINFO *AI = NULL;

    // Parse arguments
    if (argc >= 1) {
        Hostname = argv[1];
    }    

   // Initialize Winsock
    iResult = WSAStartup(MAKEWORD(2, 2), &wsaData);
    if (iResult != 0) {
        printf("WSAStartup failed: %d\n", iResult);
        return 1;
    }

    From.ss_family = (ADDRESS_FAMILY) Family;
    
    //...
        
        return 0;
}
```



> [!Note]  
> Die [**sockaddr- \_ Speicher**](/previous-versions/windows/desktop/legacy/ms740504(v=vs.85)) Struktur ist neu für Windows XP.

 

Zu Vermeider Code

In der Regel haben viele Anwendungen die [**sockaddr**](sockaddr-2.md) -Struktur verwendet, um Protokoll unabhängige Adressen zu speichern, oder die **sockaddr \_ in** der Struktur für IP-Adressen. Weder die sockaddr-Struktur noch die **sockaddr \_ in** -Struktur ist groß genug, um IPv6-Adressen aufzunehmen. beide sind nicht ausreichend, wenn Ihre Anwendung IPv6-kompatibel sein soll.

Codierungs Aufgabe

**So ändern Sie die vorhandene Codebasis von IPv4 zu IPv4-und IPv6-Interoperabilität**

1.  Erwerben Sie das Checkv4.exe-Hilfsprogramm. Das-Hilfsprogramm ist im Microsoft Windows Software Development Kit (SDK) enthalten, das über Ihr MSDN-Abonnement oder über das Internet als Download verfügbar gemacht wird.
2.  Führen Sie das Checkv4.exe-Hilfsprogramm für den Code aus. Erfahren Sie, wie Sie das Checkv4.exe-Hilfsprogramm für Ihre Dateien ausführen, [indem Sie das Checkv4.exe-Hilfsprogramm verwenden](using-the-checkv4-exe-utility-2.md).
3.  Das Hilfsprogramm warnt Sie bei der Verwendung von **sockaddr** oder **sockaddr \_ in** Strukturen und bietet Empfehlungen darüber, wie Sie entweder durch die IPv6-kompatible Struktur [**sockaddr- \_ Speicher**](/previous-versions/windows/desktop/legacy/ms740504(v=vs.85))ersetzt werden.
4.  Ersetzen Sie alle diese Instanzen und den zugehörigen Code nach Bedarf, um die **sockaddr- \_ Speicher** Struktur zu verwenden.

Alternativ dazu können Sie Ihre Codebasis nach Instanzen von **sockaddr** und **sockaddr \_ in** Strukturen durchsuchen und die gesamte Verwendung (und ggf. einen anderen zugeordneten Code) in die **sockaddr- \_ Speicher** Struktur ändern.

> [!Note]  
> Die Speicherstrukturen **addrinfo** und **\_ sockaddr** umfassen Protokoll-und Adress familienmember (**AI- \_ Familie** bzw. **SS- \_ Familie**). RFC 2553 gibt das **AI- \_ Familienmitglied** von [**addrinfo**](/windows/win32/api/ws2def/ns-ws2def-addrinfoa) als int an, während die **SS- \_ Familie** kurz angegeben wird. Daher führt eine direkte Kopie zwischen diesen Membern zu einem Compilerfehler.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[IPv6-Handbuch für Windows Sockets-Anwendungen](ipv6-guide-for-windows-sockets-applications-2.md)
</dt> <dt>

[Dual-Stack-Sockets für IPv6-Winsock-Anwendungen](dual-stack-sockets.md)
</dt> <dt>

[Funktionsaufrufe für IPv6-Winsock-Anwendungen](function-calls-2.md)
</dt> <dt>

[Verwendung von hart codierten IPv4-Adressen](use-of-hardcoded-ipv4-addresses-2.md)
</dt> <dt>

[Probleme mit der Benutzeroberfläche für IPv6-Winsock-Anwendungen](user-interface-issues-2.md)
</dt> <dt>

[Zugrunde liegende Protokolle für IPv6-Winsock-Anwendungen](underlying-protocols-2.md)
</dt> </dl>

 

 
