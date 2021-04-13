---
description: Die enumforms-Funktion Listet die Formulare auf, die vom angegebenen Drucker unterstützt werden.
ms.assetid: b13b515a-c764-4a80-ab85-95fb4abb2a6b
title: Enumforms-Funktion (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumForms
- EnumFormsA
- EnumFormsW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 18cd9ad6f8e0491700d5618e29a0a629e8045366
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345299"
---
# <a name="enumforms-function"></a>Enumforms-Funktion

Die **enumforms** -Funktion Listet die Formulare auf, die vom angegebenen Drucker unterstützt werden.

## <a name="syntax"></a>Syntax


```C++
BOOL EnumForms(
  _In_  HANDLE  hPrinter,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pForm,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded,
  _Out_ LPDWORD pcReturned
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hprinter* \[ in\]
</dt> <dd>

Handle für den Drucker, für den die Formulare aufgelistet werden sollen. Verwenden Sie die Funktion [**OpenPrinter**](openprinter.md) oder [**addprinter**](addprinter.md) zum Abrufen eines Drucker Handles.

</dd> <dt>

*Ebene* \[ in\]
</dt> <dd>

Gibt die Version der-Struktur an, auf die *pform* zeigt. Dieser Wert muss 1 oder 2 sein.

</dd> <dt>

*pform* \[ vorgenommen\]
</dt> <dd>

Zeiger auf eine oder mehrere [**Formular \_ Info \_ 1**](form-info-1.md) -Strukturen oder auf mindestens eine [**Formular \_ Info \_ 2**](form-info-2.md) -Struktur. Alle-Strukturen haben dieselbe Ebene.

</dd> <dt>

*cbbuf* \[ in\]
</dt> <dd>

Gibt die Größe des Puffers in Bytes an, auf den *pform* zeigt.

</dd> <dt>

*pcbbenötigte* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine Variable, die die Anzahl der Bytes empfängt, die in das Array kopiert werden, auf das *pform* zeigt (wenn der Vorgang erfolgreich ist), oder die Anzahl der erforderlichen Bytes (wenn Sie fehlschlägt, da *cbbuf* zu klein ist).

</dd> <dt>

*pkreturned* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine Variable, die die Anzahl der in das Array kopierten Strukturen erhält, auf die *pform* zeigt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert ein Wert ungleich 0 (null).

Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird. Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können. Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.

 

Wenn der Aufrufer Remote ist und die *Ebene* 2 ist, ist der **StringType** -Wert der zurückgegebenen [**Formular \_ Informationen \_ 2**](form-info-2.md) -Strukturen immer **String \_ langpair**.

In Windows Vista werden die von **enumforms** zurückgegebenen Formulardaten aus einem lokalen Cache abgerufen, wenn sich *hprinter* auf einen Remote Druckserver oder einen Drucker bezieht, der von einem Druckserver gehostet wird, und mindestens eine geöffnete Verbindung mit einem Drucker auf dem Remote Drucker Server vorhanden ist. In allen anderen Konfigurationen werden die Formulardaten vom Remote Druckserver abgefragt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool. h (Include Windows. h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Unicode- und ANSI-Name<br/>   | **Enumformsw** (Unicode) und **enumformsa** (ANSI)<br/>                                             |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> <dt>

[**AddPrinter**](addprinter.md)
</dt> <dt>

[**Formular \_ Informationen \_ 1**](form-info-1.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> </dl>

 

 




