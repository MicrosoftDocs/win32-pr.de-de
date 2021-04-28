---
description: 'IEnumPStoreTypes-Schnittstelle: Stellt COM-Standard-Enumerationsmethoden für die IPStore-Schnittstelle bereit.'
ms.assetid: a90bc5cf-ca42-4007-a57b-be9c59d9552a
title: IEnumPStoreTypes-Schnittstelle (Pstore.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreTypes
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 7ca2e250864889a5fda465e146287bf59a2b6346
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089358"
---
# <a name="ienumpstoretypes-interface"></a>IEnumPStoreTypes-Schnittstelle

\[Protected Storage (Pstore) ist für die Verwendung in Windows Server 2003 und Windows XP verfügbar. Es ist nur für schreibgeschützte Vorgänge in Windows Server 2008 und Windows Vista verfügbar, aber in nachfolgenden Versionen möglicherweise nicht verfügbar. Pstore verwendet eine ältere Implementierung des Datenschutzes. Entwicklern wird dringend empfohlen, den stärkeren Datenschutz zu nutzen, der von den [**Funktionen CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) und [**CryptUnprotectData bereitgestellt**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) wird.\]

Stellt COM-Standard-Enumerationsmethoden für die [**IPStore-Schnittstelle**](ipstore.md) bereit.

## <a name="members"></a>Member

Die **IEnumPStoreTypes-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IEnumPStoreTypes** verfügt auch über diese Membertypen:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IEnumPStoreTypes-Schnittstelle** verfügt über diese Methoden.



| Methode                                  | BESCHREIBUNG                                                                                        |
|:----------------------------------------|:---------------------------------------------------------------------------------------------------|
| [**Klon**](ienumpstoretypes-clone.md) | Erstellt einen weiteren Enumerator, der den gleichen Enumerationszustand wie der aktuelle Enumerator enthält.<br/> |
| [**Weiter**](ienumpstoretypes-next.md)   | Ruft den nächsten angegebenen Anbietertyp in der Enumerationssequenz ab.<br/>                      |
| [**Reset**](ienumpstoretypes-reset.md) | Setzt auf den Anfang der Enumerationssequenz zurück.<br/>                                    |
| [**Überspringen**](ienumpstoretypes-skip.md)   | Überspringt den angegebenen Anbietertyp in der Enumerationssequenz.<br/>                          |



 

## <a name="remarks"></a>Bemerkungen

Das Enumeratorobjekt muss freigegeben werden, wenn es nicht mehr verwendet wird.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Pstore.h</dt> </dl>    |
| DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



 

 
