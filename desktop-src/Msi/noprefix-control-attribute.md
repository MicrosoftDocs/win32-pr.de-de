---
description: Wenn dieses Bit für ein Text Steuerelement festgelegt ist, wird das Vorkommen des Zeichens &\# 0034; &&\# 0034; in einer Text Zeichenfolge als sich selbst angezeigt. Wenn dieses Bit nicht festgelegt ist, wird das Zeichen, das \# auf &0034; &&\# 0034; in der Text Zeichenfolge folgt, als unterstrichendes Zeichen angezeigt.
ms.assetid: b958eecb-2f44-420f-8c93-7a4bd8b589da
title: NoPrefix-Steuerelement Attribut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae1e1a0c6da65605efca1aacc4582b34a8f673d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215118"
---
# <a name="noprefix-control-attribute"></a><span data-ttu-id="46aec-104">NoPrefix-Steuerelement Attribut</span><span class="sxs-lookup"><span data-stu-id="46aec-104">NoPrefix Control Attribute</span></span>

<span data-ttu-id="46aec-105">Wenn dieses Bit für ein Text Steuerelement festgelegt ist, wird das Vorkommen des Zeichens "&" in einer Text Zeichenfolge als sich selbst angezeigt.</span><span class="sxs-lookup"><span data-stu-id="46aec-105">If this bit is set on a text control, the occurrence of the character "&" in a text string is displayed as itself.</span></span> <span data-ttu-id="46aec-106">Wenn dieses Bit nicht festgelegt ist, wird das Zeichen, das auf "&" in der Text Zeichenfolge folgt, als unterstrichendes Zeichen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="46aec-106">If this bit is not set, then the character following "&" in the text string is displayed as an underscored character.</span></span>

## <a name="valid-controls"></a><span data-ttu-id="46aec-107">Gültige Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="46aec-107">Valid Controls</span></span>

[<span data-ttu-id="46aec-108">Text</span><span class="sxs-lookup"><span data-stu-id="46aec-108">Text</span></span>](text-control.md)

## <a name="value"></a><span data-ttu-id="46aec-109">Wert</span><span class="sxs-lookup"><span data-stu-id="46aec-109">Value</span></span>



| <span data-ttu-id="46aec-110">Decimal</span><span class="sxs-lookup"><span data-stu-id="46aec-110">Decimal</span></span> | <span data-ttu-id="46aec-111">Hexadezimal</span><span class="sxs-lookup"><span data-stu-id="46aec-111">Hexadecimal</span></span> | <span data-ttu-id="46aec-112">Konstante</span><span class="sxs-lookup"><span data-stu-id="46aec-112">Constant</span></span>                           |
|---------|-------------|------------------------------------|
| <span data-ttu-id="46aec-113">131072</span><span class="sxs-lookup"><span data-stu-id="46aec-113">131072</span></span>  | <span data-ttu-id="46aec-114">0x20000</span><span class="sxs-lookup"><span data-stu-id="46aec-114">0x20000</span></span>     | <span data-ttu-id="46aec-115">**msidbcontrolattributesnoprefix**</span><span class="sxs-lookup"><span data-stu-id="46aec-115">**msidbControlAttributesNoPrefix**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="46aec-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="46aec-116">Remarks</span></span>

<span data-ttu-id="46aec-117">Um dieses Attribut für ein Steuerelement festzulegen, schließen Sie das NoPrefix-Bit in die Spalte Attribute des Datensatzes des Steuer Elements in der [Steuerelement Tabelle](control-table.md)ein.</span><span class="sxs-lookup"><span data-stu-id="46aec-117">To set this attribute on a control, include the NoPrefix bit in the Attributes column of the control's record in the [Control table](control-table.md).</span></span>

<span data-ttu-id="46aec-118">Siehe [Steuerelement Attribute](control-attributes.md) und-Steuer [Elemente](controls.md).</span><span class="sxs-lookup"><span data-stu-id="46aec-118">See [Control Attributes](control-attributes.md) and [Controls](controls.md).</span></span>

 

 



