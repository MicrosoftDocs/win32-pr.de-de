---
description: Die Funktionalität der ITConnection-Schnittstelle ist unten dargestellt.
ms.assetid: 44dc39cf-3222-41ed-b29c-df2d32615500
title: ITConnection-Schnittstelle (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a64758f6a5cf7bcd9106504412f4cf7f39e6fb7ca0b76e35b38e19dc3f815ccf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119140343"
---
# <a name="itconnection-interface"></a>ITConnection-Schnittstelle

\[Rendezvous-IP-Telefoniekonferenz-Steuerelemente und -Schnittstellen sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet ähnliche Funktionen.\]

Die **ITConnection-Schnittstelle** bietet die folgenden Funktionen:

-   Bietet Zugriff auf die Informationen zur Adresse und Gültigkeitsdauer (Time to Live, TTL) für die Sitzung.
-   Ermöglicht den Zugriff auf die Bandbreiteninformationen.
-   Ermöglicht die Bearbeitung des Verschlüsselungsschlüssels.

Die **ITConnection-Schnittstelle** wird durch Aufrufen von **QueryInterface** auf [**ITConferenceBlob**](itconferenceblob.md)erstellt.

## <a name="members"></a>Member

Die **ITConnection-Schnittstelle** erbt von der [**IDispatch-Schnittstelle.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **ITConnection** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ITConnection-Schnittstelle** verfügt über diese Methoden.



| Methode                                                               | Beschreibung                                                                                                                                    |
|:---------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------|
| [**get \_ AddressType**](itconnection-get-addresstype.md)             | Ruft den Adresstyp ab.<br/>                                                                                                              |
| [**Bandbreite abrufen \_**](itconnection-get-bandwidth.md)                 | Ruft den Bandbreitenwert ab.<br/>                                                                                                               |
| [**get \_ BandwidthModifier**](itconnection-get-bandwidthmodifier.md) | Ruft den Bandbreitenmodifizierer ab.<br/>                                                                                                        |
| [**\_Get NetworkType**](itconnection-get-networktype.md)             | Ruft den Netzwerktyp ab.<br/>                                                                                                              |
| [**get \_ NumAddresses**](itconnection-get-numaddresses.md)           | Ruft die Anzahl der Adressen ab, die für die Sitzung verwendet werden sollen.<br/>                                                                            |
| [**get \_ StartAddress**](itconnection-get-startaddress.md)           | Ruft die erste Adresse ab, die für die Sitzung verwendet werden soll.<br/>                                                                                  |
| [**Get \_ Ttl**](itconnection-get-ttl.md)                             | Ruft den [*Gültigkeitsdauerbereich*](t-tapgloss.md) (Time to Live, TTL) für Übertragungen an den Adressen ab.<br/> |
| [**GetEncryptionKey**](itconnection-getencryptionkey.md)            | Ruft den Verschlüsselungsschlüssel ab.<br/>                                                                                                            |
| [**put \_ AddressType**](itconnection-put-addresstype.md)             | Legt den Adresstyp fest.<br/>                                                                                                              |
| [**\_put NetworkType**](itconnection-put-networktype.md)             | Legt den Netzwerktyp fest.<br/>                                                                                                              |
| [**SetAddressInfo**](itconnection-setaddressinfo.md)                | Legt Adressinformationen fest.<br/>                                                                                                           |
| [**SetBandwidthInfo**](itconnection-setbandwidthinfo.md)            | Legt den Bandbreitenwert fest.<br/>                                                                                                           |
| [**SetEncryptionKey**](itconnection-setencryptionkey.md)            | Legt den Verschlüsselungsschlüssel fest, der zum Entschlüsseln der Sitzung erforderlich ist, oder einen Hinweis auf einen Mechanismus, um einen verwendbaren Schlüssel auf externe Weise abzurufen.<br/>     |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3.0 oder höher<br/>                                                 |
| Header<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Bibliothek<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



 

