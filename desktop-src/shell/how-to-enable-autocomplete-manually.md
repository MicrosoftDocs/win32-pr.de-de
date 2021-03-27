---
description: Um eine ausführlichere Kontrolle über das Auto Vervollständigen-Verhalten zu erhalten oder eine benutzerdefinierte Quelle von Auto Vervollständigen-Zeichen folgen hinzuzufügen, müssen Sie das Auto Vervollständigen-Objekt selbst verwalten.
ms.assetid: E1A7B1B0-2879-452E-9EBB-73F02B932200
title: Manuelles Aktivieren von AutoComplete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aee4b327c6ccdd62fd921c56cfb046edb8527bc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979569"
---
# <a name="how-to-enable-autocomplete-manually"></a>Manuelles Aktivieren von AutoComplete

Um eine ausführlichere Kontrolle über das Auto Vervollständigen-Verhalten zu erhalten oder eine benutzerdefinierte Quelle von Auto Vervollständigen-Zeichen folgen hinzuzufügen, müssen Sie das Auto Vervollständigen-Objekt selbst verwalten. Die automatische Vervollständigung kann auf folgende Weise manuell aktiviert werden.

## <a name="instructions"></a>Instructions

### <a name="creating-a-simple-autocomplete-object"></a>Erstellen eines einfachen AutoComplete-Objekts

In den folgenden Schritten wird gezeigt, wie ein einfaches Auto Vervollständigen-Objekt erstellt und initialisiert wird. Ein einfaches Auto Vervollständigen-Objekt schließt Zeichen folgen aus einer einzelnen Quelle ab. Die Fehlerüberprüfung wurde in diesem Beispiel absichtlich ausgelassen.

1.  Erstellen Sie das Auto Vervollständigen-Objekt.

    ```C++
    IAutoComplete *pac;

    HRESULT hr = CoCreateInstance(CLSID_AutoComplete, 
                                    NULL, 
                                  CLSCTX_INPROC_SERVER,
                                  IID_PPV_ARGS(&pac));
    ```

    

2.  Erstellen Sie die Auto Vervollständigen-Quelle. Sie können eine [vordefinierte Auto Vervollständigen-Quelle](ac-ovw.md) verwenden, oder Sie können eine eigene benutzerdefinierte Quelle schreiben.

    Im folgenden Code wird eine der vordefinierten Auto Vervollständigen-Quellen verwendet.

    ```C++
    IUnknown *punkSource;

    hr = CoCreateInstance(CLSID_ACListISF, 
                          NULL, 
                          CLSCTX_INPROC_SERVER,
                          IID_PPV_ARGS(&punkSource));
    ```

    

    Im folgenden Code wird eine benutzerdefinierte Auto Vervollständigen-Quelle verwendet. Sie können Ihre eigene Auto Vervollständigen-Quelle schreiben, indem Sie ein-Objekt implementieren, das die [**IEnumString**](/windows/win32/api/objidlbase/nn-objidlbase-ienumstring) -Schnittstelle verfügbar macht. Das-Objekt kann optional auch die [**iaclist**](/windows/win32/api/shlobj_core/nn-shlobj_core-iaclist) -und [**IACList2**](/windows/win32/api/shlobj_core/nn-shlobj_core-iaclist2) -Schnittstellen implementieren.

    ```C++
    CCustomAutoCompleteSource *pcacs = new CCustomAutoCompleteSource();

    hr = pcacs->QueryInterface(IID_PPV_ARGS(&punkSource));
    if(SUCCEEDED(hr))
    {
        // ...
    }

    pcacs->Release();
    ```

    

3.  Legen Sie die Optionen für die Auto Vervollständigen-Quelle fest (optional).

    Sie können das Verhalten der Auto Vervollständigen-Quelle anpassen, indem Sie deren Optionen festlegen, wenn die Quelle die [**IACList2**](/windows/win32/api/shlobj_core/nn-shlobj_core-iaclist2) -Schnittstelle verfügbar macht. Bei Verwendung der vordefinierten Auto Vervollständigen-Quellen exportiert nur CLSID \_ aclistisf **IACList2**. Eine umfassende Liste der Optionen und deren Werte finden Sie unter [**IACList2:: * toptions**](/windows/win32/api/shlobj_core/nf-shlobj_core-iaclist2-setoptions).

    ```C++
    IACList2 *pal2;

    hr = punkSource->QueryInterface(IID_PPV_ARGS(&pal2));
    if (SUCCEEDED(hr))
    {
        hr = pal2->SetOptions(ACLO_FILESYSONLY);
        pal2->Release();
    }
    ```

    

