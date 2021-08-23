---
description: Wenn ein Windows Installer-Paket Assemblys installiert oder ankündigt, speichert das Installationsprogramm Informationen zu diesen Assemblys in der lokalen Systemregistrierung.
ms.assetid: 1a6b0530-b5ad-49db-bc08-5b20d32420ef
title: Von Windows Installer geschriebene Assemblyregistrierungsschlüssel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3fd4a9bf3fa5e1eb557c2a179ec3e9a0853149ff197922a9fbf633a2869f41c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119746020"
---
# <a name="assembly-registry-keys-written-by-windows-installer"></a>Von Windows Installer geschriebene Assemblyregistrierungsschlüssel

Wenn ein Windows Installer-Paket Assemblys installiert oder ankündigt, speichert das Installationsprogramm Informationen zu diesen Assemblys in der lokalen Systemregistrierung. Beachten Sie, dass diese Registrierungsschlüssel nur intern von Windows Installer verwendet werden sollen und nicht von Ihrer Anwendung verwendet werden sollten. Inhalt, Speicherort und Struktur der in diesen Schlüsseln gespeicherten Informationen können sich ändern. Anwendungen sollten sich auf [**MsiProvideAssembly**](/windows/desktop/api/Msi/nf-msi-msiprovideassemblya) verlassen, um Assemblys zu verwalten.

Assemblys werden anhand ihrer Assemblynamen registriert. Die Namen der Werte, die an den folgenden Speicherorten gespeichert sind, sind die Assemblynamen. Die tatsächlichen Werte sind vom Typ REG MULTI SZ und enthalten Daten, die \_ von \_ [**MsiProvideAssembly**](/windows/desktop/api/Msi/nf-msi-msiprovideassemblya) zum Installieren oder Reparieren von Assemblys verwendet werden.

## <a name="information-about-private-assemblies"></a>Informationen zu privaten Assemblys

Windows Das Installationsprogramm speichert Informationen zu privaten Assemblys, die von Windows Installer-Paketen übertragen werden, die als benutzerspezifische Verwaltete Anwendungen installiert wurden, unter dem folgenden Registrierungsschlüssel:

**HKLM** \\ **SOFTWARE** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Installationsprogramm** \\ **Verwaltet** \\ **_Benutzer-SID_ *_\\_* Pfad** der \\ **Installerassemblys** \\ **_zur Konfigurationsdatei_**

Windows Das Installationsprogramm speichert Informationen zu privaten Assemblys, die von Windows Installer-Paketen übertragen werden, die pro Benutzer unter dem folgenden Registrierungsschlüssel installiert wurden:

**HKCU** \\ **Software** \\ **Microsoft** \\ **Installationsprogramm** \\ **Assemblys** \\ **_Pfad zur Konfigurationsdatei_**

Windows Das Installationsprogramm speichert Informationen zu privaten Assemblys, die von Windows Installer-Paketen übertragen und pro Computer unter dem folgenden Registrierungsschlüssel installiert werden:

**HKLM** \\ **SOFTWARE** \\ **Klassen** \\ **Installationsprogramm** \\ **Assemblys** \\ **_Pfad zur Konfigurationsdatei_**

## <a name="information-about-global-or-shared-assemblies"></a>Informationen zu globalen oder freigegebenen Assemblys

Windows Das Installationsprogramm speichert Informationen zu freigegebenen Assemblys, die von Windows Installer-Paketen übertragen werden, die als benutzerspezifische Verwaltete Anwendungen installiert wurden, unter dem folgenden Registrierungsschlüssel:

**HKLM** \\ **SOFTWARE** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Installationsprogramm** \\ **Verwaltet** \\ **_Benutzer-SID_ *_\\_*** \\ **Installationsprogrammassemblys** \\ **global**

Windows Das Installationsprogramm speichert Informationen zu freigegebenen Assemblys, die von Windows Installer-Paketen übertragen werden, die pro Benutzer unter dem folgenden Registrierungsschlüssel installiert wurden:

**HKCU** \\ **Software** \\ **Microsoft** \\ **Installationsprogramm** \\ **Assemblys** \\ **Global**

Windows Das Installationsprogramm speichert Informationen zu freigegebenen Assemblys, die von Windows Installer-Paketen übertragen und pro Computer unter dem folgenden Registrierungsschlüssel installiert werden:

**HKLM** \\ **SOFTWARE** \\ **Klassen** \\ **Installationsprogramm** \\ **Assemblys** \\ **Global**

 

 



