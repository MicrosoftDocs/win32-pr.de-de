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
# <a name="visual-basic-method-notes-accname"></a>Hinweise zur Visual Basic-Methode: accName

Die Object Description Language (ODL-Datei), Oleacc. ODL, enthält Informationen, die sich von der C/C++-Implementierung unterscheiden. Die Datei Oleacc. ODL enthält die folgende Definition für die Version, mit der die-Eigenschaft der-Funktion festgelegt wird:


```C++
    [hidden, propput, id(DISPID_ACC_NAME)]
    HRESULT accName(
        [in, optional] VARIANT varChild,
        [in] BSTR szName);
```



Obwohl der *varChild* -Parameter in der ODL-Datei und im Objektkatalog als optional aufgeführt ist, müssen Sie ihn beim Aufrufen der Eigenschafts Einstellungs Version von [**accName**](https://www.bing.com/search?q=**accName**)einschließen.

 

 




