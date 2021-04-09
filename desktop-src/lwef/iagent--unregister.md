---
title: Aufhebung der Registrierung durch iagent
description: Aufhebung der Registrierung durch iagent
ms.assetid: d81cde72-f9ff-45aa-9dbf-faea9a478c3c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 796e033ac823ee7c79fe5312fab2c57dec36e694
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103858248"
---
# <a name="iagentunregister"></a>Iagent:: Unregister

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT Unregister(
   long dwSinkID  //notification sink ID
);
```

Entlädt die Zeichendaten für das angegebene Zeichen aus der [**Zeichen**](/windows/desktop/lwef/the-characters-object) Auflistung.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="dwSinkID"></span><span id="dwsinkid"></span><span id="DWSINKID"></span>*dwsink ID*
</dt> <dd>

Die ID der Benachrichtigungs Senke.

</dd> </dl>

Verwenden Sie diese Methode, wenn Sie die Microsoft-Agent-Dienste nicht mehr benötigen, z. b. wenn die Anwendung heruntergefahren wird.

## <a name="see-also"></a>Weitere Informationen

[**Iagent:: Register**](iagent--register.md)


 

 