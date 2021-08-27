---
title: Registrierungsschlüssel, die von WOW64 betroffen sind
description: Unter WOW64 werden bestimmte Registrierungsschlüssel umgeleitet.
ms.assetid: 7b3f4f11-24bc-44f7-837e-d61d853c7291
keywords:
- 64-Bit-Registrierungsschlüssel Windows Programmierung
- WOW64 64-Bit-Windows Programmierung , Registrierungsschlüssel
- Umgeleitete Registrierungsschlüssel 64-Bit-Windows Programmierung
- Reflektierte Registrierungsschlüssel 64-Bit-Windows Programmierung
- 64-Bit-64-Bit-Registrierungsschlüssel Windows Programmieren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5193d4aa64848d132aca446c6d1e4a50777614725b69cae637da65aebfe94c0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120071610"
---
# <a name="registry-keys-affected-by-windows-installations-that-include-windows-on-windows-wow-support-for-multiple-processor-architectures"></a>Registrierungsschlüssel, die von Windows-Installationen betroffen sind, die Windows WOW-Unterstützung (Windows on Windows) für mehrere Prozessorarchitekturen enthalten

In 64-Bit-Windows-Installationen, die mit Windows XP und Windows Server 2003 beginnen, und in 32-Bit-ARM-Prozessorarchitekturen Windows-Installationen beginnend mit Windows RT (Windows 8) (nachfolgend als betroffene Windows-Installationen bezeichnet), werden bestimmte Registrierungsschlüssel *umgeleitet.*

Wenn bei betroffenen Windows-Installationen ein Prozess mit einer prozessorarchitektur, die sich von der Prozessorarchitektur des Betriebssystems unterscheidet (nachfolgend als **WOW-Anwendung** bezeichnet), einen Registrierungsaufruf für einen umgeleiteten Schlüssel vor sich geht, fängt der Registrierungsumleitung den Aufruf ab und ordnet ihn dem entsprechenden physischen Registrierungsspeicherort des Schlüssels zu. Beispielsweise wäre eine 32-Bit-Intel IA-32 x86-Anwendung, die auf einer \[  \] **AMD64/Intel** x86-x64 Windows-Installation ausgeführt wird, von einem umgeleiteten Registrierungsschlüssel betroffen. Wenn diese x86-Anwendung einen umgeleiteten Schlüssel aufruft, fängt der Registrierungsumleitung den Aufruf der Anwendung ab und leitet ihn an den entsprechenden physischen Registrierungsspeicherort des Schlüssels um. Weitere Informationen finden Sie unter [Registrierungsumleitung.](registry-redirector.md)

Andere Registrierungsschlüssel werden *von Anwendungen* unterschiedlicher Prozessorarchitekturen auf betroffenen Windows gemeinsam genutzt. WOW-Anwendungsregistrierungsaufrufe an freigegebene Schlüssel werden nicht umgeleitet. Stattdessen wird jeder logischen Ansicht der Registrierung eine physische Kopie des Schlüssels zugeordnet.

**Windows Server 2008, Windows Vista, Windows Server 2003 und Windows XP:** Eine Teilmenge der umgeleiteten Registrierungsschlüssel wird auch widergespiegelt, um die Schlüssel und ihre Werte zwischen 32-Bit- und 64-Bit-Ansichten der Registrierung synchron zu halten.  Die Registrierungslektion wurde ab Windows 7 und Windows Server 2008 R2 entfernt. Weitere Informationen finden Sie unter [Registry Reflection](registry-reflection.md).

In diesem Thema werden Registrierungsschlüssel aufgeführt, die umgeleitet, freigegeben oder umgeleitet und unter WOW widergespiegelt werden. Außerdem werden symbolische Verknüpfungen aufgeführt, die Kompatibilität für vorhandene Anwendungen bieten, die hartcodierte Registrierungsschlüsselpfade verwenden können, die **Wow6432Node** enthalten, den umgeleiteten Registrierungsspeicherort für x86-Prozesse, die auf AMD64-Windows ausgeführt werden. Weitere Informationen finden Sie unter

