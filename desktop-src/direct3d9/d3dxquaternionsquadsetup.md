---
description: Richtet Steuerungs Punkte für die sphärische Quadrangle-interpolung ein.
ms.assetid: f800d457-8546-49a1-800e-e5c27af96710
title: D3DXQuaternionSquadSetup-Funktion (D3dx9math. h)
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
ms.openlocfilehash: 04bae9dafbb9df90fdcccee830a1eecb64c1430f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106373505"
---
# <a name="d3dxquaternionsquadsetup-function-d3dx9mathh"></a><span data-ttu-id="1156f-103">D3DXQuaternionSquadSetup-Funktion (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="1156f-103">D3DXQuaternionSquadSetup function (D3dx9math.h)</span></span>

<span data-ttu-id="1156f-104">Richtet Steuerungs Punkte für die sphärische Quadrangle-interpolung ein.</span><span class="sxs-lookup"><span data-stu-id="1156f-104">Sets up control points for spherical quadrangle interpolation.</span></span>

## <a name="syntax"></a><span data-ttu-id="1156f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1156f-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="1156f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1156f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1156f-107">*Auslagern* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="1156f-107">*pAOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1156f-108">Typ: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="1156f-108">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="1156f-109">Zeiger auf "aout".</span><span class="sxs-lookup"><span data-stu-id="1156f-109">Pointer to AOut.</span></span>

</dd> <dt>

<span data-ttu-id="1156f-110">*pbout* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="1156f-110">*pBOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1156f-111">Typ: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="1156f-111">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="1156f-112">Zeiger auf "BOut".</span><span class="sxs-lookup"><span data-stu-id="1156f-112">Pointer to BOut.</span></span>

</dd> <dt>

<span data-ttu-id="1156f-113">*pcout* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="1156f-113">*pCOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1156f-114">Typ: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="1156f-114">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="1156f-115">Zeiger auf "cout".</span><span class="sxs-lookup"><span data-stu-id="1156f-115">Pointer to COut.</span></span>

</dd> <dt>

