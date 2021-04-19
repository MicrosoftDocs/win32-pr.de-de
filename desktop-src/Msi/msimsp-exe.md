---
description: Die empfohlene Methode zum Erstellen eines Patchpakets ist die Verwendung von Tools zur Patcherstellung, wie z. b. Msimsp.exe und Patchwiz.dll. Das Msimsp.exe Tool ist nur in den Windows SDK Komponenten für Windows Installer Entwickler verfügbar.
ms.assetid: fa8e9d68-3db1-4d17-aa99-2ca0ed421c7a
title: Msimsp.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1810fd0c544695742273bbb0e63b22138529c129
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106364301"
---
# <a name="msimspexe"></a>Msimsp.exe

Die empfohlene Methode zum Erstellen eines Patchpakets ist die Verwendung von Tools zur Patcherstellung, wie z. b. Msimsp.exe und [Patchwiz.dll](patchwiz-dll.md). Das Msimsp.exe Tool ist nur in den [Windows SDK Komponenten für Windows Installer Entwickler](platform-sdk-components-for-windows-installer-developers.md)verfügbar.

Msimsp.exe ist eine ausführbare Datei, die [Patchwiz.dll](patchwiz-dll.md)aufruft. Das Tool kann zum Erstellen eines Patchpakets verwendet werden, indem der Pfad zur Eigenschaften Datei für die Patcherstellung (PCP-Datei) und der Pfad zum Patchpaket, das erstellt wird, übergeben werden. Msimsp. Ex kann auch verwendet werden, um eine Protokolldatei zu erstellen und einen temporären Ordner anzugeben, in dem die Transformationen, Schränke und Dateien, die zum Erstellen des Patchpakets verwendet werden, gespeichert werden.

Die Befehlszeilen Syntax für Msimsp.exe lautet wie folgt:

**Msimsp.exe-s-Pfad** *\[ zu pcp- \] Datei* **-p** *\[ Pfad zur MSP- \] Datei* **{Optionen}**

Bei den Befehlszeilenoptionen wird die Groß-/Kleinschreibung nicht beachtet, und es können Schrägstriche anstelle eines Bindestrichs verwendet werden. Wenn keine Optionen angegeben sind, zeigt Msimsp.exe die aktuellen Werte der Eigenschaften der Zusammenfassungs Informationen an.

<dl> <dt>

<span id="-s_path_to_.pcp_file_"></span><span id="-S_PATH_TO_.PCP_FILE_"></span>**-s**_\[ Pfad zur PCP-Datei \]_
</dt> <dd>

Dies ist erforderlich, und es muss der Pfad zur Eigenschaften Datei für die Patcherstellung (PCP-Erweiterung) befolgt werden. Weitere Informationen finden Sie unter [PatchWiz.dll](patchwiz-dll.md).

</dd> <dt>

<span id="-ppath_to_.msp_file"></span><span id="-PPATH_TO_.MSP_FILE"></span>**-p**_Pfad zur MSP-Datei_
</dt> <dd>

Dies ist erforderlich, und es folgt der Pfad zum Patchpaket, das erstellt wird (Erweiterung. msp).

</dd> <dt>

<span id="-fpath_to_temporary_folder"></span><span id="-FPATH_TO_TEMPORARY_FOLDER"></span>**-f**_Pfad zum temporären Ordner_
</dt> <dd>

Dies ist optional. Gefolgt vom Pfad zum temporären Ordner. Der Standard Speicherort ist% tmp% \\ ~ PCW \_ tmp. tmp \\ .

</dd> <dt>

<span id="-k"></span><span id="-K"></span>**-k**
</dt> <dd>

Dies ist optional. Schlägt fehl, wenn der temporäre Ordner bereits vorhanden ist.

</dd> <dt>

<span id="-lpath_to_log_file"></span><span id="-LPATH_TO_LOG_FILE"></span>**-l**_Pfad zur Protokolldatei_
</dt> <dd>

Dies ist optional. Gefolgt vom Pfad zur Protokolldatei, in der der patcherstellungs Prozess und die Fehler beschrieben werden. Weitere Informationen finden Sie unter [Rückgabewerte für uikreatepatchpackage](return-values-for-uicreatepatchpackage.md).

</dd> <dt>

<span id="-lppath_to_log_file_with_performance_data"></span><span id="-LPPATH_TO_LOG_FILE_WITH_PERFORMANCE_DATA"></span>**-LP**_Pfad zur Protokolldatei mit Leistungsdaten_
</dt> <dd>

Dies ist optional. Gefolgt vom Pfad zur Protokolldatei, in der der patcherstellungs Prozess und die Fehler beschrieben werden. Mit dieser Option werden Leistungsdaten in die Protokolldatei geschrieben. Diese Option erfordert Version 4,0 von Patchwiz.dll.

</dd> <dt>

<span id="-d"></span><span id="-D"></span>**-d**
</dt> <dd>

Dies ist optional. Zeigt ein Dialogfeld an, wenn die Patcherstellung erfolgreich abgeschlossen wurde.

</dd> <dt>

<span id="-_"></span>**-?**
</dt> <dd>

Mit diesem Befehl wird die Befehlszeilenhilfe angezeigt.

</dd> </dl>

> [!Note]
> Msimsp.exe kann bei der Aufruf Makecab.exe einen Fehler verursachen, wenn in der Datei Spalte der [Dateitabelle](file-table.md) des Installationspakets Werte vorhanden sind, die sich nur in der Groß-/Kleinschreibung unterscheiden. Bei Windows Installer wird die Groß-/Kleinschreibung beachtet, und es wird nur ein Installationspaket wie in der folgenden Tabelle zugelassen, wenn Comp1 und Comp2 in verschiedenen Verzeichnissen installiert sind. In diesem Szenario können Sie jedoch Msimsp.exe oder [Patchwiz.dll](patchwiz-dll.md) nicht verwenden, um einen Patch für das Paket zu generieren, da Msimsp.exe und Patchwiz.dll Makecab.exe, die Groß-/Kleinschreibung nicht beachtet.
> 
> Vermeiden Sie das Erstellen eines Installationspakets, z. b. der folgenden partiellen [Dateitabelle](file-table.md).
> 
> | File       | Komponente\_ | FileName   |
> |------------|-------------|------------|
> | ReadMe.txt | Comp1       | ReadMe.txt |
> | ReadMe.txt | Comp2       | ReadMe.txt |


## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen eines Patchpakets](creating-a-patch-package.md)
</dt> <dt>

[Beispiel für ein kleines Update-Patching](a-small-update-patching-example.md)
</dt> <dt>

[Entwicklungs Tools für Windows Installer](windows-installer-development-tools.md)
</dt> <dt>

[Veröffentlichte Versionen, Tools und verteilbare Dateien](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



