---
description: Die automatische Vervollständigung erweitert Zeichenfolgen, die teilweise in ein Bearbeitungssteuerelement eingegeben wurden, in vollständige Zeichenfolgen.
title: Verwenden von AutoVervollständigen
ms.topic: article
ms.date: 05/31/2018
ms.assetid: b990395b-fc10-48f9-a718-7cc006e37eb7
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 822f2554f51adfb99b1b4b2ad9d61fe064f802def3c8804371639ec20563b54b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119223710"
---
# <a name="using-autocomplete"></a>Verwenden von AutoVervollständigen

Die automatische Vervollständigung erweitert Zeichenfolgen, die teilweise in ein [Bearbeitungssteuerelement](/windows/desktop/Controls/edit-controls) eingegeben wurden, in vollständige Zeichenfolgen. Wenn ein Benutzer beispielsweise beginnt, eine URL in das Adressbearbeitungssteuerelement einzugeben, das in die symbolleiste Windows Internet Explorer eingebettet ist, erweitert die automatische Vervollständigung die Zeichenfolge in mindestens eine vollständige URL-Option, die mit der vorhandenen Teilzeichenfolge konsistent ist. Eine partielle URL-Zeichenfolge wie "mic" kann auf " " oder " " erweitert https://www.microsoft.com https://www.microsoft.com/windows werden. Die automatische Vervollständigung wird in der Regel mit Bearbeitungssteuerelementen oder mit Steuerelementen verwendet, die über ein eingebettetes Bearbeitungssteuerelement verfügen, z. B. das [ComboBoxEx-Steuerelement.](/windows/desktop/Controls/comboboxex-control-reference)

## <a name="adding-autocomplete-functionality-to-your-application"></a>Hinzufügen von AutoVervollständigen-Funktionen zu Ihrer Anwendung

Eine Anwendung kann einem Bearbeitungssteuerelement funktionen für die automatische Vervollständigung auf zwei Arten hinzufügen:

-   [**SHAutoComplete**](/windows/desktop/api/shlwapi/nf-shlwapi-shautocomplete) ist eine einfache Funktion, die einen Dateipfad oder eine URL automatisch vervollständigen kann.
-   [**Die IAutoComplete-Schnittstelle**](/windows/desktop/api/Shldisp/nn-shldisp-iautocomplete) wird vom AutoVervollständigen-Objekt (CLSID \_ AutoComplete) verfügbar gemacht. Es ermöglicht Anwendungen, das Objekt zu initialisieren, zu aktivieren und zu deaktivieren. **IAutoComplete** ermöglicht mehr Kontrolle über AutoVervollständigen-Quellen, einschließlich der Möglichkeit, eine benutzerdefinierte Quelle hinzuzufügen. Im weiteren Verlauf dieses Themas wird die Verwendung von **IAutoComplete erläutert.** Spezifische Verwendungsbeispiele finden Sie unter How To Enable AutoComplete Manually (Manuelles Aktivieren der [automatischen Vervollständigung).](how-to-enable-autocomplete-manually.md)

## <a name="autocomplete-modes"></a>AutoVervollständigen-Modi

Bei Verwendung von [**IAutoComplete**](/windows/desktop/api/Shldisp/nn-shldisp-iautocomplete)kann die vollständige Zeichenfolge in zwei Modi angezeigt werden: autoappend und autosuggest. Die Modi sind unabhängig. Sie können entweder oder beides aktivieren. Rufen Sie [**IAutoComplete2::SetOptions**](/windows/desktop/api/Shldisp/nf-shldisp-iautocomplete2-setoptions)auf, um den Modus anzugeben.

<dl> <dt>

<span id="Autoappend"></span><span id="autoappend"></span><span id="AUTOAPPEND"></span>AutoAppend
</dt> <dd>

Im AutoAppend-Modus fügt die automatische Vervollständigung den Rest der wahrscheinlichsten Möglichenzeichenfolge an die vorhandenen Zeichen an, wobei die angefügten Zeichen hervorgehoben werden. Wenn der Benutzer weiterhin Zeichen eingibt, wird er der vorhandenen Teilzeichenfolge hinzugefügt. Wenn der Benutzer ein Zeichen hinzufügt, das mit dem nächsten hervorgehobenen Zeichen identisch ist, wird die Hervorhebung für dieses Zeichen deaktiviert. Die restlichen Zeichen werden weiterhin hervorgehoben. Wenn der Benutzer ein Zeichen hinzufügt, das nicht mit dem nächsten hervorgehobenen Zeichen übereinstimmt, versucht die automatische Vervollständigung, basierend auf der größeren Teilzeichenfolge eine neue Kandidatenzeichenfolge zu generieren, und fügt den Rest der neuen Kandidatenzeichenfolge an die aktuelle Teilzeichenfolge an. Wenn keine Kandidatenzeichenfolge gefunden werden kann, werden nur die typisierten Zeichen angezeigt, und das Bearbeitungsfeld verhält sich wie ohne automatische Vervollständigung. Dieser Prozess wird fortgesetzt, bis der Benutzer eine Zeichenfolge akzeptiert.

</dd> <dt>

<span id="Autosuggest"></span><span id="autosuggest"></span><span id="AUTOSUGGEST"></span>Autosuggest
</dt> <dd>

