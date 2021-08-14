---
description: Die ITSdp-Schnittstelle stellt Methoden für die Bearbeitung einer Sitzungsdeskriptorprotokoll-Komponente (Session Descriptor Protocol, SDP, siehe RFC 2327) bereit.
ms.assetid: 77c1e302-6290-4eeb-b7c9-462a13b29dcd
title: ITSdp-Schnittstelle (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9bba91e347fbf0de1e1b59a8e6100ccbf26babf707e6d6870d43961cbe006b23
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117945019"
---
# <a name="itsdp-interface"></a>ITSdp-Schnittstelle

\[Rendezvous-IP-Telefoniekonferenz-Steuerelemente und -Schnittstellen sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet ähnliche Funktionen.\]

Die **ITSdp-Schnittstelle** stellt Methoden für die Bearbeitung einer Sitzungsdeskriptorprotokoll-Komponente (Session Descriptor Protocol, SDP, siehe RFC 2327) bereit. Er bietet die folgenden Funktionen:

-   Ermöglicht den Zugriff auf einige der Eigenschaften, die für alle Medien gelten. Dazu gehören Attribute, die sich auf die persönlichen Informationen des Erstellers, die Sitzungsbeschreibung und die Adresstypinformationen beziehen.
-   Stellt den Ausgangspunkt für den Zugriff auf die Zeit- und Medienauflistungen über Eigenschaften bereit.

Die **ITSdp-Schnittstelle** wird durch Aufrufen von **QueryInterface** auf [**ITConferenceBlob**](itconferenceblob.md)erstellt.

## <a name="members"></a>Member

Die **ITSdp-Schnittstelle** erbt von der [**IDispatch-Schnittstelle.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **ITSdp** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ITSdp-Schnittstelle** verfügt über diese Methoden.



| Methode                                                    | BESCHREIBUNG                                                                                         |
|:----------------------------------------------------------|:----------------------------------------------------------------------------------------------------|
| [**Beschreibung abrufen \_**](itsdp-get-description.md)         | Ruft die Sitzungsbeschreibung ab.<br/>                                                            |
| [**\_IsValid abrufen**](itsdp-get-isvalid.md)                 | Überprüft das SDP-Blob auf Struktur- und Feldwerte.<br/>                                   |
| [**Get \_ MachineAddress**](itsdp-get-machineaddress.md)   | Ruft die Computeradresse des ursprünglichen Hosts ab.<br/>                                        |
| [**MediaCollection abrufen \_**](itsdp-get-mediacollection.md) | Ruft einen Zeiger auf die [**ITMediaCollection-Schnittstelle**](itmediacollection.md) für die Konferenz ab.<br/> |
| [**get \_ Name**](itsdp-get-name.md)                       | Ruft den Sitzungsnamen ab.<br/>                                                                   |
| [**get \_ Originator**](itsdp-get-originator.md)           | Ruft den Konferenzursprungsgeber ab.<br/>                                                              |
| [**get \_ ProtocolVersion**](itsdp-get-protocolversion.md) | Ruft die SDP-Protokollversion ab.<br/>                                                           |
| [**\_SessionId abrufen**](itsdp-get-sessionid.md)             | Ruft den 32-Bit-NTP-Wert (Network Time Protocol) ab, der als Sitzungsbezeichner dient.<br/> |
| [**get \_ SessionVersion**](itsdp-get-sessionversion.md)   | Ruft den 32-Bit-Wert (idealerweise NTP) ab, der als Sitzungsversion dient.<br/>                  |
| [**\_Get TimeCollection**](itsdp-get-timecollection.md)   | Ruft einen Zeiger auf die [**ITTimeCollection-Schnittstelle**](ittimecollection.md) für die Konferenz ab.<br/>   |
| [**get \_ URL**](itsdp-get-url.md)                         | Ruft die URL ab.<br/>                                                                            |
| [**GetEmailNames**](itsdp-getemailnames.md)              | Ruft ein Array von E-Mail-Namen und Adressen ab, die dem Konferenzblob zugeordnet sind.<br/>                |
| [**GetPhoneNumbers**](itsdp-getphonenumbers.md)          | Ruft die Telefonnummern ab.<br/>                                                                  |
| [**put \_ Description**](itsdp-put-description.md)         | Legt die Sitzungsbeschreibung fest.<br/>                                                            |
| [**put \_ MachineAddress**](itsdp-put-machineaddress.md)   | Legt die Computeradresse des ursprünglichen Hosts fest.<br/>                                        |
| [**put \_ Name**](itsdp-put-name.md)                       | Legt den Sitzungsnamen fest.<br/>                                                                   |
| [**put \_ Originator**](itsdp-put-originator.md)           | Ruft den Konferenzursprungsgeber ab.<br/>                                                              |
| [**put \_ SessionVersion**](itsdp-put-sessionversion.md)   | Legt die Sitzungsversion fest.<br/>                                                                    |
| [**put \_ URL**](itsdp-put-url.md)                         | Legt die URL fest.<br/>                                                                            |
| [**SetEmailNames**](itsdp-setemailnames.md)              | Legt ein Array von E-Mail-Namen und -Adressen fest, die dem Konferenzblob zugeordnet sind.<br/>                 |
| [**SetPhoneNumbers**](itsdp-setphonenumbers.md)          | Legt die Telefonnummern fest.<br/>                                                                  |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3.0 oder höher<br/>                                                 |
| Header<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Bibliothek<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



 

