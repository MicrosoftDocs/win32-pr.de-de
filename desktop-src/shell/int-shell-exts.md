---
description: Ein Großteil der Implementierung eines Shellerweiterungs-Handlerobjekts wird durch seinen Typ vorgegeben. Es gibt jedoch einige allgemeine Elemente. In diesem Thema werden die Aspekte der Implementierung erläutert, die von allen Shellerweiterungs Handlern gemeinsam genutzt werden.
ms.assetid: ce21ca0f-157c-4f69-bcf9-dc259c3bac80
title: Initialisieren von Shellerweiterungs Handlern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6a27b6273c5e342dc4caf545fb3593cdad66261
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980777"
---
# <a name="initializing-shell-extension-handlers"></a>Initialisieren von Shellerweiterungs Handlern

Ein Großteil der Implementierung eines Shellerweiterungs-Handlerobjekts wird durch seinen Typ vorgegeben. Es gibt jedoch einige allgemeine Elemente. In diesem Thema werden die Aspekte der Implementierung erläutert, die von allen Shellerweiterungs Handlern gemeinsam genutzt werden.

Alle Shellerweiterungs Handler sind in-Process-Component Object Model (com)-Objekten. Sie müssen eine GUID zugewiesen und wie unter [Registrieren von Shellerweiterungs Handlern](handlers.md)beschrieben registriert sein. Sie werden als DLLs implementiert und müssen die folgenden Standardfunktionen exportieren:

-   [**DllMain**](../dlls/dllmain.md). Der Standard Einstiegspunkt für die dll.
-   [**DllGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-dllgetclassobject). Macht die Klassenfactory des Objekts verfügbar.
-   [**DllCanUnloadNow**](/windows/win32/api/combaseapi/nf-combaseapi-dllcanunloadnow). COM ruft diese Funktion auf, um zu bestimmen, ob das Objekt Clients bedient. Andernfalls kann das System die DLL entladen und den zugeordneten Speicher freigeben.

