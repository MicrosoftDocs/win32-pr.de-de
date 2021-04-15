---
title: BorderColor-Eigenschaft
description: BorderColor-Eigenschaft
ms.assetid: 7592db02-c157-45f4-bbcf-e6d5bd99e8e8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6981d3ac280669f64219961b74d05c6ba73f1008
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471205"
---
# <a name="bordercolor-property"></a><span data-ttu-id="cb02c-103">BorderColor-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="cb02c-103">BorderColor Property</span></span>

<span data-ttu-id="cb02c-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="cb02c-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="cb02c-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="cb02c-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="cb02c-106">Gibt die Rahmenfarbe zurück, die zurzeit für das Wort sprecherfenster für das angegebene Zeichen angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="cb02c-106">Returns the border color currently displayed for the word balloon window for the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="cb02c-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="cb02c-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="cb02c-108">\*-Agent ***. Zeichen ("*** Merkmal-ID \***").** Sprechblase. BorderColor</span><span class="sxs-lookup"><span data-stu-id="cb02c-108">*agent ***.Characters ("*** CharacterID\*\*\*").*\* Balloon.BorderColor</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cb02c-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cb02c-109">Remarks</span></span>

<span data-ttu-id="cb02c-110">Der gültige Bereich für eine normale RGB-Farbe ist 0 bis 16.777.215 (&HFFFFFF).</span><span class="sxs-lookup"><span data-stu-id="cb02c-110">The valid range for a normal RGB color is 0 to 16,777,215 (&HFFFFFF).</span></span> <span data-ttu-id="cb02c-111">Das hohe Byte einer Zahl in diesem Bereich ist 0 (null). die unteren 3 Bytes, vom minimal bis zum höchst wertigen Byte, bestimmen die Größe von rot, grün und blau.</span><span class="sxs-lookup"><span data-stu-id="cb02c-111">The high byte of a number in this range equals 0; the lower 3 bytes, from least to most significant byte, determine the amount of red, green, and blue, respectively.</span></span> <span data-ttu-id="cb02c-112">Der rote, grüne und blaue Farbanteil werden jeweils durch eine Zahl zwischen 0 und 255 (&HFF) dargestellt.</span><span class="sxs-lookup"><span data-stu-id="cb02c-112">The red, green, and blue components are each represented by a number between 0 and 255 (&HFF).</span></span>

 

 




