---
description: Löscht ein Druckertreiberpaket aus dem Treiberspeicher.
ms.assetid: a43a94d1-097e-457c-bce9-d4c434ecfa93
title: DeletePrinterDriverPackage-Funktion (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeletePrinterDriverPackage
- DeletePrinterDriverPackageA
- DeletePrinterDriverPackageW
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: d7247f4f0ef4d1f77f00664792d0b7b36bc991b19d437017b54db676731ccc70
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120112550"
---
# <a name="deleteprinterdriverpackage-function"></a>DeletePrinterDriverPackage-Funktion

Löscht ein Druckertreiberpaket aus dem Treiberspeicher.

## <a name="syntax"></a>Syntax


```C++
HRESULT DeletePrinterDriverPackage(
  _In_ LPCTSTR pszServer,
  _In_ LPCTSTR pszInfPath,
  _In_ LPCTSTR pszEnvironment
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pszServer* \[ In\]
</dt> <dd>

Ein Zeiger auf eine konstante, mit NULL beendete Zeichenfolge, die den Namen des Druckerservers angibt, von dem das Treiberpaket gelöscht wird. Ein  NULL-Zeigerwert bedeutet den lokalen Computer.

</dd> <dt>

*pszInfPath* \[ In\]
</dt> <dd>

Ein Zeiger auf eine konstante, mit NULL beendete Zeichenfolge, die den Pfad zur INF-Datei des \* Treibers angibt.

</dd> <dt>

*pszEnvironment* \[ In\]
</dt> <dd>

Ein Zeiger auf eine konstante, mit NULL beendete Zeichenfolge, die die Prozessorarchitektur angibt (z. B. Windows NT x86). Dies kann **NULL sein.**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

S \_ OK, wenn der Vorgang erfolgreich war.

E \_ ACCESSDENIED, wenn das Paket im Lieferumfang Windows.

HRESULT \_ CODE (ERROR \_ PRINT DRIVER PACKAGE IN \_ \_ \_ \_ USE), wenn das Paket verwendet wird.

**Andernfalls enthält das HRESULT** einen Fehlercode.

Weitere Informationen zu COM-Fehlercodes finden Sie unter [Fehlerbehandlung.](../com/error-handling-in-com.md)

## <a name="remarks"></a>Hinweise

> [!Note]  
> Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückkehrt. Wie schnell diese Funktion zurückgegeben wird, hängt von Laufzeitfaktoren wie Netzwerkstatus, Druckerserverkonfiguration und Implementierungsfaktoren des Druckertreibers ab, die beim Schreiben einer Anwendung schwer vorherzusagen sind. Das Aufrufen dieser Funktion aus einem Thread, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte dazu kommen, dass die Anwendung nicht reagiert.

 

Der Treiberspeicher ist in der Regel %windir% \\ inf oder %windir% \\ System32 \\ DriverStore \\ FileRepository.

Ein Treiberpaket, das im Lieferumfang Windows, kann mit dieser Funktion nicht entfernt werden.

Der Benutzer muss über Druckerverwaltungsberechtigungen verfügen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Spoolss.dll</dt> </dl>                    |
| Unicode- und ANSI-Name<br/>   | **DeletePrinterDriverPackageW** (Unicode) und **DeletePrinterDriverPackageA** (ANSI)<br/>           |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> </dl>

 

