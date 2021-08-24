---
title: IWMPError-Schnittstelle (VB und C ) (Wmp.h)
description: Stellt Eigenschaften und Methoden für den Zugriff auf eine Auflistung von IWMPErrorItem-Schnittstellen zum Abrufen von Fehlerinformationen bereit. Die IWMPError-Schnittstelle macht die folgenden Eigenschaften verfügbar.
ms.assetid: c7d9f834-43ed-40a2-95a3-b1633f025118
keywords:
- IWMPError-Schnittstelle (VB und C) Windows Media Player
- IWMPError-Schnittstelle (VB und C) Windows Media Player , beschrieben
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
ms.openlocfilehash: 5f3ff7635e423d70447e371d61fbbadf02aa14c2476e118be79cbb25d974348b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119736180"
---
# <a name="iwmperror-vb-and-c-interface"></a>IWMPError-Schnittstelle (VB und C#)

Stellt Eigenschaften und Methoden für den Zugriff auf eine Auflistung von **IWMPErrorItem-Schnittstellen zum** Abrufen von Fehlerinformationen bereit.

Die **IWMPError-Schnittstelle** macht die folgenden Eigenschaften verfügbar.

## <a name="members"></a>Member

Die **IWMPError-Schnittstelle (VB und C#)** verfügt über die folgenden Membertypen:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **IWMPError-Schnittstelle (VB und C#)** verfügt über diese Methoden.



| Methode                                                                         | Beschreibung                                                                                                                                   |
|:-------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------|
| [**clearErrorQueue**](wmplibiwmperror-iwmperror-clearerrorqueue--vb-and-c.md) | Entfernt die Fehler aus der Fehlerwarteschlange.<br/>                                                                                            |
| [**Webhelp**](wmplibiwmperror-iwmperror-webhelp--vb-and-c.md)                 | Startet die Microsoft Windows Media Player-Webhilfeseite, um weitere Informationen zum ersten Fehler in der Fehlerwarteschlange anzuzeigen.<br/> |



 

### <a name="properties"></a>Eigenschaften

Die **IWMPError-Schnittstelle (VB und C#)** verfügt über diese Eigenschaften.



| Eigenschaft                                                                        | Zugriffstyp           | Beschreibung                                                                                                                         |
|:--------------------------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------------------------------------|
| [**errorCount**](wmplibiwmperror-iwmperror-errorcount--vb-and-c.md)<br/> | Schreibgeschützt<br/>  | Ruft die Anzahl der Fehler in der Fehlerwarteschlange ab.<br/>                                                                            |
| [**Element**](iwmperror-item--vb-and-c.md)<br/>                             | Lesen/Schreiben<br/> | Ruft eine **IWMPErrorItem-Schnittstelle** am angegebenen Index in der Fehlerwarteschlange ab. In C# ist dies die **get \_ Item-Methode.**<br/> |



 

Verwenden Sie die folgende Eigenschaft, um eine **IWMPError-Schnittstelle** zu erhalten.



| Object                                                                   | Eigenschaft                                                       |
|--------------------------------------------------------------------------|----------------------------------------------------------------|
| [AxWindowsMediaPlayer-Objekt](axwindowsmediaplayer-object--vb-and-c.md) | [**Fehler**](axwmplib-axwindowsmediaplayer-error--vb-and-c.md) |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wmp.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Schnittstellen für Visual Basic .NET und C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[**IWMPErrorItem-Schnittstelle (VB und C#)**](iwmperroritem--vb-and-c.md)
</dt> </dl>

 

 





