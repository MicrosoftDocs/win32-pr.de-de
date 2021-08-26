---
title: Syntax der Effektgruppe (Direct3D 11)
description: Eine Effektgruppe wird mit der in diesem Abschnitt beschriebenen Syntax deklariert.
ms.assetid: f6695ae5-198f-45bd-853b-8c02fabd0c39
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c1b2c72b0a67a31911a0f2c9f9ae6ac0e9e20463a850c303dab4a208401d1c4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120069750"
---
# <a name="effect-group-syntax-direct3d-11"></a>Syntax der Effektgruppe (Direct3D 11)

Eine Effektgruppe wird mit der in diesem Abschnitt beschriebenen Syntax deklariert.


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
| <span id="fxgroup"></span><span id="FXGROUP"></span>fxgroup<br/>                                                                                                         | equired-Schlüsselwort.<br/>                                                                                                                                                                                                         |
| <span id="GroupName"></span><span id="groupname"></span><span id="GROUPNAME"></span>Groupname<br/>                                                                       | Erforderlich. Eine ASCII-Zeichenfolge, die den Namen der Effektgruppe eindeutig identifiziert. Im Gegensatz zu Techniken müssen Gruppen Namen haben, um sicherzustellen, dass Techniken einen eindeutigen Bezeichner haben (siehe Abschnitt Gruppen und Techniken weiter unten).<br/> |
| <span id="_______________Annotations__"></span><span id="_______________annotations__"></span><span id="_______________ANNOTATIONS__"></span> < Anmerkungen ><br/> | \[in \] Optional. Mindestens ein Teil der vom Benutzer bereitgestellten Informationen (Metadaten), die vom Effektsystem ignoriert werden. Syntax finden Sie unter Anmerkungssyntax (Direct3D 11). <br/>                                                      |
| <span id="TechniqueVersion"></span><span id="techniqueversion"></span><span id="TECHNIQUEVERSION"></span>TechniqueVersion<br/>                                           | Entweder "technique10" oder "technique11". Techniken, die neue Funktionen von Direct3D 11 (5 \_ 0 Shader, BindInterfaces usw.) verwenden, müssen "technique11" verwenden.<br/>                                                                 |
| <span id="TechniqueName"></span><span id="techniquename"></span><span id="TECHNIQUENAME"></span>TechniqueName<br/>                                                       | Optional. Eine ASCII-Zeichenfolge, die den Namen der Effekttechnik eindeutig identifiziert. <br/>                                                                                                                                    |



 

## <a name="groups-and-techniques"></a>Gruppen und Techniken

Um die Kompatibilität mit fx \_ 4 \_ 0-Effekten zu gewährleisten, sind Gruppen optional. Es gibt eine implizite NULL-benannte Gruppe, die alle globalen Techniken umgibt.

Betrachten Sie das folgenden Beispiel:


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



In C++ gibt es zwei Möglichkeiten, eine Technik nach Namen zu erhalten. Die folgenden Befehle finden die offensichtlichen Techniken:


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



Um sicherzustellen, dass [**ID3DX11Effect::GetTechniqueByName**](id3dx11effect-gettechniquebyname.md) ähnlich wie Effects 10 funktioniert, müssen alle definierten Gruppen einen Namen haben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Effect-Format](d3d11-effect-format.md)
</dt> <dt>

[Effect Technique Syntax (Direct3D 11)](d3d11-effect-technique-syntax.md)
</dt> </dl>

 

 





