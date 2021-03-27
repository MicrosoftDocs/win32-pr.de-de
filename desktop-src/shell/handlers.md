---
description: Die Funktionen der Shell können mit Registrierungs Einträgen und INI-Dateien erweitert werden.
ms.assetid: 74a81e4f-7357-4901-a118-ba44e8892f25
title: Erstellen von Shellerweiterungshandlern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 991f3c1684b7491e2ad29fae29f48164ffdd47cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994702"
---
# <a name="creating-shell-extension-handlers"></a>Erstellen von Shellerweiterungshandlern

Die Funktionen der Shell können mit Registrierungs Einträgen und INI-Dateien erweitert werden. Diese Vorgehensweise zur Erweiterung der Shell ist einfach und für viele Zwecke ausreichend, Sie ist jedoch begrenzt. Wenn Sie z. b. die Registrierung verwenden, um ein benutzerdefiniertes Symbol für einen Dateityp anzugeben, wird das gleiche Symbol für jede Datei dieses Typs angezeigt. Wenn Sie die Shell mit der Registrierung erweitern, können Sie das Symbol für verschiedene Dateien desselben Typs nicht verändern. Andere Aspekte der Shell, wie z. b. das **Eigenschaften Blatt Eigenschaften** , das angezeigt werden kann, wenn mit der rechten Maustaste auf eine Datei geklickt wird, können überhaupt nicht mit der Registrierung geändert werden.

Eine leistungsfähigere und flexiblere Methode zur Erweiterung der Shell ist die Implementierung von *Shellerweiterungs Handlern*. Diese Handler können für eine Reihe von Aktionen implementiert werden, die von der Shell durchgeführt werden können. Vor dem Ausführen der Aktion fragt die Shell den Erweiterungs Handler ab und gibt ihm die Möglichkeit, die Aktion zu ändern. Ein gängiges Beispiel ist ein Erweiterungs Handler für den Kontextmenü. Wenn eine Datei für einen Dateityp implementiert ist, wird Sie jedes Mal abgefragt, wenn auf eine der Dateien mit der rechten Maustaste geklickt wird. Der Handler kann dann zusätzliche Menü Elemente auf Datei-für-Datei-Basis angeben, anstatt denselben Satz für den gesamten Dateityp zu haben.

In diesem Dokument wird erläutert, wie Sie die Erweiterungs Handler implementieren, mit denen Sie eine Vielzahl von shellaktionen ändern können. Die folgenden Handler sind einem bestimmten Dateityp zugeordnet und ermöglichen Ihnen die Angabe von Datei-für-Datei-Basis:



| Handler                                               | BESCHREIBUNG                                                                                                                                                                |
|-------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Kontextmenü Handler](context-menu-handlers.md)    | Wird aufgerufen, bevor das Kontextmenü einer Datei angezeigt wird. Sie ermöglicht das Hinzufügen von Elementen zum Kontextmenü auf Datei Basis.                                               |
| [Daten Handler](how-to-create-data-handlers.md)       | Wird aufgerufen, wenn ein Drag & Drop-Vorgang für dragshell-Objekte ausgeführt wird. Sie ermöglicht es Ihnen, zusätzliche Zwischenablage Formate für das Ablage Ziel bereitzustellen.                        |
| [Drop-Handler](how-to-create-drop-handlers.md)       | Wird aufgerufen, wenn ein Datenobjekt in einer Datei gezogen oder gelöscht wird. Sie ermöglicht es Ihnen, eine Datei in ein Ablage Ziel zu übernehmen.                                                          |
| [Symbol Handler](how-to-create-icon-handlers.md)       | Wird aufgerufen, bevor das Symbol einer Datei angezeigt wird. Dadurch können Sie das Standard Symbol der Datei durch ein benutzerdefiniertes Symbol auf Datei Basis ersetzen.                                    |
| [Eigenschaftenblatthandler](propsheet-handlers.md)      | Wird aufgerufen, bevor das **Eigenschaften** Blatt eines Objekts angezeigt wird. Sie können Seiten hinzufügen oder ersetzen.                                                              |
| [**Miniatur Ansichts Bild Handler**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) | Stellt ein Bild bereit, das das Element darstellt.                                                                                                                                   |
| [**QuickInfo-Handler**](/windows/win32/api/shlobj_core/nn-shlobj_core-iqueryinfo)                 | Stellt Popup Text bereit, wenn der Benutzer mit dem Mauszeiger auf das-Objekt zeigt.                                                                                               |
| [**Metadatenhandler**](/windows/win32/api/propsys/nn-propsys-ipropertystore)     | Bietet Lese-und Schreibzugriff auf Metadaten (Eigenschaften), die in einer Datei gespeichert sind. Dies kann verwendet werden, um die Detailansicht, die Infotipps, die Eigenschaften Seite und die Gruppierungsfunktionen zu erweitern. |



 

