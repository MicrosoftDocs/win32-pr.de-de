---
title: Laden und Registrieren einer Typbibliothek
description: Die Automation Dynamic Link Library (Oleaut32.dll) stellt mehrere Funktionen bereit, die Sie zum Laden und Registrieren einer Typbibliothek aufzurufen können. Wenn LoadTypeLibEx aufgerufen wird, wie im folgenden Beispiel gezeigt, wird die Bibliothek geladen, und die Registrierungseinträge werden erstellt.
ms.assetid: b7404919-fa0a-4de8-8c85-41b7bc7c5a52
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5d533225913d6bcfbb74df3ac42bd00b18b00e4
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104039722"
---
# <a name="loading-and-registering-a-type-library"></a>Laden und Registrieren einer Typbibliothek

Die Automation Dynamic Link Library (Oleaut32.dll) stellt mehrere Funktionen bereit, die Sie zum Laden und Registrieren einer Typbibliothek aufzurufen können. Wenn [LoadTypeLibEx](/windows/win32/api/oleauto/nf-oleauto-loadtypelibex)aufgerufen wird, wie im folgenden Beispiel gezeigt, wird die Bibliothek geladen, und die Registrierungseinträge werden erstellt.

## <a name="example"></a>Beispiel

``` syntax
ITypeLib *pTypeLib;
HRESULT hr;
hr = LoadTypeLibEx("example.tlb", REGKIND_REGISTER, &pTypeLib);
if(SUCCEEDED(hr))
{
    pTypeLib->Release();
} else {
    exit(0); // Handle errors here.
}
```

 

 