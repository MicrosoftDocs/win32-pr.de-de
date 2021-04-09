---
description: Locale \_ S1159 und locale \_ Sam
ms.assetid: dc7058af-1d5f-40a0-8d0b-17d2ff5662ce
title: LOCALE_S1159 und LOCALE_SAM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6b41f98ea5c07f1d88534c1e47acecfa81a4e62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867052"
---
# <a name="locale_s1159-and-locale_sam"></a><span data-ttu-id="b8ed6-103">Locale \_ S1159 und locale \_ Sam</span><span class="sxs-lookup"><span data-stu-id="b8ed6-103">LOCALE\_S1159 and LOCALE\_SAM</span></span>

<span data-ttu-id="b8ed6-104">Zeichenfolge für den am-Kenn Zeichner (erste 12 Stunden des Tages).</span><span class="sxs-lookup"><span data-stu-id="b8ed6-104">String for the AM designator (first 12 hours of the day).</span></span> <span data-ttu-id="b8ed6-105">Die maximale Anzahl von Zeichen, die für diese Zeichenfolge zulässig sind, einschließlich eines abschließenden NULL-Zeichens, unterscheidet sich für unterschiedliche Versionen von Windows.</span><span class="sxs-lookup"><span data-stu-id="b8ed6-105">The maximum number of characters allowed for this string, including a terminating null character, is different for different releases of Windows.</span></span>

<span data-ttu-id="b8ed6-106">**Windows XP:** 13 einschließlich eines abschließenden NULL-Zeichens für [**SetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-setlocaleinfoa).</span><span class="sxs-lookup"><span data-stu-id="b8ed6-106">**Windows XP:** Thirteen including a terminating null character for [**SetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-setlocaleinfoa).</span></span> <span data-ttu-id="b8ed6-107">15 einschließlich eines abschließenden NULL-Zeichens für [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa).</span><span class="sxs-lookup"><span data-stu-id="b8ed6-107">Fifteen including a terminating null character for [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa).</span></span>

<span data-ttu-id="b8ed6-108">**Windows Me/98/95, Windows NT 4,0, Windows 2000:** 9 einschließlich eines abschließenden NULL-Zeichens.</span><span class="sxs-lookup"><span data-stu-id="b8ed6-108">**Windows Me/98/95, Windows NT 4.0, Windows 2000:** Nine including a terminating null character.</span></span>

<span data-ttu-id="b8ed6-109">**Windows Server 2003 und höher:** 15 einschließlich eines abschließenden NULL-Zeichens.</span><span class="sxs-lookup"><span data-stu-id="b8ed6-109">**Windows Server 2003 and later:** Fifteen including a terminating null character.</span></span>

<span data-ttu-id="b8ed6-110">Windows 10 hat den Wert **locale \_ Sam** als ein besser lesbares Synonym für **locale \_ S1159** hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="b8ed6-110">Windows 10 added the value **LOCALE\_SAM** as a more readable synonym for **LOCALE\_S1159**.</span></span>

 

 



