---
description: Die empfohlene Methode zum Generieren eines Patchpakets ist die Verwendung von Tools zur Patcherstellung wie Msimsp.exe und Patchwiz.dll. Das Msimsp.exe-Tool ist nur in den sdk-Komponenten Windows für Windows Installer-Entwickler verfügbar.
ms.assetid: fa8e9d68-3db1-4d17-aa99-2ca0ed421c7a
title: Msimsp.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa82f2fbefc9046877f4f98cf4a3c126d94e6542b60076f0491bd0f311ee00a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118627797"
---
# <a name="msimspexe"></a>Msimsp.exe

Die empfohlene Methode zum Generieren eines Patchpakets ist die Verwendung von Tools zur Patcherstellung wie Msimsp.exe und [Patchwiz.dll. ](patchwiz-dll.md) Das Msimsp.exe-Tool ist nur in den [SDK Windows komponenten für Windows Installer-Entwickler verfügbar.](platform-sdk-components-for-windows-installer-developers.md)

Msimsp.exe ist eine ausführbare Datei, die [Patchwiz.dll. ](patchwiz-dll.md) Das Tool kann verwendet werden, um ein Patchpaket zu erstellen, indem der Pfad zu einer Eigenschaftendatei für die Patcherstellung (PCP-Datei) und der Pfad zum Patchpaket übergeben wird, das erstellt wird. Msimsp.ex kann auch verwendet werden, um eine Protokolldatei zu erstellen und einen temporären Ordner anzugeben, in dem die Transformationen, Schränken und Dateien, die zum Erstellen des Patchpakets verwendet werden, gespeichert werden.

Die Befehlszeilensyntax für Msimsp.exe ist:

**Msimsp.exe -s** *\[ Pfad zur PCP-Datei \]* **-p** *\[ pfad \] zur MSP-Datei* **{options}**

Bei den Befehlszeilenoptionen wird die Schreibung nicht beachtet, und anstelle eines Bindestrichs können Schrägstrichtrennzeichen verwendet werden. Wenn keine Optionen angegeben sind, Msimsp.exe die aktuellen Werte der Zusammenfassungsinformationseigenschaften angezeigt.

<dl> <dt>

<span id="-s_path_to_.pcp_file_"></span><span id="-S_PATH_TO_.PCP_FILE_"></span>**-s**_\[ Pfad zur PCP-Datei \]_
</dt> <dd>

Dies ist erforderlich, und es muss der Pfad zur Eigenschaftendatei für die Patcherstellung (ERWEITERUNG PCP) folgen. Weitere Informationen finden Sie unter [PatchWiz.dll](patchwiz-dll.md).

</dd> <dt>

<span id="-ppath_to_.msp_file"></span><span id="-PPATH_TO_.MSP_FILE"></span>**-p Pfad**_zur MSP-Datei_
</dt> <dd>

Dies ist erforderlich, gefolgt vom Pfad zum Patchpaket, das erstellt wird (MSP-Erweiterung).

</dd> <dt>

<span id="-fpath_to_temporary_folder"></span><span id="-FPATH_TO_TEMPORARY_FOLDER"></span>**-f Pfad**_zum temporären Ordner_
</dt> <dd>

Optional. Gefolgt vom Pfad zum temporären Ordner. Der Standardspeicherort ist %TMP% \\ ~pcw \_ tmp.tmp \\ .

</dd> <dt>

<span id="-k"></span><span id="-K"></span>**-k**
</dt> <dd>

Optional. Fehler, wenn der temporäre Ordner bereits vorhanden ist.

</dd> <dt>

<span id="-lpath_to_log_file"></span><span id="-LPATH_TO_LOG_FILE"></span>**-l**_Pfad zur Protokolldatei_
</dt> <dd>

Optional. Gefolgt vom Pfad zur Protokolldatei, in der der Patcherstellungsprozess und Fehler beschrieben werden. Weitere Informationen finden Sie unter [Rückgabewerte für UiCreatePatchPackage.](return-values-for-uicreatepatchpackage.md)

</dd> <dt>

<span id="-lppath_to_log_file_with_performance_data"></span><span id="-LPPATH_TO_LOG_FILE_WITH_PERFORMANCE_DATA"></span>**-lp Pfad**_zur Protokolldatei mit Leistungsdaten_
</dt> <dd>

Optional. Gefolgt vom Pfad zur Protokolldatei, in der der Patcherstellungsprozess und Fehler beschrieben werden. Diese Option schreibt Leistungsdaten in die Protokolldatei. Diese Option erfordert Version 4.0 von Patchwiz.dll.

</dd> <dt>

<span id="-d"></span><span id="-D"></span>**-d**
</dt> <dd>

Optional. Zeigt ein Dialogfeld an, wenn die Patcherstellung erfolgreich abgeschlossen wurde.

</dd> <dt>

<span id="-_"></span>**-?**
</dt> <dd>

Mit diesem Befehl wird die Befehlszeilenhilfe angezeigt.

</dd> </dl>

> [!Note]
> Msimsp.exe beim Aufrufen von Makecab.exe fehler, wenn in der Datei -Spalte [](file-table.md) der Tabelle Datei des Installationspakets Werte enthalten sind, die sich nur nach Fall unterscheiden. Windows Beim Installationsprogramm wird die Kleinschreibung beachtet, und ein Installationspaket wie in der folgenden Tabelle ist nur dann möglich, wenn Comp1 und Comp2 in verschiedenen Verzeichnissen installiert sind. In diesem Szenario können Sie Msimsp.exe oder [Patchwiz.dll](patchwiz-dll.md) jedoch nicht verwenden, um einen Patch für das Paket zu generieren, da Msimsp.exe und Patchwiz.dll Makecab.exe aufrufen, bei dem die Groß-/Kleinschreibung nicht beachtet wird.
> 
> Vermeiden Sie das Erstellen eines Installationspakets, z. B. die folgende [partielle Dateitabelle.](file-table.md)
> 
> | Datei       | Komponente\_ | FileName   |
> |------------|-------------|------------|
> | ReadMe.txt | Comp1       | ReadMe.txt |
> | ReadMe.txt | Comp2       | ReadMe.txt |


## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen eines Patchpakets](creating-a-patch-package.md)
</dt> <dt>

[Ein Beispiel für ein kleines Updatepatching](a-small-update-patching-example.md)
</dt> <dt>

[Windows Installer-Entwicklungstools](windows-installer-development-tools.md)
</dt> <dt>

[Veröffentlichte Versionen, Tools und Verteilbare Versionen](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



