---
title: Verwenden des Ressourcencompilers (RC-Befehlszeile)
description: Um RC zu starten, verwenden Sie den folgenden Befehl.
ms.assetid: da087e15-ecb5-4d03-b534-be872cf7d8b6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c34e24fdf7b9b648a9baf9c6db8981f05d5434ef
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103948668"
---
# <a name="using-rc-the-rc-command-line"></a>Verwenden des Ressourcencompilers (RC-Befehlszeile)

Um RC zu starten, verwenden Sie den folgenden Befehl.

**RC** \[ *Optionen* \] *Skriptdatei*

Der *Skriptdatei* Parameter gibt den Namen der Ressourcen Definitionsdatei an, die die Namen, Typen, Dateinamen und Beschreibungen der zu kompilierenden Ressourcen enthält.

RC kann separate Ressourcen Dateien für Anwendungen generieren, die sowohl sprachneutrale als auch sprachspezifische Ressourcen haben. Entwickler können eine [Ressourcen Konfigurationsdatei](/windows/desktop/Intl/preparing-resources) verwenden oder Befehlszeilenoptionen festlegen, um auszuwählen, welche Ressourcentypen und-Elemente nicht lokalisierbare Ressourcen der [sprach neutralen Datei (LN)](/windows/desktop/Intl/mui-resource-management) sind und welche lokalisierbare Ressourcen von sprachspezifischen MUI-Dateien sind. Weitere Informationen finden Sie unter [mehrsprachige Benutzeroberfläche](/windows/desktop/Intl/multilingual-user-interface).

Der *options* -Parameter kann eine oder mehrere der folgenden Befehlszeilenoptionen sein.

## <a name="options"></a>Optionen

<dl> <dt>

<span id="__"></span>**/?**
</dt> <dd>

Zeigt eine Liste der Befehlszeilenoptionen an.

</dd> <dt>

<span id="_c"></span><span id="_C"></span>**/c**
</dt> <dd>

Definiert eine Codepage, die von der NLS-Konvertierung verwendet wird.

</dd> <dt>

<span id="_d"></span><span id="_D"></span>**/d**
</dt> <dd>

