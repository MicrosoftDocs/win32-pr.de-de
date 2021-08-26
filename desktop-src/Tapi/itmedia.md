---
description: Die ITMedia-Schnittstelle ist eine Darstellung von Medien in einem Sitzungsdeskriptorprotokoll (Session Descriptor Protocol, SDP, siehe RFC 2327).
ms.assetid: f5cd7971-3456-4e2f-8808-deb16678099a
title: ITMedia-Schnittstelle (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfd1cf7dcf8ef294481a4687dbac950f97b4adede6a6871222292127e6255057
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120034640"
---
# <a name="itmedia-interface"></a>ITMedia-Schnittstelle

\[Rendezvous-IP-Telefoniekonferenz-Steuerelemente und -Schnittstellen sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet ähnliche Funktionen.\]

Die **ITMedia-Schnittstelle** ist eine Darstellung von Medien in einem Sitzungsdeskriptorprotokoll (Session Descriptor Protocol, SDP, siehe RFC 2327). Diese Schnittstelle exportiert Methoden, um grundlegende Medieneigenschaften wie type abzurufen und festzulegen. Die Methoden [**ITMediaCollection::get \_ Item**](itmediacollection-get-item.md) und [**ITMediaCollection::Create**](itmediacollection-create.md) erstellen die **ITMedia-Schnittstelle.**

## <a name="members"></a>Member

Die **ITMedia-Schnittstelle** erbt von der [**IDispatch-Schnittstelle.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **ITMedia** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ITMedia-Schnittstelle** verfügt über diese Methoden.



| Methode                                                          | BESCHREIBUNG                                                                                      |
|:----------------------------------------------------------------|:-------------------------------------------------------------------------------------------------|
| [**Formatcodes abrufen \_**](itmedia-get-formatcodes.md)             | Ruft die Liste der Formatcodes der Mediennutzlast ab.<br/>                                          |
| [**\_Get MediaName**](itmedia-get-medianame.md)                 | Ruft den Mediennamen ab.<br/>                                                                  |
| [**get \_ MediaTitle**](itmedia-get-mediatitle.md)               | Ruft den Medientitel ab.<br/>                                                                 |
| [**\_NumPorts abrufen**](itmedia-get-numports.md)                   | Ruft die Anzahl der ports ab, die für die Sitzung benötigt werden.<br/>                                      |
| [**get \_ StartPort**](itmedia-get-startport.md)                 | Ruft den 16-Bit-Portwert für den ersten Port ab.<br/>                                        |
| [**get \_ TransportProtocol**](itmedia-get-transportprotocol.md) | Ruft das Transportprotokoll ab.<br/>                                                          |
| [**\_put FormatCodes**](itmedia-put-formatcodes.md)             | Legt die Liste der Mediennutzlastformatcodes fest.<br/>                                          |
| [**\_Put MediaName**](itmedia-put-medianame.md)                 | Legt den Mediennamen fest.<br/>                                                                  |
| [**\_put MediaTitle**](itmedia-put-mediatitle.md)               | Legt den Medientitel fest.<br/>                                                                 |
| [**put \_ TransportProtocol**](itmedia-put-transportprotocol.md) | Legt das Transportprotokoll fest.<br/>                                                          |
| [**SetPortInfo**](itmedia-setportinfo.md)                      | Legt den 16-Bit-Portwert für den ersten Port und die Anzahl der ports fest, die für die Sitzung benötigt werden.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3.0 oder höher<br/>                                                 |
| Header<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Bibliothek<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[**ITMediaCollection**](itmediacollection.md)
</dt> <dt>

[**ITSDP**](itsdp.md)
</dt> <dt>

[**ITTime**](ittime.md)
</dt> </dl>

 