Andere Handler sind keinem bestimmten Dateityp zugeordnet, werden jedoch vor einigen shellvorgängen aufgerufen:



| Handler                                                            | BESCHREIBUNG                                                                                                                                  |
|--------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [Spaltenhandler](../lwef/column-handlers.md)                             | Wird von Windows Explorer aufgerufen, bevor die Detailansicht eines Ordners angezeigt wird. Damit können Sie der Detailansicht benutzerdefinierte Spalten hinzufügen.        |
| [Hook-Handler kopieren](how-to-create-copy-hook-handlers.md)          | Wird aufgerufen, wenn ein Ordner oder ein Drucker Objekt verschoben, kopiert, gelöscht oder umbenannt wird. Dies ermöglicht es Ihnen, den Vorgang zu genehmigen oder zu überstehen.   |
| [Drag &amp;amp; Drop-Handler](context-menu-handlers.md)                 | Wird aufgerufen, wenn eine Datei mit der rechten Maustaste gezogen wird. Es ermöglicht Ihnen, das angezeigte Kontextmenü zu ändern.                     |
| [Symbol Überlagerungs Handler](how-to-implement-icon-overlay-handlers.md) | Wird aufgerufen, bevor das Symbol einer Datei angezeigt wird. Damit können Sie ein Overlay für das Symbol der Datei angeben.                                          |
| [Such Handler](../lwef/search-handlers.md)                             | Wird aufgerufen, um eine Suchmaschine zu starten. Damit können Sie eine benutzerdefinierte Suchmaschine implementieren, auf die Sie über das **Startmenü** oder den Windows-Explorer zugreifen können. |



 

Die Details zur Implementierung bestimmter Erweiterungs Handler werden in den oben aufgeführten Abschnitten behandelt. Im restlichen Teil dieses Dokuments werden einige Implementierungsprobleme behandelt, die allen Shellerweiterungs Handlern gemeinsam sind.

