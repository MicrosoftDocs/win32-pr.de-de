---
description: Die Funktionen der Shell können mit Registrierungseinträgen und .ini erweitert werden.
ms.assetid: 74a81e4f-7357-4901-a118-ba44e8892f25
title: Erstellen von Shellerweiterungshandlern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 729fad22eb86e9c32e43c459d7a30b11f68d8d06360b60cee373bb3f74d3749f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032558"
---
# <a name="creating-shell-extension-handlers"></a>Erstellen von Shellerweiterungshandlern

Die Funktionen der Shell können mit Registrierungseinträgen und .ini erweitert werden. Dieser Ansatz zum Erweitern der Shell ist zwar einfach und für viele Zwecke ausreichend, aber er ist begrenzt. Wenn Sie beispielsweise die Registrierung verwenden, um ein benutzerdefiniertes Symbol für einen Dateityp anzugeben, wird für jede Datei dieses Typs das gleiche Symbol angezeigt. Wenn Sie die Shell mit der Registrierung erweitern, können Sie das Symbol für verschiedene Dateien desselben Typs nicht ändern. Andere Aspekte der Shell,  wie z. B. das Eigenschaftenblatt, das angezeigt werden kann, wenn mit der rechten Maustaste auf eine Datei geklickt wird, können mit der Registrierung überhaupt nicht geändert werden.

Ein leistungsstärkerer und flexiblerer Ansatz zum Erweitern der Shell ist die Implementierung von *Shellerweiterungshandlern.* Diese Handler können für eine Vielzahl von Aktionen implementiert werden, die die Shell ausführen kann. Vor dem Ausführen der Aktion fragt die Shell den Erweiterungshandler ab und gibt ihr die Möglichkeit, die Aktion zu ändern. Ein häufiges Beispiel ist ein Kontextmenü-Erweiterungshandler. Wenn eine Datei für einen Dateityp implementiert ist, wird sie jedes Mal abgefragt, wenn mit der rechten Maustaste auf eine der Dateien geklickt wird. Der Handler kann dann dateispezifische zusätzliche Menüelemente angeben, anstatt denselben Satz für den gesamten Dateityp zu verwenden.

In diesem Dokument wird erläutert, wie Sie die Erweiterungshandler implementieren, mit denen Sie eine Vielzahl von Shellaktionen ändern können. Die folgenden Handler sind einem bestimmten Dateityp zugeordnet und ermöglichen die Datei-für-Datei-Angabe:



| Handler                                               | BESCHREIBUNG                                                                                                                                                                |
|-------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Kontextmenühandler](context-menu-handlers.md)    | Wird aufgerufen, bevor das Kontextmenü einer Datei angezeigt wird. Dadurch können Sie dem Kontextmenü Datei für Datei Elemente hinzufügen.                                               |
| [Datenhandler](how-to-create-data-handlers.md)       | Wird aufgerufen, wenn ein Drag & Drop-Vorgang für dragShell-Objekte ausgeführt wird. Sie können dem Ablageziel zusätzliche Zwischenablageformate bereitstellen.                        |
| [Drop-Handler](how-to-create-drop-handlers.md)       | Wird aufgerufen, wenn ein Datenobjekt in einer Datei gezogen oder gelöscht wird. Dadurch können Sie eine Datei zu einem Abbruchziel machen.                                                          |
| [Symbolhandler](how-to-create-icon-handlers.md)       | Wird aufgerufen, bevor das Symbol einer Datei angezeigt wird. Sie können das Standardsymbol der Datei durch ein benutzerdefiniertes Symbol auf Dateibasis ersetzen.                                    |
| [Eigenschaftenblatthandler](propsheet-handlers.md)      | Wird aufgerufen, bevor das **Eigenschaftenblatt Eigenschaften** eines Objekts angezeigt wird. Dadurch können Sie Seiten hinzufügen oder ersetzen.                                                              |
| [**Handler für Miniaturansichtsbilder**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) | Stellt ein Bild zur Darstellung des Elements dar.                                                                                                                                   |
| [**QuickInfo-Handler**](/windows/win32/api/shlobj_core/nn-shlobj_core-iqueryinfo)                 | Stellt Popuptext zum Zeitpunkt der Mauszeigerbewegung über das -Objekt zurVerfingung von Popuptext zurVerkn.                                                                                               |
| [**Metadatenhandler**](/windows/win32/api/propsys/nn-propsys-ipropertystore)     | Bietet Lese- und Schreibzugriff auf Metadaten (Eigenschaften), die in einer Datei gespeichert sind. Dies kann verwendet werden, um die Detailansicht, Infotips, die Eigenschaftenseite und Gruppierungsfeatures zu erweitern. |



 

Andere Handler sind einem bestimmten Dateityp nicht zugeordnet, werden jedoch vor einigen Shellvorgängen aufgerufen:



