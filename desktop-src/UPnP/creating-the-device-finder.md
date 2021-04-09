---
title: Erstellen des Geräte Suchgeräts
description: In den folgenden Beispielen wird veranschaulicht, wie eine Instanz des Device Finder-Objekts in C++, Visual Basic und VBScript erstellt wird.
ms.assetid: 0084a64d-458e-471c-a6be-aeb6ed0962d0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3a12fc7e269f2c0ce5b577fe2f49b6d13fe3b5a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856647"
---
# <a name="creating-the-device-finder"></a><span data-ttu-id="45ac2-103">Erstellen des Geräte Suchgeräts</span><span class="sxs-lookup"><span data-stu-id="45ac2-103">Creating the Device Finder</span></span>

<span data-ttu-id="45ac2-104">In den folgenden Beispielen wird veranschaulicht, wie eine Instanz des Device Finder-Objekts in C++, Visual Basic und VBScript erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="45ac2-104">The following examples demonstrate how to create an instance of the Device Finder object in C++, Visual Basic, and VBScript.</span></span> <span data-ttu-id="45ac2-105">Die Skriptsprachen verwenden die programmgesteuerte ID (ProgID) [**UPnP. upnpdevicefinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder) , um die Geräte Such Klasse zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="45ac2-105">The script languages use the programmatic ID (ProgID) [**UPnP.UPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder) to identify the Device Finder class.</span></span> <span data-ttu-id="45ac2-106">Der C++-Code verwendet den Klassen Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="45ac2-106">The C++ code uses the class identifier.</span></span>

## <a name="c-example"></a><span data-ttu-id="45ac2-107">C++-Beispiel</span><span class="sxs-lookup"><span data-stu-id="45ac2-107">C++ Example</span></span>


```C++
HRESULT hr = S_OK;
IUPnPDeviceFinder *pDeviceFinder = NULL;

hr = CoCreateInstance(CLSID_UPnPDeviceFinder, 
                      NULL,
                      CLSCTX_INPROC_SERVER,
                      IID_IUPnPDeviceFinder,
                      (void **) &pDeviceFinder);
```



<span data-ttu-id="45ac2-108">Wie dieses C++-Beispiel zeigt, macht das Device Finder-Objekt eine Standardschnittstelle ( [**IUPnPDeviceFinder) verfügbar**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder).</span><span class="sxs-lookup"><span data-stu-id="45ac2-108">As this C++ example indicates, the Device Finder object exposes a default interface, [**IUPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder).</span></span> <span data-ttu-id="45ac2-109">Mit den Methoden dieser Schnittstelle werden Suchvorgänge gemäß den gültigen Suchkriterien für ein UPnP-basiertes Gerät durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="45ac2-109">The methods of this interface perform searches according to the valid search criteria for a UPnP-based device.</span></span> <span data-ttu-id="45ac2-110">Diese Schnittstelle ist Automatisierungs fähig, sodass Ihre Methoden von Skriptcode aufgerufen werden können.</span><span class="sxs-lookup"><span data-stu-id="45ac2-110">This interface is Automation capable, so its methods can be called by scripting code.</span></span>

## <a name="vbscript-example"></a><span data-ttu-id="45ac2-111">VBScript-Beispiel</span><span class="sxs-lookup"><span data-stu-id="45ac2-111">VBScript Example</span></span>


```VB
Dim deviceFinder

Set deviceFinder = CreateObject( "UPnP.UPnPDeviceFinder" )
```



 

 




