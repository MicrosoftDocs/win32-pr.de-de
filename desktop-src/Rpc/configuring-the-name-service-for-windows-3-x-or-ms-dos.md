---
title: Konfigurieren des Namensdiensts für Windows 3.x oder MS-DOS
description: Remoteprozeduraufruf (RPC) und Konfigurieren des Namensdiensts für Windows 3.x oder MS-DOS.
ms.assetid: 7b22a12e-43d0-4e32-a191-d63a56559143
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24884c782913c47806c702ff129594c6524fe7c0e731561de405f3b6a360c7c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120022430"
---
# <a name="configuring-the-name-service-for-windows-3x-or-ms-dos"></a>Konfigurieren des Namensdiensts für Windows 3.x oder MS-DOS

Wenn Sie Setup.exe ausführen, um die 16-Bit-RPC-Laufzeitbibliothek zu installieren, werden Sie aufgefordert, einen Namendienstanbieter auszuwählen:

-   Wenn Sie **Standardnamendienstanbieter installieren** auswählen, wird der Standard-NSP(Microsoft Locator) installiert.
-   Wenn Sie **Benutzerdefinierten Namensdienstanbieter installieren** auswählen, schließen Sie das Dialogfeld **Netzwerkadresse definieren** ab, um den DCE-Zellenverzeichnisdienst als NSP zu installieren. Der DCE-Zellenverzeichnisdienst ist der NSP, der mit DCE-Servern verwendet wird.

Die Netzwerkadresse ist der Name des Hostcomputers, auf dem der NSI-Daemon (nsid) ausgeführt wird. Dieser Computer fungiert als Gateway für den DCE-Zellenverzeichnisdienst und übergibt NSI-Funktionsaufrufe zwischen Computern, auf denen Microsoft-Betriebssysteme und DCE-Computer ausgeführt werden. Die Netzwerkadresse kann maximal 80 Zeichen umfassen, z.B. ist 11.1.9.169 eine gültige Adresse.

 

 




