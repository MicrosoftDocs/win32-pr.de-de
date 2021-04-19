---
title: D2D1_MATRIX_3X2_F (D2D1. h)
description: Stellt eine 3 x 2-Matrix dar.
ms.assetid: f05d7555-6482-4eea-950f-7b443892cc1f
keywords:
- D2D1_MATRIX_3X2_F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: beb252e35508c48570c96f251205fc8a54755687
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342192"
---
# <a name="d2d1_matrix_3x2_f"></a><span data-ttu-id="b62d1-104">D2D1 \_ Matrix \_ 3x2 \_ F</span><span class="sxs-lookup"><span data-stu-id="b62d1-104">D2D1\_MATRIX\_3X2\_F</span></span>

<span data-ttu-id="b62d1-105">Stellt eine 3 x 2-Matrix dar.</span><span class="sxs-lookup"><span data-stu-id="b62d1-105">Represents a 3-by-2 matrix.</span></span>


```C++
typedef D2D_MATRIX_3X2_F D2D1_MATRIX_3X2_F;
```



## <a name="remarks"></a><span data-ttu-id="b62d1-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b62d1-106">Remarks</span></span>

<span data-ttu-id="b62d1-107">**D2D1 \_ Matrix \_ 3x2** ist ein neuer Name für die [**D2D \_ Matrix \_ 3x2- \_ F-**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_3x2_f) Struktur.</span><span class="sxs-lookup"><span data-stu-id="b62d1-107">**D2D1\_MATRIX\_3X2** is a new name for the [**D2D\_MATRIX\_3X2\_F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_3x2_f) structure.</span></span> <span data-ttu-id="b62d1-108">Eine Liste der Felder, die von der Matrix bereitgestellt werden, finden Sie unter [**D2D \_ Matrix \_ 3x2 \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_3x2_f).</span><span class="sxs-lookup"><span data-stu-id="b62d1-108">For a list of fields provided by the matrix, see [**D2D\_MATRIX\_3X2\_F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_3x2_f).</span></span>

<span data-ttu-id="b62d1-109">Zum vereinfachen allgemeiner Matrix Vorgänge stellt Direct2D die [**D2D1:: Matrix3x2F**](/windows/win32/api/d2d1helper/nl-d2d1helper-matrix3x2f) -Klasse bereit, die aus der [**D2D1 \_ Matrix \_ 3x2-**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_3x2_f) Struktur abgeleitet ist.</span><span class="sxs-lookup"><span data-stu-id="b62d1-109">To simplify common matrix operations, Direct2D provides the [**D2D1::Matrix3x2F**](/windows/win32/api/d2d1helper/nl-d2d1helper-matrix3x2f) class, which is derived from the [**D2D1\_MATRIX\_3X2**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_3x2_f) structure.</span></span> <span data-ttu-id="b62d1-110">Die **Matrix3x2F** -Klasse stellt einen Satz von Hilfsmethoden zum Ausführen allgemeiner Aufgaben bereit, z. b. zum Erstellen einer Übersetzungs-oder schiefe-Matrix.</span><span class="sxs-lookup"><span data-stu-id="b62d1-110">The **Matrix3x2F** class provides a set of helper methods for performing common tasks, such as creating a translation or skew matrix.</span></span>

## <a name="examples"></a><span data-ttu-id="b62d1-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b62d1-111">Examples</span></span>

<span data-ttu-id="b62d1-112">Im folgenden Beispiel wird die [**D2D1:: Matrix3x2F:: Rotation**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-rotation) -Methode verwendet, um eine Rotations Matrix zu erstellen, die einen quadratischen Uhrzeigersinn um 45 Grad um die Mitte des Quadrats dreht und die Matrix an die [**setTransform**](/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f_)) -Methode des Renderziels (*m \_ prendertarget*) übergibt.</span><span class="sxs-lookup"><span data-stu-id="b62d1-112">The following example uses the [**D2D1::Matrix3x2F::Rotation**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-rotation) method to create a rotation matrix that rotates a square clockwise 45 degrees about the center of the square and passes the matrix to the [**SetTransform**](/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f_)) method of the render target (*m\_pRenderTarget*).</span></span>

<span data-ttu-id="b62d1-113">Die folgende Abbildung zeigt die Auswirkung der Anwendung der vorangehenden Rotations Transformation auf das Quadrat.</span><span class="sxs-lookup"><span data-stu-id="b62d1-113">The following illustration shows the effect of applying the preceding rotation transformation to the square.</span></span> <span data-ttu-id="b62d1-114">Das ursprüngliche Quadrat ist ein gepunkteter Umriss, und das gedrehte Quadrat ist ein voll solider Umriss.</span><span class="sxs-lookup"><span data-stu-id="b62d1-114">The original square is a dotted outline, and the rotated square is a solid outline.</span></span>

