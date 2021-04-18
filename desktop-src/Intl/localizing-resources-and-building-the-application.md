---
description: In diesem Thema wird beschrieben, wie eine typische MUI-Anwendung erstellt wird.
ms.assetid: 386e9601-ce21-4ef0-b225-0c4249d1942d
title: Lokalisieren von Ressourcen und entwickeln der Anwendung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74262499b20836ee4860f1c0fc1a1bf80e19d58d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345183"
---
# <a name="localizing-resources-and-building-the-application"></a>Lokalisieren von Ressourcen und entwickeln der Anwendung

In diesem Thema wird beschrieben, wie eine typische MUI-Anwendung erstellt wird. Es wird davon ausgegangen, dass Sie Microsoft Visual Studio für die Codierung verwenden und entweder Microsoft Visual Studio oder die Visual Studio-Befehlszeile für die Erstellung verwenden. Es wird davon ausgegangen, dass Sie eine sln-Projektmappendatei für Ihre Anwendung verwenden und eine Resource. h-Datei unterstützen, um die Ressourcen Datei der Basis Sprache widerzuspiegeln

> [!Note]  
> Wenn Sie die Visual Studio-Befehlszeile für den Build verwenden, verwenden Sie den **VCBuild** -Befehl, um die Projektmappendatei zu erstellen.

 

Anwendungs Dateien werden separat für jede Sprache erstellt. Jeder Build erstellt identische sprachneutrale. exe-und sprachspezifische. exe. MUI-Dateien. Außerdem werden verschiedene andere Dateien in die entsprechenden releaseordner kopiert.

Der anwendungsbuild hängt von der Art der Ressourcen und von der Art der Lokalisierung ab, die Sie verwenden. Bei der präbuildlokalisierung haben Sie eine Kopie der Basis Sprachdatei für jede unterstützte Sprache lokalisiert. Für die Lokalisierung nach dem Buildvorgang können Sie die MUI-Datei kopieren, die sich aus dem Build der ausführbaren Datei und dem Ressourcen Modul ergibt, und die Kopien den Lokalisierern bereitstellen.

> [!Note]  
> Im folgenden Verfahren wird davon ausgegangen, dass Win32 PE-Ressourcen mit einem Visual Studio-Projekt für jede Sprache erstellt wurden. Die grundlegenden Sprachressourcen werden in einer RC-Datei bereitgestellt und mit einem dll-Modul geladen. Sie können das Verfahren nach Bedarf wiederholen, um für alle unterstützten Sprachen zu erstellen.

 

**So erstellen Sie die Anwendung**

1.  Richten Sie ein Visual Studio-Projekt für die Basis Sprache ein.
2.  Wenn Sie an der Verwendung einer Ressourcen Konfigurationsdatei mit den Ressourcen Tools interessiert sind, legen Sie eine fest, wie unter [Vorbereiten einer Ressourcen Konfigurationsdatei](preparing-a-resource-configuration-file.md)beschrieben.
3.  Legen Sie Parameter fest, die für das RC-Compilerdienstprogramm in den Eigenschaften Seiten für das Projekt unter **Konfigurations Eigenschaften → Ressourcen → Befehlszeile → zusätzliche Optionen** erforderlich sind.
4.  Ausführen des RC-Compilers. Das Hilfsprogramm kompiliert und teilt die nicht lokalisierbaren und lokalisierbaren Ressourcen mithilfe von Ressourcen Konfigurationsdaten in zwei verschiedene Objektdateien. In diesem Schritt werden die sprach neutralen Ressourcen mit einer LN-Datei verknüpft. Weitere Informationen finden Sie in der Beschreibung des Hilfsprogramms unter [Ressourcen Hilfsprogramme](resource-utilities.md).
5.  Um die sprachspezifischen Ressourcen mit einer sprachspezifischen MUI-Datei zu verknüpfen, legen Sie ein Postbuildereignis für das Projekt auf den Eigenschaften Seiten unter **Konfigurations Eigenschaften → Buildereignisse → Postbuildereignis → Befehlszeile** fest.
6.  Legen Sie ein Postbuildereignis fest, um den Prüfsummen Wert aus der LN-Datei auf die MUI-Datei für die Sprache anzuwenden. Sie können das Dienstprogramm muject für diesen Schritt verwenden. Weitere Informationen finden Sie in der Beschreibung des Hilfsprogramms unter [Ressourcen Hilfsprogramme](resource-utilities.md).
7.  Verwenden Sie die Befehlszeile Postbuildereignis, um Befehle zum Kopieren der Dateien in die entsprechende releaseordnerstruktur hinzuzufügen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden der mehrsprachigen Benutzeroberfläche](using-multilingual-user-interface.md)
</dt> <dt>

[Vorbereiten einer Ressourcen Konfigurationsdatei](preparing-a-resource-configuration-file.md)
</dt> <dt>

[Ressourcen Hilfsprogramme](resource-utilities.md)
</dt> </dl>

 

 



