---
title: Left-Eigenschaft (Characters-Objekt)
description: Erfahren Sie mehr über die Left Characters-Objekteigenschaft. Microsoft Agent ist ab Windows 7 veraltet.
ms.assetid: f496f075-6430-4806-a237-1c7b626d355e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e2f860e6827a9c96c42014456e43b791ab70ed4
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/10/2021
ms.locfileid: "111988936"
---
# <a name="left-property-characters-object"></a><span data-ttu-id="96906-104">Left-Eigenschaft (Characters-Objekt)</span><span class="sxs-lookup"><span data-stu-id="96906-104">Left Property (Characters Object)</span></span>

<span data-ttu-id="96906-105">\[Microsoft Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="96906-105">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="96906-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="96906-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="96906-107">Gibt den linken Rand des Rahmens des angegebenen Zeichens zurück oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="96906-107">Returns or sets the left edge of the specified character's frame.</span></span>

</dd> <dt>

<span data-ttu-id="96906-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="96906-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="96906-109">*agent\***. Zeichen ("**_CharacterID_*_"). Linker_ \*  \[  =  *Wert*\]</span><span class="sxs-lookup"><span data-stu-id="96906-109">*agent\***.Characters ("**_CharacterID_*_").Left_\* \[ = *value*\]</span></span>



| <span data-ttu-id="96906-110">Teil</span><span class="sxs-lookup"><span data-stu-id="96906-110">Part</span></span>    | <span data-ttu-id="96906-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="96906-111">Description</span></span>                                                           |
|---------|-----------------------------------------------------------------------|
| <span data-ttu-id="96906-112">*value*</span><span class="sxs-lookup"><span data-stu-id="96906-112">*value*</span></span> | <span data-ttu-id="96906-113">Eine lange ganze Zahl, die den linken Rand des Rahmens des Zeichens angibt.</span><span class="sxs-lookup"><span data-stu-id="96906-113">A Long integer that specifies the left edge of the character's frame.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="96906-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="96906-114">Remarks</span></span>

<span data-ttu-id="96906-115">Die **Left-Eigenschaft** wird immer in Pixel ausgedrückt, relativ zum Ursprung des Bildschirms (links oben).</span><span class="sxs-lookup"><span data-stu-id="96906-115">The **Left** property is always expressed in pixels, relative to screen origin (upper left).</span></span> <span data-ttu-id="96906-116">Die Einstellung dieser Eigenschaft gilt für alle Clients des Zeichens.</span><span class="sxs-lookup"><span data-stu-id="96906-116">This property's setting applies to all clients of the character.</span></span>

<span data-ttu-id="96906-117">Obwohl das Zeichen in einem unregelmäßig angeordneten Bereichsfenster angezeigt wird, basiert die Position des Zeichens auf den externen Dimensionen des rechteckigen Animationsframes, der beim Kompilieren des Zeichens mit dem Microsoft Agent-Zeichen-Editor verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="96906-117">Even though the character appears in an irregularly shaped region window, the location of the character is based on the external dimensions of the rectangular animation frame used when the character was compiled with the Microsoft Agent Character Editor.</span></span>

 

 




