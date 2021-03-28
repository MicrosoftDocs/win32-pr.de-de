---
description: Die automatische Vervollständigung erweitert Zeichen folgen, die teilweise in einem Bearbeitungs Steuerelement eingegeben wurden, in vollständige Zeichen folgen.
title: Verwenden von Auto Vervollständigen
ms.topic: article
ms.date: 05/31/2018
ms.assetid: b990395b-fc10-48f9-a718-7cc006e37eb7
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: fbbf0c53fc1b26002d1b46a9a6a6f67cd15e3ead
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977424"
---
# <a name="using-autocomplete"></a>Verwenden von Auto Vervollständigen

Die automatische Vervollständigung erweitert Zeichen folgen, die teilweise in einem [Bearbeitungs Steuer](/windows/desktop/Controls/edit-controls) Element eingegeben wurden, in vollständige Zeichen folgen. Wenn ein Benutzer beispielsweise die Eingabe einer URL in das Address Edit-Steuerelement startet, das in der Windows Internet Explorer-Symbolleiste eingebettet ist, erweitert die automatische Vervollständigung die Zeichenfolge in eine oder mehrere vollständige URL-Optionen, die mit der vorhandenen partiellen Zeichenfolge konsistent sind. Eine partielle URL-Zeichenfolge, z. b. "MIC", kann auf " https://www.microsoft.com " oder "" erweitert werden https://www.microsoft.com/windows . Die automatische Vervollständigung wird in der Regel mit Bearbeitungs Steuerelementen oder mit Steuerelementen verwendet, die ein eingebettetes Bearbeitungs Steuerelement wie das [ComboBoxEx](/windows/desktop/Controls/comboboxex-control-reference) -Steuerelement aufweisen.

## <a name="adding-autocomplete-functionality-to-your-application"></a>Hinzufügen von Auto Vervollständigen-Funktionen zu Ihrer Anwendung

Eine Anwendung kann einem Bearbeitungs Steuerelement auf zwei Arten eine Auto Vervollständigen-Funktionalität hinzufügen:

-   [**SHAutoComplete**](/windows/desktop/api/shlwapi/nf-shlwapi-shautocomplete) ist eine einfache Funktion, mit der ein Dateipfad oder eine URL automatisch vervollständigt werden kann.
-   Die [**iautocomplete**](/windows/desktop/api/Shldisp/nn-shldisp-iautocomplete) -Schnittstelle wird durch das Auto Vervollständigen-Objekt (CLSID \_ Auto Vervollständigen) verfügbar gemacht. Sie ermöglicht es Anwendungen, das-Objekt zu initialisieren, zu aktivieren und zu deaktivieren. **Iautocomplete** ermöglicht mehr Kontrolle über Auto Vervollständigen-Quellen, einschließlich der Möglichkeit, eine benutzerdefinierte Quelle hinzuzufügen. Im restlichen Teil dieses Themas wird die Verwendung von **iautocomplete** erläutert. Weitere Informationen finden [Sie unter Manuelles Aktivieren von AutoComplete](how-to-enable-autocomplete-manually.md) für bestimmte Verwendungs Beispiele.

## <a name="autocomplete-modes"></a>Auto Vervollständigen-Modi

Wenn Sie [**iautocomplete**](/windows/desktop/api/Shldisp/nn-shldisp-iautocomplete)verwenden, kann die automatische Vervollständigung die abgeschlossene Zeichenfolge in zwei Modi anzeigen: AutoAppend und AutoVorschlagen. Die Modi sind unabhängig. Sie können entweder oder beides aktivieren. Um den Modus anzugeben, geben Sie [**IAutoComplete2:: * toptions**](/windows/desktop/api/Shldisp/nf-shldisp-iautocomplete2-setoptions)an.

<dl> <dt>

<span id="Autoappend"></span><span id="autoappend"></span><span id="AUTOAPPEND"></span>Automatisch anfügen
</dt> <dd>

