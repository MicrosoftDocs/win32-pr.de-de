---
description: Stellt die com-Standard-Enumerationsmethoden für die ipstore-Schnittstelle bereit.
ms.assetid: f5290e6c-8752-4380-9210-c96a87f000ba
title: Iumumpstoreitems-Schnittstelle (pstore. h)
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
ms.openlocfilehash: 11ca255cb13d998d16596bc7cc54d28d2415b227
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368347"
---
# <a name="ienumpstoreitems-interface"></a>Iumumpstoreitems-Schnittstelle

\[Geschützter Speicher (pstore) ist für die Verwendung in Windows Server 2003 und Windows XP verfügbar. Sie steht nur für schreibgeschützte Vorgänge in Windows Server 2008 und Windows Vista zur Verfügung, ist aber möglicherweise in nachfolgenden Versionen nicht verfügbar. Pstore verwendet eine ältere Implementierung des Schutzes von Daten. Entwicklern wird dringend empfohlen, den stärkeren Datenschutz zu nutzen, der von den Funktionen [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) und [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) bereitgestellt wird.\]

Stellt die com-Standard-Enumerationsmethoden für die [**ipstore**](ipstore.md) -Schnittstelle bereit.

## <a name="members"></a>Member

Die **iumumpstoreitems** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Ienumpstoreitems** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ierumpstoreitems** -Schnittstelle verfügt über diese Methoden.



| Methode                                  | BESCHREIBUNG                                                                                        |
|:----------------------------------------|:---------------------------------------------------------------------------------------------------|
| [**Klon**](ienumpstoreitems-clone.md) | Erstellt einen weiteren Enumerator, der den gleichen Enumerationszustand wie der aktuelle Enumerator enthält.<br/> |
| [**Weiter**](ienumpstoreitems-next.md)   | Ruft das nächste angegebene Datenelement in der enumerationssequenz ab.<br/>                          |
| [**Zurücksetzen**](ienumpstoreitems-reset.md) | Setzt auf den Anfang der enumerationssequenz zurück.<br/>                                    |
| [**Überspringen**](ienumpstoreitems-skip.md)   | Überspringt das angegebene Datenelement in der enumerationssequenz.<br/>                              |



 

## <a name="remarks"></a>Bemerkungen

Jedes Element muss nach dem auflisten freigegeben werden. Das Enumeratorobjekt muss auch freigegeben werden, wenn es nicht mehr verwendet wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Pstore. h</dt> </dl>    |
| DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



 

 
