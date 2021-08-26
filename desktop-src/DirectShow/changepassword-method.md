---
description: Die DVDAdm.ChangePassword-Methode speichert ein neues Anwendungskennwort in der Registrierung.
ms.assetid: 58dac785-e20e-4a41-89cf-56644964da19
title: ChangePassword-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f5d15eef943afa019f1b1bba4e3b1412978bc5dd8f52f411c504e880428848a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119999330"
---
# <a name="changepassword-method"></a>ChangePassword-Methode

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die `DVDAdm.ChangePassword` -Methode speichert ein neues Anwendungskennwort in der Registrierung.

``` syntax
        DVD.DVDAdm.ChangePassword(sUserName, sOld, sNew)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*sUserName*
</dt> <dd>

Gibt den Anmeldenamen des aktuellen Benutzers als Zeichenfolge an. Das MSDVDAdm-Objekt ignoriert diesen Parameter. Siehe Hinweise.

</dd> <dt>

<span id="sOld"></span><span id="sold"></span><span id="SOLD"></span>*Verkauft*
</dt> <dd>

Gibt das alte Kennwort des Benutzers als Zeichenfolge an.

</dd> <dt>

<span id="sNew"></span><span id="snew"></span><span id="SNEW"></span>*sNew*
</dt> <dd>

Gibt das neue Kennwort des Benutzers als Zeichenfolge an. Darf keine leere Zeichenfolge sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Hinweise

Derzeit wird der *sUserName-Parameter* für diese und alle zugehörigen Methoden ignoriert. Dies bedeutet, dass jeder, der das Kennwort kennt, die Ebene der Eltern festlegen kann. Es gibt nur ein Kennwort und eine Elternebene für die Anwendung. Es gibt keine Unterstützung für einzelne Benutzeranmeldungsnamen oder die Verwaltung mehrerer Kennwörter. Zum Erzwingen von Elternverwaltungsebenen sollten die Eltern das Kennwort festlegen und dann die Elternebene festlegen, die für mitglieder der Gruppe von Verwandten geeignet ist. Wenn Eltern einen Datenträger mit nicht jugendgefwerteten Inhalten anzeigen möchten, können sie die Ebene ändern und sie dann wieder ändern, wenn sie mit der Anzeige fertig sind. Solange die Kinder das Kennwort nicht kennen, können sie Inhalte nur auf der für sie festgelegten Ebene oder unterhalb der festgelegten Ebene ansehen.

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**ConfirmPassword**](confirmpassword-method.md)
</dt> <dt>

[MSDVDAdm-Objekt](msdvdadm-object.md)
</dt> </dl>

 

 



