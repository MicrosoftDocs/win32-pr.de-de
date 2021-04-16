---
description: Mit der dvdadm. ChangePassword-Methode wird ein neues Anwendungs Kennwort in der Registrierung gespeichert.
ms.assetid: 58dac785-e20e-4a41-89cf-56644964da19
title: ChangePassword-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bba8bfb9adcecdb88f19f3ac1b8061f93486e269
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481030"
---
# <a name="changepassword-method"></a>ChangePassword-Methode

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Mit der- `DVDAdm.ChangePassword` Methode wird ein neues Anwendungs Kennwort in der Registrierung gespeichert.

``` syntax
        DVD.DVDAdm.ChangePassword(sUserName, sOld, sNew)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*sUserName*
</dt> <dd>

Gibt den Anmelde Namen des aktuellen Benutzers als Zeichenfolge an. Das msdvdadm-Objekt ignoriert diesen Parameter. Siehe Hinweise.

</dd> <dt>

<span id="sOld"></span><span id="sold"></span><span id="SOLD"></span>*ter*
</dt> <dd>

Gibt das alte Kennwort des Benutzers als Zeichenfolge an.

</dd> <dt>

<span id="sNew"></span><span id="snew"></span><span id="SNEW"></span>*SNEW*
</dt> <dd>

Gibt das neue Kennwort des Benutzers als Zeichenfolge an. Darf keine leere Zeichenfolge sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Bemerkungen

Derzeit wird der *sUserName* -Parameter für dieses und alle zugehörigen Methoden ignoriert. Dies bedeutet, dass Personen, die das Kennwort kennen, die elternebene festlegen können. Es gibt nur ein Kennwort und eine elternebene für die Anwendung. Es gibt keine Unterstützung einzelner Benutzer Anmelde Namen oder mehrerer Kenn Wort Verwaltung. Zum Erzwingen von Verwaltungs Stufen für Eltern sollten die übergeordneten Elemente das Kennwort festlegen und dann die Jugend Stufe festlegen, die für jüngere Mitglieder der Gruppe von Angehörigen geeignet ist. Wenn übergeordnete Elemente eine CD mit Inhalten mit Erwachsener Bewertung anzeigen möchten, können Sie die Ebene ändern und dann wieder ändern, wenn die Anzeige abgeschlossen ist. Solange die untergeordneten Elemente das Kennwort nicht kennen, können Sie nur Inhalte an oder unterhalb der festgelegten Ebene ansehen.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ConfirmPassword**](confirmpassword-method.md)
</dt> <dt>

[Msdvdadm-Objekt](msdvdadm-object.md)
</dt> </dl>

 

 



