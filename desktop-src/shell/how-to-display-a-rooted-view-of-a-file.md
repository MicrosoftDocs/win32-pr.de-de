---
description: Sie können eine Namespace Erweiterung verwenden, um Benutzern zu ermöglichen, den Inhalt einer Datei zu durchsuchen, anstatt Sie als Ordner zu verwenden. Erweiterungen dieser Art werden normalerweise verwendet, um den Inhalt der Member eines Dateityps anzuzeigen.
title: Anzeigen einer rootansicht einer Datei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30ee16f3ce50cd79800dd98aa53256591d1f79d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864928"
---
# <a name="how-to-display-a-rooted-view-of-a-file"></a>Anzeigen einer rootansicht einer Datei

Sie können eine Namespace Erweiterung verwenden, um Benutzern zu ermöglichen, den Inhalt einer Datei zu durchsuchen, anstatt Sie als Ordner zu verwenden. Erweiterungen dieser Art werden normalerweise verwendet, um den Inhalt der Member eines [Dateityps](fa-file-types.md)anzuzeigen. Beispielsweise können die Member eines Dateityps mehrere komprimierte Dateien oder Bilder enthalten, die in einer Hierarchie organisiert sind. Anstatt eine Anwendung zu schreiben, die es dem Benutzer ermöglicht, den Inhalt einer solchen Datei anzuzeigen, können Sie stattdessen eine Namespace Erweiterung schreiben und Windows-Explorer die Anzeige verarbeiten lassen.

Sie müssen eine rootansicht verwenden, damit eine Erweiterung den Inhalt einer Datei anzeigen darf. Die gängigste Methode, um eine rootansicht der Member eines Dateityps bereitzustellen, ist das Definieren eines Kontext [Menü Verbs](context.md) , das eine Instanz von Explorer.exe gestartet. Wenn Sie dieses Verb als Standard Verb festlegen, wird mit einem Doppelklick auch eine rootansicht der Datei geöffnet. Sie können entweder ein Verb für alle Elemente des Dateityps definieren, indem Sie [die Registrierung ändern](context.md), oder Sie können die Verben auf Datei Basis durch Implementieren eines Kontext [Menü Handlers](context-menu-handlers.md)dynamisch definieren.

## <a name="instructions"></a>Instructions


Im folgenden Beispiel wird veranschaulicht, wie die Registrierung verwendet wird, um eine rootansicht der Member eines Dateityps durch Ändern der Registrierung bereitzustellen. Der Beispiel Registrierungs Eintrag ist eine Änderung eines der Beispiele in Erweitern von Kontext [Menüs](context.md). In den Registrierungs Einträgen werden Dateien mit der Dateinamenerweiterung MYP als Dateityp definiert, und mit dem **Browse** -Verb wird eine rootansicht von Membern dieses Typs gestartet.

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
   MyProgram.1
      (Default) = MyProgram Application
      Shell
         (Default) = browse
         browse
            command
               (Default) = %SYSTEMROOT%\explorer.exe /e,/root,{Extension CLSID}, "%1"
```

Sie können das gleiche Verb verwenden, um eine rootansicht eines Members des Dateityps Programm gesteuert zu starten, indem Sie die [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) -Funktion aufrufen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Angeben des Speicher Orts der Namespace Erweiterung](nse-junction.md)
</dt> <dt>

[Öffnen einer Stamm Ansicht eines Verknüpfungs Punkts durch die Registrierung](how-to-use-a-junction-point-to-open-a-rooted-view.md)
</dt> <dt>

[Öffnen einer Stamm Ansicht eines Verknüpfungs Punkts durch eine Verknüpfungs Datei](how-to-use-a-shortcut-file-to-open-a-rooted-view.md)
</dt> <dt>

[**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea)
</dt> </dl>

 

 



