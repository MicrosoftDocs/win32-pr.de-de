---
title: Verwenden des Ressourcencompilers (RC-Befehlszeile)
description: Verwenden Sie den folgenden Befehl, um RC zu starten.
ms.assetid: da087e15-ecb5-4d03-b534-be872cf7d8b6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e560ebee4312dccc2463caf123f05a5ad9831cd293c9976350e6de7ee13cb64a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971919"
---
# <a name="using-rc-the-rc-command-line"></a>Verwenden des Ressourcencompilers (RC-Befehlszeile)

Verwenden Sie den folgenden Befehl, um RC zu starten.

**RC** \[ *Optionen* \] *script-file*

Der *script-file-Parameter* gibt den Namen der Ressourcendefinitionsdatei an, die die Namen, Typen, Dateinamen und Beschreibungen der zu kompilierenden Ressourcen enthält.

RC kann separate Ressourcendateien für Anwendungen generieren, die sowohl sprachneutrale als auch sprachspezifische Ressourcen aufweisen. Entwickler können eine [Ressourcenkonfigurationsdatei](/windows/desktop/Intl/preparing-resources) verwenden oder Befehlszeilenoptionen festlegen, um auszuwählen, welche Ressourcentypen und Elemente nicht lokalisierbare Ressourcen der [sprachneutralen Datei (LN)](/windows/desktop/Intl/mui-resource-management) sind und welche lokalisierbaren Ressourcen sprachspezifischer LANGUAGE-Dateien sind. Weitere Informationen finden Sie im [mehrsprachige Benutzeroberfläche](/windows/desktop/Intl/multilingual-user-interface).

Der *Optionsparameter* kann eine oder mehrere der folgenden Befehlszeilenoptionen sein.

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

