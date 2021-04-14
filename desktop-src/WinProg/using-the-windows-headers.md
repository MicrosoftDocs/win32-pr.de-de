---
title: Verwenden der Windows-Header
description: Verwenden Sie die Windows-Header Dateien, um Anwendungen zu erstellen, die die Windows-API verwenden.
ms.assetid: a4def563-8ddc-4630-ae8a-86c07cf98374
keywords:
- Windows-API, Header Dateien
- C2065
- WINVER
- _WIN32_WINDOWS
- _WIN32_WINNT
- _WIN32_IE
- WIN32_LEAN_AND_MEAN
ms.topic: article
ms.date: 01/22/2020
ms.openlocfilehash: 4d27b14a6e545db9a9a38c205012b149942adf7f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390818"
---
# <a name="using-the-windows-headers"></a>Verwenden der Windows-Header

Die Header Dateien für die Windows-API ermöglichen es Ihnen, 32-und 64-Bit-Anwendungen zu erstellen. Sie enthalten Deklarationen für Unicode-und ANSI-Versionen der API. Weitere Informationen finden Sie unter [Unicode in der Windows-API](/windows/desktop/Intl/unicode-in-the-windows-api). Sie verwenden [Datentypen](windows-data-types.md) , mit denen Sie sowohl 32-als auch 64-Bit-Versionen der Anwendung aus einer einzelnen Quell Code Basis erstellen können. Weitere Informationen finden Sie unter Vorbereiten [für 64-Bit-Windows](/windows/desktop/WinProg64/getting-ready-for-64-bit-windows). Zu den zusätzlichen Features zählen [Header Anmerkungen](header-annotations.md) und eine [strikte Typüberprüfung](strict-type-checking.md).

