---
description: Sie können eine Namespaceerweiterung verwenden, damit Benutzer den Inhalt einer Datei durchsuchen können, anstatt sie als Ordner anzuzeigen. Erweiterungen dieser Art werden in der Regel verwendet, um den Inhalt der Member eines Dateityps anzuzeigen.
title: Anzeigen einer Stammansicht einer Datei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c91e17ef12393b1a95316c37a18d51876cf988293c330610a3638c7995ab12a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119596580"
---
# <a name="how-to-display-a-rooted-view-of-a-file"></a>Anzeigen einer Stammansicht einer Datei

Sie können eine Namespaceerweiterung verwenden, damit Benutzer den Inhalt einer Datei durchsuchen können, anstatt sie als Ordner anzuzeigen. Erweiterungen dieser Art werden in der Regel verwendet, um den Inhalt der Member eines [Dateityps](fa-file-types.md)anzuzeigen. Beispielsweise können die Member eines Dateityps mehrere komprimierte Dateien oder Bilder enthalten, die in einer Hierarchie organisiert sind. Anstatt eine Anwendung zu schreiben, damit der Benutzer den Inhalt einer solchen Datei anzeigen kann, können Sie stattdessen eine Namespaceerweiterung schreiben und Windows Explorer die Anzeige verarbeiten lassen.

Sie müssen eine Stammansicht verwenden, damit eine Erweiterung den Inhalt einer Datei anzeigt. Die gängigste Möglichkeit, eine Stammansicht der Member eines Dateityps bereitzustellen, besteht darin, ein [Kontextmenüverb](context.md) zu definieren, das eine Instanz von Explorer.exe startet. Wenn sie dieses Verb zum Standardverb machen, öffnet ein Doppelklick auch eine Stammansicht der Datei. Sie können entweder ein Verb für alle Member des Dateityps definieren, indem Sie [die Registrierung ändern,](context.md)oder Verben auf Dateibasis dynamisch definieren, indem Sie einen [Kontextmenühandler](context-menu-handlers.md)implementieren.

## <a name="instructions"></a>Anweisungen


Im folgenden Beispiel wird veranschaulicht, wie die Registrierung verwendet wird, um eine Stammansicht der Member eines Dateityps durch Ändern der Registrierung bereitzustellen. Der Beispielregistrierungseintrag ist eine Änderung eines der Beispiele unter [Erweitern von Kontextmenüs.](context.md) Die Registrierungseinträge definieren Dateien mit der Dateinamenerweiterung .myp als Dateityp und verwenden das **Verb zum Durchsuchen,** um eine Stammansicht von Membern dieses Typs zu starten.

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

Sie können das gleiche Verb verwenden, um programmgesteuert eine Stammansicht eines Members des Dateityps zu starten, indem Sie die [**ShellExecute-Funktion**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) aufrufen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Angeben des Speicherorts einer Namespaceerweiterung](nse-junction.md)
</dt> <dt>

[Öffnen einer Stammansicht eines Verbindungspunkts über die Registrierung](how-to-use-a-junction-point-to-open-a-rooted-view.md)
</dt> <dt>

[Öffnen einer Stammansicht eines Verbindungspunkts durch eine Verknüpfungsdatei](how-to-use-a-shortcut-file-to-open-a-rooted-view.md)
</dt> <dt>

[**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea)
</dt> </dl>

 

 



