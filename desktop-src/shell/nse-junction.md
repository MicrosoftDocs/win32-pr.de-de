---
description: Der Stamm einer Namespace Erweiterung wird normalerweise von Windows Explorer als Ordner in den Struktur-und Ordner Sichten angezeigt.
title: Angeben des Speicher Orts der Namespace Erweiterung
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 2c1fdd5d-b359-4d5c-a20e-0622f3a1cb1d
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 7617c7361c5f2ae76331c5f1b59eb845f6806395
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866160"
---
# <a name="specifying-a-namespace-extensions-location"></a>Angeben des Speicher Orts der Namespace Erweiterung

Der Stamm einer Namespace Erweiterung wird normalerweise von Windows Explorer als Ordner in den Struktur-und Ordner Sichten angezeigt. Damit Windows Explorer die Dateien und Unterordner der Erweiterung anzeigt, müssen Sie angeben, wo sich der Stamm Ordner in der Shellnamespace Hierarchie befindet. Dieser Speicherort wird als Verknüpfungs *Punkt* bezeichnet.

-   [Verwenden von virtuellen Ordnern als Verknüpfungs Punkte](#using-virtual-folders-as-junction-points)
-   [Verwenden von Datei System Ordnern als Verknüpfungs Punkte](#using-file-system-folders-as-junction-points)
-   [Öffnen einer Ansicht einer Namespace Erweiterung](#opening-a-view-of-a-namespace-extension)

## <a name="using-virtual-folders-as-junction-points"></a>Verwenden von virtuellen Ordnern als Verknüpfungs Punkte

Die einfachste Möglichkeit, den Verknüpfungs Punkt einer Erweiterung zu definieren, besteht darin, den Stamm Ordner zu einem Unterordner eines virtuellen System Ordners zu machen. Diese Art von Verbindungspunkt wird als virtueller Verknüpfungs *Punkt* bezeichnet. Die Ordner " **Desktop** " und " **Arbeitsplatz** " sind die typischen Orte für virtuelle Verknüpfungs Punkte, Sie können aber auch einen virtuellen Verknüpfungs Punkt auf einem Remote Computer oder unter den Ordnern " **meine Netzwerk Orte**", " **Internet Explorer**" und " **Systemsteuerung** " definieren.

Wenn Sie einen virtuellen Verknüpfungs Punkt definieren möchten, erstellen Sie einen Unterschlüssel des Schlüssels, der den entsprechenden virtuellen Ordner darstellt, und benennen Sie ihn mit der Zeichenfolge Form der Klassen-ID (CLSID) ihrer Erweiterung. Die registrierte CLSID würde wie folgt aussehen.

```
HKEY_LOCAL_MACHINE or HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  Virtual Folder Name
                     NameSpace
                        {Extension CLSID}
                           (Default) = Junction Point Name
```

Der *Name des virtuellen Ordners* ist einer der Unterschlüssel in der folgenden Tabelle.



| Standort          | Name des virtuellen Ordners                        |
|-------------------|--------------------------------------------|
| Systemsteuerung     | **Steuerung**                           |
| Desktop           | **Desktop**                                |
| Gesamtes Netzwerk    | **Network Neighborhood** \\ **Entirenetwork** |
| Arbeitsplatz       | **MyComputer**                             |
| Meine Netzwerk Orte | **Network Neighborhood**                    |
| Remote Computer   | **Remote Computer**                         |
| Benutzer Dateien       | **Usersfiles**                             |



 

Remote Erweiterungen müssen mit [**iremotecomputer**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iremotecomputer)initialisiert werden.

## <a name="using-file-system-folders-as-junction-points"></a>Verwenden von Datei System Ordnern als Verknüpfungs Punkte

Es gibt zwei Möglichkeiten, Dateisystem Ordner als Verknüpfungs Punkte zu definieren. Der einfachste Ansatz besteht darin, einen Ordner am entsprechenden Speicherort zu erstellen und einen Zeitraum an den Namen des Ordners anzufügen, gefolgt von der Zeichen folgen Form der CLSID der Erweiterung. Nur der Ordnername wird in Windows-Explorer angezeigt. Im folgenden Beispiel wird ein Verknüpfungs Punkt mit dem anzeigen Amen "MyFolder" erstellt.


```
MyFolder.{Extension CLSID}
```



Alternativ können Sie einen Ordner mit konventionell Namen als Verknüpfungs Punkt definieren, indem Sie folgende Schritte ausführen:

-   Festlegen, dass der Ordner schreibgeschützt ist.
-   Erstellen Sie den Ordner durch Aufrufen von [**pathmakesystemfolder**](/windows/desktop/api/Shlwapi/nf-shlwapi-pathmakesystemfoldera)zu einem Systemordner.
-   Platzieren einer ausgeblendeten Desktop.ini Datei in dem Ordner, der die CLSID der Erweiterung enthält.

Desktop.ini ist eine Standard Textdatei, die einem beliebigen Ordner hinzugefügt werden kann, um bestimmte Aspekte des Ordner Verhaltens anzupassen. Eine allgemeine Erläuterung zur Verwendung dieser Datei finden Sie unter Anpassen von [Ordnern mit Desktop.ini](how-to-customize-folders-with-desktop-ini.md). Zum Definieren eines Ordners als Verknüpfungs Punkt wird der \[ . Der shellclassinfo \] -Abschnitt des Desktop.ini muss die CLSID der Erweiterung wie folgt enthalten:


```
[.ShellClassInfo]
CLSID={Extension CLSID}
```



## <a name="opening-a-view-of-a-namespace-extension"></a>Öffnen einer Ansicht einer Namespace Erweiterung

Wenn ein Benutzer einen Verknüpfungs Punkt durchsucht, erstellt Windows-Explorer automatisch eine Ansicht des Stamm Ordners. Sie können auch eine Ansicht erstellen, indem Sie Explorer.exe explizit mit der CLSID der Erweiterung als Argument starten. Beispielsweise können Sie diese Vorgehensweise verwenden, um eine Ansicht einer Erweiterung über ein Kontextmenü oder eine Verknüpfung zu starten. Wenn Sie z. b. eine Ansicht von MyExtension starten möchten, die eine Strukturansicht enthält, können Sie die folgende Befehls Zeichenfolge verwenden.


```
%SystemRoot%\Explorer.exe /e,::{MyExtension CLSID}
```



Eine Alternative Befehls Zeichenfolge kann verwendet werden, um eine Ansicht eines Objekts innerhalb der Erweiterung zu starten. Diese Funktion wäre beispielsweise nützlich für eine Erweiterung, die eine Ordneransicht verwendet, damit Benutzer den Inhalt einer Reihe von komprimierten Dateien anzeigen können.


```
%SystemRoot%\Explorer.exe /e,::{MyExtension CLSID},objectname
```



Der *objectName* -Parameter ist der Name des Objekts, das angezeigt werden soll. Windows-Explorer konvertiert den Namen in die entsprechende PIDL und übergibt die PIDL an die [**ipersistfolder:: Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistfolder-initialize) -Methode des neuen Ordner Objekts.

> [!Note]  
> Der CLSID-Zeichenfolge muss ein paar von Doppelpunkten vorangestellt werden (::) Andernfalls schlägt der Befehl fehl. Der Schrägstrich-e (/e)-Flag, der in den beiden zuvor gezeigten Beispiel Befehlszeilen verwendet wird, weist Windows-Explorer an, eine Strukturansicht anzuzeigen. Das Flag muss von den beiden Doppelpunkten durch ein Komma getrennt werden. Wenn Sie keine Strukturansicht verwenden möchten, lassen Sie das/e-Flag und das Komma aus.

 

 

 



