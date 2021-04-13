---
description: Die deleteprintprovidor-Funktion entfernt einen von der addprintprovidor-Funktion hinzugefügten Druckanbieter.
ms.assetid: b7104f9a-111c-4904-a355-063bb4cc81f1
title: Deleteprintprovidor-Funktion (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeletePrintProvidor
- DeletePrintProvidorA
- DeletePrintProvidorW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: e68e56f115bac8abb1d0999990f57067f791d76d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216872"
---
# <a name="deleteprintprovidor-function"></a>Deleteprintprovidor-Funktion

Die **deleteprintprovidor** -Funktion entfernt einen von der [**addprintprovidor**](addprintprovidor.md) -Funktion hinzugefügten Druckanbieter.

## <a name="syntax"></a>Syntax


```C++
BOOL DeletePrintProvidor(
  _In_ LPTSTR pName,
  _In_ LPTSTR pEnvironment,
  _In_ LPTSTR pPrintProviderName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PName* \[ in\]
</dt> <dd>

Bleiben muss **null** sein.

</dd> <dt>

nach-oben  \[ in\]
</dt> <dd>

Ein Zeiger auf eine auf NULL endende Zeichenfolge, die die Umgebung angibt, aus der der Anbieter entfernt werden soll (z. b. Windows NT x86, Windows ia64 oder Windows x64). Wenn dieser Parameter **null** ist, wird der Anbieter aus der aktuellen Umgebung der aufrufenden Anwendung und des Client Computers (nicht der Zielanwendung und des Druck Servers) entfernt. **Null** ist der empfohlene Wert, da er eine maximale Portabilität ermöglicht.

</dd> <dt>

*pprintprovidername* \[ in\]
</dt> <dd>

Ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Namen des zu entfernenden Anbieters angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert ein Wert ungleich 0 (null).

Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird. Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können. Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool. h (Include Windows. h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Unicode- und ANSI-Name<br/>   | **Deleteprintprovidorw** (Unicode) und **deleteprintprovidora** (ANSI)<br/>                         |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> <dt>

[**Addprintprovidor**](addprintprovidor.md)
</dt> </dl>

 

 




