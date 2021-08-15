---
description: Stellt die COM-Standard-Enumerationsmethoden für die IPStore-Schnittstelle bereit.
ms.assetid: f5290e6c-8752-4380-9210-c96a87f000ba
title: IEnumPStoreItems-Schnittstelle (Pstore.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreItems
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: f5952dbaff2560ae4c2fc59af73246c2cd5c1d050bb53bc3c7b9091c8a39822f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119542240"
---
# <a name="ienumpstoreitems-interface"></a>IEnumPStoreItems-Schnittstelle

\[Protected Storage (Pstore) ist für die Verwendung in Windows Server 2003 und Windows XP verfügbar. Sie ist nur für schreibgeschützte Vorgänge in Windows Server 2008 und Windows Vista verfügbar, ist in nachfolgenden Versionen jedoch möglicherweise nicht verfügbar. Pstore verwendet eine ältere Implementierung des Datenschutzes. Entwicklern wird dringend empfohlen, den verstärkten Datenschutz zu nutzen, der von den Funktionen [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) und [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) bereitgestellt wird.\]

Stellt die COM-Standard-Enumerationsmethoden für die [**IPStore-Schnittstelle**](ipstore.md) bereit.

## <a name="members"></a>Member

Die **IEnumPStoreItems-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IEnumPStoreItems** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IEnumPStoreItems-Schnittstelle** verfügt über diese Methoden.



| Methode                                  | BESCHREIBUNG                                                                                        |
|:----------------------------------------|:---------------------------------------------------------------------------------------------------|
| [**Klon**](ienumpstoreitems-clone.md) | Erstellt einen weiteren Enumerator, der den gleichen Enumerationszustand wie der aktuelle Enumerator enthält.<br/> |
| [**Weiter**](ienumpstoreitems-next.md)   | Ruft das nächste angegebene Datenelement in der Enumerationssequenz ab.<br/>                          |
| [**Zurücksetzen**](ienumpstoreitems-reset.md) | Setzt auf den Anfang der Enumerationssequenz zurück.<br/>                                    |
| [**Überspringen**](ienumpstoreitems-skip.md)   | Überspringt das angegebene Datenelement in der Enumerationssequenz.<br/>                              |



 

## <a name="remarks"></a>Hinweise

Nach dem Aufzählen muss jedes Element freigegeben werden. Das Enumeratorobjekt muss auch freigegeben werden, wenn es nicht mehr verwendet wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Pstore.h</dt> </dl>    |
| DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



 

 
