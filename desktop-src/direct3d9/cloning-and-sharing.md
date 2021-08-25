---
description: Klonen und Freigeben (Direct3D 9)
ms.assetid: 1dabe611-bf3b-49bf-99ab-dbdfd343f885
title: Klonen und Freigeben (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96add856c6e3c675cbf3ac225d39517214ed9dc002abded6f4f7f9f75d4736bc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119857700"
---
# <a name="cloning-and-sharing-direct3d-9"></a>Klonen und Freigeben (Direct3D 9)

## <a name="cloning-parameters"></a>Klonparameter

Beim Klonen gelten die folgenden Einschränkungen.

-   Klone erben den Pool des ursprünglichen Effekts. Weitere Informationen finden Sie im Abschnitt Freigabeparameter.
-   Klone erben die Techniken, Durchläufe, Parameter und Anmerkungen des ursprünglichen Effekts (einschließlich aller Anmerkungen, die mit [**ID3DXEffect**](id3dxeffect.md)hinzugefügt wurden).
-   Klone erben die dynamisch hinzugefügten Anmerkungen des ursprünglichen Effekts.
-   Beim Klonen auf einem neuen Gerät tritt ein Fehler auf, wenn der Pool des ursprünglichen Effekts nicht **NULL** war und der ursprüngliche Effekt einen freigegebenen geräteabhängigen Parameter (z. B. eine Textur oder einen Shader) enthielt.

## <a name="sharing-parameters"></a>Freigeben von Parametern

Ein Pool ist ein Puffer, der Effektparameter zwischen verschiedenen Effekten teilt. Um einem Pool Parameter hinzuzufügen, geben Sie eine freigegebene Nutzung an, wenn der Effekt erstellt wird.

Für einen Pool gelten die folgenden Einschränkungen.

-   Ein Parameter wird dem Pool hinzugefügt, wenn dem Pool zum ersten Mal ein Effekt hinzugefügt wird, der diesen (freigegebenen) Parameter enthält.
-   Ein Pool ruft Anfangswerte aus dem ersten freigegebenen Parameter ab. -Parameter, die anschließend freigegeben werden, erhalten ihre Werte aus dem Pool.
-   Ein Parameter wird aus dem Pool gelöscht, wenn alle Auswirkungsverweise auf den freigegebenen Parameter freigegeben werden.
-   Alle Effekte im Pool, die den gleichen (freigegebenen) geräteabhängigen Parameter enthalten, müssen dasselbe Gerät aufweisen.

**NULL** kann verwendet werden, um keinen Pool anzugeben. In diesem Fall werden keine Parameter freigegeben. Dies ist fast gleichbedeutend mit der Angabe eines eindeutigen Pools nur für diesen Effekt. Der einzige Unterschied besteht darin, dass der Klon beim Klonen des Effekts seine freigegebenen Parameter nicht mit dem Original gemeinsam verwendet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Effektformat](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 



