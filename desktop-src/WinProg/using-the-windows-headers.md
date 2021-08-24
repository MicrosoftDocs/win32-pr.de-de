---
title: Verwenden der Windows Header
description: Verwenden Sie die Windows Headerdateien, um Anwendungen zu erstellen, die die Windows verwenden.
ms.assetid: a4def563-8ddc-4630-ae8a-86c07cf98374
keywords:
- Windows API, Headerdateien
- C2065
- Winver
- _WIN32_WINDOWS
- _WIN32_WINNT
- _WIN32_IE
- WIN32_LEAN_AND_MEAN
ms.topic: article
ms.date: 01/22/2020
ms.openlocfilehash: 886c5601683cc03fb2486f8be3b69f31c4619b721276babbc2c3e31e28c0a022
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119643590"
---
# <a name="using-the-windows-headers"></a>Verwenden der Windows Header

Mit den Headerdateien für die Windows-API können Sie 32- und 64-Bit-Anwendungen erstellen. Sie enthalten Deklarationen für Unicode- und ANSI-Versionen der API. Weitere Informationen finden Sie unter [Unicode in der Windows-API.](/windows/desktop/Intl/unicode-in-the-windows-api) Sie verwenden [Datentypen,](windows-data-types.md) mit denen Sie sowohl 32- als auch 64-Bit-Versionen Ihrer Anwendung aus einer einzigen Quellcodebasis erstellen können. Weitere Informationen finden Sie unter [Getting Ready for 64-bit Windows](/windows/desktop/WinProg64/getting-ready-for-64-bit-windows). Weitere Features sind [Headeranmerkungen](header-annotations.md) und [DIE STRICT-Typüberprüfung.](strict-type-checking.md)

