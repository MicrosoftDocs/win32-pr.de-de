---
description: Mit der addprinterdriver-Funktion wird ein lokaler oder Remote Druckertreiber installiert, und die Konfigurations-, Daten-und Treiberdateien werden zugeordnet.
ms.assetid: 0f762800-f5a5-40ea-8be1-7fd8bda23788
title: Addprinterdriver-Funktion (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddPrinterDriver
- AddPrinterDriverA
- AddPrinterDriverW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: de5a9e9d16a47dfe8b9620edc9acdc5c5fd4d552
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757860"
---
# <a name="addprinterdriver-function"></a>Addprinterdriver-Funktion

Mit der **addprinterdriver** -Funktion wird ein lokaler oder Remote Druckertreiber installiert, und die Konfigurations-, Daten-und Treiberdateien werden zugeordnet.

Wenn Sie Druckertreiber installieren oder aktualisieren, können Sie die [**addprinterdriverex**](addprinterdriverex.md) -Funktion verwenden, da Sie strikte Upgrades, strikte Downgrade, das Kopieren von neueren Dateien und das Kopieren aller Dateien (unabhängig von den Dateizeitstempeln) zulässt.

> [!Note]  
> Das Installieren eines Druckertreibers ohne Treiber Paket wird nicht mehr empfohlen. Verwenden Sie stattdessen " [**installprinterdriverfrompackage**](installprinterdriverfrompackage.md) ".

 

## <a name="syntax"></a>Syntax


```C++
BOOL AddPrinterDriver(
  _In_ LPTSTR pName,
  _In_ DWORD  Level,
  _In_ LPBYTE pDriverInfo
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PName* \[ in\]
</dt> <dd>

Ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Namen des Servers angibt, auf dem der Treiber installiert werden soll.

Wenn *PName* **null** ist, wird der Treiber lokal installiert.

</dd> <dt>

*Ebene* \[ in\]
</dt> <dd>

Die Version der-Struktur, auf die *pdriverinfo* verweist.

Dieser Wert kann 2, 3, 4, 6 oder 8 sein.

</dd> <dt>

*pdriverinfo* \[ in\]
</dt> <dd>

Ein Zeiger auf eine-Struktur, die Druckertreiber Informationen enthält. Dies hängt vom Wert der- *Ebene* ab.



| Wert | Drucker Laufwerks Struktur                  |
|-------|------------------------------------------|
| 2     | [**Treiber \_ Informationen \_ 2**](driver-info-2.md) |
| 3     | [**Treiber \_ Info \_ 3**](driver-info-3.md) |
| 4     | [**Treiber \_ Info \_ 4**](driver-info-4.md) |
| 6     | [**Treiber \_ Info \_ 6**](driver-info-6.md) |
| 8     | [**Treiber \_ Informationen \_ 8**](driver-info-8.md) |



 

Wenn der " **pvironment** "-Member der Struktur, auf die von *pdriverinfo* verwiesen wird, **null** ist, wird die aktuelle Umgebung des Aufrufers bzw. des Clients (nicht des Ziels/Servers) verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert ein Wert ungleich 0 (null).

Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird. Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können. Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.

 

Der [Aufrufer muss über die SeLoadDriverPrivilege-Berechtigung](/windows/desktop/SecAuthZ/authorization-constants)verfügen.

Bevor eine Anwendung die **addprinterdriver** -Funktion aufruft, müssen alle Dateien, die für den Treiber erforderlich sind, in das Druckertreiber Verzeichnis des Systems kopiert werden. Eine Anwendung kann den Namen dieses Verzeichnisses abrufen, indem Sie die [**getprinterdriverdirectory**](getprinterdriverdirectory.md) -Funktion aufrufen.

Eine Anwendung kann ermitteln, welche Druckertreiber zurzeit durch Aufrufen der Funktion " [**enumprinterdrivers**](enumprinterdrivers.md) " installiert werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool. h (Include Windows. h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Unicode- und ANSI-Name<br/>   | **Addprinterdriverw** (Unicode) und **addprinterdrivera** (ANSI)<br/>                               |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> <dt>

[**Addprinterdriverex**](addprinterdriverex.md)
</dt> <dt>

[**Treiber \_ Informationen \_ 2**](driver-info-2.md)
</dt> <dt>

[**Treiber \_ Info \_ 3**](driver-info-3.md)
</dt> <dt>

[**Treiber \_ Info \_ 4**](driver-info-4.md)
</dt> <dt>

[**Treiber \_ Info \_ 6**](driver-info-6.md)
</dt> <dt>

[**Enumprinterdrivers**](enumprinterdrivers.md)
</dt> <dt>

[**Getprinterdriverdirectory**](getprinterdriverdirectory.md)
</dt> </dl>

 

