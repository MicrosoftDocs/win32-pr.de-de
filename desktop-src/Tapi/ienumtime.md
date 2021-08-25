---
description: Die IEnumTime-Schnittstelle stellt COM-Standard-Enumerationsmethoden für die ITTime-Schnittstelle bereit. Die ITTimeCollection::get \_ EnumerationIf-Methode gibt einen Zeiger auf IEnumTime zurück.
ms.assetid: 395d7830-9a70-473a-8a89-4b4db48d5774
title: IEnumTime-Schnittstelle (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c79d780374bcf121dcb5010aef51725f9836e511bed4b86c855970bb47b838e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119992200"
---
# <a name="ienumtime-interface"></a>IEnumTime-Schnittstelle

\[Rendezvous-IP-Telefoniekonferenz-Steuerelemente und -Schnittstellen sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet ähnliche Funktionen.\]

Die **IEnumTime-Schnittstelle** stellt COM-Standard-Enumerationsmethoden für die [**ITTime-Schnittstelle**](ittime.md) bereit. Die [**ITTimeCollection::get \_ EnumerationIf-Methode**](ittimecollection-get-enumerationif.md) gibt einen Zeiger auf **IEnumTime** zurück.

## <a name="members"></a>Member

Die **IEnumTime-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IEnumTime** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IEnumTime-Schnittstelle** verfügt über diese Methoden.



| Methode                           | Beschreibung                                                                                        |
|:---------------------------------|:---------------------------------------------------------------------------------------------------|
| [**Klon**](ienumtime-clone.md) | Erstellt einen weiteren Enumerator, der den gleichen Enumerationszustand wie der aktuelle Enumerator enthält.<br/> |
| [**Weiter**](ienumtime-next.md)   | Ruft die nächste angegebene Anzahl von Elementen in der Enumerationssequenz ab.<br/>                 |
| [**Zurücksetzen**](ienumtime-reset.md) | Setzt auf den Anfang der Enumerationssequenz zurück.<br/>                                    |
| [**Überspringen**](ienumtime-skip.md)   | Überspringt die nächste angegebene Anzahl von Elementen in der Enumerationssequenz.<br/>           |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3.0 oder höher<br/>                                                 |
| Header<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Bibliothek<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



 

