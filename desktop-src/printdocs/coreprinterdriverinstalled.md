---
description: Die coreprinterdriverinstallierte-Funktion meldet, ob ein Kern Druckertreiber mit der angegebenen GUID, dem angegebenen Datum und der angegebenen Version installiert ist.
ms.assetid: fb859aca-bb7b-495d-bd38-16ffa084c240
title: Coreprinterdriverinstallierte-Funktion (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CorePrinterDriverInstalled
- CorePrinterDriverInstalledA
- CorePrinterDriverInstalledW
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 2e4f7033e5ca15a892a208621049c2f500873d73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042634"
---
# <a name="coreprinterdriverinstalled-function"></a>Coreprinterdriverinstallierte-Funktion

Die **coreprinterdriverinstallierte** -Funktion meldet, ob ein Kern Druckertreiber mit der angegebenen GUID, dem angegebenen Datum und der angegebenen Version installiert ist.

## <a name="syntax"></a>Syntax


```C++
HRESULT CorePrinterDriverInstalled(
  _In_  LPCTSTR   pszServer,
  _In_  LPCTSTR   pszEnvironment,
  _In_  GUID      CoreDriverGUID,
  _In_  FILETIME  ftDriverDate,
  _In_  DWORDLONG dwlDriverVersion,
  _Out_ BOOL      *pbDriverInstalled
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pszserver* \[ in\]
</dt> <dd>

Zeiger auf eine Konstante, auf NULL abschließende Zeichenfolge, die den Namen des Drucker Servers angibt. Verwenden Sie für den lokalen Computer **null** .

</dd> <dt>

*pszenvironment* \[ in\]
</dt> <dd>

Zeiger auf eine Konstante, auf NULL abschließende Zeichenfolge, die die Prozessorarchitektur angibt (z. b. Windows NT x86). Dieser Wert kann **null** sein.

</dd> <dt>

*Coredriverguid* \[ in\]
</dt> <dd>

Die GUID des Haupt Druckertreibers.

</dd> <dt>

*ftdriverdate* \[ in\]
</dt> <dd>

Das Datum des Haupt Druckertreibers.

</dd> <dt>

*dwldriverversion* \[ in\]
</dt> <dd>

Die Version des Haupt Druckertreibers.

</dd> <dt>

*pbdriverinstalliert* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf **true** , wenn der Treiber oder eine neuere Version installiert ist, andernfalls **false** .

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn der Vorgang erfolgreich ist, ist der Rückgabewert S \_ OK; andernfalls enthält das **HRESULT** einen Fehlercode.

Weitere Informationen zu COM-Fehlercodes finden Sie unter [Fehlerbehandlung](../com/error-handling-in-com.md).

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird. Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können. Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool. h (Include Windows. h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Spoolss.dll</dt> </dl>                    |
| Unicode- und ANSI-Name<br/>   | **Coreprinterdriverinstalledw** (Unicode) und **coreprinterdriverinstalleda** (ANSI)<br/>           |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> </dl>

 

