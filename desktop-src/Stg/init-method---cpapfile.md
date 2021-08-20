---
title: Init-Methode – CPapFile
description: Das folgende Codebeispiel zeigt, wie CPapFile initialisiert wird.
ms.assetid: 8312a6b2-6f3f-4a24-8aeb-9461f3b1a905
keywords:
- Init-Methode – CPapFile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5e1be255f822b17dbae82e3c5ea76eb75c0a127c3eebe23590d6331721aab4b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117961684"
---
# <a name="init-method---cpapfile"></a>Init-Methode – CPapFile

Das folgende Codebeispiel zeigt, wie **CPapFile** initialisiert wird.

Dieses Beispiel ist die **CPapFile** **Init-Methode** aus "Papfile.cpp".


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



Der *parameter pszAppFileName* wird verwendet, um CPapFile mit einem Standarddateinamen für alle nachfolgenden Lade- oder Speichervorgänge zu initialisieren. Eine Kopie wird im Member **m \_ szCurFileName für** das erste Laden beibehalten. In **StoClien wird** eine solche Auslastung versucht, wenn die Anwendung zum ersten Mal gestartet wird, nachdem CPapFile mit *pszAppFileName* initialisiert wurde, der "STOCLIEN. PAP". Dieser Dateiname wurde in einem CGuiPaper-Konstruktor erstellt, indem der name des aktuell ausgeführten Moduls erhalten wurde. (Die [**Win32-Funktion GetModuleFileName**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulefilenamea) wird aufgerufen.)

Der *pIPaper-Parameter* ist für CPapFile erforderlich, da er diese Schnittstelle für das COPaper-Objekt verwendet, um seine Lade- und Speichervorgänge durchzuführen. **AddRef** wird für diese gespeicherte Kopie *von pIPaper* in Übereinstimmung mit COM-Regeln aufgerufen. Das entsprechende **Release** wird im CPapFile-Destruktor aufgerufen.

 

 