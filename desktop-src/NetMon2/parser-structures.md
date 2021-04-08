---
description: In diesem Abschnitt werden die Strukturen beschrieben, die Sie zum Entwickeln von-Parser verwenden können. Diese Strukturen werden von Funktionen verwendet, die Sie verwenden können, um Parser und Funktionen zu entwickeln, die Sie verwenden können, um entweder Parser oder Experten zu entwickeln.
ms.assetid: ce45a8ef-4355-46fd-909e-3ab4d63a3bf1
title: Parserstrukturen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59a9b767974214472f24ea9e1ec9359c97d26fc4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103961001"
---
# <a name="parser-structures"></a><span data-ttu-id="ee537-104">Parserstrukturen</span><span class="sxs-lookup"><span data-stu-id="ee537-104">Parser Structures</span></span>

<span data-ttu-id="ee537-105">In diesem Abschnitt werden die Strukturen beschrieben, die Sie zum Entwickeln von-Parser verwenden können.</span><span class="sxs-lookup"><span data-stu-id="ee537-105">This section describes structures you can use to develop parsers.</span></span> <span data-ttu-id="ee537-106">Diese Strukturen werden von Funktionen verwendet, die Sie verwenden können, um Parser und Funktionen zu entwickeln, die Sie verwenden können, um entweder Parser oder Experten zu entwickeln.</span><span class="sxs-lookup"><span data-stu-id="ee537-106">These structures are used by functions you can use to develop parsers and functions you can use to develop either parsers or experts.</span></span>



