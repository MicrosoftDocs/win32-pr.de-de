---
description: Verwenden von von einem Besitzer gezeichneten Menüs zur Unterstützung der sprach Funktionalität für den Tablet PC.
ms.assetid: fbe2d420-f667-416b-bff3-0fee9ae22203
title: Verwenden von Owner-Drawn Menüs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42f16f9328fadfedccee2c730678fc4cd2d8ab3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751272"
---
# <a name="using-owner-drawn-menus"></a><span data-ttu-id="4499f-103">Verwenden von Owner-Drawn Menüs</span><span class="sxs-lookup"><span data-stu-id="4499f-103">Using Owner-Drawn Menus</span></span>

<span data-ttu-id="4499f-104">Wenn Sie von einem Besitzer gezeichnete Menüs verwenden, müssen Sie die Menü Namen zur Unterstützung der sprach Funktionalität zur Verfügung stellen.</span><span class="sxs-lookup"><span data-stu-id="4499f-104">When using owner-drawn menus, you must make the menu names available to support speech functionality.</span></span> <span data-ttu-id="4499f-105">Hierfür gibt es zwei Möglichkeiten:</span><span class="sxs-lookup"><span data-stu-id="4499f-105">There are two ways to do this:</span></span>

-   <span data-ttu-id="4499f-106">Machen Sie den Menü Elementnamen mithilfe der msaamenuinfo-Struktur verfügbar.</span><span class="sxs-lookup"><span data-stu-id="4499f-106">Expose the menu item name by using the MSAAMENUINFO structure.</span></span>
-   <span data-ttu-id="4499f-107">Stellen Sie eine Option bereit, um grafische Menüs durch Standard Textmenüs zu ersetzen, wenn eine Barrierefreiheits Hilfe aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="4499f-107">Provide an option to replace graphic menus with standard text menus when an accessibility aid is active.</span></span> <span data-ttu-id="4499f-108">Wenn die [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) -Funktion " **true** " zurückgibt, wobei der *uiaction* -Parameter auf SPI \_ getscreenreader festgelegt ist, verwenden Sie Standardmenüs. Die Anwendung sollte die WM \_ settingschange-Nachricht überwachen und reagieren, indem Sie den Status dieser Option Abfragen und die Anzeige entsprechend anpassen.</span><span class="sxs-lookup"><span data-stu-id="4499f-108">If the [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) function returns **TRUE** with its *uiAction* parameter set to SPI\_GETSCREENREADER, use standard menus.The application should watch for the WM\_SETTINGSCHANGE message and respond by querying the state of this option and adjusting its display appropriately.</span></span> <span data-ttu-id="4499f-109">Microsoft Visual Studio bietet z. b. eine Option, mit der Standardmenüs anstelle der benutzerdefinierten Menüs verwendet werden, die standardmäßig angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="4499f-109">For example, Microsoft Visual Studio provides an option to use standard menus instead of the custom menus that are displayed by default.</span></span>

 

 
