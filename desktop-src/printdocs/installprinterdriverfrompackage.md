---
description: Installiert einen Druckertreiber aus einem Treiberpaket, das sich im Treiberspeicher des Druckerservers befindet.
ms.assetid: 5906d9c6-9fbf-4ec6-81ce-112a9ef6d7c0
title: InstallPrinterDriverFromPackage-Funktion (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InstallPrinterDriverFromPackage
- InstallPrinterDriverFromPackageA
- InstallPrinterDriverFromPackageW
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 3248fc1a2392e2a04fd83c58ddcc08a110eec94779b634ce6a348639d4d2a5c2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120112470"
---
# <a name="installprinterdriverfrompackage-function"></a>InstallPrinterDriverFromPackage-Funktion

Installiert einen Druckertreiber aus einem Treiberpaket, das sich im Treiberspeicher des Druckerservers befindet.

## <a name="syntax"></a>Syntax


```C++
HRESULT InstallPrinterDriverFromPackage(
  _In_ LPCTSTR pszServer,
  _In_ LPCTSTR pszInfPath,
  _In_ LPCTSTR pszDriverName,
  _In_ LPCTSTR pszEnvironment,
  _In_ DWORD   dwFlags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pszServer* \[ In\]
</dt> <dd>

Ein Zeiger auf eine konstante, auf NULL endende Zeichenfolge, die den Namen des Druckservers angibt. **NULL** bedeutet den lokalen Computer.

</dd> <dt>

*pszInfPath* \[ In\]
</dt> <dd>

Ein Zeiger auf eine konstante, auf NULL endende Zeichenfolge, die den Treiberspeicherpfad zur INF-Datei des Druckertreibers angibt. **NULL** bedeutet, dass sich der Treiber in einer inf-Datei befindet, die mit Windows geliefert wird.

</dd> <dt>

*pszDriverName* \[ In\]
</dt> <dd>

Ein Zeiger auf eine auf NULL endende konstante Zeichenfolge, die den Namen des Treibers angibt.

</dd> <dt>

*pszEnvironment* \[ In\]
</dt> <dd>

Ein Zeiger auf eine konstante, auf NULL endende Zeichenfolge, die die Prozessorarchitektur angibt (z. B. Windows NT x86). Dies kann **NULL** sein.

</dd> <dt>

*dwFlags* \[ In\]
</dt> <dd>

Dies kann nur 0 oder IPDFP \_ COPY \_ ALL FILES \_ sein. Der Wert 0 bedeutet, dass der Druckertreiber hinzugefügt und alle Dateien im Druckertreiberverzeichnis, die neuer als die aktuell verwendeten Dateien sind, kopiert werden müssen. Der Wert IPDFP \_ COPY \_ ALL FILES \_ bedeutet, dass der Druckertreiber und alle Dateien im Druckertreiberverzeichnis hinzugefügt werden müssen. Die Dateizeitstempel werden ignoriert, wenn *dwFlags* über den Wert IPDFP \_ COPY ALL FILES \_ \_ verfügt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn der Vorgang erfolgreich ist, lautet der Rückgabewert S \_ OK, andernfalls enthält das **HRESULT** einen Fehlercode.

Weitere Informationen zu COM-Fehlercodes finden Sie unter [Fehlerbehandlung.](../com/error-handling-in-com.md)

## <a name="remarks"></a>Hinweise

> [!Note]  
> Dies ist eine blockierende oder synchrone Funktion und wird möglicherweise nicht sofort zurückgegeben. Wie schnell diese Funktion zurückgegeben wird, hängt von Laufzeitfaktoren wie Netzwerkstatus, Druckerserverkonfiguration und Implementierungsfaktoren für Druckertreiber ab, die beim Schreiben einer Anwendung schwer vorherzusagen sind. Das Aufrufen dieser Funktion über einen Thread, der die Interaktion mit der Benutzeroberfläche verwaltet, kann dazu bringen, dass die Anwendung scheinbar nicht reagiert.

 

Der Treiberspeicher ist in der Regel entweder %windir% \\ inf oder %windir% \\ System32 \\ DriverStore \\ FileRepository.

**InstallPrinterDriverFromPackage** installiert auch andere Dateien im Paket, z. B. Farbprofile und Druckprozessoren.

Benutzer müssen über Druckerverwaltungsrechte verfügen, um sie entweder auf einem Remotecomputer oder auf dem lokalen Computer zu installieren, wenn der Benutzer mit Terminaldiensten angemeldet ist.

Nur signierte Pakete können auf einem Remotecomputer installiert werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Spoolss.dll</dt> </dl>                    |
| Unicode- und ANSI-Name<br/>   | **InstallPrinterDriverFromPackageW** (Unicode) und **InstallPrinterDriverFromPackageA** (ANSI)<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> </dl>

 