Im AutoAppend-Modus fügt die automatische Vervollständigung den Rest der wahrscheinlichsten Kandidaten Zeichenfolge an die vorhandenen Zeichen an, wobei die angefügten Zeichen hervorgehoben werden. Wenn der Benutzer weiterhin Zeichen eingibt, werden diese der vorhandenen partiellen Zeichenfolge hinzugefügt. Wenn der Benutzer ein Zeichen hinzufügt, das mit dem nächsten markierten Zeichen identisch ist, wird die Hervorhebung für dieses Zeichen deaktiviert. Die restlichen Zeichen werden weiterhin hervorgehoben. Wenn der Benutzer ein Zeichen hinzufügt, das nicht mit dem nächsten markierten Zeichen identisch ist, versucht die automatische Vervollständigung, eine neue Kandidaten Zeichenfolge auf der Grundlage der größeren partiellen Zeichenfolge zu generieren, und fügt den Rest der neuen Kandidaten Zeichenfolge der aktuellen partiellen Zeichenfolge an. Wenn keine Kandidaten Zeichenfolge gefunden werden kann, werden nur die typisierten Zeichen angezeigt, und das Bearbeitungsfeld verhält sich wie ohne die automatische Vervollständigung. Dieser Prozess wird fortgesetzt, bis der Benutzer eine Zeichenfolge annimmt.

</dd> <dt>

<span id="Autosuggest"></span><span id="autosuggest"></span><span id="AUTOSUGGEST"></span>-Vorschlags Suche
</dt> <dd>

Im Auto vorschlagen-Modus zeigt die automatische Vervollständigung eine Dropdown Liste mit einer oder mehreren vorgeschlagenen vollständigen Zeichen folgen unterhalb des Bearbeitungs Steuer Elements an. Der Benutzer kann eine der vorgeschlagenen Zeichen folgen auswählen oder mit der Eingabe fortfahren. Wenn die Typisierung durchlaufen wird, kann die Dropdown Liste basierend auf der aktuellen partiellen Zeichenfolge geändert werden. Wenn Sie das Flag für die ACO- \_ Suche in [**IAutoComplete2:: SetOptions**](/windows/desktop/api/Shldisp/nf-shldisp-iautocomplete2-setoptions)festlegen, stellt Auto Vervollständigen unten in der Dropdown Liste eine Option für die Suche nach der aktuellen Teil Zeichenfolge bereit. Diese Option wird auch dann angezeigt, wenn keine empfohlenen Zeichen folgen vorhanden sind. Wenn der Benutzer die Suchoption auswählt, sollte Ihre Anwendung eine Suchmaschine starten, um den Benutzer zu unterstützen.

</dd> </dl>

## <a name="using-predefined-autocomplete-sources"></a>Verwenden vordefinierter Auto Vervollständigen-Quellen

Die automatische Vervollständigung hängt von der Quelle ab, die Ihr Zeichen folgen zur Verfügung stellt, die mit der Teil Zeichenfolge des Benutzers verglichen werden Sie haben die Möglichkeit, eine benutzerdefinierte Auto Vervollständigen-Quelle bereitzustellen, aber einige der gängigsten Quellen werden vom System bereitgestellt.

<dl> <dt>

<span id="CLSID_ACLHistory"></span><span id="clsid_aclhistory"></span><span id="CLSID_ACLHISTORY"></span>CLSID- \_ aclhistory
</dt> <dd>

Eine Auto Vervollständigen-Quelle, die mit der URL-Liste in der Verlaufs Liste des Benutzers übereinstimmt.

</dd> <dt>

<span id="CLSID_ACLMRU"></span><span id="clsid_aclmru"></span>CLSID- \_ aclmru
</dt> <dd>

Eine Auto Vervollständigen-Quelle, die mit der URL-Liste in der Liste der zuletzt verwendeten Benutzer übereinstimmt.

</dd> <dt>

<span id="CLSID_ACListISF"></span><span id="clsid_aclistisf"></span><span id="CLSID_ACLISTISF"></span>CLSID- \_ aclistisf
</dt> <dd>

