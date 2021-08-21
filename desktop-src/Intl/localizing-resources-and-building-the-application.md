---
description: In diesem Thema wird beschrieben, wie Sie eine typischeSTELLUNG-Anwendung erstellen.
ms.assetid: 386e9601-ce21-4ef0-b225-0c4249d1942d
title: Lokalisieren von Ressourcen und Erstellen der Anwendung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 490fde8e0b6d9381b346409efad1501331be71d2d4e958be050274dc0428fe62
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119788500"
---
# <a name="localizing-resources-and-building-the-application"></a>Lokalisieren von Ressourcen und Erstellen der Anwendung

In diesem Thema wird beschrieben, wie Sie eine typischeSTELLUNG-Anwendung erstellen. Es wird davon ausgegangen, dass Sie Microsoft Visual Studio für die Codierung verwenden und entweder Microsoft Visual Studio oder die Visual Studio zum Erstellen verwenden. Es wird davon ausgegangen, dass Sie eine SLN-Projektmappendatei für Ihre Anwendung verwenden und eine Resource.h-Datei unterstützen, um die Ressourcendatei der Basissprache widerzu erhalten.

> [!Note]  
> Wenn Sie die Visual Studio für den Build verwenden, verwenden Sie den **Befehl vcbuild,** um die Projektmappendatei zu erstellen.

 

Anwendungsdateien werden für jede Sprache separat erstellt. Jeder Build erstellt identische sprachneutrale .exe und sprachspezifische .exe.files. Darüber hinaus werden verschiedene andere Dateien in die entsprechenden Releaseordner kopiert.

Der Anwendungsaufbau hängt vom Typ der Ressourcen und der Art der Lokalisierung ab, die Sie verwenden. Für die Vorablokalisierung verfügen Sie über eine Kopie der Basissprachdatei, die für jede unterstützte Sprache lokalisiert ist. Für die Lokalisierung nach dem Build können Sie die DATEI .assembly kopieren, die sich aus dem Build der ausführbaren Datei und des Ressourcenmoduls ergibt, und die Kopien an die Lokalisierer bereitstellen.

> [!Note]  
> Im folgenden Verfahren wird davon ausgegangen, dass Win32 PE-Ressourcen mit einem Visual Studio für jede Sprache erstellt wurden. Die Basissprachressourcen werden in einer RC-Datei bereitgestellt und mithilfe eines DLL-Moduls geladen. Sie können das Verfahren nach Bedarf wiederholen, um für alle unterstützten Sprachen zu erstellen.

 

**So erstellen Sie die Anwendung**

1.  Richten Sie ein Visual Studio-Projekt für die Basissprache ein.
2.  Wenn Sie eine Ressourcenkonfigurationsdatei mit den Ressourcentools verwenden möchten, richten Sie eine wie unter [Vorbereiten einer Ressourcenkonfigurationsdatei beschrieben ein.](preparing-a-resource-configuration-file.md)
3.  Legen Sie auf den Eigenschaftenseiten für das Projekt unter Konfigurationseigenschaften → Resources → Command Line → Zusätzliche Optionen parameter fest, die für das RC-Compilerprogramm erforderlich **sind.**
4.  Führen Sie den RC-Compiler aus. Das Hilfsprogramm kompiliert und teilt die nicht lokalisierbaren und lokalisierbaren Ressourcen unter Verwendung von Ressourcenkonfigurationsdaten in zwei verschiedene Objektdateien auf. In diesem Schritt werden die sprachneutralen Ressourcen mit einer LN-Datei verknüpft. Weitere Informationen finden Sie in der Beschreibung des Hilfsprogramms unter [Ressourcenprogramme.](resource-utilities.md)
5.  Legen Sie auf den Eigenschaftenseiten unter Konfigurationseigenschaften **→ Buildereignisse → Post-Buildereignis**→-Befehlszeile ein Post-Buildereignis für das Projekt fest, um die sprachspezifischen Ressourcen mit einer sprachspezifischen DATEI zu verknüpfen.
6.  Legen Sie ein Post-Buildereignis fest, um den Prüfsummenwert aus der LN-Datei auf die DATEI .checks für die Sprache anzuwenden. Sie können für diesen Schritt das HilfsprogrammCTRCT verwenden. Weitere Informationen finden Sie in der Beschreibung des Hilfsprogramms unter [Ressourcenprogramme.](resource-utilities.md)
7.  Verwenden Sie die Befehlszeile für Post-Build-Ereignisse, um Befehle hinzuzufügen, um die Dateien in die entsprechende Releaseordnerstruktur zu kopieren.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden mehrsprachige Benutzeroberfläche](using-multilingual-user-interface.md)
</dt> <dt>

[Vorbereiten einer Ressourcenkonfigurationsdatei](preparing-a-resource-configuration-file.md)
</dt> <dt>

[Ressourcen-Hilfsprogramme](resource-utilities.md)
</dt> </dl>

 

 



