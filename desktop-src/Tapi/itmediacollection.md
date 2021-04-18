---
description: Die itmediacollection-Schnittstelle ermöglicht den Zugriff auf den Satz von Medieninformationen in einer SDP-Konferenzbeschreibung (RFC 2327).
ms.assetid: a7e7a07d-239e-432e-9984-7763f11c59ce
title: Itmediacollection-Schnittstelle (sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21305e1d1729437b53c380b7712feee3827b3ba8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365381"
---
# <a name="itmediacollection-interface"></a>Itmediacollection-Schnittstelle

\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet eine ähnliche Funktionalität.\]

Die **itmediacollection** -Schnittstelle ermöglicht den Zugriff auf den Satz von Medieninformationen in einer SDP-Konferenzbeschreibung (RFC 2327). Jede Medien Beschreibung im SDP wird durch eine [**ITmedia**](itmedia.md) -Schnittstelle beschrieben. **Itmediacollection** ermöglicht die Bearbeitung des Satzes von **ITmedia** -Informationen für den SDP, einschließlich:

-   Ermöglicht den Medien Zugriff nach Index.
-   Ermöglicht das Erstellen und Löschen von Medien.

Die [**itsdp:: get \_ mediacollection**](itsdp-get-mediacollection.md) -Methode erstellt die **itmediacollection** -Schnittstelle.

## <a name="members"></a>Member

Die **itmediacollection** -Schnittstelle erbt von der [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle. **Itmediacollection** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **itmediacollection** -Schnittstelle verfügt über diese Methoden.



| Methode                                                            | BESCHREIBUNG                                                            |
|:------------------------------------------------------------------|:-----------------------------------------------------------------------|
| [**Stelle**](itmediacollection-create.md)                        | Erstellt ein neues Medium mit Standardeigenschaften und gibt dieses zurück.<br/> |
| [**Lösch**](itmediacollection-delete.md)                        | Löscht das Medium, das dem angegebenen Index entspricht.<br/>     |
| [**" \_ \_ netwenum"**](itmediacollection-get--newenum.md)          | Gibt einen Enumerator für die Auflistung zurück.<br/>                   |
| [**get- \_ Anzahl**](itmediacollection-get-count.md)                 | Ruft die Anzahl der Medien in der Sitzung ab.<br/>                    |
| [**\_enumerationif erhalten**](itmediacollection-get-enumerationif.md) | Ruft den Zeiger auf die Enumerationsschnittstelle ab.<br/>                      |
| [**\_Element erhalten**](itmediacollection-get-item.md)                   | Gibt das Medium zurück, das dem angegebenen Index entspricht.<br/>     |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3,0 oder höher<br/>                                                 |
| Header<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Bibliothek<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



 

