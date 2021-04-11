---
description: In diesem Thema wird erläutert, wie Sie Eigenschafts Handler erstellen und registrieren, um mit dem Windows-Eigenschaften System zu arbeiten.
ms.assetid: 3b54dd65-b7db-4e6a-bc3d-1008fdabcfa9
title: Initialisieren von Eigenschaften Handlern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f8eb11bc44217e508313bfb477c65925b44216e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216260"
---
# <a name="initializing-property-handlers"></a>Initialisieren von Eigenschaften Handlern

In diesem Thema wird erläutert, wie Sie Eigenschafts Handler erstellen und registrieren, um mit dem Windows-Eigenschaften System zu arbeiten.

Dieses Thema ist wie folgt organisiert:

-   [Eigenschaften Handler](#property-handlers)
-   [Vorbereitungen](#before-you-begin)
-   [Initialisieren von Eigenschaften Handlern](#initializing-property-handlers)
-   [In-Memory-Eigenschaften Speicher](#in-memory-property-store)
-   [Umgang mit PROPVARIANT-Based Werten](#dealing-with-propvariant-based-values)
-   [Unterstützen offener Metadaten](#supporting-open-metadata)
-   [Voll Text Inhalte](#full-text-contents)
-   [Angeben von Werten für Eigenschaften](#providing-values-for-properties)
-   [Zurückschreiben von Werten](#writing-back-values)
-   [Implementieren von ipropertystorecapabilitäten](#implementing-ipropertystorecapabilities)
-   [Registrieren und Verteilen von Eigenschaften Handlern](#registering-and-distributing-property-handlers)
-   [Zugehörige Themen](#related-topics)

## <a name="property-handlers"></a>Eigenschaften Handler

Eigenschaften Handler sind ein wesentlicher Bestandteil des Eigenschaften Systems. Sie werden vom Indexer Prozess Weise aufgerufen, um Eigenschaftswerte zu lesen und zu indizieren. Außerdem werden Sie von Windows-Explorer in-Process aufgerufen, um Eigenschaftswerte direkt in den Dateien zu lesen und zu schreiben. Diese Handler müssen sorgfältig geschrieben und getestet werden, um eine Beeinträchtigung der Leistung oder des Verlusts von Daten in den betroffenen Dateien zu verhindern. Weitere Informationen zu indexerspezifischen Überlegungen, die sich auf die Implementierung von Eigenschaften Handlern auswirken, finden Sie unter [entwickeln von Eigenschaften Handlern für Windows Search](../search/-search-3x-wds-extidx-propertyhandlers.md).

In diesem Thema wird ein Beispiel für ein XML-basiertes Dateiformat erläutert, das eine Anleitung mit der Dateinamenerweiterung ". Rezept" beschreibt. Die Dateinamenerweiterung ". Rezept" ist als eigenes, eindeutiges Dateiformat registriert, anstatt sich auf das allgemeinere XML-Dateiformat zu verlassen, dessen Handler einen sekundären Stream zum Speichern von Eigenschaften verwendet. Es wird empfohlen, dass Sie eindeutige Dateinamen Erweiterungen für die Dateitypen registrieren.

## <a name="before-you-begin"></a>Vorbereitungen

Eigenschaften Handler sind COM-Objekte, die die [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) -Abstraktion für ein bestimmtes Dateiformat erstellen. Sie lesen (analysieren) und Schreiben dieses Dateiformat auf eine Weise, die der Spezifikation entspricht. Einige Eigenschaften Handler arbeiten auf der Grundlage von APIs, die den Zugriff auf ein bestimmtes Dateiformat abstrahieren. Bevor Sie einen Eigenschaften Handler für das Dateiformat entwickeln, müssen Sie verstehen, wie das Dateiformat Eigenschaften speichert, und wie diese Eigenschaften (Namen und Werte) der Eigenschafts Speicher Abstraktion zugeordnet werden.

Beachten Sie beim Planen der Implementierung, dass es sich bei den Eigenschaften Handlern um Komponenten auf niedriger Ebene handelt, die im Kontext von Prozessen wie Windows-Explorer, dem Windows Search-Indexer und Anwendungen von Drittanbietern geladen werden, die das shellelement-Programmiermodell verwenden. Folglich können Eigenschafts Handler nicht in verwaltetem Code implementiert werden und sollten in C++ implementiert werden. Wenn Ihr Handler für seine Arbeit APIs oder Dienste verwendet, müssen Sie sicherstellen, dass diese Dienste ordnungsgemäß in den Umgebungen funktionieren, in denen der Eigenschafts Handler geladen wird.

> [!Note]  
> Eigenschaften Handler sind immer bestimmten Dateitypen zugeordnet. Wenn das Dateiformat Eigenschaften enthält, die einen benutzerdefinierten Eigenschaften Handler erfordern, sollten Sie daher immer eine eindeutige Dateinamenerweiterung für jedes Dateiformat registrieren.

 

## <a name="initializing-property-handlers"></a>Initialisieren von Eigenschaften Handlern

Bevor eine Eigenschaft vom System verwendet wird, wird Sie initialisiert, indem eine Implementierung von [**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream)aufgerufen wird. Der Eigenschafts Handler sollte initialisiert werden, indem das System ihm einen Stream zuweist, anstatt diese Zuweisung der Handlerimplementierung zu überlassen. Diese Methode der Initialisierung stellt Folgendes sicher:

-   Der Eigenschaften Handler kann in einem eingeschränkten Prozess (einem wichtigen Sicherheits Feature) ausgeführt werden, ohne dass er über Zugriffsrechte verfügt, um Dateien direkt zu lesen oder zu schreiben, anstatt auf seinen Inhalt über den Stream zuzugreifen.
-   Das System kann als vertrauenswürdig eingestuft werden, um die Datei-oplocks ordnungsgemäß zu verarbeiten, was ein wichtiges Maß an Zuverlässigkeit ist.
-   Das-Eigenschaften System stellt einen automatisch sicheren speicheringdienst bereit, ohne dass zusätzliche Funktionen von der Implementierung des Eigenschaften Handlers benötigt werden. Weitere Informationen zu Streams finden Sie im Abschnitt [Zurückschreiben von Werten](#writing-back-values) .
-   Durch die Verwendung von [**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream) wird die Implementierung aus den Dateisystem Details abstrahiert. Dies ermöglicht es dem Handler, die Initialisierung durch alternative Speicher, z. b. einen File Transfer Protocol (FTP)-Ordner oder eine komprimierte Datei mit der Dateinamenerweiterung ". zip", zu unterstützen.

Es gibt Fälle, in denen die Initialisierung mit Streams nicht möglich ist. In diesen Fällen gibt es zwei weitere Schnittstellen, die von Eigenschaften Handlern implementiert werden können: [**IInitializeWithFile**](/windows/win32/api/propsys/nn-propsys-iinitializewithfile) und [**IInitializeWithItem**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem). Wenn ein Eigenschaften Handler den [**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream)nicht implementiert, muss er die Ausführung im isolierten Prozess ablehnen, in den der systemindexer ihn standardmäßig platzieren würde, wenn es eine Änderung am Stream gäbe. Wenn Sie dieses Feature ablehnen möchten, legen Sie den folgenden Registrierungs Wert fest.

```
HKEY_CLASSES_ROOT
   CLSID
      {66742402-F9B9-11D1-A202-0000F81FEDEE}
         DisableProcessIsolation = 1
```

Es ist jedoch weitaus besser, [**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream) zu implementieren und eine streambasierte Initialisierung durchzuführen. Der Eigenschafts Handler ist als Ergebnis sicherer und zuverlässiger. Die Deaktivierung der Prozess Isolation ist in der Regel nur für Legacy-Eigenschaften Handler vorgesehen und sollte durch neuen Code energisch vermieden werden.

Wenn Sie die Implementierung eines Eigenschaften Handlers detailliert untersuchen möchten, betrachten Sie das folgende Codebeispiel, das eine Implementierung von [**IInitializeWithStream:: Initialize**](/windows/win32/api/propsys/nf-propsys-iinitializewithstream-initialize)ist. Der-Handler wird initialisiert, indem ein XML-basiertes Rezept Dokument über einen Zeiger auf die zugeordnete [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) -Instanz dieses Dokuments geladen wird. Die **\_ spdocele** -Variable, die in der Nähe des Endes des Code Beispiels verwendet wird, wird weiter oben im Beispiel als msxml2:: ixmldomelementptr definiert.

> [!Note]  
> Die folgenden und alle nachfolgenden Codebeispiele stammen aus dem Rezept Handler-Beispiel, das im Windows Software Development Kit (SDK) enthalten ist. .

 


```
HRESULT CRecipePropertyStore::Initialize(IStream *pStream, DWORD grfMode)
{
    HRESULT hr = E_FAIL;
    
    try
    {
        if (!_spStream)
        {
            hr = _spDomDoc.CreateInstance(__uuidof(MSXML2::DOMDocument60));
            
            if (SUCCEEDED(hr))
            {
                if (VARIANT_TRUE == _spDomDoc->load(static_cast<IUnknown *>(pStream)))
                {
                    _spDocEle = _spDomDoc->documentElement;
                }
```



Â 

Nachdem das Dokument selbst geladen wurde, werden die Eigenschaften, die im Windows-Explorer angezeigt werden sollen, durch Aufrufen der geschützten **\_ LoadProperties** -Methode geladen, wie im folgenden Codebeispiel veranschaulicht. Dieser Prozess wird im nächsten Abschnitt ausführlich untersucht.


```
                if (_spDocEle)
                {
                    hr = _LoadProperties();
    
                    if (SUCCEEDED(hr))
                    {
                        _spStream = pStream;
                    }
                }
                else
                {
                    hr = E_FAIL;  // parse error
                }
            }
        }
        else
        {
            hr = E_UNEXPECTED;
        }
    }
    
    catch (_com_error &e)
    {
        hr = e.Error();
    }
    
    return hr;
}
```



Wenn der Stream schreibgeschützt ist, aber der *grfMode* -Parameter das STGM-Flag zum Lesen von Lese Voreinstellungen enthält \_ , sollte die Initialisierung fehlschlagen und STG \_ E \_ AccessDenied zurückgeben. Ohne diese Überprüfung zeigt Windows Explorer die Eigenschaftswerte als beschreibbar an, auch wenn dies nicht der Fall ist, was zu einem verwirrenden Endbenutzer Prozess führt.

Der Eigenschafts Handler wird in seiner Lebensdauer nur einmal initialisiert. Wenn eine zweite Initialisierung angefordert wird, sollte der Handler zurückgeben `HRESULT_FROM_WIN32(ERROR_ALREADY_INITIALIZED)` .

## <a name="in-memory-property-store"></a>Eigenschaften Speicher In-Memory

Bevor Sie sich mit der Implementierung von **\_ LoadProperties** befassen, sollten Sie das **PropertyMap** -Array verstehen, das im Beispiel verwendet wird, um Eigenschaften im XML-Dokument vorhandenen Eigenschaften im Eigenschaften System über Ihre pkey-Werte zuzuordnen.

Sie sollten nicht jedes Element und Attribut in der XML-Datei als Eigenschaft verfügbar machen. Wählen Sie stattdessen nur diejenigen aus, die für Endbenutzer in der Organisation Ihrer Dokumente (in diesem Fall Rezepte) nützlich sein werden. Dies ist ein wichtiges Konzept, das bei der Entwicklung von Eigenschaften Handlern beachtet werden muss: der Unterschied zwischen Informationen, die für Organisations Szenarios wirklich nützlich sind, und Informationen, die zu den Details Ihrer Datei gehören und durch das Öffnen der Datei selbst angezeigt werden können. Eigenschaften sind nicht als vollständige Duplizierung einer XML-Datei vorgesehen.


```
PropertyMap c_rgPropertyMap[] =
{
{ L"Recipe/Title", PKEY_Title, 
                   VT_LPWSTR, 
                   NULL, 
                   PKEY_Null },
{ L"Recipe/Comments", PKEY_Comment, 
                      VT_LPWSTR, 
                      NULL, 
                      PKEY_Null },
{ L"Recipe/Background", PKEY_Author, 
                        VT_VECTOR | VT_LPWSTR, 
                        L"Author", 
                        PKEY_Null },
{ L"Recipe/RecipeKeywords", PKEY_Keywords, 
                            VT_VECTOR | VT_LPWSTR, 
                            L"Keyword", 
                            PKEY_KeywordCount },
};
```



Hier ist die vollständige Implementierung der **\_ LoadProperties** -Methode, die von [**IInitializeWithStream:: Initialize**](/windows/win32/api/propsys/nf-propsys-iinitializewithstream-initialize)aufgerufen wird.


```
HRESULT CRecipePropertyStore::_LoadProperties()
{
    HRESULT hr = E_FAIL;    
    
    if (_spCache)
    {
        hr = <mark type="const">S_OK</mark>;
    }
    else
    {
        // Create the in-memory property store.
        hr = PSCreateMemoryPropertyStore(IID_PPV_ARGS(&_spCache));
    
        if (SUCCEEDED(hr))
        {
            // Cycle through each mapped property.
            for (UINT i = 0; i < ARRAYSIZE(c_rgPropertyMap); ++i)
            {
                _LoadProperty(c_rgPropertyMap[i]);
            }
    
            _LoadExtendedProperties();
            _LoadSearchContent();
        }
    }
    return hr;
}
```



Die **\_ LoadProperties** -Methode ruft die shellhilfsfunktion " [**pscreatememorypropertystore**](/windows/win32/api/propsys/nf-propsys-pscreatememorypropertystore) " auf, um einen Speicher internen Eigenschafts Speicher (Cache) für die behandelten Eigenschaften zu erstellen. Wenn Sie einen Cache verwenden, werden die Änderungen für Sie nachverfolgt. Dadurch können Sie nachverfolgen, ob ein Eigenschafts Wert im Cache geändert, aber noch nicht im persistenten Speicher gespeichert wurde. Außerdem werden Sie von unnötigerweise Beibehaltung von Eigenschafts Werten freigegeben, die sich nicht geändert haben.

Die **\_ LoadProperties** -Methode ruft auch **\_ LoadProperty** auf, deren Implementierung im folgenden Code dargestellt wird, und zwar einmal für jede zugeordnete Eigenschaft. **\_ LoadProperty** Ruft den Wert der Eigenschaft ab, wie im **PropertyMap** -Element im XML-Stream angegeben, und weist ihn mithilfe eines [**Ansichts namens ipropertystorecache:: setvalueandstate**](/windows/win32/api/propsys/nf-propsys-ipropertystorecache-setvalueandstate)dem in-Memory-Cache zu. Das normale PSC- \_ Flag im Aufruf von **ipropertystorecache:: setvalueandstate** gibt an, dass der Eigenschafts Wert seit dem Zeitpunkt, zu dem er in den Cache eingetreten ist, nicht geändert wurde.


```
HRESULT CRecipePropertyStore::_LoadProperty(PropertyMap &map)
{
    HRESULT hr = S_FALSE;
    
    MSXML2::IXMLDOMNodePtr spXmlNode(_spDomDoc->selectSingleNode(map.pszXPath));
    if (spXmlNode)
    {
        PROPVARIANT propvar = { 0 };
        propvar.vt = map.vt;
        
        if (map.vt == (VT_VECTOR | VT_LPWSTR))
        {
            hr = _LoadVectorProperty(spXmlNode, &propvar, map);
        }
        else
        {
            // If there is no value, set to VT_EMPTY to indicate
            // that it is not there. Do not return failure.
            if (spXmlNode->text.length() == 0)
            {
                propvar.vt = VT_EMPTY;
                hr = <mark type="const">S_OK</mark>;
            }
            else
            {
                // SimplePropVariantFromString is a helper function.
                // particular to the sample. It is found in Util.cpp.
                hr = SimplePropVariantFromString(spXmlNode->text, &propvar);
            }
        }
    
        if (S_OK == hr)
        {
            hr = _spCache->SetValueAndState(map.key, &propvar, PSC_NORMAL);
            PropVariantClear(&propvar);
        }
    }
    return hr;
}
```



## <a name="dealing-with-propvariant-based-values"></a>Umgang mit PROPVARIANT-Based Werten

In der Implementierung von **\_ LoadProperty** wird ein Eigenschafts Wert in Form einer [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)bereitgestellt. Ein Satz von APIs im Software Development Kit (SDK) wird bereitgestellt, um von primitiven Typen wie **pwstr** oder **int** in oder aus **PROPVARIANT** -Typen zu konvertieren. Diese APIs finden Sie in "propvarutil. h".

Wenn Sie z. b. eine [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) in eine Zeichenfolge konvertieren möchten, können Sie " [**propvariantto String**](/windows/win32/api/propvarutil/nf-propvarutil-propvarianttostring) " verwenden, wie hier dargestellt.


```
PropVariantToString(REFPROPVARIANT propvar, PWSTR psz, UINT cch);
```



Um eine PROPVARIANT aus einer Zeichenfolge zu initialisieren, können Sie [**initpropvariantfromstring**](/windows/win32/api/propvarutil/nf-propvarutil-initpropvariantfromstring)verwenden.


```
InitPropVariantFromString(PCWSTR psz, PROPVARIANT *ppropvar);
```



Wie Sie in jeder der im Beispiel enthaltenen Rezept Dateien sehen können, können in jeder Datei mehr als ein Schlüsselwort vorhanden sein. Um dies zu berücksichtigen, unterstützt das Eigenschaften System mehrwertige Zeichen folgen, die als Zeichen folgen Vektor dargestellt werden (z \_ . a. "VT Vector \| VT \_ LPWSTR"). Die **\_ loadvectorproperty** -Methode im Beispiel verwendet vektorbasierte Werte.


```
HRESULT CRecipePropertyStore::_LoadVectorProperty
                                (MSXML2::IXMLDOMNode *pNodeParent,
                                 PROPVARIANT *ppropvar,
                                 struct PropertyMap &map)
{
    HRESULT hr = S_FALSE;
    MSXML2::IXMLDOMNodeListPtr spList = pNodeParent->selectNodes(map.pszSubNodeName);
    
    if (spList)
    {
        UINT cElems = spList->length;
        ppropvar->calpwstr.cElems = cElems;
        ppropvar->calpwstr.pElems = (PWSTR*)CoTaskMemAlloc(sizeof(PWSTR)*cElems);
    
        if (ppropvar->calpwstr.pElems)
        {
            for (UINT i = 0; (SUCCEEDED(hr) && i < cElems); ++i)
            {
                hr = SHStrDup(spList->item[i]->text, 
                              &(ppropvar->calpwstr.pElems[i]));
            }
    
            if (SUCCEEDED(hr))
            {
                if (!IsEqualPropertyKey(map.keyCount, PKEY_Null))
                {
                    PROPVARIANT propvarCount = { VT_UI4 };
                    propvarCount.uintVal = cElems;
                    
                    _spCache->SetValueAndState(map.keyCount,
                                               &propvarCount, 
                                               PSC_NORMAL);
                }
            }
            else
            {
                PropVariantClear(ppropvar);
            }
        }
        else
        {
            hr = E_OUTOFMEMORY;
        }
    }
    
    return hr;
}
```



Wenn ein Wert in der Datei nicht vorhanden ist, wird kein Fehler zurückgegeben. Legen Sie den Wert stattdessen auf VT \_ Empty fest, und geben Sie **S \_ OK** zurück. "VT Empty" gibt an \_ , dass der Eigenschafts Wert nicht vorhanden ist.

## <a name="supporting-open-metadata"></a>Unterstützen offener Metadaten

In diesem Beispiel wird ein XML-basiertes Dateiformat verwendet. Das Schema kann erweitert werden, um Eigenschaften zu unterstützen, die während der Entwicklung nicht berücksichtigt wurden, z. b.. Dieses System wird als Open Metadata bezeichnet. In diesem Beispiel wird das Eigenschaften System erweitert, indem unter dem **Rezept** Element **ExtendedProperties** ein Knoten erstellt wird, wie im folgenden Codebeispiel veranschaulicht.


```
<ExtendedProperties>
    <Property 
        Name="{65A98875-3C80-40AB-ABBC-EFDAF77DBEE2}, 100"
        EncodedValue="HJKHJDHKJHK"/>
</ExtendedProperties>
```



Wenn Sie persistente erweiterte Eigenschaften während der Initialisierung laden möchten, implementieren Sie die **\_ loadextendedproperties** -Methode, wie im folgenden Codebeispiel veranschaulicht.


```
HRESULT CRecipePropertyStore::_LoadExtendedProperties()
{
    HRESULT hr = S_FALSE;
    MSXML2::IXMLDOMNodeListPtr spList = 
                  _spDomDoc->selectNodes(L"Recipe/ExtendedProperties/Property");
    
    if (spList)
    {
        UINT cElems = spList->length;
        
        for (UINT i = 0; i < cElems; ++i)
        {
            MSXML2::IXMLDOMElementPtr spElement;
            
            if (SUCCEEDED(spList->item[i]->QueryInterface(IID_PPV_ARGS(&spElement))))
            {
                PROPERTYKEY key;
                _bstr_t bstrPropName = spElement->getAttribute(L"Name").bstrVal;
    
                if (!!bstrPropName &&
                    (SUCCEEDED(PropertyKeyFromString(bstrPropName, &key))))
                {
                    PROPVARIANT propvar = { 0 };
                    _bstr_t bstrEncodedValue = 
                               spElement->getAttribute(L"EncodedValue").bstrVal;
                   
                    if (!!bstrEncodedValue)
                    {
                        // DeserializePropVariantFromString is a helper function
                        // particular to the sample. It is found in Util.cpp.
                        hr = DeserializePropVariantFromString(bstrEncodedValue, 
                                                              &propvar);
                    }
```



Die in "propsys. h" deklarierten Serialisierungs-APIs werden zum Serialisieren und Deserialisieren von [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) -Typen in blobdaten verwendet, und anschließend wird die Base64-Codierung zum Serialisieren dieser blobzeichen in Zeichen folgen verwendet, die in der XML-Datei gespeichert werden können. Diese Zeichen folgen werden im **encodedValue** -Attribut des **ExtendedProperties** -Elements gespeichert. Die folgende Hilfsmethode, die in der Datei "util. cpp" des Beispiels implementiert ist, führt die Serialisierung aus. Er beginnt mit einem Aufrufen der [**stgserializepropvariant**](/windows/win32/api/propvarutil/nf-propvarutil-stgserializepropvariant) -Funktion, um die binäre Serialisierung auszuführen, wie im folgenden Codebeispiel veranschaulicht.


```
HRESULT SerializePropVariantAsString(const PROPVARIANT *ppropvar, PWSTR *pszOut)
{
    SERIALIZEDPROPERTYVALUE *pBlob;
    ULONG cbBlob;
    HRESULT hr = StgSerializePropVariant(ppropvar, &pBlob, &cbBlob);
```



Anschließend führt die Funktion " [**cryptbinarydestring**](/windows/win32/api/wincrypt/nf-wincrypt-cryptbinarytostringa)", die in Wincrypt. h deklariert ist, die Base64-Konvertierung aus.


```
    if (SUCCEEDED(hr))
    {
        hr = E_FAIL;
        DWORD cchString;
        
        if (CryptBinaryToString((BYTE *)pBlob, 
                                cbBlob,
                                CRYPT_STRING_BASE64, 
                                NULL, 
                                &cchString))
        {
            *pszOut = (PWSTR)CoTaskMemAlloc(sizeof(WCHAR) *cchString);
    
            if (*pszOut)
            {
                if (CryptBinaryToString((BYTE *)pBlob, 
                                         cbBlob,
                                         CRYPT_STRING_BASE64,
                                         *pszOut, 
                                         &cchString))
                {
                    hr = <mark type="const">S_OK</mark>;
                }
                else
                {
                    CoTaskMemFree(*pszOut);
                }
            }
            else
            {
                hr = E_OUTOFMEMORY;
            }
        }
    }
    
    return <mark type="const">S_OK</mark>;}
```



Die **deserializepropvariantfromstring** -Funktion, die auch in util. cpp enthalten ist, kehrt den Vorgang um und deserialisiert Werte aus der XML-Datei.

Weitere Informationen zur Unterstützung offener Metadaten finden Sie unter "Dateitypen, die offene Metadaten unterstützen" in [Dateitypen](../shell/fa-file-types.md).

## <a name="full-text-contents"></a>Inhalt Full-Text

Eigenschaften Handler können auch eine Volltextsuche der Dateiinhalte vereinfachen, und Sie sind eine einfache Möglichkeit, diese Funktionalität bereitzustellen, wenn das Dateiformat nicht übermäßig kompliziert ist. Es gibt eine Alternative, leistungsfähigere Möglichkeit, den vollständigen Text der Datei über die Implementierung der [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) -Schnittstelle bereitzustellen.

In der folgenden Tabelle werden die Vorteile der einzelnen Ansätze mithilfe von [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) oder [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)zusammengefasst.



| Funktion                                   | IFilter                      | IPropertyStore |
|----------------------------------------------|------------------------------|----------------|
| Ermöglicht das Zurückschreiben in Dateien?                  | Nein                           | Ja            |
| Bietet eine Mischung aus Inhalt und Eigenschaften?      | Ja                          | Ja            |
| Mehrsprachige?                                | Ja                          | Nein             |
| MIME/Embedded?                               | Ja                          | Nein             |
| Text Begrenzungen?                             | Satz, Absatz, Kapitel | Keine           |
| Implementierung wird für SPS/SQL Server unterstützt? | Ja                          | Nein             |
| Implementierung                               | Komplex                      | Einfach         |



 

Im Rezept handlerbeispiel hat das Rezeptdatei Format keine komplexen Anforderungen, sodass nur [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) für die voll Textunterstützung implementiert wurde. Die Volltextsuche wird für die XML-Knoten implementiert, die im folgenden Array benannt werden.


```
const PWSTR c_rgszContentXPath[] = {
    L"Recipe/Ingredients/Item",
    L"Recipe/Directions/Step",
    L"Recipe/RecipeInfo/Yield",
    L"Recipe/RecipeKeywords/Keyword",
};
```



Das-Eigenschaften System enthält die `System.Search.Contents` Eigenschaft (pkey \_ Search \_ Content), die zum Bereitstellen von voll Text Inhalt für den Indexer erstellt wurde. Der Wert dieser Eigenschaft wird nie direkt in der Benutzeroberfläche angezeigt. der Text von allen XML-Knoten, die im obigen Array benannt werden, wird zu einer einzelnen Zeichenfolge verkettet. Diese Zeichenfolge wird dann dem Indexer als voll Text Inhalt der Rezeptdatei über einen Aufruf von [**ipropertystorecache:: setvalueandstate**](/windows/win32/api/propsys/nf-propsys-ipropertystorecache-setvalueandstate) bereitgestellt, wie im folgenden Codebeispiel veranschaulicht.


```
HRESULT CRecipePropertyStore::_LoadSearchContent()
{
    HRESULT hr = S_FALSE;
    _bstr_t bstrContent;
    
    for (UINT i = 0; i < ARRAYSIZE(c_rgszContentXPath); ++i)
    {
        MSXML2::IXMLDOMNodeListPtr spList = 
                                  _spDomDoc->selectNodes(c_rgszContentXPath[i]);
    
        if (spList)
        {
            UINT cElems = spList->length;
            
            for (UINT elt = 0; elt < cElems; ++elt)
            {
                bstrContent += L" ";
                bstrContent += spList->item[elt]->text;
            }
        }
    }
    
    if (bstrContent.length() > 0)
    {
        PROPVARIANT propvar = { VT_LPWSTR };
        hr = SHStrDup(bstrContent, &(propvar.pwszVal));
    
        if (SUCCEEDED(hr))
        {
            hr = _spCache->SetValueAndState(PKEY_Search_Contents, 
                                            &propvar, 
                                            PSC_NORMAL);
            PropVariantClear(&propvar);
        }
    }
    
    return hr;}
```



## <a name="providing-values-for-properties"></a>Angeben von Werten für Eigenschaften

Wenn Sie zum Lesen von Werten verwendet werden, werden Eigenschaften Handler in der Regel aus einem der folgenden Gründe aufgerufen:

-   , Um alle Eigenschaftswerte aufzuzählen.
-   , Um den Wert einer bestimmten Eigenschaft zu erhalten.

Bei der Enumeration wird ein Eigenschaften Handler aufgefordert, seine Eigenschaften entweder während der Indizierung aufzulisten, oder wenn im Dialogfeld Eigenschaften nach Eigenschaften zur Anzeige in der **anderen** Gruppe gefragt werden. Die Indizierung erfolgt ständig als Hintergrund Vorgang. Wenn sich eine Datei ändert, wird der Indexer benachrichtigt, und die Datei wird neu indiziert, indem der Eigenschaften Handler aufgefordert wird, seine Eigenschaften aufzuzählen. Daher ist es wichtig, dass Eigenschaften Handler effizient implementiert werden und Eigenschaftswerte so schnell wie möglich zurückgeben. Zählen Sie alle Eigenschaften, für die Sie Werte haben, genauso wie für jede beliebige Sammlung, aber keine Eigenschaften, die speicherintensive Berechnungen oder Netzwerk Anforderungen umfassen, die Sie langsam abrufen können.

Beim Schreiben eines Eigenschaften Handlers müssen Sie in der Regel die folgenden beiden Sätze von Eigenschaften in Erwägung gezogen werden.

-   Primäre Eigenschaften: Eigenschaften, die der Dateityp nativ unterstützt. Beispielsweise unterstützt ein Foto-Eigenschaften Handler für die Metadaten für die austauschbare Bilddatei (EXIF) nativ `System.Photo.FNumber` .
-   Erweiterte Eigenschaften: Eigenschaften, die vom Dateityp als Teil der geöffneten Metadaten unterstützt werden.

Da im Beispiel der in-Memory-Cache verwendet wird, ist die Implementierung von [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) -Methoden lediglich eine Frage der Delegierung an diesen Cache, wie im folgenden Codebeispiel veranschaulicht.


```
IFACEMETHODIMP GetCount(__out DWORD *pcProps)
{ return _spCache->GetCount(pcProps); }

IFACEMETHODIMP GetAt(DWORD iProp, __out PROPERTYKEY *pkey)
{ return _spCache->GetAt(iProp, pkey); }

IFACEMETHODIMP GetValue(REFPROPERTYKEY key, __out PROPVARIANT *pPropVar)
{ return _spCache->GetValue(key, pPropVar); }
```



Wenn Sie sich entscheiden, nicht an den in-Memory-Cache zu delegieren, müssen Sie die-Methoden implementieren, um> das folgende erwartete Verhalten bereitzustellen:

-   [**IPropertyStore:: GetCount**](/previous-versions/windows/desktop/legacy/bb761472(v=vs.85)): Wenn keine Eigenschaften vorhanden sind, gibt diese Methode " **S \_ OK**" zurück.
-   [**IPropertyStore:: GetAt**](/previous-versions/windows/desktop/legacy/bb761471(v=vs.85)): Wenn *iprop* größer oder gleich *cproperist*, gibt diese Methode E \_ invalidArg zurück, und die Struktur, auf die durch den *pkey* -Parameter verwiesen wird, wird mit Nullen gefüllt.
-   [**IPropertyStore:: GetCount**](/previous-versions/windows/desktop/legacy/bb761472(v=vs.85)) und [**IPropertyStore:: GetAt**](/previous-versions/windows/desktop/legacy/bb761471(v=vs.85)) spiegeln den aktuellen Zustand des Eigenschaften Handlers wider. Wenn ein [**PropertyKey**](/windows/win32/api/wtypes/ns-wtypes-propertykey) durch [**IPropertyStore:: SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85))der Datei hinzugefügt oder daraus entfernt wird, müssen diese beiden Methoden diese Änderung beim nächsten Aufrufen widerspiegeln.
-   [**IPropertyStore:: GetValue**](/previous-versions/windows/desktop/legacy/bb761473(v=vs.85)): Wenn diese Methode für einen Wert, der nicht vorhanden ist, angefordert wird, gibt Sie " **S \_ OK** " zurück, wobei der als "VT Empty" gemeldete Wert angegeben wird \_ .

## <a name="writing-back-values"></a>Zurückschreiben von Werten

Wenn der Eigenschafts Handler den Wert einer Eigenschaft mithilfe von [**IPropertyStore:: SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85))schreibt, schreibt er erst den Wert in die Datei, wenn [**IPropertyStore:: Commit**](/previous-versions/windows/desktop/legacy/bb761470(v=vs.85)) aufgerufen wird. Der in-Memory-Cache kann bei der Implementierung dieses Schemas nützlich sein. Im Beispielcode legt die **IPropertyStore:: SetValue** -Implementierung einfach den neuen Wert im in-Memory-Cache fest und legt den Zustand dieser Eigenschaft auf PSC \_ Dirty fest.


```
HRESULT CRecipePropertyStore::SetValue(REFPROPERTYKEY key, const PROPVARIANT *pPropVar)
    {
    
    HRESULT hr = E_FAIL;
    
    if (IsEqualPropertyKey(key, PKEY_Search_Contents))
    {
        // This property is read-only
        hr = HRESULT_FROM_WIN32(ERROR_NOT_SUPPORTED);  
    }
    else
    {
        hr = _spCache->SetValueAndState(key, pPropVar, PSC_DIRTY);
    }
    
    return hr;
}
```



In jeder [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) -Implementierung wird das folgende Verhalten von [**IPropertyStore:: SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85))erwartet:

-   Wenn die Eigenschaft bereits vorhanden ist, wird der Wert der Eigenschaft festgelegt.
-   Wenn die Eigenschaft nicht vorhanden ist, wird die neue Eigenschaft hinzugefügt und der Wert festgelegt.
-   Wenn der Eigenschafts Wert nicht mit derselben Genauigkeit wie angegeben beibehalten werden kann (beispielsweise aufgrund von Größenbeschränkungen im Dateiformat), wird der Wert so weit wie möglich festgelegt, und es wird eine Unterbindung von "Inplace \_ S" \_ zurückgegeben.
-   Wenn die Eigenschaft nicht vom Eigenschaften Handler unterstützt wird, `HRESULT_FROM_WIN32(ERROR_NOT_SUPPORTED)` wird zurückgegeben.
-   Wenn ein anderer Grund dafür vorliegt, dass der Eigenschafts Wert nicht festgelegt werden kann, z. b. wenn die Datei gesperrt ist oder keine Rechte zum Bearbeiten über Zugriffs Steuerungs Listen (Access Control Lists, ACLs) vorhanden sind, wird STG \_ E \_ AccessDenied zurückgegeben.

Ein wichtiger Vorteil der Verwendung von Streams als Beispiel ist die Zuverlässigkeit. Eigenschaften Handler müssen immer in Erwägung ziehen, dass eine Datei im Falle eines schwerwiegenden Fehlers nicht in einem inkonsistenten Zustand belassen wird. Das beschädigen der Dateien eines Benutzers sollte offensichtlich vermieden werden, und die beste Vorgehensweise hierfür ist ein "Copy-on-Write"-Mechanismus. Wenn Ihr Eigenschaften Handler einen Stream für den Zugriff auf eine Datei verwendet, erhalten Sie dieses Verhalten automatisch. Das System schreibt alle Änderungen in den Stream und ersetzt die Datei nur während des Commitvorgangs durch die neue Kopie.

Wenn Sie dieses Verhalten außer Kraft setzen und den Datei Speicherungs Prozess manuell steuern möchten, können Sie das sichere Speicherverhalten ablehnen, indem Sie den Wert von manualsafesave in den Registrierungs Eintrag Ihres Handlers festlegen, wie hier gezeigt.

```
HKEY_CLASSES_ROOT
   CLSID
      {66742402-F9B9-11D1-A202-0000F81FEDEE}
         ManualSafeSave = 1
```

Wenn ein Handler den Wert manualsafesave angibt, ist der Stream, mit dem er initialisiert wird, kein transaktiver Datenstrom (STGM \_ transaktiv). Der Handler selbst muss die Safe Save-Funktion implementieren, um sicherzustellen, dass die Datei nicht beschädigt ist, wenn der Speichervorgang unterbrochen wird. Wenn der Handler direkte Schreibvorgänge implementiert, wird er in den Stream geschrieben, den er erhält. Wenn der Handler dieses Feature nicht unterstützt, muss er einen Stream abrufen, mit dem die aktualisierte Kopie der Datei mit [**idestinationstreamfactory:: getdestinationstream**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-idestinationstreamfactory-getdestinationstream)geschrieben werden kann. Nachdem der Handler das Schreiben abgeschlossen hat, sollte er im ursprünglichen Stream [**IPropertyStore:: Commit**](/previous-versions/windows/desktop/legacy/bb761470(v=vs.85)) aufrufen, um den Vorgang abzuschließen, und den Inhalt des ursprünglichen Streams durch die neue Kopie der Datei ersetzen.

Manualsafesave ist auch die Standardsituation, wenn Sie den Handler nicht mit einem Stream initialisieren. Ohne einen ursprünglichen Stream zum Empfangen der Inhalte des temporären Streams müssen Sie [**ReplaceFile**](/windows/win32/api/winbase/nf-winbase-replacefilea) verwenden, um eine atomarische Ersetzung der Quelldatei vorzunehmen.

Große Dateiformate, die auf eine Weise verwendet werden, um Dateien zu erstellen, die größer als 1 MB sind, sollten die Unterstützung für direktes Schreiben von Eigenschaften implementieren. Andernfalls erfüllt das Leistungsverhalten nicht die Erwartungen von Clients des Eigenschaften Systems. In diesem Szenario sollte die für das Schreiben von Eigenschaften erforderliche Zeit nicht von der Dateigröße betroffen sein.

Für sehr große Dateien, z. b. eine Videodatei mit 1 GB oder mehr, ist eine andere Lösung erforderlich. Wenn in der Datei nicht genügend Speicherplatz für das direkte Schreiben vorhanden ist, kann es sein, dass der Handler die Aktualisierung der Eigenschaft misslingt, wenn der Speicherplatz, der für das Schreiben von direkten Eigenschaften reserviert ist, erschöpft ist. Dieser Fehler tritt auf, um eine schlechte Leistung zu vermeiden, die von 2 GB e/a verursacht wird (1 zum Lesen, 1 zum Schreiben). Aufgrund dieses möglichen Fehlers sollten diese Dateiformate ausreichend Speicherplatz für das Schreiben von direkten Eigenschaften reservieren.

Wenn die Datei über genügend Speicherplatz verfügt, um Metadaten zu schreiben, und wenn das Schreiben dieser Metadaten nicht bewirkt, dass die Datei vergrößert oder verkleinert wird, ist es möglicherweise sicher, direkt zu schreiben. Wir empfehlen 64 KB als Ausgangspunkt. Das Schreiben direkt ist äquivalent zum Handler, der manualsafesave anfordert und [**IStream:: Commit**](/windows/win32/api/objidl/nf-objidl-istream-commit) in der Implementierung von [**IPropertyStore:: Commit**](/previous-versions/windows/desktop/legacy/bb761470(v=vs.85))anfordert und eine viel bessere Leistung als Copy-on-Write-Vorgänge aufweist. Wenn sich die Dateigröße aufgrund von Eigenschafts Wertänderungen ändert, sollte das Schreiben direkt erfolgen, weil eine beschädigte Datei im Falle einer nicht ordnungsgemäßen Beendigung nicht ordnungsgemäß geschrieben werden kann.

> [!Note]  
> Aus Leistungsgründen wird empfohlen, die Option manualsafesave mit Eigenschaften Handlern zu verwenden, die mit Dateien arbeiten, die 100 KB oder größer sind.

 

Wie in der folgenden Beispiel Implementierung von [**IPropertyStore:: Commit**](/previous-versions/windows/desktop/legacy/bb761470(v=vs.85))veranschaulicht, wird der Handler für manualsafesave registriert, um die Option für die manuelle sichere Speicherung zu veranschaulichen. Die **\_ savecachetodom** -Methode schreibt die im Arbeitsspeicher Cache gespeicherten Eigenschaftswerte in das XmlDocument-Objekt.


```
HRESULT CRecipePropertyStore::Commit()
{
    HRESULT hr = E_UNEXPECTED;
    if (_pCache)
    {
        // Check grfMode to ensure writes are allowed.
        hr = STG_E_ACCESSDENIED;
        if (_grfMode & STGM_READWRITE)
        {
            // Save the internal value cache to XML DOM object.
            hr = _SaveCacheToDom();
            if (SUCCEEDED(hr))
            {
                // Reset the output stream.
                LARGE_INTEGER liZero = {};
                hr = _pStream->Seek(liZero, STREAM_SEEK_SET, NULL);
```



Stellen Sie als nächstes die Frage, ob das pcified [**idestinationstreamfactory**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-idestinationstreamfactory)unterstützt.


```
                        if (SUCCEEDED(hr))
                        {
                            // Write the XML out to the temprorary stream and commit it.
                            VARIANT varStream = {};
                            varStream.vt = VT_UNKNOWN;
                            varStream.punkVal = pStreamCommit;
                            hr = _pDomDoc->save(varStream);
                            if (SUCCEEDED(hr))
                            {
                                hr = pStreamCommit->Commit(STGC_DEFAULT);_
```



Übertragen Sie als nächstes den ursprünglichen Stream, der die Daten auf sichere Weise in die ursprüngliche Datei schreibt.


```
                        if (SUCCEEDED(hr))
                                {
                                    // Commit the real output stream.
                                    _pStream->Commit(STGC_DEFAULT);
                                }
                            }

                            pStreamCommit->Release();
                        }

                        pSafeCommit->Release();
                    }
                }
            }
        }
    }
```



Untersuchen Sie dann die **\_ savecachetodom** -Implementierung.


```
// Saves the values in the internal cache back to the internal DOM object.
HRESULT CRecipePropertyStore::_SaveCacheToDom()
{
    // Iterate over each property in the internal value cache.
    DWORD cProps;  
```



Im nächsten Schritt wird die Anzahl der Eigenschaften, die im Arbeitsspeicher Cache gespeichert werden, angezeigt.


```
HRESULT hr = _pCache->GetCount(&cProps);          
            
```



Durchlaufen Sie nun die Eigenschaften, um zu bestimmen, ob der Wert einer Eigenschaft geändert wurde, seit Sie in den Arbeitsspeicher geladen wurde.


```
    for (UINT i = 0; SUCCEEDED(hr) && (i < cProps); ++i)
    {
        PROPERTYKEY key;
        hr = _pCache->GetAt(i, &key); 
```



Mit der [**ipropertystorecache:: GetState**](/windows/win32/api/propsys/nf-propsys-ipropertystorecache-getstate) -Methode wird der Zustand der Eigenschaft im Cache abgerufen. Das PSC- \_ Flag "Dirty", das in der [**IPropertyStore:: SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85)) -Implementierung festgelegt wurde, markiert eine Eigenschaft als geändert.


```
        if (SUCCEEDED(hr))
        {
            // check the cache state; only save dirty properties
            PSC_STATE psc;
            hr = _pCache->GetState(key, &psc);
            if (SUCCEEDED(hr) && psc == PSC_DIRTY)
            {
                // get the cached value
                PROPVARIANT propvar = {};
                hr = _pCache->GetValue(key, &propvar); 
```



Ordnen Sie die-Eigenschaft dem XML-Knoten zu, wie im Feld z. b. **\_ rgpropertymap** angegeben.


```
if (SUCCEEDED(hr))
                {
                    // save as a native property if the key is in the property map
                    BOOL fIsNativeProperty = FALSE;
                    for (UINT i = 0; i < ARRAYSIZE(g_rgPROPERTYMAP); ++i)
                    {
                        if (IsEqualPropertyKey(key, *g_rgPROPERTYMAP[i].pkey))
                        {
                            fIsNativeProperty = TRUE;
                            hr = _SaveProperty(propvar, g_rgPROPERTYMAP[i]);
                            break;
                        }     
```



Wenn eine Eigenschaft nicht in der Zuordnung angezeigt wird, handelt es sich um eine neue Eigenschaft, die von Windows Explorer festgelegt wurde. Da Open Metadata unterstützt wird, speichern Sie die neue Eigenschaft im **ExtendedProperties** -Abschnitt der XML-Datei.


```
                    
                    // Otherwise, save as an extended property.
                    if (!fIsNativeProperty)
                    {
                        hr = _SaveExtendedProperty(key, propvar);
                    }

                    PropVariantClear(&propvar);
                }
            }
        }
    }

    return hr;    
```



## <a name="implementing-ipropertystorecapabilities"></a>Implementieren von ipropertystorecapabilitäten

[**Ipropertystorecapabiliinformiert**](/windows/win32/api/propsys/nn-propsys-ipropertystorecapabilities) die Shell-Benutzeroberfläche, ob eine bestimmte Eigenschaft in der Shellbenutzeroberfläche bearbeitet werden kann. Beachten Sie, dass sich dies nur auf die Möglichkeit bezieht, die Eigenschaft in der Benutzeroberfläche zu bearbeiten, nicht, ob Sie [**IPropertyStore:: SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85)) für die Eigenschaft erfolgreich aufrufen können. Eine Eigenschaft, die den Rückgabewert S \_ false aus [**ipropertystorecapabili:: ispropertywrite Table**](/windows/win32/api/propsys/nf-propsys-ipropertystorecapabilities-ispropertywritable) provoziert, kann möglicherweise trotzdem über eine Anwendung festgelegt werden.


```
interface IPropertyStoreCapabilities : IUnknown
{
    HRESULT IsPropertyWritable([in] REFPROPERTYKEY key);
}
```



[**Ispropertywrite Table**](/windows/win32/api/propsys/nf-propsys-ipropertystorecapabilities-ispropertywritable) gibt **S \_ OK** zurück, um anzugeben, dass Endbenutzer die Eigenschaft direkt bearbeiten dürfen. \_False gibt an, dass dies nicht der Fall sein sollte. ' \_ False ' kann bedeuten, dass Anwendungen für das Schreiben der Eigenschaft zuständig sind, nicht für Benutzer. Die Shell deaktiviert Bearbeitungs Steuerelemente entsprechend den Ergebnissen von Aufrufen dieser Methode je nach Bedarf. Bei einem Handler, der [**ipropertystorecapabilinicht**](/windows/win32/api/propsys/nn-propsys-ipropertystorecapabilities) implementiert, wird angenommen, dass er Open Metadata durch Unterstützung für das Schreiben einer beliebigen Eigenschaft unterstützt.

Wenn Sie einen Handler erstellen, der nur schreibgeschützte Eigenschaften behandelt, sollten Sie die **Initialize** -Methode ([**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream), [**IInitializeWithItem**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem)oder [**IInitializeWithFile**](/windows/win32/api/propsys/nn-propsys-iinitializewithfile)) implementieren, damit Sie STG \_ E AccessDenied zurückgibt, wenn Sie \_ mit dem STGM- \_ leseschreib Flag aufgerufen wird.

Für einige Eigenschaften ist das [isinnate](./propdesc-schema-typeinfo.md) -Attribut auf " **true**" festgelegt. Angeborene Eigenschaften haben die folgenden Merkmale:

-   Die-Eigenschaft wird in der Regel auf irgendeine Weise berechnet. Beispielsweise `System.Image.BitDepth` wird anhand des Bilds berechnet.
-   Das Ändern der Eigenschaft wäre nicht sinnvoll, ohne die Datei zu ändern. Wenn Sie beispielsweise `System.Image.Dimensions` die Größe des Bilds ändern, wird die Größe des Bilds nicht geändert, daher ist es nicht sinnvoll, es dem Benutzer zu gestatten.
-   In einigen Fällen werden diese Eigenschaften vom System automatisch bereitgestellt. Zu den Beispielen gehören `System.DateModified` , die vom Dateisystem bereitgestellt werden, und `System.SharedWith` , der darauf basiert, wer der Benutzer für die Datei freigegeben hat.

Aufgrund dieser Merkmale werden Eigenschaften, die als *isinnate* gekennzeichnet sind, dem Benutzer nur als schreibgeschützte Eigenschaften in der Shell-Benutzeroberfläche bereitgestellt. Wenn eine Eigenschaft als *isinnate* gekennzeichnet ist, speichert das Eigenschaften System diese Eigenschaft nicht im Eigenschaften Handler. Daher benötigen Eigenschaften Handler keinen speziellen Code, um diese Eigenschaften in ihren Implementierungen zu berücksichtigen. Wenn der Wert des *isinnate* -Attributs nicht explizit für eine bestimmte Eigenschaft angegeben wird, ist der Standardwert **false**.

## <a name="registering-and-distributing-property-handlers"></a>Registrieren und Verteilen von Eigenschaften Handlern

Nachdem der Eigenschaften Handler implementiert wurde, muss er registriert und seine Dateinamenerweiterung dem Handler zugeordnet sein. Weitere Informationen finden Sie unter [registrieren und Verteilen von Eigenschaften Handlern](./prophand-reg-dist.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Grundlegendes zu Eigenschaften Handlern](./building-property-handlers-properties.md)
</dt> <dt>

[Verwenden von Kind-Namen](./building-property-handlers-user-friendly-kind-names.md)
</dt> <dt>

[Verwenden von Eigenschaften Listen](./building-property-handlers-property-lists.md)
</dt> <dt>

[Registrieren und Verteilen von Eigenschaften Handlern](./prophand-reg-dist.md)
</dt> <dt>

[Bewährte Methoden und häufig gestellte Fragen zu Eigenschaften Handlern](./prophand-bestprac-faq.md)
</dt> </dl>

 

 
