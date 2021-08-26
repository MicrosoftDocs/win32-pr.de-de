---
description: Listet geschützte Dateien auf.
ms.assetid: 46a1ff83-afed-4ce3-bb62-551446efdb78
title: SfcGetFiles-Funktion (Sfcfiles.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SfcGetFiles
api_type:
- DllExport
api_location:
- Sfcfiles.dll
ms.openlocfilehash: 3201621808708229419542acd7fa0caab0aa7f6e7d38bfe723b7f53bc68c4005
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119999280"
---
# <a name="sfcgetfiles-function"></a>SfcGetFiles-Funktion

\[Diese Funktion ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt Anforderungen angegeben sind. Die Unterstützung für diese Funktion wurde in Windows Vista und Windows Server 2008 entfernt. Verwenden Sie stattdessen die unterstützten Funktionen, die in [WRP Functions](wfp-functions.md) aufgeführt sind.\]

Listet geschützte Dateien auf.

## <a name="syntax"></a>Syntax


```C++
NTSTATUS WINAPI SfcGetFiles(
  _Out_ PPROTECT_FILE_ENTRY ProtFileData,
  _Out_ PULONG              FileCount
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ProtFileData* \[ out\]
</dt> <dd>

Ein Zeiger auf eine [**PPROTECT \_ FILE \_ ENTRY-Struktur,**](pprotect-file-entry.md) die die Liste der geschützten Dateien enthält.

</dd> <dt>

*FileCount* \[ out\]
</dt> <dd>

Ein Zeiger auf einen Speicherort, der einen ULONG-Wert enthält, der der Anzahl der geschützten Dateien entspricht.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, lautet der Rückgabewert STATUS \_ SUCCESS. Wenn die Funktion fehlschlägt, wird der entsprechende NTSTATUS-Fehlercode zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                    |
| Ende des Supports (Client)<br/>    | Windows XP<br/>                                                                   |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                                                          |
| Header<br/>                   | <dl> <dt>Sfcfiles.h</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Sfcfiles.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**\_PPROTECT-DATEIEINTRAG \_**](pprotect-file-entry.md)
</dt> </dl>

 

 




