---
title: Iwmpcdromrip-Schnittstelle (VB und C) (WMP. h)
description: Stellt Eigenschaften und Methoden zum Verwalten von Kopier-oder einreißen-Spuren von einer AudioCD bereit. das einreißen einer CD mithilfe der iwmpcdromrip-Schnittstelle hat denselben Effekt wie das einreißen von Musik mithilfe der Windows Media Player-Benutzeroberfläche.
ms.assetid: d7fbfc68-61b5-45bf-8df5-e3125a51a4d8
keywords:
- Iwmpcdromrip (VB und C) Interface Windows Media Player
- Iwmpcdromrip (VB und C) Interface Windows Media Player, beschrieben
topic_type:
- apiref
api_name:
- IWMPCdromRip (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d069fd8bd727d6a2a380c2ef29ce7c086db88d0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372054"
---
# <a name="iwmpcdromrip-vb-and-c-interface"></a>Iwmpcdromrip-Schnittstelle (VB und c#)

Stellt Eigenschaften und Methoden zum Verwalten von Kopier-oder *einreißen*-Spuren von einer AudioCD bereit.

Das einreißen einer CD mithilfe der **iwmpcdromrip** -Schnittstelle hat die gleiche Wirkung wie das einreißen von Musik mithilfe der Windows Media Player-Benutzeroberfläche. Ausgerigter Inhalt wird der Bibliothek automatisch entsprechend den Einstellungen des Benutzers hinzugefügt. Weitere Informationen zu den Benutzereinstellungen für das CD-Ripping finden Sie unter "Ripping Music from CDs" in der Windows Media Player-Hilfe.

Die **iwmpcdromrip** -Schnittstelle macht die folgenden Eigenschaften verfügbar.

## <a name="members"></a>Member

Die **iwmpcdromrip-Schnittstelle (VB und c#)** verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **iwmpcdromrip-Schnittstelle (VB und c#)** verfügt über diese Methoden.



| Methode                                                                 | BESCHREIBUNG                              |
|:-----------------------------------------------------------------------|:-----------------------------------------|
| [**startrip**](wmplibiwmpcdromrip-iwmpcdromrip-startrip--vb-and-c.md) | Rippt die CD.<br/>                  |
| [**stoprip**](wmplibiwmpcdromrip-iwmpcdromrip-stoprip--vb-and-c.md)   | Hält den CD-einreißen-Prozess an.<br/> |



 

### <a name="properties"></a>Eigenschaften

Die **iwmpcdromrip-Schnittstelle (VB und c#)** verfügt über diese Eigenschaften.



| Eigenschaft                                                                                | Zugriffstyp          | BESCHREIBUNG                                                                                   |
|:----------------------------------------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------------------------|
| [**ripprogress**](wmplibiwmpcdromrip-iwmpcdromrip-ripprogress--vb-and-c.md)<br/> | Schreibgeschützt<br/> | Ruft den Status des CD-einreißen als Prozentsatz ab.<br/>                                  |
| [**ripstate**](wmplibiwmpcdromrip-iwmpcdromrip-ripstate--vb-and-c.md)<br/>       | Schreibgeschützt<br/> | Ruft einen Enumerationswert ab, der den aktuellen Zustand des rippingprozesses angibt.<br/> |



 

Sie erhalten eine **iwmpcdromrip** -Schnittstelle durch Umwandeln der **iwmpcdrom** -Schnittstelle der CD, die Sie zerreißen möchten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>WMP. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Schnittstellen für Visual Basic .net und C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[**Ripping einer CD**](ripping-a-cd.md)
</dt> </dl>

 

 





