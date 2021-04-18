---
title: Registrierungsschlüssel, die von WOW64 betroffen sind
description: Unter WOW64 werden bestimmte Registrierungsschlüssel umgeleitet.
ms.assetid: 7b3f4f11-24bc-44f7-837e-d61d853c7291
keywords:
- Registrierungsschlüssel 64-Bit-Windows-Programmierung
- WOW64 64-Bit-Windows-Programmierung, Registrierungsschlüssel
- umgeleitete Registrierungsschlüssel 64-Bit-Windows-Programmierung
- reflektierte Registrierungsschlüssel 64-Bit-Windows-Programmierung
- gemeinsam genutzte Registrierungsschlüssel 64-Bit-Windows-Programmierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48278bfd42656b05d0e1f2be4402496a873022d1
ms.sourcegitcommit: 35bb565804eaeed7ac5503595753f59d120076dd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "106354890"
---
# <a name="registry-keys-affected-by-windows-installations-that-include-windows-on-windows-wow-support-for-multiple-processor-architectures"></a>Registrierungsschlüssel, die von Windows-Installationen betroffen sind, die Unterstützung für Windows on Windows (WOW) für mehrere Prozessorarchitekturen enthalten

In 64-Bit-Windows-Installationen ab Windows XP und Windows Server 2003 und in 32 der Windows-Installation mit der-Bit-ARM-Prozessorarchitektur, beginnend mit Windows RT (Windows 8) (im folgenden als **betroffene Windows-Installationen** referenziert), werden bestimmte Registrierungsschlüssel *umgeleitet*.

Wenn bei betroffenen Windows-Installationen ein Prozess mit einer Prozessorarchitektur, der sich von der Prozessorarchitektur des Betriebssystems unterscheidet (im folgenden als **Wow-Anwendung** bezeichnet), einen Registrierungs Rückruf für einen umgeleiteten Schlüssel durchführt, fängt der Registrierungs-Redirector den-Befehl ab und ordnet ihn dem entsprechenden physischen Registrierungs Speicherort des Schlüssels zu. Beispielsweise \[  \] würde eine auf einer **amd64** /Intel x86-x64-Windows-Installation auf einer amd64/Intel x86-x64-Windows-Installation ausgeführt 32-Bit-Intel IA-32-Anwendung von einem umgeleiteten Registrierungsschlüssel betroffen. wenn diese x86-Anwendung einen umgeleiteten Schlüssel aufruft, fängt der Registrierungs-Redirector den Aufruf der Anwendung ab und leitet ihn an den entsprechenden physischen Registrierungs Speicherort Weitere Informationen finden Sie unter [Registry Redirector](registry-redirector.md).

Andere Registrierungsschlüssel werden von Anwendungen mit unterschiedlichen Prozessorarchitekturen auf betroffenen Windows-Installationen *gemeinsam genutzt* . WOW-Anwendungs Registrierungs Aufrufe an gemeinsam genutzte Schlüssel werden nicht umgeleitet. Stattdessen wird jeder logischen Ansicht der Registrierung eine physische Kopie des Schlüssels zugeordnet.

**Windows Server 2008, Windows Vista, Windows Server 2003 und Windows XP:** Eine Teilmenge umgeleiteter Registrierungsschlüssel wird ebenfalls *reflektiert* , um die Schlüssel und deren Werte zwischen den 32-Bit-und 64-Bit-Sichten der Registrierung zu synchronisieren. Die Registrierungs Reflektion wurde ab Windows 7 und Windows Server 2008 R2 entfernt. Weitere Informationen finden Sie unter [Registry Reflection](registry-reflection.md).

In diesem Thema werden Registrierungsschlüssel aufgelistet, die umgeleitet, freigegeben oder umgeleitet und unter wow reflektiert werden. Außerdem werden symbolische Verknüpfungen aufgelistet, die Kompatibilität für vorhandene Anwendungen bieten, die möglicherweise hart codierte Registrierungsschlüssel Pfade mit **Wow6432Node**, den umgeleiteten Registrierungs Speicherort für x86-Prozesse, die auf amd64 Windows-Installationen ausgeführt werden. Weitere Informationen finden Sie unter

