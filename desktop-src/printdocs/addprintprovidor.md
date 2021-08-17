---
description: Die AddPrintProvidor-Funktion installiert einen lokalen Druckanbieter und verknüpft die Konfigurations-, Daten- und Anbieterdateien.
ms.assetid: f34549c3-0474-48ba-9307-5b36f02dbe1c
title: AddPrintProvidor-Funktion (Winspool.h)
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
ms.openlocfilehash: ca968397441765455e74059201c128be53f50916e5e28212c700078f52124fe8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117868735"
---
# <a name="addprintprovidor-function"></a>AddPrintProvidor-Funktion

Die **AddPrintProvidor-Funktion** installiert einen lokalen Druckanbieter und verknüpft die Konfigurations-, Daten- und Anbieterdateien.

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

*pName* \[ In\]
</dt> <dd>

Ein Zeiger auf eine auf NULL beendete Zeichenfolge, die den Namen des Servers angibt, auf dem der Anbieter installiert werden soll. Für Systeme, die nur die lokale Installation von Anbietern unterstützen, sollte dieser Parameter **NULL sein.**

</dd> <dt>

*Ebene* \[ In\]
</dt> <dd>

Die Ebene der -Struktur, auf die *pProviderInfo* zeigt. Dies kann einer der folgenden Sein.



| Wert                                                                                                | Bedeutung                                                                            |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | Die Funktion verwendet eine [**PROVIDOR \_ INFO \_ 1-Struktur.**](providor-info-1.md)<br/> |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | Die Funktion verwendet eine [**PROVIDOR \_ INFO \_ 2-Struktur.**](providor-info-2.md)<br/> |



 

</dd> <dt>

*pProviderInfo* \[ In\]
</dt> <dd>

Ein Zeiger auf eine Druckanbieterstruktur, wie durch Ebene *angegeben.*

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert ein Wert ungleich 0 (null).

Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.

## <a name="remarks"></a>Hinweise

> [!Note]  
> Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückkehrt. Wie schnell diese Funktion zurückgegeben wird, hängt von Laufzeitfaktoren wie Netzwerkstatus, Druckerserverkonfiguration und Implementierungsfaktoren des Druckertreibers ab, die beim Schreiben einer Anwendung schwer vorherzusagen sind. Das Aufrufen dieser Funktion aus einem Thread, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte dazu kommen, dass die Anwendung nicht reagiert.

 

Bevor eine Anwendung die **AddPrintProvidor-Funktion** aufruft, müssen alle vom Anbieter benötigten Dateien in das Verzeichnis SYSTEM32 kopiert werden.

Ein von **AddPrintProvidor hinzugefügter** Anbieter kann durch Aufrufen von [**DeletePrintProvidor entfernt werden.**](deleteprintprovidor.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool.drv</dt> </dl>                   |
| Unicode- und ANSI-Name<br/>   | **AddPrintProvidorW** (Unicode) und **AddPrintProvidorA** (ANSI)<br/>                               |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> <dt>

[**DeletePrintProvidor**](deleteprintprovidor.md)
</dt> <dt>

[**PROVIDOR \_ INFO \_ 1**](providor-info-1.md)
</dt> <dt>

[**PROVIDOR \_ INFO \_ 2**](providor-info-2.md)
</dt> </dl>

 

 




