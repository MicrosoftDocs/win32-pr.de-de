---
description: Die notifyparser-allevelchange-Methode aktiviert oder deaktiviert die Ereignis Behandlung für Befehle der temporären Jugend Verwaltungsebene.
ms.assetid: c8252cc6-a83f-4cce-ba3e-7db669eeb465
title: Notifyparser-allevelchange-Methode (Segment. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc47b7d78af8cfdd32aa63361411e769c375ddf1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369699"
---
# <a name="notifyparentallevelchange-method"></a>Notifyparser-allevelchange-Methode

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die- `NotifyParentalLevelChange` Methode aktiviert oder deaktiviert die Ereignis Behandlung für Befehle der temporären Jugend Verwaltungsebene.

``` syntax
MSWebDVD.NotifyParentalLevelChange(bNotify)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="bNotify"></span><span id="bnotify"></span><span id="BNOTIFY"></span>*bbenachrichtigen*
</dt> <dd>

Gibt einen booleschen Wert an, der angibt, ob die Anwendung benachrichtigt wird, wenn das mswebdvd-Objekt Videosegmente mit einer restriktiveren Bewertung als die Gesamtbewertung für die Festplatte findet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Bemerkungen

Benachrichtigungs Verwaltungs Benachrichtigungen sind standardmäßig deaktiviert. Dies bedeutet, dass temporäre Jugend Befehle von der Festplatte zulässig sind, aber ignoriert werden und die Festplatte ohne Unterbrechung wiedergegeben wird. Diese Methode wird während der Initialisierung der Anwendung aufgerufen, wenn Sie die temporären Befehle der Jugend Verwaltungsebene von der Festplatte verarbeiten müssen. Um die Jugendverwaltung zu deaktivieren, nachdem Sie aktiviert wurde, müssen Sie diese Methode mit dem Argument false aufzurufen. Weitere Informationen zur Eltern Verwaltung finden Sie unter " [**Accept-Parser-allevelchange**](acceptparentallevelchange-method.md)".

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|--------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Segment. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Selectparser-allevel**](selectparentallevel-method.md)
</dt> <dt>

[**Gettitleparamevels**](gettitleparentallevels-method.md)
</dt> <dt>

[**Getplayerparameentalcountry**](getplayerparentalcountry-method.md)
</dt> <dt>

[**Getplayerparser**](getplayerparentallevel-method.md)
</dt> <dt>

[**Selectpartalcountry**](selectparentalcountry-method.md)
</dt> </dl>

 

 