![Abbildung eines Quadrats um 45 Grad im Uhrzeigersinn um die Mitte des ursprünglichen Quadrats gedreht](images/rotate-ovw.png)


```C++
    // Create a rectangle.
    D2D1_RECT_F rectangle = D2D1::Rect(438.0f, 301.5f, 498.0f, 361.5f);

    // Draw the rectangle.
    m_pRenderTarget->DrawRectangle(
        rectangle,
        m_pOriginalShapeBrush,
        1.0f,
        m_pStrokeStyleDash
        );

    // Apply the rotation transform to the render target.
    m_pRenderTarget->SetTransform(
        D2D1::Matrix3x2F::Rotation(
            45.0f,
            D2D1::Point2F(468.0f, 331.5f))
        );

    // Fill the rectangle.
    m_pRenderTarget->FillRectangle(rectangle, m_pFillBrush);

    // Draw the transformed rectangle.
    m_pRenderTarget->DrawRectangle(rectangle, m_pTransformedShapeBrush);

```



<span data-ttu-id="b62d1-116">Code wurde in diesem Beispiel ausgelassen.</span><span class="sxs-lookup"><span data-stu-id="b62d1-116">Code has been omitted from this example.</span></span> <span data-ttu-id="b62d1-117">Weitere Informationen zu Transformationen finden Sie in der [Übersicht über Transformationen](direct2d-transforms-overview.md).</span><span class="sxs-lookup"><span data-stu-id="b62d1-117">For more information about transforms, see the [Transforms Overview](direct2d-transforms-overview.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b62d1-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b62d1-118">Requirements</span></span>



| <span data-ttu-id="b62d1-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b62d1-119">Requirement</span></span> | <span data-ttu-id="b62d1-120">Wert</span><span class="sxs-lookup"><span data-stu-id="b62d1-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b62d1-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b62d1-121">Minimum supported client</span></span><br/> | <span data-ttu-id="b62d1-122">Windows 7, Windows Vista mit SP2 und Platt Form Update für Windows Vista \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="b62d1-122">Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="b62d1-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b62d1-123">Minimum supported server</span></span><br/> | <span data-ttu-id="b62d1-124">Windows Server 2008 R2, Windows Server 2008 mit SP2 und Platt Form Update für Windows Server 2008 \[ Desktop Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="b62d1-124">Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="b62d1-125">Unterstützte Mindestversion (Telefon)</span><span class="sxs-lookup"><span data-stu-id="b62d1-125">Minimum supported phone</span></span><br/>  | <span data-ttu-id="b62d1-126">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 und Windows-Runtime apps\]</span><span class="sxs-lookup"><span data-stu-id="b62d1-126">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/>                                                  |
| <span data-ttu-id="b62d1-127">Header</span><span class="sxs-lookup"><span data-stu-id="b62d1-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="b62d1-128"><dt>D2d1. h</dt></span><span class="sxs-lookup"><span data-stu-id="b62d1-128"><dt>D2d1.h</dt></span></span> </dl>                                                        |



## <a name="see-also"></a><span data-ttu-id="b62d1-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b62d1-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b62d1-130">**D2D1::Matrix3x2F**</span><span class="sxs-lookup"><span data-stu-id="b62d1-130">**D2D1::Matrix3x2F**</span></span>](/windows/win32/api/d2d1helper/nl-d2d1helper-matrix3x2f)
</dt> <dt>

[<span data-ttu-id="b62d1-131">Übersicht über Transformationen</span><span class="sxs-lookup"><span data-stu-id="b62d1-131">Transforms Overview</span></span>](direct2d-transforms-overview.md)
</dt> <dt>

[<span data-ttu-id="b62d1-132">Drehen eines Objekts</span><span class="sxs-lookup"><span data-stu-id="b62d1-132">How to Rotate an Object</span></span>](how-to-rotate.md)
</dt> <dt>

[<span data-ttu-id="b62d1-133">Skalieren eines Objekts</span><span class="sxs-lookup"><span data-stu-id="b62d1-133">How to Scale an Object</span></span>](how-to-scale.md)
</dt> <dt>

[<span data-ttu-id="b62d1-134">Vorgehensweise beim Verzerren eines Objekts</span><span class="sxs-lookup"><span data-stu-id="b62d1-134">How to Skew an Object</span></span>](how-to-skew.md)
</dt> <dt>

[<span data-ttu-id="b62d1-135">Übersetzen eines Objekts</span><span class="sxs-lookup"><span data-stu-id="b62d1-135">How to Translate an Object</span></span>](how-to-translate.md)
</dt> <dt>

[<span data-ttu-id="b62d1-136">**D2D \_ Matrix \_ 3x2 \_ F**</span><span class="sxs-lookup"><span data-stu-id="b62d1-136">**D2D\_MATRIX\_3X2\_F**</span></span>](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_3x2_f)
</dt> </dl>

 

