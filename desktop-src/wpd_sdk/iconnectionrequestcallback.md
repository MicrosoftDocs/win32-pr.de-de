---
description: Definiert eine einzelne Rückruf Methode.
ms.assetid: 579f7a29-cd98-4d97-9f8e-9b786897df1c
title: Iconnectionrequestcallback-Schnittstelle (devpkey. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IConnectionRequestCallback
api_type:
- COM
api_location:
- PortableDeviceGuids.lib
- PortableDeviceGuids.dll
ms.openlocfilehash: aca827de068ce221f013f03b35f88fd76a030dd4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960848"
---
# <a name="iconnectionrequestcallback-interface"></a>Iconnectionrequestcallback-Schnittstelle

Die **iconnectionrequestcallback** -Schnittstelle definiert eine einzelne Rückruf Methode. Eine Windows Portable Devices (WPD)-Anwendung implementiert diese optionale Component Object Model (com)-Schnittstelle zum Empfangen von Benachrichtigungen zu abgeschlossenen Anforderungen und zum Abbrechen ausstehender Anforderungen. Die Anforderungen werden mithilfe der [**iportabledeviceconnector:: Connect**](/windows/desktop/api/portabledeviceconnectapi/nf-portabledeviceconnectapi-iportabledeviceconnector-connect) -Methode und der [**iportabledeviceconnector::D isconnect**](/windows/desktop/api/portabledeviceconnectapi/nf-portabledeviceconnectapi-iportabledeviceconnector-disconnect) -Methode gesendet.

## <a name="members"></a>Member

Die **iconnectionrequestcallback** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Iconnectionrequestcallback** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **iconnectionrequestcallback** -Schnittstelle verfügt über diese Methoden.



| Methode                                                      | BESCHREIBUNG                                                                           |
|:------------------------------------------------------------|:--------------------------------------------------------------------------------------|
| [**OnComplete**](iconnectionrequestcallback-oncomplete.md) | Benachrichtigt eine Anwendung, dass eine zuvor geplante Anforderung abgeschlossen wurde.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                                                                                             |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                                                                              |
| Header<br/>                   | <dl> <dt>Devpkey. h; </dt> <dt>Portablede viceconnectapi. h</dt> </dl> |
| IDL<br/>                      | <dl> <dt>Portablede viceconnectapi. idl</dt> </dl>                                                                |
| Bibliothek<br/>                  | <dl> <dt>Portabledeviceguids. lib</dt> </dl>                                                                     |



 

