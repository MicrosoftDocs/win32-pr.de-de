---
description: Die dvdadm. saveparameentallevel-Methode speichert eine neue Standard-Jugend Stufe in der Registrierung.
ms.assetid: 8ad22098-acbd-41fd-9224-829b3cc5f8ae
title: Saveparameentallevel-Methode (Segment. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94d30d26264dff077de391b6b513f7e9ab5048c8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373778"
---
# <a name="saveparentallevel-method"></a>Saveparameentallevel-Methode

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die **dvdadm. saveparameentallevel** -Methode speichert eine neue Standard-Jugend Stufe in der Registrierung.

``` syntax
DVD.DVDAdm.SaveParentalLevel(iLevel, sUserName, sPassword)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="iLevel"></span><span id="ilevel"></span><span id="ILEVEL"></span>*iLevel*
</dt> <dd>

Gibt die Jugend Stufe als einen ganzzahligen Wert zwischen 1 und 8 an.

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

Mit dieser Methode kann ein Benutzer, der das aktuelle Kennwort kennt, eine neue Einstellung auf Jugendebene in der Registrierung speichern. Wie bei allen Methoden von **msdvdadm** wirkt sich diese Methode nicht auf die aktuelle Ebene im Player aus. Es wird nur die Registrierungs Einstellung geändert, sodass das nächste Mal, wenn das mswebdvd-Objekt gestartet wird, mit der neuen Ebene geöffnet wird. Geben Sie-1 an, um die Eltern Verwaltung zu deaktivieren Um die Jugendebene im Player zu ändern, müssen Sie [**selectparamevel**](selectparentallevel-method.md)aufzurufen, wodurch die Registrierungs Einstellung nicht geändert wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|--------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Segment. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Msdvdadm-Objekt](msdvdadm-object.md)
</dt> </dl>

 

 




