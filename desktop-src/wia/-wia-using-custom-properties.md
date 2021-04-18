---
description: Verwenden von benutzerdefinierten Eigenschaften.
ms.assetid: 09b30c95-0ce2-401c-a4ae-99c801a2048a
title: Verwenden von benutzerdefinierten Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eca9f8092afa5b8af22080b154fff79a32a6f304
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345074"
---
# <a name="using-custom-properties"></a><span data-ttu-id="0f095-103">Verwenden von benutzerdefinierten Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0f095-103">Using Custom Properties</span></span>

<span data-ttu-id="0f095-104">**Verwenden von benutzerdefinierten Eigenschaften**.</span><span class="sxs-lookup"><span data-stu-id="0f095-104">**Using Custom Properties**.</span></span>

<span data-ttu-id="0f095-105">Ein Windows-Abbild Erfassungs Treiber (WIA) kann seine eigenen benutzerdefinierten Eigenschaften definieren.</span><span class="sxs-lookup"><span data-stu-id="0f095-105">A Windows Image Acquisition (WIA) driver can define its own custom properties.</span></span> <span data-ttu-id="0f095-106">Aufrufer können benutzerdefinierte Eigenschaften genau wie normale WIA-Eigenschaften bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="0f095-106">Callers can manipulate custom properties just as they would normal WIA properties.</span></span> <span data-ttu-id="0f095-107">Allerdings kann nur Ihre Anwendung oder Ihr benutzerdefiniertes UI-Modul auf diese benutzerdefinierten Eigenschaften zugreifen.</span><span class="sxs-lookup"><span data-stu-id="0f095-107">However, only your application or custom UI module can access these custom properties.</span></span>

<span data-ttu-id="0f095-108">WIA-Treiber sollten die benutzerdefinierten Eigenschaften definieren, damit Eigenschaften Bezeichner vorhanden sind, die von WIA \_ private \_ devprop für Geräteeigenschaften versetzt werden, und \_ \_ für normale Element Eigenschaften, z. b. in [iwiaminidrv::d rvinititemproperties](https://msdn.microsoft.com/library/ms794131.aspx), eine private ItemProp-Eigenschaft verwenden.</span><span class="sxs-lookup"><span data-stu-id="0f095-108">WIA drivers should define the custom properties to have property identifiers that are offset by WIA\_PRIVATE\_DEVPROP for device properties, and use WIA\_PRIVATE\_ITEMPROP for normal item properties, such as inside [IWiaMiniDrv::drvInitItemProperties](https://msdn.microsoft.com/library/ms794131.aspx).</span></span> <span data-ttu-id="0f095-109">Weitere Informationen finden Sie unter [Definieren von benutzerdefinierten Eigenschaften](-wia-defining-custom-properties.md).</span><span class="sxs-lookup"><span data-stu-id="0f095-109">For more information, see [Defining Custom Properties](-wia-defining-custom-properties.md).</span></span>

<span data-ttu-id="0f095-110">Es gibt zwei Möglichkeiten, benutzerdefinierte Parameter an WIA-Treiber zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="0f095-110">There are two ways to pass custom parameters to WIA drivers.</span></span>

<span data-ttu-id="0f095-111">Die erste Option ist die Verwendung der **iwiaitemextras:: Escape** -Methode (beschrieben in der Platform SDK-Dokumentation).</span><span class="sxs-lookup"><span data-stu-id="0f095-111">The first option is to use the **IWiaItemExtras::Escape** method (described in the Platform SDK documentation).</span></span> <span data-ttu-id="0f095-112">Dies ähnelt der [istiusd:: Escape-](https://msdn.microsoft.com/library/ms794396.aspx) Methode, lässt jedoch zu, dass Aufrufer WIA direkt anstelle der Verwendung von "STI"-Methoden verwenden können.</span><span class="sxs-lookup"><span data-stu-id="0f095-112">This is similar to the [IStiUSD::Escape](https://msdn.microsoft.com/library/ms794396.aspx) method, but it allows callers to use WIA directly, instead of using STI methods.</span></span> <span data-ttu-id="0f095-113">Mithilfe von **iwiaitemextras:: Escape** können Sie alle Informationen an den Treiber übergeben, und der Treiber kann alle Informationen zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="0f095-113">Using **IWiaItemExtras::Escape**, you can pass any information to the driver, and the driver can pass any information back.</span></span> <span data-ttu-id="0f095-114">Der WIA-Dienst verwaltet nur die Puffer, die zwischen dem Aufrufer und dem Treiber übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="0f095-114">The WIA service manages only those buffers passed between the caller and the driver.</span></span>

<span data-ttu-id="0f095-115">Die zweite Option besteht darin, benutzerdefinierte Eigenschaften zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="0f095-115">The second option is to use custom properties.</span></span> <span data-ttu-id="0f095-116">Die Verwendung der **iwiaitemextras:: Escape** -Methode ist flexibler als die Verwendung benutzerdefinierter WIA-Eigenschaften, aber benutzerdefinierte WIA-Eigenschaften ermöglichen es Ihnen, Informationen im Eigenschaftenstream des Elements zu speichern, damit der Treiber die Informationen zu einem anderen Zeitpunkt lesen kann.</span><span class="sxs-lookup"><span data-stu-id="0f095-116">Using the **IWiaItemExtras::Escape** method is more flexible than using custom WIA properties, but custom WIA properties allow you to store information in the item's property stream so that the driver can read the information at another time.</span></span>

 

 