- [Umgeleitete, freigegebene und reflektierte Schlüssel unter WOW](#redirected-shared-and-reflected-keys-under-wow)
- [Windows on Windows 64 (WOW64) Symbolic Links](#windows-on-windows-64-wow64-symbolic-links)

## <a name="redirected-shared-and-reflected-keys-under-wow"></a>Umgeleitete, freigegebene und reflektierte Schlüssel unter WOW

Für WOW-Anwendungen auf Windows-Installationen werden in der folgenden Tabelle Registrierungsschlüssel aufgeführt, die umgeleitet, freigegeben oder umgeleitet und reflektiert werden. Unterschlüssel der Schlüssel in dieser Tabelle erben das Verhalten des übergeordneten Schlüssels, sofern nicht anders angegeben. Wenn in dieser Tabelle kein übergeordnetes Element für einen Schlüssel aufgeführt ist, wird der Schlüssel freigegeben.

| Key | Windows Server 2008 R2, Windows 7 und neuer | Windows Server 2008, Windows Vista, Windows Server 2003 und Windows XP |
|-|-|-|
| **HKEY \_ LOCAL \_ MACHINE** | Shared | Shared |
| **HKEY \_ LOCAL \_ MACHINE\SOFTWARE** | Redirected | Redirected |
| **HKEY \_ LOCAL \_ MACHINE\SOFTWARE-Klassen** \\  | Shared | Umgeleitet und reflektiert |
| **HKEY \_ LOCAL \_ MACHINE\SOFTWARE** \\ **Classes** \\ **Appid** | Shared | Umgeleitet und mit einer Ausnahme reflektiert: Die [Registrierungswerte DllSurrogate](../com/dllsurrogate.md) und [DllSurrogateExecutable]( ../com/dllsurrogateexecutable.md) werden nicht widergespiegelt, wenn ihr Wert eine leere Zeichenfolge ist. |
| **HKEY \_ LOCAL \_ MACHINE SOFTWARE** \\  \\ **Classes** \\ **CLSID** | Redirected | Wird nur für CLSIDs umgeleitet und reflektiert, die InprocServer32 oder InprocHandler32 nicht angeben. |
| **HKEY \_ LOCAL \_ MACHINE** \\  \\ **SOFTWARE-Klassen** \\ **DirectShow** | Redirected | Umgeleitet und reflektiert |
| **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE-Klassen** \\  \\ **HCP** | Shared | Shared |
| **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE Classes** \\  \\ **Interface** | Redirected | Umgeleitet und reflektiert |
| **HKEY \_ LOCAL \_ MACHINE\SOFTWARE** \\ **Classes** \\ **Media Type** | Redirected | Umgeleitet und reflektiert |
| **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE-Klassen** \\  \\ **MediaFoundation** | Redirected | Umgeleitet und reflektiert |
| **HKEY \_ LOCAL \_ MACHINE SOFTWARE** \\  \\ **Clients** | Shared | Redirected |
| **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **COM3** | Shared | Umgeleitet und reflektiert |
| **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **Cryptography** \\ **Aktuell** \\  | Shared | Shared |
| **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **Cryptography** \\ **Signatureis** \\ **Readers** | Shared | Shared |
| **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **Cryptography** \\ **Services** | Shared | Shared |
| **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **CTF** \\ **SystemShared** | Shared | Shared |
| **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **CTF** \\ **TIP** | Shared | Shared |
| **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **DFS** | Shared | Shared |
| **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **Driver Signing** | Shared | Shared |
| **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **EnterpriseCertificates** | Shared | Shared |
| **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **EventSystem** | Shared | Umgeleitet und reflektiert |
| **HKEY \_ LOKALE \_ COMPUTERSOFTWARE** \\  \\ **Microsoft** \\ **MSMQ** | Shared | Shared |
| **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **Non-Driver Signing** | Shared | Shared |
| **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **Editor** \\ **DefaultFonts** | Shared | Redirected |
| **HKEY \_ LOKALE \_ COMPUTERSOFTWARE** \\  \\ **Microsoft** \\ **OLE** | Shared | Umgeleitet und reflektiert |
| **HKEY \_ LOKALE \_ COMPUTERSOFTWARE** \\  \\ **Microsoft** \\ **RAS** | Shared | Shared |
| **HKEY \_ LOKALE \_ COMPUTERSOFTWARE** \\  \\ **Microsoft** \\ **RPC** | Shared | Umgeleitet und reflektiert |
| **HKEY \_ LOKALE \_ COMPUTERSOFTWARE** \\  \\ **Microsoft** \\ **SOFTWARE** \\ **Microsoft** Shared \\ **Tools** \\ **MSInfo** | Shared | Shared |
| **HKEY \_ LOKALE \_ COMPUTERSOFTWARE** \\  \\ **Microsoft** \\ **SystemCertificates** | Shared | Shared |
| **HKEY \_ LOKALE \_ COMPUTERSOFTWARE** \\  \\ **Microsoft** \\ **TermServLicensing** | Shared | Shared |
| **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **TransactionServer** | Shared | Shared |
| **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion App** \\ **Paths** | Shared | Redirected |
| **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Systemsteuerung** \\ **Cursors** \\ **Schemes** | Shared | Shared |
| **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Explorer** \\ **AutoplayHandlers** | Shared | Redirected |
| **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Explorer** \\ **DriveIcons** | Shared | Redirected |
| **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Explorer** \\ **KindMap** | Shared | Redirected |
| **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Gruppenrichtlinie** | Shared | Shared |
| **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Policies** | Shared | Shared |
| **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **PreviewHandlers** | Shared | Redirected |
| **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Setup** | Shared | Shared |
| **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Telefoniestandorte** \\  | Shared | Shared |
| **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **Console**| Shared | Redirected |
| **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **FontDpi** | Shared | Shared |
| **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **FontLink** | Shared | Redirected |
| **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **FontMapper** | Shared | Shared |
| **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **Fonts** | Shared | Shared |
| **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **FontSubstitutes** | Shared | Shared |
| **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** Gre \\ **\_ Initialize** | Shared | Redirected |
| **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** Image File Execution \\ **Options** | Shared | Redirected |
| **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** Language \\ **Pack** | Shared | Redirected |
| **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **NetworkCards** | Shared | Shared |
| **HKEY \_ LOKALE \_ COMPUTERSOFTWARE** \\  \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **Perflib** | Shared | Shared |
| **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **Ports** | Shared | Shared |
| **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **Print** | Shared | Shared |
| **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **ProfileList** | Shared | Shared |
| **HKEY \_ LOKALE \_ COMPUTERSOFTWARE** \\  \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion-Zeitzonen** \\  | Shared | Shared |
| **HKEY \_ \_** \\ RICHTLINIEN FÜR **LOKALE COMPUTERSOFTWARE** \\  | Shared | Shared |
| **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **RegisteredApplications** | Shared | Freigegeben; **Windows Server 2003 und Windows XP:** Dieser Schlüssel wurde in Windows Vista hinzugefügt. |
| **AKTUELLER \_ \_ HKEY-BENUTZER** | Shared | Shared |
| **HKEY \_ AKTUELLE \_** \\ **BENUTZERSOFTWARE** | Shared | Shared |
| **HKEY \_ CURRENT \_ USER** \\ **SOFTWARE** \\ **Classes** | Shared | Umgeleitet und reflektiert |
| **HKEY \_ CURRENT \_ USER** \\ **SOFTWARE** \\ **Classes** \\ **AppID** | Shared | Umgeleitet und mit einer Ausnahme reflektiert: Die Registrierungswerte [DllSurrogate](../com/dllsurrogate.md) und [DllSurrogateExecutable]( ../com/dllsurrogateexecutable.md) werden nicht widergespiegelt, wenn ihr Wert eine leere Zeichenfolge ist. |
| **HKEY \_ CURRENT \_ USER** \\ **SOFTWARE** \\ **Classes** \\ **CLSID** | Redirected | Umgeleitet und reflektiert |
| **HKEY \_ CURRENT \_ USER** \\ **SOFTWARE** \\ **Classes** \\ **DirectShow** | Redirected | Umgeleitet und reflektiert |
| **HKEY \_ CURRENT \_ USER** \\ **SOFTWARE-Klassenschnittstelle** \\  \\  | Redirected | Umgeleitet und reflektiert |
| **HKEY \_ CURRENT \_ USER** \\ **SOFTWARE** \\ **Classes** \\ **Media Type** | Redirected | Umgeleitet und reflektiert |
| **HKEY \_ CURRENT \_ USER** \\ **SOFTWARE** \\ **Classes** \\ **MediaFoundation** | Redirected | Umgeleitet und reflektiert |

**HKEY \_ CURRENT \_ USER** ist eine symbolische Verknüpfung mit der **HKEY \_** \\ **\[ USERS-SID, \]** wobei SID eine Übereinstimmung mit der \[ \] Sicherheits-ID (SID) des aktuellen Benutzers angibt. **HKEY \_ USERS** \\ **\[ SID \]** \\ **SOFTWARE** \\ **Classes** ist eine symbolische Verknüpfung mit **HKEY \_ USERS** \\ **\[ SID \] \_ Classes**.

**HKEY \_ CLASSES \_ ROOT** ist eine zusammengeführte Ansicht der **HKEY LOCAL \_ \_ MACHINE** \\ **SOFTWARE** \\ **Classes** und **HKEY CURRENT \_ \_ USER** \\ **SOFTWARE** \\ **Classes**. Umgeleitete Schlüssel in diesen Registrierungspfaden werden auch für **HKEY \_ CLASSES \_ ROOT** effektiv umgeleitet. Dies gilt auch für reflektierte Schlüssel auf Systemen, die sie unterstützen.

## <a name="windows-on-windows-64-wow64-symbolic-links"></a>Windows für symbolische Verknüpfungen Windows 64 (WOW64)

WOW64 definiert die folgenden symbolischen Verknüpfungen nur aus Gründen der Kompatibilität mit vorhandenen Anwendungen, die hartcodierte Registrierungsschlüsselpfade verwenden können, die Wow6432Node enthalten. Neue Anwendungen sollten die Verwendung von Wow6432Node in Registrierungsschlüsselpfaden vermeiden.

- **HKEY \_ LOCAL \_ MACHINE \\ SOFTWARE \\ Wow6432Node \\ Classes** is linked to **HKEY LOCAL MACHINE SOFTWARE \_ Classes \_ \\ \\ \\ Wow6432Node**
- **HKEY \_ LOCAL \_ MACHINE SOFTWARE Classes \\ \\ \\ Wow6432Node \\ AppId** is linked to **HKEY LOCAL MACHINE SOFTWARE Classes \_ \_ \\ \\ \\ AppId**
- **HKEY \_ LOCAL \_ MACHINE SOFTWARE Classes \\ \\ \\ Wow6432Node \\ PROTOCOLS** is linked to **HKEY LOCAL MACHINE SOFTWARE Classes \_ \_ \\ \\ \\ PROTOCOLS**
- **HKEY \_ LOCAL \_ MACHINE SOFTWARE Classes \\ \\ \\ Wow6432Node \\ Typelib** is linked to **HKEY LOCAL MACHINE SOFTWARE Classes \_ \_ \\ \\ \\ Typelib**

**Windows Server 2008, Windows Vista, Windows Server 2003 und Windows XP: HKEY \_ LOCAL \_ MACHINE \\ SOFTWARE \\ Wow6432Node \\ Classes** is linked to **HKEY LOCAL MACHINE SOFTWARE \_ Classes \_ \\ \\ \\ Wow6432Node**. Weitere symbolische Verknüpfungen wurden in Windows 7 und Windows Server 2008 R2 hinzugefügt.
