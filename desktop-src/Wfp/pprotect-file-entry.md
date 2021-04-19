---
description: Von der sfcgetfiles-Funktion verwendete Struktur.
ms.assetid: 958167e3-3eb3-406a-85bf-ffe2851a95a1
title: PPROTECT_FILE_ENTRY Struktur (sfcfiles. h)
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
ms.openlocfilehash: 98cda570a3677560d51800d58822d93a942847c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349252"
---
# <a name="pprotect_file_entry-structure"></a>Pprotect- \_ Datei \_ Eintrags Struktur

\[Diese Struktur steht für die Verwendung in den Betriebssystemen zur Verfügung, die im Abschnitt "Anforderungen" angegeben sind. Die Unterstützung für diese Struktur wurde in Windows Vista und Windows Server 2008 entfernt. Verwenden Sie stattdessen die in [WRP-Funktionen](wfp-functions.md) aufgeführten unterstützten Funktionen.\]

Von der [**sfcgetfiles**](sfcgetfiles.md) -Funktion verwendete Struktur.

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

Ein Zeiger auf einen Zeichen folgen Wert, der den Dateinamen der Quelldatei enthält. Dieser Wert ist **null** , wenn die Datei bei der Installation nicht umbenannt wird.

</dd> <dt>

**FileName**
</dt> <dd>

Ein Zeiger auf einen Zeichen folgen Wert, der den Ziel Dateinamen sowie den vollständigen Pfad zur Datei enthält.

</dd> <dt>

**InfName**
</dt> <dd>

Ein Zeiger auf einen Zeichen folgen Wert, der den Dateinamen der INF-Datei mit Layoutinformationen enthält. Dieser Parameter kann **null** sein, wenn das Standardlayout verwendet wird.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Ende des Supports (Client)<br/>    | Windows XP<br/>                                                                 |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                                                        |
| Header<br/>                   | <dl> <dt>Sfcfiles. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Sfcgetfiles**](sfcgetfiles.md)
</dt> </dl>

 

 




