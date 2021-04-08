---
title: Iaccessibilitydockingservice getavailablesize-Methode
description: Ruft die Dimensionen ab, die zum Andocken eines Barrierefreiheits Fensters eines Monitors verfügbar sind.
ms.assetid: 1C838B01-EF26-4FCC-878F-A36DEFBA3142
keywords:
- Getavailablesize-Methode com
- Getavailablesize-Methode com, iaccessibilitydockingservice-Schnittstelle
- Iaccessibilitydockingservice-Schnittstelle com, getavailablesize-Methode
topic_type:
- apiref
api_name:
- IAccessibilityDockingService.GetAvailableSize
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e1b9f113792b14f5fb86e0349d083ea48ffdb3fd
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104037930"
---
# <a name="iaccessibilitydockingservicegetavailablesize-method"></a>Iaccessibilitydockingservice:: getavailablesize-Methode

Ruft die Dimensionen ab, die zum Andocken eines Barrierefreiheits Fensters eines Monitors verfügbar sind.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetAvailableSize(
  [in]  HMONITOR hMonitor,
  [out] UINT     *puMaxHeight,
  [out] UINT     *puFixedWidth
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Hmonitor* \[ in\]
</dt> <dd>

Gibt den Monitor an, für den die verfügbare Docking Größe abgerufen wird.

</dd> <dt>

*pumaxheight* \[ vorgenommen\]
</dt> <dd>

Legen Sie bei Erfolg auf die maximale Höhe fest, die für das Andocken auf dem angegebenen *Hmonitor* in Pixel verfügbar ist.

Bei einem Fehler wird auf 0 (null) festgelegt.

</dd> <dt>

*pufixedwidth* \[ vorgenommen\]
</dt> <dd>

Legen Sie bei Erfolg auf die festgelegte Breite fest, die für das Andocken auf dem angegebenen *Hmonitor* in Pixel verfügbar ist. Jedes Fenster, das an diesen *Hmonitor* angedockt ist, wird auf diese Breite vergrößert.

Bei einem Fehler wird auf 0 (null) festgelegt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert



| Rückgabecode                                                                                                                          | Beschreibung                                                                      |
|--------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                                                 | Erfolg.<br/>                                                              |
| <dl> <dt>**HRESULT \_ von \_ Win32 (Fehler \_ ungültiges \_ Monitor \_ handle)**</dt> </dl> | Der vom Monitor handle angegebene Monitor unterstützt das Andocken nicht.<br/> |



 

Wenn entweder *pumaxheight* oder *pufixedwidth* NULL ist, tritt eine Zugriffsverletzung auf.

## <a name="remarks"></a>Bemerkungen

Barrierefreiheits Fenster können nur an einen Monitor angedockt werden, der mindestens 768 vertikale Bildschirm Pixel aufweist. Diese API lässt nicht zu, dass solche Fenster mit einer Höhe angedockt werden, die dazu führt, dass Windows Store-Apps weniger als 768 vertikale Bildschirm Pixel aufweisen.

## <a name="examples"></a>Beispiele


```
IAccessibilityDockingService *pDockingService;
HRESULT hr = CoCreateInstance(CLSID_AccessibilityDockingService, CLSCTX_INPROV_SERVER, nullptr, IID_PPV_ARGS(&pDockingService));
if (SUCCEEDED(hr))
{
    UINT uMaxHeight;
    UINT uFixedWidth;

    HMONITOR hMonitor = MonitorFromWindow(_hwndMyApplication, MONITOR_DEFAULTTONULL);
    if (hMonitor != nullptr)
    {
        hr = pDockingService->GetAvailableSize(hMonitor, &uMaxHeight, &uFixedWidth);
    }
}
```



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Iaccessibilitydockingservice**](/windows/desktop/api/shobjidl/nn-shobjidl-iaccessibilitydockingservice)
</dt> </dl>

 

 





