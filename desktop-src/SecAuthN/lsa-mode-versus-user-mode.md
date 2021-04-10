---
description: Wenn ein SSP/AP-Sicherheitspaket als Authentifizierungs Paket fungiert, wird es in den Prozessbereich der lokalen Sicherheits Autorität (Local Security Authority, LSA) geladen und befindet sich im LSA-Modus.
ms.assetid: ff4e61be-dbaa-4cfa-8c72-43e99fe1c3cb
title: LSA-Modus im Vergleich zum Benutzermodus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd8fadde30fe60c38a2b8ccb1f158d94ec7d5603
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050284"
---
# <a name="lsa-mode-vs-user-mode"></a><span data-ttu-id="c6f7d-103">LSA-Modus im Vergleich zum Benutzermodus</span><span class="sxs-lookup"><span data-stu-id="c6f7d-103">LSA Mode vs. User Mode</span></span>

<span data-ttu-id="c6f7d-104">Wenn ein SSP/AP- [*Sicherheitspaket*](../secgloss/s-gly.md) als [*Authentifizierungs Paket*](../secgloss/a-gly.md)fungiert, wird es in den Prozessbereich der [*lokalen Sicherheits Autorität (Local Security Authority*](../secgloss/l-gly.md) , LSA) geladen und befindet sich im LSA-Modus.</span><span class="sxs-lookup"><span data-stu-id="c6f7d-104">When an SSP/AP [*security package*](../secgloss/s-gly.md) is functioning as an [*authentication package*](../secgloss/a-gly.md), it is loaded into the process space of the [*Local Security Authority*](../secgloss/l-gly.md) (LSA) and is said to be in LSA mode.</span></span> <span data-ttu-id="c6f7d-105">Anmelde Anwendungen greifen mithilfe der [LSA-Anmelde Funktionen](authentication-functions.md)auf die Funktionen des Authentifizierungs Pakets zu.</span><span class="sxs-lookup"><span data-stu-id="c6f7d-105">Logon applications access authentication package functionality using the [LSA Logon Functions](authentication-functions.md).</span></span> <span data-ttu-id="c6f7d-106">Entwickler können LSA-Unterstützungsfunktionen verwenden, die nur im LSA-Modus verfügbar sind, um komplexere Authentifizierungs Pakete zu implementieren, als zuvor unterstützt wurden.</span><span class="sxs-lookup"><span data-stu-id="c6f7d-106">Developers can use LSA support functions available only to LSA-mode security packages to implement more sophisticated authentication packages than previously supported.</span></span>

<span data-ttu-id="c6f7d-107">Wenn ein [*Sicherheitspaket*](../secgloss/s-gly.md) Sicherheitsdienste für eine Client/Server-Anwendung bereitstellt, wird es in die Client-und Server Prozesse geladen und als Benutzermodus bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="c6f7d-107">When a [*security package*](../secgloss/s-gly.md) provides security services to a client/server application, it is loaded into the client and server processes and is said to be in user mode.</span></span> <span data-ttu-id="c6f7d-108">Client-/Serveranwendungen greifen mithilfe der Microsoft [*Security Support Provider Interface*](../secgloss/s-gly.md) (SSPI) auf die Sicherheits Unterstützungsdienste des Sicherheitspakets zu.</span><span class="sxs-lookup"><span data-stu-id="c6f7d-108">Client/server applications access the security package's security support services using Microsoft [*Security Support Provider Interface*](../secgloss/s-gly.md) (SSPI).</span></span>

<span data-ttu-id="c6f7d-109">LSA-Unterstützung für SSP/APS umfasst Funktionen, die der LSA-Modus und die benutzermodusinstanzen eines Sicherheitspakets für die Kommunikation verwenden können.</span><span class="sxs-lookup"><span data-stu-id="c6f7d-109">LSA support for SSP/APs includes functions that the LSA-mode and user-mode instances of a security package can use to communicate.</span></span> <span data-ttu-id="c6f7d-110">Darüber hinaus kann die benutzermodusinstanz eines Sicherheitspakets ausgewählte Anforderungen nach Informationen an die Instanz des Pakets im LSA-Modus delegieren.</span><span class="sxs-lookup"><span data-stu-id="c6f7d-110">Additionally, the user-mode instance of a security package can delegate selected requests for information to the LSA-mode instance of the package.</span></span>

<span data-ttu-id="c6f7d-111">Ausführliche Informationen dazu, wie Sicherheitspakete für jeden Modus initialisiert werden, finden Sie unter [Initialisierung im LSA-Modus](lsa-mode-initialization.md) und [Initialisierung im Benutzermodus](user-mode-initialization.md).</span><span class="sxs-lookup"><span data-stu-id="c6f7d-111">For details about how security packages are initialized for each mode, see [LSA-mode Initialization](lsa-mode-initialization.md) and [User-mode Initialization](user-mode-initialization.md).</span></span>

 

 
