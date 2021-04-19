---
description: Das in diesem Thema beschriebene Verfahren zeigt, wie Sie ein Windows Installer Paket erstellen, um eine Win32-Assembly zu installieren.
ms.assetid: 2d4bc2be-cce6-45e6-b6a7-7ff96d28eb96
title: Installieren von Win32-Assemblys für die private Verwendung einer Anwendung unter Windows XP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e807e22c9c5dea67ece5ead0ded95f06ab203689
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106372856"
---
# <a name="installing-win32-assemblies-for-the-private-use-of-an-application-on-windows-xp"></a>Installieren von Win32-Assemblys für die private Verwendung einer Anwendung unter Windows XP

Das in diesem Thema beschriebene Verfahren zeigt, wie Sie ein Windows Installer Paket erstellen, um eine Win32-Assembly zu installieren. Das Paket installiert die Assembly und eine Anwendungs Manifest-Datei in einem von der Anwendung verwendeten Ordner. Das Anwendungs Manifest gibt die Abhängigkeit der Anwendung auf dem private Assembly an. Nach der Installation des Pakets ist der private Assembly für die ausschließliche Verwendung der Anwendung verfügbar. Die im Anwendungs Manifest angegebene Assemblyabhängigkeit überschreibt (für diese Anwendung) alle anderen globalen Assemblyabhängigkeiten, die in Assemblymanifest-Dateien angegeben sind.

Bevor Sie fortfahren, sollten Sie wissen, wie Sie ein Windows Installer-Paket ohne Assemblys erstellen. Weitere Informationen finden Sie unter [einem Installations Beispiel](an-installation-example.md).

**So installieren Sie eine private Assembly unter Windows XP**

