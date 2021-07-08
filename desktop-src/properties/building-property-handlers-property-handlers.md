---
description: In diesem Artikel wird erläutert, wie Eigenschaftenhandler für die Arbeit mit dem Windows Eigenschaftensystem initialisiert werden.
ms.assetid: 3b54dd65-b7db-4e6a-bc3d-1008fdabcfa9
title: Initialisieren von Eigenschaftenhandlern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4482af2a029a91049d421ee49eb0f439c5fd8d0e
ms.sourcegitcommit: ecd0ba4732f5264aab9baa2839c11f7fea36318f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/07/2021
ms.locfileid: "113481905"
---
# <a name="initializing-property-handlers"></a>Initialisieren von Eigenschaftenhandlern

In diesem Thema wird erläutert, wie Eigenschaftenhandler für die Arbeit mit dem Windows Eigenschaftensystem erstellt und registriert werden.

Dieses Thema ist wie folgt organisiert:

-   [Eigenschaftenhandler](#property-handlers)
-   [Vorbereitungen](#before-you-begin)
-   [Initialisieren von Eigenschaftenhandlern](#initializing-property-handlers)
-   [In-Memory-Eigenschafts-Store](#in-memory-property-store)
-   [Umgang mit PROPVARIANT-Based Werten](#dealing-with-propvariant-based-values)
-   [Unterstützen von offenen Metadaten](#supporting-open-metadata)
-   [Volltextinhalt](#full-text-contents)
-   [Bereitstellen von Werten für Eigenschaften](#providing-values-for-properties)
-   [Zurückschreiben von Werten](#writing-back-values)
-   [Implementieren von IPropertyStoreCapabilities](#implementing-ipropertystorecapabilities)
-   [Registrieren und Verteilen von Eigenschaftenhandlern](#registering-and-distributing-property-handlers)
-   [Verwandte Themen](#related-topics)

## <a name="property-handlers"></a>Eigenschaftenhandler

Eigenschaftenhandler sind ein wichtiger Bestandteil des Eigenschaftensystems. Sie werden prozessin-process vom Indexer aufgerufen, um Eigenschaftswerte zu lesen und zu indizieren, und sie werden auch von Windows Explorer in-process aufgerufen, um Eigenschaftswerte direkt in den Dateien zu lesen und zu schreiben. Diese Handler müssen sorgfältig geschrieben und getestet werden, um leistungsbeeinträchtigungen oder Datenverlust in den betroffenen Dateien zu verhindern. Weitere Informationen zu indexerspezifischen Überlegungen, die sich auf die Implementierung von Eigenschaftenhandlern auswirken, finden Sie unter [Developing Property Handlers for Windows Search](../search/-search-3x-wds-extidx-propertyhandlers.md).

In diesem Thema wird ein XML-basiertes Beispieldateiformat erläutert, das ein Rezept mit der Dateierweiterung ".recipe" beschreibt. Die Dateierweiterung .recipe wird als eigenes unterschiedliches Dateiformat registriert, anstatt sich auf das allgemeinere .xml Dateiformat zu verlassen, dessen Handler einen sekundären Stream zum Speichern von Eigenschaften verwendet. Es wird empfohlen, eindeutige Dateinamenerweiterungen für Ihre Dateitypen zu registrieren.

## <a name="before-you-begin"></a>Vorbereitungen

Eigenschaftenhandler sind COM-Objekte, die die [**IPropertyStore-Abstraktion**](/windows/win32/api/propsys/nn-propsys-ipropertystore) für ein bestimmtes Dateiformat erstellen. Sie lesen (analysieren) und schreiben dieses Dateiformat in einer Weise, die der Spezifikation entspricht. Einige Eigenschaftenhandler arbeiten basierend auf APIs, die den Zugriff auf ein bestimmtes Dateiformat abstrahieren. Bevor Sie einen Eigenschaftenhandler für Ihr Dateiformat entwickeln, müssen Sie verstehen, wie Ihr Dateiformat Eigenschaften speichert und wie diese Eigenschaften (Namen und Werte) der Abstraktion des Eigenschaftenspeichers zugeordnet werden.

Beachten Sie beim Planen der Implementierung, dass Eigenschaftenhandler Komponenten auf niedriger Ebene sind, die im Kontext von Prozessen wie Windows Explorer, dem Windows Search-Indexer und Anwendungen von Drittanbietern geladen werden, die das Shell-Elementprogrammiermodell verwenden. Daher können Eigenschaftenhandler nicht in verwaltetem Code implementiert werden und sollten in C++ implementiert werden. Wenn Ihr Handler APIs oder Dienste verwendet, um seine Arbeit zu erledigen, müssen Sie sicherstellen, dass diese Dienste in den Umgebungen, in denen ihr Eigenschaftenhandler geladen wird, ordnungsgemäß funktionieren können.

> [!Note]  
> Eigenschaftenhandler werden immer bestimmten Dateitypen zugeordnet. Wenn Ihr Dateiformat Eigenschaften enthält, die einen benutzerdefinierten Eigenschaftenhandler erfordern, sollten Sie daher immer eine eindeutige Dateinamenerweiterung für jedes Dateiformat registrieren.

 

## <a name="initializing-property-handlers"></a>Initialisieren von Eigenschaftenhandlern

Bevor eine Eigenschaft vom System verwendet wird, wird sie durch Aufrufen einer Implementierung von [**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream)initialisiert. Der Eigenschaftenhandler sollte initialisiert werden, indem das System ihm einen Stream zuweist, anstatt diese Zuweisung der Handlerimplementierung zu überlassen. Diese Initialisierungsmethode stellt Folgendes sicher:

-   Der Eigenschaftenhandler kann in einem eingeschränkten Prozess (einem wichtigen Sicherheitsfeature) ausgeführt werden, ohne über Zugriffsrechte zum direkten Lesen oder Schreiben von Dateien zu verfügen, anstatt über den Stream auf deren Inhalt zuzugreifen.
-   Das System kann als vertrauenswürdig eingestuft werden, um die Dateioplocks ordnungsgemäß zu verarbeiten. Dies ist ein wichtiges Maß für die Zuverlässigkeit.
-   Das Eigenschaftensystem bietet einen automatischen sicheren Speicherdienst ohne zusätzliche Funktionalität, die von der Implementierung des Eigenschaftenhandlers benötigt wird. Weitere Informationen zu Streams finden Sie im Abschnitt Zurückschreiben von [Werten.](#writing-back-values)
-   Die Verwendung von [**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream) abstrahiert Ihre Implementierung aus Dateisystemdetails. Dadurch kann der Handler die Initialisierung über alternative Speicher unterstützen, z. B. einen FTP-Ordner (File Transfer Protocol) oder eine komprimierte Datei mit einer .zip Dateinamenerweiterung.

Es gibt Fälle, in denen die Initialisierung mit Streams nicht möglich ist. In diesen Situationen gibt es zwei weitere Schnittstellen, die Eigenschaftenhandler implementieren können: [**IInitializeWithFile**](/windows/win32/api/propsys/nn-propsys-iinitializewithfile) und [**IInitializeWithItem.**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem) Wenn ein Eigenschaftenhandler [**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream)nicht implementiert, muss er die Ausführung in dem isolierten Prozess deaktivieren, in den der Systemindexer ihn standardmäßig platzieren würde, wenn eine Änderung am Stream vorgenommen würde. Um dieses Feature zu deaktivieren, legen Sie den folgenden Registrierungswert fest.

```
HKEY_CLASSES_ROOT
   CLSID
      {66742402-F9B9-11D1-A202-0000F81FEDEE}
         DisableProcessIsolation = 1
```

Es ist jedoch viel besser, [**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream) zu implementieren und eine streambasierte Initialisierung durchzuführen. Ihr Eigenschaftenhandler ist daher sicherer und zuverlässiger. Das Deaktivieren der Prozessisolation ist in der Regel nur für Legacyeigenschaftenhandler vorgesehen und sollte durch neuen Code mühsam vermieden werden.

Um die Implementierung eines Eigenschaftenhandlers im Detail zu untersuchen, sehen Sie sich das folgende Codebeispiel an, bei dem es sich um eine Implementierung von [**IInitializeWithStream::Initialize handelt.**](/windows/win32/api/propsys/nf-propsys-iinitializewithstream-initialize) Der Handler wird initialisiert, indem ein XML-basiertes Rezeptdokument über einen Zeiger auf die zugeordnete [**IStream-Instanz**](/windows/win32/api/objidl/nn-objidl-istream) des Dokuments geladen wird. Die variable **\_ spDocEle,** die am Ende des Codebeispiels verwendet wird, wird weiter oben im Beispiel als MSXML2::IXMLDOMElementPtr definiert.

> [!Note]  
> Die folgenden und alle nachfolgenden Codebeispiele stammen aus dem Rezepthandlerbeispiel, das im Windows Software Development Kit (SDK) enthalten ist. .

 


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

Nachdem das Dokument selbst geladen wurde, werden die in Windows Explorer anzuzeigenden Eigenschaften geladen, indem die geschützte **\_ LoadProperties-Methode** aufgerufen wird, wie im folgenden Codebeispiel veranschaulicht. Dieser Prozess wird im nächsten Abschnitt ausführlich untersucht.


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



Wenn der Stream schreibgeschützt ist, aber der *grfMode-Parameter* das STGM \_ READWRITE-Flag enthält, sollte die Initialisierung fehlschlagen und STG \_ E \_ ACCESSDENIED zurückgeben. Ohne diese Überprüfung zeigt Windows Explorer die Eigenschaftswerte als schreibbar an, obwohl sie nicht schreibbar sind, was zu einer verwirrenden Endbenutzererfahrung führt.

Der Eigenschaftenhandler wird nur einmal in seiner Lebensdauer initialisiert. Wenn eine zweite Initialisierung angefordert wird, sollte der Handler `HRESULT_FROM_WIN32(ERROR_ALREADY_INITIALIZED)` zurückgeben.

## <a name="in-memory-property-store"></a>In-Memory Property Store

Bevor Sie sich die Implementierung von **\_ LoadProperties** ansehen, sollten Sie das **PropertyMap-Array** verstehen, das im Beispiel verwendet wird, um Eigenschaften im XML-Dokument vorhandenen Eigenschaften im Eigenschaftensystem über ihre PKEY-Werte zuzuordnen.

Sie sollten nicht jedes Element und Attribut in der XML-Datei als Eigenschaft verfügbar machen. Wählen Sie stattdessen nur diejenigen aus, von denen Sie glauben, dass sie für Endbenutzer in der Organisation ihrer Dokumente nützlich sind (in diesem Fall Rezepte). Dies ist ein wichtiges Konzept, das Sie beim Entwickeln Ihrer Eigenschaftenhandler beachten sollten: der Unterschied zwischen Informationen, die für Organisationsszenarien wirklich nützlich sind, und Informationen, die zu den Details Ihrer Datei gehören und durch Öffnen der Datei selbst angezeigt werden können. Eigenschaften sollen keine vollständige Duplizierung einer XML-Datei sein.


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



Hier ist die vollständige Implementierung der **\_ LoadProperties-Methode,** die von [**IInitializeWithStream::Initialize**](/windows/win32/api/propsys/nf-propsys-iinitializewithstream-initialize)aufgerufen wird.


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



Die **\_ LoadProperties-Methode** ruft die Shell-Hilfsfunktion [**PSCreateMemoryPropertyStore**](/windows/win32/api/propsys/nf-propsys-pscreatememorypropertystore) auf, um einen In-Memory-Eigenschaftenspeicher (Cache) für die behandelten Eigenschaften zu erstellen. Mithilfe eines Caches werden Änderungen für Sie nachverfolgt. Dadurch können Sie nicht nachverfolgen, ob ein Eigenschaftswert im Cache geändert, aber noch nicht im persistenten Speicher gespeichert wurde. Außerdem können Sie eigenschaftswerte, die sich nicht geändert haben, unnötigerweise beibehalten.

Die **\_ LoadProperties-Methode** ruft auch **\_ LoadProperty** auf, dessen Implementierung im folgenden Code veranschaulicht wird) einmal für jede zugeordnete Eigenschaft. **\_ LoadProperty** ruft den Wert der Eigenschaft ab, wie im **PropertyMap-Element** im XML-Stream angegeben, und weist ihn dem In-Memory-Cache über einen Aufruf von [**IPropertyStoreCache::SetValueAndState**](/windows/win32/api/propsys/nf-propsys-ipropertystorecache-setvalueandstate)zu. Das PSC \_ NORMAL-Flag im Aufruf von **IPropertyStoreCache::SetValueAndState** gibt an, dass der Eigenschaftswert seit dem Eintritt in den Cache nicht geändert wurde.


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

In der Implementierung von **\_ LoadProperty** wird ein Eigenschaftswert in Form eines [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)bereitgestellt. Eine Reihe von APIs im Software Development Kit (SDK) wird bereitgestellt, um von primitiven Typen wie **PWSTR** oder **int** in oder von **PROPVARIANT-Typen** zu konvertieren. Diese APIs befinden sich in Propvarutil.h.

Um z. B. eine [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) in eine Zeichenfolge zu konvertieren, können Sie [**PropVariantToString**](/windows/win32/api/propvarutil/nf-propvarutil-propvarianttostring) verwenden, wie hier dargestellt.


```
PropVariantToString(REFPROPVARIANT propvar, PWSTR psz, UINT cch);
```



Zum Initialisieren einer PROPVARIANT-Eigenschaft aus einer Zeichenfolge können Sie [**InitPropVariantFromString**](/windows/win32/api/propvarutil/nf-propvarutil-initpropvariantfromstring)verwenden.


```
InitPropVariantFromString(PCWSTR psz, PROPVARIANT *ppropvar);
```



Wie Sie in jeder der im Beispiel enthaltenen Rezeptdateien sehen können, kann jede Datei mehrere Schlüsselwörter enthalten. Um dies zu berücksichtigen, unterstützt das Eigenschaftensystem mehrwertige Zeichenfolgen, die als Vektor von Zeichenfolgen dargestellt werden (z. B. "VT \_ VECTOR \| VT \_ LPWSTR"). Die **\_ LoadVectorProperty-Methode** im Beispiel verwendet vektorbasierte Werte.


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



Wenn ein Wert in der Datei nicht vorhanden ist, geben Sie keinen Fehler zurück. Legen Sie stattdessen den Wert auf VT EMPTY fest, \_ und geben Sie S **\_ OK** zurück. VT \_ EMPTY gibt an, dass der Eigenschaftswert nicht vorhanden ist.

## <a name="supporting-open-metadata"></a>Unterstützen von offenen Metadaten

In diesem Beispiel wird ein XML-basiertes Dateiformat verwendet. Das Schema kann erweitert werden, um Eigenschaften zu unterstützen, die z. B. während der Entwicklung nicht bedacht wurden. Dieses System wird als offene Metadaten bezeichnet. In diesem Beispiel wird das Eigenschaftensystem erweitert, indem ein Knoten unter dem **Recipe-Element** namens **ExtendedProperties** erstellt wird, wie im folgenden Codebeispiel veranschaulicht.


```
<ExtendedProperties>
    <Property 
        Name="{65A98875-3C80-40AB-ABBC-EFDAF77DBEE2}, 100"
        EncodedValue="HJKHJDHKJHK"/>
</ExtendedProperties>
```



Um persistente erweiterte Eigenschaften während der Initialisierung zu laden, implementieren Sie die **\_ LoadExtendedProperties-Methode,** wie im folgenden Codebeispiel veranschaulicht.


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



In Propsys.h deklarierte Serialisierungs-APIs werden verwendet, um [**PROPVARIANT-Typen**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) in Datenblobs zu serialisieren und zu deserialisieren. Anschließend wird die Base64-Codierung verwendet, um diese Blobs in Zeichenfolgen zu serialisieren, die im XML gespeichert werden können. Diese Zeichenfolgen werden im **EncodedValue-Attribut** des **ExtendedProperties-Elements** gespeichert. Die folgende Hilfsprogrammmethode, die in der Datei "Util.cpp" des Beispiels implementiert ist, führt die Serialisierung aus. Sie beginnt mit einem Aufruf der [**StgSerializePropVariant-Funktion,**](/windows/win32/api/propvarutil/nf-propvarutil-stgserializepropvariant) um die binäre Serialisierung durchzuführen, wie im folgenden Codebeispiel veranschaulicht.


```
HRESULT SerializePropVariantAsString(const PROPVARIANT *ppropvar, PWSTR *pszOut)
{
    SERIALIZEDPROPERTYVALUE *pBlob;
    ULONG cbBlob;
    HRESULT hr = StgSerializePropVariant(ppropvar, &pBlob, &cbBlob);
```



Als Nächstes führt die in Wincrypt.h deklarierte [**CryptBinaryToString-Funktion**](/windows/win32/api/wincrypt/nf-wincrypt-cryptbinarytostringa)die Base64-Konvertierung durch.


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



Die **DeserializePropVariantFromString-Funktion,** die sich auch in Util.cpp befindet, kehrt den Vorgang um und deserialisiert Werte aus der XML-Datei.

Informationen zur Unterstützung geöffneter Metadaten finden Sie unter "Dateitypen, die offene Metadaten unterstützen" in [Dateitypen.](../shell/fa-file-types.md)

## <a name="full-text-contents"></a>Full-Text Inhalt

Eigenschaftshandler können auch eine Volltextsuche des Dateiinhalts ermöglichen und stellen eine einfache Möglichkeit zur Bereitstellung dieser Funktionalität zur Verfügung, wenn das Dateiformat nicht zu kompliziert ist. Es gibt eine alternative, leistungsfähigere Möglichkeit, den vollständigen Text der Datei über die [**IFilter-Schnittstellenimplementierung**](/windows/win32/api/filter/nn-filter-ifilter) zur Verfügung zu stellen.

In der folgenden Tabelle werden die Vorteile der einzelnen Ansätze mit [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) oder [**IPropertyStore zusammengefasst.**](/windows/win32/api/propsys/nn-propsys-ipropertystore)



| Funktion                                   | Ifilter                      | Ipropertystore |
|----------------------------------------------|------------------------------|----------------|
| Ermöglicht das Zurückschreiben in Dateien?                  | Nein                           | Ja            |
| Bietet eine Mischung aus Inhalt und Eigenschaften?      | Ja                          | Ja            |
| Mehrsprachige?                                | Ja                          | Nein             |
| MIME/Embedded?                               | Ja                          | Nein             |
| Textgrenzen?                             | Satz, Absatz, Kapitel | Keine           |
| Unterstützte Implementierung für SPS/SQL Server? | Ja                          | Nein             |
| Implementierung                               | Komplex                      | Einfach         |



 

Im Beispiel für den Rezepthandler hat das Format der Rezeptdatei keine komplexen Anforderungen, sodass nur [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) für die Volltextunterstützung implementiert wurde. Die Volltextsuche wird für die XML-Knoten implementiert, die im folgenden Array benannt sind.


```
const PWSTR c_rgszContentXPath[] = {
    L"Recipe/Ingredients/Item",
    L"Recipe/Directions/Step",
    L"Recipe/RecipeInfo/Yield",
    L"Recipe/RecipeKeywords/Keyword",
};
```



Das Eigenschaftensystem enthält die Eigenschaft (PKEY Search Contents), die erstellt wurde, um volltextbasierten Inhalt für den `System.Search.Contents` \_ \_ Indexer zur Verfügung zu stellen. Der Wert dieser Eigenschaft wird nie direkt auf der Benutzeroberfläche angezeigt. Der Text aller XML-Knoten, die im obigen Array benannt sind, wird zu einer einzelnen Zeichenfolge verkettet. Diese Zeichenfolge wird dann dem Indexer als Volltextinhalt der Rezeptdatei durch einen Aufruf von [**IPropertyStoreCache::SetValueAndState**](/windows/win32/api/propsys/nf-propsys-ipropertystorecache-setvalueandstate) bereitgestellt, wie im folgenden Codebeispiel veranschaulicht.


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



## <a name="providing-values-for-properties"></a>Bereitstellen von Werten für Eigenschaften

Beim Lesen von Werten werden Eigenschaftshandler in der Regel aus einem der folgenden Gründe aufgerufen:

-   Zum Aufzählen aller Eigenschaftswerte.
-   So erhalten Sie den Wert einer bestimmten Eigenschaft.

Bei der -Enumeration wird ein Eigenschaftenhandler aufgefordert, seine Eigenschaften entweder während der Indizierung oder beim Anzeigen von Eigenschaften in der Gruppe Sonstige im **Eigenschaftendialogfeld aufzählen.** Die Indizierung wird ständig als Hintergrundvorgang ausgeführt. Wenn sich eine Datei ändert, wird der Indexer benachrichtigt und die Datei neu indiziert, indem der Eigenschaftenhandler aufgefordert wird, seine Eigenschaften zu aufzählen. Daher ist es wichtig, dass Eigenschaftenhandler effizient implementiert werden und Eigenschaftswerte so schnell wie möglich zurückgeben. Enumerieren Sie alle Eigenschaften, für die Sie Werte haben, genau wie für jede Sammlung, aber aufzählen Sie keine Eigenschaften, die speicherintensive Berechnungen oder Netzwerkanforderungen beinhalten, die das Abrufen verlangsamen könnten.

Beim Schreiben eines Eigenschaftenhandlers müssen Sie in der Regel die folgenden beiden Sätze von Eigenschaften berücksichtigen.

-   Primäre Eigenschaften: Eigenschaften, die ihr Dateityp nativ unterstützt. Beispielsweise unterstützt ein Fotoeigenschaftshandler für Exchangeable Image File (EXIF)-Metadaten nativ `System.Photo.FNumber` .
-   Erweiterte Eigenschaften: Eigenschaften, die ihr Dateityp als Teil geöffneter Metadaten unterstützt.

Da im Beispiel In-Memory-Cache verwendet wird, ist die Implementierung von [**IPropertyStore-Methoden**](/windows/win32/api/propsys/nn-propsys-ipropertystore) nur eine Frage der Delegierung an diesen Cache, wie im folgenden Codebeispiel veranschaulicht.


```
IFACEMETHODIMP GetCount(__out DWORD *pcProps)
{ return _spCache->GetCount(pcProps); }

IFACEMETHODIMP GetAt(DWORD iProp, __out PROPERTYKEY *pkey)
{ return _spCache->GetAt(iProp, pkey); }

IFACEMETHODIMP GetValue(REFPROPERTYKEY key, __out PROPVARIANT *pPropVar)
{ return _spCache->GetValue(key, pPropVar); }
```



Wenn Sie sich dafür entscheiden, nicht an den In-Memory-Cache zu delegieren, müssen Sie Ihre Methoden implementieren, um> folgendes erwartete Verhalten zu bieten:

-   [**IPropertyStore::GetCount:**](/previous-versions/windows/desktop/legacy/bb761472(v=vs.85))Wenn keine Eigenschaften verfügbar sind, gibt diese Methode **S \_ OK zurück.**
-   [**IPropertyStore::GetAt:**](/previous-versions/windows/desktop/legacy/bb761471(v=vs.85))Wenn *iProp* größer oder gleich *cProps* ist, gibt diese Methode E INVALIDARG zurück, und die Struktur, auf die der \_ *pkey-Parameter* zeigt, wird mit Nullen gefüllt.
-   [**IPropertyStore::GetCount**](/previous-versions/windows/desktop/legacy/bb761472(v=vs.85)) und [**IPropertyStore::GetAt**](/previous-versions/windows/desktop/legacy/bb761471(v=vs.85)) spiegeln den aktuellen Zustand des Eigenschaftenhandlers wider. Wenn [**ein PROPERTYKEY**](/windows/win32/api/wtypes/ns-wtypes-propertykey) über [**IPropertyStore::SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85))der Datei hinzugefügt oder daraus entfernt wird, müssen diese beiden Methoden diese Änderung widerspiegeln, wenn sie das nächste Mal aufgerufen werden.
-   [**IPropertyStore::GetValue:**](/previous-versions/windows/desktop/legacy/bb761473(v=vs.85))Wenn diese Methode nach einem Wert gefragt wird, der nicht vorhanden ist, wird **S \_ OK** mit dem Als VT EMPTY gemeldeten Wert \_ zurückgegeben.

## <a name="writing-back-values"></a>Zurückschreiben von Werten

Wenn der Eigenschaftenhandler den Wert einer Eigenschaft mithilfe von [**IPropertyStore::SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85))schreibt, wird der Wert erst in die Datei geschrieben, wenn [**IPropertyStore::Commit**](/previous-versions/windows/desktop/legacy/bb761470(v=vs.85)) aufgerufen wird. Der In-Memory-Cache kann bei der Implementierung dieses Schemas nützlich sein. Im Beispielcode legt die **IPropertyStore::SetValue-Implementierung** einfach den neuen Wert im In-Memory-Cache fest und legt den Zustand dieser Eigenschaft auf PSC \_ DIRTY fest.


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



In jeder [**IPropertyStore-Implementierung**](/windows/win32/api/propsys/nn-propsys-ipropertystore) wird das folgende Verhalten von [**IPropertyStore::SetValue erwartet:**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85))

-   Wenn die Eigenschaft bereits vorhanden ist, wird der Wert der -Eigenschaft festgelegt.
-   Wenn die Eigenschaft nicht vorhanden ist, wird die neue Eigenschaft hinzugefügt und ihr Wert festgelegt.
-   Wenn der Eigenschaftswert nicht mit der gleichen Genauigkeit beibehalten werden kann wie angegeben (z. B. Kürzung aufgrund von Größenbeschränkungen im Dateiformat), wird der Wert so weit wie möglich festgelegt, und INPLACE \_ S \_ TRUNCATED wird zurückgegeben.
-   Wenn die Eigenschaft vom Eigenschaftenhandler nicht unterstützt wird, `HRESULT_FROM_WIN32(ERROR_NOT_SUPPORTED)` wird zurückgegeben.
-   Wenn es einen anderen Grund gibt, dass der Eigenschaftswert nicht festgelegt werden kann, z. B. die gesperrte Datei oder fehlende Bearbeitungsrechte über Zugriffssteuerungslisten (ACCESS Control Lists, ACLs), wird STG \_ E \_ ACCESSDENIED zurückgegeben.

Ein hauptvorteil der Verwendung von Datenströmen ist die Zuverlässigkeit. Eigenschaftenhandler müssen immer berücksichtigen, dass sie eine Datei im Falle eines schwerwiegenden Fehlers nicht in einem inkonsistenten Zustand belasst. Eine Beschädigung der Dateien eines Benutzers sollte natürlich vermieden werden, und die beste Möglichkeit ist ein Mechanismus zum Kopieren beim Schreiben. Wenn ihr Eigenschaftenhandler einen Stream für den Zugriff auf eine Datei verwendet, wird dieses Verhalten automatisch ausgeführt. das System schreibt alle Änderungen in den Stream und ersetzt die Datei nur während des Commit-Vorgangs durch die neue Kopie.

Um dieses Verhalten zu überschreiben und den Dateisicherungsprozess manuell zu steuern, können Sie das sichere Speicherverhalten deaktivieren, indem Sie den Wert ManualSafeSave im Registrierungseintrag Ihres Handlers festlegen, wie hier dargestellt.

```
HKEY_CLASSES_ROOT
   CLSID
      {66742402-F9B9-11D1-A202-0000F81FEDEE}
         ManualSafeSave = 1
```

Wenn ein Handler den ManualSafeSave-Wert angibt, ist der Stream, mit dem er initialisiert wird, kein transaktiver Stream (STGM \_ TRANSACTED). Der Handler selbst muss die Sichere Speicherfunktion implementieren, um sicherzustellen, dass die Datei nicht beschädigt ist, wenn der Speichervorgang unterbrochen wird. Wenn der Handler das schreiben an Ort und Stelle implementiert, wird in den angegebenen Stream geschrieben. Wenn der Handler dieses Feature nicht unterstützt, muss er einen Stream abrufen, mit dem die aktualisierte Kopie der Datei mithilfe von [**IDestinationStreamFactory::GetDestinationStream geschrieben werden soll.**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-idestinationstreamfactory-getdestinationstream) Nachdem der Handler mit dem Schreiben fertig ist, sollte er [**IPropertyStore::Commit**](/previous-versions/windows/desktop/legacy/bb761470(v=vs.85)) für den ursprünglichen Stream aufrufen, um den Vorgang abschließen zu können, und den Inhalt des ursprünglichen Streams durch die neue Kopie der Datei ersetzen.

ManualSafeSave ist auch die Standardsituation, wenn Sie den Handler nicht mit einem Stream initialisieren. Ohne einen ursprünglichen Stream, der den Inhalt des temporären Streams empfangen soll, müssen Sie [**ReplaceFile**](/windows/win32/api/winbase/nf-winbase-replacefilea) verwenden, um eine atomare Ersetzung der Quelldatei durchzuführen.

Große Dateiformate, die auf eine Weise verwendet werden, die Dateien größer als 1 MB erzeugt, sollten Unterstützung für das Schreiben von in-place-Eigenschaften implementieren. Andernfalls erfüllt das Leistungsverhalten nicht die Erwartungen der Clients des Eigenschaftensystems. In diesem Szenario sollte die Zeit, die zum Schreiben von Eigenschaften erforderlich ist, nicht von der Dateigröße beeinflusst werden.

Für sehr große Dateien, z. B. eine Videodatei mit 1 GB oder mehr, ist eine andere Lösung erforderlich. Wenn nicht genügend Speicherplatz in der Datei vorhanden ist, um das schreibende Schreiben durchzuführen, kann der Handler die Aktualisierung der Eigenschaft fehlschlagen, wenn der für das Schreiben von in-place-Eigenschaften reservierte Speicherplatz erschöpft ist. Dieser Fehler tritt auf, um eine schlechte Leistung aufgrund von 2 GB E/A (1 für Lese-, 1 für Schreibzugriff) zu vermeiden. Aufgrund dieses potenziellen Fehlers sollten diese Dateiformate genügend Speicherplatz für das Schreiben von In-Place-Eigenschaften reservieren.

Wenn die Datei über genügend Speicherplatz im Header verfügt, um Metadaten zu schreiben, und wenn das Schreiben dieser Metadaten nicht dazu führt, dass die Datei anwächst oder verkleinert wird, kann es sicher sein, dass sie an Ort und Stelle geschrieben wird. Es wird empfohlen, 64 KB als Ausgangspunkt zu verwenden. Das schreiben an Ort und Stelle entspricht dem Handler, der in der Implementierung von [**IPropertyStore::Commit**](/previous-versions/windows/desktop/legacy/bb761470(v=vs.85))nach ManualSafeSave fragt und [**IStream::Commit**](/windows/win32/api/objidl/nf-objidl-istream-commit) aufruft, und bietet eine wesentlich bessere Leistung als beim Kopieren beim Schreiben. Wenn sich die Dateigröße aufgrund von Eigenschaftswertänderungen ändert, sollte aufgrund des Potenziellen einer beschädigten Datei im Fall einer nicht ungewöhnlichen Beendigung nicht versucht werden, an Ort und Stelle zu schreiben.

> [!Note]  
> Aus Leistungsgründen wird empfohlen, die Option ManualSafeSave mit Eigenschaftenhandlern zu verwenden, die mit Dateien arbeiten, die 100 KB oder größer sind.

 

Wie in der folgenden Beispielimplementierung von [**IPropertyStore::Commit**](/previous-versions/windows/desktop/legacy/bb761470(v=vs.85))veranschaulicht, wird der Handler für ManualSafeSave registriert, um die Option zum manuellen sicheren Speichern zu veranschaulichen. Die **\_ SaveCacheToDom-Methode** schreibt die im In-Memory-Cache gespeicherten Eigenschaftswerte in das XMLdocument-Objekt.


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



Fragen Sie als Nächstes, ob die angegebene [**IDestinationStreamFactory unterstützt.**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-idestinationstreamfactory)


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



Führen Sie als Nächstes einen Commit für den ursprünglichen Stream aus, der die Daten auf sichere Weise in die ursprüngliche Datei zurück schreibt.


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



Überprüfen Sie dann die **\_ SaveCacheToDom-Implementierung.**


```
// Saves the values in the internal cache back to the internal DOM object.
HRESULT CRecipePropertyStore::_SaveCacheToDom()
{
    // Iterate over each property in the internal value cache.
    DWORD cProps;  
```



Als Nächstes erhalten Sie die Anzahl der Eigenschaften, die im In-Memory-Cache gespeichert sind.


```
HRESULT hr = _pCache->GetCount(&cProps);          
            
```



Iterieren Sie nun die Eigenschaften, um zu bestimmen, ob der Wert einer Eigenschaft seit dem Laden in den Arbeitsspeicher geändert wurde.


```
    for (UINT i = 0; SUCCEEDED(hr) && (i < cProps); ++i)
    {
        PROPERTYKEY key;
        hr = _pCache->GetAt(i, &key); 
```



Die [**IPropertyStoreCache::GetState-Methode**](/windows/win32/api/propsys/nf-propsys-ipropertystorecache-getstate) ruft den Zustand der Eigenschaft im Cache ab. Das PSC \_ DIRTY-Flag, das in der [**IPropertyStore::SetValue-Implementierung**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85)) festgelegt wurde, markiert eine Eigenschaft als geändert.


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



Ordnen Sie die -Eigenschaft dem XML-Knoten zu, wie im **\_ rgPropertyMap-Array** angegeben.


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



Wenn sich eine Eigenschaft nicht in der Zuordnung befindet, handelt es sich um eine neue Eigenschaft, die vom Windows wurde. Da geöffnete Metadaten unterstützt werden, speichern Sie die neue Eigenschaft im **Xml-Abschnitt ExtendedProperties.**


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



## <a name="implementing-ipropertystorecapabilities"></a>Implementieren von IPropertyStoreCapabilities

[**IPropertyStoreCapabilities**](/windows/win32/api/propsys/nn-propsys-ipropertystorecapabilities) informiert die Shell-Benutzeroberfläche darüber, ob eine bestimmte Eigenschaft auf der Shell-Benutzeroberfläche bearbeitet werden kann. Beachten Sie, dass sich dies nur auf die Möglichkeit bezieht, die Eigenschaft auf der Benutzeroberfläche zu bearbeiten, und nicht, ob Sie [**IPropertyStore::SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85)) für die Eigenschaft erfolgreich aufrufen können. Eine Eigenschaft, die den Rückgabewert S \_ FALSE aus [**IPropertyStoreCapabilities::IsPropertyWritable zurückgibt,**](/windows/win32/api/propsys/nf-propsys-ipropertystorecapabilities-ispropertywritable) kann möglicherweise weiterhin über eine Anwendung festgelegt werden.


```
interface IPropertyStoreCapabilities : IUnknown
{
    HRESULT IsPropertyWritable([in] REFPROPERTYKEY key);
}
```



[**IsPropertyWritable**](/windows/win32/api/propsys/nf-propsys-ipropertystorecapabilities-ispropertywritable) gibt **S \_ OK** zurück, um anzugeben, dass Endbenutzer die Eigenschaft direkt bearbeiten dürfen sollen. S \_ FALSE gibt an, dass dies nicht dere sein sollte. S \_ FALSE kann bedeuten, dass Anwendungen für das Schreiben der Eigenschaft verantwortlich sind, nicht für Benutzer. Die Shell deaktiviert die Bearbeitung von Steuerelementen je nach Bedarf basierend auf den Ergebnissen von Aufrufen dieser Methode. Es wird davon ausgegangen, dass ein Handler, der [**IPropertyStoreCapabilities**](/windows/win32/api/propsys/nn-propsys-ipropertystorecapabilities) nicht implementiert, offene Metadaten durch Unterstützung für das Schreiben von Eigenschaften unterstützt.

Wenn Sie einen Handler erstellen, der nur schreibgeschützte Eigenschaften behandelt, sollten Sie die **Initialize-Methode** ([**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream), [**IInitializeWithItem**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem)oder [**IInitializeWithFile**](/windows/win32/api/propsys/nn-propsys-iinitializewithfile)) implementieren, damit sie STG \_ E \_ ACCESSDENIED zurückgibt, wenn sie mit dem STGM \_ READWRITE-Flag aufgerufen wird.

Für einige Eigenschaften ist das [isInnate-Attribut](./propdesc-schema-typeinfo.md) auf **TRUE** festgelegt. Innate-Eigenschaften weisen die folgenden Merkmale auf:

-   Die -Eigenschaft wird in der Regel auf irgendeine Weise berechnet. Beispielsweise `System.Image.BitDepth` wird anhand des Bilds selbst berechnet.
-   Das Ändern der -Eigenschaft wäre nicht sinnvoll, ohne die Datei zu ändern. Wenn Sie z. B. `System.Image.Dimensions` ändern, wird die Größe des Bilds nicht geändert, sodass es nicht sinnvoll ist, es dem Benutzer zu erlauben, es zu ändern.
-   In einigen Fällen werden diese Eigenschaften automatisch vom System bereitgestellt. Beispiele hierfür sind `System.DateModified` , die vom Dateisystem bereitgestellt werden, und , die auf dem Benutzer `System.SharedWith` basieren, für den die Datei freigegeben wird.

Aufgrund dieser Merkmale werden Eigenschaften, die als *IsInnate* gekennzeichnet sind, dem Benutzer auf der Shell-Benutzeroberfläche nur als schreibgeschützte Eigenschaften bereitgestellt. Wenn eine Eigenschaft als *IsInnate* markiert ist, speichert das Eigenschaftensystem diese Eigenschaft nicht im Eigenschaftenhandler. Daher benötigen Eigenschaftenhandler keinen speziellen Code, um diese Eigenschaften in ihren Implementierungen zu berücksichtigen. Wenn der Wert des *IsInnate-Attributs* nicht explizit für eine bestimmte Eigenschaft angegeben wird, ist der Standardwert **false.**

## <a name="registering-and-distributing-property-handlers"></a>Registrieren und Verteilen von Eigenschaftenhandlern

Wenn der Eigenschaftenhandler implementiert ist, muss er registriert und seine Dateierweiterung dem Handler zugeordnet werden. Weitere Informationen finden Sie unter [Registrieren und Verteilen von Eigenschaftenhandlern.](./prophand-reg-dist.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Grundlegendes zu Eigenschaftenhandlern](./building-property-handlers-properties.md)
</dt> <dt>

[Verwenden von Kind-Namen](./building-property-handlers-user-friendly-kind-names.md)
</dt> <dt>

[Verwenden von Eigenschaftenlisten](./building-property-handlers-property-lists.md)
</dt> <dt>

[Registrieren und Verteilen von Eigenschaftenhandlern](./prophand-reg-dist.md)
</dt> <dt>

[Bewährte Methoden und häufig gestellte Fragen zu Eigenschaftenhandlern](./prophand-bestprac-faq.yml)
</dt> </dl>

 

 
