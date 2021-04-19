---
description: Das itstreamqualitycontrol-Steuerelement macht Methoden verfügbar, mit denen eine Anwendung Parameter für die streamqualitätskontrolle erhalten und festlegen kann.
ms.assetid: b9ecf24a-c87e-44a6-9e20-aa7bf7619314
title: Itstreamqualitycontrol-Schnittstelle (ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98a85eccc907ef2c8f4c0b67c2a32244004dbdca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370172"
---
# <a name="itstreamqualitycontrol-interface"></a>Itstreamqualitycontrol-Schnittstelle

\[ Diese Schnittstelle ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet eine ähnliche Funktionalität.\]

Das **itstreamqualitycontrol-Steuer** Element macht Methoden verfügbar, mit denen eine Anwendung Parameter für die streamqualitätskontrolle erhalten und festlegen kann.

Diese Schnittstelle wird von [ipconf MSP](ipconf-msp.md) und [h323 MSP](h323-msp.md)implementiert. Sie wird nur verfügbar gemacht, wenn ein-Rückruf diese Dienstanbieter verwendet.

## <a name="members"></a>Member

Die **itstreamqualitycontrol** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Itstreamqualitycontrol** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **itstreamqualitycontrol** -Schnittstelle verfügt über diese Methoden.



| Methode                                              | BESCHREIBUNG                                                                                                 |
|:----------------------------------------------------|:------------------------------------------------------------------------------------------------------------|
| [**Erhalten**](itstreamqualitycontrol-get.md)           | Ruft den Wert einer angegebenen [Stream Quality-Eigenschaft](streamqualityproperty.md)ab.<br/>                  |
| [**GetRange**](itstreamqualitycontrol-getrange.md) | Ruft den Bereich der gültigen Werte für eine angegebene [Eigenschaft der Streamqualität](streamqualityproperty.md)ab.<br/> |
| [**Set**](itstreamqualitycontrol-set.md)           | Legt den Wert einer angegebenen Eigenschaft für die [Streamqualität](streamqualityproperty.md)fest.<br/>                  |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|--------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3,1<br/>                                                         |
| Header<br/>       | <dl> <dt>Ipmsp. h</dt> </dl>   |
| Bibliothek<br/>      | <dl> <dt>UUID. lib</dt> </dl>  |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



 

