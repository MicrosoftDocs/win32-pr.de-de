---
title: D3DCOMPILE-Konstanten (D3DCompiler. h)
description: Die D3DCOMPILE-Konstanten geben an, wie der Compiler den HLSL-Code kompiliert.
ms.assetid: 039627DD-D6A4-4EA3-8E91-D2A20770E6FF
topic_type:
- apiref
api_name:
- D3DCOMPILE_DEBUG
- D3DCOMPILE_SKIP_VALIDATION
- D3DCOMPILE_SKIP_OPTIMIZATION
- D3DCOMPILE_PACK_MATRIX_ROW_MAJOR
- D3DCOMPILE_PACK_MATRIX_COLUMN_MAJOR
- D3DCOMPILE_PARTIAL_PRECISION
- D3DCOMPILE_FORCE_VS_SOFTWARE_NO_OPT
- D3DCOMPILE_FORCE_PS_SOFTWARE_NO_OPT
- D3DCOMPILE_NO_PRESHADER
- D3DCOMPILE_AVOID_FLOW_CONTROL
- D3DCOMPILE_PREFER_FLOW_CONTROL
- D3DCOMPILE_ENABLE_STRICTNESS
- D3DCOMPILE_ENABLE_BACKWARDS_COMPATIBILITY
- D3DCOMPILE_IEEE_STRICTNESS
- D3DCOMPILE_OPTIMIZATION_LEVEL0
- D3DCOMPILE_OPTIMIZATION_LEVEL1
- D3DCOMPILE_OPTIMIZATION_LEVEL2
- D3DCOMPILE_OPTIMIZATION_LEVEL3
- D3DCOMPILE_WARNINGS_ARE_ERRORS
- D3DCOMPILE_RESOURCES_MAY_ALIAS
- D3DCOMPILE_ENABLE_UNBOUNDED_DESCRIPTOR_TABLES
- D3DCOMPILE_ALL_RESOURCES_BOUND
api_location:
- D3DCompiler.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfd396eef06260ae879a3bb816d0bd89a078ea53
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219453"
---
# <a name="d3dcompile-constants"></a>D3DCOMPILE-Konstanten

Die D3DCOMPILE-Konstanten geben an, wie der Compiler den HLSL-Code kompiliert.

<dl> <dt>

<span id="D3DCOMPILE_DEBUG"></span><span id="d3dcompile_debug"></span>**D3DCOMPILE \_ Debuggen**
</dt> <dd> <dl> <dt>

(1 << 0)
</dt> <dt>



Weist den Compiler an, Debugdateien/Zeilen-/Typ-/Symbolinformationen in den Ausgabe Code einzufügen.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_SKIP_VALIDATION"></span><span id="d3dcompile_skip_validation"></span>**D3DCOMPILE \_ über \_ Prüfung überspringen**
</dt> <dd> <dl> <dt>

(1 << 1)
</dt> <dt>



Weist den Compiler an, den generierten Code nicht anhand bekannter Funktionen und Einschränkungen zu validieren. Es wird empfohlen, diese Konstante nur mit Shadern zu verwenden, die in der Vergangenheit erfolgreich kompiliert wurden. DirectX überprüft Shader immer, bevor Sie auf ein Gerät festgelegt werden.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_SKIP_OPTIMIZATION"></span><span id="d3dcompile_skip_optimization"></span>**D3DCOMPILE \_ Skip- \_ Optimierung**
</dt> <dd> <dl> <dt>

(1 << 2)
</dt> <dt>



Weist den Compiler an, während der Codegenerierung Optimierungsschritte zu überspringen. Es wird empfohlen, diese Konstante nur für Debugzwecke festzulegen.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_PACK_MATRIX_ROW_MAJOR"></span><span id="d3dcompile_pack_matrix_row_major"></span>**D3DCOMPILE \_ Paket \_ Matrix \_ Zeile \_ Hauptversion**
</dt> <dd> <dl> <dt>

(1 << 3)
</dt> <dt>



Weist den Compiler an, Matrizen in der Zeilen Hauptreihenfolge für die Eingabe und Ausgabe aus dem Shader zu verpacken.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_PACK_MATRIX_COLUMN_MAJOR"></span><span id="d3dcompile_pack_matrix_column_major"></span>**D3DCOMPILE \_ Paket- \_ Matrix \_ Spalte \_ Hauptversion**
</dt> <dd> <dl> <dt>

