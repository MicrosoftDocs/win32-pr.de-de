---
description: Löscht ein Druckertreiber Paket aus dem Treiber Speicher.
ms.assetid: a43a94d1-097e-457c-bce9-d4c434ecfa93
title: Deleteprinterdriverpackage-Funktion (winspool. h)
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
ms.openlocfilehash: 54d1cda53795f4feab60e397ce7e38402f22374f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106355687"
---
# <a name="deleteprinterdriverpackage-function"></a>Deleteprinterdriverpackage-Funktion

Löscht ein Druckertreiber Paket aus dem Treiber Speicher.

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

*pszserver* \[ in\]
</dt> <dd>

Ein Zeiger auf eine Konstante, auf NULL abschließende Zeichenfolge, die den Namen des Drucker Servers angibt, von dem das Treiber Paket gelöscht wird. Ein **null** -Zeiger Wert bedeutet den lokalen Computer.

</dd> <dt>

*pszinfpath* \[ in\]
</dt> <dd>

Ein Zeiger auf eine Konstante, auf NULL abschließende Zeichenfolge, die den Pfad zur INF-Datei des Treibers angibt \* .

</dd> <dt>

*pszenvironment* \[ in\]
</dt> <dd>

Ein Zeiger auf eine Konstante, auf NULL abschließende Zeichenfolge, die die Prozessorarchitektur angibt (z. b. Windows NT x86). Dieser Wert kann **null** sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

S \_ OK, wenn der Vorgang erfolgreich ist.

E \_ AccessDenied, wenn das Paket mit Windows ausgeliefert wurde.

HRESULT- \_ Code (Fehler \_ Druck \_ Treiber Paket wird \_ \_ \_ verwendet), wenn das Paket verwendet wird.

Andernfalls enthält das **HRESULT** einen Fehlercode.

Weitere Informationen zu COM-Fehlercodes finden Sie unter [Fehlerbehandlung](../com/error-handling-in-com.md).

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird. Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können. Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.

 

Der Treiber Speicher ist in der Regel% windir% \\ INF oder% windir% \\ system32 \\ DriverStore \\ FileRepository.

Ein Treiber Paket, das mit Windows ausgeliefert wurde, kann mit dieser Funktion nicht entfernt werden.

Der Benutzer muss über Administrator Berechtigungen für die Druckerverwaltung verfügen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool. h (Include Windows. h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Spoolss.dll</dt> </dl>                    |
| Unicode- und ANSI-Name<br/>   | **DeletePrinterDriverPackageW** (Unicode) und **DeletePrinterDriverPackageA** (ANSI)<br/>           |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> </dl>

 

