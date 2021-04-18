---
title: Iwmpcdromburn-Schnittstelle (VB und C) (WMP. h)
description: Stellt Eigenschaften und Methoden zum Verwalten der Erstellung von AudioCDs bereit.
ms.assetid: d98b243d-d6c2-4d85-8d5a-de49c62d0acf
keywords:
- Iwmpcdromburn (VB und C) Interface Windows Media Player
- Iwmpcdromburn (VB und C) Interface Windows Media Player, beschrieben
topic_type:
- apiref
api_name:
- IWMPCdromBurn (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2fe21a20194f57e4a8b52a3ba05032a07cb31f9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372178"
---
# <a name="iwmpcdromburn-vb-and-c-interface"></a>Iwmpcdromburn-Schnittstelle (VB und c#)

Stellt Eigenschaften und Methoden zum Verwalten der Erstellung von AudioCDs bereit.

## <a name="members"></a>Member

Die **iwmpcdromburn-Schnittstelle (VB und c#)** verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **iwmpcdromburn-Schnittstelle (VB und c#)** verfügt über diese Methoden.



| Methode                                                                             | BESCHREIBUNG                                                              |
|:-----------------------------------------------------------------------------------|:-------------------------------------------------------------------------|
| [**erase**](wmplibiwmpcdromburn-iwmpcdromburn-erase--vb-and-c.md)                 | Löscht die aktuelle CD.<br/>                                        |
| [**getItemInfo**](wmplibiwmpcdromburn-iwmpcdromburn-getiteminfo-iwmpcdromburn.md) | Ruft den Wert des angegebenen Attributs für die CD ab.<br/>    |
| [**isAvailable**](wmplibiwmpcdromburn-iwmpcdromburn-isavailable--vb-and-c.md)     | Stellt Informationen über das CD-Laufwerk und die Medien bereit.<br/>            |
| [**aktuasestatus**](wmplibiwmpcdromburn-iwmpcdromburn-refreshstatus--vb-and-c.md) | Aktualisiert die Statusinformationen für die aktuelle Burn-Wiedergabeliste.<br/> |
| [**startburn**](wmplibiwmpcdromburn-iwmpcdromburn-startburn--vb-and-c.md)         | Verbrennt die CD.<br/>                                                 |
| [**stopburn**](wmplibiwmpcdromburn-iwmpcdromburn-stopburn-iwmpcdromburn.md)       | Beendet den Vorgang zum Brennen der CD.<br/>                                 |



 

### <a name="properties"></a>Eigenschaften

Die **iwmpcdromburn-Schnittstelle (VB und c#)** verfügt über diese Eigenschaften.



| Eigenschaft                                                                                    | Zugriffstyp          | BESCHREIBUNG                                                                 |
|:--------------------------------------------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------|
| [**burnformat**](wmplibiwmpcdromburn-iwmpcdromburn-burnformat--vb-and-c.md)<br/>     | Schreibgeschützt<br/> | Ruft einen Wert ab, der den Typ der zu brennenden CD angibt.<br/>              |
| [**burnwiedergabe**](wmplibiwmpcdromburn-iwmpcdromburn-burnplaylist--vb-and-c.md)<br/> | Schreibgeschützt<br/> | Ruft die aktuelle Wiedergabeliste ab, die auf die CD gebrannt werden soll.<br/>                     |
| [**burnprogress**](wmplibiwmpcdromburn-iwmpcdromburn-burnprogress--vb-and-c.md)<br/> | Schreibgeschützt<br/> | Ruft den Fortschritt der CD-Verbrennung als Prozentsatz ab.<br/>                |
| [**burnstate**](wmplibiwmpcdromburn-iwmpcdromburn-burnstate--vb-and-c.md)<br/>       | Schreibgeschützt<br/> | Ruft einen Enumerationswert ab, der den aktuellen Brenn Zustand angibt.<br/> |
| [**ETI**](wmplibiwmpcdromburn-iwmpcdromburn-label--vb-and-c.md)<br/>               | Schreibgeschützt<br/> | Ruft die Zeichenfolge der CD-Volumebezeichnung ab.<br/>                                 |



 

Sie erhalten eine **iwmpcdromburn** -Schnittstelle durch Umwandeln der **iwmpcdrom** -Schnittstelle der CD, die Sie brennen möchten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>WMP. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Schnittstellen für Visual Basic .net und C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> </dl>

 

 





