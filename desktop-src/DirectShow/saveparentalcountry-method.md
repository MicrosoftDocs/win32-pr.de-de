---
description: Die DVDAdm.SaveParentalCountry-Methode speichert das neue Land/die Region der Eltern der Anwendung in der Registrierung.
ms.assetid: 2185ad7d-c7c1-4d8b-82e7-5ed5fffaff26
title: SaveParentalCountry-Methode (Segment.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d5391982129c799e6a565da362837a557765cf46604653f4f702ed38dcb910e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119651210"
---
# <a name="saveparentalcountry-method"></a>SaveParentalCountry-Methode

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die -Methode speichert das neue Land bzw. die Region der Eltern der Anwendung `DVDAdm.SaveParentalCountry` in der Registrierung.

``` syntax
DVD.DVDAdm.SaveParentalCountry(iCountry, sUserName, sPassword)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="iCountry"></span><span id="icountry"></span><span id="ICOUNTRY"></span>*iCountry*
</dt> <dd>

Gibt das Land/die Region der Eltern als ganze Zahl an.

</dd> <dt>

<span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*sUserName*
</dt> <dd>

Gibt den Benutzernamen als Zeichenfolge an. (Derzeit ignoriert.)

</dd> <dt>

<span id="sPassword"></span><span id="spassword"></span><span id="SPASSWORD"></span>*sPassword*
</dt> <dd>

Gibt das Kennwort als Zeichenfolge an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Hinweise

Mit dieser Methode kann ein Benutzer, der das aktuelle Kennwort kennt, eine neue Einstellung für das Land bzw. die Region der Eltern in der Registrierung speichern. Wie bei allen Methoden von **MSDVDAdm** wirkt sich diese Methode nicht auf die aktuelle Ebene im Player aus. Es wird nur die Registrierungseinstellung geändert, sodass das MSWebDVD-Objekt beim nächsten Erstellen mit dem neuen Land/der neuen Region geöffnet wird. Um das Land/die Region der Eltern im Spieler zu ändern, rufen Sie [**SelectParentalCountry**](selectparentalcountry-method.md)auf, wodurch die Registrierungseinstellung nicht geändert wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|--------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Segment.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**SaveParentalLevel**](saveparentallevel-method.md)
</dt> <dt>

[MSDVDAdm-Objekt](msdvdadm-object.md)
</dt> </dl>

 

 




