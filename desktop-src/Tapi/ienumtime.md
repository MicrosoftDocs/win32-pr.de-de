---
description: 'Die ienumtime-Schnittstelle stellt com-Standard-Enumerationsmethoden für die ittime-Schnittstelle bereit. Die ittimecollection:: get \_ enumerationif-Methode gibt einen Zeiger auf ienumtime zurück.'
ms.assetid: 395d7830-9a70-473a-8a89-4b4db48d5774
title: Ienumtime-Schnittstelle (sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2336f435ec322694847c776ac92ade93e8791207
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370730"
---
# <a name="ienumtime-interface"></a>Ienumtime-Schnittstelle

\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet eine ähnliche Funktionalität.\]

Die **ienumtime** -Schnittstelle stellt com-Standard-Enumerationsmethoden für die [**ittime**](ittime.md) -Schnittstelle bereit. Die [**ittimecollection:: get \_ enumerationif**](ittimecollection-get-enumerationif.md) -Methode gibt einen Zeiger auf **ienumtime** zurück.

## <a name="members"></a>Member

Die **ienumtime** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Ienumtime** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ienumtime** -Schnittstelle verfügt über diese Methoden.



| Methode                           | BESCHREIBUNG                                                                                        |
|:---------------------------------|:---------------------------------------------------------------------------------------------------|
| [**Klon**](ienumtime-clone.md) | Erstellt einen weiteren Enumerator, der den gleichen Enumerationszustand wie der aktuelle Enumerator enthält.<br/> |
| [**Weiter**](ienumtime-next.md)   | Ruft die nächste angegebene Anzahl von Elementen in der enumerationssequenz ab.<br/>                 |
| [**Zurücksetzen**](ienumtime-reset.md) | Setzt auf den Anfang der enumerationssequenz zurück.<br/>                                    |
| [**Überspringen**](ienumtime-skip.md)   | Überspringt die nächste angegebene Anzahl von Elementen in der enumerationssequenz.<br/>           |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3,0 oder höher<br/>                                                 |
| Header<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Bibliothek<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



 

