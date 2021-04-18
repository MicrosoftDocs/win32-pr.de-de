---
description: Stellt com-Standard-Enumerationsmethoden für die ipstore-Schnittstelle bereit.
ms.assetid: a90bc5cf-ca42-4007-a57b-be9c59d9552a
title: Iumumpstoretypes-Schnittstelle (pstore. h)
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
ms.openlocfilehash: 748f6e21701fdd27c2a88d1959b0b29cf56929f6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371503"
---
# <a name="ienumpstoretypes-interface"></a>Iumumpstoretypes-Schnittstelle

\[Geschützter Speicher (pstore) ist für die Verwendung in Windows Server 2003 und Windows XP verfügbar. Sie steht nur für schreibgeschützte Vorgänge in Windows Server 2008 und Windows Vista zur Verfügung, ist aber möglicherweise in nachfolgenden Versionen nicht verfügbar. Pstore verwendet eine ältere Implementierung des Schutzes von Daten. Entwicklern wird dringend empfohlen, den stärkeren Datenschutz zu nutzen, der von den Funktionen [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) und [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) bereitgestellt wird.\]

Stellt com-Standard-Enumerationsmethoden für die [**ipstore**](ipstore.md) -Schnittstelle bereit.

## <a name="members"></a>Member

Die **ierumpstoretypes** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Ienumpstoretypes** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ierumpstoretypes** -Schnittstelle verfügt über diese Methoden.



| Methode                                  | BESCHREIBUNG                                                                                        |
|:----------------------------------------|:---------------------------------------------------------------------------------------------------|
| [**Klon**](ienumpstoretypes-clone.md) | Erstellt einen weiteren Enumerator, der den gleichen Enumerationszustand wie der aktuelle Enumerator enthält.<br/> |
| [**Weiter**](ienumpstoretypes-next.md)   | Ruft den nächsten angegebenen Anbietertyp in der enumerationssequenz ab.<br/>                      |
| [**Zurücksetzen**](ienumpstoretypes-reset.md) | Setzt auf den Anfang der enumerationssequenz zurück.<br/>                                    |
| [**Überspringen**](ienumpstoretypes-skip.md)   | Überspringt den angegebenen Anbietertyp in der enumerationssequenz.<br/>                          |



 

## <a name="remarks"></a>Bemerkungen

Das Enumeratorobjekt muss freigegeben werden, wenn es nicht mehr verwendet wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Pstore. h</dt> </dl>    |
| DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



 

 
