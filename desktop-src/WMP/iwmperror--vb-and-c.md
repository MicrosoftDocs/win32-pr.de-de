---
title: Iwmperror (VB und C)-Schnittstelle (WMP. h)
description: Stellt Eigenschaften und Methoden für den Zugriff auf eine Auflistung von iwmperroritem-Schnittstellen zum Abrufen von Fehlerinformationen bereit. Die iwmperror-Schnittstelle macht die folgenden Eigenschaften verfügbar.
ms.assetid: c7d9f834-43ed-40a2-95a3-b1633f025118
keywords:
- Iwmperror (VB und C) Interface Windows Media Player
- Iwmperror (VB und C) Interface Windows Media Player, beschrieben
topic_type:
- apiref
api_name:
- IWMPError (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 289a39093c38e7a4b0cc43cb8f318e321ae8ef53
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359378"
---
# <a name="iwmperror-vb-and-c-interface"></a>Iwmperror (VB und c#)-Schnittstelle

Stellt Eigenschaften und Methoden für den Zugriff auf eine Auflistung von **iwmperroritem** -Schnittstellen zum Abrufen von Fehlerinformationen bereit.

Die **iwmperror** -Schnittstelle macht die folgenden Eigenschaften verfügbar.

## <a name="members"></a>Member

Die **iwmperror (VB und c#)** -Schnittstelle verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **iwmperror (VB und c#)** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                         | BESCHREIBUNG                                                                                                                                   |
|:-------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------|
| [**clearerrorqueue**](wmplibiwmperror-iwmperror-clearerrorqueue--vb-and-c.md) | Löscht die Fehler in der Fehler Warteschlange.<br/>                                                                                            |
| [**WebHelp**](wmplibiwmperror-iwmperror-webhelp--vb-and-c.md)                 | Öffnet die Microsoft Windows Media Player-Webhilfe Seite, um weitere Informationen zum ersten Fehler in der Fehler Warteschlange anzuzeigen.<br/> |



 

### <a name="properties"></a>Eigenschaften

Die **iwmperror (VB und c#)** -Schnittstelle verfügt über diese Eigenschaften.



| Eigenschaft                                                                        | Zugriffstyp           | BESCHREIBUNG                                                                                                                         |
|:--------------------------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------------------------------------|
| [**errorCount**](wmplibiwmperror-iwmperror-errorcount--vb-and-c.md)<br/> | Schreibgeschützt<br/>  | Ruft die Anzahl der Fehler in der Fehler Warteschlange ab.<br/>                                                                            |
| [**Element**](iwmperror-item--vb-and-c.md)<br/>                             | Lesen/Schreiben<br/> | Ruft eine **iwmperroritem** -Schnittstelle am angegebenen Index in der Fehler Warteschlange ab. In c# ist dies die **get \_ Item** -Methode.<br/> |



 

Verwenden Sie die folgende Eigenschaft, um eine **iwmperror** -Schnittstelle zu erhalten.



| Object                                                                   | Eigenschaft                                                       |
|--------------------------------------------------------------------------|----------------------------------------------------------------|
| [AxWindowsMediaPlayer-Objekt](axwindowsmediaplayer-object--vb-and-c.md) | [**Fehler**](axwmplib-axwindowsmediaplayer-error--vb-and-c.md) |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>WMP. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Schnittstellen für Visual Basic .net und C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[**Iwmperroritem-Schnittstelle (VB und c#)**](iwmperroritem--vb-and-c.md)
</dt> </dl>

 

 





