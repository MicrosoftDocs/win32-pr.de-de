---
description: Die addprintprovidor-Funktion installiert einen lokalen Druckanbieter und verknüpft die Konfigurations-, Daten-und Anbieter Dateien.
ms.assetid: f34549c3-0474-48ba-9307-5b36f02dbe1c
title: Addprintprovidor-Funktion (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddPrintProvidor
- AddPrintProvidorA
- AddPrintProvidorW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: adf5f914046eb82e070e3e9915325989ff868d1e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106362451"
---
# <a name="addprintprovidor-function"></a>Addprintprovidor-Funktion

Die **addprintprovidor** -Funktion installiert einen lokalen Druckanbieter und verknüpft die Konfigurations-, Daten-und Anbieter Dateien.

## <a name="syntax"></a>Syntax


```C++
BOOL AddPrintProvidor(
  _In_ LPTSTR pName,
  _In_ DWORD  Level,
  _In_ LPBYTE pProviderInfo
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PName* \[ in\]
</dt> <dd>

Ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Namen des Servers angibt, auf dem der Anbieter installiert werden soll. Für Systeme, die nur die lokale Installation von Anbietern unterstützen, sollte dieser Parameter **null** sein.

</dd> <dt>

*Ebene* \[ in\]
</dt> <dd>

Die Ebene der-Struktur, auf die *pproviderinfo* verweist. Dies kann einer der folgenden sein:



| Wert                                                                                                | Bedeutung                                                                            |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | Die Funktion verwendet eine [**providor \_ Info \_ 1**](providor-info-1.md) -Struktur.<br/> |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | Die Funktion verwendet eine [**providor \_ Info \_ 2**](providor-info-2.md) -Struktur.<br/> |



 

</dd> <dt>

*pproviderinfo* \[ in\]
</dt> <dd>

Ein Zeiger auf eine Druckanbieter Struktur, wie nach *Ebene* angegeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert ein Wert ungleich 0 (null).

Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird. Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können. Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.

 

Bevor eine Anwendung die **addprintprovidor** -Funktion aufruft, müssen alle vom Anbieter benötigten Dateien in das Verzeichnis "System32" kopiert werden.

Ein von **addprintprovidor** hinzugefügter Anbieter kann entfernt werden, indem [**deleteprintprovidor**](deleteprintprovidor.md)aufgerufen wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool. h (Include Windows. h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Unicode- und ANSI-Name<br/>   | **Addprintprovidorw** (Unicode) und **addprintprovidora** (ANSI)<br/>                               |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> <dt>

[**Deleteprintprovidor**](deleteprintprovidor.md)
</dt> <dt>

[**Providor- \_ Info \_ 1**](providor-info-1.md)
</dt> <dt>

[**Providor- \_ Info \_ 2**](providor-info-2.md)
</dt> </dl>

 

 




