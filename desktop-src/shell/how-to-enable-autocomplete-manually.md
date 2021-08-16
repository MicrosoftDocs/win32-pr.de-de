---
description: Um eine detailliertere Kontrolle über das AutoVervollständigen-Verhalten zu erhalten oder eine benutzerdefinierte Quelle von AutoVervollständigen-Zeichenfolgen hinzuzufügen, müssen Sie das AutoVervollständigen-Objekt selbst verwalten.
ms.assetid: E1A7B1B0-2879-452E-9EBB-73F02B932200
title: Manuelles Aktivieren der automatischen Vervollständigung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7df686e4c5a4a6e96b1faf82e4926dffc73398b360e3e6235d6a61451eae189
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117859707"
---
# <a name="how-to-enable-autocomplete-manually"></a>Manuelles Aktivieren der automatischen Vervollständigung

Um eine detailliertere Kontrolle über das AutoVervollständigen-Verhalten zu erhalten oder eine benutzerdefinierte Quelle von AutoVervollständigen-Zeichenfolgen hinzuzufügen, müssen Sie das AutoVervollständigen-Objekt selbst verwalten. Sie können die automatische Vervollständigung auf folgende Weise manuell aktivieren.

## <a name="instructions"></a>Anweisungen

### <a name="creating-a-simple-autocomplete-object"></a>Erstellen eines einfachen AutoVervollständigen-Objekts

Die folgenden Schritte zeigen, wie Sie ein einfaches AutoVervollständigen-Objekt erstellen und initialisieren. Ein einfaches AutoVervollständigen-Objekt schließt Zeichenfolgen aus einer einzelnen Quelle ab. Die Fehlerüberprüfung wurde in diesem Beispiel absichtlich ausgelassen.

1.  Erstellen Sie das AutoVervollständigen-Objekt.

    ```C++
    IAutoComplete *pac;

    HRESULT hr = CoCreateInstance(CLSID_AutoComplete, 
                                    NULL, 
                                  CLSCTX_INPROC_SERVER,
                                  IID_PPV_ARGS(&pac));
    ```

    

2.  Erstellen Sie die AutoVervollständigen-Quelle. Sie können eine [vordefinierte AutoVervollständigen-Quelle](ac-ovw.md) verwenden oder Eine eigene benutzerdefinierte Quelle schreiben.

    Im folgenden Code wird eine der vordefinierten AutoVervollständigen-Quellen verwendet.

    ```C++
    IUnknown *punkSource;

    hr = CoCreateInstance(CLSID_ACListISF, 
                          NULL, 
                          CLSCTX_INPROC_SERVER,
                          IID_PPV_ARGS(&punkSource));
    ```

    

    Im folgenden Code wird eine benutzerdefinierte AutoVervollständigen-Quelle verwendet. Sie können Ihre eigene AutoVervollständigen-Quelle schreiben, indem Sie ein Objekt implementieren, das die [**IEnumString-Schnittstelle**](/windows/win32/api/objidlbase/nn-objidlbase-ienumstring) verfügbar macht. Das -Objekt kann optional auch die [**Schnittstellen LIAList**](/windows/win32/api/shlobj_core/nn-shlobj_core-iaclist) und [**LIAList2**](/windows/win32/api/shlobj_core/nn-shlobj_core-iaclist2) implementieren.

    ```C++
    CCustomAutoCompleteSource *pcacs = new CCustomAutoCompleteSource();

    hr = pcacs->QueryInterface(IID_PPV_ARGS(&punkSource));
    if(SUCCEEDED(hr))
    {
        // ...
    }

    pcacs->Release();
    ```

    

3.  Legen Sie die Optionen für die AutoVervollständigen-Quelle fest (optional).

    Sie können das Verhalten der AutoVervollständigen-Quelle anpassen, indem Sie deren Optionen festlegen, wenn die Quelle die [**CSVList2-Schnittstelle**](/windows/win32/api/shlobj_core/nn-shlobj_core-iaclist2) verfügbar macht. Wenn Sie die vordefinierten AutoVervollständigen-Quellen verwenden, exportiert nur CLSID \_ ACListISF **LIAList2.** Eine vollständige Liste der Optionen und deren Werte finden Sie unter [**LIAList2::SetOptions**](/windows/win32/api/shlobj_core/nf-shlobj_core-iaclist2-setoptions).

    ```C++
    IACList2 *pal2;

    hr = punkSource->QueryInterface(IID_PPV_ARGS(&pal2));
    if (SUCCEEDED(hr))
    {
        hr = pal2->SetOptions(ACLO_FILESYSONLY);
        pal2->Release();
    }
    ```

    

