---
description: Anpassen des Erscheinungs Bilds und Verhaltens eines einzelnen Ordners mit Desktop.ini.
ms.assetid: 0361b7da-bfb3-4880-b982-85d2fe419805
title: Vorgehensweise beim Anpassen von Ordnern mit Desktop.ini
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eaac3e6a96257e63b5e4210da0aa6e6e1db77eaf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104560738"
---
# <a name="how-to-customize-folders-with-desktopini"></a>Vorgehensweise beim Anpassen von Ordnern mit Desktop.ini

Dateisystem Ordner werden häufig mit einem Standard Symbol und einem Satz von Eigenschaften angezeigt, die angeben, ob der Ordner freigegeben ist. Sie können die Darstellung und das Verhalten eines einzelnen Ordners anpassen, indem Sie eine Desktop.ini-Datei für diesen Ordner erstellen.

## <a name="instructions"></a>Instructions

### <a name="using-desktopini-files"></a>Verwenden von Desktop.ini Dateien

Ordner werden normalerweise mit dem Symbol "Standardordner" angezeigt. Die Desktop.ini Datei wird häufig verwendet, um einem Ordner ein benutzerdefiniertes Symbol oder Miniaturbild zuzuweisen. Sie können auch Desktop.ini verwenden, um einen *Infotipp* zu erstellen, der Informationen zum Ordner anzeigt und einige Aspekte des Ordners des Ordners steuert, z. b. das angeben lokalisierter Namen für den Ordner oder die Elemente im Ordner.

**Verwenden Sie das folgende Verfahren, um den Stil eines Ordners mit Desktop.ini anzupassen:**

1.  Verwenden Sie [**pathmakesystemfolder**](/windows/desktop/api/Shlwapi/nf-shlwapi-pathmakesystemfoldera) , um den Ordner zu einem Systemordner zu machen. Dadurch wird das schreibgeschützte Bit für den Ordner festgelegt, um anzugeben, dass das für Desktop.ini reservierte spezielle Verhalten aktiviert werden soll. Sie können einen Ordner auch über die Befehlszeile in einem Ordner erstellen, indem Sie **atzb + s** *FolderName* verwenden.
2.  Erstellen Sie eine Desktop.ini-Datei für den Ordner. Sie sollten Sie als *ausgeblendet* und *System* markieren, um sicherzustellen, dass Sie für normale Benutzer ausgeblendet ist.
3.  Stellen Sie sicher, dass die von Ihnen erstellte Desktop.ini Datei im Unicode-Format vorliegt. Dies ist erforderlich, um die lokalisierten Zeichen folgen zu speichern, die Benutzern angezeigt werden können.

### <a name="creating-a-desktopini-file"></a>Erstellen einer Desktop.ini Datei

Die Desktop.ini-Datei ist eine Textdatei, mit der Sie angeben können, wie ein Dateisystem Ordner angezeigt wird. Die \[ . Der Abschnitt "shellclassinfo" \] ermöglicht das Anpassen der Ordneransicht durch Zuweisen von Werten zu mehreren Einträgen:

|                   |                                                                                                                                                                                                                                                                                                                                                                                |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Eingabe**         | **Wert**                                                                                                                                                                                                                                                                                                                                                                      |
| **Confirmfileop** | Legen Sie diesen Eintrag auf 0 fest, um beim Löschen oder Verschieben des Ordners die Warnung "Sie können einen System Ordner löschen" zu vermeiden.                                                                                                                                                                                                                                                                  |
| **Nosharing**     | Wird unter Windows Vista oder höher nicht unterstützt. Legen Sie diesen Eintrag auf 1 fest, um zu verhindern, dass der Ordner freigegeben wird.                                                                                                                                                                                                                                                                       |
| **IconFile**      | Wenn Sie ein benutzerdefiniertes Symbol für den Ordner angeben möchten, legen Sie diesen Eintrag auf den Dateinamen des Symbols fest. Die Dateinamenerweiterung. ico wird bevorzugt, aber es ist auch möglich, BMP-Dateien, exe-und dll-Dateien anzugeben, die Symbole enthalten. Wenn Sie einen relativen Pfad verwenden, steht das Symbol den Personen zur Verfügung, die den Ordner über das Netzwerk anzeigen. Sie müssen auch den Eintrag **IconIndex** festlegen. |
| **IconIndex**     | Legen Sie diesen Eintrag fest, um den Index für ein benutzerdefiniertes Symbol anzugeben. Wenn die **IconFile** zugewiesene Datei nur ein einzelnes Symbol enthält, legen Sie **IconIndex** auf 0 fest.                                                                                                                                                                                                                               |
| **InfoTip**       | Legen Sie diesen Eintrag auf eine Informationstext Zeichenfolge fest. Sie wird als InfoTipp angezeigt, wenn der Cursor auf den Ordner zeigt. Wenn der Benutzer auf den Ordner klickt, wird der Informationstext im Informationsblock des Ordners unter den Standardinformationen angezeigt.                                                                                                                      |



 

Die folgenden Abbildungen sind der Ordner "Music" mit einer benutzerdefinierten Desktop.ini Datei. Jetzt der Ordner:

-   Verfügt über ein benutzerdefiniertes Symbol.
-   Wenn der Ordner verschoben oder gelöscht wird, wird von keine Warnung angezeigt, dass ein System Ordner gelöscht wird.
-   Keine gemeinsame Nutzung möglich.
-   Zeigt Informationstext an, wenn der Cursor auf den Ordner zeigt.

Die Ordneroptionen in den folgenden Abbildungen sind so festgelegt, dass ausgeblendete Dateien angezeigt werden, damit Desktop.ini sichtbar ist. Der Ordner sieht wie folgt aus:

![Screenshot des Ordners mit benutzerdefiniertem Symbol](images/webview4.jpg)

Wenn der Cursor über den Ordner bewegt wird, wird der InfoTipp angezeigt.

![Screenshot des Ordners mit einem InfoTipp](images/webview6.jpg)

Das benutzerdefinierte Symbol ersetzt das Ordnersymbol, wo der Ordnername angezeigt wird.

![Screenshot des benutzerdefinierten Symbols zum Ersetzen des Ordner Symbols](images/webview5.jpg)

Die folgende desktop.ini Datei wurde verwendet, um den Musik Ordner anzupassen, wie in den vorherigen Abbildungen gezeigt.


```
[.ShellClassInfo]
ConfirmFileOp=0
NoSharing=1
IconFile=Folder.ico
IconIndex=0
InfoTip=Some sensible information.
```



 

 



