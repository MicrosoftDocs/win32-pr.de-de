---
description: Der Rückgabewert für C++-Schnittstellen Methoden ist immer vom Typ HRESULT. Dieser Wert kann geprüft werden, um den Erfolg oder Misserfolg zu ermitteln.
ms.assetid: f6478e72-0fe9-4c3b-b08a-f71c9c943910
title: Methoden Rückgabewerte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3871cf00bd48c7fbe1432ec86b503fba7795592
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106360067"
---
# <a name="method-return-values"></a>Methoden Rückgabewerte

Der Rückgabewert für C++-Schnittstellen Methoden ist immer vom Typ **HRESULT**. Dieser Wert kann geprüft werden, um den Erfolg oder Misserfolg zu ermitteln. Die Verwendung von "Output"-Parametern ermöglicht das Zuweisen von Werten zu Variablen während des Methoden-oder Eigenschafts Aufrufes. Das folgende Beispiel zeigt einen C++-Methoden Aufrufzum Aufzählen von Anbietern.


```C++
UINT          ucEnumProvIndex = 0;
BSTR          bstrProvider = NULL;
HRESULT       hr;

// pEnroll is previously instantiated CEnroll interface pointer
hr = pEnroll->enumProviders(ucEnumProvIndex, 0, &bstrProvider);
```



Im vorangehenden Code Fragment wird Erfolg oder Fehler an die Variablen "HR" zurückgegeben. Wenn der-Befehl erfolgreich ausgeführt wurde, wird HR auf ' OK ' festgelegt, \_ und die Variable ' bstrauch Provider ' enthält den Namen des enumerationsanbieters.

Ein C++-Befehl zum Abrufen eines Eigenschafts Werts wäre wie folgt.


```C++
BSTR     bstrStoreName = NULL;
HRESULT  hr;

// pEnroll is previously instantiated CEnroll interface pointer

// get the storename
hr = pEnroll->get_CAStoreName( &bstrStoreName );

// (When done using bstrStoreName, free it by calling SysFreeString).
```



Ein C++-Befehl, um einen Eigenschafts Wert festzulegen, wäre wie folgt.


```C++
// bstrNewName previously set to a valid store name
hr = pEnroll->put_CAStoreName( bstrNewName );
```



 

 



