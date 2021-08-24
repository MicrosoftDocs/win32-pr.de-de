---
title: Laden und Registrieren einer Typbibliothek
description: Die Automation Dynamic Link Library, Oleaut32.dll, bietet mehrere Funktionen, die Sie aufrufen können, um eine Typbibliothek zu laden und zu registrieren. Beim Aufrufen von LoadTypeLibEx wird, wie im folgenden Beispiel gezeigt, sowohl die Bibliothek geladen als auch die Registrierungseinträge erstellt.
ms.assetid: b7404919-fa0a-4de8-8c85-41b7bc7c5a52
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e98ea3a28f3884cbd6a377e45f1b537d169f510fdc4ce9a433dff6e976d9c0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119854230"
---
# <a name="loading-and-registering-a-type-library"></a>Laden und Registrieren einer Typbibliothek

Die Automation Dynamic Link Library, Oleaut32.dll, bietet mehrere Funktionen, die Sie aufrufen können, um eine Typbibliothek zu laden und zu registrieren. Beim [Aufrufen von LoadTypeLibEx](/windows/win32/api/oleauto/nf-oleauto-loadtypelibex)wird, wie im folgenden Beispiel gezeigt, sowohl die Bibliothek geladen als auch die Registrierungseinträge erstellt.

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

 

 