-   [Visual C++ und die Windows-Header Dateien](#visual-c-and-the-windows-header-files)
-   [Makros für bedingte Deklarationen](#macros-for-conditional-declarations)
-   [Festlegen von WINVER oder \_ Win32 \_ Winnt](#setting-winver-or-_win32_winnt)
-   [Steuern der Struktur Verpackung](#controlling-structure-packing)
-   [Schnellere Builds mit kleineren Header Dateien](#faster-builds-with-smaller-header-files)
-   [Zugehörige Themen](#related-topics)

## <a name="visual-c-and-the-windows-header-files"></a>Visual C++ und die Windows-Header Dateien

Microsoft Visual C++ enthält Kopien der Windows-Header Dateien, die zum Zeitpunkt der Veröffentlichung von Visual C++ aktuell waren. Wenn Sie aktualisierte Header Dateien aus einem SDK installieren, können Sie daher auf Ihrem Computer mehrere Versionen der Windows-Header Dateien haben. Wenn Sie nicht sicherstellen, dass Sie die neueste Version der SDK-Header Dateien verwenden, erhalten Sie beim Kompilieren von Code, der Funktionen verwendet, die nach der Veröffentlichung von Visual C++ eingeführt wurden, den folgenden Fehlercode: error C2065: nicht deklarierter Bezeichner.

## <a name="macros-for-conditional-declarations"></a>Makros für bedingte Deklarationen

Bestimmte Funktionen, die von einer bestimmten Version von Windows abhängen, werden mithilfe von bedingtem Code deklariert. Dies ermöglicht es Ihnen, mithilfe des Compilers zu erkennen, ob Ihre Anwendung Funktionen verwendet, die in ihren Ziel Versionen von Windows nicht unterstützt werden. Um eine Anwendung zu kompilieren, die diese Funktionen verwendet, müssen Sie die entsprechenden Makros definieren. Andernfalls erhalten Sie die Fehlermeldung C2065.

Die Windows-Header Dateien verwenden Makros, um anzugeben, welche Versionen von Windows viele Programmier Elemente unterstützen. Daher müssen Sie diese Makros definieren, um neue Funktionen zu verwenden, die in den einzelnen wichtigen Betriebssystemversionen eingeführt wurden. (Einzelne Header Dateien können unterschiedliche Makros verwenden. wenn Kompilierungs Probleme auftreten, überprüfen Sie daher die Header Datei, die die Definition für bedingte Definitionen enthält.) Weitere Informationen finden Sie unter sdkddkver. h.

In der folgenden Tabelle werden die bevorzugten Makros beschrieben, die in den Windows-Header Dateien verwendet werden. Wenn Sie die ntddi- \_ Version definieren, müssen Sie auch \_ Win32 \_ Winnt definieren.



| Minimal Erforderliches System                       | Wert für ntddi- \_ Version            |
|-----------------------------------------------|-------------------------------------|
| Windows 10 1903 "19h1"                        | **Ntddi \_ WIN10 \_ 19h1** (0x0a000007) |
| Windows 10 1809 "Redstone 5"                  | **Ntddi \_ WIN10 \_ RS5** (0x0a000006)  |
| Windows 10 1803 "Redstone 4"                  | **Ntddi \_ WIN10 \_ RS4** (0x0a000005)  |
| Windows 10 1709 "Redstone 3"                  | **Ntddi \_ WIN10 \_ RS3** (0x0a000004)  |
| Windows 10 1703 "Redstone 2"                  | **Ntddi \_ WIN10 \_ RS2** (0x0a000003)  |
| Windows 10 1607 "Redstone 1"                  | **Ntddi \_ WIN10 \_ RS1** (0x0a000002)  |
| Windows 10 1511 "Schwellenwert 2"                 | **Ntddi \_ WIN10 \_ TH2** (0x0a000001)  |
| Windows 10 1507 "Schwellenwert"                   | **Ntddi \_ WIN10** (0x0a000000)       |
| Windows 8.1                                   | **Ntddi \_ Winblue** (0x06030000)     |
| Windows 8                                     | **Ntddi \_ WIN8** (0x06020000)        |
| Windows 7                                     | **Ntddi \_ Win7** (0x06010000)        |
| Windows Server 2008                           | **Ntddi \_ WS08** (0x06000100)        |
| Windows Vista mit Service Pack 1 (SP1)       | **Ntddi \_ VISTASP1** (0x06000100)    |
| Windows Vista                                 | **Ntddi \_ Vista** (0x06000000)       |
| Windows Server 2003 mit Service Pack 2 (SP2) | **Ntddi \_ WS03SP2** (0x05020200)     |
| Windows Server 2003 mit Service Pack 1 (SP1) | **Ntddi \_ WS03SP1** (0x05020100)     |
| Windows Server 2003                           | **Ntddi \_ WS03** (0x05020000)        |
| Windows XP mit Service Pack 3 (SP3)          | **Ntddi \_ WINXPSP3** (0x05010300)    |
| Windows XP mit Service Pack 2 (SP2)          | **Ntddi \_ XP SP2** (0x05010200)    |
| Windows XP mit Service Pack 1 (SP1)          | **Ntddi \_ WINXPSP1** (0x05010100)    |
| Windows XP                                    | **Ntddi \_ WinXP** (0x05010000)       |



 

In den folgenden Tabellen werden andere Makros beschrieben, die in den Windows-Header Dateien verwendet werden.



| Minimal Erforderliches System                           | Minimalwert für \_ Win32 \_ Winnt und winver |
|---------------------------------------------------|---------------------------------------------|
| Windows 10                                        | **\_ Win32- \_ Winnt- \_ WIN10** (0x0a00)          |
| Windows 8.1                                       | **\_ Win32 \_ Winnt \_ winblue** (0x0603)        |
| Windows 8                                         | **\_ Win32 \_ Winnt \_ WIN8** (0x0602)           |
| Windows 7                                         | **\_ Win32 \_ Winnt \_ Win7** (0x0601)           |
| Windows Server 2008                               | **\_ Win32- \_ Winnt- \_ WS08** (0x0600)           |
| Windows Vista                                     | **\_ Win32 \_ Winnt \_ Vista** (0x0600)          |
| Windows Server 2003 mit SP1, Windows XP mit SP2 | **\_ Win32 \_ Winnt \_ WS03** (0x0502)           |
| Windows Server 2003, Windows XP                   | **\_ Win32 \_ Winnt \_ WinXP** (0x0501)          |



 



| Mindestversion          | Minimalwert von \_ Win32 \_ IE      |
|-----------------------------------|-----------------------------------|
| Internet Explorer 11.0            | **\_ Win32 \_ IE \_ IE110** (0x0a00)   |
| Internet Explorer 10.0            | **\_ Win32 \_ IE \_ IE100** (0x0a00)   |
| Internet Explorer 9.0             | **\_ Win32 \_ IE \_ IE90** (0x0900)    |
| Internet Explorer 8.0             | **\_ Win32 \_ IE \_ IE80** (0x0800)    |
| Internet Explorer 7.0             | **\_ Win32 \_ IE \_ IE70** (0x0700)    |
| Internet Explorer 6,0 SP2         | **\_ Win32 \_ IE \_ IE60SP2** (0x0603) |
| Internet Explorer 6,0 SP1         | **\_ Win32 \_ IE \_ IE60SP1** (0x0601) |
| Internet Explorer 6.0             | **\_ Win32 \_ IE \_ IE60** (0x0600)    |
| Internet Explorer 5.5             | **\_ Win32 \_ IE \_ IE55** (0x0550)    |
| Internet Explorer 5,01            | **\_ Win32 \_ IE \_ IE501** (0x0501)   |
| Internet Explorer 5,0, 5.0 a, 5.0 b | **\_ Win32 \_ IE \_ IE50** (0x0500)    |



 

## <a name="setting-winver-or-_win32_winnt"></a>Festlegen von WINVER oder \_ Win32 \_ Winnt

Sie können diese Symbole mithilfe der define- \# Anweisung in jeder Quelldatei oder durch Angeben der/D-Compileroption definieren, die von Visual C++ unterstützt wird.

Wenn Sie z. b. winver in der Quelldatei festlegen möchten, verwenden Sie die folgende-Anweisung:

`#define WINVER 0x0502`

Verwenden Sie \_ \_ die folgende-Anweisung, um Win32 WinNT in der Quelldatei festzulegen:

`#define _WIN32_WINNT 0x0502`

Verwenden Sie zum Festlegen von \_ Win32 \_ Winnt mithilfe der/D-Compileroption den folgenden Befehl:

**cl-c/D \_ Win32 \_ Winnt = 0x0502** _Source_**. cpp**

Weitere Informationen zur Verwendung der/D-Compileroption finden Sie unter [/D (Präprozessordefinitionen)](/cpp/build/reference/d-preprocessor-definitions).

Beachten Sie, dass einige Funktionen, die in der neuesten Version von Windows eingeführt wurden, möglicherweise einer Service Pack für eine frühere Windows-Version hinzugefügt werden. Um eine Service Pack als Ziel festzulegen, müssen Sie daher möglicherweise \_ Win32 \_ Winnt mit dem Wert für die nächste Hauptversion des Betriebssystems definieren. Beispielsweise wurde die [**getdlldirectory**](/windows/desktop/api/winbase/nf-winbase-getdlldirectorya) -Funktion in Windows Server 2003 eingeführt und bedingt definiert, wenn \_ Win32 \_ Winnt 0x0502 oder größer ist. Diese Funktion wurde Windows XP mit SP1 ebenfalls hinzugefügt. Wenn Sie also \_ Win32 \_ Winnt als 0x0501 für Windows XP definieren, würden Sie die in Windows XP mit SP1 definierten Features übersehen.

## <a name="controlling-structure-packing"></a>Steuern der Struktur Verpackung

Projekte sollten kompiliert werden, um die standardmäßige Struktur Verpackung zu verwenden, die derzeit 8 Bytes beträgt, da der größte ganzzahlige Typ 8 Bytes ist. Dadurch wird sichergestellt, dass alle Strukturtypen in den Header Dateien in der Anwendung mit der gleichen Ausrichtung kompiliert werden, die von der Windows-API erwartet wird. Außerdem wird sichergestellt, dass Strukturen mit 8-Byte-Werten ordnungsgemäß ausgerichtet werden und keine Ausrichtungsfehler für Prozessoren verursachen, die die Daten Ausrichtung erzwingen.

Weitere Informationen finden Sie unter [/ZP (struct Member Alignment)](/cpp/build/reference/zp-struct-member-alignment) oder [Pack](/cpp/preprocessor/pack).

## <a name="faster-builds-with-smaller-header-files"></a>Schnellere Builds mit kleineren Header Dateien

Sie können die Größe der Windows-Header Dateien verringern, indem Sie einige der weniger allgemeinen API-Deklarationen wie folgt ausschließen:

-   Definieren \_ Sie Win32 schlank \_ und \_ Mittel, um APIs wie Cryptography, DDE, RPC, Shell und Windows Sockets auszuschließen.

    `#define WIN32_LEAN_AND_MEAN`

-   Definieren Sie mindestens ein *API* -Symbol, um die API auszuschließen. NOCOMM schließt z. b. die serielle Kommunikations-API aus. Eine Liste der unterstützten *API* -Symbole finden Sie unter Windows. h.

    `#define NOCOMM`

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Website für Windows SDK Download](https://msdn.microsoft.com/windowsserver/bb980924.aspx)
</dt> </dl>

 

 