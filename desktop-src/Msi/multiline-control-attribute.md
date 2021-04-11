---
description: Wenn dieses Bit in einem Bearbeitungs Steuerelement festgelegt ist, erstellt das Installationsprogramm ein Bearbeitungs Steuerelement mit mehreren Zeilen mit einer vertikalen Scrollleiste.
ms.assetid: cbdbe088-9cf1-4af8-a5f7-072faee7f34e
title: Multiline-Steuerelement Attribut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 936bc4b3901293e950690e878a0f86229bb03b4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215477"
---
# <a name="multiline-control-attribute"></a><span data-ttu-id="f8e4d-103">Multiline-Steuerelement Attribut</span><span class="sxs-lookup"><span data-stu-id="f8e4d-103">MultiLine Control Attribute</span></span>

<span data-ttu-id="f8e4d-104">Wenn dieses Bit in einem [Bearbeitungs Steuer](edit-control.md)Element festgelegt ist, erstellt das Installationsprogramm ein Bearbeitungs Steuerelement mit mehreren Zeilen mit einer vertikalen Scrollleiste.</span><span class="sxs-lookup"><span data-stu-id="f8e4d-104">If this bit is set on an [Edit control](edit-control.md), the installer creates a multiple line edit control with a vertical scroll bar.</span></span>

<span data-ttu-id="f8e4d-105">Wenn dieses Bit nicht festgelegt ist, gibt es an, dass ein normales Bearbeitungs Steuerelement angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="f8e4d-105">If this bit is not set, it specifies displaying a normal edit control.</span></span>

## <a name="valid-controls"></a><span data-ttu-id="f8e4d-106">Gültige Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="f8e4d-106">Valid Controls</span></span>

<span data-ttu-id="f8e4d-107">[Bearbeitungs Steuer](edit-control.md)Element.</span><span class="sxs-lookup"><span data-stu-id="f8e4d-107">[Edit control](edit-control.md).</span></span>



| <span data-ttu-id="f8e4d-108">Decimal</span><span class="sxs-lookup"><span data-stu-id="f8e4d-108">Decimal</span></span> | <span data-ttu-id="f8e4d-109">Hexadezimal</span><span class="sxs-lookup"><span data-stu-id="f8e4d-109">Hexadecimal</span></span> | <span data-ttu-id="f8e4d-110">Konstante</span><span class="sxs-lookup"><span data-stu-id="f8e4d-110">Constant</span></span>                            |
|---------|-------------|-------------------------------------|
| <span data-ttu-id="f8e4d-111">65536</span><span class="sxs-lookup"><span data-stu-id="f8e4d-111">65536</span></span>   | <span data-ttu-id="f8e4d-112">0x00010000</span><span class="sxs-lookup"><span data-stu-id="f8e4d-112">0x00010000</span></span>  | <span data-ttu-id="f8e4d-113">**msidbcontrolattributesmultiline**</span><span class="sxs-lookup"><span data-stu-id="f8e4d-113">**msidbControlAttributesMultiline**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="f8e4d-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f8e4d-114">Remarks</span></span>

<span data-ttu-id="f8e4d-115">Um dieses Attribut für ein Steuerelement festzulegen, schließen Sie das mehrzeilige Bit in die Spalte Attribute des Datensatzes des Steuer Elements in der [Steuerelement Tabelle](control-table.md)ein.</span><span class="sxs-lookup"><span data-stu-id="f8e4d-115">To set this attribute on a control, include the MultiLine bit in the Attributes column of the control's record in the [Control table](control-table.md).</span></span>

<span data-ttu-id="f8e4d-116">Siehe [Steuerelement Attribute](control-attributes.md) und-Steuer [Elemente](controls.md).</span><span class="sxs-lookup"><span data-stu-id="f8e4d-116">See [Control Attributes](control-attributes.md) and [Controls](controls.md).</span></span>

 

 



