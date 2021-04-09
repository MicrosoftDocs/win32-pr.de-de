---
title: Visual Basic Methoden Notizen-accValue
description: Die Object Description Language (ODL-Datei), Oleacc. ODL, enthält Informationen, die sich von der C/C++-Implementierung unterscheiden. Die Datei Oleacc. ODL enthält die folgende Definition für die Version, mit der die-Eigenschaft der-Funktion festgelegt wird.
ms.assetid: 8c27d63a-ae69-4667-9b65-be743a00b49d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ce93bc5d4ff2a2e01da55e30630fda42c573b7f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036811"
---
# <a name="visual-basic-method-notes-accvalue"></a><span data-ttu-id="822de-104">Hinweise zur Visual Basic-Methode: accValue</span><span class="sxs-lookup"><span data-stu-id="822de-104">Visual Basic Method Notes: accValue</span></span>

<span data-ttu-id="822de-105">Die Object Description Language (ODL-Datei), Oleacc. ODL, enthält Informationen, die sich von der C/C++-Implementierung unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="822de-105">The Object Description Language (ODL) file, Oleacc.odl, contains information that differs from the C/C++ implementation.</span></span> <span data-ttu-id="822de-106">Die Datei Oleacc. ODL enthält die folgende Definition für die Version, mit der die-Eigenschaft der-Funktion festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="822de-106">The file Oleacc.odl contains the following definition for the version that sets the property of the function.</span></span>


```C++
    [hidden, propput, id(DISPID_ACC_VALUE)]
    HRESULT accValue(
        [in, optional] VARIANT varChild,
        [in] BSTR szValue);
```



<span data-ttu-id="822de-107">Obwohl der *varChild* -Parameter in der ODL-Datei und im Objektkatalog als optional aufgeführt ist, müssen Sie ihn beim Aufrufen der Eigenschafts Einstellungs Version von [**accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-put_accvalue)einschließen.</span><span class="sxs-lookup"><span data-stu-id="822de-107">Although the *varChild* parameter is listed as optional in the ODL file and the object browser, you must include it when calling the property-setting version of [**accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-put_accvalue).</span></span>

 

 




