---
title: MCI_OVLY_OPEN_PARMS-Struktur (MMSYSTEM. h)
description: Die MCI- \_ Struktur mit OVLY- \_ Open-Parametern \_ enthält Informationen zum MCI- \_ Befehl "Öffnen" für Video Überlagerungs Geräte.
ms.assetid: 1559ae40-4aa5-4dfc-b337-7b056c706b67
keywords:
- MCI_OVLY_OPEN_PARMS Struktur Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_OVLY_OPEN_PARMS
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e64b864b4b0366421828960504aff3f5a83836b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475096"
---
# <a name="mci_ovly_open_parms-structure"></a>MCI \_ OVLY- \_ Struktur zum Öffnen von \_ Parametern

Die **MCI-Struktur mit \_ OVLY- \_ Open- \_ Parametern** enthält Informationen zum MCI-Befehl " [**\_ Öffnen**](mci-open.md) " für Video Überlagerungs Geräte.

## <a name="syntax"></a>Syntax


```C++
typedef struct {
  DWORD_PTR   dwCallback;
  MCIDEVICEID wDeviceID;
  LPCTSTR     lpstrDeviceType;
  LPCTSTR     lpstrElementName;
  LPCTSTR     lpstrAlias;
  DWORD       dwStyle;
  DWORD       hWndParent;
} MCI_OVLY_OPEN_PARMS;
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

Der Name des Geräte Elements (in der Regel ein Pfad).

</dd> <dt>

**lpstraualias**
</dt> <dd>

Optionaler Gerätealias.

</dd> <dt>

**dwstyle**
</dt> <dd>

Fenster Stil.

</dd> <dt>

**hwndParent**
</dt> <dd>

Handle für das übergeordnete Fenster.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Wenn Sie den Membern dieser Strukturdaten zuweisen, legen Sie die entsprechenden Flags im *fdwcommand* -Parameter der [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion fest, um die Elemente zu überprüfen.

Wenn Sie die erweiterten Datenmember nicht verwenden, können Sie die [**MCI-Struktur \_ Open- \_ Parser**](mci-open-parms.md) anstelle von **MCI \_ OVLY \_ Open- \_ Parametern** verwenden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                            |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>MMSYSTEM. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MCI**](mci.md)
</dt> <dt>

[**MCI-Strukturen**](mci-structures.md)
</dt> <dt>

[**MCI \_ geöffnet**](mci-open.md)
</dt> <dt>

[**geöffnete MCI- \_ \_ Parser**](mci-open-parms.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