Definiert ein Symbol für den Präprozessor, der mit der [**\# ifdef**](-ifdef.md) -Direktive getestet werden kann.

</dd> <dt>

<span id="_fm_mresname"></span><span id="_FM_MRESNAME"></span>**/FM** - *mresname*
</dt> <dd>

RC erstellt eine sprachneutrale. RES-Datei und eine sprachabhängige (MUI). RES-Datei mithilfe der *Skriptdatei*. Diese Option muss in Verbindung mit der Option **/FO** *Resname* verwendet werden. RC benennt den sprach neutralen Namen. Res file *Resname. res* und benennt die sprachabhängige (MUI). Res-Datei ( *mresname. res*).

**Windows Server 2003 und Windows XP/2000:** Diese Option ist nicht verfügbar, ohne auch die [**loadmuilibrary**](/windows/desktop/api/muiload/nf-muiload-loadmuilibrarya) -Funktion und die [**fremuilibrary**](/windows/desktop/api/muiload/nf-muiload-freemuilibrary) -Funktion in einem aktualisierten System zu verwenden.

</dd> <dt>

<span id="_fo_resname"></span><span id="_FO_RESNAME"></span>**/FO** *Resname*
</dt> <dd>

RC erstellt einen. RES Datei mit dem *Namen Resname* unter Verwendung der *Skriptdatei*.

Wenn die Option **/FM** *mresname* ebenfalls festgelegt ist, erstellt RC eine sprachneutrale. RES-Datei und eine sprachabhängige (MUI). RES-Datei.

**Windows Server 2003 und Windows XP/2000:** Diese Option ist nicht verfügbar, ohne auch die [**loadmuilibrary**](/windows/desktop/api/muiload/nf-muiload-loadmuilibrarya) -Funktion und die [**fremuilibrary**](/windows/desktop/api/muiload/nf-muiload-freemuilibrary) -Funktion in einem aktualisierten System zu verwenden.

</dd> <dt>

<span id="_g1"></span><span id="_G1"></span>**/G1**
</dt> <dd>

Wenn/G1 festgelegt ist, generiert RC eine MUI-Datei, wenn die einzige lokalisierbare Ressource, die in der MUI-Datei enthalten ist, eine Versions Ressource ist. Wenn/G1 nicht festgelegt ist, generiert RC keine MUI-Datei, wenn die einzige lokalisierbare Ressource, die in der MUI-Datei enthalten ist, eine Versions Ressource ist.

</dd> <dt>

<span id="_h"></span><span id="_H"></span>**/h**
</dt> <dd>

Zeigt die Liste der Befehlszeilenoptionen an.

</dd> <dt>

<span id="_I"></span><span id="_i"></span>**/I**
</dt> <dd>

Durchsucht das angegebene Verzeichnis, bevor die von der INCLUDE-Umgebungsvariablen angegebenen Verzeichnisse durchsucht werden.

</dd> <dt>

<span id="_j__loctype"></span><span id="_J__LOCTYPE"></span>**/j** *loctype*
</dt> <dd>

Lokalisierbare Ressourcentypen RC stellt die sprachabhängige (MUI) dar. RES-Datei. Wenn die **/q** -Option ebenfalls festgelegt ist, wird diese Option ignoriert, und die Informationen in der RC-Konfigurationsdatei haben Vorrang.

**Windows Server 2003 und Windows XP/2000:** Diese Option ist nicht verfügbar, ohne auch die [**loadmuilibrary**](/windows/desktop/api/muiload/nf-muiload-loadmuilibrarya) -Funktion und die [**fremuilibrary**](/windows/desktop/api/muiload/nf-muiload-freemuilibrary) -Funktion in einem aktualisierten System zu verwenden.

</dd> <dt>

<span id="_k_overtype"></span><span id="_K_OVERTYPE"></span>**/k** *über Schreib*
</dt> <dd>

Überlappende Ressourcentypen, die RC in beide Sprachen neutral stellen. RES und die sprachabhängige (MUI). RES-Dateien. Die von der **/k** -Option angegebenen Ressourcentypen müssen eine Teilmenge der von der **/j** -Option angegebenen Ressourcentypen sein. Zum Beispiel? J2? J3? "K3" gibt an, dass RC den Ressourcentyp 3 in den sprach neutralen und sprach abhängigen Dateien (MUI) platziert. Wenn die **/q** -Option ebenfalls festgelegt ist, wird diese Option ignoriert, und die Informationen in der RC-Konfigurationsdatei haben Vorrang.

**Windows Server 2003 und Windows XP/2000:** Diese Option ist nicht verfügbar, ohne auch die [**loadmuilibrary**](/windows/desktop/api/muiload/nf-muiload-loadmuilibrarya) -Funktion und die [**fremuilibrary**](/windows/desktop/api/muiload/nf-muiload-freemuilibrary) -Funktion in einem aktualisierten System zu verwenden.

</dd> <dt>

<span id="_l_langid"></span><span id="_L_LANGID"></span>**/l** *LangID*
</dt> <dd>

Gibt die Standardsprache für die Kompilierung an. Beispielsweise entspricht-L409 dem einschließen der folgenden-Anweisung am Anfang der Ressourcen Skriptdatei: `LANGUAGE LANG_ENGLISH,SUBLANG_ENGLISH_US`

Weitere Informationen finden Sie unter [sprach](/windows/desktop/Intl/language-identifiers)Bezeichner.

</dd> <dt>

<span id="_n"></span><span id="_N"></span>**/n**
</dt> <dd>

Null beendet alle Zeichen folgen in der Zeichen folgen Tabelle.

</dd> <dt>

<span id="_q_Mui.RCConfig"></span><span id="_q_mui.rcconfig"></span><span id="_Q_MUI.RCCONFIG"></span>**/q** *MUI. rcconfig*
</dt> <dd>

Eine RC-Konfigurationsdatei, die dem Format der RC-Konfigurationsdatei folgt. Das Format der RC-Konfigurationsdatei ermöglicht es Komponenten, Ressourcen Informationen, wie z. b. Ressourcen Versionsverwaltung, MUI-Dateipfad, Ressourcentypen und Elemente, selbst zu beschreiben. Mit dieser Datei wird angegeben, welche Ressourcen in die sprachneutrale Sprache gelangen. RES-Datei und welche Ressourcen in den sprach abhängigen (MUI). RES-Datei. Diese Option und die Informationen in der RC-Konfigurationsdatei überschreiben die Befehlszeilenoptionen **/j** und **/k**.

**Windows Server 2003 und Windows XP/2000:** Diese Option ist nicht verfügbar, ohne auch die [**loadmuilibrary**](/windows/desktop/api/muiload/nf-muiload-loadmuilibrarya) -Funktion und die [**fremuilibrary**](/windows/desktop/api/muiload/nf-muiload-freemuilibrary) -Funktion in einem aktualisierten System zu verwenden.

</dd> <dt>

<span id="_r"></span><span id="_R"></span>**/r**
</dt> <dd>

Ignoriert. Wird aus Gründen der Kompatibilität mit vorhandenen Makefiles bereitgestellt.

</dd> <dt>

<span id="_u"></span><span id="_U"></span>**/u**
</dt> <dd>

Definiert ein Symbol für den Präprozessor.

</dd> <dt>

<span id="_v"></span><span id="_V"></span>**/v**
</dt> <dd>

Zeigt Meldungen an, die den Fortschritt des Compilers melden.

</dd> <dt>

<span id="_x"></span><span id="_X"></span>**/x**
</dt> <dd>

Verhindert, dass RC die include-Umgebungsvariable bei der Suche nach Header Dateien oder Ressourcen Dateien prüft.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Bei den Optionen wird die Groß-/Kleinschreibung nicht beachtet, und ein Bindestrich (-) kann anstelle eines Schrägstrichs (/) verwendet werden. Sie können Optionen für einzelne Buchstaben kombinieren, wenn Sie keine zusätzlichen Parameter benötigen.

RC generiert in den folgenden Fällen keine MUI-Datei.

-   In der RC-Datei sind keine lokalisierbaren Ressourcen vorhanden.
-   Die einzige in der RC-Datei angegebene Ressourcen Sprachen-ID ist neutral (0x0).
-   Die RC-Datei verfügt über Ressourcen, die in mehr als einer Sprache angegeben sind. Die Ausnahme besteht darin, dass die RC-Datei zwei Sprachen enthält und eine Sprache neutral (0x0) ist, dass RC eine MUI-Datei generiert.

Weitere Informationen finden Sie unter den folgenden Themen:

-   [Definieren von Namen für den Präprozessor](defining-names-for-the-preprocessor.md)
-   [Umbenennen der kompilierten Ressourcen Datei](renaming-the-compiled-resource-file.md)
-   [Dateien werden gesucht](searching-for-files.md)
-   [Anzeigen von Statusmeldungen](displaying-progress-messages.md)
-   [RC-Diagnosemeldungen](rc-diagnostic-messages.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Multilingual User Interface](/windows/desktop/Intl/multilingual-user-interface)
</dt> </dl>

 

 