| <span data-ttu-id="ee537-107">Struktur</span><span class="sxs-lookup"><span data-stu-id="ee537-107">Structure</span></span>                                 | <span data-ttu-id="ee537-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ee537-108">Description</span></span>                                                                                                                     |
|-------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ee537-109">Macframe</span><span class="sxs-lookup"><span data-stu-id="ee537-109">MACFRAME</span></span>](macframe.md)                  | <span data-ttu-id="ee537-110">Definiert die am häufigsten verwendeten anfänglichen Protokolle.</span><span class="sxs-lookup"><span data-stu-id="ee537-110">Defines the most commonly used initial protocols.</span></span>                                                                               |
| [<span data-ttu-id="ee537-111">ENTRYPOINTS</span><span class="sxs-lookup"><span data-stu-id="ee537-111">ENTRYPOINTS</span></span>](entrypoints.md)            | <span data-ttu-id="ee537-112">Gibt Zeiger auf die Einstiegspunkte für die Parser-DLL an.</span><span class="sxs-lookup"><span data-stu-id="ee537-112">Specifies pointers to the entry points for the Parser DLL.</span></span>                                                                      |
| [<span data-ttu-id="ee537-113">PF-nach \_ Verfolgung</span><span class="sxs-lookup"><span data-stu-id="ee537-113">PF\_FOLLOWENTRY</span></span>](pf-followentry.md)     | <span data-ttu-id="ee537-114">Gibt das Protokoll an, das auf das aktuelle Protokoll folgt.</span><span class="sxs-lookup"><span data-stu-id="ee537-114">Specifies the protocol that follows the current protocol.</span></span>                                                                       |
| [<span data-ttu-id="ee537-115">PF-nach \_ Verfolgung</span><span class="sxs-lookup"><span data-stu-id="ee537-115">PF\_FOLLOWSET</span></span>](pf-followset.md)         | <span data-ttu-id="ee537-116">Gibt die Gruppe von Protokollen an, die auf das aktuelle Protokoll folgt.</span><span class="sxs-lookup"><span data-stu-id="ee537-116">Specifies the set of protocols that follows the current protocol.</span></span>                                                               |
| [<span data-ttu-id="ee537-117">PF- \_ handoffentry</span><span class="sxs-lookup"><span data-stu-id="ee537-117">PF\_HANDOFFENTRY</span></span>](pf-handoffentry.md)   | <span data-ttu-id="ee537-118">Gibt entweder das Protokoll an, das das aktuelle Protokoll übergibt, oder das Protokoll, an das das aktuelle Protokoll übergibt.</span><span class="sxs-lookup"><span data-stu-id="ee537-118">Specifies either the protocol that hands off to the current protocol or the protocol that the current protocol hands off to.</span></span>    |
| [<span data-ttu-id="ee537-119">PF- \_ handoffset</span><span class="sxs-lookup"><span data-stu-id="ee537-119">PF\_HANDOFFSET</span></span>](pf-handoffset.md)       | <span data-ttu-id="ee537-120">Gibt den Satz von Protokollen an, die an das aktuelle Protokoll oder den Satz von Protokollen übergeben werden, an die das aktuelle Protokoll übergibt.</span><span class="sxs-lookup"><span data-stu-id="ee537-120">Specifies the set of protocols that hand off to the current protocol or the set of protocols the current protocol hands off to.</span></span> |
| [<span data-ttu-id="ee537-121">PF- \_ Parser (Parser)</span><span class="sxs-lookup"><span data-stu-id="ee537-121">PF\_PARSERDLLINFO</span></span>](pf-parserdllinfo.md) | <span data-ttu-id="ee537-122">Gibt die Anzahl der Parser in der Parser-DLL und die Informationen zu den einzelnen Parser an.</span><span class="sxs-lookup"><span data-stu-id="ee537-122">Specifies the number of parsers in the parser DLL and information about each parser.</span></span>                                            |
| [<span data-ttu-id="ee537-123">PF-Parameter \_ Info</span><span class="sxs-lookup"><span data-stu-id="ee537-123">PF\_PARSERINFO</span></span>](pf-parserinfo.md)       | <span data-ttu-id="ee537-124">Gibt Informationen zu einem bestimmten Parser an.</span><span class="sxs-lookup"><span data-stu-id="ee537-124">Specifies information about a specific parser.</span></span>                                                                                  |
| [<span data-ttu-id="ee537-125">beschriftetes \_ Bit</span><span class="sxs-lookup"><span data-stu-id="ee537-125">LABELED\_BIT</span></span>](labeled-bit.md)           | <span data-ttu-id="ee537-126">Gibt Handles, Bitfelder oder Flags an.</span><span class="sxs-lookup"><span data-stu-id="ee537-126">Specifies handles, BIT fields, or flags.</span></span>                                                                                        |
| [<span data-ttu-id="ee537-127">beschriftete \_ Byte</span><span class="sxs-lookup"><span data-stu-id="ee537-127">LABELED\_BYTE</span></span>](labeled-byte.md)         | <span data-ttu-id="ee537-128">Gibt ein **Byte** Bezeichnungs Paar an.</span><span class="sxs-lookup"><span data-stu-id="ee537-128">Specifies a **BYTE** label pair.</span></span>                                                                                                |
| [<span data-ttu-id="ee537-129">gekennzeichnete \_ DWORD</span><span class="sxs-lookup"><span data-stu-id="ee537-129">LABELED\_DWORD</span></span>](labeled-dword.md)       | <span data-ttu-id="ee537-130">Gibt ein **DWORD** -Bezeichnungs Paar an.</span><span class="sxs-lookup"><span data-stu-id="ee537-130">Specifies a **DWORD** label pair.</span></span>                                                                                               |
| [<span data-ttu-id="ee537-131">gekennzeichnete \_ Word</span><span class="sxs-lookup"><span data-stu-id="ee537-131">LABELED\_WORD</span></span>](labeled-word.md)         | <span data-ttu-id="ee537-132">Gibt ein **Wort** Bezeichnungs Paar an.</span><span class="sxs-lookup"><span data-stu-id="ee537-132">Specifies a **WORD** label pair.</span></span>                                                                                                |
| [<span data-ttu-id="ee537-133">PROPERTYINFO</span><span class="sxs-lookup"><span data-stu-id="ee537-133">PROPERTYINFO</span></span>](propertyinfo.md)          | <span data-ttu-id="ee537-134">Gibt die Eigenschaften an, die der Protokoll Parser zum Beschreiben von Frames benötigt.</span><span class="sxs-lookup"><span data-stu-id="ee537-134">Specifies the properties that the protocol parser requires to describe frames.</span></span>                                                  |
| [<span data-ttu-id="ee537-135">Propertyinst</span><span class="sxs-lookup"><span data-stu-id="ee537-135">PROPERTYINST</span></span>](propertyinst.md)          | <span data-ttu-id="ee537-136">Gibt eine Instanz einer Eigenschaft in einem Frame an.</span><span class="sxs-lookup"><span data-stu-id="ee537-136">Specifies an instance of a property in a frame.</span></span>                                                                                 |
| [<span data-ttu-id="ee537-137">Propertyinstex</span><span class="sxs-lookup"><span data-stu-id="ee537-137">PROPERTYINSTEX</span></span>](propertyinstex.md)      | <span data-ttu-id="ee537-138">Gibt eine frei Form erweiterte Eigenschafts Instanz an.</span><span class="sxs-lookup"><span data-stu-id="ee537-138">Specifies a free-form, extended property instance.</span></span>                                                                              |
| [<span data-ttu-id="ee537-139">Protocolinfo</span><span class="sxs-lookup"><span data-stu-id="ee537-139">PROTOCOLINFO</span></span>](protocolinfo.md)          | <span data-ttu-id="ee537-140">Gibt ein Protokoll an.</span><span class="sxs-lookup"><span data-stu-id="ee537-140">Specifies a protocol.</span></span>                                                                                                           |
| [<span data-ttu-id="ee537-141">Bereich</span><span class="sxs-lookup"><span data-stu-id="ee537-141">RANGE</span></span>](range.md)                        | <span data-ttu-id="ee537-142">Gibt einen Bereich für eine Zahl an.</span><span class="sxs-lookup"><span data-stu-id="ee537-142">Specifies a range for a number.</span></span>                                                                                                 |
| [<span data-ttu-id="ee537-143">SET</span><span class="sxs-lookup"><span data-stu-id="ee537-143">SET</span></span>](set.md)                            | <span data-ttu-id="ee537-144">Gibt eine Tabelle mit Werten für eine Eigenschaft an.</span><span class="sxs-lookup"><span data-stu-id="ee537-144">Specifies a table of values for a property.</span></span>                                                                                     |



 

