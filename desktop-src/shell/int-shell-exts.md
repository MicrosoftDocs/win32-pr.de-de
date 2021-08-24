---
description: Ein Großteil der Implementierung eines Shell-Erweiterungshandlerobjekts wird durch seinen Typ vorgegeben. Es gibt jedoch einige allgemeine Elemente. In diesem Thema werden die Aspekte der Implementierung erläutert, die von allen Shellerweiterungshandlern gemeinsam genutzt werden.
ms.assetid: ce21ca0f-157c-4f69-bcf9-dc259c3bac80
title: Initialisieren von Shellerweiterungshandlern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82f83a47400cff5d0fa4628f6f6f9d9ba74b158947c7843f61831d54f62c7a6f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119661220"
---
# <a name="initializing-shell-extension-handlers"></a>Initialisieren von Shellerweiterungshandlern

Ein Großteil der Implementierung eines Shell-Erweiterungshandlerobjekts wird durch seinen Typ vorgegeben. Es gibt jedoch einige allgemeine Elemente. In diesem Thema werden die Aspekte der Implementierung erläutert, die von allen Shellerweiterungshandlern gemeinsam genutzt werden.

Alle Shellerweiterungshandler sind COM-Objekte (In-Process Component Object Model). Ihnen muss eine GUID zugewiesen und registriert werden, wie unter [Registrieren von Shellerweiterungshandlern](handlers.md)beschrieben. Sie werden als DLLs implementiert und müssen die folgenden Standardfunktionen exportieren:

-   [**DllMain**](../dlls/dllmain.md). Der Standardeinstiegspunkt für die DLL.
-   [**DllGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-dllgetclassobject). Macht die Klassenfactory des Objekts verfügbar.
-   [**DllCanUnloadNow**](/windows/win32/api/combaseapi/nf-combaseapi-dllcanunloadnow). COM ruft diese Funktion auf, um zu bestimmen, ob das Objekt Clients bedient. Andernfalls kann das System die DLL entladen und den zugeordneten Arbeitsspeicher freigeben.

Wie alle COM-Objekte müssen Shellerweiterungshandler eine [**IUnknown-Schnittstelle**](/windows/win32/api/unknwn/nn-unknwn-iunknown) und eine [Klassenfactory](../com/implementing-iclassfactory.md)implementieren. Die meisten müssen auch eine [**IPersistFile-**](/windows/win32/api/objidl/nn-objidl-ipersistfile) oder [**IShellExtInit-Schnittstelle**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) in Windows XP oder früher implementieren. Diese wurden in Windows Vista durch [**IInitializeWithStream,**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithstream) [**IInitializeWithItem**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem) und [**IInitializeWithFile**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithfile) ersetzt. Die Shell verwendet diese Schnittstellen, um den Handler zu initialisieren.

Die [**IPersistFile-Schnittstelle**](/windows/win32/api/objidl/nn-objidl-ipersistfile) muss wie folgt implementiert werden:

-   Symbolhandler
-   Datenhandler
-   Löschen von Handlern

Die [**IShellExtInit-Schnittstelle**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) muss wie folgt implementiert werden:

-   Kontextmenühandler
-   Drag & Drop-Handler
-   Eigenschaftenblatthandler

Die folgenden Themen werden im weiteren Verlauf dieses Themas erläutert:

