---
description: Die itcallqualitycontrol-Schnittstelle macht Methoden verfügbar, die einer Anwendung das Abrufen und Festlegen von Parametern für die Abruf Qualität ermöglichen.
ms.assetid: 8d33e3b2-6af9-4c2d-bc65-905467f4fc6a
title: Itcallqualitycontrol-Schnittstelle (ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 447e2f34db76ba15ecaec9e7bc03a0d2d398c493
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364973"
---
# <a name="itcallqualitycontrol-interface"></a>Itcallqualitycontrol-Schnittstelle

\[ Diese Schnittstelle ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet eine ähnliche Funktionalität.\]

Die **itcallqualitycontrol** -Schnittstelle macht Methoden verfügbar, die einer Anwendung das Abrufen und Festlegen von Parametern für die Abruf Qualität ermöglichen.

Diese Schnittstelle wird von [ipconf MSP](ipconf-msp.md) und [h323 MSP](h323-msp.md)implementiert. Sie wird nur verfügbar gemacht, wenn ein-Rückruf diese Dienstanbieter verwendet.

## <a name="members"></a>Member

Die **itcallqualitycontrol** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Itcallqualitycontrol** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **itcallqualitycontrol** -Schnittstelle verfügt über diese Methoden.



| Methode                                            | BESCHREIBUNG                                                                                                     |
|:--------------------------------------------------|:----------------------------------------------------------------------------------------------------------------|
| [**Erhalten**](itcallqualitycontrol-get.md)           | Ruft den Wert einer angegebenen Eigenschaft für die [Eigenschaft "Qualitätskontrolle](callqualityproperty.md)" ab.<br/>                  |
| [**GetRange**](itcallqualitycontrol-getrange.md) | Ruft den Bereich der gültigen Werte für eine angegebene [Eigenschaft des Steuer](callqualityproperty.md)Elements "Callcenter" ab.<br/> |
| [**Set**](itcallqualitycontrol-set.md)           | Legt den Wert einer angegebenen [Eigenschaft zum Abrufen der Qualitätskontrolle](callqualityproperty.md)fest.<br/>                  |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|--------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3,1<br/>                                                         |
| Header<br/>       | <dl> <dt>Ipmsp. h</dt> </dl>   |
| Bibliothek<br/>      | <dl> <dt>UUID. lib</dt> </dl>  |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



 

