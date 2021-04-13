---
title: Private Online Stores
description: Private Online Stores
ms.assetid: c1e241f5-6d29-4b53-8be0-264597e03de7
keywords:
- Windows Media Player Online Stores, privat
- Online Stores, privat
- Typ 1 Online Stores, privat
- Typ 2 Online Stores, privat
- Private Online Stores
- Registrierung, private Online Stores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e11490a8a12659dfc1e2c5445167e8d71abaf00
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388496"
---
# <a name="private-online-stores"></a><span data-ttu-id="3fb53-109">Private Online Stores</span><span class="sxs-lookup"><span data-stu-id="3fb53-109">Private Online Stores</span></span>

<span data-ttu-id="3fb53-110">Windows Media Player 10 oder höher unterstützt private Online Stores. Das heißt, Stores, die nur für bestimmte Benutzer sichtbar sind.</span><span class="sxs-lookup"><span data-stu-id="3fb53-110">Windows Media Player 10 or later supports private online stores; that is, stores that are visible only to certain users.</span></span> <span data-ttu-id="3fb53-111">Damit ein privater Onlinespeicher für den aktuellen Benutzer sichtbar ist, muss ein Eintrag vorhanden sein, der den privaten Online Store unter dem folgenden Registrierungsschlüssel darstellt.</span><span class="sxs-lookup"><span data-stu-id="3fb53-111">For a private online store to be visible to the current user, there must be an entry that represents the private online store under the following registry key.</span></span>

<span data-ttu-id="3fb53-112">HKEY \_ Current \_ User \\ Software \\ Microsoft \\ Media Player \\ privateservices</span><span class="sxs-lookup"><span data-stu-id="3fb53-112">HKEY\_CURRENT\_USER\\Software\\Microsoft\\MediaPlayer\\PrivateServices</span></span>

<span data-ttu-id="3fb53-113">Der erforderliche Registrierungs Eintrag muss das folgende Format aufweisen:</span><span class="sxs-lookup"><span data-stu-id="3fb53-113">The required registry entry must have the following format.</span></span>



| <span data-ttu-id="3fb53-114">Name</span><span class="sxs-lookup"><span data-stu-id="3fb53-114">Name</span></span>                                                         | <span data-ttu-id="3fb53-115">type</span><span class="sxs-lookup"><span data-stu-id="3fb53-115">Type</span></span>           | <span data-ttu-id="3fb53-116">Wert</span><span class="sxs-lookup"><span data-stu-id="3fb53-116">Value</span></span>                                                                     |
|--------------------------------------------------------------|----------------|---------------------------------------------------------------------------|
| <span data-ttu-id="3fb53-117">Alle Namen, die von der Person ausgewählt werden, die den Registrierungs Eintrag erstellt</span><span class="sxs-lookup"><span data-stu-id="3fb53-117">Any name chosen by the person who creates the registry entry</span></span> | <span data-ttu-id="3fb53-118">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="3fb53-118">**REG\_DWORD**</span></span> | <span data-ttu-id="3fb53-119">Eine von Microsoft bereitgestellte Zahl, die den privaten Onlinespeicher identifiziert.</span><span class="sxs-lookup"><span data-stu-id="3fb53-119">A number, provided by Microsoft, that identifies the private online store</span></span> |



 

<span data-ttu-id="3fb53-120">Das Windows Media Player 10-ActiveX-Steuerelement unterstützt private Online Stores nur, wenn das Steuerelement im Remote Modus ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3fb53-120">The Windows Media Player 10 ActiveX control supports private online stores only if the control is running in remote mode.</span></span> <span data-ttu-id="3fb53-121">Das ActiveX-Steuerelement von Windows Media Player 11 unterstützt private Onlinespeicher, unabhängig davon, ob das Steuerelement im Remote Modus ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3fb53-121">The Windows Media Player 11 ActiveX control supports private online stores regardless of whether the control is running in remote mode.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3fb53-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3fb53-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3fb53-123">**Informationen, die von Typ 1 und Typ 2 Online Stores gemeinsam sind**</span><span class="sxs-lookup"><span data-stu-id="3fb53-123">**Information Common to Type 1 and Type 2 Online Stores**</span></span>](information-common-to-type-1-and-type-2-online-stores.md)
</dt> </dl>

 

 