(1 << 4)
</dt> <dt>



Weist den Compiler an, Matrizen in der Spalte-Haupt Reihenfolge für die Eingabe und Ausgabe aus dem Shader zu verpacken. Diese Art von Verpackung ist in der Regel effizienter, da eine Reihe von Punkt Produkten dann eine Vektor Matrix Multiplikation durchführen kann.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_PARTIAL_PRECISION"></span><span id="d3dcompile_partial_precision"></span>**D3DCOMPILE \_ partielle \_ Genauigkeit**
</dt> <dd> <dl> <dt>

(1 << 5)
</dt> <dt>



Weist den Compiler an, alle Berechnungen mit teilweiser Genauigkeit auszuführen. Wenn Sie diese Konstante festlegen, kann der kompilierte Code auf Hardware möglicherweise schneller ausgeführt werden.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_FORCE_VS_SOFTWARE_NO_OPT"></span><span id="d3dcompile_force_vs_software_no_opt"></span>**D3DCOMPILE \_ Force \_ vs \_ Software \_ No \_ Opt**
</dt> <dd> <dl> <dt>

(1 << 6)
</dt> <dt>



Weist den Compiler an, einen Vertex-Shader für das nächsthöhere Shader-Profil zu kompilieren. Diese Konstante schaltet Debuggen und Optimierungen aus.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_FORCE_PS_SOFTWARE_NO_OPT"></span><span id="d3dcompile_force_ps_software_no_opt"></span>**D3DCOMPILE \_ Erzwingen von \_ PS- \_ Software \_ Nein \_ Opt**
</dt> <dd> <dl> <dt>

(1 << 7)
</dt> <dt>



Weist den Compiler an, einen PixelShader für das nächste höchste Shader-Profil zu kompilieren. Diese Konstante schaltet auch Debuggen und Optimierungen deaktiviert.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_NO_PRESHADER"></span><span id="d3dcompile_no_preshader"></span>**D3DCOMPILE \_ kein \_ preshader**
</dt> <dd> <dl> <dt>

(1 << 8)
</dt> <dt>



Weist den Compiler an, preshaders zu deaktivieren. Wenn Sie diese Konstante festlegen, führt der Compiler keinen statischen Ausdruck für die Auswertung aus.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_AVOID_FLOW_CONTROL"></span><span id="d3dcompile_avoid_flow_control"></span>**D3DCOMPILE \_ Vermeidung der \_ Fluss \_ Steuerung**
</dt> <dd> <dl> <dt>

(1 << 9)
</dt> <dt>



Weist den Compiler an, keine Flow-steuerungskonstrukte zu verwenden, sofern möglich.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_PREFER_FLOW_CONTROL"></span><span id="d3dcompile_prefer_flow_control"></span>**D3DCOMPILE \_ bevorzugen der \_ Fluss \_ Steuerung**
</dt> <dd> <dl> <dt>

(1 << 10)
</dt> <dt>



Weist den Compiler an, Fluss Steuerungs Konstrukte zu verwenden, sofern möglich.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_ENABLE_STRICTNESS"></span><span id="d3dcompile_enable_strictness"></span>**D3DCOMPILE \_ Aktivieren von \_ strictivität**
</dt> <dd> <dl> <dt>

(1 << 11)
</dt> <dt>



Erzwingt eine strikte Kompilierung, die möglicherweise keine Legacy Syntax zulässt.

Standardmäßig deaktiviert der Compiler die strenge in der veralteten Syntax.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_ENABLE_BACKWARDS_COMPATIBILITY"></span><span id="d3dcompile_enable_backwards_compatibility"></span>**D3DCOMPILE-abwärts \_ \_ \_ Kompatibilität aktivieren**
</dt> <dd> <dl> <dt>

(1 << 12)
</dt> <dt>



Weist den Compiler an, ältere Shader für die Kompilierung in 5-0-Ziele zu aktivieren \_ .


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_IEEE_STRICTNESS"></span><span id="d3dcompile_ieee_strictness"></span>**D3DCOMPILE \_ IEEE- \_ strenge**
</dt> <dd> <dl> <dt>

(1 << 13)
</dt> <dt>



