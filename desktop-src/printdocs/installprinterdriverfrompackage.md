---
description: Installiert einen Druckertreiber aus einem Treiber Paket, das sich im Treiber Speicher des Drucker Servers befindet.
ms.assetid: 5906d9c6-9fbf-4ec6-81ce-112a9ef6d7c0
title: Installprinterdriverfrompackage-Funktion (winspool. h)
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
ms.openlocfilehash: f817f5e73537f6a71d8236ad9532acdf02a53552
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218220"
---
# <a name="installprinterdriverfrompackage-function"></a>Installprinterdriverfrompackage-Funktion

Installiert einen Druckertreiber aus einem Treiber Paket, das sich im Treiber Speicher des Druck Servers befindet.

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

*pszserver* \[ in\]
</dt> <dd>

Ein Zeiger auf eine Konstante, auf NULL abschließende Zeichenfolge, die den Namen des Drucker Servers angibt. **Null** bedeutet, dass der lokale Computer ist.

</dd> <dt>

*pszinfpath* \[ in\]
</dt> <dd>

Ein Zeiger auf eine Konstante, auf NULL abschließende Zeichenfolge, die den Treiber Speicherpfad zur INF-Datei des Druckertreibers angibt. **Null** bedeutet, dass sich der Treiber in einer INF-Datei befindet, die mit Windows ausgeliefert wird.

</dd> <dt>

*pszdrivername* \[ in\]
</dt> <dd>

Ein Zeiger auf eine Konstante, auf NULL abschließende Zeichenfolge, die den Namen des Treibers angibt.

</dd> <dt>

*pszenvironment* \[ in\]
</dt> <dd>

Ein Zeiger auf eine Konstante, auf NULL abschließende Zeichenfolge, die die Prozessorarchitektur angibt (z. b. Windows NT x86). Dieser Wert kann **null** sein.

</dd> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Dies kann nur 0 sein oder alle Dateien durch ipdfp \_ kopieren \_ \_ . Der Wert 0 bedeutet, dass der Druckertreiber hinzugefügt werden muss und alle Dateien im Druckertreiber Verzeichnis, die neuer als die derzeit verwendeten Dateien sind, kopiert werden müssen. Der Wert ipdfp \_ \_ alle Dateien kopieren \_ bedeutet, dass der Druckertreiber und alle Dateien im Druckertreiber Verzeichnis hinzugefügt werden müssen. Die Zeitstempel der Datei werden ignoriert, wenn *dwFlags* den Wert ipdfp \_ \_ alle Dateien kopieren hat \_ .

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn der Vorgang erfolgreich ist, ist der Rückgabewert S \_ OK; andernfalls enthält das **HRESULT** einen Fehlercode.

Weitere Informationen zu COM-Fehlercodes finden Sie unter [Fehlerbehandlung](../com/error-handling-in-com.md).

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird. Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können. Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.

 

Der Treiber Speicher ist in der Regel entweder% windir% \\ INF oder% windir% \\ system32 \\ DriverStore \\ FileRepository.

**Installprinterdriverfrompackage** installiert auch andere Dateien im Paket, z. b. Farbprofile und Druck Prozessoren.

Benutzer müssen über Drucker Administratorrechte verfügen, um entweder auf einem Remote Computer oder auf dem lokalen Computer zu installieren, wenn der Benutzer mit Terminal Diensten angemeldet ist.

Nur signierte Pakete können auf einem Remote Computer installiert werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool. h (Include Windows. h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Spoolss.dll</dt> </dl>                    |
| Unicode- und ANSI-Name<br/>   | **Installprinterdriverfrompackagew** (Unicode) und **installprinterdriverfrompackagea** (ANSI)<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> </dl>

 

