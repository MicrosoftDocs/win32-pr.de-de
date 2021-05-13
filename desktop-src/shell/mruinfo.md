---
description: Enthält Informationen, die eine neue LISTE der zuletzt verwendeten (MRU) definieren. Wird von CreateMRUListW verwendet.
title: MRUINFO-Struktur
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _MRUINFO
- MRUINFOA
- MRUINFOW
api_type:
- NA
api_location: ''
ms.assetid: 31d5831d-9a19-4bd9-8439-ce844966c414
ms.openlocfilehash: 652168e6a4e61ac754aac3202e0681ec6b7d9e66
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109840761"
---
# <a name="mruinfo-structure"></a>MRUINFO-Struktur

Enthält Informationen, die eine neue LISTE der zuletzt verwendeten (MRU) definieren. Wird von [**CreateMRUListW verwendet.**](createmrulist.md)

## <a name="syntax"></a>Syntax


```C++
typedef struct {
  DWORD      cbSize;
  UINT       uMax;
  UINT       fFlags;
  HKEY       hKey;
  LPCTSTR    lpszSubKey;
  MRUCMPPROC lpfnCompare;
} _MRUINFO;
```



## <a name="members"></a>Member

<dl> <dt>

**cbSize**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Die Größe der -Struktur.

</dd> <dt>

**Umax**
</dt> <dd>

Typ: **UINT**

</dd> <dd>

Die maximale Anzahl von Einträgen in der MRU-Liste.

</dd> <dt>

**fFlags**
</dt> <dd>

Typ: **UINT**

</dd> <dd>

Mindestens eines der folgenden Flags.

<dt>

<span id="MRU_BINARY"></span><span id="mru_binary"></span>

<span id="MRU_BINARY"></span><span id="mru_binary"></span>**MRU \_ BINARY** (0x0001)


</dt> <dd>

Daten werden in der Registrierung als Binärdaten und nicht als Zeichenfolgendaten gespeichert.

</dd> <dt>

<span id="MRU_CACHEWRITE"></span><span id="mru_cachewrite"></span>

<span id="MRU_CACHEWRITE"></span><span id="mru_cachewrite"></span>**MRU \_ CACHEWRITE** (0x0002)


</dt> <dd>

Schreiben Sie Änderungen an der in der Registrierung gespeicherten MRU-Version nur, wenn ein neues Element hinzugefügt oder die Ressourcen der MRU-Liste aus dem Arbeitsspeicher frei werden. Beachten Sie, dass die aktive Version der MRU im Arbeitsspeicher sofort aktualisiert wird, wenn sich der Inhalt oder die Reihenfolge ändert.

</dd> </dl> </dd> <dt>

**Hkey**
</dt> <dd>

Typ: **HKEY**

</dd> <dd>

Ein Handle für den derzeit geöffneten Schlüssel oder einen der folgenden vordefinierten Werte, unter denen die MRU-Daten gespeichert werden sollen.

<dl><span id="HKEY_CURRENT_USER"></span><span id="hkey_current_user"></span><dt>

**AKTUELLER \_ \_ HKEY-BENUTZER**
</dt><span id="HKEY_LOCAL_MACHINE"></span><span id="hkey_local_machine"></span><dt>

**HKEY \_ LOCAL \_ MACHINE**
</dt> </dl> </dd> <dt>

**lpszSubKey**
</dt> <dd>

Typ: **LPCTSTR**

</dd> <dd>

Der Unterschlüssel, unter dem die MRU-Daten gespeichert werden sollen.

</dd> <dt>

**lpfnCompare**
</dt> <dd>

Typ: **[ **MRUCMPPROC**](mrucmpproc.md)**

</dd> <dd>

Ein Zeiger auf eine optionale Datenvergleichsfunktion, mit der bestimmt werden kann, ob ein Element in der MRU-Liste vorhanden ist. Dies ist nützlich, wenn die MRU-Liste mit dem **MRU \_ BINARY-Flag** erstellt wurde. Wenn dieser Member **NULL** ist, werden Standardmäßige Zeichenfolgenvergleichsfunktionen verwendet. für Binärdaten wird ein direkter Speichervergleich verwendet.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Diese Struktur ist in einer Headerdatei nicht definiert. Sie müssen es selbst definieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>       |
| Unicode- und ANSI-Name<br/>   | **MRUINFOW** (Unicode) und **MRUINFOA** (ANSI)<br/>  |



 

 




