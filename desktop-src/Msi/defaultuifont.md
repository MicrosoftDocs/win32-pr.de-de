---
description: Die defaultuifont-Eigenschaft legt den für Steuerelemente verwendeten Standard Schriftstil fest. Um die Standardeinstellung anzugeben, legen Sie defaultuifont auf eines der vordefinierten Stile in der Tabelle "TextStyle" in der Eigenschaften Tabelle fest.
ms.assetid: 594183ce-ef13-47f6-a4ae-37ba09c06cbd
title: Defaultuifont (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3791219dcef84253280fec3c797f2035afd239f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372783"
---
# <a name="defaultuifont-property"></a><span data-ttu-id="e6ee4-104">Defaultuifont (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="e6ee4-104">DefaultUIFont property</span></span>

<span data-ttu-id="e6ee4-105">Die **defaultuifont** -Eigenschaft legt den für Steuerelemente verwendeten Standard Schriftstil fest.</span><span class="sxs-lookup"><span data-stu-id="e6ee4-105">The **DefaultUIFont** property sets the default font style used for controls.</span></span> <span data-ttu-id="e6ee4-106">Um die Standardeinstellung anzugeben, legen Sie **defaultuifont** auf eines der vordefinierten Stile in der [Tabelle "TextStyle](textstyle-table.md) " in der [Eigenschaften Tabelle](property-table.md)fest.</span><span class="sxs-lookup"><span data-stu-id="e6ee4-106">To specify the default, set **DefaultUIFont** to one of the predefined styles in the [TextStyle table](textstyle-table.md) in the [Property table](property-table.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e6ee4-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e6ee4-107">Remarks</span></span>

<span data-ttu-id="e6ee4-108">Die **defaultuifont** -Eigenschaft jedes Installationspakets mit einer Benutzeroberfläche sollte in der [Eigenschaften Tabelle](property-table.md) auf einen der vordefinierten Stile in der [TextStyle-Tabelle](textstyle-table.md)festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="e6ee4-108">The **DefaultUIFont** property of every installation package with a UI should be set in the [Property table](property-table.md) to one of the predefined styles listed in the [TextStyle table](textstyle-table.md).</span></span> <span data-ttu-id="e6ee4-109">Wenn diese Eigenschaft nicht angegeben wird, verwendet das Installationsprogramm die System Schriftart.</span><span class="sxs-lookup"><span data-stu-id="e6ee4-109">If this property is not specified, the installer uses the System font.</span></span> <span data-ttu-id="e6ee4-110">Dies kann dazu führen, dass das Installationsprogramm Text Zeichenfolgen nicht ordnungsgemäß anzeigt, wenn sich die Codepage des Pakets von der standardmäßigen UI-Codepage des Benutzers unterscheidet.</span><span class="sxs-lookup"><span data-stu-id="e6ee4-110">This can cause the installer to improperly display text strings when the package's code page is different from the user's default UI code page.</span></span>

<span data-ttu-id="e6ee4-111">Der Text und der Schrift Schnitt eines Steuer Elements können wie unter [Hinzufügen von Steuerelementen und Text](adding-controls-and-text.md)beschrieben festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="e6ee4-111">The text and font style of a control can be set as described in [Adding Controls and Text](adding-controls-and-text.md).</span></span> <span data-ttu-id="e6ee4-112">Wenn die Zeichenfolge, die in der Text-Spalte der [Steuerelement Tabelle](control-table.md) oder der Tabelle " [bbcontrol](bbcontrol-table.md) " aufgeführt ist, den Schrift Schnitt nicht angibt, verwendet das Steuerelement den Wert der **defaultuifont** -Eigenschaft als Schriftart Stil.</span><span class="sxs-lookup"><span data-stu-id="e6ee4-112">If the character string listed in the Text column of the [Control table](control-table.md) or [BBControl table](bbcontrol-table.md) does not specify the font style, the control uses the value of the **DefaultUIFont** property as the font style.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6ee4-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e6ee4-113">Requirements</span></span>



| <span data-ttu-id="e6ee4-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e6ee4-114">Requirement</span></span> | <span data-ttu-id="e6ee4-115">Wert</span><span class="sxs-lookup"><span data-stu-id="e6ee4-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6ee4-116">Version</span><span class="sxs-lookup"><span data-stu-id="e6ee4-116">Version</span></span><br/> | <span data-ttu-id="e6ee4-117">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="e6ee4-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="e6ee4-118">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e6ee4-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="e6ee4-119">Windows Installer unter Windows Server 2003 oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="e6ee4-119">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="e6ee4-120">Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="e6ee4-120">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e6ee4-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e6ee4-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6ee4-122">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e6ee4-122">Properties</span></span>](properties.md)
</dt> </dl>

 

 




