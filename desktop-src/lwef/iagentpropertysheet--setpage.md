---
title: IAgentPropertySheet SetPage
description: IAgentPropertySheet SetPage
ms.assetid: 52451a45-4f05-4209-ac3a-b4f2d90b3e74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf67c3ecb10ec5a8372a00e11d356e4b050b50be4a0563d9c4ebeefcd8040f1c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118476790"
---
# <a name="iagentpropertysheetsetpage"></a>IAgentPropertySheet::SetPage

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

``` syntax
HRESULT SetPage(
   BSTR bszPage  // current property page
);
```

Legt die aktuelle Seite des Eigenschaftenblatts des Microsoft-Agents fest.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="bszPage"></span><span id="bszpage"></span><span id="BSZPAGE"></span>*bszPage*
</dt> <dd>

Ein BSTR, der die aktuelle Seite der Eigenschaft festlegt. Der Parameter kann einer der folgenden sein.



|                 | BESCHREIBUNG            |
|-----------------|------------------------|
| **"Speech"**    | Die Seite Spracheingabe. |
| **"Ausgabe"**    | Die Seite Ausgabe.       |
| **"Copyright"** | Die Copyrightseite.    |



 

</dd> </dl>

## <a name="see-also"></a>Weitere Informationen

[**IAgentPropertySheet::GetPage**](iagentpropertysheet--getpage.md)


 

 




