---
description: Im folgenden wird beschrieben, wie ein Windows Installer Paket erstellt wird, um eine Win32-Assembly zu installieren.
ms.assetid: 1234e904-fc7f-4eb7-8c50-0c959bbf5261
title: Installieren von Win32-Assemblys für die parallele Freigabe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea72c9bcb7bd85ac38dfc8857030d6b9d6afbf23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359510"
---
# <a name="installing-win32-assemblies-for-side-by-side-sharing"></a>Installieren von Win32-Assemblys für die parallele Freigabe

Im folgenden wird beschrieben, wie ein Windows Installer Paket erstellt wird, um eine Win32-Assembly zu installieren. Das Paket installiert eine parallele Assembly im WinSxS-Ordner für die gemeinsame Verwendung der Anwendung. Nach der Installation des Pakets ist die freigegebene Assembly für jede Anwendung global verfügbar, die eine Abhängigkeit von der Assembly in einer Assemblymanifest-Datei angibt. Der Installer registriert die parallele Assembly nicht global auf dem System.

Beachten Sie, dass Sie freigegebene parallele Assemblys mit [Mergemodulen](merge-modules.md)installieren können.

Bevor Sie fortfahren, sollten Sie wissen, wie ein Windows Installer Paket ohne Assemblys erstellt wird. Ein Beispiel für das Erstellen einer einfachen Installation finden Sie unter [einem Installations Beispiel](an-installation-example.md).

**So installieren Sie eine freigegebene Assembly nebeneinander**

1.  Definieren Sie eine Windows Installer Komponente, die die Win32-Assembly enthält. Diese Komponente kann andere Ressourcen enthalten, die immer mit der Assembly installiert oder entfernt werden sollten. Alle anderen Komponenten der Anwendung können genauso wie für eine Installation ohne Assemblys erstellt werden. Fügen Sie der [Komponenten Tabelle](component-table.md) eine Zeile für die Komponente hinzu, die die Win32-Assembly enthält. Geben Sie eine gültige Windows Installer [GUID](guid.md) für den Komponenten Code ein. Verwenden Sie die Manifest-Datei nicht als Schlüssel Pfad für diese Komponente.
2.  Fügen Sie der [FeatureComponents-Tabelle](featurecomponents-table.md) eine Zeile hinzu, die die Komponente an eine Windows Installer Funktion bindet. Weitere Informationen finden Sie unter [Komponenten und Features](components-and-features.md). Eine Windows Installer Funktion sollte ein Teil der Anwendungs Funktionalität sein, die für einen Benutzer erkennbar ist. Die Assembly wird aktiviert, wenn dieses Feature von einem Benutzer ausgewählt oder von einer Anwendung als fehlerhaft gekennzeichnet wird. Wenn die Assembly ein zusätzliches Feature definiert, fügen Sie der [Featuretabelle](feature-table.md) für die Attribute der Funktion eine zusätzliche Zeile hinzu. Dieser Schritt wird bei der Erstellung eines Mergemoduls nicht benötigt.
3.  Bei parallelen Assemblys werden Bindungs-und Aktivierungs Informationen, wie z. b. com-Klassen, Schnittstellen und Typbibliotheken, in Manifest-Dateien und nicht in der Registrierung gespeichert. Freigegebene Assemblys speichern diese Informationen in einem Assemblymanifest. Auf Systemen, die parallele Assemblys unterstützen, überspringt das Installationsprogramm die Verarbeitung aller Informationen über die in der [Erweiterungs Tabelle](extension-table.md), [Verb Tabelle](verb-table.md), [typelib](typelib-table.md)-Tabelle, [MIME-Tabelle](mime-table.md), [Klassen Tabelle](class-table.md), [ProgID](progid-table.md)-Tabelle und [AppID](appid-table.md)-Tabelle eingegebene Komponente. Bindungs-und Aktivierungs Informationen können in diese Tabellen eingegeben werden, damit Sie von Systemen verwendet werden können, die die parallele assemblyfreigabe nicht unterstützen.
4.  Bei der parallelen Installation wird die Assembly nicht global registriert. das Installationsprogramm überspringt die Selbstregistrierung der Komponente, wenn in der [Tabelle "selfreg](selfreg-table.md)" Informationen zur Selbstregistrierung eingegeben wurden. Informationen zur Selbstregistrierung können in der Tabelle "selfreg" zur Selbstregistrierung der Komponente in Systemen eingegeben werden, die die parallele assemblyfreigabe nicht unterstützen.
5.  Fügen Sie der [Registrierungs Tabelle](registry-table.md), der [removeregistry-Tabelle](removeregistry-table.md)und der [Umgebungs Tabelle](environment-table.md)alle weiteren Registrierungsinformationen hinzu, die exklusiv für die Bindung und Aktivierung oder die Selbstregistrierung der Komponente sind.
6.  Da es sich hierbei um eine freigegebene Assembly handelt, wird keine lokale Datei generiert. Fügen Sie keine Informationen für diese Komponente in die [isolatedcomponent-Tabelle](isolatedcomponent-table.md)ein. Das Installationsprogramm überspringt die isolatedcomponent-Tabelle für diese Komponente auf Betriebssystemen, die die parallele Freigabe unterstützen. Fügen Sie der isolatedcomponent-Tabelle Informationen hinzu, wenn die Assembly auf Systemen, die lokale Dateien unterstützen, privat sein soll.
7.  Um die parallele Freigabe zu aktivieren, muss die Win32-Assembly im Ordner WinSxS installiert werden. Dies wird erreicht, indem die Datei \_ Anwendungs Spalte der [MsiAssembly-Tabelle](msiassembly-table.md) für die Assembly auf Null belassen wird. Dadurch wird dem Installer mitgeteilt, dass die Assembly im Ordner WinSxS anstelle des-Ordners der Komponente installiert wird. Fügen Sie der [MsiAssembly-Tabelle](msiassembly-table.md) eine Zeile für die Komponente hinzu, die die Win32-Assembly enthält. Geben Sie im Feld Attribute der Tabelle MsiAssembly den Wert 1 ein, um anzugeben, dass es sich hierbei um eine Win32-Assembly handelt. Lassen Sie das Feld Datei Anwendung bei einer freigegebenen Assembly \_ leer. Fügen Sie die [msipublishassemblyaktion](msipublishassemblies-action.md) der [InstallExecuteSequence-Tabelle](installexecutesequence-table.md) oder der [AdvtExecuteSequence-Tabelle](advtexecutesequence-table.md)hinzu. Fügen Sie die [msiunpublishassemblyaktion](msiunpublishassemblies-action.md) der InstallExecuteSequence-Tabelle hinzu.
8.  Fügen Sie der [MsiAssemblyName-Tabelle](msiassemblyname-table.md) Zeilen für die Komponente hinzu. Fügen Sie für jedes im Abschnitt assemblyIdentity des Manifests angegebene Name-Wert-Paar eine Zeile hinzu. Ein Beispiel finden Sie unter [MsiAssemblyName Table](msiassemblyname-table.md).

 

 



