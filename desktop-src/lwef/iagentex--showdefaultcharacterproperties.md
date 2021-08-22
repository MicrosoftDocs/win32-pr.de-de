---
title: IAgentEx ShowDefaultCharacterProperties
description: IAgentEx ShowDefaultCharacterProperties
ms.assetid: 4817b52a-7168-4008-9cda-0b8d598daea0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 362cffa8d4b34d70111505a60fd5eadc68a220cd45c3beb519e5e39ba62f1a81
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118749814"
---
# <a name="iagentexshowdefaultcharacterproperties"></a>IAgentEx::ShowDefaultCharacterProperties

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

``` syntax
HRESULT ShowDefaultCharacterProperties(
   short x,          // x-coordinate of window
   short y,          // y-coordinate of window
   long bUseDefault  // default position flag
);
```

Zeigt das Standardeigenschaftenfenster für Zeichen an.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="x"></span><span id="X"></span>*X*
</dt> <dd>

Die x-Koordinate des Fensters in Pixel relativ zum Bildschirmursprung (oben links).

</dd> <dt>

<span id="y"></span><span id="Y"></span>*Y*
</dt> <dd>

Die y-Koordinate des Fensters in Pixel relativ zum Bildschirmursprung (oben links).

</dd> <dt>

<span id="bUseDefault"></span><span id="busedefault"></span><span id="BUSEDEFAULT"></span>*bUseDefault*
</dt> <dd>

Standardpositionsflag. Wenn dieser Parameter **True** ist, zeigt der Microsoft-Agent das Eigenschaftenblattfenster für das Standardzeichen an der letzten Angezeigten Position an.

> [!Note]  
> Für Windows 2000 muss möglicherweise die neue [**AllowSetForegroundWindow-API**](/windows/desktop/api/winuser/nf-winuser-allowsetforegroundwindow) aufgerufen werden, um sicherzustellen, dass dieses Fenster zum Vordergrundfenster wird. Weitere Informationen zum Festlegen des Vordergrundfensters unter Windows 2000 finden Sie in der Dokumentation zum Plattform-SDK.

 

</dd> </dl>

## <a name="see-also"></a>Weitere Informationen

[**IAgentNotifySinkEx::D efaultCharacterChange**](iagentnotifysinkex--defaultcharacterchange.md)


 

 