---
title: IWMDRMDeviceApp2-Schnittstelle
description: Die IWMDRMDeviceApp2-Schnittstelle erweitert IWMDRMDeviceApp um eine neue Version der QueryDeviceStatus-Methode.
ms.assetid: a7e28d5a-041f-4102-97db-0c77ca146e26
keywords:
- IWMDRMDeviceApp2-Schnittstelle windows Media Geräte-Manager
- IWMDRMDeviceApp2-Schnittstelle Windows Media Geräte-Manager , beschrieben
topic_type:
- apiref
api_name:
- IWMDRMDeviceApp2
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 17bd0d7aa729103a81fca6732ed178ac5ced583566dd353a28716d4933e602ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118584494"
---
# <a name="iwmdrmdeviceapp2-interface"></a>IWMDRMDeviceApp2-Schnittstelle

Die **IWMDRMDeviceApp2-Schnittstelle** erweitert [**IWMDRMDeviceApp**](iwmdrmdeviceapp.md) um eine neue Version der [**QueryDeviceStatus-Methode.**](iwmdrmdeviceapp-querydevicestatus.md) **Mit QueryDeviceStatus2** kann der Aufrufer eine bestimmte DRM-Anforderung abfragen.

Um diese Schnittstelle zu erhalten, rufen **Sie CoCreateInstance** auf, und übergeben Sie CLSID \_ WMDRMDeviceApp.

> [!Note]  
> Diese Schnittstelle wird in der Headerdatei definiert, die aus WMDRMDeviceApp.idl erstellt wurde. Dieser Header **\# enthält** "wmdm.h". Möglicherweise müssen Sie diesen Dateinamen ändern, damit er mit dem Header aus WMDM.idl übereinstimmen kann.

 

## <a name="members"></a>Member

Die **IWMDRMDeviceApp2-Schnittstelle** erbt von [**IWMDRMDeviceApp**](iwmdrmdeviceapp.md). **IWMDRMDeviceApp2** verfügt auch über diese Membertypen:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IWMDRMDeviceApp2-Schnittstelle** verfügt über diese Methoden.



| Methode                                                            | BESCHREIBUNG                                                          |
|:------------------------------------------------------------------|:---------------------------------------------------------------------|
| [**QueryDeviceStatus2**](iwmdrmdeviceapp2-querydevicestatus2.md) | Fragt ein Gerät nach einem bestimmten DRM-Status oder einer bestimmten Funktion ab.<br/> |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IWMDRMDeviceApp**](iwmdrmdeviceapp.md)
</dt> <dt>

[**Behandeln geschützter Inhalte in der Anwendung**](handling-protected-content-in-the-application.md)
</dt> <dt>

[**Schnittstellen für Anwendungen**](interfaces-for-applications.md)
</dt> <dt>

[**Nutzung von Messungsinhalten**](metering-content-usage.md)
</dt> </dl>

 

 





