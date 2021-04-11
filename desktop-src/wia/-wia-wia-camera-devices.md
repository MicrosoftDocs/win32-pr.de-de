---
description: WIA stellt ein Kamera Gerät als hierarchische Struktur von iwiaitem-Objekten dar.
ms.assetid: fbb2821c-7f13-4fdd-a2ea-582be303855a
title: WIA-Kamerageräte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 002a14d8e047019b1af2d2f86c1fd4a2e00d7808
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214643"
---
# <a name="wia-camera-devices"></a><span data-ttu-id="622f1-103">WIA-Kamerageräte</span><span class="sxs-lookup"><span data-stu-id="622f1-103">WIA Camera Devices</span></span>

<span data-ttu-id="622f1-104">WIA stellt ein Kamera Gerät als hierarchische Struktur von [**iwiaitem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) -Objekten dar.</span><span class="sxs-lookup"><span data-stu-id="622f1-104">WIA represents a camera device as a hierarchical tree of [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) objects.</span></span> <span data-ttu-id="622f1-105">Das Stamm Element, das von einem Aufrufen der Windows-Abbild Erfassungs Methode (WIA) Device Manager [**iwiadevmgr::**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-createdevice) up-Device-Methode zurückgegeben wird, wird zum Abrufen und Festlegen von Geräteinformationen, zum Steuern des Geräts und zum Starten der Geräte Element-Enumeration verwendet.</span><span class="sxs-lookup"><span data-stu-id="622f1-105">The root item, returned from a call to the Windows Image Acquisition (WIA) device manager [**IWiaDevMgr::CreateDevice**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-createdevice) method, is used to get and set device information, to control the device, and to begin device item enumeration.</span></span>

> [!Note]  
> <span data-ttu-id="622f1-106">WIA unterstützt keine Kameras in Windows Vista oder höher.</span><span class="sxs-lookup"><span data-stu-id="622f1-106">WIA does not support cameras in Windows Vista or later.</span></span> <span data-ttu-id="622f1-107">Verwenden Sie für diese Windows-Versionen die im Windows-Treiber Development Kit (DDK) beschriebene Windows-API für portable Geräte, um Images von Kameras abzurufen.</span><span class="sxs-lookup"><span data-stu-id="622f1-107">For those versions of the Windows, use the Windows Portable Device (WPD) API described in the Windows Driver Development Kit (DDK) to acquire images from cameras.</span></span>

 

<span data-ttu-id="622f1-108">Das folgende Diagramm veranschaulicht eine Beispiel Kamera Implementierung.</span><span class="sxs-lookup"><span data-stu-id="622f1-108">The following diagram illustrates a sample camera implementation.</span></span> <span data-ttu-id="622f1-109">Das Stamm Element der Kamera enthält drei untergeordnete Elemente, zwei Bilder und einen Ordner.</span><span class="sxs-lookup"><span data-stu-id="622f1-109">The camera root item has three child items, two pictures and one folder.</span></span> <span data-ttu-id="622f1-110">Der Ordner enthält zwei untergeordnete Elemente, beide Bilder.</span><span class="sxs-lookup"><span data-stu-id="622f1-110">The folder has two child items, both pictures.</span></span>

![Beispiel für eine Kamera Implementierung](images/wihierar.gif)

 

 



