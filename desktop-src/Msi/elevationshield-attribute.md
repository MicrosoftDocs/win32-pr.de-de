---
description: Dieses Attribut fügt dem PUSHBUTTON-Steuerelement das Symbol für die Rechte Erweiterung (User Account Control, UAC) (Schild Symbol) hinzu.
ms.assetid: ec52d660-eb83-4f27-b640-ea89156260aa
title: Elevationshield-Attribut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4c580beefd1d2c0a80b0ee63b7a44e58a2a2fae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131789"
---
# <a name="elevationshield-attribute"></a><span data-ttu-id="f2e15-103">Elevationshield-Attribut</span><span class="sxs-lookup"><span data-stu-id="f2e15-103">ElevationShield Attribute</span></span>

<span data-ttu-id="f2e15-104">Dieses Attribut fügt dem [PUSHBUTTON-Steuer](pushbutton-control.md)Element das Symbol für die Rechte Erweiterung ( [*User Account Control*](u-gly.md) , UAC) (Schild Symbol) hinzu.</span><span class="sxs-lookup"><span data-stu-id="f2e15-104">This attribute adds the [*User Account Control*](u-gly.md) (UAC) elevation icon (shield icon) to the [PushButton control](pushbutton-control.md).</span></span>

<span data-ttu-id="f2e15-105">Wenn dieses Bit festgelegt ist und die Installation noch nicht mit [*erhöhten*](e-gly.md) Rechten ausgeführt wird, wird das PUSHBUTTON-Steuerelement mithilfe des Erweiterungs Symbols für die [*Benutzerkontensteuerung (User Account Control*](u-gly.md) , UAC) erstellt.</span><span class="sxs-lookup"><span data-stu-id="f2e15-105">If this bit is set, and the installation is not yet running with [*elevated*](e-gly.md) privileges, the pushbutton control is created using the [*User Account Control*](u-gly.md) (UAC) elevation icon (shield icon).</span></span>

<span data-ttu-id="f2e15-106">Wenn dieses Bit festgelegt ist und die Installation bereits mit [*erhöhten*](e-gly.md) Rechten ausgeführt wird, wird das PUSHBUTTON-Steuerelement mithilfe der anderen Symbol Attribute erstellt.</span><span class="sxs-lookup"><span data-stu-id="f2e15-106">If this bit is set, and the installation is already running with [*elevated*](e-gly.md) privileges, the pushbutton control is created using the other icon attributes.</span></span>

<span data-ttu-id="f2e15-107">Wenn dieses Bit nicht festgelegt ist, wird das PUSHBUTTON-Steuerelement mithilfe der anderen Symbol Attribute erstellt.</span><span class="sxs-lookup"><span data-stu-id="f2e15-107">If this bit is not set, the pushbutton control is created using the other icon attributes.</span></span>

## <a name="valid-controls"></a><span data-ttu-id="f2e15-108">Gültige Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="f2e15-108">Valid Controls</span></span>

[<span data-ttu-id="f2e15-109">PUSHBUTTON</span><span class="sxs-lookup"><span data-stu-id="f2e15-109">PushButton</span></span>](pushbutton-control.md)

## <a name="value"></a><span data-ttu-id="f2e15-110">Wert</span><span class="sxs-lookup"><span data-stu-id="f2e15-110">Value</span></span>



| <span data-ttu-id="f2e15-111">Decimal</span><span class="sxs-lookup"><span data-stu-id="f2e15-111">Decimal</span></span> | <span data-ttu-id="f2e15-112">Hexadezimal</span><span class="sxs-lookup"><span data-stu-id="f2e15-112">Hexadecimal</span></span> | <span data-ttu-id="f2e15-113">Konstante</span><span class="sxs-lookup"><span data-stu-id="f2e15-113">Constant</span></span>                                  |
|---------|-------------|-------------------------------------------|
| <span data-ttu-id="f2e15-114">8388608</span><span class="sxs-lookup"><span data-stu-id="f2e15-114">8388608</span></span> | <span data-ttu-id="f2e15-115">0x00800000</span><span class="sxs-lookup"><span data-stu-id="f2e15-115">0x00800000</span></span>  | <span data-ttu-id="f2e15-116">**msidbcontrolattributeselevationshield**</span><span class="sxs-lookup"><span data-stu-id="f2e15-116">**msidbControlAttributesElevationShield**</span></span> |



 

 

 



