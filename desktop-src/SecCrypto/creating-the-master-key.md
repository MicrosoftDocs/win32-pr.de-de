---
description: Ein Hauptschlüssel ist Schlüsseldatenmaterial, von dem andere Schlüssel abgeleitet werden.
ms.assetid: c8445f74-659a-470b-9007-07ea98d36dcd
title: Erstellen des Hauptschlüssels
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dea47c64348f89563340a4e25d411ed3174ee9d18ba1705d9707eab6b39633b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876530"
---
# <a name="creating-the-master-key"></a>Erstellen des Hauptschlüssels

Ein [*Hauptschlüssel*](../secgloss/m-gly.md) ist Schlüsseldatenmaterial, von dem andere Schlüssel abgeleitet werden. Abhängig vom verwendeten Protokoll und der verwendeten Verschlüsselungssammlung kann der Hauptschlüssel zwischen 5 und 48 Bytes lang sein. Für den [*RSA*](../secgloss/r-gly.md) / [*Schannel-CSP*](../secgloss/s-gly.md) wird der Hauptschlüssel vom clientseitigen erstellt und in einem RSA-Umschlag an den Server übertragen. Für einen [*Diffie-Hellman/Schannel-CSP*](../secgloss/d-gly.md)wird der Hauptschlüssel erstellt, indem ein Diffie-Hellman Schlüsselaustausch durchgeführt wird.

Code zum Erstellen und Austauschen von Hauptschlüsseln wird in folgenden Beispielen veranschaulicht:

-   [Diffie-Hellman-Clientcode zum Erstellen des Hauptschlüssels](diffie-hellman-client-code-for-creating-the-master-key.md)
-   [Diffie-Hellman-Servercode zum Erstellen des Hauptschlüssels](diffie-hellman-server-code-for-creating-the-master-key.md)
-   [RSA-Clientcode zum Erstellen des Hauptschlüssels](rsa-client-code-for-creating-the-master-key.md)
-   [RSA-Servercode zum Erstellen des Hauptschlüssels](rsa-server-code-for-creating-the-master-key.md)
-   [Angeben der Algorithmen](specifying-the-algorithms.md)

 

 
