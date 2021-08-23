---
description: Parameter sind Effektvariablen.
ms.assetid: vs|directx_sdk|~\parameters.htm
title: Parameter (Direct3D 9)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc28d1410180aac54daf306fe586694cfa1b7f4123403efc606a77385d088326
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119606680"
---
# <a name="parameters-direct3d-9"></a>Parameter (Direct3D 9)

Parameter sind Effektvariablen.

## <a name="syntax"></a>Syntax

*Verwendungstyp-ID:* \[ *semantischer* \] \[ <  > \] \[ =  *Anmerkungsausdruck* \] ;

Parameter können von der Anwendung mit [**ID3DXEffect**](id3dxeffect.md) oder [**ID3DXEffectCompiler**](id3dxeffectcompiler.md)gelesen und in diese geschrieben werden.

Auf Parameter kann in Funktionen und Techniken verwiesen werden (insbesondere auf der rechten Seite von Zustandszuweisungen).



| Element                                                                                 | Beschreibung                                                                                                                                                     |
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="usage"></span><span id="USAGE"></span>*Verwendung*<br/>                   | Bereich des Parameters. Weitere [Informationen finden Sie unter Usages and Literals (Direct3D 9) (Verwendungen und Literale (Direct3D 9)).](usages-and-literals.md)<br/>                                                             |
| <span id="type"></span><span id="TYPE"></span>*Typ*<br/>                      | Ein [gültiger Verweis für den HLSL-Typ.](../direct3dhlsl/dx-graphics-hlsl-reference.md)<br/>                                                                        |
| <span id="ID"></span><span id="id"></span>*Id*<br/>                            | Eine eindeutige Bezeichnung.<br/>                                                                                                                                       |
| <span id="semantic"></span><span id="SEMANTIC"></span>*Semantische*<br/>          | Ein Tag nach Bezeichnerregeln, das in der Regel die Verwendung des Parameters angibt. Muss ein bestimmter Typ sein.<br/>                                     |
| <span id="annotations"></span><span id="ANNOTATIONS"></span>*Anmerkungen*<br/> | Keine oder mehrere Teile von benutzerspezifischen Informationen. Kann ein beliebiger Typ sein. Weitere [Informationen finden Sie unter Hinzufügen von Informationen zu Effektparametern mit Anmerkungen.](using-an-effect.md)<br/> |
| <span id="expression"></span><span id="EXPRESSION"></span>*Ausdruck*<br/>    | Initialisiert den Wert des Parameters. Siehe [Ausdrücke (Direct3D 9).](expressions.md)<br/>                                                                  |



 

Parameter können mit jedem gültigen Verweis für [HLSL-Ausdruck](../direct3dhlsl/dx-graphics-hlsl-reference.md) initialisiert werden, der auf einen Literalwert reduziert wird.

Parameterwerte werden durch die Ausführung von Zustandszuweisungen oder Funktionsaufrufen nicht geändert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Effect-Format](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 
