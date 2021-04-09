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
# <a name="creating-the-device-finder"></a>Erstellen des Geräte Suchgeräts

In den folgenden Beispielen wird veranschaulicht, wie eine Instanz des Device Finder-Objekts in C++, Visual Basic und VBScript erstellt wird. Die Skriptsprachen verwenden die programmgesteuerte ID (ProgID) [**UPnP. upnpdevicefinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder) , um die Geräte Such Klasse zu identifizieren. Der C++-Code verwendet den Klassen Bezeichner.

## <a name="c-example"></a>C++-Beispiel


```C++
HRESULT hr = S_OK;
IUPnPDeviceFinder *pDeviceFinder = NULL;

hr = CoCreateInstance(CLSID_UPnPDeviceFinder, 
                      NULL,
                      CLSCTX_INPROC_SERVER,
                      IID_IUPnPDeviceFinder,
                      (void **) &pDeviceFinder);
```



Wie dieses C++-Beispiel zeigt, macht das Device Finder-Objekt eine Standardschnittstelle ( [**IUPnPDeviceFinder) verfügbar**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder). Mit den Methoden dieser Schnittstelle werden Suchvorgänge gemäß den gültigen Suchkriterien für ein UPnP-basiertes Gerät durchgeführt. Diese Schnittstelle ist Automatisierungs fähig, sodass Ihre Methoden von Skriptcode aufgerufen werden können.

## <a name="vbscript-example"></a>VBScript-Beispiel


```VB
Dim deviceFinder

Set deviceFinder = CreateObject( "UPnP.UPnPDeviceFinder" )
```



 

 




