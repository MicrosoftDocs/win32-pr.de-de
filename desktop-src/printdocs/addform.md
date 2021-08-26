---
description: Die AddForm-Funktion fügt der Liste der verfügbaren Formulare, die für den angegebenen Drucker ausgewählt werden können, ein Formular hinzu.
ms.assetid: 17b59019-f93a-4b57-86fb-91c61aecbac4
title: AddForm-Funktion (Winspool.h)
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
ms.openlocfilehash: 6e9a2bac108702ff55b761b562fd8668870092b35402a6471462c3e63e5fc1e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119950830"
---
# <a name="addform-function"></a>AddForm-Funktion

Die **AddForm-Funktion** fügt der Liste der verfügbaren Formulare, die für den angegebenen Drucker ausgewählt werden können, ein Formular hinzu.

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

*hPrinter* \[ In\]
</dt> <dd>

Ein Handle für den Drucker, der das Drucken mit dem angegebenen Formular unterstützt. Verwenden Sie [**die OpenPrinter-**](openprinter.md) [**oder AddPrinter-Funktion,**](addprinter.md) um einen Druckerhandpunkt abzurufen.

</dd> <dt>

*Ebene* \[ In\]
</dt> <dd>

Die Ebene der -Struktur, auf die *pForm* zeigt. Dieser Wert muss 1 oder 2 sein.

</dd> <dt>

*pForm* \[ In\]
</dt> <dd>

Ein Zeiger auf eine [**FORM \_ INFO \_ 1- oder**](form-info-1.md) FORM INFO [**\_ \_ 2-Struktur.**](form-info-2.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert ein Wert ungleich 0 (null).

Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.

## <a name="remarks"></a>Hinweise

> [!Note]  
> Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückkehrt. Wie schnell diese Funktion zurückgegeben wird, hängt von Laufzeitfaktoren wie Netzwerkstatus, Druckerserverkonfiguration und Implementierungsfaktoren des Druckertreibers ab, die beim Schreiben einer Anwendung schwer vorherzusagen sind. Das Aufrufen dieser Funktion aus einem Thread, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte dazu kommen, dass die Anwendung nicht reagiert.

 

Eine Anwendung kann bestimmen, welche Formulare für einen Drucker verfügbar sind, indem sie die [**EnumForms-Funktion**](enumforms.md) aufruft.

Wenn *pForm* auf [**FORM INFO \_ \_ 2**](form-info-2.md)verweist, kann **AddForm** nicht verwendet werden, wenn ein Formular mit dem angegebenen Namen bereits vorhanden ist oder der *pKeyword-Wert* der Struktur bereits vorhanden ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Spoolss.dll</dt> </dl>                    |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> <dt>

[**EnumForms**](enumforms.md)
</dt> <dt>

[**FORMULARINFORMATIONEN \_ \_ 1**](form-info-1.md)
</dt> <dt>

[**FORMULARINFORMATIONEN \_ \_ 2**](form-info-2.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> </dl>

 

 




