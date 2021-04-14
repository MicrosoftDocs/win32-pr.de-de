---
description: Wenn Sie Microsoft Windows-Dialogfelder verwenden, müssen Sie alle Steuerelemente bezeichnen, um die sprach Funktionalität zu vereinfachen. Im folgenden Dialogfeld Ausführen wird eine statische Text Steuerelement-Bezeichnung für ein Dropdown-Listenfeld angezeigt. Statischer Text endet mit einem Doppelpunkt.
ms.assetid: 3b01a4d2-9deb-413f-bab8-566df86b6af9
title: Benennen von Steuerelementen in Dialog Feldern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f0f74ecb3737b422450388ee87ab4177e899aa6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104565119"
---
# <a name="naming-controls-in-dialog-boxes"></a><span data-ttu-id="12eda-105">Benennen von Steuerelementen in Dialog Feldern</span><span class="sxs-lookup"><span data-stu-id="12eda-105">Naming Controls in Dialog Boxes</span></span>

<span data-ttu-id="12eda-106">Wenn Sie Microsoft Windows-Dialogfelder verwenden, müssen Sie alle Steuerelemente bezeichnen, um die sprach Funktionalität zu vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="12eda-106">When using Microsoft Windows dialog boxes, you must label all controls to facilitate speech functionality.</span></span> <span data-ttu-id="12eda-107">Im folgenden Dialogfeld **Ausführen** wird eine statische Text Steuerelement-Bezeichnung für ein Dropdown-Listenfeld angezeigt.</span><span class="sxs-lookup"><span data-stu-id="12eda-107">The following **Run** dialog box shows a static text control label for a drop-down list box.</span></span> <span data-ttu-id="12eda-108">Statischer Text endet mit einem Doppelpunkt.</span><span class="sxs-lookup"><span data-stu-id="12eda-108">Static text ends with a colon.</span></span>

![Screenshot mit dem Dialogfeld "ausführen"](images/fb0bd076-e9f9-4260-a54a-9d7db93157da.jpg)

<span data-ttu-id="12eda-110">Es gibt zwei Arten von Kontrollen:</span><span class="sxs-lookup"><span data-stu-id="12eda-110">There are two types of controls:</span></span>

-   <span data-ttu-id="12eda-111">Steuerelemente, die über Beschriftungen als Eigenschaft dieses Steuer Elements verfügen, z. b. Befehls Schaltflächen und Kontrollkästchen.</span><span class="sxs-lookup"><span data-stu-id="12eda-111">Controls that have their captions as a property of that control, such as command buttons and check boxes.</span></span> <span data-ttu-id="12eda-112">Barrierefreiheits Hilfen haben keine Probleme, diese Steuerelemente zu identifizieren, solange die Beschriftung ordnungsgemäß definiert ist.</span><span class="sxs-lookup"><span data-stu-id="12eda-112">Accessibility aids have no trouble identifying these controls as long as the caption is properly defined.</span></span>
-   <span data-ttu-id="12eda-113">Steuerelemente, die nicht über eigene Beschriftungen verfügen (z. b. Bearbeitungs Steuerelemente, Listenfelder und Listenansichten), müssen mithilfe separater statischer Text Steuerelemente beschriftet werden.</span><span class="sxs-lookup"><span data-stu-id="12eda-113">Controls that do not have their own captions, such as edit controls, list boxes and list views, must be labeled by using separate static text controls.</span></span> <span data-ttu-id="12eda-114">Weitere Informationen zu Steuerelementen, die über keine eigenen Beschriftungen verfügen, finden Sie unter Steuer [Elemente ohne Beschriftungs Eigenschaften](controls-without-caption-properties.md).</span><span class="sxs-lookup"><span data-stu-id="12eda-114">For more information about controls that do not have their own captions, see [Controls Without Caption Properties](controls-without-caption-properties.md).</span></span>

<span data-ttu-id="12eda-115">Es können mehrere Techniken verwendet werden, um Situationen zu überwinden, in denen Steuerelemente nicht über eigene Beschriftungen verfügen, aber nur für Windows wirksam sind, die vom Standard Dialog-Manager (SDM) angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="12eda-115">Several techniques can be used to overcome situations in which controls do not have their own captions, but they are only effective for windows that are displayed by the Standard Dialog Manager (SDM).</span></span> <span data-ttu-id="12eda-116">Alle anderen Fenster müssen die Namen und Beziehungen zwischen Steuerelementen verfügbar machen, indem Microsoft Active Accessibility explizit unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="12eda-116">All other windows need to expose the names and relationship between controls by explicitly supporting Microsoft Active Accessibility.</span></span> <span data-ttu-id="12eda-117">Weitere Informationen zu Active Accessibility finden Sie im Abschnitt zur [Barrierefreiheit](/windows/desktop/accessibility) in der MSDN Library.</span><span class="sxs-lookup"><span data-stu-id="12eda-117">For more information about Active Accessibility, see the [Accessibility](/windows/desktop/accessibility) section of the MSDN Library.</span></span>

 

 
