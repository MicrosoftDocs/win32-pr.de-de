---
title: Konfigurieren des Namens Dienstanbieter für Windows 3. x oder MS-DOS
description: Remote Prozedur Aufruf (RPC) und Konfigurieren des Namens Dienstanbieter für Windows 3. x oder MS-DOS.
ms.assetid: 7b22a12e-43d0-4e32-a191-d63a56559143
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 533a0d8556f9cc51d0842768d0df1bdd0d553b5d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037118"
---
# <a name="configuring-the-name-service-for-windows-3x-or-ms-dos"></a>Konfigurieren des Namens Dienstanbieter für Windows 3. x oder MS-DOS

Wenn Sie Setup.exe ausführen, um die 16-Bit-RPC-Lauf Zeit Bibliothek zu installieren, werden Sie aufgefordert, einen Namen Dienstanbieter auszuwählen:

-   Wenn Sie die Option **Default Name Service Provider installieren** auswählen, wird der Standard-NSP, Microsoft Locator, installiert.
-   Wenn Sie **benutzerdefinierten Namen Dienstanbieter installieren** auswählen, vervollständigen Sie das Dialogfeld **Netzwerkadresse definieren** , um den DCE-Zell Verzeichnisdienst als NSP zu installieren. Der DCE-Zell Verzeichnisdienst ist das NSP, das mit DCE-Servern verwendet wird.

Die Netzwerkadresse ist der Name des Host Computers, auf dem der NSI-Daemon (nsid) ausgeführt wird. Dieser Computer fungiert als Gateway für den DCE-Zell Verzeichnisdienst und übergibt NSI-Funktionsaufrufe zwischen Computern, auf denen Microsoft-Betriebssysteme und DCE-Computer ausgeführt werden. Die Netzwerkadresse kann 80 Zeichen oder weniger betragen – beispielsweise ist 11.1.9.169 eine gültige Adresse.

 

 




