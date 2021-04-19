---
description: 'Die ienumparticipants-Schnittstelle stellt com-Standard-Enumerationsmethoden für die itparticipants-Schnittstelle bereit. Die itparticipantcontrol:: enumerateparticipants-Methode gibt einen Zeiger auf ienumteilnehmer zurück.'
ms.assetid: 8534d102-06ce-4e82-8f9c-9ab9f0d14df9
title: Ienumteilnehmer-Schnittstelle (confpriv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21a20a2cd8e72c5c44b054fc4658b304c8b4fa41
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370238"
---
# <a name="ienumparticipant-interface"></a>Ienumteilnehmer-Schnittstelle

\[**Ienumteilnehmer** ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet eine ähnliche Funktionalität.\]

Die **ienumparticipants** -Schnittstelle stellt com-Standard-Enumerationsmethoden für die [**itparticipants**](itparticipant.md) -Schnittstelle bereit. Die [**itparticipantcontrol:: enumerateparticipants**](itparticipantcontrol-enumerateparticipants.md) -Methode gibt einen Zeiger auf **ienumteilnehmer** zurück.

Die **ienumteilnehmer** -Schnittstelle ist in Visual Basic-und Skriptsprachen ausgeblendet.

## <a name="members"></a>Member

Die **ienumparticipants** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Ienumparticipants** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ienumparticipants** -Schnittstelle verfügt über diese Methoden.



| Methode                                  | BESCHREIBUNG                                                                                        |
|:----------------------------------------|:---------------------------------------------------------------------------------------------------|
| [**Klon**](ienumparticipant-clone.md) | Erstellt einen weiteren Enumerator, der den gleichen Enumerationszustand wie der aktuelle Enumerator enthält.<br/> |
| [**Weiter**](ienumparticipant-next.md)   | Ruft die nächste angegebene Anzahl von Elementen in der enumerationssequenz ab.<br/>                 |
| [**Zurücksetzen**](ienumparticipant-reset.md) | Setzt auf den Anfang der enumerationssequenz zurück.<br/>                                    |
| [**Überspringen**](ienumparticipant-skip.md)   | Überspringt die nächste angegebene Anzahl von Elementen in der enumerationssequenz.<br/>           |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3,0 oder höher<br/>                                                 |
| Header<br/>       | <dl> <dt>"Confpriv. h"</dt> </dl> |
| Bibliothek<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Itteilnehmer**](itparticipant.md)
</dt> </dl>

 

