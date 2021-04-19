---
description: Wenn dieses Bit festgelegt ist, wird der Text im Steuerelement in einer einzelnen Zeile angezeigt. Wenn der Text die Ränder des Steuer Elements überschreitet, wird er abgeschnitten und ein Auslassungs Zeichen (&\# 0034;... &\# 0034;) wird am Ende eingefügt, um das Abschneiden anzugeben. Wenn dieses Bit nicht festgelegt ist, wird Text umschlossen.
ms.assetid: 0dec3d25-0da7-4054-8d5c-55e81be16489
title: NoWrap-Steuerelement Attribut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51ee40b52fbec1c8add841f7055a7f42667eca94
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360601"
---
# <a name="nowrap-control-attribute"></a><span data-ttu-id="1d6b8-105">NoWrap-Steuerelement Attribut</span><span class="sxs-lookup"><span data-stu-id="1d6b8-105">NoWrap Control Attribute</span></span>

<span data-ttu-id="1d6b8-106">Wenn dieses Bit festgelegt ist, wird der Text im Steuerelement in einer einzelnen Zeile angezeigt.</span><span class="sxs-lookup"><span data-stu-id="1d6b8-106">If this bit is set the text in the control is displayed on a single line.</span></span> <span data-ttu-id="1d6b8-107">Wenn der Text die Ränder des Steuer Elements überschreitet, wird er abgeschnitten, und am Ende wird ein Auslassungs Zeichen ("...") eingefügt, um das Abschneiden anzugeben.</span><span class="sxs-lookup"><span data-stu-id="1d6b8-107">If the text extends beyond the control's margins it is truncated and an ellipsis ("...") is inserted at the end to indicate the truncation.</span></span> <span data-ttu-id="1d6b8-108">Wenn dieses Bit nicht festgelegt ist, wird Text umschlossen.</span><span class="sxs-lookup"><span data-stu-id="1d6b8-108">If this bit is not set, text wraps.</span></span>

## <a name="valid-controls"></a><span data-ttu-id="1d6b8-109">Gültige Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="1d6b8-109">Valid Controls</span></span>

[<span data-ttu-id="1d6b8-110">Text</span><span class="sxs-lookup"><span data-stu-id="1d6b8-110">Text</span></span>](text-control.md)

## <a name="value"></a><span data-ttu-id="1d6b8-111">Wert</span><span class="sxs-lookup"><span data-stu-id="1d6b8-111">Value</span></span>



| <span data-ttu-id="1d6b8-112">Decimal</span><span class="sxs-lookup"><span data-stu-id="1d6b8-112">Decimal</span></span> | <span data-ttu-id="1d6b8-113">Hexadezimal</span><span class="sxs-lookup"><span data-stu-id="1d6b8-113">Hexadecimal</span></span> | <span data-ttu-id="1d6b8-114">Konstante</span><span class="sxs-lookup"><span data-stu-id="1d6b8-114">Constant</span></span>                         |
|---------|-------------|----------------------------------|
| <span data-ttu-id="1d6b8-115">262144</span><span class="sxs-lookup"><span data-stu-id="1d6b8-115">262144</span></span>  | <span data-ttu-id="1d6b8-116">0x00040000</span><span class="sxs-lookup"><span data-stu-id="1d6b8-116">0x00040000</span></span>  | <span data-ttu-id="1d6b8-117">**msidbcontrolattributesnowrap**</span><span class="sxs-lookup"><span data-stu-id="1d6b8-117">**msidbControlAttributesNoWrap**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="1d6b8-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1d6b8-118">Remarks</span></span>

<span data-ttu-id="1d6b8-119">Um dieses Attribut für ein Steuerelement festzulegen, schließen Sie das nowrap-Bit in die Spalte Attribute des Datensatzes des Steuer Elements in der [Steuerelement Tabelle](control-table.md)ein.</span><span class="sxs-lookup"><span data-stu-id="1d6b8-119">To set this attribute on a control, include the NoWrap bit in the Attributes column of the control's record in the [Control table](control-table.md).</span></span>

<span data-ttu-id="1d6b8-120">Siehe [Steuerelement Attribute](control-attributes.md) und-Steuer [Elemente](controls.md).</span><span class="sxs-lookup"><span data-stu-id="1d6b8-120">See [Control Attributes](control-attributes.md) and [Controls](controls.md).</span></span>

 

 



