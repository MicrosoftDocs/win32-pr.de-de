---
title: IWMPControls3-Schnittstelle (VB und C) (WMP. h)
description: Stellt Eigenschaften und Methoden für die Auswahl und Unterstützung der Audiosprache bereit, die die IWMPControls2-Schnittstelle ergänzen. Zusätzlich zu den Eigenschaften und Methoden, die von IWMPControls2 geerbt werden, macht die IWMPControls3-Schnittstelle die folgenden Eigenschaften verfügbar.
ms.assetid: 1f42a352-da97-4382-9b59-a9b074aa2a5a
keywords:
- IWMPControls3 (VB und C) Interface Windows Media Player
- IWMPControls3 (VB und C) Interface Windows Media Player, beschrieben
topic_type:
- apiref
api_name:
- IWMPControls3 (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9788dbd1b5910d655cbaa17055c76a0ae6d0280e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372635"
---
# <a name="iwmpcontrols3-vb-and-c-interface"></a>IWMPControls3-Schnittstelle (VB und c#)

Stellt Eigenschaften und Methoden für die Auswahl und Unterstützung der Audiosprache bereit, die die **IWMPControls2** -Schnittstelle ergänzen.

Zusätzlich zu den Eigenschaften und Methoden, die von **IWMPControls2** geerbt werden, macht die **IWMPControls3** -Schnittstelle die folgenden Eigenschaften verfügbar.

## <a name="members"></a>Member

Die IWMPControls3-Schnittstelle **(VB und c#)** verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die IWMPControls3-Schnittstelle **(VB und c#)** verfügt über diese Methoden.



| Methode                                                                                                         | BESCHREIBUNG                                                                                               |
|:---------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------|
| [**getaudiolanguagedescription**](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguagedescription--vb-and-c.md) | Gibt die Beschreibung für die Audiosprache zurück, die dem angegebenen 1-basierten Index entspricht.<br/> |
| [**getaudiolanguageid**](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguageid--vb-and-c.md)                   | Gibt die LCID für einen angegebenen audiosprachindex zurück.<br/>                                         |
| [**getlanguagename**](wmplibiwmpcontrols3-iwmpcontrols3-getlanguagename--vb-and-c.md)                         | Gibt den Namen der Audiosprache mit der angegebenen LCID zurück.<br/>                                |



 

### <a name="properties"></a>Eigenschaften

Die IWMPControls3-Schnittstelle **(VB und c#)** verfügt über diese Eigenschaften.



| Eigenschaft                                                                                                              | Zugriffstyp           | BESCHREIBUNG                                                                                                                                         |
|:----------------------------------------------------------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**audiolanguagecount**](wmplibiwmpcontrols3-iwmpcontrols3-audiolanguagecount--vb-and-c.md)<br/>               | Schreibgeschützt<br/>  | Ruft die Anzahl unterstützter Audiosprachen ab. <br/>                                                                                            |
| [**currentaudiolanguage**](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguage--vb-and-c.md)<br/>           | Lesen/Schreiben<br/> | Ruft den Gebiets Schema Bezeichner (LCID) der Audiosprache für die Wiedergabe ab oder legt ihn fest. <br/>                                                           |
| [**currentaudiolanguageindex**](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguageindex--vb-and-c.md)<br/> | Lesen/Schreiben<br/> | Ruft den 1-basierten Index ab, der der Audiosprache für die Wiedergabe entspricht, oder legt diesen fest. <br/>                                                   |
| [**currentPositionTimecode**](wmplibiwmpcontrols3-iwmpcontrols3-currentpositiontimecode--vb-and-c.md)<br/>     | Lesen/Schreiben<br/> | Ruft die aktuelle Position im aktuellen Medien Element mithilfe eines Zeit Code Formats ab oder legt diese fest. Diese Eigenschaft unterstützt derzeit den SMPTE-Zeit Code. <br/> |



 

Sie erhalten eine **IWMPControls3** -Schnittstelle durch Umwandeln des Werts, der von der [**AxWindowsMediaPlayer. ctlcontrols**](axwmplib-axwindowsmediaplayer-ctlcontrols--vb-and-c.md) -Eigenschaft zurückgegeben wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>WMP. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Schnittstellen für Visual Basic .net und C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[**Iwmpcontrols-Schnittstelle (VB und c#)**](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[**IWMPControls2-Schnittstelle (VB und c#)**](iwmpcontrols2--vb-and-c.md)
</dt> </dl>

 

 