Wie alle COM-Objekte müssen Shellerweiterungs Handler eine [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle und eine [Klassenfactory](../com/implementing-iclassfactory.md)implementieren. In den meisten Fällen muss in Windows XP oder früher entweder eine [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) -oder [**ishellextinit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) -Schnittstelle implementiert werden. Diese wurden durch [**IInitializeWithStream**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithstream), [**IInitializeWithItem**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem) und [**IInitializeWithFile**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithfile) in Windows Vista ersetzt. Die Shell verwendet diese Schnittstellen, um den Handler zu initialisieren.

Die [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) -Schnittstelle muss folgendermaßen implementiert werden:

-   Symbol Handler
-   Daten Handler
-   Drop Handler

Die [**ishellextinit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) -Schnittstelle muss wie folgt implementiert werden:

-   Handler für Kontextmenü
-   Drag & Drop-Handler
-   Eigenschaften Blatt Handler

Im restlichen Teil dieses Themas werden die folgenden Themen behandelt:

-   [Implementieren von IPersistFile](#implementing-ipersistfile)
-   [Implementieren von ishellextinit](#implementing-ishellextinit)
-   [Infotip-Anpassung](#infotip-customization)
-   [Zugehörige Themen](#related-topics)

## <a name="implementing-ipersistfile"></a>Implementieren von IPersistFile

Die [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) -Schnittstelle ist so konzipiert, dass ein Objekt aus einer Datenträger Datei geladen oder in einer Datei gespeichert werden kann. Sie verfügt über sechs Methoden, zusätzlich zu [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), fünf ihrer eigenen und der [**GetClassID-**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid) Methode, die von [**ipersistent**](/windows/win32/api/objidl/nn-objidl-ipersist)erbt. Bei Shellerweiterungen wird **ipersistent** nur zum Initialisieren eines Shellerweiterungs-Handlerobjekts verwendet. Da in der Regel kein Lese-oder Schreibzugriff auf den Datenträger erforderlich ist, benötigen nur die Methoden **GetClassID** und [**Load**](/windows/win32/api/objidl/nf-objidl-ipersistfile-load) eine nicht Token-Implementierung.

Die Shell ruft zuerst [**GetClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid) auf, und die-Funktion gibt den Klassen Bezeichner (CLSID) des Erweiterungs Handler-Objekts zurück. Die Shell ruft dann [**Load**](/windows/win32/api/objidl/nf-objidl-ipersistfile-load) auf und übergibt zwei Werte. Der erste *pszFile-Datentyp* ist eine Unicode-Zeichenfolge mit dem Namen der Datei oder des Ordners, mit der die Shell arbeiten soll. Die zweite ist der *dwmode*, der den Datei Zugriffsmodus angibt. Da der Zugriff auf Dateien normalerweise nicht erforderlich ist, ist *dwmode* normalerweise 0 (null). Die-Methode speichert diese Werte nach Bedarf für den späteren Verweis.

Das folgende Code Fragment veranschaulicht, wie ein typischer shellerweiterungshandler die Methoden [**GetClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid) und [**Load**](/windows/win32/api/objidl/nf-objidl-ipersistfile-load) implementiert. Es ist für die Handhabung von ANSI oder Unicode konzipiert. CLSID \_ sampleexthandler ist die GUID des Erweiterungs Handler-Objekts, und csampleshellextension ist der Name der Klasse, die zum Implementieren der Schnittstelle verwendet wird. Die Variablen **m \_ szFilename** und **m \_ dwmode** sind private Variablen, die zum Speichern des Namens und der Zugriffsflags der Datei verwendet werden.


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



## <a name="implementing-ishellextinit"></a>Implementieren von ishellextinit

Die [**ishellextinit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) -Schnittstelle verfügt über nur eine Methode, [**ishellextinit:: Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize), zusätzlich zu [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown). Die-Methode verfügt über drei Parameter, die von der Shell verwendet werden können, um verschiedene Arten von Informationen zu übergeben. Welche Werte weitergegeben werden, hängt vom Typ des Handlers ab, und einige können auf **null** festgelegt werden.

-   *pidlfolder* enthält einen Ordner Zeiger auf eine Liste der Element Bezeichner (PIDL). Dabei handelt es sich um eine absolute PIDL. Bei Eigenschaften Blatt Erweiterungen ist dieser Wert **null**. Bei Kontextmenü Erweiterungen ist dies die PIDL des Ordners, der das Element enthält, dessen Kontextmenü angezeigt wird. Bei nicht standardmäßigen Drag & Drop-Handlern ist dies die PIDL des Ziel Ordners.
-   *pdataobject* enthält einen Zeiger auf die [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) -Schnittstelle eines Datenobjekts. Das Datenobjekt enthält einen oder mehrere Dateinamen im [CF- \_ HDROP](dragdrop.md) -Format.
-   *hregkey* enthält einen Registrierungsschlüssel für das Datei Objekt oder den Ordnertyp.

Die [**ishellextinit:: Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) -Methode speichert den Dateinamen, den [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) -Zeiger und den Registrierungsschlüssel nach Bedarf für die spätere Verwendung. Das folgende Code Fragment veranschaulicht die Implementierung von **ishellextinit:: Initialize**. Der Einfachheit halber wird in diesem Beispiel davon ausgegangen, dass das Datenobjekt nur eine einzelne Datei enthält. Im Allgemeinen enthält das Datenobjekt möglicherweise mehrere Dateien, die jeweils extrahiert werden müssen.


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



## <a name="infotip-customization"></a>Infotip-Anpassung

Es gibt zwei Möglichkeiten zum Anpassen von infotips. Eine Möglichkeit besteht darin, ein Objekt zu implementieren, das [**iqueryinfo**](/windows/win32/api/shlobj_core/nn-shlobj_core-iqueryinfo) unterstützt, und das Objekt dann unter dem richtigen Unterschlüssel in der Registrierung zu registrieren (siehe unten). Alternativ können Sie entweder eine festgelegte Zeichenfolge oder eine Liste bestimmter Dateieigenschaften angeben, die angezeigt werden sollen.

Um eine Zeichenfolge fester Zeichenfolge für eine Namespace Erweiterung anzuzeigen, erstellen Sie unter dem CLSID-Schlüssel der Namespace Erweiterung einen Unterschlüssel namens **infotip** . Legen Sie die Daten des unter Schlüssels auf die Zeichenfolge fest, die Sie anzeigen möchten.

```
HKEY_CLASSES_ROOT
   CLSID
      {CLSID}
         InfoTip = InfoTip string for your namespace extension
```

Um eine festgelegte Zeichenfolge für einen Dateityp anzuzeigen, erstellen Sie unter dem **ProgID** -Schlüssel des Dateityps, für den Sie Infotipps bereitstellen möchten, einen Unterschlüssel namens **infotip** . Legen Sie die Daten des unter Schlüssels auf die Zeichenfolge fest, die Sie anzeigen möchten.

```
HKEY_CLASSES_ROOT
   ProgID
      InfoTip = InfoTip string for all files of this type
```

Wenn Sie möchten, dass die Shell bestimmte Dateieigenschaften im Infotipp für einen bestimmten Dateityp anzeigt, erstellen Sie unter dem **ProgID** -Schlüssel dieses Dateityps einen Unterschlüssel namens **Infotipp** . Legen Sie für die Daten dieses unter Schlüssels eine durch Semikolons getrennte Liste von kanonischen Eigenschaftsnamen oder {fmtid}, PID-Paare, bei denen *propName* ein kanonischer Eigenschaftsname ist *, und {fmtid}, PID* ein [**fmtid/PID-paar**](./objects.md).

```
HKEY_CLASSES_ROOT
   ProgID
      InfoTip = propname;propname;{fmtid},pid;{fmtid},pid
```

Die folgenden Eigenschaftsnamen können verwendet werden.



| Eigenschaftenname    | BESCHREIBUNG                   | Abgerufen von                                                                            |
|------------------|-------------------------------|-------------------------------------------------------------------------------------------|
| Autor           | Autor des Dokuments        | [**pidsi- \_ Autor**](../stg/the-summary-information-property-set.md)                             |
| Titel            | Titel des Dokuments         | [**pidsi- \_ Titel**](../stg/the-summary-information-property-set.md)                              |
| Subject          | Themen Zusammenfassung               | [**pidsi- \_ Betreff**](../stg/the-summary-information-property-set.md)                            |
| Comment          | Dokument Kommentare             | [**Pidsi \_ Kommentar**](../stg/the-summary-information-property-set.md) -oder Ordner-/Laufwerkeigenschaften |
| PageCount        | Anzahl von Seiten               | [**pidsi \_ Page count**](../stg/the-summary-information-property-set.md)                          |
| Name             | Anzeigename                 | Standard Ordneransicht                                                                      |
| Ursprungs Zuordnung | Speicherort der ursprünglichen Datei     | Ordner "Briefkasten" und "Papierkorb"                                                   |
| Datedeleted      | Die Datums Datei wurde gelöscht.         | Papierkorb Ordner                                                                        |
| type             | Dateityp                  | Ansicht "Standard Ordner Details"                                                              |
| Size             | Größe der Datei                  | Ansicht "Standard Ordner Details"                                                              |
| Synccopyin       | Identisch mit "Ursprungs Zuordnung"      | Identisch mit "Ursprungs Zuordnung"                                                                  |
| Geändert         | Datum der letzten Änderung            | Ansicht "Standard Ordner Details"                                                              |
| Erstellt          | Erstellungsdatum                  | Ansicht "Standard Ordner Details"                                                              |
| Auf         | Datum des letzten Zugriffs            | Ansicht "Standard Ordner Details"                                                              |
| InFolder         | Verzeichnis, das die Datei enthält | Dokument Suchergebnisse                                                                   |
| Rang             | Qualität der Such Übereinstimmung       | Dokument Suchergebnisse                                                                   |
| FreeSpace        | Verfügbarer Speicherplatz       | Laufwerke                                                                               |
| Anzahl von besuchen   | Anzahl von Aufrufen              | Ordner "Favoriten"                                                                          |
| Attributes       | Dateiattribute               | Ansicht "Standard Ordner Details"                                                              |
| Company          | Unternehmensname                  | [**piddsi- \_ Unternehmen**](../stg/the-documentsummaryinformation-and-userdefined-property-sets.md)   |
| Kategorie         | Dokument Kategorie             | [**piddsi- \_ Kategorie**](../stg/the-documentsummaryinformation-and-userdefined-property-sets.md)  |
| Copyright        | Medien Copyright               | [**pidmsi \_ Copyright**](../stg/the-documentsummaryinformation-and-userdefined-property-sets.md) |
| Htmlinfotipfile  | HTML-infotip-Datei             | Datei für Ordner Desktop.ini                                                               |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Registrieren von Shellerweiterungs Handlern](reg-shell-exts.md)
</dt> </dl>

 

 
