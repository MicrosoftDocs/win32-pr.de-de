---
title: Save-Methode – CPapFile
description: Wenn CPapFile initialisiert wird, kann es verwendet werden, um die aktuellen Zeichnungsdaten im COPaper-Objekt zu speichern.
ms.assetid: ceac32e5-7d47-480b-b1cd-5a17ac04dd0c
keywords:
- Save-Methode – CPapFile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b465d5b275949b3cdfcea04a5023cd110a8600c59a706d2c2f1515e4225c757
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117960597"
---
# <a name="save-method---cpapfile"></a>Save-Methode – CPapFile

Wenn **CPapFile** initialisiert wird, kann es verwendet werden, um die aktuellen Zeichnungsdaten im COPaper-Objekt zu speichern.

## <a name="save-method-papfilecpp"></a>Save-Methode (PAPFILE. CPP)

Dieses Beispiel ist die **CPapFile** [**Save-Methode**](ipaper--save.md) von Papfile.cpp.


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



Wenn **NULL** für den *pszFileName-Parameter* übergeben wird, wird der gespeicherte Inhalt des Members **m \_ szCurFileName** für den Dateinamen verwendet. *nLockKey* ist der Clientsperrschlüssel, der in einem vorherigen Aufruf der COPaper [**Lock-Methode**](ipaper-methods.md) in der **IPaper-Schnittstelle** abgerufen wurde.

Die COM-Standarddienstfunktion [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) wird aufgerufen, um die Verbunddatei zu erstellen, in der die Zeichnungsdaten gespeichert werden.

Der Name der zu erstellende Verbunddatei wird als erster Parameter übergeben. Dies wird von [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) als Unicode-Zeichenfolge erwartet. Wenn **StoClien** für ANSI-Zeichenfolgen kompiliert wird (UNICODE ist nicht definiert, was der Standardwert im Makefile ist), reduziert sich dieser Aufruf tatsächlich auf einen Aufruf einer internen APPUTIL-Funktion, **einer \_ StgCreateDocfile-**. Diese Funktion führt die ordnungsgemäße Konvertierung des ANSI pszFile-Parameters in eine Unicode-Version durch, bevor **StgCreateDocfile** aufgerufen wird. Weitere Informationen finden Sie unter Apputil.h und Stoserve.htm.

Die Zugriffsmodusflags werden als zweiter Parameter übergeben und bestimmen, welche Zugriffsmodi für die neue Datei zulässig sind. Das [STGM CREATE-Zugriffsmodusflag \_ ](stgm-constants.md) erstellt eine neue Verbunddatei oder überschreibt eine vorhandene mit dem gleichen Namen. [STGM \_ READWRITE](stgm-constants.md) öffnet die Datei mit Lese-/Schreibberechtigung. [STGM \_ DIRECT](stgm-constants.md) öffnet die Datei für den direkten Zugriff und nicht für den transaktiven Zugriff. [STGM \_ SHARE \_ EXCLUSIVE](stgm-constants.md) öffnet die Datei für die exklusive, nicht freigegebene Verwendung durch den Aufrufer.

Der dritte Parameter ist reserviert und muss 0 (null) sein.

Die Adresse der Zeigervariable **m \_ pIStorage** wird als vierter Parameter an [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) übergeben. Wenn der Aufruf erfolgreich zurückgegeben wird, enthält **m \_ pIStorage** einen Schnittstellenzeiger auf eine [**IStorage-Schnittstelle.**](/windows/desktop/api/Objidl/nn-objidl-istorage) Dies ist die Schnittstelle, die für alle nachfolgenden Vorgänge in der Datei verwendet wird.

In diesem Fall ist es wichtig, dass das COPaper-Objekt seine Zeichnungsdaten in der Datei speichert. Dies erfolgt oben mithilfe der [**Save-Methode**](ipaper--save.md) der [**COPaper IPaper-Schnittstelle.**](ipaper-methods.md) Wenn COPaper seine Daten erfolgreich im bereitgestellten Speicherobjekt speichert, wird der Name der Verbunddatei als neuer aktueller Dateiname in **m \_ szCurFileName** kopiert.

 

 




