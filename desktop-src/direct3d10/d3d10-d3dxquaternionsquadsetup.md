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
ms.openlocfilehash: 8d8a778473c0b07ef984facce9c42f947755a74a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108718"
---
# <a name="d3dxquaternionsquadsetup-function-d3dx10mathh"></a><span data-ttu-id="4b2e9-103">D3DXQuaternionSquadSetup-Funktion (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="4b2e9-103">D3DXQuaternionSquadSetup function (D3DX10Math.h)</span></span>

<span data-ttu-id="4b2e9-104">Richtet Steuerungspunkte für die sphärische Quadrangleinterpolation ein.</span><span class="sxs-lookup"><span data-stu-id="4b2e9-104">Sets up control points for spherical quadrangle interpolation.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b2e9-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4b2e9-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="4b2e9-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4b2e9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4b2e9-107">*pAOut* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="4b2e9-107">*pAOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b2e9-108">Typ: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="4b2e9-108">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="4b2e9-109">Zeiger auf AOut.</span><span class="sxs-lookup"><span data-stu-id="4b2e9-109">Pointer to AOut.</span></span>

</dd> <dt>

<span data-ttu-id="4b2e9-110">*pBOut* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="4b2e9-110">*pBOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b2e9-111">Typ: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="4b2e9-111">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="4b2e9-112">Zeiger auf BOut.</span><span class="sxs-lookup"><span data-stu-id="4b2e9-112">Pointer to BOut.</span></span>

</dd> <dt>

<span data-ttu-id="4b2e9-113">*pCOut* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="4b2e9-113">*pCOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b2e9-114">Typ: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="4b2e9-114">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="4b2e9-115">Zeiger auf COut.</span><span class="sxs-lookup"><span data-stu-id="4b2e9-115">Pointer to COut.</span></span>

</dd> <dt>

<span data-ttu-id="4b2e9-116">*pQ0* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="4b2e9-116">*pQ0* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b2e9-117">Typ: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="4b2e9-117">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="4b2e9-118">Zeiger auf den Eingabesteuerpunkt Q0.</span><span class="sxs-lookup"><span data-stu-id="4b2e9-118">Pointer to the input control point, Q0.</span></span>

</dd> <dt>

<span data-ttu-id="4b2e9-119">*pQ1* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="4b2e9-119">*pQ1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b2e9-120">Typ: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="4b2e9-120">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="4b2e9-121">Zeiger auf den Eingabesteuerpunkt Q1.</span><span class="sxs-lookup"><span data-stu-id="4b2e9-121">Pointer to the input control point, Q1.</span></span>

</dd> <dt>

<span data-ttu-id="4b2e9-122">*pQ2* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="4b2e9-122">*pQ2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b2e9-123">Typ: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="4b2e9-123">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="4b2e9-124">Zeiger auf den Eingabesteuerpunkt Q2.</span><span class="sxs-lookup"><span data-stu-id="4b2e9-124">Pointer to the input control point, Q2.</span></span>

</dd> <dt>

<span data-ttu-id="4b2e9-125">*pQ3* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="4b2e9-125">*pQ3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b2e9-126">Typ: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="4b2e9-126">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="4b2e9-127">Zeiger auf den Eingabesteuerpunkt Q3.</span><span class="sxs-lookup"><span data-stu-id="4b2e9-127">Pointer to the input control point, Q3.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4b2e9-128">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4b2e9-128">Return value</span></span>

<span data-ttu-id="4b2e9-129">Keine.</span><span class="sxs-lookup"><span data-stu-id="4b2e9-129">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="4b2e9-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4b2e9-130">Remarks</span></span>

<span data-ttu-id="4b2e9-131">Diese Funktion verwendet vier Steuerungspunkte, die für die Eingaben pQ0, pQ1, pQ2 und pQ3 bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="4b2e9-131">This function takes four control points, which are supplied to the inputs pQ0, pQ1, pQ2, and pQ3.</span></span> <span data-ttu-id="4b2e9-132">Die Funktion ändert dann diese Werte, um eine Kurve zu finden, die entlang des kürzesten Pfads verläuft.</span><span class="sxs-lookup"><span data-stu-id="4b2e9-132">The function then alters these values to find a curve that flows along the shortest path.</span></span> <span data-ttu-id="4b2e9-133">Die Werte von q0, q2 und q3 werden wie unten dargestellt berechnet.</span><span class="sxs-lookup"><span data-stu-id="4b2e9-133">The values of q0, q2, and q3 are calculated as shown below.</span></span>


```
q0 = |Q0 + Q1| < |Q0 - Q1| ? -Q0 : Q0
q2 = |Q1 + Q2| < |Q1 - Q2| ? -Q2 : Q2
q3 = |Q2 + Q3| < |Q2 - Q3| ? -Q3 : Q3
```



<span data-ttu-id="4b2e9-134">Nachdem die neuen Q-Werte berechnet wurden, werden die Werte für AOut, BOut und COut wie folgt berechnet:</span><span class="sxs-lookup"><span data-stu-id="4b2e9-134">Having calculated the new Q values, the values for AOut, BOut, and COut are calculated as follows:</span></span>

