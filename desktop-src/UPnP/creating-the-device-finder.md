---
title: Erstellen des Geräte finders
description: Die folgenden Beispiele veranschaulichen das Erstellen einer Instanz des Device Finder-Objekts in C++, Visual Basic und VBScript.
ms.assetid: 0084a64d-458e-471c-a6be-aeb6ed0962d0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc6af75ea5c267e156f89f1ae1e27a08928c097bbfea731f59add575397fbc00
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119137356"
---
# <a name="creating-the-device-finder"></a>Erstellen des Geräte finders

Die folgenden Beispiele veranschaulichen das Erstellen einer Instanz des Device Finder-Objekts in C++, Visual Basic und VBScript. Die Skriptsprachen verwenden die programmgesteuerte ID (ProgID) [**UPnP.UPnPDeviceFrau,**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder) um die Device Finder-Klasse zu identifizieren. Der C++-Code verwendet den Klassenbezeichner.

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



Wie in diesem C++-Beispiel angegeben, macht das Device Finder-Objekt die Standardschnittstelle [**IUPnPDevice Genauso verfügbar.**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder) Die Methoden dieser Schnittstelle führen Suchvorgänge gemäß den gültigen Suchkriterien für ein UPnP-basiertes Gerät durch. Diese Schnittstelle ist automatisierungsfähig, sodass ihre Methoden durch Skriptcode aufgerufen werden können.

## <a name="vbscript-example"></a>VBScript-Beispiel


```VB
Dim deviceFinder

Set deviceFinder = CreateObject( "UPnP.UPnPDeviceFinder" )
```



 

 




