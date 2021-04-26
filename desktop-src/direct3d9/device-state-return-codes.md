---
description: Eine Liste einiger möglicher Rückgabecodes für Methoden und Funktionen.
ms.assetid: 391b56a1-d0aa-4d35-8dba-cf7de66513d8
title: S_PRESENT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6cd860fcc8268bf2b63a9498b9960da359ca210
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107999337"
---
# <a name="s_present"></a>S \_ PRESENT

Eine Liste einiger möglicher Rückgabecodes für Methoden und Funktionen.



| \#Definieren                  | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| S \_ OK                     | Das Gerät wird normal ausgeführt und kann zum Rendern verwendet werden.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| S \_ PRESENT \_ OCCLUDED      | Der Präsentationsbereich ist umschließend. Okklusion bedeutet, dass das Präsentationsfenster minimiert wird oder ein anderes Gerät auf demselben Monitor wie das Präsentationsfenster in den Vollbildmodus übertrat und sich das Präsentationsfenster vollständig auf diesem Monitor befindet. Okklusion tritt nicht auf, wenn der Clientbereich von einem anderen Fenster abgedeckt wird.<br/> Okcluded applications can continue rendering and all calls will succeed, but the occluded presentation window will not be updated. (Okcluded applications can continue rendering and all calls will succeed, but the occluded presentation window will not be updated. (Okcluded applications can continue rendering and all calls will succeed, but the occluded presentation window will not be updated. Vorzugsweise sollte die Anwendung das Rendern im Präsentationsfenster mithilfe des Geräts beenden und [**CheckDeviceState**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-checkdevicestate) weiterhin aufrufen, bis S OK oder \_ S PRESENT MODE CHANGED zurückgegeben \_ \_ \_ wird.<br/> |
| S \_ PRESENT \_ MODE \_ CHANGED | Der Desktopanzeigemodus wurde geändert. Die Anwendung kann das Rendering fortsetzen, es kann jedoch eine Farbkonvertierung/Streckung geben. Wählen Sie ein Zurückpufferformat aus, das dem aktuellen Anzeigemodus ähnelt, und rufen Sie Zurücksetzen auf, um die Swapketten neu zu erstellen. Das Gerät verlässt diesen Zustand, nachdem eine Zurücksetzung aufgerufen wurde.                                                                                                                                                                                                                                                                                                                                                                                                                 |



 

Andere Fehlercodes sind in [D3DERR enthalten.](d3derr.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D-Konstanten](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 




