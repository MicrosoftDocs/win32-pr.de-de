---
description: Wenn Sie Ihre eigenen parallelen Assemblys erstellen, befolgen Sie die Richtlinien zum Erstellen paralleler Assemblys und zum Erstellen einer beliebigen DLL-Datei, die in der Assembly enthalten sein soll, gemäß den Richtlinien zum Erstellen einer DLL für eine parallele Assembly.
ms.assetid: 0e98bbcd-7e23-4a33-b0fa-1f936d0ef96b
title: Erstellen von Zustands Speicher für parallele Assemblys
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eee388cf680ee3a186a225ca7e3bde8b6eae625d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757309"
---
# <a name="authoring-state-storage-for-side-by-side-assemblies"></a>Erstellen von Zustands Speicher für parallele Assemblys

Wenn Sie Ihre eigenen parallelen Assemblys erstellen, befolgen Sie die [Richtlinien zum Erstellen](guidelines-for-creating-side-by-side-assemblies.md) paralleler Assemblys und zum Erstellen einer beliebigen DLL-Datei, die in der Assembly enthalten sein soll, gemäß den Richtlinien zum Erstellen [einer DLL für eine parallele Assembly](authoring-a-dll-for-a-side-by-side-assembly.md).

Befolgen Sie die folgenden Richtlinien für die Speicherung des Zustands:

-   Entwerfen Sie den Zustands Speicher, um vorwärts und abwärts kompatibel zu sein. Erwarten Sie, dass die Versionen in beliebiger Reihenfolge verwendet werden: z. b. v1, v3 und v2.
-   Initialisieren Sie die Standardeinstellungen für die Assembly im Assemblycode, und legen Sie Sie fest. Speichern Sie die Standardeinstellungen nicht in der Registrierung.
-   Registrierungs Einstellungen müssen auf einzelner Versions Basis geschrieben werden, um mehrere Assemblyversionen zu isolieren, die gleichzeitig ausgeführt werden können. Entwerfen Sie die parallele Assembly so, dass Sie den Status der Assembly bei parallelen Freigabe Szenarien ordnungsgemäß speichert und verarbeitet.
-   Assemblys speichern normalerweise Zustandsinformationen in Registrierungs Schlüsseln. Erstellen Sie einen Satz von Header Dateien und Hilfsfunktionen, um eine einfache Möglichkeit zur Versions Angabe von Registrierungs Schlüsseln mit dem assemblystatus zu bieten.
-   Alle assemblystatusinformationen, die in der Registrierung gespeichert sind, müssen von anderen Versionen der Assembly isoliert werden. Die in der Registrierung gespeicherten Zustands Einstellungen müssen in den einzelnen Versions Abschnitten der Registrierung gespeichert werden. Dies ist sowohl für die HKLM-als auch für HKCU-Teile der Registrierung erforderlich. Speichern Sie z. b. HKCU-Zustands Einstellungen für Assemblyversion xxxx unter dem folgenden Registrierungsschlüssel:

    **HKCU** \\ **MyCompany** \\ **MeineKomponente** \\ **Versionxxxx**

-   Alle Zustandsinformationen, die von freigegebenen Assemblys in der Registrierung gespeichert werden, müssen in den einzelnen Versions Abschnitten der Registrierung gespeichert werden. Beispielsweise kann eine Zustands Einstellung namens enablesupercoolfeature den Wert **true** oder **false** aufweisen. Speichern Sie den Wert für eine frei [*gegebene parallele Assembly*](s-sbscs-gly.md) wie folgt:

    **HKEY \_ CurrentUser** \\ **Software** \\ **MyCompany** \\ **meinekomponentenversion** \\ **01.01** \\ **enablesupercoolfeature = true**

-   Alle Zustandsinformationen, die von privaten Assemblys in der Registrierung gespeichert werden, müssen in den einzelnen Anwendungs Abschnitten der Registrierung gespeichert werden. Dadurch werden die Zustands Einstellungen der Assembly auf die Anwendung isoliert. Sie können die [**GetModuleFileName**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulefilenamea) -Funktion verwenden, um ein virtuelles Stammverzeichnis einzurichten. Wenn die Assemblyversion XXYY z. b. ein private Assembly von "someapplication" ist, gibt ein **GetModuleFileName** -Rückruf "someapplication" zurück, und alle Einstellungen des privaten Zustands für die Assembly sollten unter folgendem Schlüssel geschrieben werden:

    **HKCU** \\ **MyCompany** \\ **MeineKomponente** \\ **Versionxxyy** \\ **Somedanwendung**

-   Legen Sie die Einstellungen für den freigegebenen Zustand in der Registrierung privat für den assemblykontext, der ausführt Sie können die [**GetModuleFileName**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulefilenamea) -Funktion verwenden, um ein virtuelles Stammverzeichnis einzurichten. Dies sollte für HKLM-und HKCU-branches erfolgen.
-   Im Idealfall sollten Sie ein Persistenzmodell übernehmen, in dem die Anwendung den Status beibehält und die Registrierung nicht ändert. Eine Anwendung sollte die Registrierungseinträge der Komponente nicht direkt berühren müssen. Stattdessen sollte die Assembly API-Funktionen bieten, die nebeneinander kompatible Einstellungen speichern oder wiederherstellen.
-   Assemblys können Zustands Einstellungen in Geschäften außerhalb der Registrierung speichern, damit die Assembly mit dem globalen Zustand interagieren kann. Parallele Assemblys können die folgenden Seite-an-Seite-kompatiblen Speicher verwenden:
    -   Ein geschützter Speicher (*pstore*)
    -   Ein WinInet-Cache
    -   Eine Microsoft SQL Server

 

 
