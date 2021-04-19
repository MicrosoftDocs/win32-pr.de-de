---
title: IMsRdpDeviceV2-Schnittstelle
description: Enthält Informationen zu einem Geräte Objekt. Dies ist eine Erweiterung der imsrdpdevice-Schnittstelle.
ms.assetid: 9a380a1a-d44f-4147-8917-bf1e07dbac15
ms.tgt_platform: multiple
keywords:
- IMsRdpDeviceV2-Schnittstelle Remotedesktopdienste
- IMsRdpDeviceV2 Interface Remotedesktopdienste, beschrieben
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
ms.openlocfilehash: 8c46e1e4df8f9cd521d67383960e9ccf5060bb2d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341773"
---
# <a name="imsrdpdevicev2-interface"></a>IMsRdpDeviceV2-Schnittstelle

Enthält Informationen zu einem Geräte Objekt. Dies ist eine Erweiterung der [**imsrdpdevice**](imsrdpdevice.md) -Schnittstelle.

## <a name="members"></a>Member

Die **IMsRdpDeviceV2** -Schnittstelle erbt von [**imsrdpdevice**](imsrdpdevice.md). **IMsRdpDeviceV2** verfügt auch über die folgenden Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **IMsRdpDeviceV2** -Schnittstelle verfügt über diese Eigenschaften.



| Eigenschaft                                                                 | Zugriffstyp          | BESCHREIBUNG                                                                                        |
|:-------------------------------------------------------------------------|:---------------------|:---------------------------------------------------------------------------------------------------|
| [**Cmclassguid**](imsrdpdevicev2-cmclassguid.md)<br/>             | Schreibgeschützt<br/> | Enthält die Configuration Manager-Setup Klassen-GUID für das Gerät.<br/>                     |
| [**Cmdebug**](imsrdpdevicev2-cmdeviceinstance.md)<br/>   | Schreibgeschützt<br/> | Enthält die Configuration Manager-Geräte Instanz des Geräts.<br/>                       |
| [**Devicetext**](imsrdpdevicev2-devicetext.md)<br/>               | Schreibgeschützt<br/> | Enthält den Geräte Text.<br/>                                                               |
| [**Driveletterbitmap**](imsrdpdevicev2-driveletterbitmap.md)<br/> | Schreibgeschützt<br/> | Enthält ein Bitfeld, das eine Zuordnung der im Gerät enthaltenen Laufwerk Buchstaben darstellt.<br/> |
| [**Iscompositedevice**](imsrdpdevicev2-iscompositedevice.md)<br/> | Schreibgeschützt<br/> | Gibt an, ob es sich um ein zusammengesetztes Gerät handelt.<br/>                                          |
| [**Isoptionaldevice**](imsrdpdevicev2-isoptionaldevice.md)<br/>   | Schreibgeschützt<br/> | Gibt an, ob das Gerät für die USB-Umleitung optional ist.<br/>                                |
| [**Isusbdevice**](imsrdpdevicev2-isusbdevice.md)<br/>             | Schreibgeschützt<br/> | Gibt an, ob das Gerät für die USB-Umleitung vorgesehen ist.<br/>                                         |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 mit SP1<br/>                                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2 mit SP1<br/>                                             |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpDeviceV2 wird als 5b94466-7661-42a8-98b7-01904c11668f definiert.<br/>      |



 

 





