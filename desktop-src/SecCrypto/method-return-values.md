---
description: Der Rückgabewert für C++-Schnittstellenmethoden ist immer vom Typ HRESULT. Dieser Wert kann überprüft werden, um den Erfolg oder Fehler zu ermitteln.
ms.assetid: f6478e72-0fe9-4c3b-b08a-f71c9c943910
title: Rückgabewerte der Methode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 073df1d306fb991d7e1347ff90a21d578bf42583c642a694de3160b405963a28
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100760"
---
# <a name="method-return-values"></a>Rückgabewerte der Methode

Der Rückgabewert für C++-Schnittstellenmethoden ist immer vom Typ **HRESULT**; Dieser Wert kann überprüft werden, um den Erfolg oder Fehler zu ermitteln. Die Verwendung von Ausgabeparametern ermöglicht es, Variablen während des Methoden- oder Eigenschaftsaufrufs Werte zuzuweisen. Das folgende Beispiel zeigt einen C++-Methodenaufruf zum Aufzählen von Anbietern.


```C++
UINT          ucEnumProvIndex = 0;
BSTR          bstrProvider = NULL;
HRESULT       hr;

// pEnroll is previously instantiated CEnroll interface pointer
hr = pEnroll->enumProviders(ucEnumProvIndex, 0, &bstrProvider);
```



Im vorangehenden Codefragment wird Erfolg oder Fehler an die Variable "hr" zurückgegeben. Wenn der Aufruf erfolgreich war, wird hr auf S OK festgelegt, \_ und die Variable bstrProvider enthält den Namen des aufzählten Anbieters.

Ein C++-Aufruf zum Abrufen eines Eigenschaftswerts würde wie folgt aussehen.


```C++
BSTR     bstrStoreName = NULL;
HRESULT  hr;

// pEnroll is previously instantiated CEnroll interface pointer

// get the storename
hr = pEnroll->get_CAStoreName( &bstrStoreName );

// (When done using bstrStoreName, free it by calling SysFreeString).
```



Ein C++-Aufruf zum Festlegen eines Eigenschaftswerts würde wie folgt aussehen.


```C++
// bstrNewName previously set to a valid store name
hr = pEnroll->put_CAStoreName( bstrNewName );
```



 

 