-   [Implementieren von IPersistFile](#implementing-ipersistfile)
-   [Implementieren von IShellExtInit](#implementing-ishellextinit)
-   [Anpassung von Infotips](#infotip-customization)
-   [Zugehörige Themen](#related-topics)

## <a name="implementing-ipersistfile"></a>Implementieren von IPersistFile

Die [**IPersistFile-Schnittstelle**](/windows/win32/api/objidl/nn-objidl-ipersistfile) ist so konzipiert, dass ein Objekt aus einer Datenträgerdatei geladen oder darin gespeichert werden kann. Es verfügt über sechs Methoden zusätzlich zu [**IUnknown,**](/windows/win32/api/unknwn/nn-unknwn-iunknown)fünf eigene Methoden und die [**GetClassID-Methode,**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid) die sie von [**IPersist**](/windows/win32/api/objidl/nn-objidl-ipersist)erbt. Bei Shell-Erweiterungen wird **IPersist** nur zum Initialisieren eines Shell-Erweiterungshandlerobjekts verwendet. Da in der Regel kein Lese- oder Schreibzugriff auf den Datenträger erforderlich ist, erfordern nur die Methoden **GetClassID** und [**Load**](/windows/win32/api/objidl/nf-objidl-ipersistfile-load) eine Nichttokenimplementierungen.

Die Shell ruft zuerst [**GetClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid) auf, und die Funktion gibt den Klassenbezeichner (CLSID) des Erweiterungshandlerobjekts zurück. Die Shell ruft dann [**Load auf**](/windows/win32/api/objidl/nf-objidl-ipersistfile-load) und übergibt zwei Werte. Die erste , *pszFile,* ist eine Unicode-Zeichenfolge mit dem Namen der Datei oder des Ordners, für die Shell ausgeführt werden soll. Der zweite ist *dwMode,* der den Dateizugriffsmodus angibt. Da normalerweise kein Zugriff auf Dateien erforderlich ist, ist *dwMode* in der Regel 0 (null). Die -Methode speichert diese Werte nach Bedarf für einen späteren Verweis.

Das folgende Codefragment veranschaulicht, wie ein typischer Shellerweiterungshandler die [**Methoden GetClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid) und [**Load**](/windows/win32/api/objidl/nf-objidl-ipersistfile-load) implementiert. Es ist für die Verarbeitung von ANSI oder Unicode konzipiert. CLSID \_ SampleExtHandler ist die GUID des Erweiterungshandlerobjekts, und CSampleShellExtension ist der Name der Klasse, die zum Implementieren der -Schnittstelle verwendet wird. Die Variablen **m \_ szFileName** und **m \_ dwMode** sind private Variablen, die zum Speichern des Dateinamens und der Zugriffsflags verwendet werden.


```C++
class CSampleShellExtension : public IPersistFile
{
    // Method declarations not included

    private:
    WCHAR m_szFileName[MAX_PATH];    // The file name
    DWORD m_dwMode;                  // The file access mode
}

IFACEMETHODIMP CSampleShellExtension::GetClassID(__out CLSID *pCLSID)
{
    *pCLSID = CLSID_SampleExtHandler;
}

IFACEMETHODIMP CSampleShellExtension::Load(PCWSTR pszFile, DWORD dwMode)
{
    m_dwMode = dwMode;
    return StringCchCopy(m_szFileName, ARRAYSIZE(m_szFileName), pszFile); 
}

// The implementation sample is continued in the next section.
```



## <a name="implementing-ishellextinit"></a>Implementieren von IShellExtInit

Die [**IShellExtInit-Schnittstelle**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) verfügt zusätzlich zu [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)nur über eine Methode, [**IShellExtInit::Initialize.**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) Die -Methode verfügt über drei Parameter, mit denen die Shell verschiedene Informationstypen übergeben kann. Die übergebenen Werte hängen vom Typ des Handlers ab, und einige können auf **NULL** festgelegt werden.

-   *pidlFolder* enthält den Zeiger eines Ordners auf eine Elementbezeichnerliste (PIDL). Dies ist eine absolute PIDL. Bei Eigenschaftenblatterweiterungen ist dieser Wert **NULL.** Bei Kontextmenüerweiterungen ist es die PIDL des Ordners, der das Element enthält, dessen Kontextmenü angezeigt wird. Bei Drag & Drop-Handlern ohne Standardmäßigkeit ist dies die PIDL des Zielordners.
-   *pDataObject* enthält einen Zeiger auf die [**IDataObject-Schnittstelle**](/windows/win32/api/objidl/nn-objidl-idataobject) eines Datenobjekts. Das Datenobjekt enthält mindestens einen Dateinamen im [CF \_ HDROP-Format.](dragdrop.md)
-   *hRegKey* enthält einen Registrierungsschlüssel für das Dateiobjekt oder den Ordnertyp.

Die [**IShellExtInit::Initialize-Methode**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) speichert den Dateinamen, [**den IDataObject-Zeiger**](/windows/win32/api/objidl/nn-objidl-idataobject) und den Registrierungsschlüssel nach Bedarf für die spätere Verwendung. Das folgende Codefragment veranschaulicht eine Implementierung von **IShellExtInit::Initialize**. Der Einfachheit halber wird in diesem Beispiel davon ausgegangen, dass das Datenobjekt nur eine einzelne Datei enthält. Im Allgemeinen kann das Datenobjekt mehrere Dateien enthalten, von denen jede extrahiert werden muss.


```C++
// This code continues the CSampleShellExtension sample shown in the
// "Implementing IPersistFile" section above.

class CSampleShellExtension : public IShellExtInit
{
    // Method declarations not included
    
    private:
    // IDList of the folder for extensions invoked on the folder, such as 
    // background context menu handlers or nondefault drag-and-drop handlers. 
    PIDLIST_ABSOLUTE m_pidlFolder;
    
    // The data object contains an expression of the items that the handler is 
    // being initialized for. Use SHCreateShellItemArrayFromDataObject to 
    // convert this object to an array of items. Use SHGetItemFromObject if you
    // are only interested in a single Shell item. If you need a file system
    // path, use IShellItem::GetDisplayName(SIGDN_FILESYSPATH, ...).
    IDataObject *m_pdtobj;
    
    // For context menu handlers, the registry key provides access to verb 
    // instance data that might be stored there. This is a rare feature to use 
    // so most extensions do not need this variable.
    HKEY m_hRegKey;             
}
    
// This method must be very efficient. Do not do any unnecessary work here.
// Use Initialize to acquire resources that will be used later.

IFACEMETHODIMP CSampleShellExtension::Initialize(__in_opt PCIDLIST_ABSOLUTE pidlFolder,
                                                 __in_opt IDataObject *pDataObject, 
                                                 __in_opt HKEY hRegKey) 
{ 
    // In some cases, handlers are initialized multiple times. Therefore, 
    // clear any previous state here.
    CoTaskMemFree(m_pidlFolder);
    m_pidlFolder = NULL;
    
    if (m_pdtobj)
    { 
        m_pdtobj->Release(); 
    }
    
    if (m_hRegKey)
    {
        RegCloseKey(m_hRegKey);
        m_hRegKey = NULL;
    }
    
    // Capture the inputs for use later.
    HRESULT hr = S_OK;
    
    if (pidlFolder)
    {
        m_pidlFolder = ILClone(pidlFolder);   // Make a copy to use later.
        hr = m_pidlFolder ? S_OK : E_OUTOFMEMORY;
    }
    
    if (SUCCEEDED(hr))
    {
        // If a data object pointer was passed into the method, save it and
        // extract the file name. 
        if (pDataObject) 
        { 
            m_pdtobj = pDataObject; 
            m_pdtobj->AddRef(); 
        }
    
        // It is uncommon to use the registry handle, but if you need it,
        // duplicate it now.
        if (hRegKey)
        {
            LSTATUS const result = RegOpenKeyEx(hRegKey, NULL, 0, KEY_READ, &m_hRegKey); 
            hr = HRESULT_FROM_WIN32(result);
        }
    }
    
    return hr;
}
```



## <a name="infotip-customization"></a>Anpassung von Infotips

Es gibt zwei Möglichkeiten, Infotips anzupassen. Eine Möglichkeit besteht darin, ein Objekt zu implementieren, das [**IQueryInfo**](/windows/win32/api/shlobj_core/nn-shlobj_core-iqueryinfo) unterstützt, und dann das Objekt unter dem richtigen Unterschlüssel in der Registrierung zu registrieren (siehe unten). Alternativ können Sie entweder eine feste Zeichenfolge oder eine Liste bestimmter Dateieigenschaften angeben, die angezeigt werden sollen.

Um eine feste Zeichenfolge für eine Namespaceerweiterung anzuzeigen, erstellen Sie unter dem CLSID-Schlüssel Ihrer Namespaceerweiterung einen Unterschlüssel namens **InfoTip.** Legen Sie die Daten dieses Unterschlüssels auf die Zeichenfolge fest, die angezeigt werden soll.

```
HKEY_CLASSES_ROOT
   CLSID
      {CLSID}
         InfoTip = InfoTip string for your namespace extension
```

Um eine feste Zeichenfolge für einen Dateityp anzuzeigen, erstellen Sie unter dem **ProgID-Schlüssel** des Dateityps, für den Sie Infotips bereitstellen möchten, einen Unterschlüssel namens **InfoTip.** Legen Sie die Daten dieses Unterschlüssels auf die Zeichenfolge fest, die angezeigt werden soll.

```
HKEY_CLASSES_ROOT
   ProgID
      InfoTip = InfoTip string for all files of this type
```

Wenn die Shell bestimmte Dateieigenschaften in der Infotip für einen bestimmten Dateityp anzeigen soll, erstellen Sie unter dem **ProgID-Schlüssel** dieses Dateityps einen Unterschlüssel namens **InfoTip.** Legen Sie die Daten dieses Unterschlüssels als eine durch Semikolons getrennten Liste kanonischer Eigenschaftennamen oder {fmtid}, pid-Paare fest, wobei *propname* ein kanonischer Eigenschaftenname und *{fmtid},pid* ein [**FMTID/PID-Paar**](./objects.md)ist.

```
HKEY_CLASSES_ROOT
   ProgID
      InfoTip = propname;propname;{fmtid},pid;{fmtid},pid
```

Die folgenden Eigenschaftennamen können verwendet werden.



| Eigenschaftenname    | Beschreibung                   | Abgerufen von                                                                            |
|------------------|-------------------------------|-------------------------------------------------------------------------------------------|
| Autor           | Autor des Dokuments        | [**PIDSI \_ AUTHOR**](../stg/the-summary-information-property-set.md)                             |
| Titel            | Titel des Dokuments         | [**PIDSI \_ TITLE**](../stg/the-summary-information-property-set.md)                              |
| Gegenstand          | Betreffzusammenfassung               | [**PIDSI \_ SUBJECT**](../stg/the-summary-information-property-set.md)                            |
| Kommentar          | Dokumentkommentare             | [**PIDSI \_ COMMENT-**](../stg/the-summary-information-property-set.md) oder Ordner-/Laufwerkeigenschaften |
| PageCount        | Anzahl von Seiten               | [**PIDSI \_ PAGECOUNT**](../stg/the-summary-information-property-set.md)                          |
| Name             | Anzeigename                 | Standardordneransicht                                                                      |
| OriginalLocation | Speicherort der ursprünglichen Datei     | Ordner "Kleinbuchstaben" und Papierkorb Ordner                                                   |
| DateDeleted      | Datum, an dem die Datei gelöscht wurde         | Papierkorb Ordner                                                                        |
| Typ             | Dateityp                  | Standardansicht der Ordnerdetails                                                              |
| Size             | Größe der Datei                  | Standardansicht der Ordnerdetails                                                              |
| SyncCopyIn       | Identisch mit OriginalLocation      | Identisch mit OriginalLocation                                                                  |
| Geändert         | Datum der letzten Änderung            | Standardansicht der Ordnerdetails                                                              |
| Erstellt          | Erstellungsdatum                  | Standardansicht der Ordnerdetails                                                              |
| Zugegriffen         | Datum des letzten Zugriffes            | Standardansicht der Ordnerdetails                                                              |
| InFolder         | Verzeichnis, das die Datei enthält | Dokumentsuchergebnisse                                                                   |
| Rang             | Qualität der Such übereinstimmung       | Dokumentsuchergebnisse                                                                   |
| FreeSpace        | Verfügbarer Speicherplatz       | Laufwerke                                                                               |
| NumberOfVisits   | Anzahl von Aufrufen              | Ordner "Favoriten"                                                                          |
| Attribute       | Dateiattribute               | Standardansicht der Ordnerdetails                                                              |
| Company          | Unternehmensname                  | [**PIDDSI \_ COMPANY**](../stg/the-documentsummaryinformation-and-userdefined-property-sets.md)   |
| Category         | Dokumentkategorie             | [**PIDDSI \_ CATEGORY**](../stg/the-documentsummaryinformation-and-userdefined-property-sets.md)  |
| Copyright        | Medienrechte               | [**PIDMSI \_ COPYRIGHT**](../stg/the-documentsummaryinformation-and-userdefined-property-sets.md) |
| HTMLInfoTipFile  | HTML-InfoTip-Datei             | Desktop.ini-Datei für den Ordner                                                               |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Registrieren von Shellerweiterungshandlern](reg-shell-exts.md)
</dt> </dl>

 

 
