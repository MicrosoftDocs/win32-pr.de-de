---
description: Anpassen der Darstellung und des Verhaltens eines einzelnen Ordners mit Desktop.ini.
ms.assetid: 0361b7da-bfb3-4880-b982-85d2fe419805
title: Anpassen von Ordnern mit Desktop.ini
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23ec216bedfdee16e26f87070a0196d77a8db12c802d97b1449cd78001f51a16
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117859832"
---
# <a name="how-to-customize-folders-with-desktopini"></a>Anpassen von Ordnern mit Desktop.ini

Dateisystemordner werden häufig mit einem Standardsymbol und einer Reihe von Eigenschaften angezeigt, die z. B. angeben, ob der Ordner freigegeben wird. Sie können die Darstellung und das Verhalten eines einzelnen Ordners anpassen, indem Sie eine Desktop.ini für diesen Ordner erstellen.

## <a name="instructions"></a>Anweisungen

### <a name="using-desktopini-files"></a>Verwenden Desktop.ini Dateien

Ordner werden normalerweise mit dem Standardordnersymbol angezeigt. Eine gängige Verwendung der Desktop.ini ist das Zuweisen eines benutzerdefinierten Symbols oder Miniaturbilds zu einem Ordner. Sie können auch Desktop.ini verwenden,  um eine Infotip zu erstellen, die Informationen zum Ordner anzeigt und einige Aspekte des Ordnerverhaltens steuert, z. B. die Angabe lokalisierter Namen für den Ordner oder die Elemente im Ordner.

**Verwenden Sie das folgende Verfahren, um den Stil eines Ordners mit Desktop.ini:**

1.  Verwenden [**Sie PathMakeSystemFolder,**](/windows/desktop/api/Shlwapi/nf-shlwapi-pathmakesystemfoldera) um den Ordner zu einem Systemordner zu machen. Dadurch wird das schreibgeschützte Bit für den Ordner so angegeben, dass das spezielle Verhalten aktiviert werden soll, Desktop.ini aktiviert werden soll. Sie können einen Ordner auch über die Befehlszeile zu einem Systemordner machen, indem Sie **attrib +s** *FolderName verwenden.*
2.  Erstellen Sie Desktop.ini -Datei für den Ordner. Sie sollten sie als ausgeblendet *und* als *System markieren,* um sicherzustellen, dass sie für normale Benutzer ausgeblendet ist.
3.  Stellen Sie sicher, Desktop.ini die von Ihnen erstellten Dateien im Unicode-Format vorliegen. Dies ist erforderlich, um die lokalisierten Zeichenfolgen zu speichern, die Benutzern angezeigt werden können.

### <a name="creating-a-desktopini-file"></a>Erstellen einer Desktop.ini Datei

Die Desktop.ini ist eine Textdatei, mit der Sie angeben können, wie ein Dateisystemordner angezeigt wird. Die \[ . Mit dem Abschnitt ShellClassInfo können Sie die Ansicht des Ordners anpassen, indem \] Sie mehreren Einträgen Werte zuweisen:

| Wert             | Beschreibung                                                                                                                                                                                                                                                                                                                                                                    |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **ConfirmFileOp** | Legen Sie diesen Eintrag auf 0 fest, um eine Warnung "Sie löschen einen Systemordner" beim Löschen oder Verschieben des Ordners zu vermeiden.                                                                                                                                                                                                                                                                  |
| **NoSharing**     | Wird unter Windows Vista oder höher nicht unterstützt. Legen Sie diesen Eintrag auf 1 fest, um zu verhindern, dass der Ordner freigegeben wird.                                                                                                                                                                                                                                                                       |
| **IconFile**      | Wenn Sie ein benutzerdefiniertes Symbol für den Ordner angeben möchten, legen Sie diesen Eintrag auf den Dateinamen des Symbols fest. Die ICO-Dateinamenerweiterung wird bevorzugt, aber es ist auch möglich, .bmp-Dateien oder .exe- und .dll-Dateien anzugeben, die Symbole enthalten. Wenn Sie einen relativen Pfad verwenden, ist das Symbol für Personen verfügbar, die den Ordner über das Netzwerk anzeigen. Sie müssen auch den **IconIndex-Eintrag** festlegen. |
| **IconIndex**     | Legen Sie diesen Eintrag fest, um den Index für ein benutzerdefiniertes Symbol anzugeben. Wenn die Datei, die **IconFile zugewiesen** ist, nur ein einzelnes Symbol enthält, legen **Sie IconIndex auf** 0 fest.                                                                                                                                                                                                                               |
| **InfoTip**       | Legen Sie diesen Eintrag auf eine Informationstextzeichenfolge fest. Sie wird als Infotip angezeigt, wenn der Cursor auf den Ordner zeigt. Wenn der Benutzer auf den Ordner klickt, wird der Informationstext im Informationsblock des Ordners unterhalb der Standardinformationen angezeigt.                                                                                                                      |



 

Die folgenden Abbildungen zeigen den ordner Musik mit einer benutzerdefinierten Desktop.ini Datei. Der Ordner jetzt:

-   Verfügt über ein benutzerdefiniertes Symbol.
-   Zeigt keine Warnung "Sie löschen einen Systemordner" an, wenn der Ordner verschoben oder gelöscht wird.
-   Keine gemeinsame Nutzung möglich.
-   Zeigt Informationstext an, wenn der Cursor auf den Ordner zeigt.

Die Ordneroptionen in den folgenden Abbildungen werden so festgelegt, dass ausgeblendete Dateien angezeigt werden, damit Desktop.ini angezeigt wird. Der Ordner sieht wie hier aus:

![Screenshot des Ordners mit benutzerdefiniertem Symbol](images/webview4.jpg)

Wenn der Cursor auf den Ordner zeigt, wird die Infotip angezeigt.

![Screenshot des Ordners mit einer Infotip](images/webview6.jpg)

Das benutzerdefinierte Symbol ersetzt das Ordnersymbol überall dort, wo der Ordnername angezeigt wird.

![Screenshot des benutzerdefinierten Symbols zum Ersetzen des Ordnersymbols](images/webview5.jpg)

Die folgende desktop.ini wurde verwendet, um den ordner Musik anzupassen, wie in den obigen Abbildungen zu sehen.


```
[.ShellClassInfo]
ConfirmFileOp=0
NoSharing=1
IconFile=Folder.ico
IconIndex=0
InfoTip=Some sensible information.
```



 

 



