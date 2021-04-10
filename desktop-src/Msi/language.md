---
description: Der sprach Datentyp ist eine Text Zeichenfolge, die mindestens eine gültige numerische Sprach-ID enthält. Wenn zwei oder mehr Sprach-IDs vorhanden sind, müssen diese durch Kommas getrennt werden.
ms.assetid: 547fc662-f055-421e-a621-eecdfa0b13f6
title: Sprache
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc87cb8b88dc3a693eee6890276adb67ad359e7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214630"
---
# <a name="language"></a><span data-ttu-id="43163-104">Sprache</span><span class="sxs-lookup"><span data-stu-id="43163-104">Language</span></span>

<span data-ttu-id="43163-105">Der sprach Datentyp ist eine Text Zeichenfolge, die mindestens eine gültige numerische Sprach-ID enthält.</span><span class="sxs-lookup"><span data-stu-id="43163-105">The Language data type is a text string containing one or more valid numeric language IDs.</span></span> <span data-ttu-id="43163-106">Wenn zwei oder mehr Sprach-IDs vorhanden sind, müssen diese durch Kommas getrennt werden.</span><span class="sxs-lookup"><span data-stu-id="43163-106">If there are two or more language IDs, they must be separated by commas.</span></span>

<span data-ttu-id="43163-107">Der sprach Datentyp ist ein 16-Bit-Wert, bei dem es sich um die Kombination aus einer primären und einer unter Sprachen numerischen ID handelt.</span><span class="sxs-lookup"><span data-stu-id="43163-107">The Language data type is a 16-bit value that is the combination of a primary and sublanguage numeric IDs.</span></span> <span data-ttu-id="43163-108">Die primäre langid besteht aus den Bits 0 bis 9, während die unter Sprachen-ID Bits 10 bis 15 ist.</span><span class="sxs-lookup"><span data-stu-id="43163-108">The Primary LANGID comprises bits 0 through 9 while the subLanguage ID is bits 10 through 15.</span></span> <span data-ttu-id="43163-109">Eine Liste der numerischen und numerischen IDs von Primär-und unter Sprachen finden Sie im Thema [sprach Bezeichner-Konstanten und-](../intl/language-identifier-constants-and-strings.md) Zeichen folgen.</span><span class="sxs-lookup"><span data-stu-id="43163-109">For a list of primary and sub language numeric identifiers, see the [Language Identifier Constants and Strings](../intl/language-identifier-constants-and-strings.md) topic.</span></span>

<span data-ttu-id="43163-110">Bei primären Sprach-IDs kann der Bereich von 0x200 bis 0x3ff vom Benutzer definiert werden.</span><span class="sxs-lookup"><span data-stu-id="43163-110">For primary language IDs, the range 0x200 to 0x3ff is user definable.</span></span> <span data-ttu-id="43163-111">Der Bereich 0x000 bis 0x1FF ist für die Verwendung durch das System reserviert.</span><span class="sxs-lookup"><span data-stu-id="43163-111">The range 0x000 to 0x1ff is reserved for system use.</span></span> <span data-ttu-id="43163-112">Bei unter Sprachen-IDs ist der Bereich 0x20 bis 0x3f benutzerdefinierbar.</span><span class="sxs-lookup"><span data-stu-id="43163-112">For sublanguage IDs, the range 0x20 to 0x3f is user definable.</span></span> <span data-ttu-id="43163-113">Der Bereich 0x00 bis 0x1F ist für die Verwendung durch das System reserviert.</span><span class="sxs-lookup"><span data-stu-id="43163-113">The range 0x00 to 0x1f is reserved for system use.</span></span>

 

 
