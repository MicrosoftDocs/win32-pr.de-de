---
description: Enthält Informationen, die eine neue Liste der zuletzt verwendeten (MRU) definieren. Wird von "kreatemrulistw" verwendet.
title: Mruinfo-Struktur
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
ms.openlocfilehash: 91c0b1a2c10f4ac77afa5f8af2380b3d14ced8f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104993790"
---
# <a name="mruinfo-structure"></a>Mruinfo-Struktur

Enthält Informationen, die eine neue Liste der zuletzt verwendeten (MRU) definieren. Wird von " [**kreatemrulistw**](createmrulist.md)" verwendet.

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

**CBSIZE**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Die Größe der-Struktur.

</dd> <dt>

**Umax**
</dt> <dd>

Typ: **uint**

</dd> <dd>

Die maximale Anzahl von Einträgen in der MRU-Liste.

</dd> <dt>

**fFlags**
</dt> <dd>

Typ: **uint**

</dd> <dd>

Mindestens eines der folgenden Flags.

<dt>

<span id="MRU_BINARY"></span><span id="mru_binary"></span>

<span id="MRU_BINARY"></span><span id="mru_binary"></span>**MRU \_ Binary** (0x0001)


</dt> <dd>

Daten werden in der Registrierung als Binärdaten und nicht als Zeichen folgen Daten gespeichert.

</dd> <dt>

<span id="MRU_CACHEWRITE"></span><span id="mru_cachewrite"></span>

<span id="MRU_CACHEWRITE"></span><span id="mru_cachewrite"></span>**MRU \_ Cachewrite** (0x0002)


</dt> <dd>

Schreiben Sie Änderungen an der MRU-Version, die in der Registrierung gespeichert ist, nur dann, wenn ein neues Element hinzugefügt wird oder die Ressourcen der MRU-Liste aus dem Arbeitsspeicher freigegeben werden. Beachten Sie, dass die aktive Version der MRU im Arbeitsspeicher sofort als Reaktion auf eine Änderung des Inhalts oder der Reihenfolge aktualisiert wird.

</dd> </dl> </dd> <dt>

**HKEY**
</dt> <dd>

Typ: **HKEY**

</dd> <dd>

Ein Handle für den aktuell geöffneten Schlüssel oder einen der folgenden vordefinierten Werte, unter denen die MRU-Daten gespeichert werden sollen.

<dl><span id="HKEY_CURRENT_USER"></span><span id="hkey_current_user"></span><dt>

**Aktueller HKEY- \_ \_ Benutzer**
</dt><span id="HKEY_LOCAL_MACHINE"></span><span id="hkey_local_machine"></span><dt>

**lokaler HKEY- \_ \_ Computer**
</dt> </dl> </dd> <dt>

**lpszSubKey**
</dt> <dd>

Typ: **LPCTSTR**

</dd> <dd>

Der Unterschlüssel, unter dem die MRU-Daten gespeichert werden sollen.

</dd> <dt>

**lpfncompare**
</dt> <dd>

Typ: **[ **mrucmpproc**](mrucmpproc.md)**

</dd> <dd>

Ein Zeiger auf eine optionale Daten Vergleichsfunktion, die verwendet werden kann, um zu bestimmen, ob ein Element in der MRU-Liste vorhanden ist. Dies ist hilfreich, wenn die MRU-Liste mit dem **MRU- \_ Binärflag** erstellt wurde. Wenn dieser Member **null** ist, werden standardmäßige Zeichen folgen Vergleichsfunktionen verwendet. für Binärdaten wird ein direkter Speicher Vergleich verwendet.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Struktur ist nicht in einer Header Datei definiert. Sie müssen Sie selbst definieren.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>       |
| Unicode- und ANSI-Name<br/>   | **Mruinfow** (Unicode) und **mruinfoa** (ANSI)<br/>  |



 

 




