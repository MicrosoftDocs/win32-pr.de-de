---
description: Mit der deleteprinterdriverex-Funktion wird der angegebene Druckertreiber Name aus der Liste mit den Namen unterstützter Treiber auf einem Server entfernt, und die dem Treiber zugeordneten Dateien werden gelöscht. Mit dieser Funktion können auch bestimmte Versionen des Treibers gelöscht werden.
ms.assetid: 1a3d7c7f-1d45-4877-a8f7-a77f40e3c319
title: Deleteprinterdriverex-Funktion (winspool. h)
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
ms.openlocfilehash: b88ef38236961286875a1885dad9dde936887d13
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106347403"
---
# <a name="deleteprinterdriverex-function"></a>Deleteprinterdriverex-Funktion

Mit der **deleteprinterdriverex** -Funktion wird der angegebene Druckertreiber Name aus der Liste mit den Namen unterstützter Treiber auf einem Server entfernt, und die dem Treiber zugeordneten Dateien werden gelöscht. Mit dieser Funktion können auch bestimmte Versionen des Treibers gelöscht werden.

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

*PName* \[ in\]
</dt> <dd>

Ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Namen des Servers angibt, von dem der Treiber gelöscht werden soll. Wenn dieser Parameter **null** ist, löscht die Funktion den Druckertreiber auf dem lokalen Computer.

</dd> <dt>

nach-oben  \[ in\]
</dt> <dd>

Ein Zeiger auf eine auf NULL endende Zeichenfolge, die die Umgebung angibt, aus der der Treiber gelöscht werden soll (z. b. Windows NT x86, Windows ia64 oder Windows x64). Wenn dieser Parameter **null** ist, wird der Treiber Name aus der aktuellen Umgebung der aufrufenden Anwendung und des Client Computers (nicht der Zielanwendung und des Druck Servers) gelöscht.

</dd> <dt>

*pdrivername* \[ in\]
</dt> <dd>

Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Namen des zu löschenden Treibers angibt.

</dd> <dt>

*dwdeleteflag* \[ in\]
</dt> <dd>

Die Optionen zum Löschen von Dateien und Versionen des Treibers. Dieser Parameter kann einen oder mehrere der folgenden Werte aufweisen.



| Wert                                                                                                                                                                                                     | Bedeutung                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DPD_DELETE_SPECIFIC_VERSION"></span><span id="dpd_delete_specific_version"></span><dl> <dt>**DPD \_ - \_ bestimmte \_ Version löschen**</dt> </dl> | Löscht die in *dwversionflag* angegebene Version. Dadurch wird nicht sichergestellt, dass der Treiber aus der Liste der unterstützten Treiber für den Server entfernt wird.<br/>                  |
| <span id="DPD_DELETE_UNUSED_FILES"></span><span id="dpd_delete_unused_files"></span><dl> <dt>**DPD, nicht \_ \_ verwendete \_ Dateien löschen**</dt> </dl>             | Entfernt alle nicht verwendeten Treiberdateien.<br/>                                                                                                                                           |
| <span id="DPD_DELETE_ALL_FILES"></span><span id="dpd_delete_all_files"></span><dl> <dt>**DPD \_ \_ alle \_ Dateien löschen**</dt> </dl>                      | Löscht den Treiber nur dann, wenn alle zugehörigen Dateien entfernt werden können. Der Löschvorgang schlägt fehl, wenn eine der Treiberdateien von einem anderen installierten Treiber verwendet wird.<br/> |



 

Wenn DPD \_ Delete \_ Specific \_ Version nicht angegeben ist, löscht die Funktion alle Versionen des Treibers, wenn keine dieser Versionen verwendet wird. Wenn keines \_ der DPD \_ nicht verwendete Dateien löscht und keine DPD-Dateien gelöscht \_ \_ \_ \_ werden, werden die Treiberdateien von der Funktion nicht gelöscht.

</dd> <dt>

*dwversionflag* \[ in\]
</dt> <dd>

Die Version des zu löschenden Treibers. Dieser Parameter kann 0, 1, 2 oder 3 sein. Dieser Parameter wird nur verwendet, wenn *dwdeleteflag* das Flag für die DPD- \_ \_ spezifische \_ Version enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert ein Wert ungleich 0 (null).

Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird. Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können. Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.

 

Bevor die Funktion die Treiberdateien löscht, wird die **drvdriverevent** -Funktion des Treibers aufgerufen, sodass der Treiber alle privaten Dateien entfernen kann, die nicht verwendet werden. Weitere Informationen zu **drvdriverevent** finden Sie im Microsoft Windows Driver Development Kit (DDK).

Wenn die Treiberdateien zurzeit geladen sind, verschiebt die Funktion Sie in ein temporäres Verzeichnis und markiert Sie beim Neustart für das Löschen.

Vor dem Aufrufen von **deleteprinterdriverex** müssen Sie alle Drucker Objekte löschen, die den Druckertreiber verwenden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool. h (Include Windows. h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Unicode- und ANSI-Name<br/>   | **Deleteprinterdriverexw** (Unicode) und **deleteprinterdriverexa** (ANSI)<br/>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> <dt>

[**Addprinterdriverex**](addprinterdriverex.md)
</dt> </dl>

 

 




