---
description: Eine Anwendung navigiert die Elementstruktur eines Windows-Abbild Erwerbs (WIA), um Abbilder auf diesem Gerät zu suchen und auszuwählen. Mit dieser Technik wählt eine Anwendung ein Bild aus und ruft ein Bild ab, ohne dem Benutzer ein Dialogfeld zu präsentieren.
ms.assetid: 1f124b4a-45fb-4181-b45a-e810a61ac37d
title: Navigieren in einer Elementstruktur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 787ff3b53690ae7db4ff69fd5de2f4f4186f8e43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526432"
---
# <a name="navigating-an-item-tree"></a><span data-ttu-id="ec08e-104">Navigieren in einer Elementstruktur</span><span class="sxs-lookup"><span data-stu-id="ec08e-104">Navigating an Item Tree</span></span>

<span data-ttu-id="ec08e-105">Eine Anwendung navigiert die Elementstruktur eines Windows-Abbild Erwerbs (WIA), um Abbilder auf diesem Gerät zu suchen und auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="ec08e-105">An application navigates a Windows Image Acquisition (WIA) device's item tree to find and select images on that device.</span></span> <span data-ttu-id="ec08e-106">Mit dieser Technik wählt eine Anwendung ein Bild aus und ruft ein Bild ab, ohne dem Benutzer ein Dialogfeld zu präsentieren.</span><span class="sxs-lookup"><span data-stu-id="ec08e-106">Using this technique, an application selects and acquires an image without presenting a dialog box to the user.</span></span>

<span data-ttu-id="ec08e-107">Ein WIA-Gerät wird als Stamm Element in einer Struktur von [**iwiaitem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) -oder [**IWiaItem2**](-wia-iwiaitem2.md) -Objekten dargestellt.</span><span class="sxs-lookup"><span data-stu-id="ec08e-107">A WIA device is represented as the root item in a tree of [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) or [**IWiaItem2**](-wia-iwiaitem2.md) objects.</span></span> <span data-ttu-id="ec08e-108">Die untergeordneten Elemente in der Struktur stellen Bilder für eine Kamera oder Scan Betten für einen Scanner dar.</span><span class="sxs-lookup"><span data-stu-id="ec08e-108">The child items in the tree represent images for a camera or scan beds for a scanner.</span></span>

<span data-ttu-id="ec08e-109">Nach dem Auswählen eines WIA-Geräts wird von einer Anwendung die [**iwiaitem:: enumchilditems**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumchilditems) -Methode der [**iwiaitem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) -oder [**IWiaItem2**](-wia-iwiaitem2.md) -Schnittstelle des Geräts aufgerufen, um die untergeordneten Elemente (die Bilder oder Scan Betten) des Geräts aufzuzählen.</span><span class="sxs-lookup"><span data-stu-id="ec08e-109">After a WIA device is selected, an application calls the [**IWiaItem::EnumChildItems**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumchilditems) method of the [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) or [**IWiaItem2**](-wia-iwiaitem2.md) interface of the device to enumerate the child items (the images or scan beds) of the device.</span></span> <span data-ttu-id="ec08e-110">Anweisungen hierzu finden Sie unter [Auswählen eines Geräts](-wia-selecting-a-device.md).</span><span class="sxs-lookup"><span data-stu-id="ec08e-110">For instructions, see [Selecting a Device](-wia-selecting-a-device.md).</span></span>

<span data-ttu-id="ec08e-111">Die [**iwiaitem:: enumchilditems**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumchilditems) -Methode erstellt ein Enumerationsobjekt für die untergeordneten Elemente des Geräts und gibt einen Zeiger auf die [**ienumwiaitem**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwiaitem) -Schnittstelle dieses Objekts zurück.</span><span class="sxs-lookup"><span data-stu-id="ec08e-111">The [**IWiaItem::EnumChildItems**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumchilditems) method creates an enumeration object for the child items of the device, and returns a pointer to that object's [**IEnumWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwiaitem) interface.</span></span> <span data-ttu-id="ec08e-112">Die Anwendung kann dann die Methoden der **ienumwiaitem** -Schnittstelle verwenden, um Zeiger auf die Elemente in der Elementstruktur des Geräts zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="ec08e-112">The application can then use the methods of the **IEnumWiaItem** interface to obtain pointers to the items in the device's item tree.</span></span>

 

 



