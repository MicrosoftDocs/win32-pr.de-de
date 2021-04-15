---
description: Wenn Assemblys von einem Windows Installer Paket installiert oder angekündigt werden, speichert das Installationsprogramm Informationen zu diesen Assemblys in der Registrierung des lokalen Systems.
ms.assetid: 1a6b0530-b5ad-49db-bc08-5b20d32420ef
title: Von Windows Installer geschriebene assemblyregistrierungsschlüssel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bdd2ea7d290659fa9c1578d89be9a77dcc5cc10
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528868"
---
# <a name="assembly-registry-keys-written-by-windows-installer"></a>Von Windows Installer geschriebene assemblyregistrierungsschlüssel

Wenn Assemblys von einem Windows Installer Paket installiert oder angekündigt werden, speichert das Installationsprogramm Informationen zu diesen Assemblys in der Registrierung des lokalen Systems. Beachten Sie, dass diese Registrierungsschlüssel nur für die interne Verwendung durch Windows Installer vorgesehen sind und nicht von Ihrer Anwendung verwendet werden sollen. Der Inhalt, der Speicherort und die Struktur der in diesen Schlüsseln gespeicherten Informationen können geändert werden. Anwendungen sollten sich zum Verwalten von Assemblys auf [**msiprovidebug**](/windows/desktop/api/Msi/nf-msi-msiprovideassemblya) verlassen.

Assemblys werden durch ihre Assemblynamen registriert. Die Namen der Werte, die an den folgenden Speicherorten gespeichert sind, sind die Assemblynamen. Die tatsächlichen Werte sind vom Typ reg \_ \_ MultiSZ und enthalten Daten, die von [**MsiProvideAssembly**](/windows/desktop/api/Msi/nf-msi-msiprovideassemblya) zum Installieren oder Reparieren von Assemblys verwendet werden.

## <a name="information-about-private-assemblies"></a>Informationen zu privaten Assemblys

Windows Installer speichert Informationen zu privaten Assemblys, die von Windows Installer Paketen übertragen wurden, die als verwaltete Anwendungen pro Benutzer unter dem folgenden Registrierungsschlüssel installiert wurden:

**HKLM** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Installer** \\ **Verwaltet** \\ **_Benutzer-SID_ *_\\_*** Installationsassemblypfad \\  \\ * *_zur Konfigurationsdatei_* _

Windows Installer speichert Informationen zu privaten Assemblys, die von Windows Installer Paketen getragen werden, die pro Benutzer unter dem folgenden Registrierungsschlüssel installiert wurden:

_*HKCU- **\\** Software **\\** Microsoft Installer- **\\** Assemblypfad **\\** **\\** _zur Konfigurationsdatei_*_

In Windows Installer werden Informationen zu privaten Assemblys gespeichert, die von Windows Installer Paketen übertragen und pro Computer unter dem folgenden Registrierungsschlüssel installiert werden:

_*Assemblypfad der HKLM- **\\** Software **\\** Klassen **\\** Installations **\\** **\\** _Pfad zur Konfigurationsdatei_*_

## <a name="information-about-global-or-shared-assemblies"></a>Informationen zu globalen oder freigegebenen Assemblys

In Windows Installer werden Informationen zu freigegebenen Assemblys gespeichert, die von Windows Installer Paketen verwendet werden, die als verwaltete Anwendungen pro Benutzer unter dem folgenden Registrierungsschlüssel installiert wurden:

_*HKLM **\\** Software **\\** Microsoft **\\** Windows **\\** CurrentVersion **\\** Installer **\\** Managed **\\** _User sid_*_ \\ _ *installationsassemblys **\\** **\\** Global**

In Windows Installer werden Informationen zu freigegebenen Assemblys gespeichert, die von Windows Installer Paketen verwendet werden, die pro Benutzer unter dem folgenden Registrierungsschlüssel installiert wurden:

**HKCU** \\ **Software** \\ **Microsoft** \\ **Installer** \\ Assemblys  \\ **Global**

In Windows Installer werden Informationen zu freigegebenen Assemblys gespeichert, die von Windows Installer Paketen getragen und pro Computer unter dem folgenden Registrierungsschlüssel installiert werden:

**HKLM** \\ **Software** \\ **Klassen** \\ **Installer** \\ Assemblys  \\ **Global**

 

 



