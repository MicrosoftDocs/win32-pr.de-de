---
title: IAgentBalloon GetEnabled
description: IAgentBalloon GetEnabled
ms.assetid: 1a5ea6c0-6150-459f-95eb-a9c7598c1d94
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d144374f690d295b80d0092add56439eb4e5fc9d546ba1f970ab99976cf2d7f6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119888391"
---
# <a name="iagentballoongetenabled"></a>IAgentBalloon::GetEnabled

\[Microsoft Agent ist ab Version Windows 7 veraltet und in nachfolgenden Versionen von Windows.\]

``` syntax
HRESULT GetEnabled(
  long * pbEnabled  // address of variable for Enabled setting 
);                  // for word balloon
```

Ruft den Wert der [**Enabled-Eigenschaft**](enabled-property.md) für eine Wortsprechblase ab.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="pbEnabled"></span><span id="pbenabled"></span><span id="PBENABLED"></span>*pbEnabled*
</dt> <dd>

Die Adresse einer Variablen, die **True empfängt,** wenn das Wort Balloon aktiviert ist, und **False,** wenn es deaktiviert ist.

</dd> </dl>

Der Microsoft Agent-Server zeigt automatisch das Wort Balloon für gesprochene Ausgabe an, es sei denn, es ist deaktiviert. Das Wort Balloon kann für ein Zeichen im Microsoft Agent-Zeichen-Editor oder (vom Benutzer) für alle Zeichen im Microsoft Agent-Eigenschaftenblatt deaktiviert werden. Wenn der Benutzer das Wort Balloon deaktiviert, kann der Client es nicht wiederherstellen.

 

 




