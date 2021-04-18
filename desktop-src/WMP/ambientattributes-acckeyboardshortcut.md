---
title: Ambientattribute. accKeyboardShortcut
description: Das accKeyboardShortcut-Attribut gibt eine Tastenkombination für ein beliebiges Element an oder ruft diese ab.
ms.assetid: f97cffc9-4e7c-4226-9e02-0ea7f84b7450
keywords:
- Ambientattribute. accKeyboardShortcut-Fenster Media Player
topic_type:
- apiref
api_name:
- AmbientAttributes.accKeyboardShortcut
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67d7259f0b32e3575d902a83b6508383361028d8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368365"
---
# <a name="ambientattributesacckeyboardshortcut"></a><span data-ttu-id="90e56-104">Ambientattribute. accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="90e56-104">AmbientAttributes.accKeyboardShortcut</span></span>

<span data-ttu-id="90e56-105">Das **accKeyboardShortcut** -Attribut gibt eine Tastenkombination für ein beliebiges Element an oder ruft diese ab.</span><span class="sxs-lookup"><span data-stu-id="90e56-105">The **accKeyboardShortcut** attribute specifies or retrieves a keyboard shortcut description for any element.</span></span>

``` syntax
        elementID.accKeyboardShortcut
```

## <a name="possible-values"></a><span data-ttu-id="90e56-106">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="90e56-106">Possible Values</span></span>

<span data-ttu-id="90e56-107">Dieses Attribut ist eine Lese- **/schreibzeichenfolge** mit dem Standardwert "" (leere Zeichenfolge).</span><span class="sxs-lookup"><span data-stu-id="90e56-107">This attribute is a read/write **String** with a default value of "" (empty string).</span></span> <span data-ttu-id="90e56-108">Für das **Button** -Element hat dieses Attribut den Standardwert "Leertaste oder Eingabetaste".</span><span class="sxs-lookup"><span data-stu-id="90e56-108">For the **BUTTON** element, this attribute has a default value of "Spacebar or Enter".</span></span> <span data-ttu-id="90e56-109">Der Standardwert für das **Slider** -Element ist "rechter/Pfeil nach oben, um zu vergrößern, nach-unten/Pfeil nach unten".</span><span class="sxs-lookup"><span data-stu-id="90e56-109">For the **SLIDER** element, the default value is "Right/Up Arrow to increase, Left/Down Arrow to decrease".</span></span>

## <a name="remarks"></a><span data-ttu-id="90e56-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="90e56-110">Remarks</span></span>

<span data-ttu-id="90e56-111">Dieses Attribut wird für Barrierefreiheits Zwecke verwendet.</span><span class="sxs-lookup"><span data-stu-id="90e56-111">This attribute is used for accessibility purposes.</span></span> <span data-ttu-id="90e56-112">Sie ermöglicht es, dass eine Beschreibung der Tastenkombination für ein beliebiges Element von einem Reader-Programm gelesen wird.</span><span class="sxs-lookup"><span data-stu-id="90e56-112">It allows a description of the keyboard shortcut for any element to be read aloud by a reader program.</span></span> <span data-ttu-id="90e56-113">Dieses Attribut legt die Verknüpfung nicht fest.</span><span class="sxs-lookup"><span data-stu-id="90e56-113">This attribute does not set the shortcut.</span></span> <span data-ttu-id="90e56-114">Das Skript muss dies tun.</span><span class="sxs-lookup"><span data-stu-id="90e56-114">The scripter must do that work.</span></span>

<span data-ttu-id="90e56-115">Dieses Attribut gilt auch für Schaltflächen Elemente innerhalb des Steuer Elements der Schaltflächen Gruppe.</span><span class="sxs-lookup"><span data-stu-id="90e56-115">This attribute also applies to button elements inside the button group control.</span></span>

## <a name="requirements"></a><span data-ttu-id="90e56-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="90e56-116">Requirements</span></span>



| <span data-ttu-id="90e56-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="90e56-117">Requirement</span></span> | <span data-ttu-id="90e56-118">Wert</span><span class="sxs-lookup"><span data-stu-id="90e56-118">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="90e56-119">Version</span><span class="sxs-lookup"><span data-stu-id="90e56-119">Version</span></span><br/> | <span data-ttu-id="90e56-120">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="90e56-120">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="90e56-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="90e56-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90e56-122">**Ambient-Attribute**</span><span class="sxs-lookup"><span data-stu-id="90e56-122">**Ambient Attributes**</span></span>](ambient-attributes.md)
</dt> </dl>

 

 





