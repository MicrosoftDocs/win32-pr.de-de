---
title: IAgentPropertySheet SetPage
description: IAgentPropertySheet SetPage
ms.assetid: 52451a45-4f05-4209-ac3a-b4f2d90b3e74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b84f9b9d5f74170644488cc2049376ecf409997
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120745"
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

Ein BSTR, der die aktuelle Seite der Eigenschaft festlegt. Der -Parameter kann einer der folgenden sein.



|                 | Beschreibung            |
|-----------------|------------------------|
| **"Speech"**    | Die Seite Spracheingabe. |
| **"Ausgabe"**    | Die Seite Ausgabe.       |
| **"Copyright"** | Die Copyrightseite.    |



 

</dd> </dl>

## <a name="see-also"></a>Weitere Informationen

[**IAgentPropertySheet::GetPage**](iagentpropertysheet--getpage.md)


 

 




