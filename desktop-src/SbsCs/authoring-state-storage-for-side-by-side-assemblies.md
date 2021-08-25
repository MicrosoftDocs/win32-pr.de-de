---
description: Wenn Sie ihre eigenen parallelen Assemblys erstellen, befolgen Sie die Richtlinien zum Erstellen paralleler Assemblys, und erstellen Sie jede DLL, die gemäß den Richtlinien unter Erstellen einer DLL für eine parallele Assembly in die Assembly aufgenommen werden soll.
ms.assetid: 0e98bbcd-7e23-4a33-b0fa-1f936d0ef96b
title: Erstellungsstatus Storage für nebenseitige Assemblys
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91dd3b3dc62726c45a03fd388864faa7f359112687f0c03fb133276eef2280ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119885520"
---
# <a name="authoring-state-storage-for-side-by-side-assemblies"></a>Erstellungsstatus Storage für nebenseitige Assemblys

Befolgen Sie beim Erstellen ihrer eigenen parallelen Assemblys die Richtlinien zum Erstellen paralleler [Assemblys,](guidelines-for-creating-side-by-side-assemblies.md) und erstellen Sie jede DLL, die gemäß den Richtlinien unter [Erstellen einer DLL für eine parallele Assembly](authoring-a-dll-for-a-side-by-side-assembly.md)in die Assembly aufgenommen werden soll.

Befolgen Sie die folgenden Richtlinien für die Speicherung des Zustands:

-   Entwerfen Sie Zustandsspeicher als vorwärts- und abwärtskompatibel. Erwarten Sie, dass die Versionen in beliebiger Reihenfolge verwendet werden: z. B. v1, dann v3 und v2.
-   Initialisieren sie die Standardeinstellungen für die Assembly im Assemblycode, und legen Sie sie fest. Speichern Sie die Standardeinstellungen nicht in der Registrierung.
-   Registrierungseinstellungen müssen auf Einzelversionsbasis geschrieben werden, um mehrere Assemblyversionen zu isolieren, die gleichzeitig ausgeführt werden können. Entwerfen Sie ihre side-by-side-Assembly so, dass sie den Zustand der Assembly in Szenarien mit der side-by-side-Freigabe ordnungsgemäß speichert und behandelt.
-   Assemblys speichern in der Regel Zustandsinformationen in Registrierungsschlüsseln. Erstellen Sie eine Reihe von Headerdateien und Hilfsfunktionen, um eine einfache Möglichkeit zur Versionsversion von Registrierungsschlüsseln zu bieten, die den Assemblyzustand enthalten.
-   Alle in der Registrierung gespeicherten Assemblyzustandsinformationen müssen von anderen Versionen der Assembly isoliert werden. In der Registrierung gespeicherte Zustandseinstellungen müssen in einzelnen Versionsabschnitten der Registrierung gespeichert werden. Dies ist sowohl im HKLM- als auch im HKCU-Teil der Registrierung erforderlich. Speichern Sie beispielsweise HKCU-Statuseinstellungen für assembly version XXXX unter dem folgenden Registrierungsschlüssel:

    **HKCU** \\ **MyCompany** \\ **MyComponent** \\ **VersionXXXX**

-   Alle Zustandsinformationen, die von freigegebenen Assemblys in der Registrierung gespeichert werden, müssen in einzelnen Versionsabschnitten der Registrierung gespeichert werden. Beispielsweise kann eine Zustandseinstellung namens EnableSuperFeature den Wert **TRUE** oder **FALSE aufweisen.** Store den Wert für eine [*freigegebene side-by-side-Assembly*](s-sbscs-gly.md) wie folgt aus:

    **HKEY \_ CurrentUser** \\ **Software** \\ **MyCompany** \\ **MyComponent** \\ **Version01.01** \\ **EnableSuperStringFeature = TRUE**

-   Alle Zustandsinformationen, die von privaten Assemblys in der Registrierung gespeichert werden, müssen in einzelnen Anwendungsabschnitten der Registrierung gespeichert werden. Dadurch werden die Zustandseinstellungen der Assembly von der Anwendung isoliert. Sie können die [**GetModuleFileName-Funktion**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulefilenamea) verwenden, um einen virtuellen Stamm einzurichten. Wenn die Assemblyversion XXYY beispielsweise eine private Assembly von "SomeApplication" ist, gibt ein Aufruf von **GetModuleFileName** "SomeApplication" zurück, und alle Einstellungen für den privaten Zustand der Assembly sollten unter dem folgenden Schlüssel geschrieben werden:

    **HKCU** \\ **MyCompany** \\ **MyComponent** \\ **VersionXXYY** \\ **SomeApplication**

-   Machen Sie freigegebene Zustandseinstellungen, die in der Registrierung gespeichert sind, für den assemblykontext, der ausgeführt wird, privat. Sie können die [**GetModuleFileName-Funktion**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulefilenamea) verwenden, um einen virtuellen Stamm einzurichten. Dies sollte für HKLM- und HKCU-Branches erfolgen.
-   Im Idealfall sollten Sie ein Persistenzmodell übernehmen, in dem die Anwendung den Zustand beibehält und die Registrierung nicht ändert. Eine Anwendung sollte die Registrierungseinträge der Komponente nicht direkt berühren müssen. Stattdessen sollte die Assembly API-Funktionen bereitstellen, die einstellungen speichern oder wiederherstellen, die nebeneinander kompatibel sind.
-   Assemblys können Zustandseinstellungen in Speichern außerhalb der Registrierung speichern, damit die Assembly mit dem globalen Zustand interagieren kann. Nebenassemblys können die folgenden nebeneinander kompatiblen Speicher verwenden:
    -   Ein geschützter Speicher (*pstore*)
    -   Ein WinInet-Cache
    -   Ein Microsoft SQL Server

 

 
