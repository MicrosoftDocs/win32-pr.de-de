---
description: Mit dem Verfahren in diesem Thema wird beschrieben, wie Sie ein Windows Installer-Paket erstellen, um eine Win32-Assembly zu installieren.
ms.assetid: 2d4bc2be-cce6-45e6-b6a7-7ff96d28eb96
title: Installieren von Win32-Assemblys für die private Verwendung einer Anwendung auf Windows XP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f478bddeb04ca9112610bd88338437002082204cc62078bde200539a8a18b6bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119893810"
---
# <a name="installing-win32-assemblies-for-the-private-use-of-an-application-on-windows-xp"></a>Installieren von Win32-Assemblys für die private Verwendung einer Anwendung auf Windows XP

Mit dem Verfahren in diesem Thema wird beschrieben, wie Sie ein Windows Installer-Paket erstellen, um eine Win32-Assembly zu installieren. Das Paket installiert die Assembly und eine Anwendungsmanifestdatei in einem von der Anwendung verwendeten erstellten Ordner. Das Anwendungsmanifest gibt die Abhängigkeit der Anwendung von der privaten Assembly an. Nach der Installation des Pakets ist die private Assembly für die exklusive Verwendung der Anwendung verfügbar. Die im Anwendungsmanifest angegebene Assemblyabhängigkeit überschreibt (für diese Anwendung) alle anderen globalen Assemblyabhängigkeiten, die in Assemblymanifestdateien angegeben sind.

Bevor Sie fortfahren, ist es eine gute Idee zu verstehen, wie Sie ein Windows Installer-Paket ohne Assemblys erstellen. Weitere Informationen finden Sie unter [Ein Installationsbeispiel.](an-installation-example.md)

**So installieren Sie eine private Assembly auf Windows XP**

