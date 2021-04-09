---
title: BackColor-Eigenschaft (Features der Legacy-Windows-Umgebung)
description: BackColor-Eigenschaft
ms.assetid: a82c23bc-b280-4a52-9272-68879557cac7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3332fcc6a9081b52300dbee4c69c77602e84a62e
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "103739656"
---
# <a name="backcolor-property-legacy-windows-environment-features"></a><span data-ttu-id="42f11-103">BackColor-Eigenschaft (Features der Legacy-Windows-Umgebung)</span><span class="sxs-lookup"><span data-stu-id="42f11-103">BackColor Property (Legacy Windows Environment Features)</span></span>

<span data-ttu-id="42f11-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="42f11-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="42f11-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="42f11-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="42f11-106">Gibt die Hintergrundfarbe zurück, die derzeit im Word-sprecherfenster für das angegebene Zeichen angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="42f11-106">Returns the background color currently displayed in the word balloon window for the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="42f11-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="42f11-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="42f11-108">\*Agent \***. Zeichen ("**_Merkmal-ID_*_"). Sprechblase. BackColor_*</span><span class="sxs-lookup"><span data-stu-id="42f11-108">*agent\***.Characters ("**_CharacterID_*_").Balloon.BackColor_\*</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="42f11-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="42f11-109">Remarks</span></span>

<span data-ttu-id="42f11-110">Der gültige Bereich für eine normale RGB-Farbe ist 0 bis 16.777.215 (&HFFFFFF).</span><span class="sxs-lookup"><span data-stu-id="42f11-110">The valid range for a normal RGB color is 0 to 16,777,215 (&HFFFFFF).</span></span> <span data-ttu-id="42f11-111">Das hohe Byte einer Zahl in diesem Bereich ist 0 (null). die unteren 3 Bytes, vom minimal bis zum höchst wertigen Byte, bestimmen die Größe von rot, grün und blau.</span><span class="sxs-lookup"><span data-stu-id="42f11-111">The high byte of a number in this range equals 0; the lower 3 bytes, from least to most significant byte, determine the amount of red, green, and blue, respectively.</span></span> <span data-ttu-id="42f11-112">Der rote, grüne und blaue Farbanteil werden jeweils durch eine Zahl zwischen 0 und 255 (&HFF) dargestellt.</span><span class="sxs-lookup"><span data-stu-id="42f11-112">The red, green, and blue components are each represented by a number between 0 and 255 (&HFF).</span></span>

 

 




