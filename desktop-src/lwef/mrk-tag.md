---
title: MRK-Tag
description: MRK-Tag
ms.assetid: 1bc04853-f919-4f6f-90c2-21ac836bb1e4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 805a66b9ce5863bda7b7b95317bcab9cf1d80f32
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710511"
---
# <a name="mrk-tag"></a><span data-ttu-id="f6eb2-103">MRK-Tag</span><span class="sxs-lookup"><span data-stu-id="f6eb2-103">Mrk Tag</span></span>

<span data-ttu-id="f6eb2-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="f6eb2-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="f6eb2-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f6eb2-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="f6eb2-106">Definiert ein Lesezeichen im gesprochenen Text.</span><span class="sxs-lookup"><span data-stu-id="f6eb2-106">Defines a bookmark in the spoken text.</span></span>

</dd> <dt>

<span data-ttu-id="f6eb2-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="f6eb2-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="f6eb2-108">**\\MRK =***Zahl***\\**</span><span class="sxs-lookup"><span data-stu-id="f6eb2-108">**\\Mrk=***number***\\**</span></span>



| <span data-ttu-id="f6eb2-109">Teil</span><span class="sxs-lookup"><span data-stu-id="f6eb2-109">Part</span></span>     | <span data-ttu-id="f6eb2-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f6eb2-110">Description</span></span>                                        |
|----------|----------------------------------------------------|
| <span data-ttu-id="f6eb2-111">*Zahl*</span><span class="sxs-lookup"><span data-stu-id="f6eb2-111">*number*</span></span> | <span data-ttu-id="f6eb2-112">Ein Long Integer-Wert, der das Lesezeichen identifiziert.</span><span class="sxs-lookup"><span data-stu-id="f6eb2-112">A Long integer value that identifies the bookmark.</span></span> |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="f6eb2-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f6eb2-113">Remarks</span></span>

<span data-ttu-id="f6eb2-114">Wenn der Server ein Lesezeichen verarbeitet, wird ein Lesezeichen Ereignis generiert.</span><span class="sxs-lookup"><span data-stu-id="f6eb2-114">When the server processes a bookmark, it generates a bookmark event.</span></span> <span data-ttu-id="f6eb2-115">Sie müssen eine Zahl angeben, die größer als 0 (null) und nicht gleich 2147483647 oder 2147483646 ist.</span><span class="sxs-lookup"><span data-stu-id="f6eb2-115">You must specify a number greater than zero (0) and not equal to 2147483647 or 2147483646.</span></span>

 

 




