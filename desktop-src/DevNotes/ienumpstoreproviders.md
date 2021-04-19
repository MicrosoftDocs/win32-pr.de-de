---
description: Stellt com-Standard-Enumerationsmethoden für die ipstore-Schnittstelle bereit.
ms.assetid: d4c0482c-a751-4d41-bcd1-326878fdcf16
title: Ienumpstoreproviders-Schnittstelle (pstore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreProviders
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: e01bd28722fdb4d5a0ff7e3db4f715ddc1df2315
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356051"
---
# <a name="ienumpstoreproviders-interface"></a>Ienumpstoreproviders-Schnittstelle

\[Geschützter Speicher (pstore) ist für die Verwendung in Windows Server 2003 und Windows XP verfügbar. Sie steht nur für schreibgeschützte Vorgänge in Windows Server 2008 und Windows Vista zur Verfügung, ist aber möglicherweise in nachfolgenden Versionen nicht verfügbar. Pstore verwendet eine ältere Implementierung des Schutzes von Daten. Entwicklern wird dringend empfohlen, den stärkeren Datenschutz zu nutzen, der von den Funktionen [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) und [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) bereitgestellt wird.\]

Stellt com-Standard-Enumerationsmethoden für die [**ipstore**](ipstore.md) -Schnittstelle bereit.

## <a name="members"></a>Member

Die **ienumpstoreproviders** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Ienumpstoreproviders** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ienumpstoreproviders** -Schnittstelle verfügt über diese Methoden.



| Methode                                      | BESCHREIBUNG                                                                                        |
|:--------------------------------------------|:---------------------------------------------------------------------------------------------------|
| [**Klon**](ienumpstoreproviders-clone.md) | Erstellt einen weiteren Enumerator, der den gleichen Enumerationszustand wie der aktuelle Enumerator enthält.<br/> |
| [**Weiter**](ienumpstoreproviders-next.md)   | Ruft den nächsten angegebenen Anbieter in der enumerationssequenz ab.<br/>                           |
| [**Zurücksetzen**](ienumpstoreproviders-reset.md) | Setzt auf den Anfang der enumerationssequenz zurück.<br/>                                    |
| [**Überspringen**](ienumpstoreproviders-skip.md)   | Überspringt den angegebenen Anbieter in der enumerationssequenz.<br/>                               |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Pstore. h</dt> </dl>    |
| DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



 

 
