---
title: Load-Methode – CPapFile
description: Wenn diese Vorgänge erfolgreich sind, wird die abgerufene IStorage-Schnittstelle freigegeben. Dadurch wird die Datei geschlossen und angegeben, dass die Datei während anderer Clientvorgänge nicht geöffnet gehalten wird. Sie wird bei Bedarf erneut geöffnet.
ms.assetid: 40f79adb-87f3-4b0e-9cfe-927a4bc9ada5
keywords:
- Load-Methode – CPapFile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49eac23bcb79738a30b18eb87a4d8ef4598aba89de0748c58b433df28d614886
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120034890"
---
# <a name="load-method---cpapfile"></a>Load-Methode – CPapFile

Wenn diese Vorgänge erfolgreich sind, wird die abgerufene [**IStorage-Schnittstelle**](/windows/desktop/api/Objidl/nn-objidl-istorage) freigegeben. Dadurch wird die Datei geschlossen und angegeben, dass die Datei während anderer Clientvorgänge nicht geöffnet gehalten wird. Sie wird bei Bedarf erneut geöffnet.

Dieses Beispiel ist die **CPapFile** **Load-Methode** aus Papfile.cpp.


```C++
HRESULT CPapFile::Load(
                      SHORT nLockKey,
                      TCHAR* pszFileName)
  {
    HRESULT hr = E_FAIL;
    BOOL bNewFile = (NULL != pszFileName);
    TCHAR* pszFile;

    // If null file name passed then use current file name.
    pszFile = bNewFile ? pszFileName : m_szCurFileName;

    // Verify that the file is using the APPUTIL function.
    if (FileExist(pszFile))
    {
      // Use the COM service to verify that the file is actually a 
      // valid compound file.
      hr = StgIsStorageFile(pszFile);
      if (SUCCEEDED(hr))
      {
        // Use the COM service to open the compound file and
        // obtain an IStorage interface.
        hr = StgOpenStorage(
               pszFile,
               NULL,
               STGM_DIRECT | STGM_READ | STGM_SHARE_EXCLUSIVE,
               NULL,
               0,
               &m_pIStorage);
        if (SUCCEEDED(hr))
        {
          // An IStorage interface has been obtained. Now, request 
          // the COPaper object on the server side to load into  
          // itself the file's paper data using IStorage for our 
          // client-provided compound file.
          hr = m_pIPaper->Load(nLockKey, m_pIStorage);
          if (SUCCEEDED(hr))
          {
            // The paper data was loaded and a current compound
            // file name exists. Copy it for later use in a saves 
            // and loads.
            if (bNewFile)
              StringCchCopy(m_szCurFileName, sizeof(m_szCurFileName), pszFileName);
          }

          // The Storage object is not required now. Do not hold the 
          // file open. Re-obtain the IStorage again later, when 
          // required (and thus re-open the compound file) for
          // another save or load.
          RELEASE_INTERFACE(m_pIStorage);
        }
      }
    }

    return (hr);
  }
  
```



### <a name="remarks"></a>Hinweise

Wie bei der [**Save-Methode**](save-method---cpapfile.md) wird der gespeicherte Inhalt von Member **m \_ szCurFileName** für den Dateinamen verwendet, wenn **NULL** für den *pszFileName-Parameter* übergeben wird. Da eine vorhandene Datei geöffnet werden kann, wird zuerst die APPUTIL **FileExist-Funktion** verwendet, um zu überprüfen, ob die Datei vorhanden ist. Falls vorhanden, wird die [**StgIsStorageFile-Standarddienstfunktion**](/windows/desktop/api/coml2api/nf-coml2api-stgisstoragefile) aufgerufen, um das Format der Datei zu überprüfen, um zu ermitteln, ob es sich um eine gültige Verbunddatei handelt.

Wenn die Datei gültig ist, wird die [**StgOpenStorage-Standarddienstfunktion**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage) aufgerufen, um die Datei zu öffnen und einen Zeiger auf eine [**IStorage-Schnittstelle**](/windows/desktop/api/Objidl/nn-objidl-istorage) dafür zurückzugeben.

Der erste Parameter ist der Name der zu öffnende Verbunddatei. Wie beim [**StgCreateDocfile-Aufruf**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) wird diese Zeichenfolge im Unicode-Format erwartet, und während der ANSI-Kompilierung wird ein APPUTIL-Makro verwendet, um sicherzustellen, dass der ANSI-Parameter in den erwarteten Unicode-Code konvertiert wird.

Der zweite Speicherparameter mit Priorität ist **NULL** und gibt an, dass er in diesem Beispiel nicht verwendet wird.

Die Zugriffsmodusflags werden als dritter Parameter übergeben, um anzugeben, welche Zugriffsmodi für die geöffnete Datei zulässig sind. [**STGM \_ READ**](stgm-constants.md) öffnet die Datei mit schreibgeschützter Berechtigung. [**STGM \_ DIRECT**](stgm-constants.md) öffnet die Datei für den direkten Zugriff und nicht für den transaktiven Zugriff. [**STGM \_ SHARE \_ EXCLUSIVE**](stgm-constants.md) öffnet die Datei für die exklusive, nicht freigegebene Verwendung durch den Aufrufer.

Der vierte Elementausschlussparameter in **NULL,** der angibt, dass er in diesem Beispiel nicht verwendet wird.

Der fünfte Parameter ist für die zukünftige Verwendung reserviert und muss 0 (null) sein.

Die Adresse der Zeigervariable **\_ m pIStorage** wird als sechster Parameter übergeben. Wenn der Aufruf erfolgreich zurückgegeben wird, enthält **m \_ pIStorage** einen Zeiger auf eine [**IStorage-Schnittstelle.**](/windows/desktop/api/Objidl/nn-objidl-istorage) Dies ist die Schnittstelle, die für alle nachfolgenden Vorgänge in der geöffneten Datei verwendet wird.

In diesem Fall ist es wichtig, dass das COPaper-Objekt seine Zeichnungsdaten aus der Datei lädt. Dies erfolgt oben mithilfe der **Load-Methode** der [**IPaper-Schnittstelle von COPaper.**](ipaper-methods.md) Wenn COPaper seine Daten mithilfe der bereitgestellten [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) laden kann, wird der Name der Verbunddatei als neuer aktueller Dateiname in **m \_ szCurFileName** kopiert.

Wenn diese Vorgänge erfolgreich abgeschlossen wurden, wird die [**abgerufene IStorage-Schnittstelle**](/windows/desktop/api/Objidl/nn-objidl-istorage) freigegeben. Dadurch wird die Datei geschlossen und bedeutet, dass die Datei während anderer Clientvorgänge nicht geöffnet gehalten wird. Sie wird bei Bedarf erneut geöffnet.

 

 




