---
description: Ein Hauptschlüssel ist ein wichtiges Datenmaterial, von dem andere Schlüssel abgeleitet werden.
ms.assetid: c8445f74-659a-470b-9007-07ea98d36dcd
title: Erstellen des Haupt Schlüssels
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b35a6aef52525bdce622355ede4ae9723f7cd8b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525739"
---
# <a name="creating-the-master-key"></a>Erstellen des Haupt Schlüssels

Ein [*Hauptschlüssel*](../secgloss/m-gly.md) ist ein wichtiges Datenmaterial, von dem andere Schlüssel abgeleitet werden. Je nach verwendetem Protokoll und Verschlüsselungs Sammlung kann der Hauptschlüssel zwischen 5 und 48 Byte lang sein. Für den [*RSA*](../secgloss/r-gly.md) / [*SChannel*](../secgloss/s-gly.md) CSP wird der Hauptschlüssel von der Clientseite erstellt und in einem RSA-Umschlag auf den Server übertragen. Für einen [*Diffie-Hellman*](../secgloss/d-gly.md)/SChannel CSP wird der Hauptschlüssel erstellt, indem ein Diffie-Hellman Schlüsselaustausch durchgeführt wird.

Code zum Erstellen und Austauschen von Haupt Schlüsseln wird in veranschaulicht:

-   [Diffie-Hellman-Client Code zum Erstellen des Haupt Schlüssels](diffie-hellman-client-code-for-creating-the-master-key.md)
-   [Diffie-Hellman-Server Code zum Erstellen des Haupt Schlüssels](diffie-hellman-server-code-for-creating-the-master-key.md)
-   [RSA-Client Code zum Erstellen des Haupt Schlüssels](rsa-client-code-for-creating-the-master-key.md)
-   [RSA-Server Code zum Erstellen des Haupt Schlüssels](rsa-server-code-for-creating-the-master-key.md)
-   [Angeben der Algorithmen](specifying-the-algorithms.md)

 

 