-   [Implementieren von Shellerweiterungs Handlern](#implementing-shell-extension-handlers)
    -   [Implementieren von IPersistFile](#implementing-ipersistfile)
    -   [Implementieren von ishellextinit](#implementing-ishellextinit)
    -   [Infotip-Anpassung](#infotip-customization)
-   [Verbessern der Windows-Suche mit Shellerweiterungs Handlern](#enhancing-windows-search-with-shell-extension-handlers)
-   [Registrieren von Shellerweiterungs Handlern](#registering-shell-extension-handlers)
    -   [Handlernamen](#handler-names)
    -   [Vordefinierte Shellobjekte](#predefined-shell-objects)
    -   [Beispiel für eine erweiterungshandlerregistrierung](#example-of-an-extension-handler-registration)
-   [Zugehörige Themen](#related-topics)

## <a name="implementing-shell-extension-handlers"></a>Implementieren von Shellerweiterungs Handlern

Ein Großteil der Implementierung eines Shellerweiterungs-Handlerobjekts hängt vom Typ ab. Es gibt jedoch einige allgemeine Elemente. In diesem Abschnitt werden die Aspekte der Implementierung erläutert, die von allen Shellerweiterungs Handlern gemeinsam genutzt werden.

Viele Shellerweiterungs Handler sind in-Process-Component Object Model (com)-Objekten. Sie müssen eine GUID zugewiesen und wie unter Registrieren von Shellerweiterungs Handlern beschrieben registriert sein. Sie werden als DLLs implementiert und müssen die folgenden Standardfunktionen exportieren:

-   [**DllMain**](../dlls/dllmain.md). Der Standard Einstiegspunkt für die dll.
-   [**DllGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-dllgetclassobject). Macht die Klassenfactory des Objekts verfügbar.
-   [**DllCanUnloadNow**](/windows/win32/api/combaseapi/nf-combaseapi-dllcanunloadnow). COM ruft diese Funktion auf, um zu bestimmen, ob das Objekt Clients bedient. Andernfalls kann das System die DLL entladen und den zugeordneten Speicher freigeben.

Wie alle COM-Objekte müssen Shellerweiterungs Handler eine [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle und eine [Klassenfactory](../com/implementing-iclassfactory.md)implementieren. Die meisten Erweiterungs Handler müssen in Windows XP oder früher entweder eine [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) -oder [**ishellextinit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) -Schnittstelle implementieren. Diese wurden durch [**IInitializeWithStream**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithstream), [**IInitializeWithItem**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem) und [**IInitializeWithFile**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithfile) in Windows Vista ersetzt. Die Shell verwendet diese Schnittstellen, um den Handler zu initialisieren.

Die [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) -Schnittstelle muss folgendermaßen implementiert werden:

-   Daten Handler
-   Drop Handler

In der Vergangenheit waren auch Symbol Handler erforderlich, um [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile)zu implementieren, dies ist jedoch nicht mehr der Fall. Bei Symbol Handlern ist **IPersistFile** jetzt optional, und andere Schnittstellen, wie z. b. [**IInitializeWithItem**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem) , werden bevorzugt.

Die [**ishellextinit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) -Schnittstelle muss wie folgt implementiert werden:

-   Handler für Kontextmenü
-   Drag & Drop-Handler
-   Eigenschaften Blatt Handler

### <a name="implementing-ipersistfile"></a>Implementieren von IPersistFile

Die [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) -Schnittstelle soll es ermöglichen, ein Objekt aus einer Datenträger Datei zu laden oder in eine Datei zu speichern. Sie verfügt über sechs Methoden, zusätzlich zu [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), fünf ihrer eigenen und der [**GetClassID-**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid) Methode, die von [**ipersistent**](/windows/win32/api/objidl/nn-objidl-ipersist)erbt. Bei Shellerweiterungen wird **ipersistent** nur zum Initialisieren eines Shellerweiterungs-Handlerobjekts verwendet. Da in der Regel kein Lese-oder Schreibzugriff auf den Datenträger erforderlich ist, benötigen nur die Methoden **GetClassID** und [**Load**](/windows/win32/api/objidl/nf-objidl-ipersistfile-load) eine nicht Token-Implementierung.

Die Shell ruft zuerst [**GetClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid) auf, und die-Funktion gibt den Klassen Bezeichner (CLSID) des Erweiterungs Handler-Objekts zurück. Die Shell ruft dann [**Load**](/windows/win32/api/objidl/nf-objidl-ipersistfile-load) auf und übergibt zwei Werte. Der erste, *pszFileName*, ist eine Unicode-Zeichenfolge mit dem Namen der Datei oder des Ordners, mit der die Shell arbeiten soll. Die zweite ist der *dwmode*, der den Datei Zugriffsmodus angibt. Da der Zugriff auf Dateien in der Regel nicht erforderlich ist, ist *dwmode* normalerweise 0 (null). Die-Methode speichert diese Werte nach Bedarf für den späteren Verweis.

Das folgende Code Fragment veranschaulicht, wie ein typischer shellerweiterungshandler die Methoden [**GetClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid) und [**Load**](/windows/win32/api/objidl/nf-objidl-ipersistfile-load) implementiert. Es ist für die Handhabung von ANSI oder Unicode konzipiert. CLSID \_ sampleexthandler ist die GUID des Erweiterungs Handler-Objekts, und csampleexthandler ist der Name der Klasse, die zum Implementieren der Schnittstelle verwendet wird. Die Variablen **m \_ szFilename** und **m \_ dwmode** sind private Variablen, die zum Speichern des Namens und der Zugriffsflags der Datei verwendet werden.


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

### <a name="implementing-ishellextinit"></a>Implementieren von ishellextinit

Die [**ishellextinit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) -Schnittstelle verfügt über nur eine Methode, [**ishellextinit:: Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize), zusätzlich zu [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown). Die-Methode verfügt über drei Parameter, die von der Shell verwendet werden können, um verschiedene Arten von Informationen zu übergeben. Welche Werte weitergegeben werden, hängt vom Typ des Handlers ab, und einige können auf **null** festgelegt werden.

-   *pidfolder* enthält einen Ordner Zeiger auf eine Element Bezeichner-Liste (PIDL). Bei Eigenschaften Blatt Erweiterungen ist der Wert **null**. Bei Kontextmenü Erweiterungen ist dies die PIDL des Ordners, der das Element enthält, dessen Kontextmenü angezeigt wird. Bei nicht standardmäßigen Drag & Drop-Handlern ist dies die PIDL des Ziel Ordners.
-   *pdataobject* enthält einen Zeiger auf die [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) -Schnittstelle eines Datenobjekts. Das Datenobjekt enthält einen oder mehrere Dateinamen im [CF- \_ HDROP](dragdrop.md) -Format.
-   *hregkey* enthält einen Registrierungsschlüssel für das Datei Objekt oder den Ordnertyp.

Die [**ishellextinit:: Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) -Methode speichert den Dateinamen, den [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) -Zeiger und den Registrierungsschlüssel nach Bedarf für die spätere Verwendung. Das folgende Code Fragment veranschaulicht die Implementierung von **ishellextinit:: Initialize**. Der Einfachheit halber wird in diesem Beispiel davon ausgegangen, dass das Datenobjekt nur eine einzelne Datei enthält. Im Allgemeinen kann es mehrere Dateien enthalten, die jeweils extrahiert werden müssen.


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

Csampleexthandler ist der Name der Klasse, die verwendet wird, um die Schnittstelle zu implementieren. Die Variablen " **m \_ pidfolder**", " **m \_ pdataobject**", " **m \_ szFilename**" und " **m \_ hregkey** " sind private Variablen, die zum Speichern der übergebenen Informationen verwendet werden. Der Einfachheit halber wird in diesem Beispiel davon ausgegangen, dass nur ein Dateiname vom Datenobjekt gespeichert wird. Nachdem die [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) -Struktur aus dem Datenobjekt abgerufen wurde, wird [**dragqueryfile**](/windows/desktop/api/Shellapi/nf-shellapi-dragqueryfilea) verwendet, um den Dateinamen aus dem **mittleren. HGLOBAL** -Member der **FORMATETC** -Struktur zu extrahieren. Wenn ein Registrierungsschlüssel an die-Methode übermittelt wird, verwendet die-Methode [**RegOpenKeyEx**](/windows/win32/api/winreg/nf-winreg-regopenkeyexa) , um den Schlüssel zu öffnen, und weist dem **m \_ hregkey** das Handle zu.

### <a name="infotip-customization"></a>Infotip-Anpassung

Es gibt zwei Möglichkeiten zum Anpassen von infotips:

-   Implementieren Sie ein Objekt, das [**iqueryinfo**](/windows/win32/api/shlobj_core/nn-shlobj_core-iqueryinfo) unterstützt, und registrieren Sie dieses Objekt dann unter dem richtigen Unterschlüssel in der Registrierung (siehe [Registrieren von shellerweiterungshandlern](#registering-shell-extension-handlers) unten).
-   Geben Sie eine festgelegte Zeichenfolge oder eine Liste mit bestimmten Dateieigenschaften an, die angezeigt werden sollen.

Um eine Zeichenfolge fester Zeichenfolge für eine Namespace Erweiterung anzuzeigen, erstellen `InfoTip` Sie einen Eintrag mit dem Namen im *{CLSID}* -Schlüssel der Namespace Erweiterung. Legen Sie den Wert dieses Eintrags entweder auf die Literalzeichenfolge fest, die Sie anzeigen möchten, wie in diesem Beispiel gezeigt, oder eine indirekte Zeichenfolge, die eine Ressource und einen Index innerhalb dieser Ressource angibt (zu Lokalisierungs Zwecken).

```
HKEY_CLASSES_ROOT
   CLSID
      {CLSID}
         InfoTip = InfoTip string for your namespace extension
```

Um eine festgelegte Zeichenfolge für einen Dateityp anzuzeigen, erstellen Sie einen Eintrag `InfoTip` mit dem Namen im *ProgID* -Schlüssel dieses Dateityps. Legen Sie den Wert dieses Eintrags entweder auf die Literale Zeichenfolge fest, die Sie anzeigen möchten, oder eine indirekte Zeichenfolge, die eine Ressource und einen Index innerhalb dieser Ressource (zu Lokalisierungs Zwecken) angibt, wie in diesem Beispiel gezeigt.

```
HKEY_CLASSES_ROOT
   ProgID
      InfoTip = Resource.dll, 3
```

Wenn Sie möchten, dass die Shell bestimmte Dateieigenschaften im Infotipp für einen bestimmten Dateityp anzeigt, erstellen Sie `InfoTip` im *ProgID* -Schlüssel für diesen Dateityp einen Eintrag mit dem Namen. Legen Sie den Wert dieses Eintrags auf eine durch Semikolons getrennte Liste von kanonischen Eigenschaftsnamen, Format Bezeichnern (fmtid)/Property Identifier (PID)-Paaren oder beides fest. Dieser Wert muss mit "prop:" beginnen, um ihn als Eigenschaften Listen Zeichenfolge zu identifizieren. Wenn Sie "prop:" weglassen, wird der Wert als Literalzeichenfolge betrachtet und als solche angezeigt.

Im folgenden Beispiel ist *propName* ein kanonischer Eigenschaften Name (z. b. System. Date) und *{fmtid}, PID* ist ein [**fmtid/PID-**](./objects.md) Paar.

```
HKEY_CLASSES_ROOT
   ProgID
      InfoTip = prop:propname;propname;{fmtid},pid;{fmtid},pid
```

Die folgenden Eigenschaften Namen können verwendet werden:



| Eigenschaftenname    | BESCHREIBUNG                   | Abgerufen von                                                                             |
|------------------|-------------------------------|--------------------------------------------------------------------------------------------|
| Autor           | Autor des Dokuments        | [**pidsi- \_ Autor**](../stg/the-summary-information-property-set.md)                              |
| Titel            | Titel des Dokuments         | [**pidsi- \_ Titel**](../stg/the-summary-information-property-set.md)                               |
| Subject          | Themen Zusammenfassung               | [**pidsi- \_ Betreff**](../stg/the-summary-information-property-set.md)                             |
| Comment          | Dokument Kommentare             | [**Pidsi \_ Kommentar**](../stg/the-summary-information-property-set.md) -oder Ordner-/Treibereigenschaften |
| PageCount        | Anzahl von Seiten               | [**pidsi \_ Page count**](../stg/the-summary-information-property-set.md)                           |
| Name             | Anzeigename                 | Standard Ordneransicht                                                                       |
| Ursprungs Zuordnung | Speicherort der ursprünglichen Datei     | Ordner "Briefkasten" und "Papierkorb"                                                    |
| Datedeleted      | Die Datums Datei wurde gelöscht.         | Papierkorb Ordner                                                                         |
| type             | Dateityp                  | Ansicht "Standard Ordner Details"                                                               |
| Size             | Größe der Datei                  | Ansicht "Standard Ordner Details"                                                               |
| Synccopyin       | Identisch mit "Ursprungs Zuordnung"      | Identisch mit "Ursprungs Zuordnung"                                                                   |
| Geändert         | Datum der letzten Änderung            | Ansicht "Standard Ordner Details"                                                               |
| Erstellt          | Erstellungsdatum                  | Ansicht "Standard Ordner Details"                                                               |
| Auf         | Datum des letzten Zugriffs            | Ansicht "Standard Ordner Details"                                                               |
| InFolder         | Verzeichnis, das die Datei enthält | Dokument Suchergebnisse                                                                    |
| Rang             | Qualität der Such Übereinstimmung       | Dokument Suchergebnisse                                                                    |
| FreeSpace        | Verfügbarer Speicherplatz       | Laufwerke                                                                                |
| Anzahl von besuchen   | Anzahl von Aufrufen              | Ordner "Favoriten"                                                                           |
| Attributes       | Dateiattribute               | Ansicht "Standard Ordner Details"                                                               |
| Company          | Unternehmensname                  | [**piddsi- \_ Unternehmen**](../stg/the-documentsummaryinformation-and-userdefined-property-sets.md)    |
| Kategorie         | Dokument Kategorie             | [**piddsi- \_ Kategorie**](../stg/the-documentsummaryinformation-and-userdefined-property-sets.md)   |
| Copyright        | Medien Copyright               | [**pidmsi \_ Copyright**](../stg/the-documentsummaryinformation-and-userdefined-property-sets.md)  |
| Htmlinfotipfile  | HTML-infotip-Datei             | Datei für Ordner Desktop.ini                                                                |



 

## <a name="enhancing-windows-search-with-shell-extension-handlers"></a>Verbessern der Windows-Suche mit Shellerweiterungs Handlern

Shellerweiterungs Handler können verwendet werden, um die Benutzer Leistung eines Windows Search-Protokollhandler zu verbessern. Um solche Erweiterungen zu ermöglichen, muss der Handler für die unterstützende Shellerweiterung so entworfen werden, dass er in den Such Protokollhandler als Datenquelle integriert wird. Weitere Informationen zum Verbessern eines Windows Search-Protokoll Handlers durch Integration in einen Shellerweiterungs Handler finden Sie unter [Hinzufügen von Symbolen, Vorschauen und Kontextmenüs](../search/-search-3x-wds-ph-ui-extensions.md). Weitere Informationen zu Windows Search-Protokoll Handlern finden Sie unter [entwickeln von Protokoll Handlern](../search/-search-3x-wds-phaddins.md).

## <a name="registering-shell-extension-handlers"></a>Registrieren von Shellerweiterungs Handlern

Ein shellerweiterungshandlerobjekt muss registriert werden, bevor es von der Shell verwendet werden kann. In diesem Abschnitt wird die Registrierung eines Shellerweiterungs Handlers ausführlicher erläutert.

Jedes Mal, wenn Sie einen Shellerweiterungs Handler erstellen oder ändern, ist es wichtig, das System zu benachrichtigen, dass Sie eine Änderung mit [**shchangenotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify)vorgenommen haben. dabei wird das Ereignis **shcne \_ assocchanged** angegeben. Wenn Sie **shchangenotify** nicht aufrufen, wird die Änderung möglicherweise erst erkannt, wenn das System neu gestartet wird.

Wie bei allen COM-Objekten müssen Sie mithilfe eines Tools wie UUIDGEN.exe eine GUID für den Handler erstellen. Erstellen Sie einen Schlüssel unter **HKEY \_ Classes \_ root** \\ **CLSID** , deren Name die Zeichen folgen Form der GUID ist. Da es sich bei Shellerweiterungs Handlern um Prozess interne Server handelt, müssen Sie einen **InProcServer32** -Schlüssel unter dem GUID-Schlüssel erstellen, wobei der Standardwert auf den Pfad der DLL des Handler festgelegt ist. Verwenden Sie das Apartment Threading Modell.

Jedes Mal, wenn die Shell eine Aktion ausführt, die einen Shellerweiterungs Handler einschließen kann, wird der entsprechende Registrierungsschlüssel überprüft. Der Schlüssel, unter dem ein Erweiterungs Handler registriert ist, steuert, wann er aufgerufen wird. Beispielsweise ist es üblich, dass ein Kontextmenü Handler aufgerufen wird, wenn die Shell ein Kontextmenü für einen Member eines [Dateityps](fa-file-types.md)anzeigt. In diesem Fall muss der Handler unter dem **ProgID** -Schlüssel des Dateityps registriert werden.

### <a name="handler-names"></a>Handlernamen

Erstellen Sie zum Aktivieren eines Shellerweiterungs Handlers einen Unterschlüssel mit dem Namen des unter Schlüssels des Handlers (siehe unten) unter dem **shellex** -Unterschlüssel der **ProgID** (für Dateitypen) oder dem shellobjekttypnamen (für [vordefinierte Shellobjekte](#predefined-shell-objects)).

Wenn Sie z. b. einen Erweiterungs Handler für das Kontextmenü für MyProgram. 1 registrieren möchten, erstellen Sie zunächst den folgenden Unterschlüssel:

```
HKEY_CLASSES_ROOT
   MyProgram.1
      ShellEx
         ContextMenuHandlers
```

Erstellen Sie für die folgenden Handler einen Unterschlüssel unter dem Schlüssel Name des unter Schlüssels "Handler", dessen Name die Zeichen folgen Version der CLSID der Shellerweiterung ist. Mehrere Erweiterungen können unter dem namens Schlüssel für den Unterschlüssel des Handlers registriert werden, indem mehrere Unterschlüssel erstellt werden.



| Handler                                               | Schnittstelle          | Name des unter Schlüssels des Handlers       |
|-------------------------------------------------------|--------------------|---------------------------|
| Kontextmenü Handler                                 | IContextMenu       | **ContextMenuHandlers**   |
| Copyhook-Handler                                      | Icopyhook          | **Copyhuokhandlers**      |
| Drag &amp; Drop-Handler                                 | IContextMenu       | **Dragdrophandlers**      |
| Eigenschaftenblatthandler                                | Ishellpropsheetext | **Propertysheethandlers** |
| Spalten Anbieter Handler (in Windows Vista veraltet) | Icolumnprovider    | **Columnhandlers**        |



 

Bei den folgenden Handlern ist der Standardwert für den Schlüssel Name des unter Schlüssels "Handler" die Zeichen folgen Version der CLSID der Shellerweiterung. Für diese Handler kann nur eine Erweiterung registriert werden.



| Handler                 | Schnittstelle                                         | Name des unter Schlüssels des Handlers                        |
|-------------------------|---------------------------------------------------|--------------------------------------------|
| Daten Handler            | IDataObject                                       | **DataHandler**                            |
| Drop-Handler            | IDropTarget                                       | **Drophandler**                            |
| Symbol Handler            | Iextracticona/W                                   | **Iconhandler**                            |
| Bild Handler           | Iextractimage                                     | **{BB2E617C-0920-11d1-9A0B-00C04FC2D6C1}** |
| Miniatur Ansichts Bild Handler | IThumbnailProvider                                | **{E357FCCD-A995-4576-B01F-234630154E96}** |
| QuickInfo-Handler         | Iqueryinfo                                        | **{00021500-0000-0000-C000-000000000046}** |
| Shelllink (ANSI)      | IShellLinkA                                       | **{000214ee-0000-0000-C000-000000000046}** |
| Shelllink (Unicode)    | Ishelllinkw                                       | **{0002149-0000-0000-C000-000000000046}** |
| Strukturierter Speicher      | IStorage                                          | **{0000000b-0000-0000-C000-000000000046}** |
| Metadaten                | IPropertyStore                                    | **Propertyhandler**                        |
| Metadaten                | IPropertySetStorage (in Windows Vista veraltet) | **Propertyhandler**                        |
| An Startmenü anheften       | Istartmenupinnedlist                              | **{a2a9545d-a0c2-42b4-9708-a0b2badd77c8}** |
| An Taskleiste anheften          |                                                   | **{90aa3a4e-1cba-4233-B8BB-535773d48449}** |



 

Die angegebenen Unterschlüssel zum Hinzufügen einer **PIN zum Startmenü** und zum Anheften **an die Taskleiste** an das Kontextmenü eines Elements sind nur für Dateitypen erforderlich, die den [IsShortcut](./links.md) -Eintrag enthalten.

Die Unterstützung von Spalten Anbieter Handlern wurde in Windows Vista entfernt. Außerdem wurde [**IPropertySetStorage**](/windows/win32/api/propidl/nn-propidl-ipropertysetstorage) ab Windows Vista zugunsten von [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)als veraltet eingestuft.

Obwohl [**iextractimage**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iextractimage) weiterhin unterstützt wird, wird [**IThumbnailProvider**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) für Windows Vista und höher bevorzugt.

### <a name="predefined-shell-objects"></a>Vordefinierte Shellobjekte

Die Shell definiert zusätzliche Objekte unter **HKEY \_ Classes \_ root** , die auf die gleiche Weise wie Dateitypen erweitert werden können. Wenn Sie z. b. einen Eigenschaften Blatt Handler für alle Dateien hinzufügen möchten, können Sie sich unter dem **propertysheethandlers** -Schlüssel registrieren.

```
HKEY_CLASSES_ROOT
   *
      shellex
         PropertySheetHandlers
```

In der folgenden Tabelle sind die verschiedenen Unterschlüssel von **HKEY- \_ Klassen \_ root** , unter denen Erweiterungs Handler registriert werden können, zu finden. Beachten Sie, dass viele Erweiterungs Handler nicht unter allen aufgelisteten unter Schlüsseln registriert werden können. Weitere Informationen finden Sie in der Dokumentation des jeweiligen Handlers.



| Unterschlüssel                    | BESCHREIBUNG                                                          | Mögliche Handler                                | Version |
|---------------------------|----------------------------------------------------------------------|--------------------------------------------------|---------|
| **\** _                    | Alle Dateien                                                            | Kontextmenü, Eigenschaften Blatt, Verben (siehe unten) | All     |
| _ *AllFilesystemObjects**  | Alle Dateien und Datei Ordner                                           | Kontextmenü, Eigenschaften Blatt, Verben             | 4.71    |
| **Ordner**                | Alle Ordner                                                          | Kontextmenü, Eigenschaften Blatt, Verben             | All     |
| **Verzeichnis**             | Datei Ordner                                                         | Kontextmenü, Eigenschaften Blatt, Verben             | All     |
| **Verzeichnis \\ Hintergrund** | Hintergrund des Datei Ordners                                               | Nur Kontextmenü                               | 4.71    |
| **Laufwerk**                 | Alle Laufwerke in "MyComputer", z. b. "C: \\ "                             | Kontextmenü, Eigenschaften Blatt, Verben             | All     |
| **Network**               | Gesamtes Netzwerk (unter "meine Netzwerk Plätze")                             | Kontextmenü, Eigenschaften Blatt, Verben             | All     |
| **\\Netzwerktyp\\\#**     | Alle Objekte des Typs \# (siehe unten)                                   | Kontextmenü, Eigenschaften Blatt, Verben             | 4.71    |
| **NetShare**              | Alle Netzwerkfreigaben                                                   | Kontextmenü, Eigenschaften Blatt, Verben             | 4.71    |
| **Netserver**             | Alle Netzwerkserver                                                  | Kontextmenü, Eigenschaften Blatt, Verben             | 4.71    |
| *Name des Netzwerk \_ Anbieters \_* | Alle Objekte, die vom Netzwerkanbieter "*Netzwerk \_ Anbieter \_ Name*" bereitgestellt werden | Kontextmenü, Eigenschaften Blatt, Verben             | All     |
| **Drucker**              | Alle Drucker                                                         | Kontextmenü, Eigenschaften Blatt                    | All     |
| **AudioCD**               | AudioCD in CD-Laufwerk                                                 | Nur Verben                                       | All     |
| **DVD**                   | DVD-Laufwerk (Windows 2000)                                             | Kontextmenü, Eigenschaften Blatt, Verben             | 4.71    |



 

Hinweise:

-   Der Zugriff auf das Kontextmenü des Datei Ordners wird durch einen Rechtsklick innerhalb eines Datei Ordners, aber nicht über den Inhalt des Ordners erreicht.
-   "Verbs" sind spezielle Befehle, die unter **HKEY \_ Classes \_ root** \\ *subkey* \\ **Shell** \\ **Verb** registriert sind.
-   Für den \\ **Netzwerktyp** \\ **\#** \# ist "" ein Netzwerk Anbietertyp Code in Dezimal. Der Typ Code des Netzwerk Anbieters ist das hohe Wort eines Netzwerk Typs. Die Liste der Netzwerktypen wird in der "winnetwk. h"-Header Datei (wnnc \_ net \_ \* Values) angegeben. Beispielsweise ist wnnc \_ net \_ Shiva 0x00330000, daher wäre der entsprechende Typschlüssel **HKEY \_ Classes \_ root** \\ **Network** \\ **Type** \\ **51** .
-   der *Name \_ des \_ Netzwerk Anbieters wird* von [**wnetgetprovidername**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetprovidernamea)angegeben, wobei die Leerzeichen in Unterstriche konvertiert werden. Wenn z. b. der Microsoft-Netzwerk Netzwerkanbieter installiert ist, lautet sein Anbieter Name "Microsoft Windows-Netzwerk", und der entsprechende *Netzwerk \_ Anbieter \_ Name* lautet **Microsoft \_ Windows- \_ Netzwerk**.

### <a name="example-of-an-extension-handler-registration"></a>Beispiel für eine erweiterungshandlerregistrierung

Um einen bestimmten Handler zu aktivieren, erstellen Sie unter dem Typ des erweiterungshandlers einen Unterschlüssel mit dem Namen des Handlers. Die Shell verwendet nicht den Namen des Handlers, aber Sie muss sich von allen anderen Namen unter diesem typunter Schlüssel unterscheiden. Legen Sie den Standardwert des Namens unter Schlüssels auf die Zeichen folgen Form der GUID des Handlers fest.

Das folgende Beispiel veranschaulicht Registrierungseinträge, die Erweiterungs Handler für Kontextmenü und Eigenschaften Blätter mit dem Dateityp example. MYP aktivieren:

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

Das in diesem Abschnitt beschriebene Registrierungsverfahren muss für alle Windows-Systeme befolgt werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Leitfaden für die Implementierung von In-Process-Erweiterungen](shell-and-managed-code.md)
</dt> </dl>

 

 
