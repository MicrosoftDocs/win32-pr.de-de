---
description: Die Erweiterbarkeit wird erreicht, indem neue Objekt Bezeichner (OIDs), neue Codierungs Typen und neue DLLs verwendet werden.
ms.assetid: 95e992fe-af30-4b4e-b20d-cfe5318d0a38
title: OID-Übersicht
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9cc371d18bd144ac68c7bc95d7b3ef71140b2e1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866967"
---
# <a name="oid-overview"></a><span data-ttu-id="9a248-103">OID-Übersicht</span><span class="sxs-lookup"><span data-stu-id="9a248-103">OID Overview</span></span>

<span data-ttu-id="9a248-104">Die Erweiterbarkeit wird erreicht, indem neue [*Objekt*](../secgloss/o-gly.md) Bezeichner (OIDs), neue Codierungs Typen und neue DLLs verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9a248-104">Extensibility is achieved by providing for the use of new [*object identifiers*](../secgloss/o-gly.md) (OIDs), new encoding types, and new DLLs.</span></span>

<span data-ttu-id="9a248-105">CryptoAPI-OIDs können eine der folgenden Formen annehmen:</span><span class="sxs-lookup"><span data-stu-id="9a248-105">CryptoAPI OIDs can take any of the following forms:</span></span>

-   <span data-ttu-id="9a248-106">Eine numerische Zeichenfolge, z. b. "1.2.3.500.88"</span><span class="sxs-lookup"><span data-stu-id="9a248-106">A numeric string such as "1.2.3.500.88"</span></span>
-   <span data-ttu-id="9a248-107">Eine alphanumerische Zeichenfolge, z. b. *MyFunction*</span><span class="sxs-lookup"><span data-stu-id="9a248-107">An alphanumeric string such as *MyFunction*</span></span>
-   <span data-ttu-id="9a248-108">Eine Konstante mit einem Wert, der kleiner oder gleich 0xFFFF ist.</span><span class="sxs-lookup"><span data-stu-id="9a248-108">A constant with a value that is less than or equal to 0xFFFF.</span></span> <span data-ttu-id="9a248-109">Diese Konstanten sind häufig mit einem Namen verknüpft, indem eine **\# define** -Anweisung in einer Header Datei verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9a248-109">These constants are often associated with a name through the use of a **\#define** statement in a header file.</span></span>

<span data-ttu-id="9a248-110">Erweiterbare Funktionen akzeptieren OID-und Codierungstyp Argumente.</span><span class="sxs-lookup"><span data-stu-id="9a248-110">Extensible functions accept OID and encoding type arguments.</span></span> <span data-ttu-id="9a248-111">Diese Funktionen durchsuchen die Systemregistrierung, um eine DLL zu suchen, die den OID-und Codierungstyp Argumenten der Funktion zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="9a248-111">These functions search the system registry to find a DLL associated with the OID and encoding type arguments passed to the function.</span></span> <span data-ttu-id="9a248-112">Wenn eine DLL für die OID, Codierungstyp Kombination gefunden wird, wird die dll geladen, und die zugehörige Funktion wird aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="9a248-112">If a DLL for the OID, encoding type combination is found, the DLL is loaded and its function is called.</span></span> <span data-ttu-id="9a248-113">Die folgende Abbildung zeigt diesen Ablauf für die [**cryptencodeobject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject) -Funktion:</span><span class="sxs-lookup"><span data-stu-id="9a248-113">The following illustration shows this flow for the [**CryptEncodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject) function:</span></span>

![OID-Fluss](images/oidflow.png)

<span data-ttu-id="9a248-115">Dadurch kann die Funktionalität der kryptoapi nach Bedarf erweitert werden.</span><span class="sxs-lookup"><span data-stu-id="9a248-115">This allows the functionality of the CryptoAPI to be extended as the need arises.</span></span> <span data-ttu-id="9a248-116">Durch die Verwendung dieser Methodik können Entwickler der neuen Funktionalität den gesamten erforderlichen Code für diese Funktionalität schreiben.</span><span class="sxs-lookup"><span data-stu-id="9a248-116">Use of this methodology places a burden on the developer of the new functionality to write all the necessary code for that functionality.</span></span> <span data-ttu-id="9a248-117">Zum Codieren einer neuen Datenstruktur muss z. b. die-Funktion in der DLL den gesamten Codierungsprozess ausführen.</span><span class="sxs-lookup"><span data-stu-id="9a248-117">To encode some new data structure, for example, the function in the DLL must perform the entire encoding process.</span></span>

 

 
