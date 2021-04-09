---
title: Entwickeln von RPC-Windows-Anwendungen
description: Wenn Sie das Platform Software Development Kit (SDK) installieren, werden die folgenden RPC-Entwicklungsumgebungen, die Laufzeitbibliotheken und Tools automatisch installiert.
ms.assetid: d5da3bca-5251-4ba4-b873-0817fe0f298d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b418358649d0cf7205b9a3bde236cf66d3ce81e0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039497"
---
# <a name="developing-rpc-windows-applications"></a>Entwickeln von RPC-Windows-Anwendungen

Wenn Sie das Platform Software Development Kit (SDK) installieren, werden die folgende RPC-Entwicklungsumgebung, die Laufzeitbibliotheken und-Tools automatisch installiert:

-   C/C++-sprach Header (. H) Dateien
-   RPC-Import Bibliotheken (. lib)
-   Beispiel Programme
-   RPC-Verweis Hilfedateien
-   Das Hilfsprogramm **"uuidgen**

Wenn Sie Windows installieren, werden Folgendes installiert:

-   RPC-Lauf Zeit-DLLs
-   Microsoft Locator (wird unter Windows Vista und höher nicht unterstützt)
-   RPC-Endpunkt-Mapping-Dienste

Die folgenden RPC-Import Bibliotheken.



| Bibliothek importieren | BESCHREIBUNG                |
|----------------|----------------------------|
| Rpcns4. lib     | Name-Service-Funktionen     |
| Rpcrt4. lib     | Windows-Lauf Zeitfunktionen |



 

> [!Note]  
> Rpcns4. lib ist veraltet und wird nicht mehr unterstützt.

 

Die folgenden RPC-Bibliotheken sind für die Unterstützung der untergeordneten Ebene enthalten.



| Dynamic Link Library | Beschreibung                 | Plattform                           |
|----------------------|-----------------------------|------------------------------------|
| Rpcltc1.dll          | Client Named Pipe-Transport | Windows NT, Windows 98, Windows 95 |
| Rpclts1.dll          | Server Named Pipe-Transport | Windows NT, Windows 98, Windows 95 |
| Rpcltc3.dll          | TCP/IP-Client Transport     | Windows NT, Windows 98, Windows 95 |
| Rpclts3.dll          | Server-TCP/IP-Transport     | Windows NT, Windows 98, Windows 95 |
| Rpcltc5.dll          | Client-NetBIOS-Transport    | Windows NT, Windows 98, Windows 95 |
| Rpclts5.dll          | Server-NetBIOS-Transport    | Windows NT, Windows 98, Windows 95 |
| Rpcltc6.dll          | Client-SPX-Transport        | Windows NT, Windows 98, Windows 95 |
| Rpclts6.dll          | Server-SPX-Transport        | Windows NT, Windows 98, Windows 95 |
| Rpcdgc6.dll          | IPX-Client Transport        | Windows NT                         |
| Rpcdgs6.dll          | IPX-Server Transport        | Windows NT                         |
| Rpcdgc3.dll          | UDP-Client Transport        | Windows NT                         |
| Rpcdgs3.dll          | UDP-Server Transport        | Windows NT                         |



 

Außerdem benötigen Sie den Microsoft Interface Definition Language-Compiler (mittlerer l). Weitere Informationen finden Sie unter [using the Mittel l Compiler](/windows/desktop/Midl/using-the-midl-compiler-2).

 

 