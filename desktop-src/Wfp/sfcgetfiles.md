---
description: Listet geschützte Dateien auf.
ms.assetid: 46a1ff83-afed-4ce3-bb62-551446efdb78
title: Sfcgetfiles-Funktion (sfcfiles. h)
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
ms.openlocfilehash: 6b38b761372db656308e778fd96ea48607cf1f21
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865976"
---
# <a name="sfcgetfiles-function"></a>Sfcgetfiles-Funktion

\[Diese Funktion ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Die Unterstützung für diese Funktion wurde in Windows Vista und Windows Server 2008 entfernt. Verwenden Sie stattdessen die in [WRP-Funktionen](wfp-functions.md) aufgeführten unterstützten Funktionen.\]

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

" *Protfiledata* \[ " vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine [**pprotect- \_ Datei \_ Eintrags**](pprotect-file-entry.md) Struktur, die die Liste der geschützten Dateien enthält.

</dd> <dt>

*Dateianzahl* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf einen Speicherort, der einen Ulong-Wert enthält, der die Anzahl der geschützten Dateien ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, lautet der Rückgabewert Status \_ Success. Wenn die Funktion fehlschlägt, wird der entsprechende NTSTATUS-Fehlercode zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                    |
| Ende des Supports (Client)<br/>    | Windows XP<br/>                                                                   |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                                                          |
| Header<br/>                   | <dl> <dt>Sfcfiles. h</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Sfcfiles.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**pprotect- \_ Datei \_ Eintrag**](pprotect-file-entry.md)
</dt> </dl>

 

 




