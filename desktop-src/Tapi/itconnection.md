---
description: Die Funktionalität der itconnection-Schnittstelle ist unten dargestellt.
ms.assetid: 44dc39cf-3222-41ed-b29c-df2d32615500
title: Itconnection-Schnittstelle (sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a00da80631c0ef4e8186aa36425f18e4d2a62bfc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371779"
---
# <a name="itconnection-interface"></a>Itconnection-Schnittstelle

\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet eine ähnliche Funktionalität.\]

Die **itconnection** -Schnittstelle bietet die folgenden Funktionen:

-   Bietet Zugriff auf die Informationen zu Adresse und Gültigkeitsdauer (Time to Live, TTL) für die Sitzung.
-   Ermöglicht den Zugriff auf die Bandbreiten Informationen.
-   Ermöglicht die Bearbeitung des Verschlüsselungsschlüssels.

Die **itconnection** -Schnittstelle wird durch Aufrufen von **QueryInterface** für [**itconferenceblob**](itconferenceblob.md)erstellt.

## <a name="members"></a>Member

Die **itconnection** -Schnittstelle erbt von der [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle. **Itconnection** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **itconnection** -Schnittstelle verfügt über diese Methoden.



| Methode                                                               | BESCHREIBUNG                                                                                                                                    |
|:---------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_adressstypen erhalten**](itconnection-get-addresstype.md)             | Ruft den Adresstyp ab.<br/>                                                                                                              |
| [**\_Bandbreite erhalten**](itconnection-get-bandwidth.md)                 | Ruft den Bandbreitenwert ab.<br/>                                                                                                               |
| [**get \_ bandwidthmodifier**](itconnection-get-bandwidthmodifier.md) | Ruft den bandbreitmodifizierer ab.<br/>                                                                                                        |
| [**\_NetworkType erhalten**](itconnection-get-networktype.md)             | Ruft den Netzwerktyp ab.<br/>                                                                                                              |
| [**\_numadkleider erhalten**](itconnection-get-numaddresses.md)           | Ruft die Anzahl der Adressen ab, die für die Sitzung verwendet werden sollen.<br/>                                                                            |
| [**\_STARTADDRESS erhalten**](itconnection-get-startaddress.md)           | Ruft die erste Adresse ab, die für die Sitzung verwendet werden soll.<br/>                                                                                  |
| [**Gültigkeitsdauer \_**](itconnection-get-ttl.md)                             | Ruft den Gültigkeitsbereich der Gültigkeits [*Dauer*](t-tapgloss.md) (TTL) für Übertragungen für die Adressen ab.<br/> |
| [**GetEncryptionKey**](itconnection-getencryptionkey.md)            | Ruft den Verschlüsselungsschlüssel ab.<br/>                                                                                                            |
| [**Put- \_ Adresstype**](itconnection-put-addresstype.md)             | Legt den adrestyp fest.<br/>                                                                                                              |
| [**\_NetworkType platzieren**](itconnection-put-networktype.md)             | Legt den Netzwerktyp fest.<br/>                                                                                                              |
| [**Setaddressinfo**](itconnection-setaddressinfo.md)                | Legt Adressinformationen fest.<br/>                                                                                                           |
| [**Setbandwidthinfo**](itconnection-setbandwidthinfo.md)            | Legt den Bandbreitenwert fest.<br/>                                                                                                           |
| [**SetEncryptionKey**](itconnection-setencryptionkey.md)            | Legt den Verschlüsselungsschlüssel fest, der zum Entschlüsseln der Sitzung erforderlich ist, oder einen Indikator für einen Mechanismus, um einen verwendbaren Schlüssel auf externe Weise zu erhalten.<br/>     |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3,0 oder höher<br/>                                                 |
| Header<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Bibliothek<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



 

