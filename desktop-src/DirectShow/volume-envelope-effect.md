---
description: Effekt "VolumeUmschlag"
ms.assetid: 17b6d842-e79c-49b0-baa4-1535b4a2c6ae
title: Effekt "VolumeUmschlag"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4ecb66914063596849522a0e4bb340fc84f7d80e5ea1113bfdae2d32e855d3b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119746950"
---
# <a name="volume-envelope-effect"></a>Effekt "VolumeUmschlag"

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Releases von Windows entfernt werden.\]

 

Der Effekt VolumeUmschlag legt das Volume in einem Audiostream fest.

Klassen-ID (CLSID): {036A9790-C153-11D2-9EF7-006008039E37}

CLSID-Variablenname: CLSID \_ AudMixer

Eigenschaften



| Eigenschaft | type   | Standard | Beschreibung                                                                                                           |
|----------|--------|---------|-----------------------------------------------------------------------------------------------------------------------|
| Vol      | double | 1.0     | Volume als Prozentsatz des erstellten Volumes. Sie können Audiowiedergaben erzeugen, indem Sie diesen Eigenschaftswert im Laufe der Zeit variieren. |



 

## <a name="remarks"></a>Hinweise

Jedes Objekt in einer Zeitachse kann höchstens einen Volumeumschlageffekt haben. In einer Komposition oder Gruppe wird der Volumeumschlag unabhängig von seiner Priorität zuerst vor anderen Audioeffekten angewendet. In einer Quelle oder einer Spur wird der Volumeeffekt entsprechend seiner Priorität angewendet.

 

 



