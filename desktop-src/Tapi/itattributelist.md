---
description: Die itattributelist-Schnittstelle stellt Methoden zum erhalten und Festlegen von nicht interpretierten Attributen bereit.
ms.assetid: 12806c2e-615c-4d78-a4bb-5cc35ea21175
title: Itattributelist-Schnittstelle (sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2afbc7ab447188943c0f02e6c5a664bbcc4c6d0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352123"
---
# <a name="itattributelist-interface"></a>Itattributelist-Schnittstelle

\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet eine ähnliche Funktionalität.\]

Die **itattributelist** -Schnittstelle stellt Methoden zum erhalten und Festlegen von nicht interpretierten Attributen bereit. Bezüglich der Position der Attribut Zeichenfolgen in einem Sitzungs Deskriptor-Protokoll (SDP, siehe RFC 2327), wird von den Methoden angenommen, dass alle Attribut Zeichenfolgen direkt vor dem Angeben der Medien Attribute und nach allen allgemeinen Attributen vorhanden sind. Die **itattributelist** -Schnittstelle wird erstellt, indem **QueryInterface** für [**itdirectoryobject**](/windows/desktop/api/Rend/nn-rend-itdirectoryobject)aufgerufen wird.

## <a name="members"></a>Member

Die **itattributelist** -Schnittstelle erbt von der [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle. **Itattributelist** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **itattributelist** -Schnittstelle verfügt über diese Methoden.



| Methode                                                          | BESCHREIBUNG                                             |
|:----------------------------------------------------------------|:--------------------------------------------------------|
| [**Eren**](itattributelist-add.md)                              | Fügt das Attribut am angegebenen Index hinzu.<br/>   |
| [**Lösch**](itattributelist-delete.md)                        | Löscht das Attribut am angegebenen Index.<br/> |
| [**\_AttributeList erhalten**](itattributelist-get-attributelist.md) | Ruft die Liste der Attribute ab.<br/>                 |
| [**get- \_ Anzahl**](itattributelist-get-count.md)                 | Ruft die Anzahl der Attribute ab.<br/>               |
| [**\_Element erhalten**](itattributelist-get-item.md)                   | Ruft das durch den Index angegebene Attribut ab.<br/>   |
| [**\_AttributeList platzieren**](itattributelist-put-attributelist.md) | Legt die Liste der Attribute fest.<br/>                 |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3,0 oder höher<br/>                                                 |
| Header<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Bibliothek<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



 

