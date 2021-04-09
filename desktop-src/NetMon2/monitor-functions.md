---
description: In diesem Abschnitt werden die Hilfsfunktionen beschrieben, die Sie zum Entwickeln von benutzerdefinierten Monitoren verwenden können.
ms.assetid: 2c019183-9823-4e34-bb41-cf35f2731b8f
title: Überwachen von Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9391927104196e282d4438c0b047e233d61f3619
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862855"
---
# <a name="monitor-functions"></a><span data-ttu-id="da9cc-103">Überwachen von Funktionen</span><span class="sxs-lookup"><span data-stu-id="da9cc-103">Monitor Functions</span></span>

<span data-ttu-id="da9cc-104">In diesem Abschnitt werden die Hilfsfunktionen beschrieben, die Sie zum Entwickeln von benutzerdefinierten Monitoren verwenden können.</span><span class="sxs-lookup"><span data-stu-id="da9cc-104">This section describes the helper functions you can use to develop custom monitors.</span></span>



| <span data-ttu-id="da9cc-105">Funktion</span><span class="sxs-lookup"><span data-stu-id="da9cc-105">Function</span></span>                                       | <span data-ttu-id="da9cc-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="da9cc-106">Description</span></span>                                                                                                                                                      |
|------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="da9cc-107">Dllgetmonitorobject</span><span class="sxs-lookup"><span data-stu-id="da9cc-107">DllGetMonitorObject</span></span>](dllgetmonitorobject.md) | <span data-ttu-id="da9cc-108">Erstellt eine Instanz des Monitors.</span><span class="sxs-lookup"><span data-stu-id="da9cc-108">Creates an instance of the monitor.</span></span>                                                                                                                              |
| [<span data-ttu-id="da9cc-109">Htmlvaluetounicode</span><span class="sxs-lookup"><span data-stu-id="da9cc-109">HTMLValueToUnicode</span></span>](htmlvaluetounicode.md)   | <span data-ttu-id="da9cc-110">Konvertiert eine HTML CP \_ UTF8-Versions Zeichenfolge in Unicode.</span><span class="sxs-lookup"><span data-stu-id="da9cc-110">Converts an HTML CP\_UTF8 version string to Unicode.</span></span>                                                                                                             |
| [<span data-ttu-id="da9cc-111">Loaddword</span><span class="sxs-lookup"><span data-stu-id="da9cc-111">LoadDWORD</span></span>](loaddword.md)                     | <span data-ttu-id="da9cc-112">Lädt ein **DWORD** aus einer HTML-Konfigurations Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="da9cc-112">Loads a **DWORD** from an HTML configuration string.</span></span>                                                                                                             |
| [<span data-ttu-id="da9cc-113">Loadipadressen</span><span class="sxs-lookup"><span data-stu-id="da9cc-113">LoadIPAddresses</span></span>](loadipaddresses.md)         | <span data-ttu-id="da9cc-114">Lädt eine IP-Adressliste aus einer HTML-TEXTAREA-Konfigurations Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="da9cc-114">Loads an IP address list from an HTML TEXTAREA configuration string.</span></span>                                                                                             |
| [<span data-ttu-id="da9cc-115">Loadipxadressen</span><span class="sxs-lookup"><span data-stu-id="da9cc-115">LoadIPXAddresses</span></span>](loadipxaddresses.md)       | <span data-ttu-id="da9cc-116">Lädt eine IPX-Adressliste aus einer HTML-TEXTAREA-Konfigurations Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="da9cc-116">Loads an IPX address list from an HTML TEXTAREA configuration string.</span></span>                                                                                            |
| [<span data-ttu-id="da9cc-117">Loadmacadressen</span><span class="sxs-lookup"><span data-stu-id="da9cc-117">LoadMACAddresses</span></span>](loadmacaddresses.md)       | <span data-ttu-id="da9cc-118">Lädt eine Mac-Adressliste aus einer HTML-TEXTAREA-Konfigurations Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="da9cc-118">Loads a MAC address list from an HTML TEXTAREA configuration string.</span></span>                                                                                             |
| [<span data-ttu-id="da9cc-119">Loadstringaddr</span><span class="sxs-lookup"><span data-stu-id="da9cc-119">LoadStringAddr</span></span>](loadstringaddr.md)           | <span data-ttu-id="da9cc-120">Wandelt eine Zeichenfolge (z. b. "157.54.32.45") in eine **DWORD** -Adresse um.</span><span class="sxs-lookup"><span data-stu-id="da9cc-120">Transforms a string (such as "157.54.32.45") to a **DWORD** address.</span></span>                                                                                             |
| [<span data-ttu-id="da9cc-121">Loadtchar</span><span class="sxs-lookup"><span data-stu-id="da9cc-121">LoadTCHAR</span></span>](loadtchar.md)                     | <span data-ttu-id="da9cc-122">Sucht in der Konfigurations Zeichenfolge nach einem angeforderten Variablennamen und ordnet ausreichend Speicherplatz (mithilfe von **heapbelegcmemory**) zu, um ihn zu speichern, zu kopieren und zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="da9cc-122">Searches for a requested variable name in the configuration string, and allocates sufficient space (by using **HeapAllocMemory**) to store, copy, and return it.</span></span> |
| [<span data-ttu-id="da9cc-123">Onloadingdll</span><span class="sxs-lookup"><span data-stu-id="da9cc-123">OnLoadingDLL</span></span>](onloadingdll.md)               | <span data-ttu-id="da9cc-124">Gibt an, dass die DLL bereits geladen wurde.</span><span class="sxs-lookup"><span data-stu-id="da9cc-124">Indicates that the DLL has begun to load.</span></span> <span data-ttu-id="da9cc-125">Die mcsvc ruft diese Funktion auf, wenn Sie zum ersten Mal die Monitor-DLL lädt.</span><span class="sxs-lookup"><span data-stu-id="da9cc-125">The MCSVC calls this function when it first loads the monitor DLL.</span></span>                                                     |



 

 

 



