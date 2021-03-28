---
description: Um dem Untermenü Programme ein Element hinzuzufügen, führen Sie die folgenden Schritte aus.
ms.assetid: F8793C33-2281-4E4A-9659-4189E1C8279A
title: Vorgehensweise beim Hinzufügen von Verknüpfungen zum Startmenü
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77ee942e07c48ed7addf07160412008bfb5b9322
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131629"
---
# <a name="how-to-add-shortcuts-to-the-start-menu"></a><span data-ttu-id="a5831-103">Vorgehensweise beim Hinzufügen von Verknüpfungen zum Startmenü</span><span class="sxs-lookup"><span data-stu-id="a5831-103">How to Add Shortcuts to the Start Menu</span></span>

<span data-ttu-id="a5831-104">Um dem Untermenü **Programme** ein Element hinzuzufügen, führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="a5831-104">To add an item to the **Programs** submenu, follow these steps.</span></span>

## <a name="instructions"></a><span data-ttu-id="a5831-105">Instructions</span><span class="sxs-lookup"><span data-stu-id="a5831-105">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="a5831-106">Schritt 1:</span><span class="sxs-lookup"><span data-stu-id="a5831-106">Step 1:</span></span>

<span data-ttu-id="a5831-107">Erstellen Sie eine [Shellverknüpfung](./links.md) mithilfe der [**IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="a5831-107">Create a [shell link](./links.md) by using the [**IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) interface.</span></span>

### <a name="step-2"></a><span data-ttu-id="a5831-108">Schritt 2:</span><span class="sxs-lookup"><span data-stu-id="a5831-108">Step 2:</span></span>

<span data-ttu-id="a5831-109">Rufen Sie den Speicherort des Ordners "Programme" mithilfe der Funktion " [**shgetknownfolderpath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath) " ab, und übergeben Sie [**folderid- \_ Programme**](knownfolderid.md).</span><span class="sxs-lookup"><span data-stu-id="a5831-109">Obtain the location of the Programs folder by using the [**SHGetKnownFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath) function, passing [**FOLDERID\_Programs**](knownfolderid.md).</span></span>

### <a name="step-3"></a><span data-ttu-id="a5831-110">Schritt 3:</span><span class="sxs-lookup"><span data-stu-id="a5831-110">Step 3:</span></span>

<span data-ttu-id="a5831-111">Fügen Sie den shelllink zum Ordner Programme hinzu.</span><span class="sxs-lookup"><span data-stu-id="a5831-111">Add the Shell link to the Programs folder.</span></span> <span data-ttu-id="a5831-112">Sie können auch einen Ordner im Ordner Programme erstellen und diesem Ordner den Link hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="a5831-112">You can also create a folder in the Programs folder and add the link to that folder.</span></span>

 

 
