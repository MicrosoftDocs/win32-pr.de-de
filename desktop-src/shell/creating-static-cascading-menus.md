---
description: Ab Windows 7 werden Cascading-Menüs über den Registrierungs Eintrag Unterbefehle, den extendedsubcommandskey-Registrierungs Eintrag oder die IExplorerCommand-Schnittstelle erstellt.
title: Erstellen von statischen kaskadierenden Menüs
ms.topic: article
ms.date: 05/31/2018
ms.assetid: E3A6F174-BE53-48EF-AE9B-A3F297E91B95
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: d812b4d3d2fb0754002cb37d72718e4fe861ce15
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104569035"
---
# <a name="creating-static-cascading-menus"></a><span data-ttu-id="924b7-103">Erstellen von statischen kaskadierenden Menüs</span><span class="sxs-lookup"><span data-stu-id="924b7-103">Creating Static Cascading Menus</span></span>

<span data-ttu-id="924b7-104">In Windows 7 und höher wird die Cascading-Menü Implementierung durch Registrierungs Einstellungen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="924b7-104">In Windows 7 and later, cascading menu implementation is supported through registry settings.</span></span> <span data-ttu-id="924b7-105">Vor Windows 7 war die Erstellung von kaskadierenden Menüs nur durch die Implementierung der [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) -Schnittstelle möglich.</span><span class="sxs-lookup"><span data-stu-id="924b7-105">Prior to Windows 7, the creation of cascading menus was possible only through the implementation of the [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) interface.</span></span> <span data-ttu-id="924b7-106">In Windows 7 und höher sollten Sie nur auf Component Object Model Code basierte Lösungen (com) zugreifen, wenn die statischen Methoden nicht ausreichen.</span><span class="sxs-lookup"><span data-stu-id="924b7-106">In Windows 7 and later, you should resort to Component Object Model (COM) code-based solutions only when the static methods are insufficient.</span></span>

<span data-ttu-id="924b7-107">Der folgende Screenshot zeigt ein Beispiel für ein Cascading-Menü.</span><span class="sxs-lookup"><span data-stu-id="924b7-107">The following screen shot provides an example of a cascading menu.</span></span>

![Screenshot mit einem Beispiel für ein Cascading-Menü](images/file-assoc/filecascademenu2ndex.png)

<span data-ttu-id="924b7-109">In Windows 7 und höher gibt es drei Möglichkeiten, Kaskadierende Menüs zu erstellen, die in den folgenden Abschnitten beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="924b7-109">In Windows 7 and later, there are three ways to create cascading menus, which are described in the following sections.</span></span>

-   [<span data-ttu-id="924b7-110">Erstellen von kaskadierenden Menüs mit dem Registrierungs Eintrag "Unterbefehle"</span><span class="sxs-lookup"><span data-stu-id="924b7-110">How to Create Cascading Menus with the SubCommands Registry Entry</span></span>](how-to--create-cascading-menus-with-the-subcommands-registry-entry.md)
-   [<span data-ttu-id="924b7-111">Erstellen von kaskadierenden Menüs mit dem Registrierungs Eintrag "extendedsubcommandskey"</span><span class="sxs-lookup"><span data-stu-id="924b7-111">How to Create Cascading Menus with the ExtendedSubCommandsKey Registry Entry</span></span>](how-to-create-cascading-menus-with-the-extendedsubcommandskey-registry-entry.md)
-   [<span data-ttu-id="924b7-112">Erstellen von kaskadierenden Menüs mit der IExplorerCommand-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="924b7-112">How to Create Cascading Menus with the IExplorerCommand Interface</span></span>](how-to-create-cascading-menus-with-the-iexplorercommand-interface.md)

 

 
