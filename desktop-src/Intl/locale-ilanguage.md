---
description: Gebiets Schema- \_ iLanguage
ms.assetid: 8f80a941-8ba6-4a0d-92fa-77230fe0a9d1
title: LOCALE_ILANGUAGE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2b68ccd270319fa00cd2e983b5f9159d454f160
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346266"
---
# <a name="locale_ilanguage"></a><span data-ttu-id="f4f17-103">Gebiets Schema- \_ iLanguage</span><span class="sxs-lookup"><span data-stu-id="f4f17-103">LOCALE\_ILANGUAGE</span></span>

<span data-ttu-id="f4f17-104">Der [Sprachen Bezeichner](language-identifiers.md) mit einem hexadezimalen Wert.</span><span class="sxs-lookup"><span data-stu-id="f4f17-104">[Language identifier](language-identifiers.md) with a hexadecimal value.</span></span> <span data-ttu-id="f4f17-105">Beispielsweise hat Englisch (USA) den Wert 0409, der 0x0409 hexadezimal angibt und 1033 Decimal entspricht.</span><span class="sxs-lookup"><span data-stu-id="f4f17-105">For example, English (United States) has the value 0409, which indicates 0x0409 hexadecimal, and is equivalent to 1033 decimal.</span></span> <span data-ttu-id="f4f17-106">Die maximal zulässige Anzahl von Zeichen für diese Zeichenfolge ist fünf, einschließlich eines abschließenden NULL-Zeichens.</span><span class="sxs-lookup"><span data-stu-id="f4f17-106">The maximum number of characters allowed for this string is five, including a terminating null character.</span></span>

<span data-ttu-id="f4f17-107">**Windows Vista und höher:** Die Verwendung dieser Konstante kann bewirken, dass [**getlocaleingefo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) einen ungültigen Gebiets Schema Bezeichner zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="f4f17-107">**Windows Vista and later:** Use of this constant can cause [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) to return an invalid locale identifier.</span></span> <span data-ttu-id="f4f17-108">Die Anwendung sollte beim Aufrufen dieser Funktion die [ \_ sname](locale-sname.md) -Konstante für das Gebiets Schema verwenden.</span><span class="sxs-lookup"><span data-stu-id="f4f17-108">Your application should use the [LOCALE\_SNAME](locale-sname.md) constant when calling this function.</span></span>

 

 



