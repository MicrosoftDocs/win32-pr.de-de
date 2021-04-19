---
description: Die AddForm-Funktion fügt der Liste der verfügbaren Formulare, die für den angegebenen Drucker ausgewählt werden können, ein Formular hinzu.
ms.assetid: 17b59019-f93a-4b57-86fb-91c61aecbac4
title: AddForm-Funktion (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddForm
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 2de3ddbdc57a5a41bac048a94a8175cd124df4ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349835"
---
# <a name="addform-function"></a>AddForm-Funktion

Die **AddForm** -Funktion fügt der Liste der verfügbaren Formulare, die für den angegebenen Drucker ausgewählt werden können, ein Formular hinzu.

## <a name="syntax"></a>Syntax


```C++
BOOL AddForm(
  _In_ HANDLE hPrinter,
  _In_ DWORD  Level,
  _In_ LPBYTE pForm
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hprinter* \[ in\]
</dt> <dd>

Ein Handle für den Drucker, der das Drucken mit dem angegebenen Formular unterstützt. Verwenden Sie die Funktion [**OpenPrinter**](openprinter.md) oder [**addprinter**](addprinter.md) zum Abrufen eines Drucker Handles.

</dd> <dt>

*Ebene* \[ in\]
</dt> <dd>

Die Ebene der-Struktur, auf die *pform* zeigt. Dieser Wert muss 1 oder 2 sein.

</dd> <dt>

*pform* \[ in\]
</dt> <dd>

Ein Zeiger auf das [**Formular \_ Info \_ 1**](form-info-1.md) oder die [**Form \_ Info \_ 2**](form-info-2.md) -Struktur.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert ein Wert ungleich 0 (null).

Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird. Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können. Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.

 

Eine Anwendung kann ermitteln, welche Formulare für einen Drucker verfügbar sind, indem die [**enumforms**](enumforms.md) -Funktion aufgerufen wird.

Wenn *pform* auf das [**Formular \_ Info \_ 2**](form-info-2.md)zeigt, schlägt **AddForm** fehl, wenn entweder ein Formular mit dem angegebenen Namen bereits vorhanden ist oder der *pkeyword* -Wert der Struktur bereits vorhanden ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool. h (Include Windows. h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Spoolss.dll</dt> </dl>                    |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> <dt>

[**Enumforms**](enumforms.md)
</dt> <dt>

[**Formular \_ Informationen \_ 1**](form-info-1.md)
</dt> <dt>

[**Formular \_ Informationen \_ 2**](form-info-2.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> </dl>

 

 




