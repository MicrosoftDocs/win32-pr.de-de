---
description: Wenn dieses Bitflag festgelegt ist, werden die Schriftarten mithilfe der standardmäßigen UI-Codepage des Benutzers erstellt. Wenn das Bitflag nicht festgelegt ist, werden die Schriftarten mithilfe der Daten Bank Codepage erstellt.
ms.assetid: 6a3dbabe-6a14-4401-b46c-e8a0bd0cbe63
title: Userslanguage-Steuerelement Attribut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aff4109c5c0819b199343bb8ee38bfecc069ad4f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106357512"
---
# <a name="userslanguage-control-attribute"></a><span data-ttu-id="30313-104">Userslanguage-Steuerelement Attribut</span><span class="sxs-lookup"><span data-stu-id="30313-104">UsersLanguage Control Attribute</span></span>

<span data-ttu-id="30313-105">Wenn dieses Bitflag festgelegt ist, werden die Schriftarten mithilfe der standardmäßigen UI-Codepage des Benutzers erstellt.</span><span class="sxs-lookup"><span data-stu-id="30313-105">If this bit flag is set, fonts are created using the user's default UI code page.</span></span> <span data-ttu-id="30313-106">Wenn das Bitflag nicht festgelegt ist, werden die Schriftarten mithilfe der Daten Bank Codepage erstellt.</span><span class="sxs-lookup"><span data-stu-id="30313-106">If the bit flag is not set, fonts are created using the database code page.</span></span>

## <a name="valid-controls"></a><span data-ttu-id="30313-107">Gültige Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="30313-107">Valid Controls</span></span>

[<span data-ttu-id="30313-108">Text</span><span class="sxs-lookup"><span data-stu-id="30313-108">Text</span></span>](text-control.md)

 

[<span data-ttu-id="30313-109">ListBox</span><span class="sxs-lookup"><span data-stu-id="30313-109">ListBox</span></span>](listbox-control.md)

 

[<span data-ttu-id="30313-110">ComboBox</span><span class="sxs-lookup"><span data-stu-id="30313-110">ComboBox</span></span>](combobox-control.md)

## <a name="value"></a><span data-ttu-id="30313-111">Wert</span><span class="sxs-lookup"><span data-stu-id="30313-111">Value</span></span>



| <span data-ttu-id="30313-112">Decimal</span><span class="sxs-lookup"><span data-stu-id="30313-112">Decimal</span></span> | <span data-ttu-id="30313-113">Hexadezimal</span><span class="sxs-lookup"><span data-stu-id="30313-113">Hexadecimal</span></span> | <span data-ttu-id="30313-114">Konstante</span><span class="sxs-lookup"><span data-stu-id="30313-114">Constant</span></span>                                |
|---------|-------------|-----------------------------------------|
| <span data-ttu-id="30313-115">1048576</span><span class="sxs-lookup"><span data-stu-id="30313-115">1048576</span></span> | <span data-ttu-id="30313-116">0x00100000</span><span class="sxs-lookup"><span data-stu-id="30313-116">0x00100000</span></span>  | <span data-ttu-id="30313-117">**msidbcontrolattributesuserslanguage**</span><span class="sxs-lookup"><span data-stu-id="30313-117">**msidbControlAttributesUsersLanguage**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="30313-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="30313-118">Remarks</span></span>

<span data-ttu-id="30313-119">Dieses Steuerelement kann verwendet werden, um Text anzuzeigen, den der Benutzer in ein [Edit](edit-control.md) -oder [pathedit](pathedit-control.md) -Steuerelement eingegeben hat.</span><span class="sxs-lookup"><span data-stu-id="30313-119">This control attribute can be used to display text that the user has entered into an [Edit](edit-control.md) or [PathEdit](pathedit-control.md) control.</span></span>

<span data-ttu-id="30313-120">Das Bearbeitungs Steuerelement, das Steuerelement "pathedit", das [Director-Listen Steuer](directorylist-control.md) Element und das [directoriycombo-Steuer](directorycombo-control.md) Element verwenden immer die Schriftarten, die auf der Benutzeroberfläche der Standardbenutzer Oberfläche</span><span class="sxs-lookup"><span data-stu-id="30313-120">The Edit control, PathEdit control, [DirectoryList control](directorylist-control.md) and [DirectoryCombo control](directorycombo-control.md) always use the fonts created in the user's default UI code page.</span></span> <span data-ttu-id="30313-121">Dies kann Probleme verursachen, wenn zusätzliche Sprachen auf dem Betriebssystem installiert wurden.</span><span class="sxs-lookup"><span data-stu-id="30313-121">This can cause problems if additional languages have been installed on the operating system.</span></span> <span data-ttu-id="30313-122">In diesem Fall sind die Schriftarten auf dem Computer möglicherweise nicht in der Lage, alle Zeichen in den hinzugefügten Sprachen darzustellen.</span><span class="sxs-lookup"><span data-stu-id="30313-122">In this case, the fonts on the computer may not be able to represent all the characters in the added languages.</span></span> <span data-ttu-id="30313-123">Um zu ermitteln, welche Schriftarten verwendet werden können, suchen Sie nach den Werten in **HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ fontlink \\ Systemlink**.</span><span class="sxs-lookup"><span data-stu-id="30313-123">To determine what fonts can be used, look up the values in **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\FontLink\\SystemLink**.</span></span>

<span data-ttu-id="30313-124">Weitere Informationen finden Sie unter [Steuerelement Attribute](control-attributes.md) und-Steuer [Elemente](controls.md).</span><span class="sxs-lookup"><span data-stu-id="30313-124">For more information, see [Control Attributes](control-attributes.md) and [Controls](controls.md).</span></span>

 

 