<span data-ttu-id="4b2e9-135">AOut = q1 \* e<sup> \[ -0.25\ \* (\ Ln \[ Exp(q1) \* q2 \] \ +\ Ln \[ Exp(q1) \* q0 \ \] )\ \] </sup></span><span class="sxs-lookup"><span data-stu-id="4b2e9-135">AOut = q1 \* e<sup>\[-0.25\ \*(\ Ln\[Exp(q1)\*q2\]\ +\ Ln\[Exp(q1)\*q0\]\ )\ \]</sup></span></span>

<span data-ttu-id="4b2e9-136">BOut = q2 \* e<sup> \[ -0.25\ \* (\ Ln \[ Exp(q2) \* q3 \] \ +\ Ln \[ Exp(q2) \* q1 \ \] )\ \] </sup></span><span class="sxs-lookup"><span data-stu-id="4b2e9-136">BOut = q2 \* e<sup>\[-0.25\ \*(\ Ln\[Exp(q2)\*q3\]\ +\ Ln\[Exp(q2)\*q1\]\ )\ \]</sup></span></span>

<span data-ttu-id="4b2e9-137">COut = q2</span><span class="sxs-lookup"><span data-stu-id="4b2e9-137">COut = q2</span></span>

> [!Note]  
> <span data-ttu-id="4b2e9-138">Ln ist die API-Methode [**D3DXQuaternionLn,**](d3d10-d3dxquaternionln.md) und Exp ist die API-Methode [**D3DXQuaternionExp.**](d3d10-d3dxquaternionexp.md)</span><span class="sxs-lookup"><span data-stu-id="4b2e9-138">Ln is the API method [**D3DXQuaternionLn**](d3d10-d3dxquaternionln.md) and Exp is the API method [**D3DXQuaternionExp**](d3d10-d3dxquaternionexp.md).</span></span>

 

<span data-ttu-id="4b2e9-139">Verwenden Sie [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) für alle Quaternioneingaben, die nicht bereits normalisiert sind.</span><span class="sxs-lookup"><span data-stu-id="4b2e9-139">Use [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

### <a name="examples"></a><span data-ttu-id="4b2e9-140">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4b2e9-140">Examples</span></span>

<span data-ttu-id="4b2e9-141">Das folgende Beispiel zeigt, wie Sie einen Satz von Quaternionsschlüsseln (Q0, Q1, Q2, Q3) verwenden, um die inneren Quadranglepunkte (A, B, C) zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="4b2e9-141">The following example shows how to use a set of quaternion keys (Q0, Q1, Q2, Q3) to compute the inner quadrangle points (A, B, C).</span></span> <span data-ttu-id="4b2e9-142">Dadurch wird sichergestellt, dass die Tangenten über angrenzende Segmente hinweg kontinuierlich sind.</span><span class="sxs-lookup"><span data-stu-id="4b2e9-142">This ensures that the tangents are continuous across adjacent segments.</span></span>


```
      A     B
Q0    Q1    Q2    Q3
```



<span data-ttu-id="4b2e9-143">Im folgenden Codebeispiel wird veranschaulicht, wie Sie zwischen Q1 und Q2 interpolieren können.</span><span class="sxs-lookup"><span data-stu-id="4b2e9-143">The following code example demonstrates how you can interpolate between Q1 and Q2.</span></span>


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
> -   <span data-ttu-id="4b2e9-144">C ist +/- Q2, abhängig vom Ergebnis der Funktion.</span><span class="sxs-lookup"><span data-stu-id="4b2e9-144">C is +/- Q2 depending on the result of the function.</span></span>
> -   <span data-ttu-id="4b2e9-145">Qt ist das Ergebnis der Funktion.</span><span class="sxs-lookup"><span data-stu-id="4b2e9-145">Qt is the result of the function.</span></span>
>
> <span data-ttu-id="4b2e9-146">Das Ergebnis ist eine Drehung von 45 Grad um die Z-Achse für die Zeit = 0,5.</span><span class="sxs-lookup"><span data-stu-id="4b2e9-146">The result is a rotation of 45 degrees around the z-axis for time = 0.5.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4b2e9-147">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4b2e9-147">Requirements</span></span>



| <span data-ttu-id="4b2e9-148">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4b2e9-148">Requirement</span></span> | <span data-ttu-id="4b2e9-149">Wert</span><span class="sxs-lookup"><span data-stu-id="4b2e9-149">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4b2e9-150">Header</span><span class="sxs-lookup"><span data-stu-id="4b2e9-150">Header</span></span><br/>  | <dl> <span data-ttu-id="4b2e9-151"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="4b2e9-151"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="4b2e9-152">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="4b2e9-152">Library</span></span><br/> | <dl> <span data-ttu-id="4b2e9-153"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="4b2e9-153"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="4b2e9-154">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="4b2e9-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b2e9-155">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="4b2e9-155">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
