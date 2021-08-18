---
description: 'D3DXQuaternionSquadSetup-Funktion (D3DX10Math.h): Richtet Steuerungspunkte für die sphärische Quadrangleinterpolation ein.'
ms.assetid: c66227bd-8cc1-4173-9dc2-5aab9d57301e
title: D3DXQuaternionSquadSetup-Funktion (D3DX10Math.h)
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
ms.openlocfilehash: 94f6c3fbfa72a46132efe0b9a8057983728d161cc06ba0364019f9d39b4635fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118990980"
---
# <a name="d3dxquaternionsquadsetup-function-d3dx10mathh"></a>D3DXQuaternionSquadSetup-Funktion (D3DX10Math.h)

Richtet Steuerungspunkte für die sphärische Quadrangleinterpolation ein.

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

*pAOut* \[ In\]
</dt> <dd>

Typ: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***

Zeiger auf AOut.

</dd> <dt>

*pBOut* \[ In\]
</dt> <dd>

Typ: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***

Zeiger auf BOut.

</dd> <dt>

*pCOut* \[ In\]
</dt> <dd>

Typ: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***

Zeiger auf COut.

</dd> <dt>

*pQ0* \[ In\]
</dt> <dd>

Typ: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***

Zeiger auf den Eingabesteuerpunkt Q0.

</dd> <dt>

*pQ1* \[ In\]
</dt> <dd>

Typ: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***

Zeiger auf den Eingabesteuerpunkt Q1.

</dd> <dt>

*pQ2* \[ In\]
</dt> <dd>

Typ: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***

Zeiger auf den Eingabesteuerpunkt Q2.

</dd> <dt>

*pQ3* \[ In\]
</dt> <dd>

Typ: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***

Zeiger auf den Eingabesteuerpunkt Q3.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Keine.

## <a name="remarks"></a>Hinweise

Diese Funktion verwendet vier Steuerungspunkte, die für die Eingaben pQ0, pQ1, pQ2 und pQ3 bereitgestellt werden. Die Funktion ändert dann diese Werte, um eine Kurve zu finden, die entlang des kürzesten Pfads verläuft. Die Werte von q0, q2 und q3 werden wie unten dargestellt berechnet.


```
q0 = |Q0 + Q1| < |Q0 - Q1| ? -Q0 : Q0
q2 = |Q1 + Q2| < |Q1 - Q2| ? -Q2 : Q2
q3 = |Q2 + Q3| < |Q2 - Q3| ? -Q3 : Q3
```



Nachdem die neuen Q-Werte berechnet wurden, werden die Werte für AOut, BOut und COut wie folgt berechnet:

AOut = q1 \* e<sup> \[ -0.25\ \* (\ Ln \[ Exp(q1) \* q2 \] \ +\ Ln \[ Exp(q1) \* q0 \ \] )\ \] </sup>

BOut = q2 \* e<sup> \[ -0.25\ \* (\ Ln \[ Exp(q2) \* q3 \] \ +\ Ln \[ Exp(q2) \* q1 \ \] )\ \] </sup>

COut = q2

> [!Note]  
> Ln ist die API-Methode [**D3DXQuaternionLn,**](d3d10-d3dxquaternionln.md) und Exp ist die API-Methode [**D3DXQuaternionExp.**](d3d10-d3dxquaternionexp.md)

 

Verwenden Sie [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) für alle Quaternioneingaben, die noch nicht normalisiert sind.

### <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt, wie Sie einen Satz von Quaternionsschlüsseln (Q0, Q1, Q2, Q3) verwenden, um die inneren Quadranglepunkte (A, B, C) zu berechnen. Dadurch wird sichergestellt, dass die Tangenten über angrenzende Segmente hinweg kontinuierlich sind.


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
> -   C ist +/- Q2, abhängig vom Ergebnis der Funktion.
> -   Qt ist das Ergebnis der Funktion.
>
> Das Ergebnis ist eine Drehung von 45 Grad um die Z-Achse für die Zeit = 0,5.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10Math.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3DX10.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Mathematische Funktionen](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
