---
description: Die DeletePrinterDriverEx-Funktion entfernt den angegebenen Druckertreibernamen aus der Liste der Namen der unterstützten Treiber auf einem Server und löscht die dateien, die dem Treiber zugeordnet sind. Diese Funktion kann auch bestimmte Versionen des Treibers löschen.
ms.assetid: 1a3d7c7f-1d45-4877-a8f7-a77f40e3c319
title: DeletePrinterDriverEx-Funktion (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeletePrinterDriverEx
- DeletePrinterDriverExA
- DeletePrinterDriverExW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 88cc39227ffc5b1700a1348541e18215bc10c8b87a6bff942611f098059a70e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119950040"
---
# <a name="deleteprinterdriverex-function"></a>DeletePrinterDriverEx-Funktion

Die **DeletePrinterDriverEx-Funktion** entfernt den angegebenen Druckertreibernamen aus der Liste der Namen der unterstützten Treiber auf einem Server und löscht die dateien, die dem Treiber zugeordnet sind. Diese Funktion kann auch bestimmte Versionen des Treibers löschen.

## <a name="syntax"></a>Syntax


```C++
BOOL DeletePrinterDriverEx(
  _In_ LPTSTR pName,
  _In_ LPTSTR pEnvironment,
  _In_ LPTSTR pDriverName,
  _In_ DWORD  dwDeleteFlag,
  _In_ DWORD  dwVersionFlag
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pName* \[ In\]
</dt> <dd>

Ein Zeiger auf eine auf NULL beendete Zeichenfolge, die den Namen des Servers angibt, von dem der Treiber gelöscht werden soll. Wenn dieser Parameter **NULL ist,** löscht die Funktion den Druckertreiber vom lokalen Computer.

</dd> <dt>

*pUmgebung* \[ In\]
</dt> <dd>

Ein Zeiger auf eine auf NULL beendete Zeichenfolge, die die Umgebung angibt, aus der der Treiber gelöscht werden soll (z. B. Windows NT x86, Windows IA64 oder Windows x64). Wenn dieser Parameter **NULL ist,** wird der Treibername aus der aktuellen Umgebung der aufrufenden Anwendung und des Clientcomputers (nicht der Zielanwendung und des Druckerservers) gelöscht.

</dd> <dt>

*pDriverName* \[ In\]
</dt> <dd>

Ein Zeiger auf eine auf NULL beendete Zeichenfolge, die den Namen des zu löschenden Treibers angibt.

</dd> <dt>

*dwDeleteFlag* \[ In\]
</dt> <dd>

Die Optionen zum Löschen von Dateien und Versionen des Treibers. Dieser Parameter kann einen oder mehrere der folgenden Werte sein.



| Wert                                                                                                                                                                                                     | Bedeutung                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DPD_DELETE_SPECIFIC_VERSION"></span><span id="dpd_delete_specific_version"></span><dl> <dt>**DPD \_ DELETE \_ SPECIFIC \_ VERSION**</dt> </dl> | Löscht die in *dwVersionFlag angegebene Version.* Dadurch wird nicht sichergestellt, dass der Treiber aus der Liste der unterstützten Treiber für den Server entfernt wird.<br/>                  |
| <span id="DPD_DELETE_UNUSED_FILES"></span><span id="dpd_delete_unused_files"></span><dl> <dt>**DPD \_ LÖSCHT NICHT VERWENDETE \_ \_ DATEIEN.**</dt> </dl>             | Entfernt alle nicht verwendeten Treiberdateien.<br/>                                                                                                                                           |
| <span id="DPD_DELETE_ALL_FILES"></span><span id="dpd_delete_all_files"></span><dl> <dt>**DPD \_ DELETE \_ ALL \_ FILES**</dt> </dl>                      | Löscht den Treiber nur, wenn alle zugehörigen Dateien entfernt werden können. Der Löschvorgang schlägt fehl, wenn eine der Dateien des Treibers von einem anderen installierten Treiber verwendet wird.<br/> |



 

Wenn DPD DELETE SPECIFIC VERSION nicht angegeben ist, löscht die Funktion alle Versionen des Treibers, wenn keine dieser Versionen \_ \_ verwendet \_ wird. Wenn weder DPD DELETE UNUSED FILES noch DPD DELETE ALL FILES angegeben ist, löscht die Funktion \_ \_ keine \_ \_ \_ \_ Treiberdateien.

</dd> <dt>

*dwVersionFlag* \[ In\]
</dt> <dd>

Die Version des zu löschenden Treibers. Dieser Parameter kann 0, 1, 2 oder 3 sein. Dieser Parameter wird nur verwendet, *wenn dwDeleteFlag* das FLAG DPD \_ DELETE SPECIFIC VERSION \_ \_ enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert ein Wert ungleich 0 (null).

Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.

## <a name="remarks"></a>Hinweise

> [!Note]  
> Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückkehrt. Wie schnell diese Funktion zurückgegeben wird, hängt von Laufzeitfaktoren wie Netzwerkstatus, Druckerserverkonfiguration und Implementierungsfaktoren des Druckertreibers ab, die beim Schreiben einer Anwendung schwer vorherzusagen sind. Das Aufrufen dieser Funktion aus einem Thread, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte dazu kommen, dass die Anwendung nicht reagiert.

 

Bevor die Funktion die Treiberdateien löscht, ruft sie die **DrvDriverEvent-Funktion** des Treibers auf, sodass der Treiber alle privaten Dateien entfernen kann, die nicht verwendet werden. Weitere Informationen zu **DrvDriverEvent finden** Sie im Microsoft Windows Driver Development Kit (DDK).

Wenn die Treiberdateien derzeit geladen sind, verschiebt die Funktion sie in ein temporäres Verzeichnis und markiert sie beim Neustart zum Löschen.

Vor dem **Aufrufen von DeletePrinterDriverEx** müssen Sie alle Druckerobjekte löschen, die den Druckertreiber verwenden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool.drv</dt> </dl>                   |
| Unicode- und ANSI-Name<br/>   | **DeletePrinterDriverExW** (Unicode) und **DeletePrinterDriverExA** (ANSI)<br/>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> <dt>

[**AddPrinterDriverEx**](addprinterdriverex.md)
</dt> </dl>

 

 




