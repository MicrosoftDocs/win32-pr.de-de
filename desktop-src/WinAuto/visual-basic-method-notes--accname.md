---
title: Visual Basic Methoden Notizen accName
description: Die Object Description Language (ODL-Datei), Oleacc. ODL, enthält Informationen, die sich von der C/C++-Implementierung unterscheiden.
ms.assetid: f7960acd-cb1a-4c34-a392-0243155a100f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c404c093fc3b92b4d653b0b1258c62918af8e25
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856248"
---
# <a name="visual-basic-method-notes-accname"></a><span data-ttu-id="9e183-103">Hinweise zur Visual Basic-Methode: accName</span><span class="sxs-lookup"><span data-stu-id="9e183-103">Visual Basic Method Notes: accName</span></span>

<span data-ttu-id="9e183-104">Die Object Description Language (ODL-Datei), Oleacc. ODL, enthält Informationen, die sich von der C/C++-Implementierung unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="9e183-104">The Object Description Language (ODL) file, Oleacc.odl, contains information that differs from the C/C++ implementation.</span></span> <span data-ttu-id="9e183-105">Die Datei Oleacc. ODL enthält die folgende Definition für die Version, mit der die-Eigenschaft der-Funktion festgelegt wird:</span><span class="sxs-lookup"><span data-stu-id="9e183-105">The file Oleacc.odl contains the following definition for the version that sets the property of the function:</span></span>


```C++
    [hidden, propput, id(DISPID_ACC_NAME)]
    HRESULT accName(
        [in, optional] VARIANT varChild,
        [in] BSTR szName);
```



<span data-ttu-id="9e183-106">Obwohl der *varChild* -Parameter in der ODL-Datei und im Objektkatalog als optional aufgeführt ist, müssen Sie ihn beim Aufrufen der Eigenschafts Einstellungs Version von [**accName**](https://www.bing.com/search?q=**accName**)einschließen.</span><span class="sxs-lookup"><span data-stu-id="9e183-106">Although the *varChild* parameter is listed as optional in the ODL file and the object browser, you must include it when calling the property-setting version of [**accName**](https://www.bing.com/search?q=**accName**).</span></span>

 

 