Erzwingt die IEEE Strict-Kompilierung.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_OPTIMIZATION_LEVEL0"></span><span id="d3dcompile_optimization_level0"></span>**D3DCOMPILE- \_ Optimierung \_ LEVEL0**
</dt> <dd> <dl> <dt>

(1 << 14)
</dt> <dt>



Weist den Compiler an, die niedrigste Optimierungs Ebene zu verwenden. Wenn Sie diese Konstante festlegen, erzeugt der Compiler möglicherweise langsameren Code, erzeugt den Code aber schneller. Legen Sie diese Konstante fest, wenn Sie den Shader iterativ entwickeln.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_OPTIMIZATION_LEVEL1"></span><span id="d3dcompile_optimization_level1"></span>**D3DCOMPILE- \_ Optimierung \_ Level1**
</dt> <dd> <dl> <dt>

0
</dt> <dt>



Weist den Compiler an, die zweite niedrigste Optimierungs Ebene zu verwenden.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_OPTIMIZATION_LEVEL2"></span><span id="d3dcompile_optimization_level2"></span>**D3DCOMPILE- \_ Optimierung \_ Level2**
</dt> <dd> <dl> <dt>

((1 << 14) \| (1 << 15))
</dt> <dt>



Weist den Compiler an, die zweithöchste Optimierungs Ebene zu verwenden.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_OPTIMIZATION_LEVEL3"></span><span id="d3dcompile_optimization_level3"></span>**D3DCOMPILE- \_ Optimierung \_ LEVEL3**
</dt> <dd> <dl> <dt>

(1 << 15)
</dt> <dt>



Weist den Compiler an, die höchste Optimierungs Ebene zu verwenden. Wenn Sie diese Konstante festlegen, erzeugt der Compiler den bestmöglichen Code, kann aber erheblich länger dauern. Legen Sie diese Konstante für endgültige Builds einer Anwendung fest, wenn die Leistung der wichtigste Faktor ist.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_WARNINGS_ARE_ERRORS"></span><span id="d3dcompile_warnings_are_errors"></span>**D3DCOMPILE- \_ Warnungen \_ sind \_ Fehler**
</dt> <dd> <dl> <dt>

(1 << 18)
</dt> <dt>



Weist den Compiler an, alle Warnungen als Fehler zu behandeln, wenn der Shader-Code kompiliert wird. Es wird empfohlen, diese Konstante für neuen Shader-Code zu verwenden, damit Sie alle Warnungen auflösen und die Anzahl von schwer zu suchenden Code Fehlern verringern können.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_RESOURCES_MAY_ALIAS"></span><span id="d3dcompile_resources_may_alias"></span>**D3DCOMPILE \_ - \_ Ressourcen \_ Alias**
</dt> <dd> <dl> <dt>

(1 << 19)
</dt> <dt>



Weist den Compiler an, davon auszugehen, dass für CS 5 0 ein Alias für nicht geordnete Zugriffs Sichten (UAVs) und Shader-Ressourcen Sichten (Srvs) möglich ist \_ \_ .

> [!Note]  
> Diese Compilerkonstante ist neu, beginnend mit dem D3dcompiler- \_47.dll.

 


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_ENABLE_UNBOUNDED_DESCRIPTOR_TABLES"></span><span id="d3dcompile_enable_unbounded_descriptor_tables"></span>**D3DCOMPILE \_ Aktivieren von \_ ungebundenen \_ \_ deskriptortabellen**
</dt> <dd> <dl> <dt>

(1 << 20)
</dt> <dt>



Weist den Compiler an, ungebundene deskriptortabellen zu aktivieren.

> [!Note]  
> Diese Compilerkonstante ist neu, beginnend mit dem D3dcompiler- \_47.dll.

 


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_ALL_RESOURCES_BOUND"></span><span id="d3dcompile_all_resources_bound"></span>**D3DCOMPILE \_ alle \_ Ressourcen \_ gebunden**
</dt> <dd> <dl> <dt>

(1 << 21)
</dt> <dt>



Weist den Compiler an, sicherzustellen, dass alle Ressourcen gebunden sind.

> [!Note]  
> Diese Compilerkonstante ist neu, beginnend mit dem D3dcompiler- \_47.dll.

 


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3DCompiler. h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[D3DCompiler-Konstanten](dx-graphics-d3dcompiler-reference-constants.md)
</dt> </dl>

 

 





