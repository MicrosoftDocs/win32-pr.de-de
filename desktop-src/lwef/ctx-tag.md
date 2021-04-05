---
title: CTX-Tag
description: CTX-Tag
ms.assetid: 96ceaa98-869d-4c51-a419-882cc9d40ae2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f16beae0fd4ccc062969d9aafb4d8747e4c5afe9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037202"
---
# <a name="ctx-tag"></a><span data-ttu-id="9532d-103">CTX-Tag</span><span class="sxs-lookup"><span data-stu-id="9532d-103">Ctx Tag</span></span>

<span data-ttu-id="9532d-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="9532d-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="9532d-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9532d-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="9532d-106">Legt den Kontext des Ausgabe Textes fest.</span><span class="sxs-lookup"><span data-stu-id="9532d-106">Sets the context of the output text.</span></span>

</dd> <dt>

<span data-ttu-id="9532d-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="9532d-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="9532d-108">\\**Ctx** = *Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="9532d-108">\\**Ctx**=*string*</span></span>\\



| <span data-ttu-id="9532d-109">Teil</span><span class="sxs-lookup"><span data-stu-id="9532d-109">Part</span></span>     | <span data-ttu-id="9532d-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9532d-110">Description</span></span>                                                                                                                                                                                                                                                                                      |
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9532d-111">*string*</span><span class="sxs-lookup"><span data-stu-id="9532d-111">*string*</span></span> | <span data-ttu-id="9532d-112">Eine Zeichenfolge, die den Text Kontext des nachfolgenden Texts angibt, der bestimmt, wie Symbole oder Abkürzungen gesprochen werden.</span><span class="sxs-lookup"><span data-stu-id="9532d-112">A string specifying the context of the text that follows, which determines how symbols or abbreviations are spoken.</span></span><br/> <span data-ttu-id="9532d-113">**"Address"**    Adressen und/oder Telefonnummern.</span><span class="sxs-lookup"><span data-stu-id="9532d-113">**"Address"**    Addresses and/or phone numbers.</span></span><br/> <span data-ttu-id="9532d-114">**"E-Mail"**    Elektronische e-Mail.</span><span class="sxs-lookup"><span data-stu-id="9532d-114">**"E-mail"**    Electronic mail.</span></span><br/> <span data-ttu-id="9532d-115">Der Kontext **"unknown"** (Standard) ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="9532d-115">**"Unknown"**    (Default) Context is unknown.</span></span><br/> |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="9532d-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9532d-116">Remarks</span></span>

<span data-ttu-id="9532d-117">Dieses Tag wird nur für die von TTS generierte Ausgabe unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9532d-117">This tag is supported only for TTS-generated output.</span></span> <span data-ttu-id="9532d-118">Der Wertebereich für den-Parameter kann abhängig von der installierten TTS-Engine variieren.</span><span class="sxs-lookup"><span data-stu-id="9532d-118">The range of values for the parameter may vary depending on the installed TTS engine.</span></span>

 

 





