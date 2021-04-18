---
description: LOCALE \_ sshortdate
ms.assetid: 55333a53-1205-42eb-aa1a-c248c52a8a3f
title: LOCALE_SSHORTDATE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d15077b4466fd74c02dd53bd7324aceba9233cc3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106354552"
---
# <a name="locale_sshortdate"></a><span data-ttu-id="f15d1-103">LOCALE \_ sshortdate</span><span class="sxs-lookup"><span data-stu-id="f15d1-103">LOCALE\_SSHORTDATE</span></span>

<span data-ttu-id="f15d1-104">Kurze Datums Formatierungs Zeichenfolge für das Gebiets Schema.</span><span class="sxs-lookup"><span data-stu-id="f15d1-104">Short date formatting string for the locale.</span></span> <span data-ttu-id="f15d1-105">Die maximale Anzahl von Zeichen, die für diese Zeichenfolge zulässig ist, ist 80, einschließlich eines abschließenden NULL-Zeichens.</span><span class="sxs-lookup"><span data-stu-id="f15d1-105">The maximum number of characters allowed for this string is 80, including a terminating null character.</span></span> <span data-ttu-id="f15d1-106">Die Zeichenfolge kann aus einer Kombination aus den [Format Bildern Day, month, year und ERA](day--month--year--and-era-format-pictures.md)bestehen.</span><span class="sxs-lookup"><span data-stu-id="f15d1-106">The string can consist of a combination of [day, month, year, and era format pictures](day--month--year--and-era-format-pictures.md).</span></span> <span data-ttu-id="f15d1-107">"M/d/yyyy" gibt beispielsweise an, dass der 3. September 2004 9/3/2004 ist.</span><span class="sxs-lookup"><span data-stu-id="f15d1-107">For example, "M/d/yyyy" indicates that September 3, 2004 is written 9/3/2004.</span></span>

<span data-ttu-id="f15d1-108">Gebiets Schemas können mehrere kurze Datumsformate definieren.</span><span class="sxs-lookup"><span data-stu-id="f15d1-108">Locales can define multiple short date formats.</span></span> <span data-ttu-id="f15d1-109">Um alle kurzen Datumsformate für dieses Gebiets Schema zu erhalten, verwenden Sie [enumdateformats](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsa), [enumdateformatsex](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexa)oder [enumdateformatsexex](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexex).</span><span class="sxs-lookup"><span data-stu-id="f15d1-109">To get all of the short date formats for this locale, use [EnumDateFormats](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsa), [EnumDateFormatsEx](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexa), or [EnumDateFormatsExEx](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexex).</span></span>

 

 



