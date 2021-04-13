---
title: 'Init-Methode: cpapfile'
description: Im folgenden Codebeispiel wird gezeigt, wie cpapfile initialisiert wird.
ms.assetid: 8312a6b2-6f3f-4a24-8aeb-9461f3b1a905
keywords:
- 'Init-Methode: cpapfile'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea4fb5729ddcf20545254e3e461070c3e68f3421
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390793"
---
# <a name="init-method---cpapfile"></a>Init-Methode: cpapfile

Im folgenden Codebeispiel wird gezeigt, wie **cpapfile** initialisiert wird.

Bei diesem Beispiel handelt es sich um die **cpapfile**- **Init** -Methode von papfile. cpp.


```C++
HRESULT CPapFile::Init(
                      TCHAR* pszAppFileName,
                      IPaper* pIPaper)
  {
    HRESULT hr = E_FAIL;

    if (NULL != pIPaper)
    {
      // Keep CPapFile copy of pIPaper. Thus AddRef it.
      // Released in Destructor.
      m_pIPaper = pIPaper;
      m_pIPaper->AddRef();

      if (NULL != pszAppFileName)
      {
        // Set the default current file name.
        StringCchCopy(m_szCurFileName, sizeof(m_szCurFileName), pszAppFileName);

        hr = NOERROR;
      }
    }

    return (hr);
  }
  
```



Der *pszappfilename* -Parameter wird verwendet, um cpapfile mit einem Standard Dateinamen für alle nachfolgenden Lade-oder Speichervorgänge zu initialisieren. Eine Kopie wird für das erste Laden im Member " **m \_ szcurrfilename** " beibehalten. In **stoclien** wird ein solcher Ladevorgang versucht, wenn die Anwendung zum ersten Mal gestartet wird, nachdem cpapfile mit *pszappfilename* mit dem zugewiesenen "stoclien" initialisiert wurde. PAP ". Der Dateiname wurde in einem cguipaper-Konstruktor erstellt, indem der Name des aktuellen ausführenden Moduls erhalten wurde. (Die Win32-Funktion [**GetModuleFileName**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulefilenamea) wird aufgerufen.)

Der *pipaper* -Parameter ist für cpapfile erforderlich, da er diese Schnittstelle für das copaper-Objekt verwendet, um Lade-und Speichervorgänge auszuführen. **Adressf** wird für diese gespeicherte Kopie von *pipaper* in Übereinstimmung mit com-Regeln aufgerufen. Das entsprechende **Release** wird im cpapfile-Dekonstruktor aufgerufen.

 

 