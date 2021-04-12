---
title: Iagentcommand setconficetext
description: Iagentcommand setconficetext
ms.assetid: e776a2ba-3592-4f26-a3e3-2c044eed7f0c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cff1ae34c03f8ff67da61bea1834c25d6844ab2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104390155"
---
# <a name="iagentcommandsetconfidencetext"></a>Iagentcommand:: setconficetext

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT SetConfidenceText(
   BSTR bszTipText  // ConfidenceText setting for Command 
);
```

Legt den Wert des lauschtexttexts für einen [**Befehl**](/windows/desktop/lwef/the-command-object)fest.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="bszTipText"></span><span id="bsztiptext"></span><span id="BSZTIPTEXT"></span>*bsztiptext*
</dt> <dd>

Ein BSTR, der den Text für die [**conficetext**](confidencetext-property.md) -Eigenschaft eines [**Befehls**](/windows/desktop/lwef/the-command-object)angibt.

</dd> </dl>

Wenn der von der am besten zurückgegebene Wert zurückgegebene Vertrauens Wert den Wert, der [**für die Eigenschaft**](/windows/desktop/lwef/the-command-object) [**conficethreshold**](/windows/desktop/lwef/confidence-property) zurückgegeben wurde, nicht überschreitet, wird der in *bsztiptext* angegebene Text in der lausch Info angezeigt.

## <a name="see-also"></a>Weitere Informationen

[**Iagentcommand:: setconficethreshold**](iagentcommand--setconfidencethreshold.md), [**iagentcommand:: getconficethreshold**](iagentcommand--getconfidencethreshold.md), [**iagentcommand:: getconficetext**](iagentcommand--getconfidencetext.md), [**iagentuserinput:: getitemconfidence**](iagentuserinput--getitemconfidence.md)


 

 