4.  Initialisieren Sie das AutoVervollständigen-Objekt.

    In diesem Beispiel ist **hwndEdit** das Handle des Bearbeitungssteuerelementfensters, für das die automatische Vervollständigung aktiviert werden soll. Eine Beschreibung der letzten beiden nicht verwendeten Parameter finden Sie unter [**IAutoComplete::Init.**](/windows/desktop/api/Shldisp/nf-shldisp-iautocomplete-init)

    ```C++
    hr = pac->Init(hwndEdit, punkSource, NULL, NULL);
    ```

    

5.  Legen Sie die Optionen des AutoVervollständigen-Objekts fest (optional).

    Sie können das Verhalten des AutoVervollständigen-Objekts anpassen, indem Sie dessen Optionen festlegen. Eine vollständige Liste der Optionen und deren Werte finden Sie in der Dokumentation zu [**INSTALLERList2::SetOptions.**](/windows/win32/api/shlobj_core/nf-shlobj_core-iaclist2-setoptions)

    ```C++
    IAutoComplete2 *pac2;

    hr = pac->QueryInterface(IID_PPV_ARGS(&pac2));

    if (SUCCEEDED(hr))
    {
        hr = pac2->SetOptions(ACO_AUTOSUGGEST);
        pac2->Release();
    }
    ```

    

6.  Geben Sie die Objekte frei.

    > [!Note]  
    > Das AutoVervollständigen-Objekt bleibt auch nach der Freigabe an das Bearbeitungssteuerelement angefügt. Wenn Sie beabsichtigen, später auf diese Objekte zugreifen zu müssen , z. B. wenn Sie die Optionen für die automatische Vervollständigung zu einem späteren Zeitpunkt ändern möchten, ist es nicht erforderlich, dass Sie sie an diesem Punkt freigeben.

     

    ```C++
    punkSource->Release();
    pac->Release();
    ```

    

### <a name="creating-a-compound-autocomplete-object"></a>Erstellen eines zusammengesetzten AutoVervollständigen-Objekts

Ein zusammengesetztes AutoVervollständigen-Objekt stimmt mit Zeichenfolgen aus mehreren Quellen überein. Beispielsweise verwendet die Windows Internet Explorer Adressleiste ein zusammengesetztes AutoVervollständigen-Objekt, da der Benutzer möglicherweise mit der Eingabe des Namens einer Datei oder einer URL beginnt. Die meisten Schritte beim Erstellen eines zusammengesetzten AutoVervollständigen-Objekts sind identisch mit den Schritten in "Erstellen eines einfachen AutoVervollständigen-Objekts". Diese Schritte werden als solche angegeben.

1.  Erstellen Sie das AutoVervollständigen-Objekt. Dies entspricht Schritt 1 oben.

2.  Erstellen Sie den AutoVervollständigen-Verbundquellobjekt-Manager.

    Mit dem zusammengesetzten AutoVervollständigen-Quellobjekt können mehrere AutoVervollständigen-Quellen zu einer einzelnen AutoVervollständigen-Quelle kombiniert werden.

    ```C++
    IObjMgr *pom;

    hr = CoCreateInstance(CLSID_ACLMulti, 
                          NULL, 
                          CLSCTX_INPROC_SERVER,
                          IID_PPV_ARGS(&pom));
    ```

    

3.  Erstellen und Festlegen von Optionen für jede AutoVervollständigen-Quelle. Wiederholen Sie die obigen Schritte 2 und 3 für jede Quelle.

4.  Fügen Sie jede AutoVervollständigen-Quelle an den Quellobjekt-Manager an.

    ```C++
    hr = pom->Append(punkSource1);
    hr = pom->Append(punkSource2);
    ```

    

5.  Initialisieren Sie das AutoVervollständigen-Objekt.

    Dies ist identisch mit Schritt 4 oben, außer dass Sie den Verbundquellobjekt-Manager übergeben, anstatt die einfache AutoVervollständigen-Quelle an [**IAutoComplete::Init**](/windows/desktop/api/Shldisp/nf-shldisp-iautocomplete-init)zu übergeben.

    ```C++
    hr = pac->Init(hwndEdit, pom, NULL, NULL);
    ```

    

6.  Legen Sie die Optionen des AutoVervollständigen-Objekts fest. Dies entspricht Schritt 5 oben.

7.  Geben Sie die Objekte frei.

    Wie im einfachen Fall können Sie die Objekte freigeben, sobald Sie die Verwendung abgeschlossen haben. Sie können sie aber auch beibehalten, um die Optionen später zu ändern.

    ```C++
    pac->Release();
    pom->Release();

    // Release each individual source.
    punkSource1->Release(); 
    punkSource2->Release();
    ```

    

 

 
