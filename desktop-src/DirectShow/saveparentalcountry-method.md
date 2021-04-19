---
description: Die dvdadm. saveparameentalcountry-Methode speichert das neue Eltern Land/die Region der Anwendung in der Registrierung.
ms.assetid: 2185ad7d-c7c1-4d8b-82e7-5ed5fffaff26
title: Saveparameentalcountry-Methode (Segment. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9ca47a6ca10f25298b4eb10fdcf532c8d764b96
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354199"
---
# <a name="saveparentalcountry-method"></a>Saveparameentalcountry-Methode

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die `DVDAdm.SaveParentalCountry` -Methode speichert das neue Eltern Land/die Region der Anwendung in der Registrierung.

``` syntax
DVD.DVDAdm.SaveParentalCountry(iCountry, sUserName, sPassword)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="iCountry"></span><span id="icountry"></span><span id="ICOUNTRY"></span>*iCountry*
</dt> <dd>

Gibt das Eltern Land/die Region als Ganzzahl an.

</dd> <dt>

<span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*sUserName*
</dt> <dd>

Gibt den Benutzernamen als Zeichenfolge an. (Wird zurzeit ignoriert.)

</dd> <dt>

<span id="sPassword"></span><span id="spassword"></span><span id="SPASSWORD"></span>*sPassword*
</dt> <dd>

Gibt das Kennwort als Zeichenfolge an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Bemerkungen

Mit dieser Methode kann ein Benutzer, der das aktuelle Kennwort kennt, eine neue Einstellung für das elterliche Land/die Region in der Registrierung speichern. Wie bei allen Methoden von **msdvdadm** wirkt sich diese Methode nicht auf die aktuelle Ebene im Player aus. Es wird nur die Registrierungs Einstellung geändert, sodass das nächste Mal, wenn das mswebdvd-Objekt erstellt wird, mit dem neuen Land/der neuen Region geöffnet wird. Um das Eltern Land/die Region im Player zu ändern, müssen Sie [**selectpartalcountry**](selectparentalcountry-method.md)anrufen, wodurch die Registrierungs Einstellung nicht geändert wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|--------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Segment. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Saveparameentallevel**](saveparentallevel-method.md)
</dt> <dt>

[Msdvdadm-Objekt](msdvdadm-object.md)
</dt> </dl>

 

 




