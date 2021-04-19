---
description: Die von TSPI verwendeten Datenstrukturen sind identisch mit denen, die in TAPI-Strukturen definiert sind, mit Ausnahme von "tuispikreatedialoginstancepara".
ms.assetid: 99d966ea-49b5-4a84-83a1-99dc8465c751
title: TSPI-Strukturen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e3468171bc160ca03ac9f5501a9eba7fd9221ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348600"
---
# <a name="tspi-structures"></a><span data-ttu-id="db8cb-103">TSPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="db8cb-103">TSPI Structures</span></span>

<span data-ttu-id="db8cb-104">Die von TSPI verwendeten Datenstrukturen sind identisch mit denen, die in [TAPI-Strukturen](./tapi-structures.md)definiert sind, mit Ausnahme von " [**tuispikreatedialoginstancepara**](/windows/win32/api/tspi/ns-tspi-tuispicreatedialoginstanceparams)".</span><span class="sxs-lookup"><span data-stu-id="db8cb-104">The data structures TSPI uses are identical to those defined in [TAPI Structures](./tapi-structures.md), with the exception of [**TUISPICREATEDIALOGINSTANCEPARAMS**](/windows/win32/api/tspi/ns-tspi-tuispicreatedialoginstanceparams).</span></span>

<span data-ttu-id="db8cb-105">Bei den meisten größeren Datenstrukturen ist die Verantwortung für das Ausfüllen von Membern zwischen dem Dienstanbieter und TAPI aufgeteilt.</span><span class="sxs-lookup"><span data-stu-id="db8cb-105">In the case of most of the larger data structures, the responsibility for filling in members is divided between the service provider and TAPI.</span></span> <span data-ttu-id="db8cb-106">Der Dienstanbieter muss die Werte, die in Membern von TAPI vorhanden sind, beibehalten.</span><span class="sxs-lookup"><span data-stu-id="db8cb-106">The service provider must preserve the values present in members owned by TAPI.</span></span> <span data-ttu-id="db8cb-107">Die Beschreibung, welche Member vom Dienstanbieter festgelegt werden müssen und welche beibehalten werden muss, wird im Abschnitt Functions in den Funktionen bereitgestellt, die auf diese Datenstruktur verweisen.</span><span class="sxs-lookup"><span data-stu-id="db8cb-107">The description of which members must be set by the service provider and which must be preserved is provided in the Functions section in the functions that refer to that data structure.</span></span>

<span data-ttu-id="db8cb-108">Der Abschnitt Reference listet für jede Struktur die folgenden Elemente auf:</span><span class="sxs-lookup"><span data-stu-id="db8cb-108">For each structure, the reference section lists the following items:</span></span>

-   <span data-ttu-id="db8cb-109">Der Zweck der Struktur</span><span class="sxs-lookup"><span data-stu-id="db8cb-109">The purpose of the structure</span></span>
-   <span data-ttu-id="db8cb-110">Eine Beschreibung der Werte oder Felder.</span><span class="sxs-lookup"><span data-stu-id="db8cb-110">A description of the values or fields</span></span>
-   <span data-ttu-id="db8cb-111">Eine Beschreibung der Erweiterbarkeit der Struktur.</span><span class="sxs-lookup"><span data-stu-id="db8cb-111">A description of the structure's extensibility</span></span>
-   <span data-ttu-id="db8cb-112">Optionale Kommentare zur Verwendung der Struktur</span><span class="sxs-lookup"><span data-stu-id="db8cb-112">Optional comments about using the structure</span></span>
-   <span data-ttu-id="db8cb-113">Optionale Verweise auf andere Funktionen, Nachrichten, Konstanten oder Strukturen.</span><span class="sxs-lookup"><span data-stu-id="db8cb-113">Optional references to other functions, messages, constants, or structures.</span></span>

<span data-ttu-id="db8cb-114">Der Arbeitsspeicher für alle Datenstrukturen, deren Darstellung sowohl von TAPI als auch vom Dienstanbieter veröffentlicht und freigegeben wird, wird von TAPI oder einer Anwendung mithilfe von TAPI zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="db8cb-114">Memory for all data structures whose representation is published and shared by both TAPI and the service provider is allocated by TAPI or an application using TAPI.</span></span> <span data-ttu-id="db8cb-115">TAPI übergibt einen Zeiger an die TSPI-Funktion, die die Informationen zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="db8cb-115">TAPI passes a pointer to the TSPI function that returns the information.</span></span> <span data-ttu-id="db8cb-116">TSPI füllt die Datenstruktur mit den angeforderten Informationen.</span><span class="sxs-lookup"><span data-stu-id="db8cb-116">TSPI fills the data structure with the requested information.</span></span> <span data-ttu-id="db8cb-117">Wenn der Vorgang asynchron ist, sind die Informationen erst verfügbar, wenn der asynchrone Antwort Rückruf einen Erfolg angibt.</span><span class="sxs-lookup"><span data-stu-id="db8cb-117">If the operation is asynchronous, the information is not available until the asynchronous reply callback indicates success.</span></span>

> [!Note]  
> <span data-ttu-id="db8cb-118">Einige Strukturen enthalten Größen-und Offset Felder zum Definieren der Position und Länge von Zeichen folgen im Variablen Teil der Struktur.</span><span class="sxs-lookup"><span data-stu-id="db8cb-118">Some structures include Size and Offset fields for defining the location and length of strings in the variable portion of the structure.</span></span> <span data-ttu-id="db8cb-119">Wenn der Dienstanbieter aufgefordert wird, eine Zeichenfolge hinzuzufügen, aber keine Zeichenfolge verfügbar ist, muss der Dienstanbieter diese Bedingung auf eine der folgenden Weisen angeben:</span><span class="sxs-lookup"><span data-stu-id="db8cb-119">If the service provider is requested to add a string but no string is available, the service provider must indicate this condition in one of these ways:</span></span>
>
> -   <span data-ttu-id="db8cb-120">Legen Sie die Felder Größe und Offset auf 0 fest.</span><span class="sxs-lookup"><span data-stu-id="db8cb-120">Set both the Size and Offset fields to 0.</span></span>
> -   <span data-ttu-id="db8cb-121">Legen Sie für das Offset-Feld einen Wert ungleich 0 (null) fest.</span><span class="sxs-lookup"><span data-stu-id="db8cb-121">Set the Offset field to nonzero but Size to 0.</span></span>
> -   <span data-ttu-id="db8cb-122">Legen Sie für das Offset-Feld den Wert ungleich 0 (null), für Größe 1 und für das Byte am Offset den Wert 0 fest.</span><span class="sxs-lookup"><span data-stu-id="db8cb-122">Set the Offset field to nonzero, Size to 1, and the byte at the Offset to 0.</span></span>

 

 

 
