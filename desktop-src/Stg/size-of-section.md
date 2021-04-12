---
title: Größe des Abschnitts
description: Der Abschnitts Größen Datentyp gibt die Größe des Abschnitts in Byte an.
ms.assetid: 6438fbce-42b9-4b16-a6b0-80c80246e546
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d71b19df1c2f9a65f6952855a4ab325565c759af
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104207328"
---
# <a name="size-of-section"></a><span data-ttu-id="84f2b-103">Größe des Abschnitts</span><span class="sxs-lookup"><span data-stu-id="84f2b-103">Size of Section</span></span>

<span data-ttu-id="84f2b-104">Der Abschnitts Größen Datentyp gibt die Größe des Abschnitts in Byte an.</span><span class="sxs-lookup"><span data-stu-id="84f2b-104">The section size data type indicates the size, in bytes, of the section.</span></span> <span data-ttu-id="84f2b-105">Da es sich bei der Abschnitts Größe um die ersten 4 Bytes handelt, können Abschnitte als Bytearray kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="84f2b-105">Because the section size is the first 4 bytes, sections can be copied as an array of bytes.</span></span> <span data-ttu-id="84f2b-106">Die Abschnitts Größe sollte immer ein Vielfaches von vier sein.</span><span class="sxs-lookup"><span data-stu-id="84f2b-106">The section size should always be a multiple of four.</span></span>

<span data-ttu-id="84f2b-107">Beispielsweise würde ein leerer Abschnitt, d. h. eine mit NULL-Eigenschaften darin, eine Byte Anzahl von acht (die **DWORD** -Byte Anzahl und die **DWORD** -Anzahl von Eigenschaften) enthalten.</span><span class="sxs-lookup"><span data-stu-id="84f2b-107">For example, an empty section, that is, one with zero properties in it, would have a byte count of eight (the **DWORD** byte count and the **DWORD** count of properties).</span></span> <span data-ttu-id="84f2b-108">Der-Abschnitt enthält die 8 Bytes: **08 00 00 00 00 00 00 00**.</span><span class="sxs-lookup"><span data-stu-id="84f2b-108">The section itself would contain the 8 bytes: **08 00 00 00 00 00 00 00**.</span></span>

 

 




