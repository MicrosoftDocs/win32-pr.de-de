---
title: ForeColor-Eigenschaft
description: ForeColor-Eigenschaft
ms.assetid: b5cef81b-55e1-49a5-bdbf-f7101520a13a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ef05c9f51e040326c75f142e4649a8dbd0cfdbb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855632"
---
# <a name="forecolor-property"></a><span data-ttu-id="a11d2-103">ForeColor-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="a11d2-103">ForeColor Property</span></span>

<span data-ttu-id="a11d2-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="a11d2-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="a11d2-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a11d2-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="a11d2-106">Gibt die Vordergrundfarbe zurück, die derzeit im Word-sprecherfenster für das angegebene Zeichen angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="a11d2-106">Returns the foreground color currently displayed in the word balloon window for the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="a11d2-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="a11d2-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="a11d2-108">*Agent ***. Zeichen ("*** Merkmal-ID \* \* *"). Sprechblase. ForeColor**</span><span class="sxs-lookup"><span data-stu-id="a11d2-108">*agent ***.Characters ("*** CharacterID\*\*\*").Balloon.ForeColor*\*</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a11d2-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a11d2-109">Remarks</span></span>

<span data-ttu-id="a11d2-110">Die **ForeColor** -Eigenschaft gibt einen Wert zurück, der die Textfarbe in der Wort Sprechblase angibt.</span><span class="sxs-lookup"><span data-stu-id="a11d2-110">The **ForeColor** property returns a value that specifies the color of text in the word balloon.</span></span> <span data-ttu-id="a11d2-111">Der gültige Bereich für eine normale RGB-Farbe ist 0 bis 16.777.215 (&HFFFFFF).</span><span class="sxs-lookup"><span data-stu-id="a11d2-111">The valid range for a normal RGB color is 0 to 16,777,215 (&HFFFFFF).</span></span> <span data-ttu-id="a11d2-112">Das hohe Byte einer Zahl in diesem Bereich ist 0 (null). die unteren 3 Bytes, vom minimal bis zum höchst wertigen Byte, bestimmen die Größe von rot, grün und blau.</span><span class="sxs-lookup"><span data-stu-id="a11d2-112">The high byte of a number in this range equals 0; the lower 3 bytes, from least to most significant byte, determine the amount of red, green, and blue, respectively.</span></span> <span data-ttu-id="a11d2-113">Der rote, grüne und blaue Farbanteil werden jeweils durch eine Zahl zwischen 0 und 255 (&HFF) dargestellt.</span><span class="sxs-lookup"><span data-stu-id="a11d2-113">The red, green, and blue components are each represented by a number between 0 and 255 (&HFF).</span></span>

 

 




