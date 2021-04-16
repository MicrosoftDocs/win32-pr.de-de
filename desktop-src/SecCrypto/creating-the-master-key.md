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
# <a name="creating-the-master-key"></a><span data-ttu-id="ba231-103">Erstellen des Haupt Schlüssels</span><span class="sxs-lookup"><span data-stu-id="ba231-103">Creating the Master Key</span></span>

<span data-ttu-id="ba231-104">Ein [*Hauptschlüssel*](../secgloss/m-gly.md) ist ein wichtiges Datenmaterial, von dem andere Schlüssel abgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="ba231-104">A [*master key*](../secgloss/m-gly.md) is key data material from which other keys are derived.</span></span> <span data-ttu-id="ba231-105">Je nach verwendetem Protokoll und Verschlüsselungs Sammlung kann der Hauptschlüssel zwischen 5 und 48 Byte lang sein.</span><span class="sxs-lookup"><span data-stu-id="ba231-105">Depending on the protocol and cipher suite used, the master key can be from 5 to 48 bytes in length.</span></span> <span data-ttu-id="ba231-106">Für den [*RSA*](../secgloss/r-gly.md) / [*SChannel*](../secgloss/s-gly.md) CSP wird der Hauptschlüssel von der Clientseite erstellt und in einem RSA-Umschlag auf den Server übertragen.</span><span class="sxs-lookup"><span data-stu-id="ba231-106">For the [*RSA*](../secgloss/r-gly.md)/[*Schannel*](../secgloss/s-gly.md) CSP, the master key is created by the client-side and transferred to the server in an RSA envelope.</span></span> <span data-ttu-id="ba231-107">Für einen [*Diffie-Hellman*](../secgloss/d-gly.md)/SChannel CSP wird der Hauptschlüssel erstellt, indem ein Diffie-Hellman Schlüsselaustausch durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ba231-107">For a [*Diffie-Hellman*](../secgloss/d-gly.md)/Schannel CSP, the master key is created by performing a Diffie-Hellman key exchange.</span></span>

<span data-ttu-id="ba231-108">Code zum Erstellen und Austauschen von Haupt Schlüsseln wird in veranschaulicht:</span><span class="sxs-lookup"><span data-stu-id="ba231-108">Code for creating and exchanging master keys is demonstrated in:</span></span>

-   [<span data-ttu-id="ba231-109">Diffie-Hellman-Client Code zum Erstellen des Haupt Schlüssels</span><span class="sxs-lookup"><span data-stu-id="ba231-109">Diffie-Hellman Client Code for Creating the Master Key</span></span>](diffie-hellman-client-code-for-creating-the-master-key.md)
-   [<span data-ttu-id="ba231-110">Diffie-Hellman-Server Code zum Erstellen des Haupt Schlüssels</span><span class="sxs-lookup"><span data-stu-id="ba231-110">Diffie-Hellman Server Code for Creating the Master Key</span></span>](diffie-hellman-server-code-for-creating-the-master-key.md)
-   [<span data-ttu-id="ba231-111">RSA-Client Code zum Erstellen des Haupt Schlüssels</span><span class="sxs-lookup"><span data-stu-id="ba231-111">RSA Client Code for Creating the Master Key</span></span>](rsa-client-code-for-creating-the-master-key.md)
-   [<span data-ttu-id="ba231-112">RSA-Server Code zum Erstellen des Haupt Schlüssels</span><span class="sxs-lookup"><span data-stu-id="ba231-112">RSA Server Code for Creating the Master Key</span></span>](rsa-server-code-for-creating-the-master-key.md)
-   [<span data-ttu-id="ba231-113">Angeben der Algorithmen</span><span class="sxs-lookup"><span data-stu-id="ba231-113">Specifying the Algorithms</span></span>](specifying-the-algorithms.md)

 

 
