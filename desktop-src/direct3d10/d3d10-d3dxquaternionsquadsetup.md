---
description: Richtet Steuerungs Punkte für die sphärische Quadrangle-interpolung ein.
ms.assetid: c66227bd-8cc1-4173-9dc2-5aab9d57301e
title: D3DXQuaternionSquadSetup-Funktion (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionSquadSetup
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 4a0683bce3642b0300e68be348d8aed39b3c333d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355829"
---
# <a name="d3dxquaternionsquadsetup-function-d3dx10mathh"></a>D3DXQuaternionSquadSetup-Funktion (D3DX10Math. h)

Richtet Steuerungs Punkte für die sphärische Quadrangle-interpolung ein.

## <a name="syntax"></a>Syntax


```C++
void D3DXQuaternionSquadSetup(
  _In_       D3DXQUATERNION *pAOut,
  _In_       D3DXQUATERNION *pBOut,
  _In_       D3DXQUATERNION *pCOut,
  _In_ const D3DXQUATERNION *pQ0,
  _In_ const D3DXQUATERNION *pQ1,
  _In_ const D3DXQUATERNION *pQ2,
  _In_ const D3DXQUATERNION *pQ3
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Auslagern* \[ in\]
</dt> <dd>

Typ: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***

Zeiger auf "aout".

</dd> <dt>

*pbout* \[ in\]
</dt> <dd>

Typ: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***

Zeiger auf "BOut".

</dd> <dt>

*pcout* \[ in\]
</dt> <dd>

Typ: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***

Zeiger auf "cout".

</dd> <dt>

*pQ0* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***

Zeiger auf den Eingabe Steuerungspunkt, q0.

</dd> <dt>

*pQ1* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***

Zeiger auf den Eingabe Steuerungspunkt (Q1).

</dd> <dt>

*pQ2* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***

Zeiger auf den Eingabe Steuerungspunkt (Q2).

</dd> <dt>

*pQ3* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***

Zeiger auf den Eingabe Steuerungspunkt (Q3).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Keine.

## <a name="remarks"></a>Bemerkungen

Diese Funktion nimmt vier Steuerungs Punkte an, die für die Eingaben pQ0, pQ1, pQ2 und pQ3 bereitgestellt werden. Die-Funktion ändert dann diese Werte, um eine Kurve zu finden, die entlang des kürzesten Pfads verläuft. Die Werte von Q0, Q2 und Q3 werden wie unten dargestellt berechnet.


```
q0 = |Q0 + Q1| < |Q0 - Q1| ? -Q0 : Q0
q2 = |Q1 + Q2| < |Q1 - Q2| ? -Q2 : Q2
q3 = |Q2 + Q3| < |Q2 - Q3| ? -Q3 : Q3
```



Wenn Sie die neuen Q-Werte berechnet haben, werden die Werte für "aout", "BOut" und "cout" wie folgt berechnet:

Aout = Q1 \* e<sup> \[ -0,25 \ \* (\ LN \[ Exp (Q1) \* Q2 \] \ + \ LN \[ Exp (Q1) \* q0 \] \) \ \] </sup>

BOut = Q2 \* e<sup> \[ -0,25 \ \* (\ LN \[ Exp (Q2) \* Q3 \] \ + \ LN \[ Exp (Q2) \* Q1 \] \) \ \] </sup>

Cout = Q2

> [!Note]  
> LN ist die API-Methode [**D3DXQuaternionLn**](d3d10-d3dxquaternionln.md) und Exp ist die API-Methode [**D3DXQuaternionExp**](d3d10-d3dxquaternionexp.md).

 

Verwenden Sie [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) für eine beliebige Quaternion-Eingabe, die nicht bereits normalisiert ist.

### <a name="examples"></a>Beispiele

Im folgenden Beispiel wird gezeigt, wie ein Satz von Quaternion-Schlüsseln (q0, Q1, Q2, Q3) zum Berechnen der inneren Quadranten Punkte (a, B, C) verwendet wird. Dadurch wird sichergestellt, dass die Tangenten in angrenzenden Segmenten kontinuierlich sind.


```
      A     B
Q0    Q1    Q2    Q3
```



Im folgenden Codebeispiel wird veranschaulicht, wie Sie zwischen Q1 und Q2 interpolieren können.


```
// Rotation about the z-axis
D3DXQUATERNION Q0 = D3DXQUATERNION(0,  0, 0.707f, -.707f);
D3DXQUATERNION Q1 = D3DXQUATERNION(0,  0, 0.000f, 1.000f);
D3DXQUATERNION Q2 = D3DXQUATERNION(0,  0, 0.707f, 0.707f);
D3DXQUATERNION Q3 = D3DXQUATERNION(0,  0, 1.000f, 0.000f);
D3DXQUATERNION A, B, C, Qt;
FLOAT time = 0.5f;

D3DXQuaternionSquadSetup(&A, &B, &C, &Q0, &Q1, &Q2, &Q3);
D3DXQuaternionSquad(&Qt, &Q1, &A, &B, &C, time);
```



> [!Note]
>
> -   C ist +/-Q2, abhängig vom Ergebnis der Funktion.
> -   Qt ist das Ergebnis der-Funktion.
>
> Das Ergebnis ist eine Drehung von 45 Grad um die z-Achse für time = 0,5.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10Math. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx10. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mathematische Funktionen](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
