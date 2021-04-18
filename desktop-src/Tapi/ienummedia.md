---
description: 'Die ienummedia-Schnittstelle stellt com-Standard-Enumerationsmethoden für die ITmedia-Schnittstelle bereit. Die itmediacollection:: get \_ enumerationif-Methode gibt einen Zeiger auf ienummedia zurück.'
ms.assetid: 827f8866-2445-4b7c-88fe-eed19f48c93b
title: Ienummedia-Schnittstelle (sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7127e7d1d751ee487ad5b86326602cfcfe5aae0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352142"
---
# <a name="ienummedia-interface"></a>Ienummedia-Schnittstelle

\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet eine ähnliche Funktionalität.\]

Die **ienummedia** -Schnittstelle stellt com-Standard-Enumerationsmethoden für die [**ITmedia**](itmedia.md) -Schnittstelle bereit. Die [**itmediacollection:: get \_ enumerationif**](itmediacollection-get-enumerationif.md) -Methode gibt einen Zeiger auf **ienummedia** zurück.

## <a name="members"></a>Member

Die **ienummedia** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Ienummedia** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ienummedia** -Schnittstelle verfügt über diese Methoden.



| Methode                            | BESCHREIBUNG                                                                                        |
|:----------------------------------|:---------------------------------------------------------------------------------------------------|
| [**Klon**](ienummedia-clone.md) | Erstellt einen weiteren Enumerator, der den gleichen Enumerationszustand wie der aktuelle Enumerator enthält.<br/> |
| [**Weiter**](ienummedia-next.md)   | Ruft die nächste angegebene Anzahl von Elementen in der enumerationssequenz ab.<br/>                 |
| [**Zurücksetzen**](ienummedia-reset.md) | Setzt auf den Anfang der enumerationssequenz zurück.<br/>                                    |
| [**Überspringen**](ienummedia-skip.md)   | Überspringt die nächste angegebene Anzahl von Elementen in der enumerationssequenz.<br/>           |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3,0 oder höher<br/>                                                 |
| Header<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Bibliothek<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



 