-   [Visual C++ und die Windows Headerdateien](#visual-c-and-the-windows-header-files)
-   [Makros für bedingte Deklarationen](#macros-for-conditional-declarations)
-   [Festlegen von WINVER oder \_ WIN32 \_ WINNT](#setting-winver-or-_win32_winnt)
-   [Steuern der Strukturpackung](#controlling-structure-packing)
-   [Schnellere Builds mit kleineren Headerdateien](#faster-builds-with-smaller-header-files)
-   [Zugehörige Themen](#related-topics)

## <a name="visual-c-and-the-windows-header-files"></a>Visual C++ und die Windows Headerdateien

Microsoft Visual C++ enthält Kopien der Windows Headerdateien, die zum Zeitpunkt der Visual C++ waren. Wenn Sie aktualisierte Headerdateien aus einem SDK installieren, erhalten Sie daher möglicherweise mehrere Versionen der Windows-Headerdateien auf Ihrem Computer. Wenn Sie nicht sicherstellen, dass Sie die neueste Version der SDK-Headerdateien verwenden, erhalten Sie den folgenden Fehlercode beim Kompilieren von Code, der Features verwendet, die nach der Benachrichtigung von Visual C++ eingeführt wurden: Fehler C2065: nicht deklarierter Bezeichner.

## <a name="macros-for-conditional-declarations"></a>Makros für bedingte Deklarationen

Bestimmte Funktionen, die von einer bestimmten Version der Windows werden mit bedingtem Code deklariert. Auf diese Weise können Sie den Compiler verwenden, um zu ermitteln, ob Ihre Anwendung Funktionen verwendet, die für ihre Zielversionen von nicht unterstützt Windows. Um eine Anwendung zu kompilieren, die diese Funktionen verwendet, müssen Sie die entsprechenden Makros definieren. Andernfalls erhalten Sie die Fehlermeldung C2065.

Die Windows Headerdateien verwenden Makros, um anzugeben, welche Versionen von Windows viele Programmierelemente unterstützen. Daher müssen Sie diese Makros definieren, um neue Funktionen zu verwenden, die in den einzelnen Hauptversionen des Betriebssystems eingeführt werden. (Einzelne Headerdateien können unterschiedliche Makros verwenden. Überprüfen Sie daher bei Kompilierungsproblemen die Headerdatei, die die Definition für bedingte Definitionen enthält.) Weitere Informationen finden Sie unter SdkDdkVer.h.

In der folgenden Tabelle werden die bevorzugten Makros beschrieben, die in Windows Headerdateien verwendet werden. Wenn Sie NTDDI \_ VERSION definieren, müssen Sie auch \_ WIN32 \_ WINNT definieren.



| Mindestens erforderliches System                       | Wert für NTDDI \_ VERSION            |
|-----------------------------------------------|-------------------------------------|
| Windows 10 1903 "19H1"                        | **NTDDI \_ WIN10 \_ 19H1** (0x0A000007) |
| Windows 10 1809 "Redstone 5"                  | **NTDDI \_ WIN10 \_ RS5** (0x0A000006)  |
| Windows 10 1803 "Redstone 4"                  | **NTDDI \_ WIN10 \_ RS4** (0x0A000005)  |
| Windows 10 1709 "Redstone 3"                  | **NTDDI \_ WIN10 \_ RS3** (0x0A000004)  |
| Windows 10 1703 "Redstone 2"                  | **NTDDI \_ WIN10 \_ RS2** (0x0A000003)  |
| Windows 10 1607 "Redstone 1"                  | **NTDDI \_ WIN10 \_ RS1** (0x0A000002)  |
| Windows 10 1511 "Schwellenwert 2"                 | **NTDDI \_ WIN10 \_ TH2** (0x0A000001)  |
| Windows 10 1507 "Schwellenwert"                   | **NTDDI \_ WIN10** (0x0A000000)       |
| Windows 8.1                                   | **NTDDI \_ WINBLUE** (0x06030000)     |
| Windows 8                                     | **NTDDI \_ WIN8** (0x06020000)        |
| Windows 7                                     | **NTDDI \_ WIN7** (0x06010000)        |
| Windows Server 2008                           | **NTDDI \_ WS08** (0x06000100)        |
| Windows Vista mit Service Pack 1 (SP1)       | **NTDDI \_ VISTASP1** (0x06000100)    |
| Windows Vista                                 | **NTDDI \_ VISTA** (0x06000000)       |
| Windows Server 2003 mit Service Pack 2 (SP2) | **NTDDI \_ WS03SP2** (0x05020200)     |
| Windows Server 2003 mit Service Pack 1 (SP1) | **NTDDI \_ WS03SP1** (0x05020100)     |
| Windows Server 2003                           | **NTDDI \_ WS03** (0x05020000)        |
| Windows XP mit Service Pack 3 (SP3)          | **NTDDI \_ WINXPSP3** (0x05010300)    |
| Windows XP mit Service Pack 2 (SP2)          | **NTDDI \_ WINXPSP2** (0x05010200)    |
| Windows XP mit Service Pack 1 (SP1)          | **NTDDI \_ WINXPSP1** (0x05010100)    |
| Windows XP                                    | **NTDDI \_ WINXP** (0x05010000)       |



 

In den folgenden Tabellen werden andere Makros beschrieben, die in Windows Headerdateien verwendet werden.



| Mindestens erforderliches System                           | Mindestwert für \_ WIN32 \_ WINNT und WINVER |
|---------------------------------------------------|---------------------------------------------|
| Windows 10                                        | **\_ WIN32 \_ WINNT \_ WIN10** (0x0A00)          |
| Windows 8.1                                       | **\_ WIN32 \_ WINNT \_ WINBLUE** (0x0603)        |
| Windows 8                                         | **\_ WIN32 \_ WINNT \_ WIN8** (0x0602)           |
| Windows 7                                         | **\_ WIN32 \_ WINNT \_ WIN7** (0x0601)           |
| Windows Server 2008                               | **\_ WIN32 \_ WINNT \_ WS08** (0x0600)           |
| Windows Vista                                     | **\_ WIN32 \_ WINNT \_ VISTA** (0x0600)          |
| Windows Server 2003 mit SP1, Windows XP mit SP2 | **\_ WIN32 \_ WINNT \_ WS03** (0x0502)           |
| Windows Server 2003, Windows XP                   | **\_ WIN32 \_ WINNT \_ WINXP** (0x0501)          |



 



| Mindestversion          | Mindestwert von \_ WIN32 \_ IE      |
|-----------------------------------|-----------------------------------|
| Internet Explorer 11.0            | **\_ WIN32 \_ IE \_ IE110** (0x0A00)   |
| Internet Explorer 10.0            | **\_ WIN32 \_ IE \_ IE100** (0x0A00)   |
| Internet Explorer 9.0             | **\_ WIN32 \_ \_ IE90** (0x0900)    |
| Internet Explorer 8.0             | **\_ WIN32 \_ \_ IE80** (0x0800)    |
| Internet Explorer 7.0             | **\_ WIN32 \_ \_ IE70** (0x0700)    |
| Internet Explorer 6.0 SP2         | **\_ WIN32 \_ IE \_ IE60SP2** (0x0603) |
| Internet Explorer 6.0 SP1         | **\_ WIN32 \_ \_ IE60SP1** (0x0601) |
| Internet Explorer 6.0             | **\_ WIN32 \_ \_ IE60** (0x0600)    |
| Internet Explorer 5.5             | **\_ WIN32 \_ \_ IE55** (0x0550)    |
| Internet Explorer 5.01            | **\_ WIN32 \_ IE \_ IE501** (0x0501)   |
| Internet Explorer 5.0, 5.0a, 5.0b | **\_ WIN32 \_ IE \_ IE50** (0x0500)    |



 

## <a name="setting-winver-or-_win32_winnt"></a>Festlegen von WINVER oder \_ WIN32 \_ WINNT

Sie können diese Symbole definieren, indem Sie die define-Anweisung in jeder Quelldatei verwenden oder indem Sie die /D-Compileroption angeben, die von \# Visual C++.

Verwenden Sie beispielsweise die folgende -Anweisung, um WINVER in Ihrer Quelldatei festlegen:

`#define WINVER 0x0502`

Verwenden Sie die folgende Anweisung, um \_ \_ WIN32 WINNT in der Quelldatei fest zu legen:

`#define _WIN32_WINNT 0x0502`

Verwenden Sie den folgenden Befehl, um WIN32 WINNT mithilfe der \_ \_ Compileroption /D festlegen:

**cl -c /D \_ WIN32 \_ WINNT=0x0502** **CPP-Quelldatei** 

Informationen zur Verwendung der Compileroption /D finden Sie unter [/D (Präprozessordefinitionen).](/cpp/build/reference/d-preprocessor-definitions)

Beachten Sie, dass einige features, die in der neuesten Version von Windows eingeführt wurden, einem Service Pack für eine frühere Version von Windows. Daher müssen Sie möglicherweise \_ WIN32 WINNT mit dem Wert für die nächste Hauptversion des Betriebssystems definieren, um ein Service Pack \_ als Ziel festzulegen. Die [**GetDllDirectory-Funktion**](/windows/desktop/api/winbase/nf-winbase-getdlldirectorya) wurde beispielsweise in Windows Server 2003 eingeführt und ist bedingt definiert, wenn \_ WIN32 \_ WINNT 0x0502 ist. Diese Funktion wurde auch Windows XP mit SP1 hinzugefügt. Wenn Sie WIN32 WINNT als 0x0501 als Ziel für Windows XP definieren würden, würden Ihnen daher Funktionen fehlen, die in Windows XP mit \_ \_ SP1 definiert sind.

## <a name="controlling-structure-packing"></a>Steuern der Strukturpackung

Projekte sollten kompiliert werden, um die standardmäßige Strukturpackung zu verwenden, die derzeit 8 Bytes beträgt, da der größte integrale Typ 8 Bytes ist. Dadurch wird sichergestellt, dass alle Strukturtypen in den Headerdateien in die Anwendung mit der gleichen Ausrichtung kompiliert werden, die die Windows API erwartet. Außerdem wird sichergestellt, dass Strukturen mit 8-Byte-Werten ordnungsgemäß ausgerichtet sind und keine Ausrichtungsfehler bei Prozessoren verursachen, die die Datenausrichtung erzwingen.

Weitere Informationen finden Sie unter [/Zp (Struktur-Memberausrichtung)](/cpp/build/reference/zp-struct-member-alignment) oder [Packen von](/cpp/preprocessor/pack).

## <a name="faster-builds-with-smaller-header-files"></a>Schnellere Builds mit kleineren Headerdateien

Sie können die Größe der Windows-Headerdateien reduzieren, indem Sie einige der weniger häufigen API-Deklarationen wie folgt ausschließen:

-   Definieren Sie WIN32 LEAN AND MEAN, um APIs wie \_ \_ \_ Kryptografie, DDE, RPC, Shell und Windows Sockets auszuschließen.

    `#define WIN32_LEAN_AND_MEAN`

-   Definieren Sie mindestens eines der *NO-API-Symbole,* um die API auszuschließen. NOCOMM schließt beispielsweise die API für die serielle Kommunikation aus. Eine Liste der UNTERSTÜTZTEN *NO-API-Symbole* finden Sie unter Windows.h.

    `#define NOCOMM`

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Windows SDK-Downloadwebsite](https://msdn.microsoft.com/windowsserver/bb980924.aspx)
</dt> </dl>

 

 