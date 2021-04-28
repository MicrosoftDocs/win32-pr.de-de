---
description: 'D3DXQuaternionSquadSetup-Funktion (D3dx9math.h): Richtet Steuerungspunkte für die sphärische Quadrangleinterpolation ein.'
ms.assetid: f800d457-8546-49a1-800e-e5c27af96710
title: D3DXQuaternionSquadSetup-Funktion (D3dx9math.h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1dcaa90380ec703b4b56458906ab8bd965d7568c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093948"
---
# <a name="d3dxquaternionsquadsetup-function-d3dx9mathh"></a>D3DXQuaternionSquadSetup-Funktion (D3dx9math.h)

Richtet Steuerungspunkte für die sphärische Quadrangleinterpolation ein.

## <a name="syntax"></a>Syntax


```C++
void D3DXQuaternionSquadSetup(
  _Out_       D3DXQUATERNION *pAOut,
  _Out_       D3DXQUATERNION *pBOut,
  _Out_       D3DXQUATERNION *pCOut,
  _In_  const D3DXQUATERNION *pQ0,
  _In_  const D3DXQUATERNION *pQ1,
  _In_  const D3DXQUATERNION *pQ2,
  _In_  const D3DXQUATERNION *pQ3
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pAOut* \[ out\]
</dt> <dd>

Typ: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***

Zeiger auf AOut.

</dd> <dt>

*pBOut* \[ out\]
</dt> <dd>

Typ: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***

Zeiger auf BOut.

</dd> <dt>

*pCOut* \[ out\]
</dt> <dd>

Typ: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***

Zeiger auf COut.

</dd> <dt>

*pQ0* \[ In\]
</dt> <dd>

Typ: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***

Zeiger auf den Eingabesteuerpunkt Q0.

</dd> <dt>

*pQ1* \[ In\]
</dt> <dd>

Typ: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***

Zeiger auf den Eingabesteuerpunkt Q1.

</dd> <dt>

*pQ2* \[ In\]
</dt> <dd>

Typ: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***

Zeiger auf den Eingabesteuerungspunkt Q2.

</dd> <dt>

*pQ3* \[ In\]
</dt> <dd>

Typ: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***

Zeiger auf den Eingabesteuerungspunkt Q3.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Keine.

## <a name="remarks"></a>Bemerkungen

Diese Funktion nimmt vier Kontrollpunkte an, die für die Eingaben pQ0, pQ1, pQ2 und pQ3 bereitgestellt werden. Die Funktion ändert dann diese Werte, um eine Kurve zu finden, die entlang des kürzesten Pfads fließt. Die Werte für q0, q2 und q3 werden wie unten dargestellt berechnet.


```
q0 = |Q0 + Q1| < |Q0 - Q1| ? -Q0 : Q0
q2 = |Q1 + Q2| < |Q1 - Q2| ? -Q2 : Q2
q3 = |Q2 + Q3| < |Q2 - Q3| ? -Q3 : Q3
```



Nachdem die neuen Q-Werte berechnet wurden, werden die Werte für AOut, BOut und COut wie folgt berechnet:

AOut = q1 \* e<sup> \[ -0,25\ \* (\ Ln \[ Exp(q1) \* q2 \] \ +\ Ln \[ Exp(q1) \* q0 \ \] )\ \] </sup>

BOut = q2 \* e<sup> \[ -0,25\ \* (\ Ln \[ Exp(q2) \* q3 \] \ +\ Ln \[ Exp(q2) \* q1 \ \] )\ \] </sup>

COut = q2

> [!Note]  
> Ln ist die API-Methode [**D3DXQuaternionLn,**](d3dxquaternionln.md) und Exp ist die API-Methode [**D3DXQuaternionExp.**](d3dxquaternionexp.md)

 

Verwenden [**Sie D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) für alle Quaternioneingaben, die noch nicht normalisiert sind.

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
> -   C ist abhängig vom Ergebnis der Funktion +/- Q2.
> -   Qt ist das Ergebnis der Funktion.
>
> Das Ergebnis ist eine Drehung um 45 Grad um die Z-Achse für die Zeit = 0,5.

 

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Mathematische Funktionen](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXQuaternionSquad**](d3dxquaternionsquad.md)
</dt> </dl>

 

 




