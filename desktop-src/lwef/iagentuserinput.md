---
title: Iagentuserinput
description: Iagentuserinput
ms.assetid: 59ce7337-6031-4449-8b29-fd0c6737c3e8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b37d195d6b5d1294c071a1b73d1da95548cb7a0
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104390237"
---
# <a name="iagentuserinput"></a><span data-ttu-id="8e8af-103">Iagentuserinput</span><span class="sxs-lookup"><span data-stu-id="8e8af-103">IAgentUserInput</span></span>

<span data-ttu-id="8e8af-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="8e8af-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="8e8af-105">Wenn vom Server der Eingabe-aktiv-Client mit dem [**Befehl iagentnotifysink::**](iagentnotifysink--command.md)benachrichtigt wird, werden Informationen über das [**iagentuserinput**](/windows/desktop/lwef/iagentuserinput) -Objekt zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8e8af-105">When the server notifies the input-active client with [**IAgentNotifySink::Command**](iagentnotifysink--command.md), it returns information through the [**IAgentUserInput**](/windows/desktop/lwef/iagentuserinput) object.</span></span> <span data-ttu-id="8e8af-106">**Iagentuserinput** definiert eine Schnittstelle, die es Anwendungen ermöglicht, diese Werte abzufragen.</span><span class="sxs-lookup"><span data-stu-id="8e8af-106">**IAgentUserInput** defines an interface that allows applications to query these values.</span></span>

<span data-ttu-id="8e8af-107">**Methoden in Vtable-Reihenfolge**</span><span class="sxs-lookup"><span data-stu-id="8e8af-107">**Methods in Vtable Order**</span></span>



| <span data-ttu-id="8e8af-108">Iagentuserinput-Methoden</span><span class="sxs-lookup"><span data-stu-id="8e8af-108">IAgentUserInput Methods</span></span>                                         | <span data-ttu-id="8e8af-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8e8af-109">Description</span></span>                                                                                                                              |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8e8af-110">**GetCount**</span><span class="sxs-lookup"><span data-stu-id="8e8af-110">**GetCount**</span></span>](iagentuserinput--getcount.md)                   | <span data-ttu-id="8e8af-111">Gibt die Anzahl der Befehls Alternativen zurück, die in einem [**Befehls**](command-event.md) Ereignis zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="8e8af-111">Returns the number of command alternatives returned in a [**Command**](command-event.md) event.</span></span>                                         |
| [<span data-ttu-id="8e8af-112">**GetItemID**</span><span class="sxs-lookup"><span data-stu-id="8e8af-112">**GetItemID**</span></span>](iagentuserinput--getitemid.md)                 | <span data-ttu-id="8e8af-113">Gibt die ID für eine bestimmte [**Befehls**](command-event.md) Alternative zurück.</span><span class="sxs-lookup"><span data-stu-id="8e8af-113">Returns the ID for a specific [**Command**](command-event.md) alternative.</span></span>                                                              |
| [<span data-ttu-id="8e8af-114">**Getitemconfidence**</span><span class="sxs-lookup"><span data-stu-id="8e8af-114">**GetItemConfidence**</span></span>](iagentuserinput--getitemconfidence.md) | <span data-ttu-id="8e8af-115">Gibt den Wert der [**Confidence**](confidence-property.md) -Eigenschaft für eine bestimmte [**Befehls**](command-event.md) Alternative zurück.</span><span class="sxs-lookup"><span data-stu-id="8e8af-115">Returns the value of the [**Confidence**](confidence-property.md) property for a specific [**Command**](command-event.md) alternative.</span></span> |
| [<span data-ttu-id="8e8af-116">**GetItemText**</span><span class="sxs-lookup"><span data-stu-id="8e8af-116">**GetItemText**</span></span>](iagentuserinput--getitemtext.md)             | <span data-ttu-id="8e8af-117">Gibt den Wert von [**voicetext für**](voice-property.md) eine bestimmte [**Befehls**](command-event.md) Alternative zurück.</span><span class="sxs-lookup"><span data-stu-id="8e8af-117">Returns the value of [**Voice**](voice-property.md) text for a specific [**Command**](command-event.md) alternative.</span></span>                   |
| [<span data-ttu-id="8e8af-118">**Getallitemdata**</span><span class="sxs-lookup"><span data-stu-id="8e8af-118">**GetAllItemData**</span></span>](iagentuserinput--getallitemdata.md)       | <span data-ttu-id="8e8af-119">Gibt die Daten für alle [**Befehls**](command-event.md) Alternativen zurück.</span><span class="sxs-lookup"><span data-stu-id="8e8af-119">Returns the data for all [**Command**](command-event.md) alternatives.</span></span>                                                                  |



 

 

 