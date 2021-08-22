---
description: Definiert eine einzelne Rückrufmethode.
ms.assetid: 579f7a29-cd98-4d97-9f8e-9b786897df1c
title: IConnectionRequestCallback-Schnittstelle (Devpkey.h)
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
ms.openlocfilehash: 53e1549767c8577507b3126b3a293dfe4e523612809c144ff24c04dce4ab1ff4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118697418"
---
# <a name="iconnectionrequestcallback-interface"></a>IConnectionRequestCallback-Schnittstelle

Die **IConnectionRequestCallback-Schnittstelle** definiert eine einzelne Rückrufmethode. Eine Windows Portable Devices (WPD) implementiert diese optionale Component Object Model-Schnittstelle (COM), um Benachrichtigungen über abgeschlossene Anforderungen zu empfangen und ausstehende Anforderungen abzubricht. Die Anforderungen werden mithilfe der [**Methoden IPortableDeviceConnector::Verbinden**](/windows/desktop/api/portabledeviceconnectapi/nf-portabledeviceconnectapi-iportabledeviceconnector-connect) und [**IPortableDeviceConnector::D isconnect**](/windows/desktop/api/portabledeviceconnectapi/nf-portabledeviceconnectapi-iportabledeviceconnector-disconnect) gesendet.

## <a name="members"></a>Member

Die **IConnectionRequestCallback-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IConnectionRequestCallback** verfügt auch über diese Membertypen:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IConnectionRequestCallback-Schnittstelle** verfügt über diese Methoden.



| Methode                                                      | Beschreibung                                                                           |
|:------------------------------------------------------------|:--------------------------------------------------------------------------------------|
| [**Oncomplete**](iconnectionrequestcallback-oncomplete.md) | Benachrichtigt eine Anwendung, dass eine zuvor geplante Anforderung abgeschlossen wurde.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                                                                                                             |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                                                                              |
| Header<br/>                   | <dl> <dt>Devpkey.h; </dt> <dt>Portabledeviceconnectapi.h</dt> </dl> |
| Idl<br/>                      | <dl> <dt>Portabledeviceconnectapi.idl</dt> </dl>                                                                |
| Bibliothek<br/>                  | <dl> <dt>PortableDeviceGuids.lib</dt> </dl>                                                                     |



 

