---
description: Wenn das combolist-Steuerelement Bit in einem Kombinations Feld festgelegt ist, wird das Bearbeitungsfeld durch ein statisches Textfeld ersetzt. Dadurch wird verhindert, dass ein Benutzer einen neuen Wert eingibt, und der Benutzer muss nur einen der vordefinierten Werte auswählen.
ms.assetid: 79af4bb0-1e0f-4df3-ae25-d2798842adb6
title: Combolist-Steuerelement Attribut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2dcb1c51e8eccaba03c3b4d905b0501e8a3f97a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352430"
---
# <a name="combolist-control-attribute"></a><span data-ttu-id="c1e7d-104">Combolist-Steuerelement Attribut</span><span class="sxs-lookup"><span data-stu-id="c1e7d-104">ComboList Control Attribute</span></span>

<span data-ttu-id="c1e7d-105">Wenn das combolist-Steuerelement Bit in einem Kombinations Feld festgelegt ist, wird das Bearbeitungsfeld durch ein statisches Textfeld ersetzt.</span><span class="sxs-lookup"><span data-stu-id="c1e7d-105">If the ComboList Control bit is set on a combo box, the edit field is replaced by a static text field.</span></span> <span data-ttu-id="c1e7d-106">Dadurch wird verhindert, dass ein Benutzer einen neuen Wert eingibt, und der Benutzer muss nur einen der vordefinierten Werte auswählen.</span><span class="sxs-lookup"><span data-stu-id="c1e7d-106">This prevents a user from entering a new value and requires the user to choose only one of the predefined values.</span></span>

<span data-ttu-id="c1e7d-107">Wenn dieses Bit nicht festgelegt ist, weist das Kombinations Feld ein Bearbeitungsfeld auf.</span><span class="sxs-lookup"><span data-stu-id="c1e7d-107">If this bit is not set, the combo box has an edit field.</span></span>

## <a name="valid-controls"></a><span data-ttu-id="c1e7d-108">Gültige Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="c1e7d-108">Valid Controls</span></span>

[<span data-ttu-id="c1e7d-109">ComboBox</span><span class="sxs-lookup"><span data-stu-id="c1e7d-109">ComboBox</span></span>](combobox-control.md)

## <a name="value"></a><span data-ttu-id="c1e7d-110">Wert</span><span class="sxs-lookup"><span data-stu-id="c1e7d-110">Value</span></span>



| <span data-ttu-id="c1e7d-111">Decimal</span><span class="sxs-lookup"><span data-stu-id="c1e7d-111">Decimal</span></span> | <span data-ttu-id="c1e7d-112">Hexadezimal</span><span class="sxs-lookup"><span data-stu-id="c1e7d-112">Hexadecimal</span></span> | <span data-ttu-id="c1e7d-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c1e7d-113">Description</span></span>                     |
|---------|-------------|---------------------------------|
| <span data-ttu-id="c1e7d-114">131072</span><span class="sxs-lookup"><span data-stu-id="c1e7d-114">131072</span></span>  | <span data-ttu-id="c1e7d-115">0x00020000</span><span class="sxs-lookup"><span data-stu-id="c1e7d-115">0x00020000</span></span>  | <span data-ttu-id="c1e7d-116">msidbcontrolattributescombolist</span><span class="sxs-lookup"><span data-stu-id="c1e7d-116">msidbControlAttributesComboList</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="c1e7d-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c1e7d-117">Remarks</span></span>

<span data-ttu-id="c1e7d-118">Um dieses Attribut für ein Steuerelement festzulegen, schließen Sie das combolist-Bit in die Spalte Attribute des Datensatzes des Steuer Elements in der [Steuerelement Tabelle](control-table.md)ein.</span><span class="sxs-lookup"><span data-stu-id="c1e7d-118">To set this attribute on a control, include the ComboList bit in the Attributes column of the control's record in the [Control table](control-table.md).</span></span>

<span data-ttu-id="c1e7d-119">Siehe [Steuerelement Attribute](control-attributes.md) und das Steuerelement, das Sie unter Steuer [Elementen](controls.md)erstellen müssen.</span><span class="sxs-lookup"><span data-stu-id="c1e7d-119">See [Control Attributes](control-attributes.md) and the control you need to create under [Controls](controls.md).</span></span>

 

 



