---
description: 'Weitere Informationen finden Sie unter: Navigieren in einer Struktur von Element Objekten'
ms.assetid: e91f72c8-3ad6-49e8-88cc-aa99c13cd4c2
title: Navigieren in einer Struktur von Element Objekten
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 04e87444c2b9c473268c5e97dd9c26d04d95b93b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106354494"
---
# <a name="navigating-a-tree-of-item-objects"></a><span data-ttu-id="fd340-103">Navigieren in einer Struktur von Element Objekten</span><span class="sxs-lookup"><span data-stu-id="fd340-103">Navigating a Tree of Item Objects</span></span>

> [!Note]  
> <span data-ttu-id="fd340-104">Dieses Skript System wurde durch die Windows-Abbild Erwerbs-Automatisierungs Schicht (WIA) ersetzt.</span><span class="sxs-lookup"><span data-stu-id="fd340-104">This scripting system has been replaced with Windows Image Acquisition (WIA) Automation Layer.</span></span> <span data-ttu-id="fd340-105">Weitere Informationen finden Sie unter [Automatisierungs Schicht für Windows-Abbild](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage)</span><span class="sxs-lookup"><span data-stu-id="fd340-105">See [Windows Image Acquisition Automation Layer](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage).</span></span>

 

<span data-ttu-id="fd340-106">Eine Anwendung oder ein Skript navigiert von der Elementstruktur eines Windows-Abbild Erwerbs (WIA), um Images auf diesem Gerät zu suchen und auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="fd340-106">An application or script navigates a Windows Image Acquisition (WIA) device's item tree to find and select images on that device.</span></span> <span data-ttu-id="fd340-107">Mithilfe dieses Verfahrens wählt eine Anwendung ein Bild aus und ruft es ab, ohne ein Dialogfeld zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="fd340-107">Using this technique, an application selects and acquires an image without the use of a dialog box.</span></span>

<span data-ttu-id="fd340-108">Ein WIA-Gerät wird als Stamm Element in einer Struktur von [**Item**](-wia-item.md) -Objekten dargestellt.</span><span class="sxs-lookup"><span data-stu-id="fd340-108">A WIA device is represented as the root item in a tree of [**Item**](-wia-item.md) objects.</span></span> <span data-ttu-id="fd340-109">Die untergeordneten Elemente in der Struktur stellen Ordner und Bilder für eine Kamera oder Scan Betten für einen Scanner dar.</span><span class="sxs-lookup"><span data-stu-id="fd340-109">The child items in the tree represent folders and images for a camera or scan beds for a scanner.</span></span>

<span data-ttu-id="fd340-110">Nachdem Sie eine Verbindung mit einem Gerät hergestellt haben, rufen Sie die [**Children**](-wia-iwiadispatchitem-children.md) -Eigenschaft des [**Item**](-wia-item.md) -Objekts auf, das das Gerät darstellt (das Stamm Element der Struktur), um eine Auflistung der untergeordneten Elemente (die Bilder oder Scan Betten) des Geräts zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="fd340-110">After connecting to a device, call the [**Children**](-wia-iwiadispatchitem-children.md) property of the [**Item**](-wia-item.md) object that represents the device (the root item of the tree) to obtain a collection of the child items (the images or scan beds) of the device.</span></span>

<span data-ttu-id="fd340-111">Auflisten Sie diese Auflistung (bei Bedarf rekursiv), um die Elementstruktur zu navigieren.</span><span class="sxs-lookup"><span data-stu-id="fd340-111">Enumerate this collection (recursively, if necessary) to navigate item tree.</span></span>

 

 
