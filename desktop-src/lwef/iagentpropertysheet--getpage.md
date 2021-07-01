---
title: IAgentPropertySheet GetPage
description: IAgentPropertySheet GetPage
ms.assetid: 40d00e9b-dd81-4e23-907a-6ca24a28fa95
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7c08e564b5170d62cf5757536b9e11baec4883c
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119865"
---
# <a name="iagentpropertysheetgetpage"></a>IAgentPropertySheet::GetPage

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

``` syntax
HRESULT GetPage(
BSTR * pbszPage  // address of variable for current property page
);
```

Ruft die aktuelle Seite des Eigenschaftenblatts des Microsoft-Agents ab.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="pbszPage"></span><span id="pbszpage"></span><span id="PBSZPAGE"></span>*pbszPage*
</dt> <dd>

Adresse einer Variablen, die die aktuelle Seite des Eigenschaftenblatts empfängt (zuletzt angezeigte Seite, wenn das Fenster nicht geöffnet ist). Der -Parameter kann eine der folgenden Sein:



|                 | Beschreibung            |
|-----------------|------------------------|
| **"Speech"**    | Die Seite Spracheingabe. |
| **"Ausgabe"**    | Die Seite Ausgabe.       |
| **"Copyright"** | Die Copyrightseite.    |



 

</dd> </dl>

## <a name="see-also"></a>Weitere Informationen

[**IAgentPropertySheet::SetPage**](iagentpropertysheet--setpage.md)


 

 