Eine Auto Vervollständigen-Quelle, die mit Elementen im Shellnamespace übereinstimmt: Dateien auf dem Computer des Benutzers sowie Elemente in virtuellen Ordnern, z. b. in der Systemsteuerung.

</dd> </dl>

Es gibt Situationen, in denen Sie anstelle der sofortigen Freigabe der Ressourcen die Schnittstellen Zeiger auf die verschiedenen an AutoComplete beteiligten Objekte beibehalten möchten. Dies ist insbesondere dann der Fall, wenn Sie das Auto Vervollständigen-Verhalten dynamisch anpassen möchten. Die häufigste Instanz dieses Vorgangs tritt auf, wenn das CLSID- \_ aclistisf-Objekt verwendet wird, das automatisch vom Shell-Namespace vervollständigt wird und die Option ([**aclo \_ CurrentDir**](/windows/win32/api/shlobj_core/nn-shlobj_core-iaclist2)) der Auflistung aus dem aktuellen Verzeichnis enthält. Wenn Sie z. b. zu einem neuen Ordner navigieren, ändert Internet Explorer das aktuelle Verzeichnis der Adressleiste, sodass die Einstellungen dynamisch geändert werden müssen. Es gibt zwei Möglichkeiten, das Verzeichnis anzugeben, das vom CLSID- \_ aclistisf-Objekt als Aktuelles Verzeichnis behandelt werden soll:

-   [**Ipersistfolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder) gibt das Verzeichnis über eine [**itemittellist**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist)an.
-   [**Icurrentworkingdirectory**](/windows/win32/api/shlobj/nn-shlobj-icurrentworkingdirectory) gibt das Verzeichnis über eine Pfad Zeichenfolge an.

Gehen Sie wie folgt vor, dass **PAL** ein Zeiger auf die [**iaclist**](/windows/win32/api/shlobj_core/nn-shlobj_core-iaclist) -Schnittstelle eines CLSID- \_ aclistisf-Objekts ist:

-   Verwenden von " [**ipersistfolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder)":

    Um dem CLSID- \_ aclistisf-Objekt mitzuteilen, dass eine bestimmte [**itemittel List**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) als Aktuelles Verzeichnis behandelt werden soll, können Sie die [**ipersistfolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder) -Schnittstelle des Objekts verwenden. Da eine **itemittel List** auf einen virtuellen Ordner verweisen kann, ist diese Methode flexibler als die Verwendung von [**icurrentworkingdirectory**](/windows/win32/api/shlobj/nn-shlobj-icurrentworkingdirectory).

    Beachten Sie, dass in den folgenden Beispielen die vorlagenbasierte QueryInterface-Schnittstelle verwendet wird, die eine vereinfachte Parameterliste zulässt.

    ```C++
    IPersistFolder *ppf;

    hr = pal2->QueryInterface(IID_PPV_ARGS(&ppf));   
    if (SUCCEEDED(hr))
    {
        hr = ppf->Initialize(pidlCurrentDirectory);
        ppf->Release();
    }
    ```

    

-   Verwenden von [**icurrentworkingdirectory**](/windows/win32/api/shlobj/nn-shlobj-icurrentworkingdirectory):

    Um dem CLSID- \_ aclistisf-Objekt einen Pfad als Aktuelles Verzeichnis zu übergeben, können Sie die [**icurrentworkingdirectory**](/windows/win32/api/shlobj/nn-shlobj-icurrentworkingdirectory) -Schnittstelle des Objekts verwenden.

    ```C++
    WCHAR pwszDirectory[MAX_PATH] = L"C:\\Program Files";
    ICurrentWorkingDirectory *pcwd;

    hr = pal2->QueryInterface(IID_PPV_ARGS(&pcwd));    
    if (SUCCEEDED(hr))
    {
        hr = pcwd->SetDirectory(pwszDirectory);
        pcwd->Release();
    }
    ```

    

 

 