1.  Definieren Sie eine Windows Installer Komponente, die die Win32-Assembly und die Anwendungs Manifest-Datei enthält. Diese Komponente kann andere Ressourcen enthalten, die immer mit der Assembly installiert oder entfernt werden sollten. In den restlichen Schritten dieses Verfahrens wird beschrieben, wie Sie die Installations Datenbank zum Installieren dieser Komponente erstellen.
2.  Fügen Sie der [Komponenten Tabelle](component-table.md) eine Zeile für die Komponente hinzu, die die Win32-Assembly und die Anwendungs Manifest-Datei enthält. Geben Sie eine gültige Windows Installer [GUID](guid.md) für den Komponenten Code ein. Weitere Informationen finden Sie unter [Ändern des Komponenten Codes](changing-the-component-code.md) und [Was geschieht, wenn die Komponenten Regeln beschädigt sind?](what-happens-if-the-component-rules-are-broken.md)
3.  Das Installationsprogramm kopiert die Assemblymanifest-Datei in den Ordner, der die Datei enthält, die im \_ Feld Datei Anwendung der [MsiAssembly-Tabelle](msiassembly-table.md)angegeben ist.
4.  Fügen Sie der [FeatureComponents-Tabelle](featurecomponents-table.md) eine Zeile hinzu, die die Komponente an eine Windows Installer Funktion bindet. Weitere Informationen finden Sie unter [Komponenten und Features](components-and-features.md). Eine Windows Installer Funktion sollte ein Teil der Anwendungs Funktionalität sein, die ein Benutzer erkennen kann. Die Assembly wird aktiviert, wenn dieses Feature von einem Benutzer ausgewählt oder von einer Anwendung als fehlerhaft gekennzeichnet wird. Wenn die Assembly ein zusätzliches Feature definiert, fügen Sie der [Funktions Tabelle](feature-table.md) eine zusätzliche Zeile für die FeatureAttribute hinzu. Dieser Schritt ist nicht erforderlich, wenn Sie ein Mergemodul erstellen.
5.  Bei parallelen Assemblys werden Bindungs-und Aktivierungs Informationen, z. b. com-Klassen, Schnittstellen und Typbibliotheken, in Manifest-Dateien und nicht in der Registrierung gespeichert. Private Assemblys speichern diese Informationen in einem Assemblymanifest. Auf Systemen, die parallele Assemblys unterstützen, überspringt das Installationsprogramm die Verarbeitung sämtlicher Informationen über die Komponente, die in der [Erweiterungs Tabelle](extension-table.md), [Verb-Tabelle](verb-table.md), [typelib-Tabelle](typelib-table.md), MIME- [Tabelle](mime-table.md), [Klassen Tabelle](class-table.md), [ProgID-Tabelle](progid-table.md)und [AppID-Tabelle](appid-table.md)eingegeben wird. Bindungs-und Aktivierungs Informationen können in die Tabellen eingegeben werden, damit Sie von Systemen verwendet werden können, die die parallele assemblyfreigabe nicht unterstützen.
6.  Bei der parallelen Installation wird die Assembly nicht global registriert. Das Installationsprogramm überspringt die Selbstregistrierung der Komponente, wenn in der [Tabelle "selfreg](selfreg-table.md)" Informationen zur Selbstregistrierung eingegeben werden. Informationen zur Selbstregistrierung können in die Tabelle "selfreg" eingegeben werden, damit die Komponente auf Systemen, die die parallele assemblyfreigabe nicht unterstützen, selbst registriert wird.
7.  Fügen Sie der [Registrierungs Tabelle](registry-table.md), der [removeregistry-Tabelle](removeregistry-table.md)und der [Umgebungs Tabelle](environment-table.md)alle weiteren Registrierungsinformationen hinzu, die exklusiv für die Bindung und Aktivierung oder die Selbstregistrierung der Komponente sind.
8.  Das Installationsprogramm überspringt die [isolatedcomponent-Tabelle](isolatedcomponent-table.md) für diese Komponente auf Betriebssystemen, die die parallele Freigabe unterstützen. Geben Sie Informationen in diese Tabelle ein, wenn die Assembly auf Systemen, die lokale Dateien unterstützen, privat sein soll.
9.  Fügen Sie der [MsiAssembly-Tabelle](msiassembly-table.md) eine Zeile für die Komponente hinzu, die die Win32-Assembly enthält. Geben Sie im Feld Attribute der Tabelle MsiAssembly den Wert 1 ein, um anzugeben, dass es sich hierbei um eine Win32-Assembly handelt. Geben Sie den Datei Schlüssel des private Assembly in das \_ Feld Datei Anwendung der [Tabelle MsiAssembly](msiassembly-table.md)ein. Fügen Sie die [msipublishassemblyaktion](msipublishassemblies-action.md) der [InstallExecuteSequence-Tabelle](installexecutesequence-table.md) oder der [AdvtExecuteSequence-Tabelle](advtexecutesequence-table.md)hinzu. Fügen Sie die [msiunpublishassemblyaktion](msiunpublishassemblies-action.md) der InstallExecuteSequence-Tabelle hinzu. Erstellen Sie einen Ordner für die Assembly und die Manifest-Datei in der [Verzeichnis Tabelle](directory-table.md). Dieser Ordner sollte sich im Stammverzeichnis der Anwendung befinden und die Datei enthalten, die im \_ Feld Datei Anwendung der [Tabelle MsiAssembly](msiassembly-table.md)angegeben ist. Während der Installation der Anwendung löst das Installationsprogramm die [Verzeichnis Tabelle](directory-table.md) für den Pfad zu diesem Ordner auf. Weitere Informationen finden Sie unter [Verwenden der Verzeichnis Tabelle](using-the-directory-table.md).
10. Fügen Sie der [MsiAssemblyName-Tabelle](msiassemblyname-table.md) Zeilen für die Komponente hinzu. Fügen Sie für jedes im Abschnitt assemblyIdentity des Manifests angegebene Name-Wert-Paar eine Zeile hinzu. Weitere Informationen finden Sie unter [MsiAssemblyName Table](msiassemblyname-table.md).

 

 



