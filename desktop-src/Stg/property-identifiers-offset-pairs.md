---
title: Eigenschafts Bezeichner/Offset-Paare
description: Nach der Anzahl von Eigenschaften Satz Wert für Eigenschaften ist ein Array von Eigenschafts Werten für Eigenschaften Bezeichner/Offset Paare festgelegt.
ms.assetid: 341608a1-3ab1-4fa9-ab9a-4124c63c78a7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b55ed20aef2c76dc97fcb3f4acfe981b9800308
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106339449"
---
# <a name="property-identifiersoffset-pairs"></a><span data-ttu-id="47c42-103">Eigenschafts Bezeichner/Offset-Paare</span><span class="sxs-lookup"><span data-stu-id="47c42-103">Property Identifiers/Offset Pairs</span></span>

<span data-ttu-id="47c42-104">Nach der Anzahl von Eigenschaften Satz Wert für Eigenschaften ist ein Array von Eigenschafts Werten für Eigenschaften Bezeichner/Offset Paare festgelegt.</span><span class="sxs-lookup"><span data-stu-id="47c42-104">Following the Count of Properties property set value is an array of Property Identifiers/Offset Pairs property set values.</span></span> <span data-ttu-id="47c42-105">Eigenschafts Bezeichner sind 32-Bit-Werte, die eine Eigenschaft innerhalb eines Abschnitts eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="47c42-105">Property Identifiers are 32-bit values that uniquely identify a property within a section.</span></span> <span data-ttu-id="47c42-106">Die Offset Paare geben den Abstand zwischen dem Anfang des Abschnitts und dem Anfang des Eigenschaftentyp-Wert-Paars an.</span><span class="sxs-lookup"><span data-stu-id="47c42-106">The Offset Pairs indicate the distance from the start of the section to the start of the property Type/Value Pair.</span></span> <span data-ttu-id="47c42-107">Da die Offsets relativ zum Abschnitt sind, können Abschnitte als Bytearray kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="47c42-107">Because the offsets are relative to the section, sections can be copied as an array of bytes.</span></span>

<span data-ttu-id="47c42-108">Eigenschafts Bezeichner werden nicht in einer bestimmten Reihenfolge sortiert.</span><span class="sxs-lookup"><span data-stu-id="47c42-108">Property identifiers are not sorted in any particular order.</span></span> <span data-ttu-id="47c42-109">Eigenschaften können im gespeicherten Eigenschaften Satz ausgelassen werden. die Leser dürfen sich nicht auf eine bestimmte Reihenfolge oder einen bestimmten Bereich von Eigenschafts Bezeichner verlassen.</span><span class="sxs-lookup"><span data-stu-id="47c42-109">Properties can be omitted from the stored property set; readers must not rely on a specific order or range of property identifiers.</span></span>

 

 




