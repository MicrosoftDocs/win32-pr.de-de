---
description: Die ITQOSApplicationID-Schnittstelle macht eine Methode verfügbar, die es einer Anwendung ermöglicht, den QOS-Bezeichner für den aktuellen Aufruf zu erhalten.
ms.assetid: 1df50b3a-bd16-4e9b-afca-b025bfe537a4
title: ITQOSApplicationID-Schnittstelle (Ipmsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d4067d7a476e2a402c278b22dcee21b6542919396178350e73017d56ba92258
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120126280"
---
# <a name="itqosapplicationid-interface"></a>ITQOSApplicationID-Schnittstelle

\[Diese Schnittstelle ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet ähnliche Funktionen.\]

Die **ITQOSApplicationID-Schnittstelle** macht eine Methode verfügbar, die es einer Anwendung ermöglicht, den QOS-Bezeichner für den aktuellen Aufruf zu erhalten.

Diese Schnittstelle wird vom [IPConf-MSP](ipconf-msp.md) implementiert und nur verfügbar gemacht, wenn ein Aufruf IP-Konferenzdienste verwendet.

## <a name="members"></a>Member

Die **ITQOSApplicationID-Schnittstelle** erbt von der [**IDispatch-Schnittstelle.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **ITQOSApplicationID** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ITQOSApplicationID-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                | Beschreibung                         |
|:----------------------------------------------------------------------|:------------------------------------|
| [**SetQOSApplicationID**](itqosapplicationid-setqosapplicationid.md) | Legt den QOS-Bezeichner fest.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|--------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3.1<br/>                                                         |
| Header<br/>       | <dl> <dt>Ipmsp.h</dt> </dl>   |
| Bibliothek<br/>      | <dl> <dt>Uuid.lib</dt> </dl>  |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



 

