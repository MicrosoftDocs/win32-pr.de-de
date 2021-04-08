---
title: 'Save-Methode: cpapfile'
description: Wenn cpapfile initialisiert ist, kann es verwendet werden, um die aktuellen Zeichnungsdaten im copaper-Objekt zu speichern.
ms.assetid: ceac32e5-7d47-480b-b1cd-5a17ac04dd0c
keywords:
- 'Save-Methode: cpapfile'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3166b649f28cb1a8ddc37e9efc53465a6cb5d3e0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103948094"
---
# <a name="save-method---cpapfile"></a>Save-Methode: cpapfile

Wenn **cpapfile** initialisiert ist, kann es verwendet werden, um die aktuellen Zeichnungsdaten im copaper-Objekt zu speichern.

## <a name="save-method-papfilecpp"></a>Save-Methode (papfile. CPP

Bei diesem Beispiel handelt es sich um die **cpapfile**-Methode zum  [**Speichern**](ipaper--save.md) von papfile. cpp.


```C++
HRESULT CPapFile::Save(
                      SHORT nLockKey,
                      TCHAR* pszFileName)
  {
    HRESULT hr = E_FAIL;
    BOOL bNewFile = (NULL != pszFileName);
    TCHAR* pszFile;

    // If a null file name is passed, then use current file name.
    pszFile = bNewFile ? pszFileName : m_szCurFileName;

    // Use the COM service to reopen, or create, the compound file.
    hr = StgCreateDocfile(
        pszFile,
    STGM_CREATE | STGM_DIRECT | STGM_READWRITE | STGM_SHARE_EXCLUSIVE,
        0,
        &m_pIStorage);
    if (SUCCEEDED(hr))
    {
      // Obtained the IStorage. The compound file is open.
      // Instruct the COPaper object on the server side to save its
      // paper data into the compound file using the IStorage of our
      // client-provided compound file.
      hr = m_pIPaper->Save(nLockKey, m_pIStorage);
      if (SUCCEEDED(hr))
      {
        // The paper data was saved and obtained a new current 
        // compound file name. Copy it for later use in saves 
        // and loads.
        if (bNewFile)
          StringCchCopy(m_szCurFileName, sizeof(m_szCurFileName), pszFileName);
      }

      // Storage complete. Do not hold the file open.
      // Re-obtain the IStorage again later (and thus re-open
      // the compound file) when required for another save or load.
      RELEASE_INTERFACE(m_pIStorage);
    }

    return (hr);
  }
  
```



Wenn **null** für den *pszFileName* -Parameter übergeben wird, wird der gespeicherte Inhalt des Members **m \_ szcurrfilename** als Dateiname verwendet. Der *nlockkey* ist der Client Sperr Schlüssel, der in einem vorherigen-Befehl der copaper [**Lock**](ipaper-methods.md) -Methode in der **iPaper** -Schnittstelle abgerufen wurde.

Die Dienstfunktion "com-Standard [**stgkreatedocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) " wird aufgerufen, um die Verbund Datei zu erstellen, in der die Zeichnungsdaten gespeichert werden.

Der Name der zu erstellenden Verbund Datei wird als erster Parameter übergeben. Dies wird von [**stgkreatedocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) als Unicode-Zeichenfolge erwartet. Wenn **stoclien** für ANSI-Zeichen folgen kompiliert werden (Unicode ist nicht definiert, was der Standardwert in Makefile ist), reduziert sich dieser Aufrufe tatsächlich auf einen Aufrufen einer internen apputil-Funktion, **einer \_ stgfiatedocfile**. Diese Funktion führt die ordnungsgemäße Konvertierung des ANSI pszFile-Parameters in eine Unicode-Version vor, bevor **StgCreateDocfile** aufgerufen wird. Weitere Informationen finden Sie unter apputil. h und Stoserve.htm.

Die zugriffsmodusflags werden als zweiter Parameter übergeben und legen fest, welche Zugriffs Modi für die neue Datei zulässig sind. Mit dem STGM-Flag zum [ \_ Erstellen](stgm-constants.md) eines Zugriffsmodus wird eine neue Verbund Datei erstellt oder ein vorhandener mit dem gleichen Namen überschrieben. [STGM \_ Der Lesevorgang öffnet die](stgm-constants.md) Datei mit Lese-/Schreibberechtigung. [STGM \_ Direkt](stgm-constants.md) öffnet die Datei für den direkten Zugriff im Gegensatz zum transaktiven Zugriff. [STGM \_ Freigabe \_ exklusiv](stgm-constants.md) öffnet die Datei für den exklusiven, nicht freigegebenen Gebrauch durch den Aufrufer.

Der dritte Parameter ist reserviert und muss NULL sein.

Die Adresse der Zeiger Variablen **m \_ pistorage** wird als vierter Parameter an [**stgkreatedocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) übergeben. Wenn der-Rückruf erfolgreich zurückgegeben wurde, enthält **m \_ pistorage** einen Schnittstellen Zeiger auf eine [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) -Schnittstelle. Dies ist die Schnittstelle, die für nachfolgende Vorgänge in der Datei verwendet wird.

Der wichtige Vorgang in diesem Fall besteht darin, dass das copaper-Objekt seine Zeichnungsdaten in der Datei speichert. Dies erfolgt oben mithilfe der [**Save**](ipaper--save.md) -Methode der copaper [**iPaper**](ipaper-methods.md) -Schnittstelle. Wenn copaper das Speichern der Daten im angegebenen Speicher Objekt erfolgreich abgeschlossen hat, wird der Name der Verbund Datei als neuer aktueller Dateiname in **m \_ szcurrfilename** kopiert.

 

 




