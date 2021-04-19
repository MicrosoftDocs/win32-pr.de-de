---
description: Im folgenden finden Sie eine Liste der lib-Dateien, die zum Kompilieren verschiedener TAPI 3-Anwendungen (ab 1/22/01) erforderlich sind.
ms.assetid: f1765829-9a5d-4e85-b898-6679279aa6d9
title: Erforderliche Bibliotheken
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0948599041c466a337d2d6828750a9996dc8d813
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106350495"
---
# <a name="libraries-required"></a>Erforderliche Bibliotheken

Eine Liste von lib-Dateien, die erforderlich sind, um verschiedene TAPI 3-Anwendungen zu kompilieren, wie 1/22/01:

-   Advapi32. lib
-   Amstrinmid. lib (ActiveMovie-GUIDs)
-   Kernel32.lib
-   Mdhcpid. lib (Multicast-GUIDs)
-   Ole32. lib (com)
-   Oleaut32. lib (com-Automatisierung)
-   Rendid. lib (Rendezvous-GUIDs)
-   Rpcndr. lib
-   Rpcns4. lib
-   Rpcrt4. lib
-   Sdpblbid. lib (Sitzungs Deskriptor Protocol (SDP) GUIDs)
-   "" "" ". Lib"
-   User32. lib
-   UUID. lib
-   Wldap32. lib
-   Ws2 \_ 32. lib

Wenn Sie Microsoft Visual Studio verwenden, müssen Sie möglicherweise Ihre Version aktualisieren. Insbesondere muss Link.exe ein Datum von 3/19/98 oder höher aufweisen.

Compilerdefinitionen müssen \_ Win32 \_ Winnt enthalten, das auf mindestens 0x500 und \_ Win32 DCOM festgelegt ist \_ .

 

 



