---
title: IWMDRMDeviceApp2-Schnittstelle
description: Die IWMDRMDeviceApp2-Schnittstelle erweitert iwmdrmdeviceapp durch Bereitstellen einer neuen Version der querydevicestatus-Methode.
ms.assetid: a7e28d5a-041f-4102-97db-0c77ca146e26
keywords:
- IWMDRMDeviceApp2 Interface Windows Media Device Manager
- IWMDRMDeviceApp2 Interface Windows Media Device Manager, beschrieben
topic_type:
- apiref
api_name:
- IWMDRMDeviceApp2
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: df4bfdb023198631b16ffa0e511488fa52423c5e
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104313134"
---
# <a name="iwmdrmdeviceapp2-interface"></a>IWMDRMDeviceApp2-Schnittstelle

Die **IWMDRMDeviceApp2** -Schnittstelle erweitert [**iwmdrmdeviceapp**](iwmdrmdeviceapp.md) durch Bereitstellen einer neuen Version der [**querydevicestatus**](iwmdrmdeviceapp-querydevicestatus.md) -Methode. **QueryDeviceStatus2** ermöglicht dem Aufrufer, eine bestimmte DRM-Anforderung abzufragen.

Um diese Schnittstelle zu erhalten, müssen Sie **cokreateinstance** aufrufen und CLSID \_ wmdrmdeviceapp übergeben.

> [!Note]  
> Diese Schnittstelle ist in der Header Datei definiert, die aus wmdrmdeviceapp. idl erstellt wurde. Dieser Header **\# enthält** "WMDM. h". Möglicherweise müssen Sie diesen Dateinamen ändern, damit er mit dem aus WMDM. idl erstellten Header identisch ist.

 

## <a name="members"></a>Member

Die **IWMDRMDeviceApp2** -Schnittstelle erbt von [**iwmdrmdeviceapp**](iwmdrmdeviceapp.md). **IWMDRMDeviceApp2** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IWMDRMDeviceApp2** -Schnittstelle verfügt über diese Methoden.



| Methode                                                            | BESCHREIBUNG                                                          |
|:------------------------------------------------------------------|:---------------------------------------------------------------------|
| [**QueryDeviceStatus2**](iwmdrmdeviceapp2-querydevicestatus2.md) | Fragt ein Gerät nach einem bestimmten DRM-Status oder einer bestimmten Funktion ab.<br/> |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iwmdrmdeviceapp**](iwmdrmdeviceapp.md)
</dt> <dt>

[**Behandeln geschützter Inhalte in der Anwendung**](handling-protected-content-in-the-application.md)
</dt> <dt>

[**Schnittstellen für Anwendungen**](interfaces-for-applications.md)
</dt> <dt>

[**Verwendung von Messungs Inhalten**](metering-content-usage.md)
</dt> </dl>

 

 