<span data-ttu-id="ee537-145">Informationen zu den Funktionen, die zum Entwickeln von Parser-DLLs verwendet werden, finden Sie in den folgenden Themen.</span><span class="sxs-lookup"><span data-stu-id="ee537-145">For information about functions used to develop parser DLLs, see the following topics.</span></span>



| <span data-ttu-id="ee537-146">Informationen über</span><span class="sxs-lookup"><span data-stu-id="ee537-146">For information about</span></span>                                         | <span data-ttu-id="ee537-147">Finden Sie unter</span><span class="sxs-lookup"><span data-stu-id="ee537-147">See</span></span>                                                                          |
|---------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="ee537-148">Funktionen, die vom Parser exportiert werden.</span><span class="sxs-lookup"><span data-stu-id="ee537-148">Functions that the parser DLLs export.</span></span>                        | [<span data-ttu-id="ee537-149">Export Funktionen der Parser-DLL</span><span class="sxs-lookup"><span data-stu-id="ee537-149">Parser DLL Export Functions</span></span>](parser-dll-export-functions.md)               |
| <span data-ttu-id="ee537-150">Funktionen, die Sie verwenden können, um Parser-DLLs zu entwickeln.</span><span class="sxs-lookup"><span data-stu-id="ee537-150">Functions that you can use to develop parser DLLs.</span></span>            | [<span data-ttu-id="ee537-151">Parser-Funktionen</span><span class="sxs-lookup"><span data-stu-id="ee537-151">Parser Functions</span></span>](parser-functions.md)                                     |
| <span data-ttu-id="ee537-152">Funktionen, die Sie verwenden können, um Parser-und Experten-DLLs zu entwickeln.</span><span class="sxs-lookup"><span data-stu-id="ee537-152">Functions that you can use to develop parser and expert DLLs.</span></span> | [<span data-ttu-id="ee537-153">Allgemeine Funktionen für Experten und Parser</span><span class="sxs-lookup"><span data-stu-id="ee537-153">Expert and Parser Common Functions</span></span>](expert-and-parser-common-functions.md) |



 

 

 



