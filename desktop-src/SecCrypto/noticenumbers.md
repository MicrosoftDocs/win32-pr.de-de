---
description: Stellt eine Auflistung von Erweiterungs Objekten dar.
ms.assetid: b0d69df9-12c4-4872-b883-b029c4350502
title: Noticenenumbers-Objekt
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
ms.openlocfilehash: 58d954fdeef66d6d0e5eadb3086cb549b59e5669
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361000"
---
# <a name="noticenumbers-object"></a>Noticenenumbers-Objekt

\[Das **noticenenumbers** -Objekt ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Weitere Informationen finden Sie unter [**Qualifizierer**](qualifier.md).\]

Das **noticenenumbers** -Objekt stellt eine Auflistung von [**Erweiterungs**](extension.md) Objekten dar. Jedes [**Erweiterungs**](extension.md) Objekt stellt eine Benutzer-Benachrichtigungs Nummer dar.

## <a name="when-to-use"></a>Verwendung

Das **noticenenumbers** -Objekt wird verwendet, um die folgenden Aufgaben auszuführen:

-   Ruft die Anzahl der [**Erweiterungs**](extension.md) Objekte in der Auflistung ab.
-   Ruft ein bestimmtes [**Erweiterungs**](extension.md) Objekt aus der Auflistung ab.
-   Iterieren Sie die Auflistung.

## <a name="members"></a>Member

Das benachrichtitenenumerationsobjekt enthält diese Typen von **Membern** :

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Das **noticenenumbers** -Objekt verfügt über diese Eigenschaften.



| Eigenschaft                                              | Zugriffstyp          | BESCHREIBUNG                                                                                                                                                                                                                     |
|:------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_"Netwenum"**](noticenumbers-newenum.md)<br/> | Schreibgeschützt<br/> | Ruft eine [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) -Schnittstelle für ein Objekt ab, das zum Auflisten der Auflistung verwendet werden kann. Diese Eigenschaft wird in Visual Basic Scripting Edition (VBScript) ausgeblendet.<br/> |
| [**Countdown**](noticenumbers-count.md)<br/>       | Schreibgeschützt<br/> | Ruft die Anzahl der [**Erweiterungs**](extension.md) Objekte in der Auflistung ab.<br/>                                                                                                                                    |
| [**Element**](noticenumbers-item.md)<br/>         | Schreibgeschützt<br/> | Ruft das [**Erweiterungs**](extension.md) Objekt ab, das die indizierte Benachrichtigungs Nummer der Auflistung darstellt.<br/> Dies ist die Standard Eigenschaft.<br/>                                                            |



 

## <a name="remarks"></a>Bemerkungen

Das **noticenenumbers** -Objekt kann nicht erstellt werden.

Das noticenenumbers-Objekt wird in der [**Qualifizierer. noticenumschlag**](qualifier-noticenumbers.md) -Eigenschaft verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
