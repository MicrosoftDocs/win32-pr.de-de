---
description: ICE71 überprüft, ob die Medien Tabelle einen Eintrag mit einem DiskId-Wert gleich 1 enthält.
ms.assetid: b48c2f3f-24ef-48a8-849f-7abed69c0fc9
title: ICE71
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c6e136362caa13da2b6305e3d8c3ca9c3a5c7bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960482"
---
# <a name="ice71"></a><span data-ttu-id="b3ee8-103">ICE71</span><span class="sxs-lookup"><span data-stu-id="b3ee8-103">ICE71</span></span>

<span data-ttu-id="b3ee8-104">ICE71 überprüft, ob die [Medien Tabelle](media-table.md) einen Eintrag mit einem DiskId-Wert gleich 1 enthält.</span><span class="sxs-lookup"><span data-stu-id="b3ee8-104">ICE71 verifies that the [Media table](media-table.md) contains an entry with DiskId equal to 1.</span></span> <span data-ttu-id="b3ee8-105">(Windows Installer geht davon aus, dass sich das MSI-Paket auf Datenträger 1 befindet.)</span><span class="sxs-lookup"><span data-stu-id="b3ee8-105">(Windows Installer assumes that the .msi package is on disk 1.)</span></span>

## <a name="result"></a><span data-ttu-id="b3ee8-106">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="b3ee8-106">Result</span></span>

<span data-ttu-id="b3ee8-107">ICE71 gibt einen Fehler zurück, wenn die Medien Tabelle keinen Eintrag enthält, bei dem DiskId gleich 1 ist.</span><span class="sxs-lookup"><span data-stu-id="b3ee8-107">ICE71 returns an error if the Media table does not contain an entry with DiskId equal to 1.</span></span>

## <a name="example"></a><span data-ttu-id="b3ee8-108">Beispiel</span><span class="sxs-lookup"><span data-stu-id="b3ee8-108">Example</span></span>

<span data-ttu-id="b3ee8-109">ICE71 meldet den folgenden Fehler für das gezeigte Beispiel.</span><span class="sxs-lookup"><span data-stu-id="b3ee8-109">ICE71 reports the following error for the example shown.</span></span>

``` syntax
The Media table requires an entry with DiskId=1. First DiskId is '2'.
```

<span data-ttu-id="b3ee8-110">T0 beheben Sie diesen Fehler, und ändern Sie die DiskId des Eintrags, in dem das Paket gespeichert ist, auf 1.</span><span class="sxs-lookup"><span data-stu-id="b3ee8-110">T0 fix this error, change the DiskId of the entry where the package is stored to 1.</span></span>

<span data-ttu-id="b3ee8-111">[Medien Tabelle](media-table.md) (partiell)</span><span class="sxs-lookup"><span data-stu-id="b3ee8-111">[Media Table](media-table.md) (partial)</span></span>



| <span data-ttu-id="b3ee8-112">DiskId</span><span class="sxs-lookup"><span data-stu-id="b3ee8-112">DiskId</span></span> |
|--------|
| <span data-ttu-id="b3ee8-113">2</span><span class="sxs-lookup"><span data-stu-id="b3ee8-113">2</span></span>      |



 

## <a name="related-topics"></a><span data-ttu-id="b3ee8-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b3ee8-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b3ee8-115">Ice-Referenz</span><span class="sxs-lookup"><span data-stu-id="b3ee8-115">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



