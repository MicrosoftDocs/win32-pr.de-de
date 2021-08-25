---
description: Befolgen Sie beim Erstellen eines 64-Bit-Windows Installer-Pakets die folgenden Richtlinien.
ms.assetid: e7dfd188-fd4d-49d6-8cf5-c17182b697ca
title: Verwenden von 64-Bit-Windows-Installerpaketen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9c3bca5c666f7a6a0f1757efca40a26b1406d4241abf7d32a066c2d7fa01b92
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119809090"
---
# <a name="using-64-bit-windows-installer-packages"></a>Verwenden von 64-Bit-Windows-Installerpaketen

Wenn Sie [64-Bit-Windows Installerpakete](64-bit-windows-installer-packages.md) oder Anwendungen erstellen, die Windows Installer aufrufen, um 64-Bit-Pakete zu installieren, gehen Sie folgendermaßen vor:

-   Verwenden Sie ein Windows Installer-Datenbankschema von 200 oder höher. Geben Sie an, dass Version 2.0 die Mindestversion des Installationsprogramms ist, die zum Installieren des Pakets erforderlich ist, indem Sie die Page [**Count Summary-Eigenschaft**](page-count-summary.md) auf die ganze Zahl 200 festlegen. Frühere Windows Installer-Versionen lehnen Versuche ab, 64-Bit-Pakete zu installieren. Für 64-Bit-Pakete auf der Arm64-Plattform muss das Windows Installer-Datenbankschema 500 oder höher sein.
-   Geben Sie in der [**Eigenschaft Vorlagenzusammenfassung**](template-summary.md) des Paketzusammenfassungs-Informationsstreams an, dass es sich um ein 64-Bit-Paket handelt. Geben Sie "Intel64" in das Feld Plattform der **Eigenschaft Vorlagenzusammenfassung** ein, wenn das Paket auf einem Intel64-Prozessor ausgeführt werden soll. Geben Sie "x64" ein, wenn das Paket auf einem erweiterten 64-Bit-Prozessor ausgeführt werden soll. Geben Sie "Arm64" ein, wenn das Paket auf einem Arm64-Prozessor ausgeführt werden soll. Ein Paket kann nicht als unterstützend für Intel64- und x64-Plattformen markiert werden. Der Eigenschaftswert **"Template Summary"** von "Intel64,x64" ist ungültig. Ein Paket kann nicht als Unterstützung für 32-Bit- und 64-Bit-Plattformen markiert werden. Die Eigenschaftswerte der **Vorlagenzusammenfassung** von "Intel,x64" oder "Intel,Intel64" sind ungültig.
-   Identifizieren Sie jede 64-Bit-Komponente, indem Sie **msidbComponentAttributes64bit** in der Attributes -Spalte der [Component-Tabelle](component-table.md) festlegen.
-   Verwenden Sie optionale bedingte Anweisungen, die die Version des 64-Bit-Betriebssystems überprüfen, indem Sie auf die [**VersionNT64-Eigenschaft**](versionnt64.md) verweisen. Windows Das Installationsprogramm legt diese Eigenschaft auf die 64-Bit-Windows-Version fest und lässt VersionNT64 undefiniert, wenn das Betriebssystem nicht 64-Bit-Windows ist. Weitere Informationen finden Sie unter [Verwenden von Eigenschaften in bedingten Anweisungen.](using-properties-in-conditional-statements.md)
-   Verwenden Sie optionale bedingte Anweisungen, die die numerische Prozessorebene des Computers überprüfen, indem Sie auf die [**Intel64-**](intel64.md) oder [**Msix64-Eigenschaft**](msix64.md) verweisen. Der Windows Installer legt diese Eigenschaften auf die aktuelle numerische Prozessorebene des Computers fest und lässt die **Intel64-Eigenschaft** nicht definiert, wenn es sich nicht um einen Itanium-basierten Prozessor handelt. Weitere Informationen finden Sie unter [Verwenden von Eigenschaften in bedingten Anweisungen.](using-properties-in-conditional-statements.md)
-   Verwenden Sie die [AppSearch-Tabelle](appsearch-table.md) und die [AppSearch-Aktion,](appsearch-action.md) um optionale Suchvorgänge in der Registrierung für vorhandene 64-Bit-Komponenten durchzuführen. Um nach vorhandenen 64-Bit-Komponenten zu suchen, schließen Sie das **msidbLocatorType64bit-Bit** in die Type-Spalte der [RegLocator-Tabelle ein.](reglocator-table.md) Weitere Informationen finden Sie unter [Suchen nach vorhandenen Anwendungen, Dateien, Registrierungseinträgen oder .ini-Eigenschaft "Dateieinträge".](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md)
-   Rufen Sie die Pfade zu Systemordnern ab, indem Sie für die 64-Bit-Ordner auf die [**System64Folder-Eigenschaft,**](system64folder.md)die [**ProgramFiles64Folder-Eigenschaft**](programfiles64folder.md) und die [**CommonFiles64Folder-Eigenschaft**](commonfiles64folder.md) sowie auf die [**SystemFolder-Eigenschaft,**](systemfolder.md) [**die ProgramFilesFolder-Eigenschaft**](programfilesfolder.md) und die [**CommonFilesFolder-Eigenschaft**](commonfilesfolder.md) für die 32-Bit-Ordner verweisen.
-   Vergewissern Sie sich, dass die Anwendung beim Verweisen auf eine 64-Bit-Komponente die richtige GUID verwendet. Wenn es 32-Bit- und 64-Bit-Versionen einer bestimmten Komponente gibt, sollten diese unterschiedliche Komponenten-ID-GUIDs aufweisen.
-   Bestimmen Sie, ob beim Installieren von 64-Bit-Anwendungen neue Umgebungsvariablen definiert werden müssen.
-   Wenn ein 64-Bit-ODBC-Treiber-Manager installiert werden soll, sollte die Komponente mit dem Namen ODBCDriverManager64 benannt werden. Der ODBC-Treiber-Manager muss im Installationspaket erstellt werden, und eine Komponente namens ODBCDriverManager64 muss enthalten sein. Der Manager wird bei Bedarf installiert.
-   Stellen Sie sicher, dass die Anwendung nur 32-Bit-Dienste aufruft, die als ausführbare Dateien ausgeführt werden. Anwendungen sollten keine 32-Bit-Dienste aufrufen, die in DLLs ausgeführt werden.
-   Wenn die Anwendung parallel vorhandene 32-Bit- und 64-Bit-Versionen einer Komponente installiert, überprüfen Sie, ob die Anwendung .ini Dateiinformationen ordnungsgemäß gemeinsam nutzt.
-   Stellen Sie sicher, dass die Anwendung nur 32-Bit-Patches auf 32-Bit-Binärdateien und 64-Bit-Patches auf 64-Bit-Binärdateien anwendet.
-   Berücksichtigen Sie zukünftige Upgradeszenarien für 32-Bit- und 64-Bit-Versionen, und verwalten Sie Upgradecodes. Weitere Informationen finden Sie unter [Patchen und Upgrades.](patching-and-upgrades.md)
-   Wenn Sie eine [Bootstrappinganwendung](bootstrapping.md) zum Installieren eines [64-Bit-Windows Installer-Pakets](64-bit-windows-installer-packages.md)verwenden, kompilieren Sie die Bootstrappinganwendung als 64-Bit-Anwendung.
-   Um [die Registrierungsreflektion](../winprog64/registry-reflection.md) für Registrierungsschlüssel zu deaktivieren, die von einer bestimmten Komponente betroffen sind, legen Sie das Bit **msidbComponentAttributesDisableRegistryReflection** im Feld Attributes der [Tabelle Component](component-table.md) fest. Dies kann erforderlich sein, damit 32-Bit- und 64-Bit-Kopien derselben Anwendung gleichzeitig vorhanden sind. Wenn dieses Bit festgelegt ist, ruft der Windows Installer die [**RegDisableReflectionKey-Funktion**](/windows/win32/api/winreg/nf-winreg-regdisablereflectionkey) für jeden Schlüssel auf, auf den von der Komponente zugegriffen wird. Dieses Bit ist mit Windows Installer Version 4.0 verfügbar. Dieses Bit wird auf 32-Bit-Systemen ignoriert. Dieses Bit wird in den 64-Bit-Versionen von Windows XP und Windows 2000 ignoriert.

> [!Note]  
> Der Wert des numerischen Registrierungsstamms, der vom *lpPathBuf-Parameter* der [**MsiGetComponentPath-Funktion**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha) zurückgegeben wird, unterscheidet zwischen Komponenten unter 32-Bit- und 64-Bit-Betriebssystemen. Weitere Informationen finden Sie unter **MsiGetComponentPath-Funktion.**

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Benutzerdefinierte 64-Bit-Aktionen](64-bit-custom-actions.md)
</dt> </dl>

 

 
