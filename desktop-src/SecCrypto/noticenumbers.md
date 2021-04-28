---
description: 'NoticeNumbers-Objekt: Stellt eine Auflistung von Extension-Objekten dar.'
ms.assetid: b0d69df9-12c4-4872-b883-b029c4350502
title: NoticeNumbers-Objekt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NoticeNumbers
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: b2bd6e653eabe9b25588fd29517ac94e0c878fdb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090758"
---
# <a name="noticenumbers-object"></a>NoticeNumbers-Objekt

\[Das **NoticeNumbers-Objekt** ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt Anforderungen angegeben sind. Weitere Informationen finden Sie unter [**Qualifizierer**](qualifier.md).\]

Das **NoticeNumbers-Objekt** stellt eine Auflistung von [**Extension-Objekten**](extension.md) dar. Jedes [**Extension-Objekt**](extension.md) stellt eine Benutzerhinweisnummer dar.

## <a name="when-to-use"></a>Verwendung

Das **NoticeNumbers-Objekt** wird verwendet, um die folgenden Aufgaben auszuführen:

-   Ruft die Anzahl der [**Extension-Objekte**](extension.md) in der Auflistung ab.
-   Ruft ein bestimmtes [**Extension-Objekt**](extension.md) aus der Auflistung ab.
-   Iterieren Sie die Auflistung.

## <a name="members"></a>Member

Das **NoticeNumbers-Objekt** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Das **NoticeNumbers-Objekt** verfügt über diese Eigenschaften.



| Eigenschaft                                              | Zugriffstyp          | BESCHREIBUNG                                                                                                                                                                                                                     |
|:------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](noticenumbers-newenum.md)<br/> | Schreibgeschützt<br/> | Ruft eine [**IEnumVARIANT-Schnittstelle**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) für ein Objekt ab, das zum Aufzählen der Auflistung verwendet werden kann. Diese Eigenschaft wird in Visual Basic Scripting Edition (VBScript) ausgeblendet.<br/> |
| [**Anzahl**](noticenumbers-count.md)<br/>       | Schreibgeschützt<br/> | Ruft die Anzahl der [**Extension-Objekte**](extension.md) in der Auflistung ab.<br/>                                                                                                                                    |
| [**Element**](noticenumbers-item.md)<br/>         | Schreibgeschützt<br/> | Ruft das [**Extension-Objekt**](extension.md) ab, das die indizierte Hinweisnummer der Auflistung darstellt.<br/> Dies ist die Standardeigenschaft.<br/>                                                            |



 

## <a name="remarks"></a>Bemerkungen

Das **NoticeNumbers-Objekt** kann nicht erstellt werden.

Das NoticeNumbers-Objekt wird in der [**Qualifier.NoticeNumbers-Eigenschaft**](qualifier-noticenumbers.md) verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2.0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
