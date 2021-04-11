---
description: Der reservierte Spaltenname \_ RowState stellt den nicht persistenten Zustand dar, der jeder Tabellenzeile in einer Installer-Datenbanktabelle zugeordnet ist.
ms.assetid: ff570b47-7c16-47ae-b1c2-2ecad9266372
title: _RowState Spalte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e61a2964d7d11c1c2429ad95e9de2b8bdb148954
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104042162"
---
# <a name="_rowstate-column"></a><span data-ttu-id="9f28c-103">\_RowState-Spalte</span><span class="sxs-lookup"><span data-stu-id="9f28c-103">\_RowState Column</span></span>

<span data-ttu-id="9f28c-104">Der reservierte Spaltenname \_ RowState stellt den nicht persistenten Zustand dar, der jeder Tabellenzeile in einer Installer-Datenbanktabelle zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="9f28c-104">The reserved column name \_RowState represents the non-persistent state associated with each table row in an installer database table.</span></span> <span data-ttu-id="9f28c-105">Die Pseudo Spalte hat den Typ " [Integer](integer.md)", und der Wert besteht aus einem Satz von Bitflags.</span><span class="sxs-lookup"><span data-stu-id="9f28c-105">The pseudo-column is of type [Integer](integer.md), and the value consists of a set of bit flags.</span></span> <span data-ttu-id="9f28c-106">Alle Bits sind lesbar, aber nur die Benutzerinformationen und temporären Bits können festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="9f28c-106">All the bits are readable, but only the UserInfo and Temporary bits can be set.</span></span> <span data-ttu-id="9f28c-107">Diese Daten sind nur verfügbar, solange die Tabellen gesperrt sind oder verwendet werden (d. h., während eine Sicht vorhanden ist, die die Tabellen enthält).</span><span class="sxs-lookup"><span data-stu-id="9f28c-107">This data is available only as long as the tables are locked or in use (that is, while a view containing the tables exists).</span></span> <span data-ttu-id="9f28c-108">In der folgenden Tabelle sind die Attribute aufgeführt, die eine Zeile aufweisen kann.</span><span class="sxs-lookup"><span data-stu-id="9f28c-108">The following table shows the attributes a row can have.</span></span>



| <span data-ttu-id="9f28c-109">Name</span><span class="sxs-lookup"><span data-stu-id="9f28c-109">Name</span></span>           | <span data-ttu-id="9f28c-110">Wert</span><span class="sxs-lookup"><span data-stu-id="9f28c-110">Value</span></span> | <span data-ttu-id="9f28c-111">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="9f28c-111">Meaning</span></span>                                                        |
|----------------|-------|----------------------------------------------------------------|
| <span data-ttu-id="9f28c-112">"iriererinfo"</span><span class="sxs-lookup"><span data-stu-id="9f28c-112">iraUserInfo</span></span>    | <span data-ttu-id="9f28c-113">0x01</span><span class="sxs-lookup"><span data-stu-id="9f28c-113">0x01</span></span>  | <span data-ttu-id="9f28c-114">Das-Attribut ist für die externe Verwendung vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="9f28c-114">The attribute is for external use.</span></span> <span data-ttu-id="9f28c-115">Dieser Wert kann aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="9f28c-115">This value can be updated.</span></span>  |
| <span data-ttu-id="9f28c-116">"unatemporary"</span><span class="sxs-lookup"><span data-stu-id="9f28c-116">iraTemporary</span></span>   | <span data-ttu-id="9f28c-117">0x02</span><span class="sxs-lookup"><span data-stu-id="9f28c-117">0x02</span></span>  | <span data-ttu-id="9f28c-118">Die Zeile ist nicht persistent.</span><span class="sxs-lookup"><span data-stu-id="9f28c-118">The row is not persistent.</span></span> <span data-ttu-id="9f28c-119">Dieser Wert kann aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="9f28c-119">This value can be updated.</span></span>          |
| <span data-ttu-id="9f28c-120">iramodified</span><span class="sxs-lookup"><span data-stu-id="9f28c-120">iraModified</span></span>    | <span data-ttu-id="9f28c-121">0x04</span><span class="sxs-lookup"><span data-stu-id="9f28c-121">0x04</span></span>  | <span data-ttu-id="9f28c-122">Eine Zeile wurde aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="9f28c-122">A row has been updated.</span></span>                                        |
| <span data-ttu-id="9f28c-123">iraeingefügt</span><span class="sxs-lookup"><span data-stu-id="9f28c-123">iraInserted</span></span>    | <span data-ttu-id="9f28c-124">0x08</span><span class="sxs-lookup"><span data-stu-id="9f28c-124">0x08</span></span>  | <span data-ttu-id="9f28c-125">Es wurde eine Zeile eingefügt.</span><span class="sxs-lookup"><span data-stu-id="9f28c-125">A row has been inserted.</span></span>                                       |
| <span data-ttu-id="9f28c-126">iramergefailed</span><span class="sxs-lookup"><span data-stu-id="9f28c-126">iraMergeFailed</span></span> | <span data-ttu-id="9f28c-127">0x0f</span><span class="sxs-lookup"><span data-stu-id="9f28c-127">0x0F</span></span>  | <span data-ttu-id="9f28c-128">Es wurde versucht, eine Zusammenführung mit nicht identischen, nicht Schlüsseldaten durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="9f28c-128">An attempt was made to merge with non-identical, non-key data.</span></span> |



 

<span data-ttu-id="9f28c-129">Bits 6 bis 8 sind reserviert.</span><span class="sxs-lookup"><span data-stu-id="9f28c-129">Bits 6 through 8 are reserved.</span></span>

 

 



