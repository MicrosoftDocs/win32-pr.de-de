---
description: ICE04 überprüft, ob die Sequenznummer jeder Datei in der Dateitabelle kleiner oder gleich der größten Sequenznummer in der LastSequence-Spalte der Medien Tabelle ist.
ms.assetid: ecde1389-50ea-479e-bbc1-a36ce3aceccd
title: ICE04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4da25a23a26f8a2c49e224ad334791a6081b697b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960045"
---
# <a name="ice04"></a><span data-ttu-id="6ca41-103">ICE04</span><span class="sxs-lookup"><span data-stu-id="6ca41-103">ICE04</span></span>

<span data-ttu-id="6ca41-104">ICE04 überprüft, ob die Sequenznummer jeder Datei in der [Dateitabelle](file-table.md) kleiner oder gleich der größten Sequenznummer in der LastSequence-Spalte der [Medien Tabelle](media-table.md)ist.</span><span class="sxs-lookup"><span data-stu-id="6ca41-104">ICE04 validates that the sequence number of every file in the [File table](file-table.md) is less than or equal to the largest sequence number in the LastSequence column of the [Media table](media-table.md).</span></span>

<span data-ttu-id="6ca41-105">Jeder Datensatz in der Medien Tabelle stellt einen Datenträger auf dem Quell Medium dar, der alle Dateien mit einer Sequenznummer enthält, die kleiner oder gleich dem Wert in der Spalte LastSequence ist, und größer als der LastSequence-Wert im Datensatz des vorangehenden Datenträgers.</span><span class="sxs-lookup"><span data-stu-id="6ca41-105">Each record in the Media table represents a disk on the source media containing all the files with a sequence number less than or equal to the value in the LastSequence column and greater than the LastSequence value in the record of the preceding disk.</span></span>

## <a name="result"></a><span data-ttu-id="6ca41-106">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="6ca41-106">Result</span></span>

<span data-ttu-id="6ca41-107">ICE04 gibt eine Fehlermeldung aus, wenn eine Datei mit einer Sequenznummer größer als die größte Last Sequenznummer für das Quell Medium ist.</span><span class="sxs-lookup"><span data-stu-id="6ca41-107">ICE04 posts an error message if there is a file with a sequence number greater than the largest LastSequence number for the source media.</span></span>

## <a name="example"></a><span data-ttu-id="6ca41-108">Beispiel</span><span class="sxs-lookup"><span data-stu-id="6ca41-108">Example</span></span>

<span data-ttu-id="6ca41-109">ICE04 würde den folgenden Fehler für das gezeigte Beispiel melden:</span><span class="sxs-lookup"><span data-stu-id="6ca41-109">ICE04 would report the following error for the example shown:</span></span>

``` syntax
File: MyFile, Sequence: 210 Greater Than Max Allowed by Media Table.
```

<span data-ttu-id="6ca41-110">[Dateitabelle](file-table.md) (partiell)</span><span class="sxs-lookup"><span data-stu-id="6ca41-110">[File Table](file-table.md) (partial)</span></span>



| <span data-ttu-id="6ca41-111">File</span><span class="sxs-lookup"><span data-stu-id="6ca41-111">File</span></span>   | <span data-ttu-id="6ca41-112">Sequenz</span><span class="sxs-lookup"><span data-stu-id="6ca41-112">Sequence</span></span> |
|--------|----------|
| <span data-ttu-id="6ca41-113">MyFile</span><span class="sxs-lookup"><span data-stu-id="6ca41-113">MyFile</span></span> | <span data-ttu-id="6ca41-114">210</span><span class="sxs-lookup"><span data-stu-id="6ca41-114">210</span></span>      |



 

<span data-ttu-id="6ca41-115">[Medien Tabelle](media-table.md) (partiell)</span><span class="sxs-lookup"><span data-stu-id="6ca41-115">[Media Table](media-table.md) (partial)</span></span>



| <span data-ttu-id="6ca41-116">DiskId</span><span class="sxs-lookup"><span data-stu-id="6ca41-116">DiskId</span></span> | <span data-ttu-id="6ca41-117">LastSequence</span><span class="sxs-lookup"><span data-stu-id="6ca41-117">LastSequence</span></span> |
|--------|--------------|
| <span data-ttu-id="6ca41-118">1</span><span class="sxs-lookup"><span data-stu-id="6ca41-118">1</span></span>      | <span data-ttu-id="6ca41-119">100</span><span class="sxs-lookup"><span data-stu-id="6ca41-119">100</span></span>          |



 

## <a name="related-topics"></a><span data-ttu-id="6ca41-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6ca41-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6ca41-121">Ice-Referenz</span><span class="sxs-lookup"><span data-stu-id="6ca41-121">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



