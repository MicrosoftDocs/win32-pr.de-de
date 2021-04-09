---
title: 'Load-Methode: cpapfile'
description: Wenn diese Vorgänge erfolgreich ausgeführt wurden, wird die erhaltene IStorage-Schnittstelle freigegeben. Dadurch wird die Datei geschlossen, und es wird angegeben, dass die Datei bei anderen Client Vorgängen nicht offen gehalten ist. Sie wird bei Bedarf erneut geöffnet.
ms.assetid: 40f79adb-87f3-4b0e-9cfe-927a4bc9ada5
keywords:
- 'Load-Methode: cpapfile'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fe70be7241fe1e1eaeb779317e11a76fb479f76
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103857004"
---
# <a name="load-method---cpapfile"></a>Load-Methode: cpapfile

Wenn diese Vorgänge erfolgreich ausgeführt wurden, wird die erhaltene [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) -Schnittstelle freigegeben. Dadurch wird die Datei geschlossen, und es wird angegeben, dass die Datei bei anderen Client Vorgängen nicht offen gehalten ist. Sie wird bei Bedarf erneut geöffnet.

Bei diesem Beispiel handelt es sich um die **cpapfile**-Methode zum  **Laden** von papfile. cpp.


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



### <a name="remarks"></a>Bemerkungen

Wie bei der [**Save**](save-method---cpapfile.md) -Methode wird beim Übergeben von **null** für den *pszFileName* -Parameter der gespeicherte Inhalt des Members **m \_ szcurrfilename** als Dateiname verwendet. Da eine vorhandene Datei geöffnet werden kann, wird zuerst die apputil **FileExist** -Funktion verwendet, um zu überprüfen, ob die Datei vorhanden ist. Wenn dies der Fall ist, wird die Standard Dienstfunktion " [**stgisstoragefile**](/windows/desktop/api/coml2api/nf-coml2api-stgisstoragefile) " aufgerufen, um das Format der Datei zu überprüfen, um festzustellen, ob es sich um eine gültige Verbund Datei handelt.

Wenn die Datei gültig ist, wird die Standard Dienstfunktion " [**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage) " aufgerufen, um die Datei zu öffnen und einen Zeiger auf eine [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) -Schnittstelle für Sie zurückzugeben.

Der erste Parameter ist der Name der zu öffnenden Verbund Datei. Wie beim " [**stganatedocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) "-Befehl wird diese Zeichenfolge in der Unicode-Form erwartet. während der ANSI-Kompilierung wird ein apputil-Makro verwendet, um sicherzustellen, dass der ANSI-Parameter in den erwarteten Unicode-Parameter konvertiert wird.

Der Speicher Parameter für die zweite Priorität ist **null**, was darauf hinweist, dass er in diesem Beispiel nicht verwendet wird.

Die zugriffsmodusflags werden als dritter Parameter übergeben, um anzugeben, welche Zugriffs Modi für die geöffnete Datei zulässig sind. [**STGM \_ Lesen**](stgm-constants.md) öffnet die Datei mit der Berechtigung schreibgeschützt. [**STGM \_ Direkt**](stgm-constants.md) öffnet die Datei für den direkten Zugriff im Gegensatz zum transaktiven Zugriff. [**STGM \_ Freigabe \_ exklusiv**](stgm-constants.md) öffnet die Datei für den exklusiven, nicht freigegebenen Gebrauch durch den Aufrufer.

Der vierte Element Ausschluss Parameter in **null**, der angibt, dass er in diesem Beispiel nicht verwendet wird.

Der fünfte Parameter ist für die zukünftige Verwendung reserviert und muss NULL sein.

Die Adresse der Zeiger Variablen **m \_ pistorage** wird als der sechste Parameter übergeben. Wenn der-Rückruf erfolgreich zurückgegeben wurde, enthält **m \_ pistorage** einen Zeiger auf eine [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) -Schnittstelle. Dies ist die Schnittstelle, die für nachfolgende Vorgänge in der geöffneten Datei verwendet wird.

Der wichtige Vorgang in diesem Fall besteht darin, dass das copaper-Objekt seine Zeichnungsdaten aus der Datei lädt. Dies erfolgt oben mithilfe der **Load** -Methode der [**iPaper**](ipaper-methods.md) -Schnittstelle von copaper. Wenn copaper das Laden der Daten mit dem bereitgestellten [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) erfolgreich durchläuft, wird der Name der Verbund Datei als neuer aktueller Dateiname in **m \_ szcurrfilename** kopiert.

Wenn diese Vorgänge erfolgreich abgeschlossen wurden, wird die [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) -Schnittstelle freigegeben, die abgerufen wurde. Dadurch wird die Datei geschlossen und bedeutet, dass die Datei bei anderen Client Vorgängen nicht offen gehalten wird. Sie wird bei Bedarf erneut geöffnet.

 

 




