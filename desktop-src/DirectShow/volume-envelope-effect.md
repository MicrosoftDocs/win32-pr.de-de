---
description: Volumeumschlags Effekt
ms.assetid: 17b6d842-e79c-49b0-baa4-1535b4a2c6ae
title: Volumeumschlags Effekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9364b88b1928e533a031f0700cb8a2c44bc9822d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106357876"
---
# <a name="volume-envelope-effect"></a>Volumeumschlags Effekt

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Der volumeumschlags Effekt legt das Volume in einem Audiostream fest.

Klassen-ID (CLSID): {036a9790-C153-11d2-9ef7-006008039e37}

CLSID-Variablen Name: CLSID- \_ audmixer

Eigenschaften



| Eigenschaft | type   | Standard | BESCHREIBUNG                                                                                                           |
|----------|--------|---------|-----------------------------------------------------------------------------------------------------------------------|
| Volumen      | double | 1.0     | Volume als Prozentsatz des erstellten Volumes. Sie können Audioüberblendungen entwickeln, indem Sie diesen Eigenschafts Wert im Zeitverlauf variieren |



 

## <a name="remarks"></a>Bemerkungen

Jedes Objekt in einer Zeitachse kann höchstens einen volumeumschlags Effekt haben. In einer Komposition oder einer Gruppe wird der volumeumschlag vor allen anderen Audioeffekten unabhängig von seiner Priorität zuerst angewendet. In einer Quelle oder einer Spur wird der volumeeffekt entsprechend seiner Priorität angewendet.

 

 



