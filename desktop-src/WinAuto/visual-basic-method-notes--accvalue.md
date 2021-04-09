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
# <a name="visual-basic-method-notes-accvalue"></a>Hinweise zur Visual Basic-Methode: accValue

Die Object Description Language (ODL-Datei), Oleacc. ODL, enthält Informationen, die sich von der C/C++-Implementierung unterscheiden. Die Datei Oleacc. ODL enthält die folgende Definition für die Version, mit der die-Eigenschaft der-Funktion festgelegt wird.


```C++
    [hidden, propput, id(DISPID_ACC_VALUE)]
    HRESULT accValue(
        [in, optional] VARIANT varChild,
        [in] BSTR szValue);
```



Obwohl der *varChild* -Parameter in der ODL-Datei und im Objektkatalog als optional aufgeführt ist, müssen Sie ihn beim Aufrufen der Eigenschafts Einstellungs Version von [**accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-put_accvalue)einschließen.

 

 




