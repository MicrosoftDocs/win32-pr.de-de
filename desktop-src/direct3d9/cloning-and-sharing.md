---
description: Klonen und freigeben (Direct3D 9)
ms.assetid: 1dabe611-bf3b-49bf-99ab-dbdfd343f885
title: Klonen und freigeben (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 983e674af4cdd24e21fcc2517eb8a32d6aec291c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861631"
---
# <a name="cloning-and-sharing-direct3d-9"></a>Klonen und freigeben (Direct3D 9)

## <a name="cloning-parameters"></a>Klonen von Parametern

Für das Klonen gelten die folgenden Einschränkungen.

-   Klone erben den ursprünglichen Effekt Pool. Weitere Informationen finden Sie im Abschnitt Freigabe Parameter.
-   Klone erben die Techniken, Pass, Parameter und Anmerkungen des ursprünglichen Effekts (einschließlich aller Anmerkungen, die mit [**ID3DXEffect**](id3dxeffect.md)hinzugefügt wurden).
-   Klone erben die dynamisch hinzugefügten Anmerkungen des ursprünglichen Effekts.
-   Das Klonen auf einem neuen Gerät schlägt fehl, wenn der Pool des ursprünglichen Effekts nicht **null** war und der ursprüngliche Effekt einen freigegebenen geräteabhängigen Parameter enthielt (z. b. eine Textur oder ein Shader).

## <a name="sharing-parameters"></a>Freigabe Parameter

Ein Pool ist ein Puffer, der Effektparameter zwischen unterschiedlichen Effekten freigibt. Zum Hinzufügen von Parametern zu einem Pool geben Sie eine freigegebene Verwendung an, wenn der Effekt erstellt wird.

Für einen Pool gelten die folgenden Einschränkungen.

-   Dem Pool wird ein Parameter hinzugefügt, wenn dem Pool das erste Mal ein Effekt hinzugefügt wird, der diesen Parameter (Shared) enthält.
-   Ein Pool ruft Anfangswerte aus dem ersten freigegebenen Parameter ab. Parameter, die anschließend freigegeben werden, erhalten ihre Werte aus dem Pool.
-   Ein Parameter wird aus dem Pool gelöscht, wenn alle Auswirkung-Verweise auf den freigegebenen Parameter freigegeben werden.
-   Alle Effekte im Pool, die denselben (gemeinsam genutzten) geräteabhängigen Parameter enthalten, müssen das gleiche Gerät aufweisen.

**Null** kann verwendet werden, um keinen Pool anzugeben. in diesem Fall werden keine Parameter freigegeben. Dies entspricht fast der Angabe eines eindeutigen Pools nur für diesen Effekt. Der einzige Unterschied besteht darin, dass der Klon seine freigegebenen Parameter nicht mit dem Original gemeinsam verwendet, wenn der Effekt geklont wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Effekt Format](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 



