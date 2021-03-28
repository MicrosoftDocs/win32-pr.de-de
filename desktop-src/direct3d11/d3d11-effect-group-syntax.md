---
title: Effekt Gruppen Syntax (Direct3D 11)
description: Eine Effekt Gruppe wird mit der in diesem Abschnitt beschriebenen Syntax deklariert.
ms.assetid: f6695ae5-198f-45bd-853b-8c02fabd0c39
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9221341810990801f1ed07005e0dcb917df42360
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104472045"
---
# <a name="effect-group-syntax-direct3d-11"></a>Effekt Gruppen Syntax (Direct3D 11)

Eine Effekt Gruppe wird mit der in diesem Abschnitt beschriebenen Syntax deklariert.


```
fxgroup GroupName  [ <Annotations > ]
{
    TechniqueVersion TechniqueName [ <Annotations > ] 
    { 
       ...
    } 
    TechniqueVersion TechniqueName [ <Annotations > ] 
    { 
       ...
    } 
}



```



## <a name="parameters"></a>Parameter



| Element                                                                                                                                                                           | BESCHREIBUNG                                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="fxgroup"></span><span id="FXGROUP"></span>fxgroup<br/>                                                                                                         | erforderliche-Schlüsselwort.<br/>                                                                                                                                                                                                         |
| <span id="GroupName"></span><span id="groupname"></span><span id="GROUPNAME"></span>GroupName<br/>                                                                       | Erforderlich. Eine ASCII-Zeichenfolge, die den Namen der Effekt Gruppe eindeutig identifiziert. Anders als bei Techniken müssen Gruppen über Namen verfügen, um sicherzustellen, dass Techniken einen eindeutigen Bezeichner aufweisen (siehe Abschnitt "Gruppen und Techniken" weiter unten).<br/> |
| <span id="_______________Annotations__"></span><span id="_______________annotations__"></span><span id="_______________ANNOTATIONS__"></span> < Anmerkungen ><br/> | \[in \] optional. Ein oder mehrere Teile der vom Benutzer bereitgestellten Informationen (Metadaten), die vom Effektsystem ignoriert werden. Informationen zur Syntax finden Sie unter Annotation-Syntax (Direct3D 11). <br/>                                                      |
| <span id="TechniqueVersion"></span><span id="techniqueversion"></span><span id="TECHNIQUEVERSION"></span>Techniqueversion<br/>                                           | Entweder "technique10" oder "technique11". Bei Techniken, die neue Funktionen für Direct3D 11 verwenden (5 \_ 0 Shader, bindinterfaces usw.), muss "technique11" verwendet werden.<br/>                                                                 |
| <span id="TechniqueName"></span><span id="techniquename"></span><span id="TECHNIQUENAME"></span>Techniquename<br/>                                                       | Optional. Eine ASCII-Zeichenfolge, die den Namen der Effekt Technik eindeutig identifiziert. <br/>                                                                                                                                    |



 

## <a name="groups-and-techniques"></a>Gruppen und Techniken

Um die Kompatibilität mit den Effekten von FX \_ 4 \_ 0 aufrechtzuerhalten, sind Gruppen optional. Es gibt eine implizite Gruppe mit NULL-Namen, die alle globalen Techniken umfasst.

Betrachten Sie das folgende Beispiel:


```
technique11 GlobalTech
{
}
fxgroup Group1
{
     technique11 Tech1 { ... }
     technique11 Tech2 { ... }
}
fxgroup Group2
{
     technique11 Tech1 { ... }
     technique11 Tech2 { ... }
}
```



In C++ kann eine Technik anhand des Namens auf zwei Arten erhalten werden. Die folgenden Befehle werden die offensichtlichen Techniken finden:


```
pEffect->GetTechniqueByName( "GlobalTech" );
pEffect->GetTechniqueByName( "|GlobalTech" );
pEffect->GetTechniqueByName( "Group1|Tech1" );
pEffect->GetTechniqueByName( "Group1|Tech2" );
pEffect->GetTechniqueByName( "Group2|Tech1" );
pEffect->GetTechniqueByName( "Group2|Tech2" );
pEffect->GetGroupByName("Group1")->GetTechniqueByName( "Tech1" );
pEffect->GetGroupByName("Group1")->GetTechniqueByName( "Tech2" );
pEffect->GetGroupByName("Group2")->GetTechniqueByName( "Tech1" );
pEffect->GetGroupByName("Group2")->GetTechniqueByName( "Tech2" );
```



Um sicherzustellen, dass [**ID3DX11Effect:: gettechniquebyname**](id3dx11effect-gettechniquebyname.md) ähnlich wie die Auswirkungen 10 funktioniert, müssen alle definierten Gruppen einen Namen haben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Effekt Format](d3d11-effect-format.md)
</dt> <dt>

[Effekt Technik Syntax (Direct3D 11)](d3d11-effect-technique-syntax.md)
</dt> </dl>

 

 