1.  Definieren Sie eine Windows Installer-Komponente, die die Win32-Assembly und die Anwendungsmanifestdatei enthält. Diese Komponente kann andere Ressourcen enthalten, die immer mit der Assembly installiert oder entfernt werden sollten. In den verbleibenden Schritten dieses Verfahrens wird beschrieben, wie die Installationsdatenbank für die Installation dieser Komponente erstellt wird.
2.  Fügen Sie der [Tabelle Komponente](component-table.md) eine Zeile für die Komponente hinzu, die die Win32-Assembly und die Anwendungsmanifestdatei enthält. Geben Sie eine gültige Windows [Installer-GUID](guid.md) für diesen Komponentencode ein. Weitere Informationen finden Sie unter [Ändern des Komponentencodes](changing-the-component-code.md) und [Was geschieht, wenn die Komponentenregeln verletzt werden?](what-happens-if-the-component-rules-are-broken.md)
3.  Das Installationsprogramm kopiert die Assemblymanifestdatei in den Ordner, der die im \_ Feld Dateianwendung der [MsiAssembly-Tabelle](msiassembly-table.md)angegebene Datei enthält.
4.  Fügen Sie der [Tabelle FeatureComponents](featurecomponents-table.md) eine Zeile hinzu, die die Komponente an ein Windows Installer-Feature bindet. Weitere Informationen finden Sie unter [Komponenten und Features.](components-and-features.md) Ein Windows Installer-Feature sollte ein Teil der Anwendungsfunktionen sein, die ein Benutzer erkennen kann. Die Assembly wird aktiviert, wenn dieses Feature von einem Benutzer ausgewählt oder von einer Anwendung fehlerhaft ist. Wenn die Assembly ein zusätzliches Feature definiert, fügen Sie der [Tabelle Feature](feature-table.md) für die Featureattribute eine zusätzliche Zeile hinzu. Dieser Schritt ist beim Erstellen eines Mergemoduls nicht erforderlich.
5.  Für parallele Assemblys werden Bindungs- und Aktivierungsinformationen, z. B. COM-Klassen, Schnittstellen und Typbibliotheken, nicht in der Registrierung, sondern in Manifestdateien gespeichert. Private Assemblys speichern diese Informationen in einem Assemblymanifest. Auf Systemen, die parallele Assemblys unterstützen, überspringt das Installationsprogramm die Verarbeitung sämtlicher Informationen über die Komponente, die in die [Erweiterungstabelle](extension-table.md), [Verbtabelle,](verb-table.md) [TypeLib-Tabelle,](typelib-table.md) [MIME-Tabelle,](mime-table.md) [Klassentabelle,](class-table.md) [ProgId-Tabelle](progid-table.md)und [AppId-Tabelle](appid-table.md)eingegeben wird. Bindungs- und Aktivierungsinformationen können in die Tabellen eingegeben werden, damit sie von Systemen verwendet werden können, die die gemeinsame Nutzung von Assemblys nicht unterstützen.
6.  Bei der installation von Seite an Seite wird die Assembly nicht global registriert. Das Installationsprogramm überspringt die Selbstregistrierung der Komponente, wenn in der [SelfReg-Tabelle](selfreg-table.md)Selbstregistrierungsinformationen eingegeben werden. Informationen zur Selbstregistrierung können in die SelfReg-Tabelle für die Selbstregistrierung der Komponente auf Systemen eingegeben werden, die keine seiteseitige Assemblyfreigabe unterstützen.
7.  Fügen Sie der [Registrierungstabelle,](registry-table.md)der [RemoveRegistry-Tabelle](removeregistry-table.md)und der [Umgebungstabelle](environment-table.md)alle anderen Registrierungsinformationen hinzu, ausschließlich Bindung und Aktivierung oder Selbstregistrierung der Komponente.
8.  Das Installationsprogramm überspringt die [Tabelle IsolatedComponent](isolatedcomponent-table.md) für diese Komponente unter Betriebssystemen, die die gemeinsame Nutzung unterstützen. Geben Sie Informationen in diese Tabelle ein, wenn die Assembly auf Systemen, die lokale Dateien unterstützen, privat sein soll.
9.  Fügen Sie der [MsiAssembly-Tabelle](msiassembly-table.md) eine Zeile für die Komponente hinzu, die die Win32-Assembly enthält. Geben Sie im Feld Attribute der MsiAssembly-Tabelle den Wert 1 ein, um anzugeben, dass es sich um eine Win32-Assembly handelt. Geben Sie den Dateischlüssel der privaten Assembly in das \_ Feld Dateianwendung der [MsiAssembly-Tabelle](msiassembly-table.md)ein. Fügen Sie die [MsiPublishAssemblies-Aktion](msipublishassemblies-action.md) der [Tabelle InstallExecuteSequence](installexecutesequence-table.md) oder der [Tabelle AdvtExecuteSequence hinzu.](advtexecutesequence-table.md) Fügen Sie die [MsiUnpublishAssemblies-Aktion](msiunpublishassemblies-action.md) der Tabelle InstallExecuteSequence hinzu. Erstellen Sie einen Ordner für die Assembly und die Manifestdatei in der [Verzeichnistabelle](directory-table.md). Dieser Ordner sollte sich im Stammverzeichnis der Anwendung befinden und die im \_ Feld Dateianwendung der [MsiAssembly-Tabelle](msiassembly-table.md)angegebene Datei enthalten. Während der Installation der Anwendung löst das Installationsprogramm die [Verzeichnistabelle](directory-table.md) für den Pfad zu diesem Ordner auf. Weitere Informationen finden Sie unter [Verwenden der Verzeichnistabelle](using-the-directory-table.md).
10. Fügen Sie der [MsiAssemblyName-Tabelle](msiassemblyname-table.md) Zeilen für die Komponente hinzu. Fügen Sie eine Zeile für jedes Name-Wert-Paar hinzu, das im AssemblyIdentity-Abschnitt des Manifests angegeben ist. Weitere Informationen finden Sie unter [MsiAssemblyName-Tabelle.](msiassemblyname-table.md)

 

 



