---
title: partial_ignore-Attribut
description: Das ACF-Attribut \ partielle \_ Ignore \ definiert eine spezialisierte Version von \ Unique \-Zeigern, die eine optionale Semantik bereitstellt.
ms.assetid: 8a8f88b0-4a12-496d-bf77-ee57241b577b
keywords:
- partial_ignore Attribut-Mittel l
topic_type:
- apiref
api_name:
- partial_ignore
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82d133275ca77032341d160b51b95b20235c8f2a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104389280"
---
# <a name="partial_ignore-attribute"></a><span data-ttu-id="7475c-104">partielles \_ Ignore-Attribut</span><span class="sxs-lookup"><span data-stu-id="7475c-104">partial\_ignore attribute</span></span>

<span data-ttu-id="7475c-105">Das ACF-Attribut **\[ partielle \_ Ignore \]** definiert eine **\[ \]** spezialisierte Version eindeutiger Zeiger, die eine optionale Semantik bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="7475c-105">The ACF attribute **\[partial\_ignore\]** defines a specialized version of **\[unique\]** pointers that provides optional-out semantics.</span></span>

``` syntax
[ [function-attribute-list <>] ] type-specifier <> [pointer- <>declarator <>] function-name <>( [ partial_ignore [ , parameter-attribute-list <> ] ] type-specifier <> [declarator <>] , ...);
```

## <a name="remarks"></a><span data-ttu-id="7475c-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7475c-106">Remarks</span></span>

<span data-ttu-id="7475c-107">Beim Erstellen einer Funktion ist es üblich, Benutzern das Angeben eines nicht-**null** -Zeigers auf optionale Rückgabe Daten zu ermöglichen. Dies wird häufig als optionaler-out-Zeiger bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="7475c-107">When creating a function, it is common to allow users to specify a non-**NULL** pointer to optional return data, often referred to as an optional-out pointer.</span></span> <span data-ttu-id="7475c-108">Der Speicher, auf den der Benutzer zeigt, muss in der Regel nicht initialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="7475c-108">The memory pointed to by the user is not typically required to be initialized.</span></span> <span data-ttu-id="7475c-109">Diese Technik stellt ein Problem dar, wenn die Funktion über RPC verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7475c-109">This technique represents a problem when the function is used over RPC.</span></span>

<span data-ttu-id="7475c-110">Wenn der optionale-out-Zeiger gültig ist, aber auf nicht initialisierte Daten zeigt, versucht RPC, diese Daten zu Mars Hallen und an den Server zu senden, was dazu führen kann, dass das Marshalling fehlschlägt und den Aufruf abbricht.</span><span class="sxs-lookup"><span data-stu-id="7475c-110">If the optional-out pointer is valid, but points to uninitialized data, RPC attempts to marshal that data and send it to the server, which can cause the marshaling to fail and abort the call.</span></span> <span data-ttu-id="7475c-111">Auch wenn das Marshalling erfolgreich ist, wird eine potenziell große Menge an nutzlosen Daten an den Server gesendet.</span><span class="sxs-lookup"><span data-stu-id="7475c-111">Even if the marshaling succeeds, a potentially large amount of useless data is sent to the server.</span></span>

<span data-ttu-id="7475c-112">Diese Probleme werden gelöst, indem der Zeiger als **\[ in, out, Unique, partiell \_ Ignore \]** gekennzeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="7475c-112">These problems are solved by marking the pointer as **\[in, out, unique, partial\_ignore\]**.</span></span> <span data-ttu-id="7475c-113">Alle vier Attribute müssen vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="7475c-113">All four attributes must be present.</span></span> <span data-ttu-id="7475c-114">Wenn ein **\[ partieller \_ Ignore \]** -Zeiger auf der Clientseite gemarshallt wird, ist ein Indikator, der anzeigt, ob der Zeiger **null** ist.</span><span class="sxs-lookup"><span data-stu-id="7475c-114">When a **\[partial\_ignore\]** pointer is marshaled on the client side, the only data sent to the server is an indicator showing whether the pointer is **NULL**.</span></span> <span data-ttu-id="7475c-115">Wenn der Zeiger nicht **null** ist, empfängt die serverseitige Routine einen gültigen Zeiger auf einen Speicherblock, der mit Nullen initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="7475c-115">If the pointer is non-**NULL**, the server-side routine receives a valid pointer to a block of memory that has been initialized with zeros.</span></span> <span data-ttu-id="7475c-116">Wenn der Zeiger **null** ist, empfängt die serverseitige Routine einen **null** -Zeiger.</span><span class="sxs-lookup"><span data-stu-id="7475c-116">If the pointer is **NULL**, the server-side routine receives a **NULL** pointer.</span></span>

<span data-ttu-id="7475c-117">In dieser Situation muss die maximale Größe des Zeigers entweder zum Zeitpunkt der Kompilierung oder basierend auf den Eingabe Parametern festgelegt werden, da der Server Speicherplatz für den Speicherbereich zuweisen muss, auf den verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="7475c-117">In this situation, the maximum size of the pointer must be well defined either at compile time or based on input parameters, because the server needs to allocate space for the memory location being pointed to.</span></span> <span data-ttu-id="7475c-118">Ein einfacher **\[ Zeichen \]** folgen Zeiger hat z. b. keine klar definierte Größe, da die Zeichenfolge implizit mit einem NULL-Zeichen beendet wird.</span><span class="sxs-lookup"><span data-stu-id="7475c-118">For example, a simple **\[string\]** pointer does not have a well defined size because the string is implicitly terminated by a NULL character.</span></span> <span data-ttu-id="7475c-119">Wenn in diesem Fall die maximale Größe der Zeichenfolge durch Hinzufügen eines **\[ size \_ is \]** -Attributs angegeben wird, wird die genau definierte Größen Anforderung erreicht.</span><span class="sxs-lookup"><span data-stu-id="7475c-119">In this case, specifying the maximum size of the string by adding a **\[size\_is\]** attribute would achieve the well defined size requirement.</span></span>

## <a name="examples"></a><span data-ttu-id="7475c-120">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7475c-120">Examples</span></span>

``` syntax
/* The MoveLeft function will move one position to the left and optionally return the previous position */
void MoveLeft([in, out, unique, partial_ignore] long *pPrevPosition);
```

## <a name="see-also"></a><span data-ttu-id="7475c-121">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="7475c-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7475c-122">**gem**</span><span class="sxs-lookup"><span data-stu-id="7475c-122">**unique**</span></span>](unique.md)
</dt> </dl>

 

 




