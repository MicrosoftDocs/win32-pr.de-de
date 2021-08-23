---
description: Im Folgenden wird beschrieben, wie Sie ein Windows Installer-Paket erstellen, um eine Win32-Assembly zu installieren.
ms.assetid: 1234e904-fc7f-4eb7-8c50-0c959bbf5261
title: Installieren von Win32-Assemblys für die side-by-side-Freigabe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c62607b37a9abd26ce031d922e67fa3f48963193af054e1d71c6903474220e82
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119500700"
---
# <a name="installing-win32-assemblies-for-side-by-side-sharing"></a>Installieren von Win32-Assemblys für die side-by-side-Freigabe

Im Folgenden wird beschrieben, wie Sie ein Windows Installer-Paket erstellen, um eine Win32-Assembly zu installieren. Das Paket installiert eine seiteseitige Assembly im Ordner Winsxs für die gemeinsame Verwendung der Anwendung. Nach der Installation des Pakets ist die freigegebene Assembly global für jede Anwendung verfügbar, die eine Abhängigkeit von der Assembly in einer Assemblymanifestdatei angibt. Das Installationsprogramm registriert die nebenseitige Assembly nicht global auf dem System.

Beachten Sie, dass Sie freigegebene, nebenseitige Assemblys mithilfe von [Mergemodulen installieren können.](merge-modules.md)

Bevor Sie fortfahren, sollten Sie verstehen, wie Sie ein Paket Windows Installer ohne Assemblys erstellen. Ein Beispiel zum Erstellen einer einfachen Installation finden Sie unter [An Installation Example](an-installation-example.md).

**So installieren Sie eine freigegebene Assembly nebeneinander**

1.  Definieren Sie eine Windows Installer-Komponente, die die Win32-Assembly enthält. Diese Komponente kann andere Ressourcen enthalten, die immer mit der Assembly installiert oder entfernt werden sollten. Alle anderen Komponenten der Anwendung können genau wie bei einer Installation ohne Assemblys entwickelt werden. Fügen Sie der [Component-Tabelle für die Komponente, die](component-table.md) die Win32-Assembly enthält, eine Zeile hinzu. Geben Sie eine gültige Windows [Installer-GUID](guid.md) für diesen Komponentencode ein. Verwenden Sie die Manifestdatei nicht als Schlüsselpfad für diese Komponente.
2.  Fügen Sie der [Tabelle FeatureComponents](featurecomponents-table.md) eine Zeile hinzu, die die Komponente an Windows Installer-Feature binden. Weitere Informationen finden Sie unter [Komponenten und Features.](components-and-features.md) Ein Windows-Installer sollte ein Teil der Funktionalität der Anwendung sein, der für einen Benutzer erkennbar ist. Die Assembly wird aktiviert, wenn diese Funktion von einem Benutzer ausgewählt oder von einer Anwendung fehlerhaft ist. Wenn die Assembly ein zusätzliches Feature definiert, fügen Sie der [Featuretabelle](feature-table.md) eine zusätzliche Zeile für die Attribute des Features hinzu. Dieser Schritt ist beim Erstellen eines Mergemoduls nicht erforderlich.
3.  Bei assemblyseitigen Assemblys werden Bindungs- und Aktivierungsinformationen wie COM-Klassen, Schnittstellen und Typbibliotheken nicht in der Registrierung, sondern in Manifestdateien gespeichert. Freigegebene Assemblys speichern diese Informationen in einem Assemblymanifest. Auf Systemen, die side-by-side-Assemblys unterstützen, überspringt das Installationsprogramm die Verarbeitung von Informationen zur Komponente, die in der Erweiterungstabelle [,](extension-table.md) [verb table](verb-table.md), [TypeLib table](typelib-table.md), MIME [table](mime-table.md), [Class table,](class-table.md) [ProgId table](progid-table.md)und [AppId](appid-table.md)table eingegeben wurden. Bindungs- und Aktivierungsinformationen können in diese Tabellen eingegeben werden, um sie von Systemen zu verwenden, die die gemeinsame Nutzung von Assemblys nicht unterstützen.
4.  Bei der side-by-side-Installation wird die Assembly nicht global registriert. Das Installationsprogramm überspringt die Selbstregistrierung der Komponente, wenn Selbstregistrierungsinformationen in die [SelfReg-Tabelle eingegeben wurden.](selfreg-table.md) Informationen zur Selbstregistrierung können in die SelfReg-Tabelle eingegeben werden, um die Komponente selbst auf Systemen zu registrieren, die die gemeinsame Nutzung von Assemblys nicht unterstützen.
5.  Fügen Sie der Registrierungstabelle, der [RemoveRegistry-Tabelle](removeregistry-table.md)und der [](registry-table.md)Umgebungstabelle alle anderen Registrierungsinformationen hinzu, die keine Bindung und Aktivierung oder Selbstregistrierung [der Komponente enthalten.](environment-table.md)
6.  Da es sich um eine freigegebene Assembly handelt, generieren Sie keine LOKALE Datei. Schließen Sie keine Informationen für diese Komponente in die [IsolatedComponent-Tabelle ein.](isolatedcomponent-table.md) Das Installationsprogramm überspringt die Tabelle IsolatedComponent für diese Komponente auf Betriebssystemen, die die gemeinsame Nutzung unterstützen. Fügen Sie der Tabelle IsolatedComponent Informationen hinzu, wenn die Assembly auf Systemen, die LOKALE Dateien unterstützen, privat sein soll.
7.  Um die side-by-side-Freigabe zu aktivieren, muss die Win32-Assembly im Ordner Winsxs installiert sein. Dies wird erreicht, indem die Spalte \_ Dateianwendung der [MsiAssembly-Tabelle](msiassembly-table.md) für die Assembly NULL belässt. Dies weist das Installationsprogramm an, die Assembly im Ordner WinSxS statt im Ordner der Komponente zu installieren. Fügen Sie der [MsiAssembly-Tabelle](msiassembly-table.md) für die Komponente, die die Win32-Assembly enthält, eine Zeile hinzu. Geben Sie im Feld Attribute der Tabelle MsiAssembly den Wert 1 ein, um anzugeben, dass es sich um eine Win32-Assembly handelt. Lassen Sie für eine freigegebene Assembly das Feld \_ Dateianwendung leer. Fügen Sie der Tabelle [InstallExecuteSequence](installexecutesequence-table.md) oder der [Tabelle AdvtExecuteSequence](advtexecutesequence-table.md)die Aktion [MsiPublishAssemblies](msipublishassemblies-action.md) hinzu. Fügen Sie der Tabelle InstallExecuteSequence die Aktion [MsiUnpublishAssemblies](msiunpublishassemblies-action.md) hinzu.
8.  Fügen Sie der [MsiAssemblyName-Tabelle für die](msiassemblyname-table.md) Komponente Zeilen hinzu. Fügen Sie eine Zeile für jedes Name-Wert-Paar hinzu, das im Abschnitt assemblyIdentity des Manifests angegeben ist. Ein Beispiel finden Sie unter [MsiAssemblyName-Tabelle](msiassemblyname-table.md).

 

 



