---
description: Der Stamm einer Namespaceerweiterung wird normalerweise vom Windows-Explorer sowohl in der Strukturansicht als auch in der Ordneransicht als Ordner angezeigt.
title: Angeben des Speicherorts einer Namespaceerweiterung
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 2c1fdd5d-b359-4d5c-a20e-0622f3a1cb1d
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: e20b9a1644b2272ee06ff8a792198f79ffebca8b8a971b690c1be1160830aae8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118719886"
---
# <a name="specifying-a-namespace-extensions-location"></a>Angeben des Speicherorts einer Namespaceerweiterung

Der Stamm einer Namespaceerweiterung wird normalerweise vom Windows-Explorer sowohl in der Strukturansicht als auch in der Ordneransicht als Ordner angezeigt. Damit Windows Explorer die Dateien und Unterordner Ihrer Erweiterung anzeigen kann, müssen Sie angeben, wo sich der Stammordner in der Namespacehierarchie der Shell befindet. Diese Position wird als *Verbindungspunkt* bezeichnet.

-   [Verwenden von virtuellen Ordnern als Verbindungspunkt](#using-virtual-folders-as-junction-points)
-   [Verwenden von Dateisystemordnern als Verbindungspunkt](#using-file-system-folders-as-junction-points)
-   [Öffnen einer Ansicht einer Namespaceerweiterung](#opening-a-view-of-a-namespace-extension)

## <a name="using-virtual-folders-as-junction-points"></a>Verwenden von virtuellen Ordnern als Verbindungspunkt

Die einfachste Möglichkeit, den Verbindungspunkt einer Erweiterung zu definieren, besteht darin, den Stammordner zu einem Unterordner eines virtuellen Systemordners zu machen. Dieser Typ von Verbindungspunkt wird als *virtueller Verbindungspunkt* bezeichnet. Die Ordner **Desktop** und **Arbeitsplatz** sind die typischen Speicherorte für virtuelle Verbindungspunkte. Sie können jedoch auch einen virtuellen Verbindungspunkt auf einem Remotecomputer oder unter **den Ordnern Meine Netzwerkstandorte**, **Internet Explorer** und **Systemsteuerung** definieren.

Um einen virtuellen Verbindungspunkt zu definieren, erstellen Sie einen Unterschlüssel des Schlüssels, der den entsprechenden virtuellen Ordner darstellt, und benennen Sie ihn mit der Zeichenfolgenform des Klassenbezeichners (CLSID) Ihrer Erweiterung. Die registrierte CLSID würde wie folgt aussehen.

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

Der Name des *virtuellen Ordners* ist einer der Unterschlüssel in der folgenden Tabelle.



| Standort          | Name des virtuellen Ordners                        |
|-------------------|--------------------------------------------|
| Systemsteuerung     | **ControlPanel**                           |
| Desktop           | **Desktop**                                |
| Gesamtes Netzwerk    | **NetworkNeighborhood** \\ **EntireNetwork** |
| Arbeitsplatz       | **Mycomputer**                             |
| Meine Netzwerkorte | **NetworkNeighborhood**                    |
| Remotecomputer   | **RemoteComputer**                         |
| Benutzerdateien       | **UsersFiles**                             |



 

Remoteerweiterungen müssen mit [**IRemoteComputer**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iremotecomputer)initialisiert werden.

## <a name="using-file-system-folders-as-junction-points"></a>Verwenden von Dateisystemordnern als Verbindungspunkt

Es gibt zwei Möglichkeiten, Dateisystemordner als Verbindungspunkt zu definieren. Der einfachste Ansatz besteht darin, einen Ordner am entsprechenden Speicherort zu erstellen und einen Punkt an den Namen des Ordners anzufügen, gefolgt von der Zeichenfolgenform der CLSID Ihrer Erweiterung. Nur der Ordnername wird in Windows Explorer angezeigt. Im folgenden Beispiel wird ein Verbindungspunkt mit dem Anzeigenamen MyFolder erstellt.


```
MyFolder.{Extension CLSID}
```



Alternativ können Sie einen konventionell benannten Ordner wie folgt als Verbindungspunkt definieren:

-   Schreibgeschützt für den Ordner.
-   Machen Sie den Ordner zu einem Systemordner, indem [**Sie PathMakeSystemFolder**](/windows/desktop/api/Shlwapi/nf-shlwapi-pathmakesystemfoldera)aufrufen.
-   Platzieren sie eine ausgeblendete Desktop.ini-Datei im Ordner, der die CLSID der Erweiterung enthält.

Desktop.ini ist eine Standardtextdatei, die jedem Ordner hinzugefügt werden kann, um bestimmte Aspekte des Ordnerverhaltens anzupassen. Eine allgemeine Erläuterung der Verwendung dieser Datei finden Sie unter Anpassen von [Ordnern mit Desktop.ini](how-to-customize-folders-with-desktop-ini.md). Um einen Ordner als Verbindungspunkt zu definieren, der \[ . \] Der ShellClassInfo-Abschnitt von Desktop.ini muss die CLSID der Erweiterung wie folgt enthalten:


```
[.ShellClassInfo]
CLSID={Extension CLSID}
```



## <a name="opening-a-view-of-a-namespace-extension"></a>Öffnen einer Ansicht einer Namespaceerweiterung

Wenn ein Benutzer einen Verbindungspunkt durchsucht, erstellt Windows Explorer automatisch eine Ansicht des Stammordners. Sie können eine Sicht auch erstellen, indem Sie explizit Explorer.exe mit der CLSID der Erweiterung als Argument starten. Sie können diesen Ansatz beispielsweise verwenden, um eine Ansicht einer Erweiterung über ein Kontextmenü oder eine Verknüpfung zu starten. Um beispielsweise eine Ansicht von MyExtension zu starten, die eine Strukturansicht enthält, können Sie die folgende Befehlszeichenfolge verwenden.


```
%SystemRoot%\Explorer.exe /e,::{MyExtension CLSID}
```



Eine alternative Befehlszeichenfolge kann verwendet werden, um eine Ansicht eines Objekts innerhalb der Erweiterung zu starten. Dieses Feature wäre z. B. für eine Erweiterung nützlich, die eine Ordneransicht verwendet, damit Benutzer den Inhalt einer Reihe komprimierter Dateien anzeigen können.


```
%SystemRoot%\Explorer.exe /e,::{MyExtension CLSID},objectname
```



Der *objectname-Parameter* ist der Name des Objekts, das angezeigt werden soll. Windows Explorer konvertiert den Namen in die entsprechende PIDL und übergibt die PIDL an die [**IPersistFolder::Initialize-Methode**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistfolder-initialize) des neuen Ordnerobjekts.

> [!Note]  
> Der CLSID-Zeichenfolge muss ein Doppelpunktpaar vorangestellt werden (::) oder der Befehl schlägt fehl. Das flag slash-e (/e), das in den beiden oben gezeigten Beispielbefehlszeilen verwendet wird, weist Windows Explorer an, eine Strukturansicht anzuzeigen. Das Flag muss durch ein Komma von den beiden Doppelpunkt getrennt werden. Wenn Sie keine Strukturansicht wünschen, lassen Sie das /e-Flag und das Komma weg.

 

 

 



