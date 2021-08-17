---
title: Visual Basic Hinweise zur Methode accValue
description: Die ODL-Datei (Object Description Language, Oleacc.odl) enthält Informationen, die sich von der C/C++-Implementierung unterscheiden. Die Datei Oleacc.odl enthält die folgende Definition für die Version, die die -Eigenschaft der Funktion festlegt.
ms.assetid: 8c27d63a-ae69-4667-9b65-be743a00b49d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f552f5a79740e71984b4d9beaba9faad23142b2c9afc78a7378e9b11be4dc521
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117744780"
---
# <a name="visual-basic-method-notes-accvalue"></a>Visual Basic Hinweise zur Methode: accValue

Die ODL-Datei (Object Description Language, Oleacc.odl) enthält Informationen, die sich von der C/C++-Implementierung unterscheiden. Die Datei Oleacc.odl enthält die folgende Definition für die Version, die die -Eigenschaft der Funktion festlegt.


```C++
    [hidden, propput, id(DISPID_ACC_VALUE)]
    HRESULT accValue(
        [in, optional] VARIANT varChild,
        [in] BSTR szValue);
```



Obwohl der *varChild-Parameter* in der ODL-Datei und im Objektbrowser als optional aufgeführt ist, müssen Sie ihn beim Aufrufen der Eigenschafteneinstellungsversion von [**accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-put_accvalue)einschließen.

 

 




