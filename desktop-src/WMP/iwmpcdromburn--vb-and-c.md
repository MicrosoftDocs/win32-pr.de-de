---
title: IWMPCnutzeroberfläche (VB und C) (Wmp.h)
description: Stellt Eigenschaften und Methoden zum Verwalten der Erstellung von Audio-CDs bereit.
ms.assetid: d98b243d-d6c2-4d85-8d5a-de49c62d0acf
keywords:
- IWMPCnutzeroberfläche (VB und C) Windows Media Player
- Beschriebene IWMPCnutzeroberfläche (VB und C) Windows Media Player
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
ms.openlocfilehash: 7731d5491e683c2a5d2e577c41dc96264c90f0d070538405d0fa3c3ea7283a0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118575958"
---
# <a name="iwmpcdromburn-vb-and-c-interface"></a>IWMPCnutzeroberfläche (VB und C#)

Stellt Eigenschaften und Methoden zum Verwalten der Erstellung von Audio-CDs bereit.

## <a name="members"></a>Member

Die **IWMPCnutzeroberfläche (VB und C#)** verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **IWMPCnutzeroberfläche (VB und C#)** verfügt über diese Methoden.



| Methode                                                                             | Beschreibung                                                              |
|:-----------------------------------------------------------------------------------|:-------------------------------------------------------------------------|
| [**erase**](wmplibiwmpcdromburn-iwmpcdromburn-erase--vb-and-c.md)                 | Löscht die aktuelle CD.<br/>                                        |
| [**getItemInfo**](wmplibiwmpcdromburn-iwmpcdromburn-getiteminfo-iwmpcdromburn.md) | Ruft den Wert des angegebenen Attributs für die CD ab.<br/>    |
| [**Isavailable**](wmplibiwmpcdromburn-iwmpcdromburn-isavailable--vb-and-c.md)     | Stellt Informationen zum CD-Laufwerk und den Medien bereit.<br/>            |
| [**refreshStatus**](wmplibiwmpcdromburn-iwmpcdromburn-refreshstatus--vb-and-c.md) | Aktualisiert die Statusinformationen für die aktuelle Wiedergabeliste für das Burning.<br/> |
| [**start Vererz.**](wmplibiwmpcdromburn-iwmpcdromburn-startburn--vb-and-c.md)         | Lädt die CD.<br/>                                                 |
| [**stop Vererzung**](wmplibiwmpcdromburn-iwmpcdromburn-stopburn-iwmpcdromburn.md)       | Beendet den CD-Prozess.<br/>                                 |



 

### <a name="properties"></a>Eigenschaften

Die **IWMPCnutzeroberfläche (VB und C#)** verfügt über diese Eigenschaften.



| Eigenschaft                                                                                    | Zugriffstyp          | Beschreibung                                                                 |
|:--------------------------------------------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------|
| [**burnFormat**](wmplibiwmpcdromburn-iwmpcdromburn-burnformat--vb-and-c.md)<br/>     | Schreibgeschützt<br/> | Ruft einen Wert ab, der den Typ der zu verwertenden CD angibt.<br/>              |
| [**burnPlaylist**](wmplibiwmpcdromburn-iwmpcdromburn-burnplaylist--vb-and-c.md)<br/> | Schreibgeschützt<br/> | Ruft die aktuelle Wiedergabeliste ab, die auf die CD zusammengestellt werden soll.<br/>                     |
| [**burnProgress**](wmplibiwmpcdromburn-iwmpcdromburn-burnprogress--vb-and-c.md)<br/> | Schreibgeschützt<br/> | Ruft den Fortschritt der CD als Abgeschlossen in Prozent ab.<br/>                |
| [**burnState**](wmplibiwmpcdromburn-iwmpcdromburn-burnstate--vb-and-c.md)<br/>       | Schreibgeschützt<br/> | Ruft einen Enumerationswert ab, der den aktuellen Burn-Zustand angibt.<br/> |
| [**Etikett**](wmplibiwmpcdromburn-iwmpcdromburn-label--vb-and-c.md)<br/>               | Schreibgeschützt<br/> | Ruft die CD-Volumebezeichnungszeichenfolge ab.<br/>                                 |



 

Erhalten Sie eine **IWMPCnutzeroberfläche,** indem Sie die **IWMPCaku-Schnittstelle** der CD umwandeln, die Sie verwerfen möchten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wmp.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Schnittstellen für Visual Basic .NET und C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> </dl>

 

 