- [Umgeleitete, freigegebene und reflektierte Schlüssel unter wow](#redirected-shared-and-reflected-keys-under-wow)
- [Symbolische Links zu Windows auf Windows 64 (WOW64)](#windows-on-windows-64-wow64-symbolic-links)

## <a name="redirected-shared-and-reflected-keys-under-wow"></a>Umgeleitete, freigegebene und reflektierte Schlüssel unter wow

Für WoW-Anwendungen auf betroffenen Windows-Installationen werden in der folgenden Tabelle die Registrierungsschlüssel aufgelistet, die umgeleitet, freigegeben oder umgeleitet und reflektiert werden. Die Unterschlüssel der Schlüssel in dieser Tabelle erben das Verhalten des übergeordneten Schlüssels, sofern nicht anders angegeben. Wenn für einen Schlüssel kein übergeordnetes Element in dieser Tabelle aufgelistet ist, wird der Schlüssel freigegeben.

| Schlüssel | Windows Server 2008 R2, Windows 7 und höher | Windows Server 2008, Windows Vista, Windows Server 2003 und Windows XP |
|-|-|-|
| **lokaler HKEY- \_ \_ Computer** | Shared | Shared |
| **HKEY \_ lokale \_ machine\software** | Redirected | Redirected |
| **HKEY \_ Lokale \_ machine\softwareklassen** \\  | Shared | Umgeleitet und reflektiert |
| **HKEY \_ Lokale \_ machine\softwareklassen** \\  \\ **AppID** | Shared | Umgeleitet und reflektieren mit einer Ausnahme: die Registrierungs Werte [dllersatz](../com/dllsurrogate.md) und [dllsurrogateexe]( ../com/dllsurrogateexecutable.md) werden nicht widergespiegelt, wenn ihr Wert eine leere Zeichenfolge ist. |
| **HKEY \_ \_** \\  \\  \\ **CLSID** der Software Klassen für lokale Computer | Redirected | Umgeleitet und spiegeln sich nur für CLSIDs wider, die InprocServer32 oder InprocHandler32 nicht angeben. |
| **HKEY \_ \_** Software Klassen des lokalen Computers \\  \\  \\ **DirectShow** | Redirected | Umgeleitet und reflektiert |
| **HKEY \_ Software Klassen für lokale \_ Computer** \\  \\  \\ **HCP** | Shared | Shared |
| **HKEY \_ \_** \\  \\  \\ **Schnittstelle** der Software Klassen für lokale Computer | Redirected | Umgeleitet und reflektiert |
| **HKEY \_ Medientyp "local \_ machine\software** \\ **Classes** \\  " | Redirected | Umgeleitet und reflektiert |
| **HKEY \_ \_** Software Klassen von lokalen Computern \\  \\  \\ **mediafoundung** | Redirected | Umgeleitet und reflektiert |
| **HKEY \_ \_** \\ **Software** \\ **Clients** für lokale Computer | Shared | Redirected |
| **HKEY \_ Software für den lokalen \_ Computer** \\  \\ **Microsoft** \\ **COM3** | Shared | Umgeleitet und reflektiert |
| **HKEY \_ Lokale \_ Computer** \\ **Software** \\ **Microsoft** \\ **Cryptography** \\ **Calais** \\ **aktuell** | Shared | Shared |
| **HKEY \_ Lokale \_ Computer** \\ **Software** \\ **Microsoft** \\ **Cryptography** \\ **Calais**- \\ **Reader** | Shared | Shared |
| **HKEY \_ Software für den lokalen \_ Computer** \\  \\ **Microsoft** \\ **Kryptografiedienste** \\  | Shared | Shared |
| **HKEY \_ Software für den lokalen \_ Computer** \\  \\ **Microsoft** \\ **CTF** \\ **systemshared** | Shared | Shared |
| **HKEY \_ Software für den lokalen \_ Computer** \\  \\ **Microsoft** \\ **CTF** \\ **Tip** | Shared | Shared |
| **HKEY \_ Software für den lokalen \_ Computer** \\  \\ **Microsoft** \\ **DFS** | Shared | Shared |
| **HKEY \_ Lokale \_ Computer** \\ **Software** \\ **Microsoft**- \\ **Treiber Signierung** | Shared | Shared |
| **HKEY \_ Software für den lokalen \_ Computer** \\  \\ **Microsoft** \\ **enterpriszertifikate** | Shared | Shared |
| **HKEY \_ Lokale \_ Computer** \\ **Software** \\ **Microsoft** \\ **EventSystem** | Shared | Umgeleitet und reflektiert |
| **HKEY \_ Software für den lokalen \_ Computer** \\  \\ **Microsoft** \\ **MSMQ** | Shared | Shared |
| **HKEY \_ Lokale \_ Computer** \\ **Software** \\ **Microsoft** \\ **-nicht-Treiber Signatur** | Shared | Shared |
| **HKEY \_ Software für den lokalen \_ Computer** \\  \\ **Microsoft** \\ **Notepad** \\ **defaultfonts** | Shared | Redirected |
| **HKEY \_ Software für den lokalen \_ Computer** \\  \\ **Microsoft** \\ **OLE** | Shared | Umgeleitet und reflektiert |
| **HKEY \_ Software für den lokalen \_ Computer** \\  \\ **Microsoft** \\ **RAS** | Shared | Shared |
| **HKEY \_ Software für den lokalen \_ Computer** \\  \\ **Microsoft** \\ **RPC** | Shared | Umgeleitet und reflektiert |
| **HKEY \_ Software für den lokalen \_ Computer** \\  \\ **Microsoft** \\ **Software** \\ **Microsoft** \\ **Shared Tools** \\ **msinfo** | Shared | Shared |
| **HKEY \_ Software für den lokalen \_ Computer** \\  \\ **Microsoft** \\ **Systemzertifikate** | Shared | Shared |
| **HKEY \_ Software für den lokalen \_ Computer** \\  \\ **Microsoft** \\ **termservlicensing** | Shared | Shared |
| **HKEY \_ Software für den lokalen \_ Computer** \\  \\ **Microsoft** \\ **transaktionserver** | Shared | Shared |
| **HKEY \_ Lokale \_ Computer** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion**- \\ **App-Pfade** | Shared | Redirected |
| **HKEY \_ Lokale \_ Computer** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **System Steuerungs** \\ **Cursor** \\ **Schemas** | Shared | Shared |
| **HKEY \_ Software für den lokalen \_ Computer** \\  \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Explorer** \\ **autoplayhandlers** | Shared | Redirected |
| **HKEY \_ Lokale \_ Computer** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Explorer** \\ **DriveIcons** | Shared | Redirected |
| **HKEY \_ Lokale \_ Computer** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Explorer** \\ **kindmap** | Shared | Redirected |
| **HKEY \_ Lokale \_ Computer** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Gruppenrichtlinie** | Shared | Shared |
| **HKEY \_ Lokale \_ Computer** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion**- \\ **Richtlinien** | Shared | Shared |
| **HKEY \_ Lokale \_ Computer** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **PreviewHandlers** | Shared | Redirected |
| **HKEY \_ Lokale \_ Computer** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion**- \\ **Setup** | Shared | Shared |
| **HKEY \_ Lokale \_ Computer** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Telefoniestandorte** \\  | Shared | Shared |
| **HKEY \_ Lokale \_ Computer** \\ **Software** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **Console**| Shared | Redirected |
| **HKEY \_ Lokale \_ Computer** \\ **Software** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **fontdpi** | Shared | Shared |
| **HKEY \_ Lokale \_ Computer** \\ **Software** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **fontlink** | Shared | Redirected |
| **HKEY \_ Lokale \_ Computer** \\ **Software** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **fontmapper** | Shared | Shared |
| **HKEY \_ Lokale \_ Computer** \\ **Software** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **Fonts** | Shared | Shared |
| **HKEY \_ Lokale \_ Computer** \\ **Software** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **fontsubstitutionen** | Shared | Shared |
| **HKEY \_ Lokale \_ Computer** \\ **Software** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **GRE \_ initialisieren** | Shared | Redirected |
| **HKEY \_ Lokale \_ Computer** \\ **Software** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **Image File Execution Options** | Shared | Redirected |
| **HKEY \_ Lokale \_ Computer** \\ **Software** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **Language Pack** | Shared | Redirected |
| **HKEY \_ Lokale \_ Computer** \\ **Software** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **networkcards** | Shared | Shared |
| **HKEY \_ Lokale \_ Computer** \\ **Software** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **Perflib** | Shared | Shared |
| **HKEY \_ Lokale \_ Computer** \\ **Software** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion**- \\ **Ports** | Shared | Shared |
| **HKEY \_ Lokale \_ Computer** \\ **Software** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **Print** | Shared | Shared |
| **HKEY \_ Lokale \_ Computer** \\ **Software** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **ProfileList** | Shared | Shared |
| **HKEY \_ Lokale \_ Computer** \\ **Software** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\  Zeitzonen | Shared | Shared |
| **HKEY \_ \_** \\ **Software** \\ **Richtlinien** für lokale Computer | Shared | Shared |
| **HKEY \_ \_** \\ **Software**- \\ **RegisteredApplications** für lokale Computer | Shared | Genu **Windows Server 2003 und Windows XP:** Dieser Schlüssel wurde in Windows Vista hinzugefügt. |
| **Aktueller HKEY- \_ \_ Benutzer** | Shared | Shared |
| **HKEY \_ aktuelle \_ Benutzer** \\ **Software** | Shared | Shared |
| **HKEY \_ Aktuelle \_ Benutzer** \\ **Software**- \\ **Klassen** | Shared | Umgeleitet und reflektiert |
| **HKEY \_ Aktuelle \_ Benutzer** \\ **Software** \\ **Klassen** \\ **AppID** | Shared | Umgeleitet und reflektieren mit einer Ausnahme: die Registrierungs Werte [dllersatz](../com/dllsurrogate.md) und [dllsurrogateexe]( ../com/dllsurrogateexecutable.md) werden nicht widergespiegelt, wenn ihr Wert eine leere Zeichenfolge ist. |
| **HKEY \_ CLSID der aktuellen \_ Benutzer** \\ **Software** \\ **Klassen** \\  | Redirected | Umgeleitet und reflektiert |
| **HKEY \_ Aktuelle \_ Benutzer** \\ **Software** \\ **Klassen** \\ **DirectShow** | Redirected | Umgeleitet und reflektiert |
| **HKEY \_ Schnittstelle der aktuellen \_ Benutzer** \\ **Software** \\ **Klassen** \\  | Redirected | Umgeleitet und reflektiert |
| **HKEY \_ Medientyp der aktuellen \_ Benutzer** \\ **Software** \\ **Klassen** \\  | Redirected | Umgeleitet und reflektiert |
| **HKEY \_ Aktuelle \_ Benutzer** \\ **Software** \\ **Klassen** \\ **mediafoundung** | Redirected | Umgeleitet und reflektiert |

**HKEY \_ Aktueller \_ Benutzer** ist ein symbolischer Link zur **HKEY- \_ Benutzer** \\ -**\[ sid \]** , wobei sid eine Entsprechung \[ \] für die Sicherheits-ID (SID) des aktuellen Benutzers angibt. **HKEY \_ Benutzer**- \\ **\[ sid \]**- \\ **Software** \\ **Klassen** ist ein symbolischer Link zu **HKEY- \_ Benutzern**- \\ **\[ sid- \] \_ Klassen**.

**HKEY \_ Klassen \_** Stamm ist eine zusammengeführte Ansicht von HKEY-Software Klassen für **\_ lokale \_ Computer** \\  \\  und HKEY-Software Klassen für **\_ aktuelle \_ Benutzer** \\  \\ . Umgeleitete Schlüssel in diesen Registrierungs Pfaden werden auch für **HKEY- \_ Klassen \_ root** umgeleitet. Dies gilt auch für reflektierte Schlüssel auf Systemen, die diese unterstützen.

## <a name="windows-on-windows-64-wow64-symbolic-links"></a>Symbolische Links zu Windows auf Windows 64 (WOW64)

WOW64 definiert die folgenden symbolischen Verknüpfungen nur aus Gründen der Kompatibilität mit vorhandenen Anwendungen, die möglicherweise hart codierte Registrierungsschlüssel Pfade mit Wow6432Node verwenden. Neue Anwendungen sollten die Verwendung von Wow6432Node in Registrierungsschlüssel Pfaden vermeiden.

- **HKEY \_ Software des lokalen Computers \_ \\ \\ Wow6432Node \\ Klassen** sind mit **HKEY \_ - \_ \\ Software \\ Klassen \\ für lokale Computer verknüpft Wow6432Node**
- **HKEY \_ Software Klassen für den lokalen \_ Computer \\ \\ \\ Wow6432Node \\ AppID** ist mit **HKEY- \_ \_ Software Klassen für lokale Computer- \\ \\ \\ AppID** verknüpft
- **HKEY \_ Software Klassen des lokalen Computers \_ \\ \\ \\ Wow6432Node \\ Protokolle** sind mit **HKEY \_ - \_ \\ Software \\ Klassen \\ Protokollen für lokale Computer** verknüpft
- **HKEY \_ Software Klassen des lokalen Computers \_ \\ \\ \\ Wow6432Node \\ typelib** ist mit **HKEY \_ - \_ Software Klassen der lokalen Maschine \\ \\ \\ typelib** verknüpft.

**Windows Server 2008, Windows Vista, Windows Server 2003 und Windows XP: HKEY \_ Software des lokalen Computers \_ \\ \\ Wow6432Node \\ Klassen** sind mit **HKEY \_ - \_ Software Klassen für lokale Computer \\ \\ \\ Wow6432Node** verknüpft. Weitere symbolische Verknüpfungen wurden in Windows 7 und Windows Server 2008 R2 hinzugefügt.
