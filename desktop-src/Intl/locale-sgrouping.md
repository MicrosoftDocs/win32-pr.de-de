---
description: Gebiets Schema- \_ sgruppierung
ms.assetid: 3f07ecae-38f4-477b-8b23-a9cd87613c24
title: LOCALE_SGROUPING
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db7242f7d515ce17872376b9a067a7b41831a331
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103961007"
---
# <a name="locale_sgrouping"></a><span data-ttu-id="b7895-103">Gebiets Schema- \_ sgruppierung</span><span class="sxs-lookup"><span data-stu-id="b7895-103">LOCALE\_SGROUPING</span></span>

<span data-ttu-id="b7895-104">Größen für jede Gruppe von Ziffern auf der linken Seite des Dezimal Trennzeichens.</span><span class="sxs-lookup"><span data-stu-id="b7895-104">Sizes for each group of digits to the left of the decimal.</span></span> <span data-ttu-id="b7895-105">Die maximale Anzahl von Zeichen, die für diese Zeichenfolge zulässig ist, ist zehn, einschließlich eines abschließenden NULL-Zeichens.</span><span class="sxs-lookup"><span data-stu-id="b7895-105">The maximum number of characters allowed for this string is ten, including a terminating null character.</span></span> <span data-ttu-id="b7895-106">Für jede Gruppe ist eine explizite Größe erforderlich, und die Größen werden durch Semikolons getrennt.</span><span class="sxs-lookup"><span data-stu-id="b7895-106">An explicit size is needed for each group, and sizes are separated by semicolons.</span></span> <span data-ttu-id="b7895-107">Wenn der letzte Wert 0 ist, wird der vorangehende Wert wiederholt.</span><span class="sxs-lookup"><span data-stu-id="b7895-107">If the last value is 0, the preceding value is repeated.</span></span> <span data-ttu-id="b7895-108">Wenn Sie z. b. Tausende gruppieren möchten, geben Sie 3; 0 an.</span><span class="sxs-lookup"><span data-stu-id="b7895-108">For example, to group thousands, specify 3;0.</span></span> <span data-ttu-id="b7895-109">Indic-Gebiets Schemas gruppieren die ersten Tausender und Gruppieren dann nach Hunderten.</span><span class="sxs-lookup"><span data-stu-id="b7895-109">Indic locales group the first thousand and then group by hundreds.</span></span> <span data-ttu-id="b7895-110">Beispielsweise wird der Wert 12, 34, 56789 durch 3; 2; 0 dargestellt.</span><span class="sxs-lookup"><span data-stu-id="b7895-110">For example, 12,34,56,789 is represented by 3;2;0.</span></span>

<span data-ttu-id="b7895-111">Weitere Beispiele:</span><span class="sxs-lookup"><span data-stu-id="b7895-111">Further examples:</span></span>



| <span data-ttu-id="b7895-112">Spezifikation</span><span class="sxs-lookup"><span data-stu-id="b7895-112">Specification</span></span> | <span data-ttu-id="b7895-113">Resultierende Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="b7895-113">Resulting string</span></span>   |
|---------------|--------------------|
| <span data-ttu-id="b7895-114">3; 0</span><span class="sxs-lookup"><span data-stu-id="b7895-114">3;0</span></span>           | <span data-ttu-id="b7895-115">3 Billionen</span><span class="sxs-lookup"><span data-stu-id="b7895-115">3,000,000,000,000</span></span>  |
| <span data-ttu-id="b7895-116">3; 2; 0</span><span class="sxs-lookup"><span data-stu-id="b7895-116">3;2;0</span></span>         | <span data-ttu-id="b7895-117">30, 00, 00, 00, 00000</span><span class="sxs-lookup"><span data-stu-id="b7895-117">30,00,00,00,00,000</span></span> |
| <span data-ttu-id="b7895-118">3</span><span class="sxs-lookup"><span data-stu-id="b7895-118">3</span></span>             | <span data-ttu-id="b7895-119">3 Billionen</span><span class="sxs-lookup"><span data-stu-id="b7895-119">3000000000,000</span></span>     |
| <span data-ttu-id="b7895-120">3; 2</span><span class="sxs-lookup"><span data-stu-id="b7895-120">3;2</span></span>           | <span data-ttu-id="b7895-121">30000000, 00000</span><span class="sxs-lookup"><span data-stu-id="b7895-121">30000000,00,000</span></span>    |



 

 

 



