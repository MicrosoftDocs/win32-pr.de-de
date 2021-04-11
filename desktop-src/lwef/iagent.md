---
title: Iagent
description: Iagent
ms.assetid: 35b12006-a938-450c-969a-7b73a3768a4d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12900a4288b9917d695dd25d4b81362b67c93587
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310051"
---
# <a name="iagent"></a><span data-ttu-id="9099c-103">Iagent</span><span class="sxs-lookup"><span data-stu-id="9099c-103">IAgent</span></span>

<span data-ttu-id="9099c-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="9099c-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="9099c-105">**Iagent** definiert eine Schnittstelle, die es Anwendungen ermöglicht, Zeichen zu laden, Ereignisse zu empfangen und den aktuellen Status des Microsoft-Agent-Servers zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="9099c-105">**IAgent** defines an interface that allows applications to load characters, receive events, and check the current state of the Microsoft Agent Server.</span></span> <span data-ttu-id="9099c-106">Diese Funktionen sind auch über [**iagentex**](iagentex.md)verfügbar.</span><span class="sxs-lookup"><span data-stu-id="9099c-106">These functions are also available from [**IAgentEx**](iagentex.md).</span></span>

<span data-ttu-id="9099c-107">Die in früheren Versionen enthaltene getangeh-Methode ist veraltet und gibt aus Gründen der Abwärtskompatibilität **false** zurück.</span><span class="sxs-lookup"><span data-stu-id="9099c-107">The GetSuspended method included in previous versions is obsolete and returns **False** for backward compatibility.</span></span>

<span data-ttu-id="9099c-108">**Methoden in Vtable-Reihenfolge**</span><span class="sxs-lookup"><span data-stu-id="9099c-108">**Methods in Vtable Order**</span></span>



| <span data-ttu-id="9099c-109">Iagent-Methoden</span><span class="sxs-lookup"><span data-stu-id="9099c-109">IAgent Methods</span></span>                               | <span data-ttu-id="9099c-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9099c-110">Description</span></span>                                                   |
|----------------------------------------------|---------------------------------------------------------------|
| [<span data-ttu-id="9099c-111">**Laden**</span><span class="sxs-lookup"><span data-stu-id="9099c-111">**Load**</span></span>](load-method.md)                  | <span data-ttu-id="9099c-112">Lädt die Datendatei eines Zeichens.</span><span class="sxs-lookup"><span data-stu-id="9099c-112">Loads a character's data file.</span></span>                                |
| [<span data-ttu-id="9099c-113">**Entladen**</span><span class="sxs-lookup"><span data-stu-id="9099c-113">**Unload**</span></span>](unload-method.md)              | <span data-ttu-id="9099c-114">Entlädt die Datendatei eines Zeichens.</span><span class="sxs-lookup"><span data-stu-id="9099c-114">Unloads a character's data file.</span></span>                              |
| [<span data-ttu-id="9099c-115">**Registrieren**</span><span class="sxs-lookup"><span data-stu-id="9099c-115">**Register**</span></span>](iagent--register.md)         | <span data-ttu-id="9099c-116">Registriert eine Benachrichtigungs Senke für den Client.</span><span class="sxs-lookup"><span data-stu-id="9099c-116">Registers a notification sink for the client.</span></span>                 |
| [<span data-ttu-id="9099c-117">**Unegiester**</span><span class="sxs-lookup"><span data-stu-id="9099c-117">**Unegister**</span></span>](iagent--unregister.md)      | <span data-ttu-id="9099c-118">Hebt die Registrierung der Benachrichtigungs Senke eines Clients auf.</span><span class="sxs-lookup"><span data-stu-id="9099c-118">Unregisters a client's notification sink.</span></span>                     |
| [<span data-ttu-id="9099c-119">**Getcharacter**</span><span class="sxs-lookup"><span data-stu-id="9099c-119">**GetCharacter**</span></span>](iagent--getcharacter.md) | <span data-ttu-id="9099c-120">Gibt die iagentcharacter-Schnittstelle für ein geladenes Zeichen zurück.</span><span class="sxs-lookup"><span data-stu-id="9099c-120">Returns the IAgentCharacter interface for a loaded character.</span></span> |



 

 

 




