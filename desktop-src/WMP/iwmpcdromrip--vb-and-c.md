---
title: IWMPCorporaRip-Schnittstelle (VB und C) (Wmp.h)
description: Stellt Eigenschaften und Methoden zum Verwalten von Kopier- oder Löschspuren von einer Audio-CD bereit. Das Bespiel einer CD mithilfe der IWMPC usernameRip-Schnittstelle hat die gleiche Auswirkung wie die Musikausgabe mithilfe der Windows Media Player Benutzeroberfläche.
ms.assetid: d7fbfc68-61b5-45bf-8df5-e3125a51a4d8
keywords:
- IWMPCorporaRip-Schnittstelle (VB und C) Windows Media Player
- IWMPCredoRip-Schnittstelle (VB und C) Windows Media Player beschrieben
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
ms.openlocfilehash: 98a418f71ad8605e81115fa9ef1a45488a6830db94c260ef60aa0d991724d80a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117747936"
---
# <a name="iwmpcdromrip-vb-and-c-interface"></a>IWMPCorporaRip-Schnittstelle (VB und C#)

Stellt Eigenschaften und Methoden zum Verwalten von Kopier- oder *Löschspuren* von einer Audio-CD bereit.

Das Erstellen einer CD mithilfe der **IWMPC usernameRip-Schnittstelle** hat die gleiche Auswirkung wie die Musik mithilfe der Windows Media Player Benutzeroberfläche. Der Bibliothek werden automatisch inhalte gemäß den Einstellungen des Benutzers hinzugefügt. Weitere Informationen zu Benutzereinstellungen für CD-Platteing finden Sie unter "Musik von CDs wird fälschen" in Windows Media Player-Hilfe.

Die **IWMPC csvRip-Schnittstelle** macht die folgenden Eigenschaften verfügbar.

## <a name="members"></a>Member

Die **IWMPCmemberRip-Schnittstelle (VB und C#)** verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **IWMPC csvRip-Schnittstelle (VB und C#)** verfügt über diese Methoden.



| Methode                                                                 | Beschreibung                              |
|:-----------------------------------------------------------------------|:-----------------------------------------|
| [**startRip**](wmplibiwmpcdromrip-iwmpcdromrip-startrip--vb-and-c.md) | Reift die CD.<br/>                  |
| [**stopRip**](wmplibiwmpcdromrip-iwmpcdromrip-stoprip--vb-and-c.md)   | Beendet den CD-Prozess.<br/> |



 

### <a name="properties"></a>Eigenschaften

Die **IWMPC csvRip-Schnittstelle (VB und C#)** verfügt über diese Eigenschaften.



| Eigenschaft                                                                                | Zugriffstyp          | Beschreibung                                                                                   |
|:----------------------------------------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------------------------|
| [**ripProgress**](wmplibiwmpcdromrip-iwmpcdromrip-ripprogress--vb-and-c.md)<br/> | Schreibgeschützt<br/> | Ruft den CD-Status als Abgeschlossen in Prozent ab.<br/>                                  |
| [**ripState**](wmplibiwmpcdromrip-iwmpcdromrip-ripstate--vb-and-c.md)<br/>       | Schreibgeschützt<br/> | Ruft einen Enumerationswert ab, der den aktuellen Zustand des Löschprozesses angibt.<br/> |



 

Erhalten Sie eine **IWMPC csvRip-Schnittstelle,** indem Sie die **IWMPCaku-Schnittstelle** der CD umwandeln, die Sie zerrissen möchten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wmp.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Schnittstellen für Visual Basic .NET und C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[**Bearbeitung einer CD**](ripping-a-cd.md)
</dt> </dl>

 

 





