---
description: 'Eine weitere Option zum Hinzufügen von Verben zu einem kaskadierenden Menü ist die Verwendung von IExplorerCommand:: enumsubcommands.'
ms.assetid: 010157F3-B950-4A57-B0AA-248B4990DA34
title: Erstellen von kaskadierenden Menüs mit der IExplorerCommand-Schnittstelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5afb88a7ac04857ac64e79115a4e8984d325e47b
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/28/2021
ms.locfileid: "104570967"
---
# <a name="how-to-create-cascading-menus-with-the-iexplorercommand-interface"></a><span data-ttu-id="32969-103">Erstellen von kaskadierenden Menüs mit der IExplorerCommand-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="32969-103">How to Create Cascading Menus with the IExplorerCommand Interface</span></span>

<span data-ttu-id="32969-104">Eine weitere Option zum Hinzufügen von Verben zu einem kaskadierenden Menü ist die Verwendung von [**IExplorerCommand:: enumsubcommands**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-enumsubcommands).</span><span class="sxs-lookup"><span data-stu-id="32969-104">Another option for adding verbs to a cascading menu is through [**IExplorerCommand::EnumSubCommands**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-enumsubcommands).</span></span> <span data-ttu-id="32969-105">Diese Methode ermöglicht Datenquellen, die ihre Befehls Modul Befehle über die [**IExplorerCommandProvider**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandprovider) -Schnittstelle bereitstellen, diese Befehle als Verben in einem Kontextmenü zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="32969-105">This method enables data sources that provide their command module commands through the [**IExplorerCommandProvider**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandprovider) interface to use those commands as verbs on a shortcut menu.</span></span> <span data-ttu-id="32969-106">In Windows 7 und höher können Sie die gleiche Verb Implementierung mithilfe der [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) -Schnittstelle bereitstellen, wie Sie es mit der [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) -Schnittstelle erreichen können.</span><span class="sxs-lookup"><span data-stu-id="32969-106">In Windows 7 and later, you can provide the same verb implementation using the [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) interface as you can with the [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) interface.</span></span>

## <a name="instructions"></a><span data-ttu-id="32969-107">Instructions</span><span class="sxs-lookup"><span data-stu-id="32969-107">Instructions</span></span>


<span data-ttu-id="32969-108">Die folgenden beiden Screenshots veranschaulichen die Verwendung von kaskadierenden Menüs im Ordner " **Geräte** ".</span><span class="sxs-lookup"><span data-stu-id="32969-108">The following two screen shots illustrate the use of cascading menus in the **Devices** folder.</span></span>

![Screenshot, der ein Beispiel für ein kaskadieres Menü im Geräte Ordner anzeigt.](images/file-assoc/filecascademenu.png)

![Screenshot mit einem Beispiel für ein kaskadieres Menü im Geräte Ordner](images/file-assoc/cascadedevices2.png)

## <a name="remarks"></a><span data-ttu-id="32969-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="32969-111">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="32969-112">Da [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) nur die Prozess interne Aktivierung unterstützt, empfiehlt es sich, von shelldatenquellen zu verwenden, die die Implementierung zwischen Befehlen und Kontextmenüs freigeben müssen.</span><span class="sxs-lookup"><span data-stu-id="32969-112">Because [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) supports in-process activation only, it is recommended for use by Shell data sources that need to share the implementation between commands and shortcut menus.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="32969-113">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="32969-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="32969-114">**IExplorerCommand**</span><span class="sxs-lookup"><span data-stu-id="32969-114">**IExplorerCommand**</span></span>](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand)
</dt> <dt>

[<span data-ttu-id="32969-115">**IExplorerCommandProvider**</span><span class="sxs-lookup"><span data-stu-id="32969-115">**IExplorerCommandProvider**</span></span>](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandprovider)
</dt> <dt>

[<span data-ttu-id="32969-116">**IContextMenu**</span><span class="sxs-lookup"><span data-stu-id="32969-116">**IContextMenu**</span></span>](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu)
</dt> </dl>

 

 
