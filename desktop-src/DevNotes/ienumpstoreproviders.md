---
description: 'IEnumPStoreProviders-Schnittstelle: Stellt COM-Standard-Enumerationsmethoden für die IPStore-Schnittstelle bereit.'
ms.assetid: d4c0482c-a751-4d41-bcd1-326878fdcf16
title: IEnumPStoreProviders-Schnittstelle (Pstore.h)
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
ms.openlocfilehash: cf203e0e6de08b6faff3d3b4a040018ec1122975
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089348"
---
# <a name="ienumpstoreproviders-interface"></a>IEnumPStoreProviders-Schnittstelle

\[Protected Storage (Pstore) ist für die Verwendung in Windows Server 2003 und Windows XP verfügbar. Es ist nur für schreibgeschützte Vorgänge in Windows Server 2008 und Windows Vista verfügbar, aber in nachfolgenden Versionen möglicherweise nicht verfügbar. Pstore verwendet eine ältere Implementierung des Datenschutzes. Entwicklern wird dringend empfohlen, den stärkeren Datenschutz zu nutzen, der von den [**Funktionen CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) und [**CryptUnprotectData bereitgestellt**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) wird.\]

Stellt COM-Standard-Enumerationsmethoden für die [**IPStore-Schnittstelle**](ipstore.md) bereit.

## <a name="members"></a>Member

Die **IEnumPStoreProviders-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IEnumPStoreProviders** verfügt auch über diese Membertypen:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IEnumPStoreProviders-Schnittstelle** verfügt über diese Methoden.



| Methode                                      | BESCHREIBUNG                                                                                        |
|:--------------------------------------------|:---------------------------------------------------------------------------------------------------|
| [**Klon**](ienumpstoreproviders-clone.md) | Erstellt einen weiteren Enumerator, der den gleichen Enumerationszustand wie der aktuelle Enumerator enthält.<br/> |
| [**Weiter**](ienumpstoreproviders-next.md)   | Ruft den nächsten angegebenen Anbieter in der Enumerationssequenz ab.<br/>                           |
| [**Reset**](ienumpstoreproviders-reset.md) | Setzt auf den Anfang der Enumerationssequenz zurück.<br/>                                    |
| [**Überspringen**](ienumpstoreproviders-skip.md)   | Überspringt den angegebenen Anbieter in der Enumerationssequenz.<br/>                               |



 

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Pstore.h</dt> </dl>    |
| DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



 

 
