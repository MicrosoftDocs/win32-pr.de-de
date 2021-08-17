---
description: Die ITTimeCollection-Schnittstelle ist eine anbieterspezifische Schnittstelle für das SDP-Konferenzblobobjekt (Session Descriptor Protocol).
ms.assetid: 6309e9f2-8a73-4d42-ae0a-2165352d6244
title: ITTimeCollection-Schnittstelle (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d086dcf0df7fb4d55552c734798244209fc3e9f52a2f2462693f6aaad7110347
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117762294"
---
# <a name="ittimecollection-interface"></a>ITTimeCollection-Schnittstelle

\[Rendezvous IP-Telefoniekonferenz-Steuerelemente und -Schnittstellen sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet ähnliche Funktionen.\]

Die **ITTimeCollection-Schnittstelle** ist eine anbieterspezifische Schnittstelle für das SDP-Konferenzblobobjekt (Session Descriptor Protocol). Diese Schnittstelle ermöglicht den Zugriff [**auf ITTime-Schnittstellen**](ittime.md) nach Index sowie das Erstellen und Löschen von Zeitkomponenten. Die [**\_ TimeCollection-Methode ITSdp::get**](itsdp-get-timecollection.md) erstellt die **ITTimeCollection-Schnittstelle.**

## <a name="members"></a>Member

Die **ITTimeCollection-Schnittstelle** erbt von der [**IDispatch-Schnittstelle.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **ITTimeCollection** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ITTimeCollection-Schnittstelle** verfügt über diese Methoden.



| Methode                                                           | Beschreibung                                                                                                           |
|:-----------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------|
| [**Erstellen**](ittimecollection-create.md)                        | Erstellt eine [**ITTime-Komponente.**](ittime.md)<br/>                                                             |
| [**Löschen**](ittimecollection-delete.md)                        | Löscht eine [**ITTime-Komponente.**](ittime.md)<br/>                                                             |
| [**get \_ \_ NewEnum**](ittimecollection-get--newenum.md)          | Gibt einen Enumerator für die Auflistung zurück.<br/>                                                                  |
| [**get \_ Count**](ittimecollection-get-count.md)                 | Ruft die Anzahl der Elemente in der Auflistung ab.<br/>                                                                        |
| [**get \_ EnumerationIf**](ittimecollection-get-enumerationif.md) | Gibt die [**IEnumTime-Enumerationsschnittstelle**](ienumtime.md) zurück, die [**ITTime aufzählt.**](ittime.md)<br/> |
| [**Element \_ "get"**](ittimecollection-get-item.md)                   | Bei einem Index gibt ein Element in der Auflistung zurück.<br/>                                                         |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3.0 oder höher<br/>                                                 |
| Header<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Bibliothek<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



 

