---
title: Entwickeln von RPC Windows Anwendungen
description: Wenn Sie das Platform Software Development Kit (SDK) installieren, werden die folgende RPC-Entwicklungsumgebung, die Laufzeitbibliotheken und tools automatisch installiert.
ms.assetid: d5da3bca-5251-4ba4-b873-0817fe0f298d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31ddb48a38faadb8235064fa735fa8a75a80a62308990373ab1971d4a6cd9ecb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118930795"
---
# <a name="developing-rpc-windows-applications"></a>Entwickeln von RPC Windows Anwendungen

Wenn Sie das Platform Software Development Kit (SDK) installieren, werden die folgende RPC-Entwicklungsumgebung, die Laufzeitbibliotheken und die Tools automatisch installiert:

-   C/C++-Sprachheader (. H)-Dateien
-   RPC-Importbibliotheksdateien (LIB)
-   Beispielprogramme
-   RPC-Referenzhilfedateien
-   Das **Hilfsprogramm uuidgen**

Wenn Sie Windows installieren, wird Folgendes installiert:

-   RPC-Laufzeit-DLLs
-   Microsoft Locator (unter Windows Vista und höher nicht unterstützt)
-   RPC-Endpunktzuordnungsdienste

Die folgenden RPC-Importbibliotheken.



| Importieren der Bibliothek | BESCHREIBUNG                |
|----------------|----------------------------|
| Rpcns4.lib     | Name-Service-Funktionen     |
| Rpcrt4.lib     | Windows Laufzeitfunktionen |



 

> [!Note]  
> Rpcns4.lib ist veraltet und wird nicht mehr unterstützt.

 

Die folgenden RPC-Bibliotheken sind für die Downlevelunterstützung enthalten.



| Dynamic Link Library | Beschreibung                 | Plattform                           |
|----------------------|-----------------------------|------------------------------------|
| Rpcltc1.dll          | Named Pipe-Transport des Clients | Windows NT, Windows 98, Windows 95 |
| Rpclts1.dll          | Named Pipe-Transport auf serverseitigem Server | Windows NT, Windows 98, Windows 95 |
| Rpcltc3.dll          | TCP/IP-Clienttransport     | Windows NT, Windows 98, Windows 95 |
| Rpclts3.dll          | TCP/IP-Servertransport     | Windows NT, Windows 98, Windows 95 |
| Rpcltc5.dll          | NetBIOS-Clienttransport    | Windows NT, Windows 98, Windows 95 |
| Rpclts5.dll          | NetBIOS-Servertransport    | Windows NT, Windows 98, Windows 95 |
| Rpcltc6.dll          | Client-SPX-Transport        | Windows NT, Windows 98, Windows 95 |
| Rpclts6.dll          | Server-SPX-Transport        | Windows NT, Windows 98, Windows 95 |
| Rpcdgc6.dll          | Client-IPX-Transport        | Windows NT                         |
| Rpcdgs6.dll          | IPX-Servertransport        | Windows NT                         |
| Rpcdgc3.dll          | Client-UDP-Transport        | Windows NT                         |
| Rpcdgs3.dll          | Server-UDP-Transport        | Windows NT                         |



 

Sie benötigen auch den MIDL-Compiler (Microsoft Interface Definition Language(midl).) Weitere Informationen finden Sie unter [Verwenden des MIDL-Compilers.](/windows/desktop/Midl/using-the-midl-compiler-2)

 

 