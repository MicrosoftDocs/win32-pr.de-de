---
title: MCI_OPEN_PARMS-Struktur (mciapi. h)
description: Die geöffnete MCI- \_ \_ Struktur enthält Informationen für den MCI- \_ Befehl "Öffnen".
ms.assetid: d22cefeb-3d49-47cf-a946-f73c77ae43fd
keywords:
- MCI_OPEN_PARMS Struktur Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_OPEN_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 658f97a9b2677347c9818265c1f05c2115c95fdd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103442"
---
# <a name="mci_open_parms-structure"></a>MCI \_ - \_ Struktur mit offenen Parametern

Die **\_ geöffnete \_ MCI** -Struktur enthält Informationen für den MCI-Befehl " [**\_ Öffnen**](mci-open.md) ".

## <a name="syntax"></a>Syntax


```C++
typedef struct {
  DWORD_PTR   dwCallback;
  MCIDEVICEID wDeviceID;
  LPCTSTR     lpstrDeviceType;
  LPCTSTR     lpstrElementName;
  LPCTSTR     lpstrAlias;
} MCI_OPEN_PARMS;
```



## <a name="members"></a>Member

<dl> <dt>

**dwcallback**
</dt> <dd>

Das nieder wertige Wort gibt ein Fenster Handle an, das für das MCI-Benachrichtigungs Kennzeichen verwendet wird \_ .

</dd> <dt>

**WDE viceid**
</dt> <dd>

An die Anwendung zurückgegebener Bezeichner.

</dd> <dt>

**lpstraude vicetype**
</dt> <dd>

Der Name oder Konstantenbezeichner des Gerätetyps. (Der Name des Geräts wird in der Regel aus der Registrierung oder SYSTEM.INI Datei abgerufen.) Wenn dieser Member eine Konstante ist, kann er einer der Werte sein, die in den [MCI-Gerätetypen](mci-device-types.md)aufgeführt sind.

</dd> <dt>

**lpstrelementname**
</dt> <dd>

Device-Element (häufig ein Pfad).

</dd> <dt>

**lpstraualias**
</dt> <dd>

Optionaler Gerätealias.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Wenn Sie den Membern dieser Strukturdaten zuweisen, legen Sie die entsprechenden Flags im *fdwcommand* -Parameter der [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion fest, um die Elemente zu überprüfen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Mciapi. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MCI**](mci.md)
</dt> <dt>

[**MCI-Strukturen**](mci-structures.md)
</dt> <dt>

[**MCI \_ geöffnet**](mci-open.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

