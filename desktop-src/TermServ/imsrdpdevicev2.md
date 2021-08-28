---
title: IMsRdpDeviceV2-Schnittstelle
description: Enthält Informationen zu einem Geräteobjekt. Dies ist eine Erweiterung der IMsRdpDevice-Schnittstelle.
ms.assetid: 9a380a1a-d44f-4147-8917-bf1e07dbac15
ms.tgt_platform: multiple
keywords:
- IMsRdpDeviceV2-Schnittstelle Remotedesktopdienste
- IMsRdpDeviceV2-Schnittstelle Remotedesktopdienste beschrieben
topic_type:
- apiref
api_name:
- IMsRdpDeviceV2
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cca125024592851b260fb8e4c1f43c7621d4897fec0fc19dfc80d18278e09cf2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119000750"
---
# <a name="imsrdpdevicev2-interface"></a>IMsRdpDeviceV2-Schnittstelle

Enthält Informationen zu einem Geräteobjekt. Dies ist eine Erweiterung der [**IMsRdpDevice-Schnittstelle.**](imsrdpdevice.md)

## <a name="members"></a>Member

Die **IMsRdpDeviceV2-Schnittstelle** erbt von [**IMsRdpDevice**](imsrdpdevice.md). **IMsRdpDeviceV2** verfügt auch über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **IMsRdpDeviceV2-Schnittstelle** verfügt über diese Eigenschaften.



| Eigenschaft                                                                 | Zugriffstyp          | Beschreibung                                                                                        |
|:-------------------------------------------------------------------------|:---------------------|:---------------------------------------------------------------------------------------------------|
| [**CmClassGuid**](imsrdpdevicev2-cmclassguid.md)<br/>             | Schreibgeschützt<br/> | Enthält die Configuration Manager-Setupklassen-GUID für das Gerät.<br/>                     |
| [**CmDeviceInstance**](imsrdpdevicev2-cmdeviceinstance.md)<br/>   | Schreibgeschützt<br/> | Enthält die Configuration Manager-Geräteinstanz des Geräts.<br/>                       |
| [**DeviceText**](imsrdpdevicev2-devicetext.md)<br/>               | Schreibgeschützt<br/> | Enthält den Gerätetext.<br/>                                                               |
| [**DriveLetterBitmap**](imsrdpdevicev2-driveletterbitmap.md)<br/> | Schreibgeschützt<br/> | Enthält ein Bitfeld, das eine Zuordnung von Laufwerkbuchstaben darstellt, die im Gerät enthalten sind.<br/> |
| [**IsCompositeDevice**](imsrdpdevicev2-iscompositedevice.md)<br/> | Schreibgeschützt<br/> | Gibt an, ob das Gerät ein zusammengesetztes Gerät ist.<br/>                                          |
| [**IsOptionalDevice**](imsrdpdevicev2-isoptionaldevice.md)<br/>   | Schreibgeschützt<br/> | Gibt an, ob das Gerät für die USB-Umleitung optional ist.<br/>                                |
| [**IsUSBDevice**](imsrdpdevicev2-isusbdevice.md)<br/>             | Schreibgeschützt<br/> | Gibt an, ob das Gerät für die USB-Umleitung vorgesehen ist.<br/>                                         |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 mit SP1<br/>                                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2 mit SP1<br/>                                             |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpDeviceV2 ist als 5fb94466-7661-42a8-98b7-01904c11668f definiert.<br/>      |



 

 





