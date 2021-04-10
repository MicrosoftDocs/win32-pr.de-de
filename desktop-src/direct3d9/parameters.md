---
description: Parameter sind Effekt Variablen.
ms.assetid: vs|directx_sdk|~\parameters.htm
title: Parameter (Direct3D 9)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e5c78a4f6c0518c99b61be10b721d98b17630ab
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125582"
---
# <a name="parameters-direct3d-9"></a>Parameter (Direct3D 9)

Parameter sind Effekt Variablen.

## <a name="syntax"></a>Syntax

*Verwendungstyp-ID* \[ : Ausdruck für *semantische* \] \[ < *Anmerkung (en)* > \] \[ =   \] ;

Parameter können von der Anwendung gelesen und mit [**ID3DXEffect**](id3dxeffect.md) oder [**ID3DXEffectCompiler**](id3dxeffectcompiler.md)geschrieben werden.

Auf Parameter kann in Funktionen und in Techniken (insbesondere auf der rechten Seite von Zustands Zuweisungen) verwiesen werden.



| Element                                                                                 | BESCHREIBUNG                                                                                                                                                     |
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="usage"></span><span id="USAGE"></span>*ungs*<br/>                   | Bereich des Parameters. Weitere Informationen finden Sie unter [Verwendungen und Literale (Direct3D 9)](usages-and-literals.md).<br/>                                                             |
| <span id="type"></span><span id="TYPE"></span>*Sorte*<br/>                      | Jeder gültige [Verweis für den HLSL](../direct3dhlsl/dx-graphics-hlsl-reference.md) -Typ.<br/>                                                                        |
| <span id="ID"></span><span id="id"></span>*Name*<br/>                            | Eine eindeutige Bezeichnung.<br/>                                                                                                                                       |
| <span id="semantic"></span><span id="SEMANTIC"></span>*tischer*<br/>          | Ein Tag, das folgende Bezeichnerregeln angibt, die in der Regel die Verwendung des Parameters angeben Muss ein bestimmter Typ sein.<br/>                                     |
| <span id="annotations"></span><span id="ANNOTATIONS"></span>*Anmerkungen*<br/> | NULL oder mehr Teile Benutzer spezifischer Informationen. Kann ein beliebiger Typ sein. Weitere [Informationen finden Sie unter Hinzufügen von Informationen zu Effekt Parametern mit Anmerkungen](using-an-effect.md).<br/> |
| <span id="expression"></span><span id="EXPRESSION"></span>*Begriff*<br/>    | Initialisiert den Wert des Parameters. Weitere Informationen finden Sie unter [Ausdrücke (Direct3D 9)](expressions.md).<br/>                                                                  |



 

Parameter können mit jedem gültigen [Verweis für den HLSL](../direct3dhlsl/dx-graphics-hlsl-reference.md) -Ausdruck initialisiert werden, der auf einen Literalwert reduziert wird.

Parameter Werte werden nicht durch die Ausführung von Zustands Zuweisungs-oder Funktionsaufrufen geändert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Effekt Format](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 