Definiert ein Symbol für den Präprozessor, das Sie mit der [**\# ifdef-Direktive**](-ifdef.md) testen können.

</dd> <dt>

<span id="_fm_mresname"></span><span id="_FM_MRESNAME"></span>**/fm** *mresname*
</dt> <dd>

RC erstellt eine sprachneutrale . RES-Datei und eine sprachabhängige (LANGUAGE-dependent, LANGUAGE) . *RES-Datei mithilfe* der Skriptdatei . Diese Option muss zusammen mit der Option **/fo** *resname* verwendet werden. RC benennt die sprachneutrale . RES file *resname.res* and names the language-dependent (DOSSIER) . RES-Datei *mresname.res*.

**Windows Server 2003 und Windows XP/2000:** Diese Option ist nicht verfügbar, ohne auch die Funktionen [**LoadMUILibrary**](/windows/desktop/api/muiload/nf-muiload-loadmuilibrarya) und [**FreeMUILibrary**](/windows/desktop/api/muiload/nf-muiload-freemuilibrary) auf einem aktualisierten System zu verwenden.

</dd> <dt>

<span id="_fo_resname"></span><span id="_FO_RESNAME"></span>**/fo** *resname*
</dt> <dd>

RC erstellt eine . RES-Datei namens *resname* mithilfe der *Skriptdatei*.

Wenn auch die Option **/fm** *mresname* festgelegt ist, erstellt RC eine sprachneutrale . RES-Datei und eine sprachabhängige (LANGUAGE-dependent, LANGUAGE) . RES-Datei.

**Windows Server 2003 und Windows XP/2000:** Diese Option ist nicht verfügbar, ohne auch die Funktionen [**LoadMUILibrary**](/windows/desktop/api/muiload/nf-muiload-loadmuilibrarya) und [**FreeMUILibrary**](/windows/desktop/api/muiload/nf-muiload-freemuilibrary) auf einem aktualisierten System zu verwenden.

</dd> <dt>

<span id="_g1"></span><span id="_G1"></span>**/g1**
</dt> <dd>

Wenn /g1 festgelegt ist, generiert RC eine CSV-Datei, wenn die einzige lokalisierbare Ressource, die in der CSV-Datei enthalten ist, eine Versionsressource ist. Wenn /g1 nicht festgelegt ist, generiert RC keine CSV-Datei, wenn die einzige lokalisierbare Ressource, die in der DATEI AUSschreibbar ist, eine Versionsressource ist.

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

Lokalisierbare Ressourcentypen RC platziert in die sprachabhängige (LANGUAGE-dependent, LANGUAGE) . RES-Datei. Wenn auch die Option **/q** festgelegt ist, wird diese Option ignoriert, und die Informationen in der RC-Konfigurationsdatei haben Vorrang.

**Windows Server 2003 und Windows XP/2000:** Diese Option ist nicht verfügbar, ohne auch die Funktionen [**LoadMUILibrary**](/windows/desktop/api/muiload/nf-muiload-loadmuilibrarya) und [**FreeMUILibrary**](/windows/desktop/api/muiload/nf-muiload-freemuilibrary) auf einem aktualisierten System zu verwenden.

</dd> <dt>

<span id="_k_overtype"></span><span id="_K_OVERTYPE"></span>**/k** *overtype*
</dt> <dd>

Überlappende Ressourcentypen, die RC in beide sprachneutrale platziert. RES und die sprachabhängige (LANGUAGE-dependent, LANGUAGE) RES-Dateien. Die von der Option **/k** angegebenen Ressourcentypen müssen eine Teilmenge der Ressourcentypen sein, die von der **Option /j** angegeben werden. Zum Beispiel? J2 ? J3 ? K3 gibt an, dass RC den Ressourcentyp 3 sowohl in den sprachneutralen als auch in sprachabhängigen Dateien (LANGUAGE-Dependent, LANGUAGE- ) platziert. Wenn auch die Option **/q** festgelegt ist, wird diese Option ignoriert, und die Informationen in der RC-Konfigurationsdatei haben Vorrang.

**Windows Server 2003 und Windows XP/2000:** Diese Option ist nicht verfügbar, ohne auch die Funktionen [**LoadMUILibrary**](/windows/desktop/api/muiload/nf-muiload-loadmuilibrarya) und [**FreeMUILibrary**](/windows/desktop/api/muiload/nf-muiload-freemuilibrary) auf einem aktualisierten System zu verwenden.

</dd> <dt>

<span id="_l_langid"></span><span id="_L_LANGID"></span>**/l** *langid*
</dt> <dd>

Gibt die Standardsprache für die Kompilierung an. Beispielsweise entspricht -l409 dem Einschließen der folgenden Anweisung am Anfang der Ressourcenskriptdatei: `LANGUAGE LANG_ENGLISH,SUBLANG_ENGLISH_US`

Weitere Informationen finden Sie unter [Sprachbezeichner.](/windows/desktop/Intl/language-identifiers)

</dd> <dt>

<span id="_n"></span><span id="_N"></span>**/n**
</dt> <dd>

NULL beendet alle Zeichenfolgen in der Zeichenfolgentabelle.

</dd> <dt>

<span id="_q_Mui.RCConfig"></span><span id="_q_mui.rcconfig"></span><span id="_Q_MUI.RCCONFIG"></span>**/q:** *Csv.RCConfig*
</dt> <dd>

Eine RC-Konfigurationsdatei, die dem RC-Konfigurationsdateiformat folgt. Mit dem RC-Konfigurationsdateiformat können Komponenten Ressourceninformationen wie Ressourcenversionsverwaltung, ZIP-Dateipfad, Ressourcentypen und Elemente selbst beschreiben. Diese Datei gibt an, welche Ressourcen in die sprachneutrale gelangen. RES-Datei und welche Ressourcen in die sprachabhängige (LANGUAGE-dependent, LANGUAGE) gelangen. RES-Datei. Diese Option und die in der RC-Konfigurationsdatei bereitgestellten Informationen überschreiben die Befehlszeilenoptionen **/j** und **/k.**

**Windows Server 2003 und Windows XP/2000:** Diese Option ist nicht verfügbar, ohne auch die Funktionen [**LoadMUILibrary**](/windows/desktop/api/muiload/nf-muiload-loadmuilibrarya) und [**FreeMUILibrary**](/windows/desktop/api/muiload/nf-muiload-freemuilibrary) auf einem aktualisierten System zu verwenden.

</dd> <dt>

<span id="_r"></span><span id="_R"></span>**/r**
</dt> <dd>

Ignoriert. Aus Gründen der Kompatibilität mit vorhandenen Makefiles bereitgestellt.

</dd> <dt>

<span id="_u"></span><span id="_U"></span>**/u**
</dt> <dd>

Definiert ein Symbol für den Präprozessor nicht.

</dd> <dt>

<span id="_v"></span><span id="_V"></span>**/v**
</dt> <dd>

Zeigt Meldungen an, die den Fortschritt des Compilers melden.

</dd> <dt>

<span id="_x"></span><span id="_X"></span>**/x**
</dt> <dd>

Verhindert, dass RC die INCLUDE-Umgebungsvariable überprüft, wenn nach Headerdateien oder Ressourcendateien gesucht wird.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Bei Optionen wird die Groß-/Kleinschreibung nicht beachtet, und anstelle eines Schrägstrichs (/) kann ein Bindestrich (-) verwendet werden. Sie können Optionen mit einem Buchstaben kombinieren, wenn keine zusätzlichen Parameter erforderlich sind.

RC generiert in den folgenden Fällen keine CSV-Datei.

-   In der RC-Datei sind keine lokalisierbaren Ressourcen vorhanden.
-   Die einzige in der RC-Datei angegebene Ressourcensprach-ID ist neutral (0x0).
-   Die RC-Datei verfügt über Ressourcen, die in mehreren Sprachen angegeben sind. Die Ausnahme ist, wenn die RC-Datei zwei Sprachen enthält und eine Sprache neutral (0x0) ist, generiert RC eine CSV-Datei.

Weitere Informationen finden Sie in den folgenden Themen:

-   [Definieren von Namen für den Präprozessor](defining-names-for-the-preprocessor.md)
-   [Umbenennen der kompilierten Ressourcendatei](renaming-the-compiled-resource-file.md)
-   [Suchen nach Dateien](searching-for-files.md)
-   [Anzeigen von Statusmeldungen](displaying-progress-messages.md)
-   [RC-Diagnosemeldungen](rc-diagnostic-messages.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Multilingual User Interface](/windows/desktop/Intl/multilingual-user-interface)
</dt> </dl>

 

 