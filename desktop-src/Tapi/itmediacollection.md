---
description: Die ITMediaCollection-Schnittstelle bietet Zugriff auf den Satz von Medieninformationen in einer SDP-Konferenzbeschreibung (RFC 2327).
ms.assetid: a7e7a07d-239e-432e-9984-7763f11c59ce
title: ITMediaCollection-Schnittstelle (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2425ae89f376d5cb2d7cc23e70abd33f87750d3d1b5343a17c8ecb05d7de760d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120034610"
---
# <a name="itmediacollection-interface"></a>ITMediaCollection-Schnittstelle

\[Rendezvous-IP-Telefoniekonferenz-Steuerelemente und -Schnittstellen sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet ähnliche Funktionen.\]

Die **ITMediaCollection-Schnittstelle** bietet Zugriff auf den Satz von Medieninformationen in einer SDP-Konferenzbeschreibung (RFC 2327). Jede Medienbeschreibung im SDP wird von einer [**ITMedia-Schnittstelle**](itmedia.md) beschrieben. **ITMediaCollection** ermöglicht die Bearbeitung des Satzes von **ITMedia-Informationen** für den SDP, einschließlich:

-   Ermöglicht den Medienzugriff nach Index.
-   Ermöglicht das Erstellen und Löschen von Medien.

Die [**ITSdp::get \_ MediaCollection-Methode**](itsdp-get-mediacollection.md) erstellt die **ITMediaCollection-Schnittstelle.**

## <a name="members"></a>Member

Die **ITMediaCollection-Schnittstelle** erbt von der [**IDispatch-Schnittstelle.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **ITMediaCollection** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ITMediaCollection-Schnittstelle** verfügt über diese Methoden.



| Methode                                                            | BESCHREIBUNG                                                            |
|:------------------------------------------------------------------|:-----------------------------------------------------------------------|
| [**Erstellen**](itmediacollection-create.md)                        | Erstellt ein neues Medium mit Standardeigenschaften und gibt es zurück.<br/> |
| [**Löschen**](itmediacollection-delete.md)                        | Löscht die Medien, die dem angegebenen Index entsprechen.<br/>     |
| [**get \_ \_ NewEnum**](itmediacollection-get--newenum.md)          | Gibt einen Enumerator für die Auflistung zurück.<br/>                   |
| [**get \_ Count**](itmediacollection-get-count.md)                 | Ruft die Anzahl der Medien in der Sitzung ab.<br/>                    |
| [**get \_ EnumerationIf**](itmediacollection-get-enumerationif.md) | Ruft einen Zeiger auf die Enumerationsschnittstelle ab.<br/>                      |
| [**get \_ Item**](itmediacollection-get-item.md)                   | Gibt die Medien zurück, die dem angegebenen Index entsprechen.<br/>     |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3.0 oder höher<br/>                                                 |
| Header<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Bibliothek<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



 

