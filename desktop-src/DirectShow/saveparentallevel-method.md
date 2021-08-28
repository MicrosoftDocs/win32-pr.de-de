---
description: Die DVDAdm.SaveParentalLevel-Methode speichert eine neue Standardelternebene in der Registrierung.
ms.assetid: 8ad22098-acbd-41fd-9224-829b3cc5f8ae
title: SaveParentalLevel-Methode (Segment.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e372563a6f5a1fe8e893efeb86633baa6a03a7b72c79e3f05a3ec7372bec2e0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119315950"
---
# <a name="saveparentallevel-method"></a>SaveParentalLevel-Methode

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die **DVDAdm.SaveParentalLevel-Methode** speichert eine neue Standardelternebene in der Registrierung.

``` syntax
DVD.DVDAdm.SaveParentalLevel(iLevel, sUserName, sPassword)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="iLevel"></span><span id="ilevel"></span><span id="ILEVEL"></span>*iLevel*
</dt> <dd>

Gibt die Elternebene alsInteger-Wert von 1 bis 8 an.

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

Mit dieser Methode kann ein Benutzer, der das aktuelle Kennwort kennt, eine neue Einstellung auf Elternebene in der Registrierung speichern. Wie bei allen Methoden von **MSDVDAdm** wirkt sich diese Methode nicht auf die aktuelle Ebene im Player aus. es ändert nur die Registrierungseinstellung, sodass das MSWebDVD-Objekt beim nächsten Start mit der neuen Ebene geöffnet wird. Geben Sie -1 an, um die Verwaltung der Eltern zu deaktivieren. Um die Elternebene im Player zu ändern, rufen [**Sie SelectParentalLevel**](selectparentallevel-method.md)auf, wodurch die Registrierungseinstellung nicht geändert wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|--------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Segment.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[MSDVDAdm-Objekt](msdvdadm-object.md)
</dt> </dl>

 

 




