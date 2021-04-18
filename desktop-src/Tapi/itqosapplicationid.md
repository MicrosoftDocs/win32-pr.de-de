---
description: Die itqosapplicationid-Schnittstelle macht eine Methode verfügbar, die es einer Anwendung ermöglicht, den QoS-Bezeichner für den aktuellen Aufruf abzurufen.
ms.assetid: 1df50b3a-bd16-4e9b-afca-b025bfe537a4
title: Itqosapplicationid-Schnittstelle (ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23df8da80798cc52ecd73b4f29288812f3774d9f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372001"
---
# <a name="itqosapplicationid-interface"></a>Itqosapplicationid-Schnittstelle

\[ Diese Schnittstelle ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet eine ähnliche Funktionalität.\]

Die **itqosapplicationid** -Schnittstelle macht eine Methode verfügbar, die es einer Anwendung ermöglicht, den QoS-Bezeichner für den aktuellen Aufruf abzurufen.

Diese Schnittstelle wird vom [ipconf-MSP](ipconf-msp.md) implementiert und wird nur verfügbar gemacht, wenn ein-Rückruf IP-Konferenzen verwendet.

## <a name="members"></a>Member

Die **itqosapplicationid** -Schnittstelle erbt von der [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle. **Itqosapplicationid** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **itqosapplicationid** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                | BESCHREIBUNG                         |
|:----------------------------------------------------------------------|:------------------------------------|
| [**Setqosapplicationid**](itqosapplicationid-setqosapplicationid.md) | Legt den QoS-Bezeichner fest.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|--------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3,1<br/>                                                         |
| Header<br/>       | <dl> <dt>Ipmsp. h</dt> </dl>   |
| Bibliothek<br/>      | <dl> <dt>UUID. lib</dt> </dl>  |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



 

