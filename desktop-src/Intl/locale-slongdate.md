---
description: '\_Gebiets Schema slongdate'
ms.assetid: 1b72cd57-819e-4b1f-bbb0-b600a9e8631c
title: LOCALE_SLONGDATE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 503b24d81318f471b33a4ab644a059607e5ac490
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129685"
---
# <a name="locale_slongdate"></a><span data-ttu-id="ecff5-103">\_Gebiets Schema slongdate</span><span class="sxs-lookup"><span data-stu-id="ecff5-103">LOCALE\_SLONGDATE</span></span>

<span data-ttu-id="ecff5-104">Lange Datums Formatierungs Zeichenfolge für das Gebiets Schema.</span><span class="sxs-lookup"><span data-stu-id="ecff5-104">Long date formatting string for the locale.</span></span> <span data-ttu-id="ecff5-105">Die maximale Anzahl von Zeichen, die für diese Zeichenfolge zulässig ist, ist 80, einschließlich eines abschließenden NULL-Zeichens.</span><span class="sxs-lookup"><span data-stu-id="ecff5-105">The maximum number of characters allowed for this string is 80, including a terminating null character.</span></span> <span data-ttu-id="ecff5-106">Die Zeichenfolge kann aus einer Kombination von [Format Bildern für Tag, Monat, Jahr und ERA](day--month--year--and-era-format-pictures.md) bestehen und jede Zeichenfolge, die in einfache Anführungszeichen eingeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="ecff5-106">The string can consist of a combination of [day, month, year, and era format pictures](day--month--year--and-era-format-pictures.md) and any string of characters enclosed in single quotes.</span></span> <span data-ttu-id="ecff5-107">Zeichen in einfachen Anführungszeichen bleiben wie angegeben.</span><span class="sxs-lookup"><span data-stu-id="ecff5-107">Characters in single quotes remain as specified.</span></span> <span data-ttu-id="ecff5-108">Das lange Datum für Spanisch (Spanien) lautet beispielsweise "dddd, dd ' de ' MMMM ' de ' yyyy".</span><span class="sxs-lookup"><span data-stu-id="ecff5-108">For example, the Spanish (Spain) long date is "dddd, dd' de 'MMMM' de 'yyyy".</span></span> <span data-ttu-id="ecff5-109">Gebiets Schemas können mehrere lange Datumsformate definieren.</span><span class="sxs-lookup"><span data-stu-id="ecff5-109">Locales can define multiple long date formats.</span></span>

<span data-ttu-id="ecff5-110">Um alle langen Datumsformate für ein Gebiets Schema zu erhalten, verwenden Sie [enumdateformats](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsa), [enumdateformatsex](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexa)oder [enumdateformatsexex](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexex).</span><span class="sxs-lookup"><span data-stu-id="ecff5-110">To get all of the long date formats for a locale, use [EnumDateFormats](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsa), [EnumDateFormatsEx](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexa), or [EnumDateFormatsExEx](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexex).</span></span>

 

 



