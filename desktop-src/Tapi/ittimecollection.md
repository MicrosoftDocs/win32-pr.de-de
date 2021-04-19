---
description: Die ittimecollection-Schnittstelle ist eine anbieterspezifische Schnittstelle für das Sitzungs Deskriptor Protocol (SDP)-Konferenz-BLOB-Objekt.
ms.assetid: 6309e9f2-8a73-4d42-ae0a-2165352d6244
title: Ittimecollection-Schnittstelle (sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19ca297a26b0eac34396726e6145a24fba5a2ed6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373710"
---
# <a name="ittimecollection-interface"></a>Ittimecollection-Schnittstelle

\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet eine ähnliche Funktionalität.\]

Die **ittimecollection** -Schnittstelle ist eine anbieterspezifische Schnittstelle für das Sitzungs Deskriptor Protocol (SDP)-Konferenz-BLOB-Objekt. Diese Schnittstelle ermöglicht den Zugriff auf [**ittime**](ittime.md) -Schnittstellen nach Index und ermöglicht außerdem das Erstellen und Löschen von Zeit Komponenten. Die [**itsdp:: get \_ timecollection**](itsdp-get-timecollection.md) -Methode erstellt die **ittimecollection** -Schnittstelle.

## <a name="members"></a>Member

Die **ittimecollection** -Schnittstelle erbt von der [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle. **Ittimecollection** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ittimecollection** -Schnittstelle verfügt über diese Methoden.



| Methode                                                           | BESCHREIBUNG                                                                                                           |
|:-----------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------|
| [**Stelle**](ittimecollection-create.md)                        | Erstellt eine [**ittime**](ittime.md) -Komponente.<br/>                                                             |
| [**Lösch**](ittimecollection-delete.md)                        | Löscht eine [**ittime**](ittime.md) -Komponente.<br/>                                                             |
| [**" \_ \_ netwenum"**](ittimecollection-get--newenum.md)          | Gibt einen Enumerator für die Auflistung zurück.<br/>                                                                  |
| [**get- \_ Anzahl**](ittimecollection-get-count.md)                 | Ruft die Anzahl der Elemente in der Auflistung ab.<br/>                                                                        |
| [**\_enumerationif erhalten**](ittimecollection-get-enumerationif.md) | Gibt die [**ienumtime**](ienumtime.md) -Enumerationsschnittstelle zurück, die [**ittime**](ittime.md)auflistet.<br/> |
| [**\_Element erhalten**](ittimecollection-get-item.md)                   | Gibt ein Element in der Auflistung zurück, wenn ein Index angegeben ist.<br/>                                                         |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3,0 oder höher<br/>                                                 |
| Header<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Bibliothek<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



 

