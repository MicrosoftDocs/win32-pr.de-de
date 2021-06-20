---
description: In diesem Artikel wird erläutert, wie Eigenschaftenhandler für die Arbeit mit dem Windows-Eigenschaftensystem initialisiert werden.
ms.assetid: 3b54dd65-b7db-4e6a-bc3d-1008fdabcfa9
title: Initialisieren von Eigenschaftenhandlern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7d7626f92b3d81a6764e635c10302747f82a383
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406993"
---
# <a name="initializing-property-handlers"></a>Initialisieren von Eigenschaftenhandlern

In diesem Thema wird erläutert, wie Eigenschaftenhandler für die Arbeit mit dem Windows-Eigenschaftensystem erstellt und registriert werden.

Dieses Thema ist wie folgt organisiert:

-   [Eigenschaftenhandler](#property-handlers)
-   [Vorbereitungen](#before-you-begin)
-   [Initialisieren von Eigenschaftenhandlern](#initializing-property-handlers)
-   [In-Memory-Property Store](#in-memory-property-store)
-   [Umgang mit PROPVARIANT-Based Werten](#dealing-with-propvariant-based-values)
-   [Unterstützen von offenen Metadaten](#supporting-open-metadata)
-   [Volltextinhalt](#full-text-contents)
-   [Bereitstellen von Werten für Eigenschaften](#providing-values-for-properties)
-   [Zurückschreiben von Werten](#writing-back-values)
-   [Implementieren von IPropertyStoreCapabilities](#implementing-ipropertystorecapabilities)
-   [Registrieren und Verteilen von Eigenschaftenhandlern](#registering-and-distributing-property-handlers)
-   [Verwandte Themen](#related-topics)

## <a name="property-handlers"></a>Eigenschaftenhandler

Eigenschaftenhandler sind ein wichtiger Bestandteil des Eigenschaftensystems. Sie werden vom Indexer prozessin process aufgerufen, um Eigenschaftswerte zu lesen und zu indizieren, und sie werden auch von Windows-Explorer in-process aufgerufen, um Eigenschaftswerte direkt in den Dateien zu lesen und zu schreiben. Diese Handler müssen sorgfältig geschrieben und getestet werden, um eine Verschlechterung der Leistung oder den Verlust von Daten in den betroffenen Dateien zu verhindern. Weitere Informationen zu indexerspezifischen Überlegungen, die sich auf die Implementierung von Eigenschaftenhandlern auswirken, finden Sie unter [Developing Property Handlers for Windows Search](../search/-search-3x-wds-extidx-propertyhandlers.md).

In diesem Thema wird ein XML-basiertes Beispieldateiformat erläutert, das ein Rezept mit der Dateierweiterung .recipe beschreibt. Die .recipe-Dateinamenerweiterung wird als eigenes eindeutiges Dateiformat registriert, anstatt sich auf das generischere .xml-Dateiformat zu verlassen, dessen Handler einen sekundären Stream zum Speichern von Eigenschaften verwendet. Es wird empfohlen, eindeutige Dateierweiterungen für Ihre Dateitypen zu registrieren.

## <a name="before-you-begin"></a>Vorbereitungen

Eigenschaftshandler sind COM-Objekte, die die [**IPropertyStore-Abstraktion**](/windows/win32/api/propsys/nn-propsys-ipropertystore) für ein bestimmtes Dateiformat erstellen. Sie lesen (analysieren) und schreiben dieses Dateiformat in einer Weise, die der Spezifikation entspricht. Einige Eigenschaftenhandler arbeiten basierend auf APIs, die den Zugriff auf ein bestimmtes Dateiformat abstrahieren. Bevor Sie einen Eigenschaftenhandler für das Dateiformat entwickeln, müssen Sie verstehen, wie das Dateiformat Eigenschaften speichert und wie diese Eigenschaften (Namen und Werte) der Eigenschaftenspeicherabstraktion zugeordnet werden.

Denken Sie bei der Planung Ihrer Implementierung daran, dass Eigenschaftenhandler Komponenten auf niedriger Ebene sind, die im Kontext von Prozessen wie Windows-Explorer, dem Windows Search-Indexer und Anwendungen von Drittanbietern geladen werden, die das Shell-Elementprogrammiermodell verwenden. Daher können Eigenschaftshandler nicht in verwaltetem Code implementiert werden und sollten in C++ implementiert werden. Wenn Ihr Handler APIs oder Dienste verwendet, um seine Arbeit zu erfüllen, müssen Sie sicherstellen, dass diese Dienste in den Umgebung(en) ordnungsgemäß funktionieren, in die der Eigenschaftenhandler geladen wird.

> [!Note]  
> Eigenschaftenhandler sind immer bestimmten Dateitypen zugeordnet. Wenn Ihr Dateiformat Eigenschaften enthält, die einen benutzerdefinierten Eigenschaftenhandler erfordern, sollten Sie daher immer eine eindeutige Dateierweiterung für jedes Dateiformat registrieren.

 

## <a name="initializing-property-handlers"></a>Initialisieren von Eigenschaftenhandlern

Bevor eine Eigenschaft vom System verwendet wird, wird sie durch Aufrufen einer Implementierung von [**IInitializeWithStream initialisiert.**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream) Der Eigenschaftenhandler sollte initialisiert werden, indem das System ihm einen Stream zulässt, anstatt diese Zuweisung der Handlerimplementierung zu belässt. Diese Initialisierungsmethode stellt Folgendes sicher:

-   Der Eigenschaftenhandler kann in einem eingeschränkten Prozess (ein wichtiges Sicherheitsfeature) ausgeführt werden, ohne über Zugriffsrechte zum direkten Lesen oder Schreiben von Dateien zu verfügen, anstatt über den Stream auf ihre Inhalte zu zugreifen.
-   Das System kann als vertrauenswürdig eingestuft werden, um die Dateioplocks ordnungsgemäß zu verarbeiten. Dies ist eine wichtige Zuverlässigkeitsmaßnahme.
-   Das Eigenschaftensystem bietet einen automatisch sicheren Speicherungsdienst ohne zusätzliche Funktionalität, die für die Implementierung des Eigenschaftenhandlers erforderlich ist. Weitere Informationen [zu Streams finden Sie](#writing-back-values) im Abschnitt Zurückschreiben von Werten.
-   Die Verwendung von [**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream) abstrahiert Ihre Implementierung aus Dateisystemdetails. Dadurch kann der Handler die Initialisierung über alternative Speicher unterstützen, z. B. einen File Transfer Protocol-Ordner (FTP) oder eine komprimierte Datei mit .zip Dateinamenerweiterung.

Es gibt Fälle, in denen die Initialisierung mit Streams nicht möglich ist. In diesen Situationen gibt es zwei weitere Schnittstellen, die Eigenschaftenhandler implementieren können: [**IInitializeWithFile**](/windows/win32/api/propsys/nn-propsys-iinitializewithfile) und [**IInitializeWithItem**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem). Wenn ein Eigenschaftenhandler den [**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream)nicht implementiert, muss er die Ausführung in dem isolierten Prozess deaktivieren, in den der Systemindexer ihn standardmäßig platzieren würde, wenn eine Änderung am Stream erfolgt. Legen Sie den folgenden Registrierungswert fest, um dieses Feature zu deaktivieren.

```
HKEY_CLASSES_ROOT
   CLSID
      {66742402-F9B9-11D1-A202-0000F81FEDEE}
         DisableProcessIsolation = 1
```

Es ist jedoch viel besser, [**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream) zu implementieren und eine streambasierte Initialisierung zu verwenden. Ihr Eigenschaftenhandler ist dadurch sicherer und zuverlässiger. Das Deaktivieren der Prozessisolation ist in der Regel nur für Legacyeigenschaftshandler vorgesehen und sollte durch neuen Code aufs Härten vermieden werden.

Um die Implementierung eines Eigenschaftenhandlers im Detail zu untersuchen, sehen Sie sich das folgende Codebeispiel an, bei dem es sich um eine Implementierung von [**IInitializeWithStream::Initialize handelt.**](/windows/win32/api/propsys/nf-propsys-iinitializewithstream-initialize) Der Handler wird initialisiert, indem ein XML-basiertes Rezeptdokument über einen Zeiger auf die zugeordnete [**IStream-Instanz**](/windows/win32/api/objidl/nn-objidl-istream) dieses Dokuments geladen wird. Die **\_ variable spDocEle,** die am Ende des Codebeispiels verwendet wird, wird weiter oben im Beispiel als MSXML2::IXMLDOMElementPtr definiert.

> [!Note]  
> Die folgenden und alle nachfolgenden Codebeispiele sind aus dem Beispiel für den Rezepthandler im Windows Software Development Kit (SDK) entnommen. .

 


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

Nachdem das Dokument selbst geladen wurde, werden die eigenschaften, die in Windows-Explorer angezeigt werden sollen, durch Aufrufen der geschützten **\_ LoadProperties-Methode** geladen, wie im folgenden Codebeispiel veranschaulicht. Dieser Prozess wird im nächsten Abschnitt ausführlich untersucht.


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



Wenn der Stream schreibgeschützt ist, der *grfMode-Parameter* jedoch das STGM READWRITE-Flag enthält, sollte die Initialisierung fehlschlagen und \_ STG \_ E \_ ACCESSDENIED zurückgeben. Ohne diese Überprüfung Windows-Explorer die Eigenschaftswerte als beschreibbar, obwohl sie nicht beschreibbar sind, was zu einer verwirrenden Endbenutzererfahrung führt.

Der Eigenschaftenhandler wird nur einmal in seiner Lebensdauer initialisiert. Wenn eine zweite Initialisierung angefordert wird, sollte der Handler `HRESULT_FROM_WIN32(ERROR_ALREADY_INITIALIZED)` zurückgeben.

## <a name="in-memory-property-store"></a>In-Memory Property Store

Bevor Sie sich die Implementierung von **\_ LoadProperties** ansehen, sollten Sie das **PropertyMap-Array** kennen, das im Beispiel zum Zuordnen von Eigenschaften im XML-Dokument zu vorhandenen Eigenschaften im Eigenschaftensystem über ihre PKEY-Werte verwendet wird.

Sie sollten nicht jedes Element und Attribut in der XML-Datei als Eigenschaft verfügbar machen. Wählen Sie stattdessen nur diejenigen aus, von denen Sie glauben, dass sie für Endbenutzer in der Organisation ihrer Dokumente nützlich sein werden (in diesem Fall Rezepte). Dies ist ein wichtiges Konzept, das Sie bei der Entwicklung Ihrer Eigenschaftenhandler beachten sollten: den Unterschied zwischen Informationen, die für Organisationsszenarien wirklich nützlich sind, und Informationen, die zu den Details Ihrer Datei gehören und durch Öffnen der Datei selbst gesehen werden können. Eigenschaften sind nicht als vollständige Duplizierung einer XML-Datei vorgesehen.


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



Hier ist die vollständige Implementierung der **\_ LoadProperties-Methode,** die von [**IInitializeWithStream::Initialize aufgerufen wird.**](/windows/win32/api/propsys/nf-propsys-iinitializewithstream-initialize)


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



Die **\_ LoadProperties-Methode** ruft die Shell-Hilfsfunktion [**PSCreateMemoryPropertyStore**](/windows/win32/api/propsys/nf-propsys-pscreatememorypropertystore) auf, um einen In-Memory-Eigenschaftenspeicher (Cache) für die behandelten Eigenschaften zu erstellen. Mithilfe eines Caches werden Änderungen für Sie nachverfolgt. Dadurch können Sie nicht nachverfolgen, ob ein Eigenschaftswert im Cache geändert, aber noch nicht im persistenten Speicher gespeichert wurde. Außerdem können Sie keine Eigenschaftswerte unnötig beibehalten, die sich nicht geändert haben.

Die **\_ LoadProperties-Methode** ruft auch **\_ LoadProperty** auf, dessen Implementierung im folgenden Code veranschaulicht wird) einmal für jede zugeordnete Eigenschaft. **\_ LoadProperty** ruft den Wert der -Eigenschaft ab, wie im **PropertyMap-Element** im XML-Stream angegeben, und weist ihn dem In-Memory-Cache durch einen Aufruf von [**IPropertyStoreCache::SetValueAndState**](/windows/win32/api/propsys/nf-propsys-ipropertystorecache-setvalueandstate)zu. Das PSC NORMAL-Flag im Aufruf von \_ **IPropertyStoreCache::SetValueAndState** gibt an, dass der Eigenschaftswert seit dem Zeitpunkt, zu dem er in den Cache eingegeben wurde, nicht geändert wurde.


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

In der Implementierung von **\_ LoadProperty** wird ein Eigenschaftswert in Form einer [**PROPVARIANT bereitgestellt.**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) Ein Satz von APIs im Software Development Kit (SDK) wird bereitgestellt, um primitive Typen wie **PWSTR** oder **int** in oder aus **PROPVARIANT-Typen zu** konvertieren. Diese APIs befinden sich in Propvarutil.h.

Um z. B. eine [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) in eine Zeichenfolge zu konvertieren, können Sie [**PropVariantToString**](/windows/win32/api/propvarutil/nf-propvarutil-propvarianttostring) wie hier dargestellt verwenden.


```
PropVariantToString(REFPROPVARIANT propvar, PWSTR psz, UINT cch);
```



Zum Initialisieren einer PROPVARIANT aus einer Zeichenfolge können Sie [**InitPropVariantFromString verwenden.**](/windows/win32/api/propvarutil/nf-propvarutil-initpropvariantfromstring)


```
InitPropVariantFromString(PCWSTR psz, PROPVARIANT *ppropvar);
```



Wie Sie in jeder der im Beispiel enthaltenen Rezeptdateien sehen können, kann jede Datei mehr als ein Schlüsselwort enthalten. Um dies zu berücksichtigen, unterstützt das Eigenschaftensystem mehrwertige Zeichenfolgen, die als Vektor von Zeichenfolgen dargestellt werden (z.B. "VT \_ VECTOR \| VT \_ LPWSTR"). Die **\_ LoadVectorProperty-Methode** im Beispiel verwendet vektorbasierte Werte.


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



Wenn in der Datei kein Wert vorhanden ist, geben Sie keinen Fehler zurück. Legen Sie stattdessen den Wert auf VT \_ EMPTY fest, und geben Sie **S \_ OK zurück.** VT \_ EMPTY gibt an, dass der Eigenschaftswert nicht vorhanden ist.

## <a name="supporting-open-metadata"></a>Unterstützen von offenen Metadaten

In diesem Beispiel wird ein XML-basiertes Dateiformat verwendet. Das Schema kann erweitert werden, um z. B. Eigenschaften zu unterstützen, die während der Entwicklung nicht verwendet wurden. Dieses System wird als offene Metadaten bezeichnet. In diesem Beispiel wird das Eigenschaftensystem erweitert, indem unter dem **Recipe-Element** **namens ExtendedProperties** ein Knoten erstellt wird, wie im folgenden Codebeispiel veranschaulicht.


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



Serialisierungs-APIs, die in Propsys.h deklariert sind, werden verwendet, um [**PROPVARIANT-Typen**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) in Datenblobs zu serialisieren und zu deserialisieren. Anschließend wird die Base64-Codierung verwendet, um diese Blobs in Zeichenfolgen zu serialisieren, die im XML-Code gespeichert werden können. Diese Zeichenfolgen werden im **EncodedValue-Attribut** des **ExtendedProperties-Elements** gespeichert. Die folgende Hilfsprogrammmethode, die in der Datei Util.cpp des Beispiels implementiert ist, führt die Serialisierung aus. Sie beginnt mit einem Aufruf der [**StgSerializePropVariant-Funktion,**](/windows/win32/api/propvarutil/nf-propvarutil-stgserializepropvariant) um die binäre Serialisierung durchzuführen, wie im folgenden Codebeispiel veranschaulicht.


```
HRESULT SerializePropVariantAsString(const PROPVARIANT *ppropvar, PWSTR *pszOut)
{
    SERIALIZEDPROPERTYVALUE *pBlob;
    ULONG cbBlob;
    HRESULT hr = StgSerializePropVariant(ppropvar, &pBlob, &cbBlob);
```



Als Nächstes führt die in Wincrypt.h deklarierte [**CryptBinaryToString-Funktion**](/windows/win32/api/wincrypt/nf-wincrypt-cryptbinarytostringa)die Base64-Konvertierung aus.


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



Die **DeserializePropVariantFromString-Funktion,** die auch in Util.cpp enthalten ist, kehrt den Vorgang um und deserialisiert Werte aus der XML-Datei.

Informationen zur Unterstützung für geöffnete Metadaten finden Sie unter "Dateitypen, die geöffnete Metadaten unterstützen" in [Dateitypen.](../shell/fa-file-types.md)

## <a name="full-text-contents"></a>Full-Text Inhalt

Eigenschaftenhandler können auch eine Volltextsuche der Dateiinhalte ermöglichen. Sie sind eine einfache Möglichkeit, diese Funktionalität bereitzustellen, wenn das Dateiformat nicht übermäßig kompliziert ist. Es gibt eine alternative, leistungsfähigere Möglichkeit, den vollständigen Text der Datei über die Implementierung der [**IFilter-Schnittstelle**](/windows/win32/api/filter/nn-filter-ifilter) bereitzustellen.

In der folgenden Tabelle werden die Vorteile der einzelnen Ansätze mithilfe von [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) oder [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)zusammengefasst.



| Funktion                                   | Ifilter                      | Ipropertystore |
|----------------------------------------------|------------------------------|----------------|
| Lässt das Zurückschreiben in Dateien zu?                  | Nein                           | Ja            |
| Bietet eine Mischung aus Inhalt und Eigenschaften?      | Ja                          | Ja            |
| Mehrsprachige?                                | Ja                          | Nein             |
| MIME/Embedded?                               | Ja                          | Nein             |
| Textgrenzen?                             | Satz, Absatz, Kapitel | Keine           |
| Implementierung für SPS/SQL Server unterstützt? | Ja                          | Nein             |
| Implementierung                               | Komplex                      | Einfach         |



 

Im Beispiel für den Rezepthandler weist das Format der Rezeptdatei keine komplexen Anforderungen auf, sodass nur [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) für die Volltextunterstützung implementiert wurde. Die Volltextsuche wird für die XML-Knoten implementiert, die im folgenden Array benannt sind.


```
const PWSTR c_rgszContentXPath[] = {
    L"Recipe/Ingredients/Item",
    L"Recipe/Directions/Step",
    L"Recipe/RecipeInfo/Yield",
    L"Recipe/RecipeKeywords/Keyword",
};
```



Das Eigenschaftensystem enthält die `System.Search.Contents` Eigenschaft (PKEY \_ Search \_ Contents), die erstellt wurde, um dem Indexer Volltextinhalt bereitzustellen. Der Wert dieser Eigenschaft wird nie direkt auf der Benutzeroberfläche angezeigt. Der Text aus allen XML-Knoten, die im obigen Array benannt sind, wird zu einer einzelnen Zeichenfolge verkettet. Diese Zeichenfolge wird dann dem Indexer als Volltextinhalt der Rezeptdatei durch einen Aufruf von [**IPropertyStoreCache::SetValueAndState**](/windows/win32/api/propsys/nf-propsys-ipropertystorecache-setvalueandstate) bereitgestellt, wie im folgenden Codebeispiel veranschaulicht.


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

Beim Lesen von Werten werden Eigenschaftenhandler in der Regel aus einem der folgenden Gründe aufgerufen:

-   Zum Aufzählen aller Eigenschaftswerte.
-   So erhalten Sie den Wert einer bestimmten Eigenschaft.

Zur Enumeration wird ein Eigenschaftenhandler aufgefordert, seine Eigenschaften entweder während der Indizierung aufzuzählen oder wenn das Eigenschaftendialogfeld nach Eigenschaften fragt, die in der Gruppe **Andere** angezeigt werden sollen. Die Indizierung wird ständig als Hintergrundvorgang durchgeführt. Wenn sich eine Datei ändert, wird der Indexer benachrichtigt und indiziert die Datei neu, indem der Eigenschaftenhandler aufgefordert wird, seine Eigenschaften aufzuzählen. Daher ist es wichtig, dass Eigenschaftenhandler effizient implementiert werden und Eigenschaftswerte so schnell wie möglich zurückgeben. Aufzählen Sie alle Eigenschaften, für die Sie Werte haben, genau wie für jede Auflistung, aber zählen Sie keine Eigenschaften auf, die speicherintensive Berechnungen oder Netzwerkanforderungen umfassen, die deren Abruf verlangsamen könnten.

Beim Schreiben eines Eigenschaftenhandlers müssen Sie in der Regel die folgenden beiden Sätze von Eigenschaften berücksichtigen.

-   Primäre Eigenschaften: Eigenschaften, die ihr Dateityp nativ unterstützt. Beispielsweise unterstützt ein Fotoeigenschaftenhandler für EXIF-Metadaten (Exchangeable Image File) nativ `System.Photo.FNumber` .
-   Erweiterte Eigenschaften: Eigenschaften, die ihr Dateityp als Teil geöffneter Metadaten unterstützt.

Da im Beispiel der In-Memory-Cache verwendet wird, ist die Implementierung von [**IPropertyStore-Methoden**](/windows/win32/api/propsys/nn-propsys-ipropertystore) nur eine Frage der Delegierung an diesen Cache, wie im folgenden Codebeispiel veranschaulicht.


```
IFACEMETHODIMP GetCount(__out DWORD *pcProps)
{ return _spCache->GetCount(pcProps); }

IFACEMETHODIMP GetAt(DWORD iProp, __out PROPERTYKEY *pkey)
{ return _spCache->GetAt(iProp, pkey); }

IFACEMETHODIMP GetValue(REFPROPERTYKEY key, __out PROPVARIANT *pPropVar)
{ return _spCache->GetValue(key, pPropVar); }
```



Wenn Sie nicht an den In-Memory-Cache delegieren möchten, müssen Sie Ihre Methoden implementieren, um> das folgende erwartete Verhalten bereitzustellen:

-   [**IPropertyStore::GetCount:**](/previous-versions/windows/desktop/legacy/bb761472(v=vs.85))Wenn keine Eigenschaften vorhanden sind, gibt diese Methode **S \_ OK** zurück.
-   [**IPropertyStore::GetAt:**](/previous-versions/windows/desktop/legacy/bb761471(v=vs.85))Wenn *iProp* größer oder gleich *cProps* ist, gibt diese Methode E \_ INVALIDARG zurück, und die Struktur, auf die der *pkey-Parameter zeigt,* wird mit Nullen gefüllt.
-   [**IPropertyStore::GetCount**](/previous-versions/windows/desktop/legacy/bb761472(v=vs.85)) und [**IPropertyStore::GetAt**](/previous-versions/windows/desktop/legacy/bb761471(v=vs.85)) spiegeln den aktuellen Zustand des Eigenschaftenhandlers wider. Wenn ein [**PROPERTYKEY**](/windows/win32/api/wtypes/ns-wtypes-propertykey) der Datei über [**IPropertyStore::SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85))hinzugefügt oder daraus entfernt wird, müssen diese beiden Methoden diese Änderung beim nächsten Aufruf widerspiegeln.
-   [**IPropertyStore::GetValue:**](/previous-versions/windows/desktop/legacy/bb761473(v=vs.85))Wenn diese Methode nach einem Wert gefragt wird, der nicht vorhanden ist, wird **S \_ OK** zurückgegeben, wobei der Wert als VT EMPTY gemeldet \_ wird.

## <a name="writing-back-values"></a>Zurückschreiben von Werten

Wenn der Eigenschaftenhandler den Wert einer Eigenschaft mithilfe von [**IPropertyStore::SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85))schreibt, wird der Wert erst in die Datei geschrieben, wenn [**IPropertyStore::Commit**](/previous-versions/windows/desktop/legacy/bb761470(v=vs.85)) aufgerufen wird. Der In-Memory-Cache kann bei der Implementierung dieses Schemas nützlich sein. Im Beispielcode legt die **IPropertyStore::SetValue-Implementierung** einfach den neuen Wert im In-Memory-Cache und den Zustand dieser Eigenschaft auf PSC \_ DIRTY fest.


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



In jeder [**IPropertyStore-Implementierung**](/windows/win32/api/propsys/nn-propsys-ipropertystore) wird das folgende Verhalten von [**IPropertyStore::SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85))erwartet:

-   Wenn die Eigenschaft bereits vorhanden ist, wird der Wert der Eigenschaft festgelegt.
-   Wenn die Eigenschaft nicht vorhanden ist, wird die neue Eigenschaft hinzugefügt und ihr Wert festgelegt.
-   Wenn der Eigenschaftswert nicht mit der angegebenen Genauigkeit beibehalten werden kann (z. B. Abschneiden aufgrund von Größenbeschränkungen im Dateiformat), wird der Wert so weit wie möglich festgelegt, und INPLACE \_ S \_ TRUNCATED wird zurückgegeben.
-   Wenn die Eigenschaft vom Eigenschaftenhandler nicht unterstützt wird, `HRESULT_FROM_WIN32(ERROR_NOT_SUPPORTED)` wird zurückgegeben.
-   Wenn es einen anderen Grund gibt, warum der Eigenschaftswert nicht festgelegt werden kann, z. B. wenn die Datei gesperrt ist oder keine Bearbeitungsrechte über Zugriffssteuerungslisten (ACLs) vorhanden sind, wird STG \_ E \_ ACCESSDENIED zurückgegeben.

Ein wichtiger Vorteil der Verwendung von Streams als Beispiel ist die Zuverlässigkeit. Eigenschaftenhandler müssen immer berücksichtigen, dass sie eine Datei im Falle eines schwerwiegenden Fehlers nicht in einem inkonsistenten Zustand belassen können. Eine Beschädigung der Dateien eines Benutzers sollte natürlich vermieden werden, und die beste Möglichkeit hierfür ist ein Mechanismus zum Kopieren beim Schreiben. Wenn Ihr Eigenschaftenhandler einen Stream für den Zugriff auf eine Datei verwendet, erhalten Sie dieses Verhalten automatisch. Das System schreibt alle Änderungen in den Stream, wobei die Datei nur während des Commitvorgangs durch die neue Kopie ersetzt wird.

Um dieses Verhalten zu überschreiben und den Dateispeichervorgang manuell zu steuern, können Sie das sichere Speicherverhalten deaktivieren, indem Sie den Wert ManualSafeSave im Registrierungseintrag Ihres Handlers festlegen, wie hier gezeigt.

```
HKEY_CLASSES_ROOT
   CLSID
      {66742402-F9B9-11D1-A202-0000F81FEDEE}
         ManualSafeSave = 1
```

Wenn ein Handler den ManualSafeSave-Wert angibt, ist der Stream, mit dem er initialisiert wird, kein transaktiver Stream (STGM \_ TRANSACTED). Der Handler selbst muss die sichere Speicherfunktion implementieren, um sicherzustellen, dass die Datei nicht beschädigt ist, wenn der Speichervorgang unterbrochen wird. Wenn der Handler das schreibende Schreiben implementiert, wird er in den angegebenen Stream geschrieben. Wenn der Handler dieses Feature nicht unterstützt, muss er einen Stream abrufen, mit dem die aktualisierte Kopie der Datei mithilfe von [**IDestinationStreamFactory::GetDestinationStream**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-idestinationstreamfactory-getdestinationstream)geschrieben werden soll. Nachdem der Handler mit dem Schreiben fertig ist, sollte er [**IPropertyStore::Commit**](/previous-versions/windows/desktop/legacy/bb761470(v=vs.85)) für den ursprünglichen Stream aufrufen, um den Vorgang abzuschließen, und den Inhalt des ursprünglichen Streams durch die neue Kopie der Datei ersetzen.

ManualSafeSave ist auch die Standardsituation, wenn Sie Ihren Handler nicht mit einem Stream initialisieren. Ohne einen ursprünglichen Stream, um den Inhalt des temporären Streams zu empfangen, müssen Sie [**ReplaceFile**](/windows/win32/api/winbase/nf-winbase-replacefilea) verwenden, um eine atomare Ersetzung der Quelldatei durchzuführen.

Große Dateiformate, die auf eine Weise verwendet werden, die Dateien größer als 1 MB erzeugt, sollten Unterstützung für das Schreiben von in-place-Eigenschaften implementieren. Andernfalls entspricht das Leistungsverhalten nicht den Erwartungen der Clients des Eigenschaftensystems. In diesem Szenario sollte die Zeit, die zum Schreiben von Eigenschaften erforderlich ist, nicht von der Dateigröße beeinflusst werden.

Für sehr große Dateien, z. B. eine Videodatei von 1 GB oder mehr, ist eine andere Lösung erforderlich. Wenn in der Datei nicht genügend Speicherplatz vorhanden ist, um das schreiben zu können, schlägt der Handler möglicherweise bei der Eigenschaftenaktualisierung fehl, wenn der für das Schreiben von in der -Eigenschaft reservierte Speicherplatz erschöpft ist. Dieser Fehler tritt auf, um eine schlechte Leistung aufgrund von 2 GB E/A (1 zu lesen, 1 zum Schreiben) zu vermeiden. Aufgrund dieses potenziellen Fehlers sollten diese Dateiformate genügend Speicherplatz für das schreiben von Eigenschaften reservieren.

Wenn die Datei über genügend Speicherplatz im Header zum Schreiben von Metadaten verfügt und das Schreiben dieser Metadaten nicht dazu führt, dass die Datei vergrößert oder verkleinert wird, ist es möglicherweise sicher, dass sie an Ort und Stelle geschrieben wird. Wir empfehlen 64 KB als Ausgangspunkt. Das Schreiben von "in-place" entspricht dem Handler, der nach ManualSafeSave fragt und [**IStream::Commit**](/windows/win32/api/objidl/nf-objidl-istream-commit) in der Implementierung von [**IPropertyStore::Commit**](/previous-versions/windows/desktop/legacy/bb761470(v=vs.85))aufruft, und weist eine viel bessere Leistung als copy-on-write auf. Wenn sich die Dateigröße aufgrund von Änderung des Eigenschaftswerts ändert, sollte nicht versucht werden, eine dateiveränderliche Datei zu schreiben, wenn eine nicht ordnungsgemäß beendet wird.

> [!Note]  
> Aus Leistungsgründen wird empfohlen, die Option ManualSafeSave mit Eigenschaftenhandlern zu verwenden, die mit Dateien arbeiten, die 100 KB oder größer sind.

 

Wie in der folgenden Beispielimplementierung von [**IPropertyStore::Commit**](/previous-versions/windows/desktop/legacy/bb761470(v=vs.85))veranschaulicht, wird der Handler für ManualSafeSave registriert, um die Option zum manuellen sicheren Speichern zu veranschaulichen. Die **\_ SaveCacheToDom-Methode** schreibt die im Speichercache gespeicherten Eigenschaftswerte in das XMLdocument-Objekt.


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



Fragen Sie als Nächstes, ob die angegebene [**IDestinationStreamFactory**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-idestinationstreamfactory)unterstützt.


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



Committen Sie als Nächstes den ursprünglichen Stream, der die Daten auf sichere Weise zurück in die ursprüngliche Datei schreibt.


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



Untersuchen Sie dann die **\_ SaveCacheToDom-Implementierung.**


```
// Saves the values in the internal cache back to the internal DOM object.
HRESULT CRecipePropertyStore::_SaveCacheToDom()
{
    // Iterate over each property in the internal value cache.
    DWORD cProps;  
```



Als Nächstes erhalten Sie die Anzahl der eigenschaften, die im In-Memory-Cache gespeichert sind.


```
HRESULT hr = _pCache->GetCount(&cProps);          
            
```



Durchlaufen Sie nun die Eigenschaften, um zu bestimmen, ob der Wert einer Eigenschaft seit dem Laden in den Arbeitsspeicher geändert wurde.


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



Ordnen Sie die -Eigenschaft dem XML-Knoten zu, wie im **Array \_ rgPropertyMap** angegeben.


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



Wenn sich eine Eigenschaft nicht in der Zuordnung befindet, handelt es sich um eine neue Eigenschaft, die von Windows-Explorer festgelegt wurde. Da geöffnete Metadaten unterstützt werden, speichern Sie die neue Eigenschaft im Abschnitt **ExtendedProperties** des XML-Code.


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

[**IPropertyStoreCapabilities**](/windows/win32/api/propsys/nn-propsys-ipropertystorecapabilities) informiert die Shell-Benutzeroberfläche darüber, ob eine bestimmte Eigenschaft in der Shell-Benutzeroberfläche bearbeitet werden kann. Beachten Sie, dass sich dies nur auf die Möglichkeit bezieht, die Eigenschaft in der Benutzeroberfläche zu bearbeiten, und nicht darauf, ob [**Sie IPropertyStore::SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85)) erfolgreich für die Eigenschaft aufrufen können. Eine Eigenschaft, die den Rückgabewert S FALSE von \_ [**IPropertyStoreCapabilities::IsPropertyWritable**](/windows/win32/api/propsys/nf-propsys-ipropertystorecapabilities-ispropertywritable) zurückerrechnt, kann möglicherweise weiterhin über eine Anwendung festgelegt werden.


```
interface IPropertyStoreCapabilities : IUnknown
{
    HRESULT IsPropertyWritable([in] REFPROPERTYKEY key);
}
```



[**IsPropertyWritable gibt**](/windows/win32/api/propsys/nf-propsys-ipropertystorecapabilities-ispropertywritable) **S OK \_ zurück,** um anzugeben, dass Endbenutzer die Eigenschaft direkt bearbeiten dürfen. S \_ FALSE gibt an, dass dies nicht der Wert sein sollte. S FALSE kann bedeuten, dass Anwendungen für das Schreiben der Eigenschaft und nicht für \_ Benutzer verantwortlich sind. Die Shell deaktiviert die Bearbeitungssteuerelemente entsprechend den Ergebnissen der Aufrufe dieser Methode. Es wird davon ausgegangen, dass ein Handler, der [**IPropertyStoreCapabilities**](/windows/win32/api/propsys/nn-propsys-ipropertystorecapabilities) nicht implementiert, offene Metadaten durch Unterstützung für das Schreiben von Eigenschaften unterstützt.

Wenn Sie einen Handler erstellen, der nur schreibgeschützte Eigenschaften behandelt, sollten Sie die **Initialize-Methode** ([**IInitializeWithStream,**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream) [**IInitializeWithItem**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem)oder [**IInitializeWithFile**](/windows/win32/api/propsys/nn-propsys-iinitializewithfile)) implementieren, sodass stg E ACCESSDENIED zurückgegeben wird, wenn sie mit dem \_ \_ STGM READWRITE-Flag aufgerufen \_ wird.

Bei einigen Eigenschaften ist das [isInnate-Attribut](./propdesc-schema-typeinfo.md) auf **true festgelegt.** Innierte Eigenschaften haben die folgenden Merkmale:

-   Die -Eigenschaft wird in der Regel in irgendeiner Weise berechnet. Beispielsweise wird `System.Image.BitDepth` aus dem Bild selbst berechnet.
-   Das Ändern der -Eigenschaft wäre nicht sinnvoll, ohne die Datei zu ändern. Wenn Sie z. B. ändern, wird die Größe des Bilds nicht geändert, daher ist es nicht sinnvoll, dem Benutzer zu erlauben, `System.Image.Dimensions` es zu ändern.
-   In einigen Fällen werden diese Eigenschaften automatisch vom System bereitgestellt. Beispiele hierfür sind , das vom Dateisystem bereitgestellt wird, und , die darauf basieren, für wen der Benutzer `System.DateModified` `System.SharedWith` die Datei gemeinsam verwendet.

Aufgrund dieser Merkmale werden eigenschaften, die als *IsInnate* gekennzeichnet sind, dem Benutzer auf der Shell-Benutzeroberfläche nur als schreibgeschützte Eigenschaften bereitgestellt. Wenn eine Eigenschaft als *IsInnate markiert* ist, wird diese Eigenschaft vom Eigenschaftensystem nicht im Eigenschaftenhandler gespeichert. Daher benötigen Eigenschaftenhandler keinen speziellen Code, um diese Eigenschaften in ihren Implementierungen zu berücksichtigen. Wenn der Wert des *IsInnate-Attributs* nicht explizit für eine bestimmte Eigenschaft angegeben ist, ist der Standardwert **FALSE.**

## <a name="registering-and-distributing-property-handlers"></a>Registrieren und Verteilen von Eigenschaftenhandlern

Wenn der Eigenschaftenhandler implementiert ist, muss er registriert werden, und seine Dateierweiterung muss dem Handler zugeordnet sein. Weitere Informationen finden Sie unter [Registrieren und Verteilen von Eigenschaftenhandlern.](./prophand-reg-dist.md)

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

[Bewährte Methoden und häufig gestellte Fragen zu Eigenschaftenhandlern](./prophand-bestprac-faq.md)
</dt> </dl>

 

 