| Handler                                                            | BESCHREIBUNG                                                                                                                                  |
|--------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [Spaltenhandler](../lwef/column-handlers.md)                             | Wird von Windows Explorer aufgerufen, bevor die Detailansicht eines Ordners angezeigt wird. Sie können der Detailansicht benutzerdefinierte Spalten hinzufügen.        |
| [Hookhandler kopieren](how-to-create-copy-hook-handlers.md)          | Wird aufgerufen, wenn ein Ordner oder Druckerobjekt verschoben, kopiert, gelöscht oder umbenannt werden soll. Sie können den Vorgang genehmigen oder blockieren.   |
| [Drag &amp;amp; Drop-Handler](context-menu-handlers.md)                 | Wird aufgerufen, wenn eine Datei mit der rechten Maustaste gezogen wird. Sie können das angezeigte Kontextmenü ändern.                     |
| [Symbolüberlagerungshandler](how-to-implement-icon-overlay-handlers.md) | Wird aufgerufen, bevor das Symbol einer Datei angezeigt wird. Dadurch können Sie eine Überlagerung für das Symbol der Datei angeben.                                          |
| [Suchhandler](../lwef/search-handlers.md)                             | Wird aufgerufen, um eine Suchmaschine zu starten. Sie können eine benutzerdefinierte Suchmaschine implementieren, auf die über das **Startmenü oder** den Windows kann. |



 

Die Details zum Implementieren bestimmter Erweiterungshandler werden in den oben aufgeführten Abschnitten behandelt. Im restlichen Teil dieses Dokuments werden einige Implementierungsprobleme behandelt, die für alle Shell-Erweiterungshandler gelten.

