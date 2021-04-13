---
title: Iagentex showdefaultcharacters-Eigenschaften
description: Iagentex showdefaultcharacters-Eigenschaften
ms.assetid: 4817b52a-7168-4008-9cda-0b8d598daea0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65436135d9763f1cb75db6fb92b9e5f0672e17a8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104473060"
---
# <a name="iagentexshowdefaultcharacterproperties"></a>Iagentex:: showdefaultcharacters-Eigenschaften

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT ShowDefaultCharacterProperties(
   short x,          // x-coordinate of window
   short y,          // y-coordinate of window
   long bUseDefault  // default position flag
);
```

Zeigt das Standard Zeichen Eigenschaften Fenster an.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="x"></span><span id="X"></span>*Stuben*
</dt> <dd>

Die x-Koordinate des Fensters in Pixel relativ zum Bildschirm Ursprung (oben links).

</dd> <dt>

<span id="y"></span><span id="Y"></span>*Teenie*
</dt> <dd>

Die y-Koordinate des Fensters in Pixel relativ zum Bildschirm Ursprung (oben links).

</dd> <dt>

<span id="bUseDefault"></span><span id="busedefault"></span><span id="BUSEDEFAULT"></span>*busekunden default*
</dt> <dd>

Standardpositionsflag. Wenn dieser Parameter **true** ist, zeigt der Microsoft-Agent das Eigenschaften Blatt Fenster für das Standard Zeichen an der letzten Position an, an der es aufgetreten ist.

> [!Note]  
> Für Windows 2000 ist es möglicherweise erforderlich, die neue [**allowsetforegroundwindow**](/windows/desktop/api/winuser/nf-winuser-allowsetforegroundwindow) -API aufzurufen, um sicherzustellen, dass dieses Fenster zum Vordergrund Fenster wird. Weitere Informationen zum Festlegen des Vordergrund Fensters unter Windows 2000 finden Sie in der Platform SDK-Dokumentation.

 

</dd> </dl>

## <a name="see-also"></a>Weitere Informationen

[**Iagentnotifysinkex::D efaultcharacters-Änderung**](iagentnotifysinkex--defaultcharacterchange.md)


 

 