4.  Initialisieren Sie das Auto Vervollständigen-Objekt.

    In diesem Beispiel ist **hwndedit** das Handle des Fensters Bearbeitungs Steuerelement, für das Auto Vervollständigen aktiviert werden soll. Eine Beschreibung der letzten beiden nicht verwendeten Parameter finden Sie unter [**iautocomplete:: init**](/windows/desktop/api/Shldisp/nf-shldisp-iautocomplete-init) .

    ```C++
    hr = pac->Init(hwndEdit, punkSource, NULL, NULL);
    ```

    

5.  Legen Sie die Optionen für das Auto Vervollständigen-Objekt fest (optional).

    Sie können das Verhalten des Objekts Auto Vervollständigen anpassen, indem Sie dessen Optionen festlegen. Eine umfassende Liste der Optionen und deren Werte finden Sie in der Dokumentation zu [**IACList2::-toptions**](/windows/win32/api/shlobj_core/nf-shlobj_core-iaclist2-setoptions).

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
    > Das Auto Vervollständigen-Objekt bleibt auch nach der Freigabe an das Bearbeitungs Steuerelement angefügt. Wenn Sie einen späteren Zugriff auf diese Objekte vorsehen – wenn Sie die Auto Vervollständigen-Optionen zu einem späteren Zeitpunkt ändern möchten, z. b. –, ist es nicht erforderlich, dass Sie Sie an diesem Punkt freigeben.

     

    ```C++
    punkSource->Release();
    pac->Release();
    ```

    

### <a name="creating-a-compound-autocomplete-object"></a>Erstellen eines Verbund Objekts mit automatischer Vervollständigung

Ein zusammengesetztes Auto Vervollständigen-Objekt entspricht Zeichen folgen aus mehreren Quellen. Beispielsweise wird in der Windows Internet Explorer-Adressleiste ein Verbund Objekt für das automatische vervollständigen verwendet, da der Benutzer möglicherweise mit der Eingabe des Namens einer Datei oder einer URL beginnt. Die meisten Schritte zum Erstellen eines Verbund Objekts mit automatischer Vervollständigung sind identisch mit den Schritten unter "Erstellen eines einfachen Auto Vervollständigen-Objekts". Diese Schritte werden als solche Schritte angezeigt.

1.  Erstellen Sie das Auto Vervollständigen-Objekt. Dies ist das gleiche wie in Schritt 1 oben.

2.  Erstellen Sie den Auto Vervollständigen-Verbund Quell Objekt-Manager.

    Das Auto Vervollständigen-Verbund Quell Objekt ermöglicht das Kombinieren mehrerer Auto Vervollständigen-Quellen zu einer einzelnen Auto Vervollständigen-Quelle.

    ```C++
    IObjMgr *pom;

    hr = CoCreateInstance(CLSID_ACLMulti, 
                          NULL, 
                          CLSCTX_INPROC_SERVER,
                          IID_PPV_ARGS(&pom));
    ```

    

3.  Erstellen und Festlegen von Optionen für jede der Auto Vervollständigen-Quellen Wiederholen Sie die Schritte 2 und 3 für jede Quelle.

4.  Fügen Sie jede Auto Vervollständigen-Quelle an den Quell Objekt-Manager an.

    ```C++
    hr = pom->Append(punkSource1);
    hr = pom->Append(punkSource2);
    ```

    

5.  Initialisieren Sie das Auto Vervollständigen-Objekt.

    Dies entspricht Schritt 4 oben, mit der Ausnahme, dass Sie den Verbund Quell Objekt-Manager übergeben, anstatt die einfache Auto Vervollständigen-Quelle an [**iautocomplete:: init**](/windows/desktop/api/Shldisp/nf-shldisp-iautocomplete-init)zu übergeben.

    ```C++
    hr = pac->Init(hwndEdit, pom, NULL, NULL);
    ```

    

6.  Legen Sie die Optionen des Objekts Auto Vervollständigen fest. Dies entspricht dem oben beschriebenen Schritt 5.

7.  Geben Sie die Objekte frei.

    Wie im einfachen Fall können Sie die Objekte freigeben, sobald Sie Sie verwenden, aber Sie können Sie auch später beibehalten, um die Optionen zu ändern.

    ```C++
    pac->Release();
    pom->Release();

    // Release each individual source.
    punkSource1->Release(); 
    punkSource2->Release();
    ```

    

 

 
