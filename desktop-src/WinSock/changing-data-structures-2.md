---
description: Wenn Sie Unterstützung für IPv6 hinzufügen, müssen Sie sicherstellen, dass Ihre Anwendung Datenstrukturen mit ordnungsgemäßer Größe definiert.
ms.assetid: 2bf353e2-38d5-462c-9e6c-65886b617215
title: Ändern von Datenstrukturen für IPv6 Winsock-Appications
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2999c0d0c5a335c1367165c227fc1aad805579db5a790a19d316a1624e922947
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117741550"
---
# <a name="changing-data-structures-for-ipv6-winsock-appications"></a>Ändern von Datenstrukturen für IPv6 Winsock-Appications

Wenn Sie Unterstützung für IPv6 hinzufügen, müssen Sie sicherstellen, dass Ihre Anwendung Datenstrukturen mit ordnungsgemäßer Größe definiert. Die Größe einer IPv6-Adresse ist viel größer als eine IPv4-Adresse. Strukturen, die hart codiert sind, um die Größe einer IPv4-Adresse beim Speichern einer IP-Adresse zu verarbeiten, verursachen Probleme in Ihrer Anwendung und müssen geändert werden.

Bewährte Methode

Der beste Ansatz, um sicherzustellen, dass Ihre Strukturen eine ordnungsgemäße Größe haben, ist die Verwendung der [**SOCKADDR \_ STORAGE-Struktur.**](/previous-versions/windows/desktop/legacy/ms740504(v=vs.85)) Die **SOCKADDR \_ STORAGE-Struktur** ist unabhängig von der IP-Adressversion. Wenn die **SOCKADDR \_ STORAGE-Struktur** zum Speichern von IP-Adressen verwendet wird, können IPv4- und IPv6-Adressen ordnungsgemäß mit einer Codebasis verarbeitet werden.

Das folgende Beispiel, bei dem es sich um einen Auszug aus der Datei Server.c in Anhang B handelt, identifiziert eine geeignete Verwendung der **SOCKADDR \_ STORAGE-Struktur.** Beachten Sie, dass die -Struktur bei ordnungsgemäßer Verwendung wie in diesem Beispiel ordnungsgemäß entweder eine IPv4- oder IPv6-Adresse verarbeitet.


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
> Die [**SOCKADDR \_ STORAGE-Struktur**](/previous-versions/windows/desktop/legacy/ms740504(v=vs.85)) ist neu für Windows XP.

 

Code, der vermieden werden soll

In der Regel verwendeten viele Anwendungen die [**Sockaddr-Struktur,**](sockaddr-2.md) um protokollunabhängige Adressen zu speichern, oder den **Sockaddr \_ in** der Struktur für IP-Adressen. Weder die Sockaddr-Struktur noch der **Sockaddr \_ in** der Struktur sind groß genug, um IPv6-Adressen zu speichern. Daher sind beide nicht ausreichend, wenn Ihre Anwendung IPv6-kompatibel sein soll.

Codierungsaufgabe

**So ändern Sie Ihre vorhandene Codebasis von IPv4 in IPv4- und IPv6-Interoperabilität**

1.  Erwerben Sie das Checkv4.exe Hilfsprogramm. Das Hilfsprogramm ist im Microsoft Windows Software Development Kit (SDK) enthalten, das über Ihr MSDN-Abonnement oder über das Web als Download zur Verfügung gestellt wird.
2.  Führen Sie Checkv4.exe Hilfsprogramm für Ihren Code aus. Informationen zum Ausführen des Hilfsprogramms Checkv4.exe für Ihre Dateien finden Sie im Abschnitt Verwenden des Checkv4.exe [Hilfsprogramms](using-the-checkv4-exe-utility-2.md).
3.  Das Hilfsprogramm warnt Sie vor der Verwendung von **sockaddr** oder **sockaddr \_ in** Strukturen und bietet Empfehlungen dazu, wie Sie entweder durch die IPv6-kompatible Struktur [**SOCKADDR \_ STORAGE ersetzen.**](/previous-versions/windows/desktop/legacy/ms740504(v=vs.85))
4.  Ersetzen Sie solche Instanzen und den zugehörigen Code entsprechend, um die **SOCKADDR \_ STORAGE-Struktur zu** verwenden.

Alternativ können Sie Ihre Codebasis nach Instanzen von **sockaddr** und **sockaddr \_ in** Strukturen durchsuchen und diese Nutzung (und gegebenenfalls anderen zugehörigen Code) in die **SOCKADDR \_ STORAGE-Struktur** ändern.

> [!Note]  
> Die **addrinfo-** und **SOCKADDR \_ STORAGE-Strukturen** enthalten Protokoll- und Adressfamilienmitglieder (**ai family \_ bzw.** **ss \_ family**). RFC 2553 gibt **\_** das ai-Familienmitglied von [**addrinfo**](/windows/win32/api/ws2def/ns-ws2def-addrinfoa) als int an, während **die \_ ss-Familie** als short angegeben wird. Daher führt eine direkte Kopie zwischen diesen Membern zu einem Compilerfehler.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[IPv6-Leitfaden für Windows Sockets-Anwendungen](ipv6-guide-for-windows-sockets-applications-2.md)
</dt> <dt>

[Dual-Stack-Sockets für IPv6-Winsock-Anwendungen](dual-stack-sockets.md)
</dt> <dt>

[Funktionsaufrufe für IPv6 Winsock-Anwendungen](function-calls-2.md)
</dt> <dt>

[Verwenden von hartcodierten IPv4-Adressen](use-of-hardcoded-ipv4-addresses-2.md)
</dt> <dt>

[Benutzeroberfläche von IPv6-Winsock-Anwendungen](user-interface-issues-2.md)
</dt> <dt>

[Zugrunde liegende Protokolle für IPv6 Winsock-Anwendungen](underlying-protocols-2.md)
</dt> </dl>

 

 
