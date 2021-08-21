---
description: Die von der SfcGetFiles-Funktion verwendete Struktur.
ms.assetid: 958167e3-3eb3-406a-85bf-ffe2851a95a1
title: PPROTECT_FILE_ENTRY -Struktur (Sfcfiles.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PPROTECT_FILE_ENTRY
api_type:
- HeaderDef
api_location:
- Sfcfiles.h
ms.openlocfilehash: c9070290170febf08e532b071812600fb0ef8755302a4bd1603858659196d0c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119053198"
---
# <a name="pprotect_file_entry-structure"></a>PPROTECT \_ FILE \_ ENTRY-Struktur

\[Diese Struktur ist für die Verwendung in den im Abschnitt Anforderungen angegebenen Betriebssystemen verfügbar. Die Unterstützung für diese Struktur wurde in Windows Vista und Windows Server 2008 entfernt. Verwenden Sie stattdessen die unterstützten Funktionen, die in [WRP-Funktionen](wfp-functions.md) aufgeführt sind.\]

Die von der [**SfcGetFiles-Funktion verwendete**](sfcgetfiles.md) Struktur.

## <a name="syntax"></a>Syntax


```C++
typedef struct _PPROTECT_FILE_ENTRY {
  PWSTR SourceFileName;
  PWSTR FileName;
  PWSTR InfName;
} PPROTECT_FILE_ENTRY, *PPPROTECT_FILE_ENTRY;
```



## <a name="members"></a>Member

<dl> <dt>

**SourceFileName**
</dt> <dd>

Zeiger auf einen Zeichenfolgenwert, der den Dateinamen der Quelldatei enthält. Dieser Wert ist **NULL,** wenn die Datei bei der Installation nicht umbenannt wird.

</dd> <dt>

**FileName**
</dt> <dd>

Zeiger auf den Zeichenfolgenwert, der den Zieldateinamen plus den vollständigen Pfad zur Datei enthält.

</dd> <dt>

**InfName**
</dt> <dd>

Zeiger auf den Zeichenfolgenwert, der den Dateinamen der INF-Datei enthält, die Layoutinformationen enthält. Dieser Parameter kann NULL **sein,** wenn das Standardlayout verwendet wird.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Ende des Supports (Client)<br/>    | Windows XP<br/>                                                                 |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                                                        |
| Header<br/>                   | <dl> <dt>Sfcfiles.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**SfcGetFiles**](sfcgetfiles.md)
</dt> </dl>

 

 




