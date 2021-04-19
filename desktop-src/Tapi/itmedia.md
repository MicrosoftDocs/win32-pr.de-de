---
description: Die ITmedia-Schnittstelle ist eine Darstellung von Medien in einem Sitzungs Deskriptor-Protokoll (SDP, siehe RFC 2327).
ms.assetid: f5cd7971-3456-4e2f-8808-deb16678099a
title: ITmedia-Schnittstelle (sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8dd00d7eab685fe99b089556bcdb0ed2bf6329df
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354233"
---
# <a name="itmedia-interface"></a>ITmedia-Schnittstelle

\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet eine ähnliche Funktionalität.\]

Die **ITmedia** -Schnittstelle ist eine Darstellung von Medien in einem Sitzungs Deskriptor-Protokoll (SDP, siehe RFC 2327). Diese Schnittstelle exportiert Methoden zum erhalten und Festlegen grundlegender Medien Eigenschaften, z. b. Typ. Das [**itmediacollection:: get- \_ Element**](itmediacollection-get-item.md) und die [**itmediacollection:: Create**](itmediacollection-create.md) -Methode erstellen die **ITmedia** -Schnittstelle.

## <a name="members"></a>Member

Die **ITmedia** -Schnittstelle erbt von der [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle. **ITmedia** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ITmedia** -Schnittstelle verfügt über diese Methoden.



| Methode                                                          | BESCHREIBUNG                                                                                      |
|:----------------------------------------------------------------|:-------------------------------------------------------------------------------------------------|
| [**\_Formatcodes erhalten**](itmedia-get-formatcodes.md)             | Ruft die Liste der Formatcodes der Medien Nutzlast ab.<br/>                                          |
| [**" \_ MEDIANAME" erhalten**](itmedia-get-medianame.md)                 | Ruft den Mediennamen ab.<br/>                                                                  |
| [**\_mediatitle erhalten**](itmedia-get-mediatitle.md)               | Ruft den Medien Titel ab.<br/>                                                                 |
| [**\_numports erhalten**](itmedia-get-numports.md)                   | Ruft die Anzahl der für die Sitzung benötigten Ports ab.<br/>                                      |
| [**\_startport starten**](itmedia-get-startport.md)                 | Ruft den 16-Bit-Portwert für den ersten Port ab.<br/>                                        |
| [**\_transportprotocol-Protokoll**](itmedia-get-transportprotocol.md) | Ruft das Transportprotokoll ab.<br/>                                                          |
| [**Put- \_ Formatcodes**](itmedia-put-formatcodes.md)             | Legt die Liste der Medien Nutzlast-Formatcodes fest.<br/>                                          |
| [**\_MEDIANAME platzieren**](itmedia-put-medianame.md)                 | Legt den Mediennamen fest.<br/>                                                                  |
| [**\_mediatitle platzieren**](itmedia-put-mediatitle.md)               | Legt den Medien Titel fest.<br/>                                                                 |
| [**\_transportprotocol ablegen**](itmedia-put-transportprotocol.md) | Legt das Transportprotokoll fest.<br/>                                                          |
| [**Setportinfo**](itmedia-setportinfo.md)                      | Legt den Wert für den 16-Bit-Port für den ersten Port und die Anzahl der für die Sitzung benötigten Ports fest.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3,0 oder höher<br/>                                                 |
| Header<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Bibliothek<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[**Itmediacollection**](itmediacollection.md)
</dt> <dt>

[**Itsdp**](itsdp.md)
</dt> <dt>

[**Ittime**](ittime.md)
</dt> </dl>

 

