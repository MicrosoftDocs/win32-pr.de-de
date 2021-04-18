---
title: MCI_SYSINFO_PARMS-Struktur (mciapi. h)
description: Die MCI- \_ sysinfo- \_ Struktur enthält Informationen für den MCI- \_ Befehl "sysinfo".
ms.assetid: 433649ed-7c00-440d-84f3-164949e01cc4
keywords:
- MCI_SYSINFO_PARMS Struktur Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_SYSINFO_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf143bb0d895dc03df38bbb0a657467d506eac77
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106337705"
---
# <a name="mci_sysinfo_parms-structure"></a>Struktur von MCI- \_ sysinfo- \_ Parametern

Die **MCI- \_ sysinfo \_** -Struktur enthält Informationen für den [**MCI-Befehl " \_ sysinfo**](mci-sysinfo.md) ".

## <a name="syntax"></a>Syntax


```C++
typedef struct {
  DWORD_PTR dwCallback;
  LPTSTR    lpstrReturn;
  DWORD     dwRetSize;
  DWORD     dwNumber;
  UINT      wDeviceType;
} MCI_SYSINFO_PARMS;
```



## <a name="members"></a>Member

<dl> <dt>

**dwcallback**
</dt> <dd>

Das nieder wertige Wort gibt ein Fenster Handle an, das für das MCI-Benachrichtigungs Kennzeichen verwendet wird \_ .

</dd> <dt>

**lpstraureturn**
</dt> <dd>

Zeiger auf einen vom Benutzer bereitgestellten Puffer für die Rückgabe Zeichenfolge. Sie wird auch verwendet, um einen **DWORD** -Wert zurückzugeben, wenn das MCI-Flag für die \_ sysinfo- \_ Menge verwendet wird.

</dd> <dt>

**dwretsize**
</dt> <dd>

Größe (in Bytes) des Rückgabe Puffers.

</dd> <dt>

**dwnumber**
</dt> <dd>

Zahl, die die Geräte Position in der MCI-Gerätetabelle oder in der Liste der geöffneten Geräte angibt, wenn das MCI- \_ sysinfo- \_ Flag zum Öffnen festgelegt ist.

</dd> <dt>

**WDE vicetype**
</dt> <dd>

Typ des Geräts. Dieser Member kann einer der Werte sein, die in den [MCI-Gerätetypen](mci-device-types.md)aufgeführt sind.

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

[**MCI- \_ sysinfo**](mci-sysinfo.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