Im Modus für die automatischeUggeste zeigt die automatische Vervollständigung eine Dropdownliste mit mindestens einer vorgeschlagenen vollständigen Zeichenfolge unterhalb des Bearbeitungssteuerelements an. Der Benutzer kann eine der vorgeschlagenen Zeichenfolgen auswählen oder die Eingabe fortsetzen. Während die Eingabe fortschreitet, kann die Dropdownliste basierend auf der aktuellen Teilzeichenfolge geändert werden. Wenn Sie das ACO \_ SEARCH-Flag in [**IAutoComplete2::SetOptions**](/windows/desktop/api/Shldisp/nf-shldisp-iautocomplete2-setoptions)festlegen, bietet autocomplete eine Option am unteren Rand der Dropdownliste, um nach der aktuellen Teilzeichenfolge zu suchen. Diese Option wird auch dann angezeigt, wenn keine vorgeschlagenen Zeichenfolgen vorhanden sind. Wenn der Benutzer die Suchoption auswählt, sollte Ihre Anwendung eine Suchmaschine starten, um den Benutzer zu unterstützen.

</dd> </dl>

## <a name="using-predefined-autocomplete-sources"></a>Verwenden vordefinierter AutoVervollständigen-Quellen

Die automatische Vervollständigung hängt davon ab, dass sie über eine Quelle verfügt, die Zeichenfolgen bereitstellt, die mit der Teilzeichenfolge des Benutzers übereinstimmen. Sie haben die Möglichkeit, eine benutzerdefinierte AutoVervollständigen-Quelle bereitzustellen, aber mehrere der gängigsten Quellen werden vom System bereitgestellt.

<dl> <dt>

<span id="CLSID_ACLHistory"></span><span id="clsid_aclhistory"></span><span id="CLSID_ACLHISTORY"></span>\_CLSID-ACLHistory
</dt> <dd>

Eine AutoVervollständigen-Quelle, die mit der URL-Liste in der Verlaufsliste des Benutzers übereinstimmt.

</dd> <dt>

<span id="CLSID_ACLMRU"></span><span id="clsid_aclmru"></span>CLSID \_ ACLMRU
</dt> <dd>

Eine AutoVervollständigen-Quelle, die mit der URL-Liste in der Liste Zuletzt verwendet des Benutzers übereinstimmt.

</dd> <dt>

<span id="CLSID_ACListISF"></span><span id="clsid_aclistisf"></span><span id="CLSID_ACLISTISF"></span>CLSID \_ ACListISF
</dt> <dd>

Eine AutoVervollständigen-Quelle, die mit Elementen im Shellnamespace übereinstimmt: Dateien auf dem Computer des Benutzers sowie Elemente in virtuellen Ordnern wie Systemsteuerung.

</dd> </dl>

Es gibt Situationen, in denen Sie die Schnittstellenzeiger auf die verschiedenen Objekte, die an der automatischen Vervollständigung beteiligt sind, beibehalten möchten, anstatt die Ressourcen sofort freizulassen. Dies geschieht insbesondere, wenn Sie das AutoVervollständigen-Verhalten dynamisch anpassen möchten. Die gängigste Instanz dieses -Objekts tritt auf, wenn das \_ CLSID-ACListISF-Objekt verwendet wird, das automatisch aus dem Shellnamespace vervollständigt wird und die Option ([**ACLO \_ CURRENTDIR**](/windows/win32/api/shlobj_core/nn-shlobj_core-iaclist2)) zum Auflisten aus dem aktuellen Verzeichnis hat. Wenn Sie beispielsweise zu einem neuen Ordner navigieren, ändert Internet Explorer das aktuelle Verzeichnis der Adressleiste. Daher müssen die Einstellungen dynamisch geändert werden. Es gibt zwei Möglichkeiten, das Verzeichnis anzugeben, das das \_ CLSID-ACListISF-Objekt als aktuelles Verzeichnis behandeln soll:

-   [**IPersistFolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder) gibt das Verzeichnis über [**itemidlist**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist)an.
-   [**ICurrentWorkingDirectory**](/windows/win32/api/shlobj/nn-shlobj-icurrentworkingdirectory) gibt das Verzeichnis über eine Pfadzeichenfolge an.

Gehen Sie im Folgenden davon aus, dass **pal** ein Zeiger auf die [**LIAList-Schnittstelle**](/windows/win32/api/shlobj_core/nn-shlobj_core-iaclist) eines CLSID \_ ACListISF-Objekts ist:

-   Verwenden von [**IPersistFolder:**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder)

    Um dem CLSID \_ ACListISF-Objekt mitzuteilen, dass eine bestimmte [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) als das aktuelle Verzeichnis behandelt werden soll, können Sie die [**IPersistFolder-Schnittstelle**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder) des Objekts verwenden. Da eine **ITEMIDLIST** auf einen virtuellen Ordner verweisen kann, ist diese Methode flexibler als die Verwendung von [**ICurrentWorkingDirectory**](/windows/win32/api/shlobj/nn-shlobj-icurrentworkingdirectory).

    Beachten Sie, dass in den folgenden Beispielen die vorlagende QueryInterface verwendet wird, die eine vereinfachte Parameterliste ermöglicht.

    ```C++
    IPersistFolder *ppf;

    hr = pal2->QueryInterface(IID_PPV_ARGS(&ppf));   
    if (SUCCEEDED(hr))
    {
        hr = ppf->Initialize(pidlCurrentDirectory);
        ppf->Release();
    }
    ```

    

-   Verwenden von [**ICurrentWorkingDirectory:**](/windows/win32/api/shlobj/nn-shlobj-icurrentworkingdirectory)

    Um dem CLSID \_ ACListISF-Objekt einen Pfad als aktuelles Verzeichnis zu geben, können Sie die [**ICurrentWorkingDirectory-Schnittstelle**](/windows/win32/api/shlobj/nn-shlobj-icurrentworkingdirectory) des Objekts verwenden.

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

    

 

 
