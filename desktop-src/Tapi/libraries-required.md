---
description: Im Folgenden finden Sie eine Liste der LIB-Dateien, die zum Kompilieren verschiedener TAPI 3-Anwendungen ab dem 22.1.2011 erforderlich sind.
ms.assetid: f1765829-9a5d-4e85-b898-6679279aa6d9
title: Erforderliche Bibliotheken
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8337042681d84b5f93d5d0218cff18c4bef9259543f60fd13f692ebe5611835
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119621360"
---
# <a name="libraries-required"></a>Erforderliche Bibliotheken

Eine Liste der LIB-Dateien, die zum Kompilieren verschiedener TAPI 3-Anwendungen erforderlich sind, ab dem 22.1.2011:

-   Advapi32.lib
-   Amstrmid.lib (ActiveMovie-GUIDs)
-   Kernel32.lib
-   Mdhcpid.lib (Multicast-GUIDs)
-   Ole32.lib (COM)
-   Oleaut32.lib (COM-Automatisierung)
-   Rendid.lib (Rendezvous-GUIDs)
-   Rpcndr.lib
-   Rpcns4.lib
-   Rpcrt4.lib
-   Sdpblbid.lib (SDP-GUIDs (Session Descriptor Protocol)
-   Strmiids.lib
-   User32.lib
-   Uuid.lib
-   Wldap32.lib
-   Ws2 \_ 32.lib

Wenn Sie die Microsoft Visual Studio, müssen Sie möglicherweise Ihre Version aktualisieren. Insbesondere müssen Link.exe Datum 19.03.98 oder höher haben.

Compiler definiert muss WIN32 WINNT enthalten, das mindestens auf 0x500 \_ \_ und \_ WIN32 \_ DCOM festgelegt ist.

 

 



