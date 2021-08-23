---
title: IAgentCharacter SetIdleOn
description: IAgentCharacter SetIdleOn
ms.assetid: 397d223a-0970-4535-ad46-2923df6b9975
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fde86da6dda12744aedcd780b93d92c45fe2906dd16073bf0e3555848718e747
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119665680"
---
# <a name="iagentcharactersetidleon"></a>IAgentCharacter::SetIdleOn

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

``` syntax
HRESULT SetIdleOn(
   long bOn  // idle processing flag
);
```

Legt die automatische Leerlaufverarbeitung für ein Zeichen fest.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="bOn"></span><span id="bon"></span><span id="BON"></span>*Bon*
</dt> <dd>

Leerlauf-Verarbeitungsflag. Wenn dieser Parameter **True** ist, gibt der Microsoft-Agent automatisch Idling-Zustandsanimationen wieder. 

</dd> </dl>

Der Server legt automatisch ein Time out nach der letzten Animation fest, die für ein Zeichen wiedergegeben wurde. Wenn das Intervall dieses Timers abgeschlossen ist, beginnt der Server die **Idling-Zustände** für ein Zeichen und spielt die zugeordneten **Idling-Animationen** in regelmäßigen Abständen ab. Wenn Sie die **Idling-Zustandsanimationen** selbst verwalten möchten, legen Sie die -Eigenschaft auf **False** fest. Diese Eigenschaft gilt nur für die Verwendung des Zeichens durch Ihre Clientanwendung. Die Einstellung wirkt sich nicht auf andere Clients des Zeichens oder anderer Zeichen Ihrer Clientanwendung aus.

## <a name="see-also"></a>Weitere Informationen

[**IAgentCharacter::GetIdleOn**](iagentcharacter--getidleon.md)


 

 




