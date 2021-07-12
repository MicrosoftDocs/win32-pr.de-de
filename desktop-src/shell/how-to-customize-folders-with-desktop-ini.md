---
description: Anpassen der Darstellung und des Verhaltens eines einzelnen Ordners mit Desktop.ini.
ms.assetid: 0361b7da-bfb3-4880-b982-85d2fe419805
title: Anpassen von Ordnern mit Desktop.ini
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a671b169c4b025683cdd220ee3a920b4d592488
ms.sourcegitcommit: 822413efb4a70dd464e5db4d9e8693ef74f8132f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/09/2021
ms.locfileid: "113581748"
---
# <a name="how-to-customize-folders-with-desktopini"></a>Anpassen von Ordnern mit Desktop.ini

Dateisystemordner werden häufig mit einem Standardsymbol und einer Reihe von Eigenschaften angezeigt, die z. B. angeben, ob der Ordner freigegeben ist. Sie können die Darstellung und das Verhalten eines einzelnen Ordners anpassen, indem Sie eine Desktop.ini-Datei für diesen Ordner erstellen.

## <a name="instructions"></a>Anweisungen

### <a name="using-desktopini-files"></a>Verwenden von Desktop.ini Dateien

Ordner werden normalerweise mit dem Standardordnersymbol angezeigt. Eine häufige Verwendung der Desktop.ini Datei besteht darin, einem Ordner ein benutzerdefiniertes Symbol oder miniaturansichtsbild zuzuweisen. Sie können auch Desktop.ini verwenden, um eine *Infoinfo* zu erstellen, die Informationen zum Ordner anzeigt und einige Aspekte des Ordnerverhaltens steuert, z. B. die Angabe lokalisierter Namen für den Ordner oder Elemente im Ordner.

**Verwenden Sie das folgende Verfahren, um den Stil eines Ordners mit Desktop.ini anzupassen:**

1.  Verwenden Sie [**PathMakeSystemFolder,**](/windows/desktop/api/Shlwapi/nf-shlwapi-pathmakesystemfoldera) um den Ordner zu einem Systemordner zu machen. Dadurch wird das schreibgeschützte Bit im Ordner festgelegt, um anzugeben, dass das für Desktop.ini reservierte spezielle Verhalten aktiviert werden soll. Sie können einen Ordner auch über die Befehlszeile zu einem Systemordner machen, indem Sie **attrib +s** *FolderName verwenden.*
2.  Erstellen Sie eine Desktop.ini-Datei für den Ordner. Sie sollten es als *ausgeblendet* markieren und *als System,* um sicherzustellen, dass es für normale Benutzer ausgeblendet ist.
3.  Stellen Sie sicher, dass die von Ihnen erstellte Desktop.ini-Datei im Unicode-Format vorliegt. Dies ist erforderlich, um die lokalisierten Zeichenfolgen zu speichern, die Benutzern angezeigt werden können.

### <a name="creating-a-desktopini-file"></a>Erstellen einer Desktop.ini-Datei

Die Desktop.ini-Datei ist eine Textdatei, mit der Sie angeben können, wie ein Dateisystemordner angezeigt wird. Der \[ . Im Abschnitt ShellClassInfo \] können Sie die Ansicht des Ordners anpassen, indem Sie mehreren Einträgen Werte zuweisen:

| Wert             | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                    |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **ConfirmFileOp** | Legen Sie diesen Eintrag auf 0 fest, um die Warnung "Sie löschen einen Systemordner" beim Löschen oder Verschieben des Ordners zu vermeiden.                                                                                                                                                                                                                                                                  |
| **NoSharing**     | Wird unter Windows Vista oder höher nicht unterstützt. Legen Sie diesen Eintrag auf 1 fest, um zu verhindern, dass der Ordner freigegeben wird.                                                                                                                                                                                                                                                                       |
| **IconFile**      | Wenn Sie ein benutzerdefiniertes Symbol für den Ordner angeben möchten, legen Sie diesen Eintrag auf den Dateinamen des Symbols fest. Die ICO-Dateinamenerweiterung wird bevorzugt, aber es ist auch möglich, .bmp Dateien oder .exe und .dll Dateien anzugeben, die Symbole enthalten. Wenn Sie einen relativen Pfad verwenden, ist das Symbol für Personen verfügbar, die den Ordner über das Netzwerk anzeigen. Sie müssen auch den **Eintrag IconIndex** festlegen. |
| **IconIndex**     | Legen Sie diesen Eintrag fest, um den Index für ein benutzerdefiniertes Symbol anzugeben. Wenn die **Datei,** die IconFile zugewiesen ist, nur ein einzelnes Symbol enthält, legen **Sie IconIndex** auf 0 fest.                                                                                                                                                                                                                               |
| **InfoTip**       | Legen Sie diesen Eintrag auf eine Informationstextzeichenfolge fest. Sie wird als Infotip angezeigt, wenn der Cursor auf den Ordner zeigt. Wenn der Benutzer auf den Ordner klickt, wird der Informationstext im Informationsblock des Ordners unterhalb der Standardinformationen angezeigt.                                                                                                                      |



 

Die folgenden Abbildungen enthalten den ordner Musik mit einer benutzerdefinierten Desktop.ini-Datei. Der Ordner jetzt:

-   Verfügt über ein benutzerdefiniertes Symbol.
-   Die Warnung "Sie löschen einen Systemordner" wird nicht angezeigt, wenn der Ordner verschoben oder gelöscht wird.
-   Keine gemeinsame Nutzung möglich.
-   Zeigt Informationstext an, wenn der Cursor auf den Ordner zeigt.

Die Ordneroptionen in den folgenden Abbildungen sind so festgelegt, dass ausgeblendete Dateien angezeigt werden, damit Desktop.ini sichtbar ist. Der Ordner sieht wie folgt aus:

![Screenshot des Ordners mit benutzerdefiniertem Symbol](images/webview4.jpg)

Wenn der Cursor auf den Ordner zeigt, wird die Infotip angezeigt.

![Screenshot des Ordners mit infotip](images/webview6.jpg)

Das benutzerdefinierte Symbol ersetzt das Ordnersymbol überall dort, wo der Ordnername angezeigt wird.

![Screenshot des benutzerdefinierten Symbols zum Ersetzen des Ordnersymbols](images/webview5.jpg)

Die folgende desktop.ini Datei wurde verwendet, um den Ordner Musik anzupassen, wie in den vorherigen Abbildungen dargestellt.


```
[.ShellClassInfo]
ConfirmFileOp=0
NoSharing=1
IconFile=Folder.ico
IconIndex=0
InfoTip=Some sensible information.
```



 

 



