---
description: Die ITAttributeList-Schnittstelle stellt Methoden zum Abrufen und Festlegen von nicht interpretierten Attributen bereit.
ms.assetid: 12806c2e-615c-4d78-a4bb-5cc35ea21175
title: ITAttributeList-Schnittstelle (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a8dd0ac143791a09eedbd3fe575dcecb894a1fb6dbb218c8ecfdcadf60ebd60
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117762426"
---
# <a name="itattributelist-interface"></a>ITAttributeList-Schnittstelle

\[Rendezvous IP-Telefoniekonferenz-Steuerelemente und -Schnittstellen sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet ähnliche Funktionen.\]

Die **ITAttributeList-Schnittstelle** stellt Methoden zum Abrufen und Festlegen von nicht interpretierten Attributen bereit. In Bezug auf die Position der Attributzeichenfolgen in einem SDP-Paket (Session Descriptor Protocol, siehe RFC 2327) gehen die Methoden davon aus, dass alle Attributzeichenfolgen direkt vor der Angabe der Medienattribute und nach allen allgemeinen Attributen vorhanden sind. Die **ITAttributeList-Schnittstelle** wird durch Aufrufen von **QueryInterface** für [**ITDirectoryObject erstellt.**](/windows/desktop/api/Rend/nn-rend-itdirectoryobject)

## <a name="members"></a>Member

Die **ITAttributeList-Schnittstelle** erbt von der [**IDispatch-Schnittstelle.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **ITAttributeList** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ITAttributeList-Schnittstelle** verfügt über diese Methoden.



| Methode                                                          | BESCHREIBUNG                                             |
|:----------------------------------------------------------------|:--------------------------------------------------------|
| [**Hinzufügen**](itattributelist-add.md)                              | Fügt das Attribut am angegebenen Index hinzu.<br/>   |
| [**Löschen**](itattributelist-delete.md)                        | Löscht das Attribut am angegebenen Index.<br/> |
| [**get \_ AttributeList**](itattributelist-get-attributelist.md) | Ruft die Liste der Attribute ab.<br/>                 |
| [**get \_ Count**](itattributelist-get-count.md)                 | Ruft die Anzahl der Attribute ab.<br/>               |
| [**Element \_ "get"**](itattributelist-get-item.md)                   | Ruft das vom Index angegebene Attribut ab.<br/>   |
| [**put \_ AttributeList**](itattributelist-put-attributelist.md) | Legt die Liste der Attribute fest.<br/>                 |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3.0 oder höher<br/>                                                 |
| Header<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Bibliothek<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



 

