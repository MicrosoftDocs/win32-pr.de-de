---
title: Vol-Tag
description: Vol-Tag
ms.assetid: a6444eb2-79c2-4c86-8474-846d908479df
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7979278b2eb89c352b9e53f6141cb585fb0ed134
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036516"
---
# <a name="vol-tag"></a><span data-ttu-id="9f478-103">Vol-Tag</span><span class="sxs-lookup"><span data-stu-id="9f478-103">Vol Tag</span></span>

<span data-ttu-id="9f478-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="9f478-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="9f478-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9f478-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="9f478-106">Legt das Baseline-Lautstärke der Sprachausgabe fest.</span><span class="sxs-lookup"><span data-stu-id="9f478-106">Sets the baseline speaking volume of the speech output.</span></span>

</dd> <dt>

<span data-ttu-id="9f478-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="9f478-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="9f478-108">**\\Vol =***Zahl***\\**</span><span class="sxs-lookup"><span data-stu-id="9f478-108">**\\Vol=***number***\\**</span></span>



| <span data-ttu-id="9f478-109">Teil</span><span class="sxs-lookup"><span data-stu-id="9f478-109">Part</span></span>     | <span data-ttu-id="9f478-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9f478-110">Description</span></span>                                                         |
|----------|---------------------------------------------------------------------|
| <span data-ttu-id="9f478-111">*Zahl*</span><span class="sxs-lookup"><span data-stu-id="9f478-111">*number*</span></span> | <span data-ttu-id="9f478-112">Baselineversprechungvolume: 0 ist Ruhe und 65535 ist das maximale Volume.</span><span class="sxs-lookup"><span data-stu-id="9f478-112">Baseline speaking volume: 0 is silence and 65535 is maximum volume.</span></span> |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="9f478-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9f478-113">Remarks</span></span>

<span data-ttu-id="9f478-114">Die volumeeinstellung wirkt sich auf den linken und den rechten Kanal aus.</span><span class="sxs-lookup"><span data-stu-id="9f478-114">The volume setting affects both left and right channels.</span></span> <span data-ttu-id="9f478-115">Das Volume der einzelnen Kanäle kann nicht separat festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="9f478-115">You cannot set the volume of each channel separately.</span></span> <span data-ttu-id="9f478-116">Dieses Tag wird nur für die von TTS generierte Ausgabe unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9f478-116">This tag is supported only for TTS-generated output.</span></span>

 

 




