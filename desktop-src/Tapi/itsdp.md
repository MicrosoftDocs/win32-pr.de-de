---
description: Die itsdp-Schnittstelle stellt Methoden für die Bearbeitung eines Sitzungs deskriptorprotokolls (SDP, siehe RFC 2327) Conference BLOB Component bereit.
ms.assetid: 77c1e302-6290-4eeb-b7c9-462a13b29dcd
title: Itsdp-Schnittstelle (sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 401dbe2548375227be2ca024ee75de3054fa6f6f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369311"
---
# <a name="itsdp-interface"></a>Itsdp-Schnittstelle

\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet eine ähnliche Funktionalität.\]

Die **itsdp** -Schnittstelle stellt Methoden für die Bearbeitung eines Sitzungs deskriptorprotokolls (SDP, siehe RFC 2327) Conference BLOB Component bereit. Er bietet die folgenden Funktionen:

-   Bietet Zugriff auf einige Eigenschaften, die allen Medien gemeinsam sind. Diese umfassen Attribute, die sich auf die personenbezogenen Informationen, Sitzungs Beschreibungen und Adresstyp Informationen des Erstellers beziehen.
-   Stellt den Ausgangspunkt für den Zugriff auf die Zeit-und Medien Auflistungen über Eigenschaften bereit.

Die **itsdp** -Schnittstelle wird durch Aufrufen von **QueryInterface** für [**itconferenceblob**](itconferenceblob.md)erstellt.

## <a name="members"></a>Member

Die **itsdp** -Schnittstelle erbt von der [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle. **Itsdp** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **itsdp** -Schnittstelle verfügt über diese Methoden.



| Methode                                                    | BESCHREIBUNG                                                                                         |
|:----------------------------------------------------------|:----------------------------------------------------------------------------------------------------|
| [**\_Beschreibung erhalten**](itsdp-get-description.md)         | Ruft die Beschreibung der Sitzung ab.<br/>                                                            |
| [**get \_ IsValid**](itsdp-get-isvalid.md)                 | Überprüft das SDP-BLOB für Struktur-und Feldwerte.<br/>                                   |
| [**\_machineaddress erhalten**](itsdp-get-machineaddress.md)   | Ruft die Computer Adresse des Ursprungs Hosts ab.<br/>                                        |
| [**\_mediacollection erhalten**](itsdp-get-mediacollection.md) | Ruft den Zeiger auf die [**itmediacollection**](itmediacollection.md) -Schnittstelle für die Konferenz ab.<br/> |
| [**\_Name erhalten**](itsdp-get-name.md)                       | Ruft den Sitzungs Namen ab.<br/>                                                                   |
| [**Absender \_ erhalten**](itsdp-get-originator.md)           | Ruft den Absender der Konferenz ab.<br/>                                                              |
| [**\_ProtocolVersion erhalten**](itsdp-get-protocolversion.md) | Ruft die SDP-Protokollversion ab.<br/>                                                           |
| [**\_SessionID erhalten**](itsdp-get-sessionid.md)             | Ruft den 32-Bit-NTP (Network Time Protocol)-Wert ab, der als Sitzungs Bezeichner fungiert.<br/> |
| [**\_sessionversion erhalten**](itsdp-get-sessionversion.md)   | Ruft den 32-Bit-Wert (idealerweise NTP) ab, der als Sitzungs Version fungiert.<br/>                  |
| [**\_timecollection erhalten**](itsdp-get-timecollection.md)   | Ruft den Zeiger auf die [**ittimecollection**](ittimecollection.md) -Schnittstelle für Conference ab.<br/>   |
| [**\_URL erhalten**](itsdp-get-url.md)                         | Ruft die URL ab.<br/>                                                                            |
| [**Getemailnames**](itsdp-getemailnames.md)              | Ruft ein Array von e-Mail-Namen und Adressen ab, die dem Konferenz-BLOB<br/>                |
| [**Getphonenumbers**](itsdp-getphonenumbers.md)          | Ruft die Telefonnummern ab.<br/>                                                                  |
| [**Put- \_ Beschreibung**](itsdp-put-description.md)         | Legt die Sitzungs Beschreibung fest.<br/>                                                            |
| [**\_machineaddress platzieren**](itsdp-put-machineaddress.md)   | Legt die Computer Adresse des Ursprungs Hosts fest.<br/>                                        |
| [**Put- \_ Name**](itsdp-put-name.md)                       | Legt den Sitzungs Namen fest.<br/>                                                                   |
| [**Put \_ -Absender**](itsdp-put-originator.md)           | Ruft den Absender der Konferenz ab.<br/>                                                              |
| [**\_sessionversion platzieren**](itsdp-put-sessionversion.md)   | Legt die Sitzungs Version fest.<br/>                                                                    |
| [**Put- \_ URL**](itsdp-put-url.md)                         | Legt die URL fest.<br/>                                                                            |
| [**"Menmailnames"**](itsdp-setemailnames.md)              | Legt ein Array von e-Mail-Namen und Adressen fest, die dem Konferenz-BLOB<br/>                 |
| [**Setphonenumbers**](itsdp-setphonenumbers.md)          | Legt die Telefonnummern fest.<br/>                                                                  |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3,0 oder höher<br/>                                                 |
| Header<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Bibliothek<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



 