-   [Implementieren von Shellerweiterungshandlern](#implementing-shell-extension-handlers)
    -   [Implementieren von IPersistFile](#implementing-ipersistfile)
    -   [Implementieren von IShellExtInit](#implementing-ishellextinit)
    -   [Infotip-Anpassung](#infotip-customization)
-   [Erweitern Windows Suche mit Shell-Erweiterungshandlern](#enhancing-windows-search-with-shell-extension-handlers)
-   [Registrieren von Shellerweiterungshandlern](#registering-shell-extension-handlers)
    -   [Handlernamen](#handler-names)
    -   [Vordefinierte Shellobjekte](#predefined-shell-objects)
    -   [Beispiel für eine Erweiterungshandlerregistrierung](#example-of-an-extension-handler-registration)
-   [Zugehörige Themen](#related-topics)

## <a name="implementing-shell-extension-handlers"></a>Implementieren von Shellerweiterungshandlern

Ein Größerer Teil der Implementierung eines Shell-Erweiterungshandlerobjekts hängt vom Typ ab. Es gibt jedoch einige allgemeine Elemente. In diesem Abschnitt werden die Aspekte der Implementierung erläutert, die von allen Shell-Erweiterungshandlern gemeinsam genutzt werden.

Viele Shellerweiterungshandler sind IN-Process-Component Object Model (COM)-Objekte. Sie müssen einer GUID zugewiesen und registriert werden, wie unter Registrieren von Shell-Erweiterungshandlern beschrieben. Sie werden als DLLs implementiert und müssen die folgenden Standardfunktionen exportieren:

-   [**DllMain**](../dlls/dllmain.md). Der Standardeinstiegspunkt für die DLL.
-   [**DllGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-dllgetclassobject). Macht die Klassen factory des Objekts verfügbar.
-   [**DllCanUnloadNow**](/windows/win32/api/combaseapi/nf-combaseapi-dllcanunloadnow). COM ruft diese Funktion auf, um zu bestimmen, ob das Objekt Clients bedient. Falls nicht, kann das System die DLL entladen und den zugeordneten Arbeitsspeicher frei geben.

Wie alle COM-Objekte müssen Shell-Erweiterungshandler eine [**IUnknown-Schnittstelle**](/windows/win32/api/unknwn/nn-unknwn-iunknown) und eine Klassen [factory implementieren.](../com/implementing-iclassfactory.md) Die meisten Erweiterungshandler müssen auch eine [**IPersistFile-**](/windows/win32/api/objidl/nn-objidl-ipersistfile) oder [**IShellExtInit-Schnittstelle**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) in Windows XP oder früher implementieren. Diese wurden durch [**IInitializeWithStream,**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithstream) [**IInitializeWithItem**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem) und [**IInitializeWithFile**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithfile) in Windows Vista ersetzt. Die Shell verwendet diese Schnittstellen, um den Handler zu initialisieren.

Die [**IPersistFile-Schnittstelle**](/windows/win32/api/objidl/nn-objidl-ipersistfile) muss wie folgt implementiert werden:

-   Datenhandler
-   Drop-Handler

In der Vergangenheit waren auch Symbolhandler erforderlich, um [**IPersistFile zu**](/windows/win32/api/objidl/nn-objidl-ipersistfile)implementieren. Dies ist jedoch nicht mehr der Fall. Für Symbolhandler ist **IPersistFile** jetzt optional, und andere Schnittstellen wie [**IInitializeWithItem**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem) werden bevorzugt.

Die [**IShellExtInit-Schnittstelle**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) muss wie folgt implementiert werden:

-   Kontextmenühandler
-   Drag & Drop-Handler
-   Eigenschaftenblatthandler

### <a name="implementing-ipersistfile"></a>Implementieren von IPersistFile

Die [**IPersistFile-Schnittstelle**](/windows/win32/api/objidl/nn-objidl-ipersistfile) soll ermöglichen, dass ein Objekt aus einer Datenträgerdatei geladen oder in einer Datenträgerdatei gespeichert werden kann. Es verfügt über sechs Methoden zusätzlich zu [**IUnknown,**](/windows/win32/api/unknwn/nn-unknwn-iunknown)fünf eigene Methoden und die [**GetClassID-Methode,**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid) die von [**IPersist geerbt wird.**](/windows/win32/api/objidl/nn-objidl-ipersist) Bei Shellerweiterungen **wird IPersist** nur zum Initialisieren eines Shell-Erweiterungshandlerobjekts verwendet. Da in der Regel kein Lese- oder Schreibzugriff auf den Datenträger erforderlich ist, erfordern nur die **Methoden GetClassID** und [**Load**](/windows/win32/api/objidl/nf-objidl-ipersistfile-load) eine Nichttokenimplementierung.

Die Shell ruft [**zuerst GetClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid) auf, und die Funktion gibt den Klassenbezeichner (CLSID) des Erweiterungshandlerobjekts zurück. Die Shell ruft dann [**Load auf und**](/windows/win32/api/objidl/nf-objidl-ipersistfile-load) übergibt zwei Werte. Die erste , *pszFileName,* ist eine Unicode-Zeichenfolge mit dem Namen der Datei oder des Ordners, mit der die Shell ausgeführt werden soll. Die zweite ist *dwMode,* was den Dateizugriffsmodus angibt. Da in der Regel kein Zugriff auf Dateien notwendig ist, *ist dwMode* in der Regel 0 (null). Die -Methode speichert diese Werte nach Bedarf für einen späteren Verweis.

Das folgende Codefragment veranschaulicht, wie ein typischer Shell-Erweiterungshandler die [**Methoden GetClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid) und [**Load**](/windows/win32/api/objidl/nf-objidl-ipersistfile-load) implementiert. Sie ist für die Handhabung von ANSI oder Unicode konzipiert. CLSID SampleExtHandler ist die GUID des Erweiterungshandlerobjekts, und CSampleExtHandler ist der Name der Klasse, die zum Implementieren \_ der Schnittstelle verwendet wird. Die **Variablen m \_ szFileName** und **m \_ dwMode** sind private Variablen, die zum Speichern des Dateinamens und der Zugriffsflags verwendet werden.


```C++
wchar_t m_szFileName[MAX_PATH];    // The file name
DWORD m_dwMode;                  // The file access mode

CSampleExtHandler::GetClassID(CLSID *pCLSID)
{
    *pCLSID = CLSID_SampleExtHandler;
}

CSampleExtHandler::Load(PCWSTR pszFile, DWORD dwMode)
{
    m_dwMode = dwMode;
    return StringCchCopy(_szFileName, ARRAYSIZE(m_szFileName), pszFile);
}
```

### <a name="implementing-ishellextinit"></a>Implementieren von IShellExtInit

Die [**IShellExtInit-Schnittstelle**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) verfügt zusätzlich zu [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)nur über eine Methode, [**IShellExtInit::Initialize.**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) Die -Methode verfügt über drei Parameter, die die Shell verwenden kann, um verschiedene Arten von Informationen zu übergeben. Die übergebenen Werte hängen vom Typ des Handlers ab, und einige können auf **NULL festgelegt werden.**

-   *pIDFolder* enthält den Zeiger eines Ordners auf eine Elementbezeichnerliste (PIDL). Für Eigenschaftenblatterweiterungen ist es **NULL.** Bei Kontextmenüerweiterungen ist es die PIDL des Ordners, der das Element enthält, dessen Kontextmenü angezeigt wird. Bei Nichtstandard-Drag & Drop-Handlern ist dies die PIDL des Zielordners.
-   *pDataObject enthält* einen Zeiger auf die [**IDataObject-Schnittstelle eines Datenobjekts.**](/windows/win32/api/objidl/nn-objidl-idataobject) Das Datenobjekt enthält mindestens einen Dateinamen im [CF \_ HDROP-Format.](dragdrop.md)
-   *hRegKey enthält* einen Registrierungsschlüssel für das Dateiobjekt oder den Ordnertyp.

Die [**IShellExtInit::Initialize-Methode**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) speichert den Dateinamen, [**den IDataObject-Zeiger**](/windows/win32/api/objidl/nn-objidl-idataobject) und den Registrierungsschlüssel nach Bedarf für die spätere Verwendung. Das folgende Codefragment veranschaulicht eine Implementierung von **IShellExtInit::Initialize**. Der Einfachheit halber wird in diesem Beispiel davon ausgegangen, dass das Datenobjekt nur eine einzelne Datei enthält. Im Allgemeinen kann es mehrere Dateien enthalten, die jeweils extrahiert werden müssen.


```C++
LPCITEMIDLIST  m_pIDFolder;           //The folder's PIDL
wchar_t        m_szFile[MAX_PATH];    //The file name
IDataObject   *m_pDataObj;            //The IDataObject pointer
HKEY           m_hRegKey;             //The file or folder's registry key

STDMETHODIMP CShellExt::Initialize(LPCITEMIDLIST pIDFolder, 
                                   IDataObject *pDataObj, 
                                   HKEY hRegKey) 
{ 
    // If Initialize has already been called, release the old PIDL
    ILFree(m_pIDFolder);
    m_pIDFolder = nullptr;

    // Store the new PIDL.
    if (pIDFolder)
    {
        m_pIDFolder = ILClone(pIDFolder);
    }
    
    // If Initialize has already been called, release the old
    // IDataObject pointer.
    if (m_pDataObj)
    { 
        m_pDataObj->Release(); 
    }
     
    // If a data object pointer was passed in, save it and
    // extract the file name. 
    if (pDataObj) 
    { 
        m_pDataObj = pDataObj; 
        pDataObj->AddRef(); 
      
        STGMEDIUM   medium;
        FORMATETC   fe = {CF_HDROP, NULL, DVASPECT_CONTENT, -1, TYMED_HGLOBAL};
        UINT        uCount;

        if (SUCCEEDED(m_pDataObj->GetData(&fe, &medium)))
        {
            // Get the count of files dropped.
            uCount = DragQueryFile((HDROP)medium.hGlobal, (UINT)-1, NULL, 0);

            // Get the first file name from the CF_HDROP.
            if (uCount)
                DragQueryFile((HDROP)medium.hGlobal, 0, m_szFile, 
                              sizeof(m_szFile)/sizeof(TCHAR));

            ReleaseStgMedium(&medium);
        }
    }

    // Duplicate the registry handle. 
    if (hRegKey) 
        RegOpenKeyEx(hRegKey, nullptr, 0L, MAXIMUM_ALLOWED, &m_hRegKey); 
    return S_OK; 
}
```

CSampleExtHandler ist der Name der Klasse, die zum Implementieren der -Schnittstelle verwendet wird. Die **Variablen \_ m pIDFolder,** **m \_ pDataObject,** **m \_ szFileName** und **m \_ hRegKey** sind private Variablen, die zum Speichern der übergebenen Informationen verwendet werden. Der Einfachheit halber wird in diesem Beispiel davon ausgegangen, dass das Datenobjekt nur einen Dateinamen enthält. Nachdem die [**FORMATETC-Struktur**](/windows/win32/api/objidl/ns-objidl-formatetc) aus dem Datenobjekt abgerufen wurde, wird [**DragQueryFile**](/windows/desktop/api/Shellapi/nf-shellapi-dragqueryfilea) verwendet, um den Dateinamen aus dem **medium.hGlobal-Member** der **FORMATETC-Struktur** zu extrahieren. Wenn ein Registrierungsschlüssel übergeben wird, verwendet die Methode [**RegOpenKeyEx,**](/windows/win32/api/winreg/nf-winreg-regopenkeyexa) um den Schlüssel zu öffnen, und weist das Handle **m \_ hRegKey zu.**

### <a name="infotip-customization"></a>Infotip-Anpassung

Es gibt zwei Möglichkeiten zum Anpassen von Infotips:

-   Implementieren Sie ein Objekt, das [**IQueryInfo unterstützt,**](/windows/win32/api/shlobj_core/nn-shlobj_core-iqueryinfo) und registrieren Sie dieses Objekt dann unter dem richtigen Unterschlüssel in der Registrierung (siehe Registrieren von [Shell-Erweiterungshandlern](#registering-shell-extension-handlers) weiter unten).
-   Geben Sie eine feste Zeichenfolge oder eine Liste bestimmter Dateieigenschaften an, die angezeigt werden sollen.

Um eine feste Zeichenfolge für eine Namespaceerweiterung anzuzeigen, erstellen Sie einen Eintrag namens `InfoTip` im *{CLSID}-Schlüssel* Ihrer Namespaceerweiterung. Legen Sie den Wert dieses Eintrags entweder auf die literale Zeichenfolge fest, die Sie wie in diesem Beispiel anzeigen möchten, oder auf eine indirekte Zeichenfolge, die eine Ressource und einen Index innerhalb dieser Ressource angibt (zu Lokalisierungszwecken).

```
HKEY_CLASSES_ROOT
   CLSID
      {CLSID}
         InfoTip = InfoTip string for your namespace extension
```

Um eine feste Zeichenfolge für einen Dateityp anzuzeigen, erstellen Sie einen Eintrag namens `InfoTip` im *ProgID-Schlüssel* dieses Dateityps. Legen Sie den Wert dieses Eintrags entweder auf die literale Zeichenfolge fest, die Sie anzeigen möchten, oder auf eine indirekte Zeichenfolge, die eine Ressource und einen Index innerhalb dieser Ressource angibt (zu Lokalisierungszwecken), wie in diesem Beispiel gezeigt.

```
HKEY_CLASSES_ROOT
   ProgID
      InfoTip = Resource.dll, 3
```

Wenn die Shell bestimmte Dateieigenschaften in der Infotip für einen bestimmten Dateityp anzeigen soll, erstellen Sie einen Eintrag namens im `InfoTip` *ProgID-Schlüssel* für diesen Dateityp. Legen Sie den Wert dieses Eintrags auf eine durch Semikolons getrennten Liste von kanonischen Eigenschaftennamen, Formatbezeichnerpaaren (FMTID)/Eigenschaftenbezeichnerpaaren (PID) oder beidem fest. Dieser Wert muss mit "prop:" beginnen, um ihn als Eigenschaftenlistenzeichenfolge zu identifizieren. Wenn Sie "prop:" weglassen, wird der Wert als Literalzeichenfolge angezeigt und als solche angezeigt.

Im folgenden Beispiel ist *propname* ein kanonischer Eigenschaftenname (z.B. System.Date), und *{fmtid}, pid* ist ein [**FMTID-/PID-Paar.**](./objects.md)

```
HKEY_CLASSES_ROOT
   ProgID
      InfoTip = prop:propname;propname;{fmtid},pid;{fmtid},pid
```

Die folgenden Eigenschaftennamen können verwendet werden:



| Eigenschaftenname    | Beschreibung                   | Abgerufen von                                                                             |
|------------------|-------------------------------|--------------------------------------------------------------------------------------------|
| Autor           | Autor des Dokuments        | [**PIDSI \_ AUTHOR**](../stg/the-summary-information-property-set.md)                              |
| Titel            | Titel des Dokuments         | [**PIDSI \_ TITLE**](../stg/the-summary-information-property-set.md)                               |
| Gegenstand          | Zusammenfassung des Betreffs               | [**PIDSI \_ SUBJECT**](../stg/the-summary-information-property-set.md)                             |
| Kommentar          | Dokumentkommentare             | [**PIDSI \_ COMMENT-**](../stg/the-summary-information-property-set.md) oder Ordner-/Treibereigenschaften |
| PageCount        | Anzahl von Seiten               | [**PIDSI \_ PAGECOUNT**](../stg/the-summary-information-property-set.md)                           |
| Name             | Anzeigename                 | Standardordneransicht                                                                       |
| OriginalLocation | Speicherort der ursprünglichen Datei     | Ordner "Kleinbuchstaben" und Papierkorb Ordner                                                    |
| DateDeleted      | Datum, an dem die Datei gelöscht wurde         | Papierkorb Ordner                                                                         |
| Typ             | Dateityp                  | Standardansicht der Ordnerdetails                                                               |
| Size             | Größe der Datei                  | Standardansicht der Ordnerdetails                                                               |
| SyncCopyIn       | Identisch mit OriginalLocation      | Identisch mit OriginalLocation                                                                   |
| Geändert         | Datum der letzten Änderung            | Standardansicht der Ordnerdetails                                                               |
| Erstellt          | Erstellungsdatum                  | Standardansicht der Ordnerdetails                                                               |
| Zugegriffen         | Datum des letzten Zugriffes            | Standardansicht der Ordnerdetails                                                               |
| InFolder         | Verzeichnis, das die Datei enthält | Dokumentsuchergebnisse                                                                    |
| Rang             | Qualität der Such übereinstimmung       | Dokumentsuchergebnisse                                                                    |
| FreeSpace        | Verfügbarer Speicherplatz       | Laufwerke                                                                                |
| NumberOfVisits   | Anzahl von Aufrufen              | Ordner "Favoriten"                                                                           |
| Attribute       | Dateiattribute               | Standardansicht der Ordnerdetails                                                               |
| Company          | Unternehmensname                  | [**PIDDSI \_ COMPANY**](../stg/the-documentsummaryinformation-and-userdefined-property-sets.md)    |
| Category         | Dokumentkategorie             | [**PIDDSI \_ CATEGORY**](../stg/the-documentsummaryinformation-and-userdefined-property-sets.md)   |
| Copyright        | Medienrechte               | [**PIDMSI \_ COPYRIGHT**](../stg/the-documentsummaryinformation-and-userdefined-property-sets.md)  |
| HTMLInfoTipFile  | HTML-InfoTip-Datei             | Desktop.ini-Datei für den Ordner                                                                |



 

## <a name="enhancing-windows-search-with-shell-extension-handlers"></a>Erweitern Windows Suche mit Shell-Erweiterungshandlern

Shell-Erweiterungshandler können verwendet werden, um die Benutzeroberfläche zu verbessern, die von einem Windows Search-Protokollhandler bereitgestellt wird. Um solche Erweiterungen zu aktivieren, muss der unterstützende Shell-Erweiterungshandler so konzipiert sein, dass er in den Suchprotokollhandler als Datenquelle integriert werden kann. Informationen zum Verbessern eines Protokollhandlers für die Windows-Suche durch Die Integration in einen Shell-Erweiterungshandler finden Sie unter Hinzufügen von Symbolen, Vorschauen und [Kontextmenüs.](../search/-search-3x-wds-ph-ui-extensions.md) Weitere Informationen zu Protokollhandlern Windows Search finden Sie unter Developing Protocol Handlers ( [Entwickeln von Protokollhandlern](../search/-search-3x-wds-phaddins.md)).

## <a name="registering-shell-extension-handlers"></a>Registrieren von Shellerweiterungshandlern

Ein Shell-Erweiterungshandlerobjekt muss registriert werden, bevor die Shell es verwenden kann. In diesem Abschnitt wird allgemein erläutert, wie Ein Shell-Erweiterungshandler registriert wird.

Jedes Mal, wenn Sie einen Shell-Erweiterungshandler erstellen oder ändern, ist es wichtig, das System zu benachrichtigen, dass Sie eine Änderung mit [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify)vorgenommen haben, und dabei das **SHCNE \_ ASSOCCHANGED-Ereignis** anzugeben. Wenn Sie **SHChangeNotify nicht aufrufen,** wird die Änderung möglicherweise erst erkannt, wenn das System neu gestartet wird.

Wie bei allen COM-Objekten müssen Sie eine GUID für den Handler mithilfe eines Tools wie UUIDGEN.exe. Erstellen Sie unter **HKEY \_ CLASSES \_ ROOT** CLSID einen Schlüssel, dessen Name \\  die Zeichenfolgenform der GUID ist. Da es sich bei Shell-Erweiterungshandlern um Prozessserver handelt, müssen Sie einen **InProcServer32-Schlüssel** unter dem GUID-Schlüssel erstellen, bei dem der Standardwert auf den Pfad der DLL des Handlers festgelegt ist. Verwenden Sie das Apartmentthreadingmodell.

Jedes Mal, wenn die Shell eine Aktion mit einem Shell-Erweiterungshandler durchführen kann, überprüft sie den entsprechenden Registrierungsschlüssel. Der Schlüssel, unter dem ein Erweiterungshandler registriert ist, steuert daher, wann er aufgerufen wird. Beispielsweise ist es üblich, einen Kontextmenühandler namens zu verwenden, wenn die Shell ein Kontextmenü für einen Member eines [Dateityps anzeigt.](fa-file-types.md) In diesem Fall muss der Handler unter dem **ProgID-Schlüssel** des Dateityps registriert werden.

### <a name="handler-names"></a>Handlernamen

Um einen Shell-Erweiterungshandler zu aktivieren, erstellen Sie einen Unterschlüssel mit dem Namen des Handlerunterschlüssels (siehe unten) unter dem **ShellEx-Unterschlüssel** der **ProgID** (für Dateitypen) oder des Shell-Objekttypnamens (für [vordefinierte Shellobjekte).](#predefined-shell-objects)

Wenn Sie beispielsweise einen Kontextmenü-Erweiterungshandler für MyProgram.1 registrieren möchten, erstellen Sie zunächst den folgenden Unterschlüssel:

```
HKEY_CLASSES_ROOT
   MyProgram.1
      ShellEx
         ContextMenuHandlers
```

Erstellen Sie für die folgenden Handler einen Unterschlüssel unterhalb des Schlüssels "HandlerUnterschlüsselname", dessen Name die Zeichenfolgenversion der CLSID der Shellerweiterung ist. Mehrere Erweiterungen können unter dem Namensschlüssel des Handlerunterschlüssels registriert werden, indem mehrere Unterschlüssel erstellt werden.



| Handler                                               | Schnittstelle          | Name des Handlerunterschlüssels       |
|-------------------------------------------------------|--------------------|---------------------------|
| Kontextmenühandler                                 | IContextMenu       | **ContextMenuHandlers**   |
| Copyhook-Handler                                      | ICopyHook          | **CopyHookHandlers**      |
| Drag &amp; Drop-Handler                                 | IContextMenu       | **DragDropHandlers**      |
| Eigenschaftenblatthandler                                | IShellPropSheetExt | **PropertySheetHandlers** |
| Spaltenanbieterhandler (veraltet in Windows Vista) | IColumnProvider    | **ColumnHandlers**        |



 

Für die folgenden Handler ist der Standardwert des Schlüssels "Handler Subkey Name" die Zeichenfolgenversion der CLSID der Shellerweiterung. Für diese Handler kann nur eine Erweiterung registriert werden.



| Handler                 | Schnittstelle                                         | Name des Handlerunterschlüssels                        |
|-------------------------|---------------------------------------------------|--------------------------------------------|
| Datenhandler            | Idataobject                                       | **Datahandler**                            |
| Drop-Handler            | Idroptarget                                       | **DropHandler**                            |
| Symbolhandler            | IExtractIconA/W                                   | **IconHandler**                            |
| Bildhandler           | IExtractImage                                     | **{BB2E617C-0920-11d1-9A0B-00C04FC2D6C1}** |
| Handler für Miniaturansichtsbilder | IThumbnailProvider                                | **{E357FCCD-A995-4576-B01F-234630154E96}** |
| QuickInfo-Handler         | IQueryInfo                                        | **{00021500-0000-0000-C000-000000000046}** |
| Shelllink (ANSI)      | IShellLinkA                                       | **{000214EE-0000-0000-C000-000000000046}** |
| Shelllink (UNICODE)    | IShellLinkW                                       | **{000214F9-0000-0000-C000-000000000046}** |
| Strukturierter Speicher      | Istorage                                          | **{0000000B-0000-0000-C000-000000000046}** |
| Metadaten                | Ipropertystore                                    | **PropertyHandler**                        |
| Metadaten                | IPropertySetStorage (veraltet in Windows Vista) | **PropertyHandler**                        |
| An Startmenü anheften       | IStartMenuPinnedList                              | **{a2a9545d-a0c2-42b4-9708-a0b2badd77c8}** |
| An Taskleiste anheften          |                                                   | **{90AA3A4E-1CBA-4233-B8BB-535773D48449}** |



 

Die Unterschlüssel, die zum Hinzufügen **von An Startmenü anheften** und An Taskleiste an das Kontextmenü eines Elements **anheften** angegeben sind, sind nur für Dateitypen erforderlich, die den [IsShortCut-Eintrag](./links.md) enthalten.

Die Unterstützung für Spaltenanbieterhandler wurde in Windows Vista entfernt. Ab Windows Vista ist [**IPropertySetStorage**](/windows/win32/api/propidl/nn-propidl-ipropertysetstorage) zugunsten von [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)veraltet.

[**Obwohl IExtractImage**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iextractimage) weiterhin unterstützt wird, wird [**IThumbnailProvider**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) für Windows Vista und höher bevorzugt.

### <a name="predefined-shell-objects"></a>Vordefinierte Shellobjekte

Die Shell definiert zusätzliche Objekte unter **HKEY \_ CLASSES \_ ROOT,** die auf die gleiche Weise wie Dateitypen erweitert werden können. Um beispielsweise einen Eigenschaftenblatthandler für alle Dateien hinzuzufügen, können Sie sich unter dem **PropertySheetHandlers-Schlüssel** registrieren.

```
HKEY_CLASSES_ROOT
   *
      shellex
         PropertySheetHandlers
```

Die folgende Tabelle enthält die verschiedenen Unterschlüssel von **HKEY \_ CLASSES \_ ROOT,** unter denen Erweiterungshandler registriert werden können. Beachten Sie, dass viele Erweiterungshandler nicht unter allen aufgelisteten Unterschlüsseln registriert werden können. Weitere Informationen finden Sie in der Dokumentation des jeweiligen Handlers.



| Unterschlüssel                    | Beschreibung                                                          | Mögliche Handler                                | Version |
|---------------------------|----------------------------------------------------------------------|--------------------------------------------------|---------|
| **\***                    | Alle Dateien                                                            | Kontextmenü, Eigenschaftenblatt, Verben (siehe unten) | Alle     |
| **AllFileSystemObjects**  | Alle Dateien und Dateiordner                                           | Kontextmenü, Eigenschaftenblatt, Verben             | 4.71    |
| **Ordner**                | Alle Ordner                                                          | Kontextmenü, Eigenschaftenblatt, Verben             | Alle     |
| **Verzeichnis**             | Dateiordner                                                         | Kontextmenü, Eigenschaftenblatt, Verben             | Alle     |
| **\\Verzeichnishintergrund** | Hintergrund des Dateiordners                                               | Nur Kontextmenü                               | 4.71    |
| **Laufwerk**                 | Alle Laufwerke in MyComputer, z. B. "C: \\ "                             | Kontextmenü, Eigenschaftenblatt, Verben             | Alle     |
| **Netzwerk**               | Gesamtes Netzwerk (unter "Meine Netzwerkorte")                             | Kontextmenü, Eigenschaftenblatt, Verben             | Alle     |
| **\\Netzwerktyp\\\#**     | Alle Objekte vom Typ \# (siehe unten)                                   | Kontextmenü, Eigenschaftenblatt, Verben             | 4.71    |
| **Netshare**              | Alle Netzwerkfreigaben                                                   | Kontextmenü, Eigenschaftenblatt, Verben             | 4.71    |
| **NetServer**             | Alle Netzwerkserver                                                  | Kontextmenü, Eigenschaftenblatt, Verben             | 4.71    |
| *\_ \_ Netzwerkanbietername* | Alle vom Netzwerkanbieter bereitgestellten Objekte "*\_ \_ Netzwerkanbietername*" | Kontextmenü, Eigenschaftenblatt, Verben             | Alle     |
| **Drucker**              | Alle Drucker                                                         | Kontextmenü, Eigenschaftenblatt                    | Alle     |
| **Audiocd**               | Audio-CD auf CD-Laufwerk                                                 | Nur Verben                                       | Alle     |
| **Dvd**                   | DVD-Laufwerk (Windows 2000)                                             | Kontextmenü, Eigenschaftenblatt, Verben             | 4.71    |



 

Hinweise:

-   Auf das Kontextmenü des Dateiordners wird zugegriffen, indem Sie mit der rechten Maustaste auf einen Dateiordner klicken, jedoch nicht auf den Inhalt des Ordners.
-   "Verben" sind spezielle Befehle, die unter **HKEY \_ CLASSES \_ ROOT** \\ *Subkey* Shell Verb registriert \\  \\  sind.
-   Für **Den** \\ **Netzwerktyp** \\ **\#** ist " " ein \# Netzwerkanbietertypcode im Dezimalformat. Der Typcode des Netzwerkanbieters ist das obere Wort eines Netzwerktyps. Die Liste der Netzwerktypen wird in der Headerdatei Winnetwk.h angegeben (WNNC \_ \_ \* NET-Werte). Beispielsweise ist WNNC \_ NET \_ SHIVA 0x00330000, sodass der entsprechende Typschlüssel **HKEY \_ CLASSES \_ ROOT** \\ **Network** \\ **Type** \\ **51** wäre.
-   "*\_ \_ Netzwerkanbietername*" ist ein Netzwerkanbietername, wie durch [**WNetGetProviderName**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetprovidernamea)angegeben, wobei die Leerzeichen in Unterstriche konvertiert werden. Wenn beispielsweise der Microsoft-Netzwerknetzwerkanbieter installiert ist, lautet der Anbietername "Microsoft Windows Network" und der entsprechende *\_ \_ Netzwerkanbietername* **Microsoft Windows \_ \_ Network.**

### <a name="example-of-an-extension-handler-registration"></a>Beispiel für die Registrierung eines Erweiterungshandlers

Um einen bestimmten Handler zu aktivieren, erstellen Sie einen Unterschlüssel unter dem Typschlüssel des Erweiterungshandlers mit dem Namen des Handlers. Die Shell verwendet nicht den Namen des Handlers, muss sich jedoch von allen anderen Namen unter diesem Typunterschlüssel unterscheiden. Legen Sie den Standardwert des Unterschlüssels name auf die Zeichenfolgenform der GUID des Handlers fest.

Das folgende Beispiel veranschaulicht Registrierungseinträge, die Kontextmenü- und Eigenschaftenblatterweiterungshandler mithilfe eines Beispieldateityps vom Typ ".myp" aktivieren:

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
   CLSID
      {00000000-1111-2222-3333-444444444444}
         InProcServer32
            (Default) = C:\MyDir\MyCommand.dll
            ThreadingModel = Apartment
      {11111111-2222-3333-4444-555555555555}
         InProcServer32
            (Default) = C:\MyDir\MyPropSheet.dll
            ThreadingModel = Apartment
   MyProgram.1
      (Default) = MyProgram Application
      Shellex
         ContextMenuHandler
            MyCommand
               (Default) = {00000000-1111-2222-3333-444444444444}
         PropertySheetHandlers
            MyPropSheet
               (Default) = {11111111-2222-3333-4444-555555555555}
```

Das in diesem Abschnitt beschriebene Registrierungsverfahren muss für alle Windows Systeme befolgt werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Leitfaden zum Implementieren von In-Process-Erweiterungen](shell-and-managed-code.md)
</dt> </dl>

 

 
