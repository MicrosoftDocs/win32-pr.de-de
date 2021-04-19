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
# <a name="method-return-values"></a><span data-ttu-id="1a244-103">Methoden Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="1a244-103">Method Return Values</span></span>

<span data-ttu-id="1a244-104">Der Rückgabewert für C++-Schnittstellen Methoden ist immer vom Typ **HRESULT**. Dieser Wert kann geprüft werden, um den Erfolg oder Misserfolg zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="1a244-104">The return value for C++ interface methods is always of type **HRESULT**; this value can be checked to determine success or failure.</span></span> <span data-ttu-id="1a244-105">Die Verwendung von "Output"-Parametern ermöglicht das Zuweisen von Werten zu Variablen während des Methoden-oder Eigenschafts Aufrufes.</span><span class="sxs-lookup"><span data-stu-id="1a244-105">The use of "output" parameters allows values to be assigned to variables during the method or property call.</span></span> <span data-ttu-id="1a244-106">Das folgende Beispiel zeigt einen C++-Methoden Aufrufzum Aufzählen von Anbietern.</span><span class="sxs-lookup"><span data-stu-id="1a244-106">The following example shows a C++ method call to enumerate providers.</span></span>


```C++
UINT          ucEnumProvIndex = 0;
BSTR          bstrProvider = NULL;
HRESULT       hr;

// pEnroll is previously instantiated CEnroll interface pointer
hr = pEnroll->enumProviders(ucEnumProvIndex, 0, &bstrProvider);
```



<span data-ttu-id="1a244-107">Im vorangehenden Code Fragment wird Erfolg oder Fehler an die Variablen "HR" zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="1a244-107">In the preceding code fragment, success or failure is returned to the "hr" variable.</span></span> <span data-ttu-id="1a244-108">Wenn der-Befehl erfolgreich ausgeführt wurde, wird HR auf ' OK ' festgelegt, \_ und die Variable ' bstrauch Provider ' enthält den Namen des enumerationsanbieters.</span><span class="sxs-lookup"><span data-stu-id="1a244-108">If the call was successful, hr will be set to S\_OK and the variable bstrProvider will contain the name of the enumerated provider.</span></span>

<span data-ttu-id="1a244-109">Ein C++-Befehl zum Abrufen eines Eigenschafts Werts wäre wie folgt.</span><span class="sxs-lookup"><span data-stu-id="1a244-109">A C++ call to retrieve a property value would be as follows.</span></span>


```C++
BSTR     bstrStoreName = NULL;
HRESULT  hr;

// pEnroll is previously instantiated CEnroll interface pointer

// get the storename
hr = pEnroll->get_CAStoreName( &bstrStoreName );

// (When done using bstrStoreName, free it by calling SysFreeString).
```



<span data-ttu-id="1a244-110">Ein C++-Befehl, um einen Eigenschafts Wert festzulegen, wäre wie folgt.</span><span class="sxs-lookup"><span data-stu-id="1a244-110">A C++ call to set a property value would be as follows.</span></span>


```C++
// bstrNewName previously set to a valid store name
hr = pEnroll->put_CAStoreName( bstrNewName );
```



 

 



