---
title: Bookmark-Ereignis
description: Bookmark-Ereignis
ms.assetid: 6733cd4e-2ba0-4cff-b68d-abfea284f748
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0695ccd04f93eae46eaae66955c84fefb9e0c963
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206597"
---
# <a name="bookmark-event"></a><span data-ttu-id="2fb62-103">Bookmark-Ereignis</span><span class="sxs-lookup"><span data-stu-id="2fb62-103">Bookmark Event</span></span>

<span data-ttu-id="2fb62-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="2fb62-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="2fb62-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2fb62-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="2fb62-106">Tritt auf, wenn ein Lesezeichen in einer sprach Text Zeichenfolge aktiviert wird, die von der Anwendung definiert wurde</span><span class="sxs-lookup"><span data-stu-id="2fb62-106">Occurs when a bookmark in a speech text string that your application defined is activated.</span></span>

</dd> <dt>

<span data-ttu-id="2fb62-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="2fb62-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="2fb62-108">**Sub-** *Agent*- \_ **Lesezeichen** **(ByVal** - *BookmarkID \* \* *)**</span><span class="sxs-lookup"><span data-stu-id="2fb62-108">**Sub** *agent*\_**Bookmark** **(ByVal** *BookmarkID\*\*\*)*\*</span></span>



| <span data-ttu-id="2fb62-109">Teil</span><span class="sxs-lookup"><span data-stu-id="2fb62-109">Part</span></span>         | <span data-ttu-id="2fb62-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2fb62-110">Description</span></span>                                     |
|--------------|-------------------------------------------------|
| <span data-ttu-id="2fb62-111">*BookmarkID*</span><span class="sxs-lookup"><span data-stu-id="2fb62-111">*BookmarkID*</span></span> | <span data-ttu-id="2fb62-112">Eine lange ganze Zahl, die die Lesezeichen Nummer identifiziert.</span><span class="sxs-lookup"><span data-stu-id="2fb62-112">A Long integer identifying the bookmark number.</span></span> |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="2fb62-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2fb62-113">Remarks</span></span>

<span data-ttu-id="2fb62-114">Um ein Lesezeichen Ereignis anzugeben, verwenden Sie die [**Sprech**](speak-method.md) Methode mit einem **MRK** -Tag im angegebenen Text.</span><span class="sxs-lookup"><span data-stu-id="2fb62-114">To specify a bookmark event, use the [**Speak**](speak-method.md) method with a **Mrk** tag in your supplied text.</span></span> <span data-ttu-id="2fb62-115">Weitere Informationen zu Tags finden Sie unter Sprachausgabe Tags.</span><span class="sxs-lookup"><span data-stu-id="2fb62-115">For more information about tags, see Speech Output Tags.</span></span>

 

 