<span data-ttu-id="1156f-116">*pQ0* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1156f-116">*pQ0* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1156f-117">Typ: **Konstanten [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="1156f-117">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="1156f-118">Zeiger auf den Eingabe Steuerungspunkt, q0.</span><span class="sxs-lookup"><span data-stu-id="1156f-118">Pointer to the input control point, Q0.</span></span>

</dd> <dt>

<span data-ttu-id="1156f-119">*pQ1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1156f-119">*pQ1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1156f-120">Typ: **Konstanten [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="1156f-120">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="1156f-121">Zeiger auf den Eingabe Steuerungspunkt (Q1).</span><span class="sxs-lookup"><span data-stu-id="1156f-121">Pointer to the input control point, Q1.</span></span>

</dd> <dt>

<span data-ttu-id="1156f-122">*pQ2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1156f-122">*pQ2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1156f-123">Typ: **Konstanten [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="1156f-123">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="1156f-124">Zeiger auf den Eingabe Steuerungspunkt (Q2).</span><span class="sxs-lookup"><span data-stu-id="1156f-124">Pointer to the input control point, Q2.</span></span>

</dd> <dt>

<span data-ttu-id="1156f-125">*pQ3* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1156f-125">*pQ3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1156f-126">Typ: **Konstanten [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="1156f-126">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="1156f-127">Zeiger auf den Eingabe Steuerungspunkt (Q3).</span><span class="sxs-lookup"><span data-stu-id="1156f-127">Pointer to the input control point, Q3.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1156f-128">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1156f-128">Return value</span></span>

<span data-ttu-id="1156f-129">Keine.</span><span class="sxs-lookup"><span data-stu-id="1156f-129">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="1156f-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1156f-130">Remarks</span></span>

<span data-ttu-id="1156f-131">Diese Funktion nimmt vier Steuerungs Punkte an, die für die Eingaben pQ0, pQ1, pQ2 und pQ3 bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="1156f-131">This function takes four control points, which are supplied to the inputs pQ0, pQ1, pQ2, and pQ3.</span></span> <span data-ttu-id="1156f-132">Die-Funktion ändert dann diese Werte, um eine Kurve zu finden, die entlang des kürzesten Pfads verläuft.</span><span class="sxs-lookup"><span data-stu-id="1156f-132">The function then alters these values to find a curve that flows along the shortest path.</span></span> <span data-ttu-id="1156f-133">Die Werte von Q0, Q2 und Q3 werden wie unten dargestellt berechnet.</span><span class="sxs-lookup"><span data-stu-id="1156f-133">The values of q0, q2, and q3 are calculated as shown below.</span></span>


```
q0 = |Q0 + Q1| < |Q0 - Q1| ? -Q0 : Q0
q2 = |Q1 + Q2| < |Q1 - Q2| ? -Q2 : Q2
q3 = |Q2 + Q3| < |Q2 - Q3| ? -Q3 : Q3
```



<span data-ttu-id="1156f-134">Wenn Sie die neuen Q-Werte berechnet haben, werden die Werte für "aout", "BOut" und "cout" wie folgt berechnet:</span><span class="sxs-lookup"><span data-stu-id="1156f-134">Having calculated the new Q values, the values for AOut, BOut, and COut are calculated as follows:</span></span>

<span data-ttu-id="1156f-135">Aout = Q1 \* e<sup> \[ -0,25 \ \* (\ LN \[ Exp (Q1) \* Q2 \] \ + \ LN \[ Exp (Q1) \* q0 \] \) \ \] </sup></span><span class="sxs-lookup"><span data-stu-id="1156f-135">AOut = q1 \* e<sup>\[-0.25\ \*(\ Ln\[Exp(q1)\*q2\]\ +\ Ln\[Exp(q1)\*q0\]\ )\ \]</sup></span></span>

<span data-ttu-id="1156f-136">BOut = Q2 \* e<sup> \[ -0,25 \ \* (\ LN \[ Exp (Q2) \* Q3 \] \ + \ LN \[ Exp (Q2) \* Q1 \] \) \ \] </sup></span><span class="sxs-lookup"><span data-stu-id="1156f-136">BOut = q2 \* e<sup>\[-0.25\ \*(\ Ln\[Exp(q2)\*q3\]\ +\ Ln\[Exp(q2)\*q1\]\ )\ \]</sup></span></span>

<span data-ttu-id="1156f-137">Cout = Q2</span><span class="sxs-lookup"><span data-stu-id="1156f-137">COut = q2</span></span>

> [!Note]  
> <span data-ttu-id="1156f-138">LN ist die API-Methode [**D3DXQuaternionLn**](d3dxquaternionln.md) und Exp ist die API-Methode [**D3DXQuaternionExp**](d3dxquaternionexp.md).</span><span class="sxs-lookup"><span data-stu-id="1156f-138">Ln is the API method [**D3DXQuaternionLn**](d3dxquaternionln.md) and Exp is the API method [**D3DXQuaternionExp**](d3dxquaternionexp.md).</span></span>

 

<span data-ttu-id="1156f-139">Verwenden Sie [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) für eine beliebige Quaternion-Eingabe, die nicht bereits normalisiert ist.</span><span class="sxs-lookup"><span data-stu-id="1156f-139">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

### <a name="examples"></a><span data-ttu-id="1156f-140">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1156f-140">Examples</span></span>

<span data-ttu-id="1156f-141">Im folgenden Beispiel wird gezeigt, wie ein Satz von Quaternion-Schlüsseln (q0, Q1, Q2, Q3) zum Berechnen der inneren Quadranten Punkte (a, B, C) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1156f-141">The following example shows how to use a set of quaternion keys (Q0, Q1, Q2, Q3) to compute the inner quadrangle points (A, B, C).</span></span> <span data-ttu-id="1156f-142">Dadurch wird sichergestellt, dass die Tangenten in angrenzenden Segmenten kontinuierlich sind.</span><span class="sxs-lookup"><span data-stu-id="1156f-142">This ensures that the tangents are continuous across adjacent segments.</span></span>


```
      A     B
Q0    Q1    Q2    Q3
```



<span data-ttu-id="1156f-143">Im folgenden Codebeispiel wird veranschaulicht, wie Sie zwischen Q1 und Q2 interpolieren können.</span><span class="sxs-lookup"><span data-stu-id="1156f-143">The following code example demonstrates how you can interpolate between Q1 and Q2.</span></span>


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
> -   <span data-ttu-id="1156f-144">C ist +/-Q2, abhängig vom Ergebnis der Funktion.</span><span class="sxs-lookup"><span data-stu-id="1156f-144">C is +/- Q2 depending on the result of the function.</span></span>
> -   <span data-ttu-id="1156f-145">Qt ist das Ergebnis der-Funktion.</span><span class="sxs-lookup"><span data-stu-id="1156f-145">Qt is the result of the function.</span></span>
>
> <span data-ttu-id="1156f-146">Das Ergebnis ist eine Drehung von 45 Grad um die z-Achse für time = 0,5.</span><span class="sxs-lookup"><span data-stu-id="1156f-146">The result is a rotation of 45 degrees around the z-axis for time = 0.5.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="1156f-147">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1156f-147">Requirements</span></span>



| <span data-ttu-id="1156f-148">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1156f-148">Requirement</span></span> | <span data-ttu-id="1156f-149">Wert</span><span class="sxs-lookup"><span data-stu-id="1156f-149">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1156f-150">Header</span><span class="sxs-lookup"><span data-stu-id="1156f-150">Header</span></span><br/>  | <dl> <span data-ttu-id="1156f-151"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="1156f-151"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="1156f-152">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1156f-152">Library</span></span><br/> | <dl> <span data-ttu-id="1156f-153"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1156f-153"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1156f-154">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1156f-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1156f-155">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="1156f-155">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="1156f-156">**D3DXQuaternionSquad**</span><span class="sxs-lookup"><span data-stu-id="1156f-156">**D3DXQuaternionSquad**</span></span>](d3dxquaternionsquad.md)
</dt> </dl>

 

 




