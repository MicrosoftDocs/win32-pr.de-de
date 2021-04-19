---
description: Beachten Sie beim Erstellen eines 64-Bit-Windows Installer Pakets die folgenden Richtlinien.
ms.assetid: e7dfd188-fd4d-49d6-8cf5-c17182b697ca
title: Verwenden von 64-Bit-Windows Installer Paketen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b46ab8a9668d816ea99bd92c2575e9ea6367352
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364069"
---
# <a name="using-64-bit-windows-installer-packages"></a>Verwenden von 64-Bit-Windows Installer Paketen

Wenn Sie [64-Bit-Windows Installer Pakete](64-bit-windows-installer-packages.md) oder Anwendungen erstellen, die Windows Installer zum Installieren von 64-Bit-Paketen aufruft, gehen Sie wie folgt vor:

-   Verwenden Sie ein Windows Installer-Datenbankschema von 200 oder höher. Geben Sie an, dass Version 2,0 die mindestens erforderliche Version des Installationsprogramms ist, das zum Installieren des Pakets erforderlich ist, indem Sie die [**Zusammenfassungs Eigenschaft der Seitenanzahl**](page-count-summary.md) auf die ganze Zahl 200 Frühere Windows Installer Versionen ablehnen versuchen, 64-Bit-Pakete zu installieren. Bei 64-Bit-Paketen auf der Arm64-Plattform muss das Windows Installer-Datenbankschema 500 oder höher sein.
-   Geben Sie in der Eigenschaft [**Vorlagen Zusammenfassung**](template-summary.md) des paketzusammenfassungs-Informations Stroms an, dass es sich um ein 64-Bit-Paket handelt Geben Sie "Intel64" in das Feld "Platform" der **Template Summary** -Eigenschaft ein, wenn das Paket auf einem Intel64-Prozessor ausgeführt werden soll. Geben Sie "x64" ein, wenn das Paket auf einem erweiterten 64-Bit-Prozessor ausgeführt werden soll. Geben Sie "Arm64" ein, wenn das Paket auf einem Arm64-Prozessor ausgeführt werden soll. Ein Paket kann nicht als Unterstützung sowohl für Intel64-als auch für x64-Plattformen gekennzeichnet werden. der Eigenschafts Wert der **Vorlagen Zusammenfassung** "Intel64, x64" ist ungültig Ein Paket kann nicht als Unterstützung für 32-Bit-und 64-Bit-Plattformen gekennzeichnet werden. die **Vorlagen Zusammenfassungs** -Eigenschaftswerte "Intel, x64" oder "Intel, Intel64" sind ungültig.
-   Identifizieren Sie jede 64-Bit-Komponente, indem Sie die **msidbComponentAttributes64bit** in der Spalte Attribute der [Komponenten](component-table.md) Tabelle festlegen.
-   Verwenden Sie optionale bedingte Anweisungen, die die Version des 64-Bit-Betriebssystems überprüfen, indem Sie auf die [**VersionNT64**](versionnt64.md) -Eigenschaft verweisen. Windows Installer legt diese Eigenschaft auf die 64-Bit-Windows-Version fest und verlässt VersionNT64 nicht definiert, wenn das Betriebssystem nicht 64-Bit-Windows ist. Weitere Informationen finden Sie unter [Verwenden von Eigenschaften in Bedingungs Anweisungen](using-properties-in-conditional-statements.md).
-   Verwenden Sie optionale bedingte Anweisungen, die die numerische Prozessor Ebene des Computers überprüfen, indem Sie auf die [**Intel64**](intel64.md) -Eigenschaft oder die [**Msix64**](msix64.md) -Eigenschaft verweisen. Die Windows Installer legt diese Eigenschaften auf die aktuelle numerische Prozessor Ebene des Computers fest und lässt die **Intel64** -Eigenschaft nicht definiert, wenn es sich nicht um einen Itanium-basierten Prozessor handelt. Weitere Informationen finden Sie unter [Verwenden von Eigenschaften in Bedingungs Anweisungen](using-properties-in-conditional-statements.md).
-   Mithilfe der [AppSearch-Tabelle](appsearch-table.md) und der [AppSearch-Aktion](appsearch-action.md) können Sie optionale Suchvorgänge für die Registrierung vorhandener 64-Bit-Komponenten ausführen. Wenn Sie nach vorhandenen 64-Bit-Komponenten suchen möchten, schließen Sie das **msidbLocatorType64bit** -Bit in die Typspalte der [reglocator-Tabelle](reglocator-table.md)ein. Weitere Informationen finden Sie unter [Suchen nach vorhandenen Anwendungen, Dateien, Registrierungs Einträgen oder INI-Datei Einträgen (Eigenschaft).](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md)
-   Rufen Sie die Pfade zu Systemordnern ab, indem Sie auf die [**System64Folder**](system64folder.md)-Eigenschaft, die [**ProgramFiles64Folder**](programfiles64folder.md) -Eigenschaft und die [**CommonFiles64Folder**](commonfiles64folder.md) -Eigenschaft für die 64-Bit-Ordner und die [**System Folder**](systemfolder.md) -Eigenschaft, die [**ProgramFilesFolder**](programfilesfolder.md) -Eigenschaft und die [**CommonFilesFolder**](commonfilesfolder.md) -Eigenschaft für die 32-Bit-Ordner verweisen.
-   Überprüfen Sie, ob die Anwendung die richtige GUID verwendet, wenn Sie auf eine 64-Bit-Komponente verweist. Wenn 32-Bit-und 64-Bit-Versionen einer bestimmten Komponente vorhanden sind, sollten diese über unterschiedliche Komponenten-ID-GUIDs verfügen.
-   Bestimmen Sie, ob bei der Installation von 64-Bit-Anwendungen neue Umgebungsvariablen definiert werden müssen.
-   Wenn ein 64-Bit-ODBC-Treiber-Manager installiert werden soll, sollte die Komponente, die Sie enthält, den Namen ODBCDriverManager64 haben. Der ODBC-Treiber-Manager muss im Installer-Paket erstellt werden, und es muss eine Komponente mit dem Namen ODBCDriverManager64 eingeschlossen werden. Der Manager wird bei Bedarf installiert.
-   Vergewissern Sie sich, dass die Anwendung nur 32-Bit-Dienste aufruft, die als ausführbare Dateien ausgeführt werden. Anwendungen sollten keine 32-Bit-Dienste, die in DLLs ausgeführt werden, abrufen.
-   Wenn die Anwendung vorhandene 32-Bit-und 64-Bit-Versionen einer Komponente installiert, vergewissern Sie sich, dass die Dateiinformationen der INI-Datei von der Anwendung ordnungsgemäß frei geleitet werden.
-   Vergewissern Sie sich, dass die Anwendung nur 32-Bit-Patches auf 32-Bit-Binärdateien und 64-Bit-Patches auf 64-Bit-Binärdateien anwendet.
-   Beachten Sie zukünftige Upgradeszenarien für 32-Bit-und 64-Bit-Versionen, und behalten Sie upgradecodes bei. Weitere Informationen finden Sie unter [Patching und Upgrades](patching-and-upgrades.md).
-   Wenn Sie eine [Bootstrapping](bootstrapping.md) -Anwendung zum Installieren eines [64-Bit-Windows Installer Pakets](64-bit-windows-installer-packages.md)verwenden, kompilieren Sie die Bootstrapping-Anwendung als eine 64-Bit-Anwendung.
-   Zum Deaktivieren der [Registrierungs Reflektion](../winprog64/registry-reflection.md) für Registrierungsschlüssel, die von einer bestimmten Komponente betroffen sind, legen Sie das **msidbcomponentattributesdisableregistryreflection** -Bit im Feld Attribute der [Komponenten](component-table.md) Tabelle fest. Dies kann erforderlich sein, damit 32-Bit-und 64-Bit-Kopien derselben Anwendung gleichzeitig vorhanden sind. Wenn dieses Bit festgelegt ist, ruft der Windows Installer die [**regdisablereflectionkey**](/windows/win32/api/winreg/nf-winreg-regdisablereflectionkey) -Funktion für jeden Schlüssel auf, auf den die Komponente zugreift. Dieses Bit ist in Windows Installer Version 4,0 verfügbar. Dieses Bit wird auf 32-Bit-Systemen ignoriert. Dieses Bit wird in den 64-Bit-Versionen von Windows XP und Windows 2000 ignoriert.

> [!Note]  
> Der Wert des numerischen Registrierungs Stamms, der vom *lppathbuf* -Parameter der [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha) -Funktion zurückgegeben wird, unterscheidet zwischen Komponenten auf 32-Bit-und 64-Bit-Betriebssystemen. Weitere Informationen finden Sie unter **MsiGetComponentPath** -Funktion.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[benutzerdefinierte 64-Bit-Aktionen](64-bit-custom-actions.md)
</dt> </dl>

 

 
