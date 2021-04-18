---
title: Anhang Matrixtransformationen
description: Dieses Thema bietet eine mathematische Übersicht über Matrix Transformationen für 2D-Grafiken.
ms.assetid: 8cc01f45-dd84-4f3e-a5f2-26edc5cbdfa1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a5a9b09f75b17e4baf8afe5e7fde8643c06982f
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/28/2021
ms.locfileid: "104563886"
---
# <a name="appendix-matrix-transforms"></a><span data-ttu-id="2b942-103">Anhang: Matrix Transformationen</span><span class="sxs-lookup"><span data-stu-id="2b942-103">Appendix: Matrix Transforms</span></span>

<span data-ttu-id="2b942-104">Dieses Thema bietet eine mathematische Übersicht über Matrix Transformationen für 2D-Grafiken.</span><span class="sxs-lookup"><span data-stu-id="2b942-104">This topic provides a mathematical overview of matrix transforms for 2-D graphics.</span></span> <span data-ttu-id="2b942-105">Allerdings müssen Sie Matrizen Mathematik nicht kennen, um Transformationen in Direct2D verwenden zu können.</span><span class="sxs-lookup"><span data-stu-id="2b942-105">However, you don't need to know matrix math in order to use transforms in Direct2D.</span></span> <span data-ttu-id="2b942-106">Lesen Sie dieses Thema, wenn Sie an der Mathematik interessiert sind. Andernfalls können Sie dieses Thema überspringen.</span><span class="sxs-lookup"><span data-stu-id="2b942-106">Read this topic if you are interested in the math; otherwise, feel free to skip this topic.</span></span>

-   [<span data-ttu-id="2b942-107">Einführung in Matrizen</span><span class="sxs-lookup"><span data-stu-id="2b942-107">Introduction to Matrices</span></span>](#introduction-to-matrices)
    -   [<span data-ttu-id="2b942-108">Matrix Vorgänge</span><span class="sxs-lookup"><span data-stu-id="2b942-108">Matrix Operations</span></span>](#matrix-operations)
-   [<span data-ttu-id="2b942-109">Affine Transformationen</span><span class="sxs-lookup"><span data-stu-id="2b942-109">Affine Transforms</span></span>](#affine-transforms)
    -   [<span data-ttu-id="2b942-110">Übersetzungs Transformation</span><span class="sxs-lookup"><span data-stu-id="2b942-110">Translation Transform</span></span>](#translation-transform)
    -   [<span data-ttu-id="2b942-111">Skalierungs Transformation</span><span class="sxs-lookup"><span data-stu-id="2b942-111">Scaling Transform</span></span>](#scaling-transform)
    -   [<span data-ttu-id="2b942-112">Drehung um den Ursprung</span><span class="sxs-lookup"><span data-stu-id="2b942-112">Rotation Around the Origin</span></span>](#rotation-around-the-origin)
    -   [<span data-ttu-id="2b942-113">Drehung um einen beliebigen Punkt</span><span class="sxs-lookup"><span data-stu-id="2b942-113">Rotation Around an Arbitrary Point</span></span>](#rotation-around-an-arbitrary-point)
    -   [<span data-ttu-id="2b942-114">Verzerrungs Transformation</span><span class="sxs-lookup"><span data-stu-id="2b942-114">Skew Transform</span></span>](#skew-transform)
-   [<span data-ttu-id="2b942-115">Darstellen von Transformationen in Direct2D</span><span class="sxs-lookup"><span data-stu-id="2b942-115">Representing Transforms in Direct2D</span></span>](#representing-transforms-in-direct2d)
-   [<span data-ttu-id="2b942-116">Nächste</span><span class="sxs-lookup"><span data-stu-id="2b942-116">Next</span></span>](#next)

## <a name="introduction-to-matrices"></a><span data-ttu-id="2b942-117">Einführung in Matrizen</span><span class="sxs-lookup"><span data-stu-id="2b942-117">Introduction to Matrices</span></span>

<span data-ttu-id="2b942-118">Eine Matrix ist ein rechteckiges Array von reellen Zahlen.</span><span class="sxs-lookup"><span data-stu-id="2b942-118">A matrix is a rectangular array of real numbers.</span></span> <span data-ttu-id="2b942-119">Die *Reihenfolge* der Matrix entspricht der Anzahl von Zeilen und Spalten.</span><span class="sxs-lookup"><span data-stu-id="2b942-119">The *order* of the matrix is the number of rows and columns.</span></span> <span data-ttu-id="2b942-120">Wenn die Matrix z. b. drei Zeilen und 2 Spalten enthält, ist die Reihenfolge 3 × 2.</span><span class="sxs-lookup"><span data-stu-id="2b942-120">For example, if the matrix has 3 rows and 2 columns, the order is 3 × 2.</span></span> <span data-ttu-id="2b942-121">Matrizen werden normalerweise mit den Matrixelementen angezeigt, die in eckigen Klammern eingeschlossen sind:</span><span class="sxs-lookup"><span data-stu-id="2b942-121">Matrices are usually shown with the matrix elements enclosed in square brackets:</span></span>

![3 x 2-Matrix.](images/matrix01.png)

<span data-ttu-id="2b942-123">Notation: eine Matrix wird durch einen Großbuchstaben angegeben.</span><span class="sxs-lookup"><span data-stu-id="2b942-123">Notation: A matrix is designated by a capital letter.</span></span> <span data-ttu-id="2b942-124">-Elemente werden durch Kleinbuchstaben angegeben.</span><span class="sxs-lookup"><span data-stu-id="2b942-124">Elements are designated by lowercase letters.</span></span> <span data-ttu-id="2b942-125">Index gibt die Zeilen-und Spaltennummer eines Elements an.</span><span class="sxs-lookup"><span data-stu-id="2b942-125">Subscripts indicate the row and column number of an element.</span></span> <span data-ttu-id="2b942-126">Ein *IJ* ist beispielsweise das Element in der Zeile "n" und der "j."-Spalte der Matrix a.</span><span class="sxs-lookup"><span data-stu-id="2b942-126">For example, a *ij* is the element at the i'th row and j'th column of the matrix A.</span></span>

<span data-ttu-id="2b942-127">Das folgende Diagramm zeigt eine i × j-Matrix mit den einzelnen Elementen in den einzelnen Zellen der Matrix.</span><span class="sxs-lookup"><span data-stu-id="2b942-127">The following diagram shows an i × j matrix, with the individual elements in each cell of the matrix.</span></span>

![eine Matrix mit i-Zeilen und j-Spalten.](images/matrix15.png)

### <a name="matrix-operations"></a><span data-ttu-id="2b942-129">Matrix Vorgänge</span><span class="sxs-lookup"><span data-stu-id="2b942-129">Matrix Operations</span></span>

<span data-ttu-id="2b942-130">Dieser Abschnitt beschreibt die grundlegenden Vorgänge, die für Matrizen definiert sind.</span><span class="sxs-lookup"><span data-stu-id="2b942-130">This section describes the basic operations defined on matrices.</span></span>

<span data-ttu-id="2b942-131">*Fügen Sie hinzu*.</span><span class="sxs-lookup"><span data-stu-id="2b942-131">*Addition*.</span></span> <span data-ttu-id="2b942-132">Die Summe A + B von zwei Matrizen wird durch Hinzufügen der entsprechenden Elemente von A und b abgerufen:</span><span class="sxs-lookup"><span data-stu-id="2b942-132">The sum A + B of two matrices is obtained by adding the corresponding elements of A and B:</span></span>

<dl> <span data-ttu-id="2b942-133">A + b = \[ a *IJ* \]  +  \[ B *IJ* \]  =  \[ a *IJ* + b *IJ*\]</span><span class="sxs-lookup"><span data-stu-id="2b942-133">A + B = \[ a *ij* \] + \[ b *ij* \] = \[ a *ij* + b *ij* \]</span></span>
</dl>

<span data-ttu-id="2b942-134">*Skalare Multiplikation*.</span><span class="sxs-lookup"><span data-stu-id="2b942-134">*Scalar multiplication*.</span></span> <span data-ttu-id="2b942-135">Durch diesen Vorgang wird eine Matrix mit einer reellen Zahl multipliziert.</span><span class="sxs-lookup"><span data-stu-id="2b942-135">This operation multiplies a matrix by a real number.</span></span> <span data-ttu-id="2b942-136">Bei einer reellen Zahl *k* wird das Skalarprodukt "Ka" abgerufen, indem jedes Element von a mit *k* multipliziert wird.</span><span class="sxs-lookup"><span data-stu-id="2b942-136">Given a real number *k*, the scalar product kA is obtained by multiplying every element of A by *k*.</span></span>

<dl> <span data-ttu-id="2b942-137">Ka = k \[ a *IJ* \]  =  \[ k × a *IJ*\]</span><span class="sxs-lookup"><span data-stu-id="2b942-137">kA = k\[ a *ij* \] = \[ k × a *ij* \]</span></span>
</dl>

<span data-ttu-id="2b942-138">*Matrix Multiplikation*.</span><span class="sxs-lookup"><span data-stu-id="2b942-138">*Matrix multiplication*.</span></span> <span data-ttu-id="2b942-139">Bei zwei Matrizen A und B mit der Reihenfolge (m × n) und (n × p) ist das Produkt C = a × b eine Matrix mit der Reihenfolge (m × p), die wie folgt definiert wird:</span><span class="sxs-lookup"><span data-stu-id="2b942-139">Given two matrices A and B with order (m × n) and (n × p), the product C = A × B is a matrix with order (m × p), defined as follows:</span></span>

![Zeigt eine Formel für die Matrix Multiplikation an.](images/matrix02.png)

<span data-ttu-id="2b942-141">oder, gleichwertig:</span><span class="sxs-lookup"><span data-stu-id="2b942-141">or, equivalently:</span></span>

<dl> <span data-ttu-id="2b942-142">c *IJ* = a *i* 1 x B1 *j* + a *i* 2 x B2 *j* +... + a *in* + b *NJ*  
</span><span class="sxs-lookup"><span data-stu-id="2b942-142">c *ij* = a *i* 1 x b1 *j* + a *i* 2 x b2 *j* + ... + a *in* + b *nj*  
</span></span></dl>

<span data-ttu-id="2b942-143">Um jedes Element c *IJ* zu berechnen, führen Sie die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="2b942-143">That is, to compute each element c *ij*, do the following:</span></span>

1.  <span data-ttu-id="2b942-144">Nehmen Sie in der Zeile "a" und in der "j."-Spalte den Typ "B".</span><span class="sxs-lookup"><span data-stu-id="2b942-144">Take the i'th row of A and the j'th column of B.</span></span>
2.  <span data-ttu-id="2b942-145">Multiplizieren Sie jedes Paar von Elementen in der Zeile und Spalte: der erste Zeileneintrag mit dem ersten Spalten Eintrag, der zweite Zeileneintrag mit dem zweiten Spalten Eintrag usw.</span><span class="sxs-lookup"><span data-stu-id="2b942-145">Multiply each pair of elements in the row and column: the first row entry by the first column entry, the second row entry by the second column entry, and so forth.</span></span>
3.  <span data-ttu-id="2b942-146">Addieren Sie das Ergebnis.</span><span class="sxs-lookup"><span data-stu-id="2b942-146">Sum the result.</span></span>

<span data-ttu-id="2b942-147">Im folgenden finden Sie ein Beispiel für das Multiplizieren einer (2 × 2) Matrix mit einer Matrix (2 × 3).</span><span class="sxs-lookup"><span data-stu-id="2b942-147">Here is an example of multiplying a (2 × 2) matrix by a (2 × 3) matrix.</span></span>

![Matrix Multiplikation.](images/matrix03.png)

<span data-ttu-id="2b942-149">Die Matrix Multiplikation ist nicht kommutativ.</span><span class="sxs-lookup"><span data-stu-id="2b942-149">Matrix multiplication is not commutative.</span></span> <span data-ttu-id="2b942-150">Das heißt, ein × b ≠ B × a. Aus der Definition folgt auch, dass nicht jedes Matrizen paar multipliziert werden kann.</span><span class="sxs-lookup"><span data-stu-id="2b942-150">That is, A × B ≠ B × A. Also, from the definition it follows that not every pair of matrices can be multiplied.</span></span> <span data-ttu-id="2b942-151">Die Anzahl der Spalten in der linken Matrix muss gleich der Anzahl der Zeilen in der rechten Matrix sein.</span><span class="sxs-lookup"><span data-stu-id="2b942-151">The number of columns in the left-hand matrix must equal the number of rows in the right-hand matrix.</span></span> <span data-ttu-id="2b942-152">Andernfalls ist der ×-Operator nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="2b942-152">Otherwise, the × operator is not defined.</span></span>

<span data-ttu-id="2b942-153">*Identifizieren* Sie die Matrix.</span><span class="sxs-lookup"><span data-stu-id="2b942-153">*Identify matrix*.</span></span> <span data-ttu-id="2b942-154">Eine Identitätsmatrix, die als I bezeichnet wird, ist eine quadratische Matrix, die wie folgt definiert wird:</span><span class="sxs-lookup"><span data-stu-id="2b942-154">An identity matrix, designated I, is a square matrix defined as follows:</span></span>

<dl> <span data-ttu-id="2b942-155">Ich habe "*IJ* = 1", wenn *i*  =  *j*, andernfalls "0".</span><span class="sxs-lookup"><span data-stu-id="2b942-155">I *ij* = 1 if *i* = *j*, or 0 otherwise.</span></span>  
</dl>

<span data-ttu-id="2b942-156">Mit anderen Worten: eine Identitätsmatrix enthält 1 für jedes Element, bei dem die Zeilennummer gleich der Spaltennummer ist, und 0 für alle anderen Elemente.</span><span class="sxs-lookup"><span data-stu-id="2b942-156">In other words, an identity matrix contains 1 for each element where the row number equals the column number, and zero for all other elements.</span></span> <span data-ttu-id="2b942-157">Hier ist beispielsweise die 3 × 3-Identitätsmatrix.</span><span class="sxs-lookup"><span data-stu-id="2b942-157">For example, here is the 3 × 3 identity matrix.</span></span>

![Identitätsmatrix.](images/matrix04.png)

<span data-ttu-id="2b942-159">Die folgenden equalitäten enthalten für jede Matrix M.</span><span class="sxs-lookup"><span data-stu-id="2b942-159">The following equalities hold for any matrix M.</span></span>

<dl> <span data-ttu-id="2b942-160">M x I = m</span><span class="sxs-lookup"><span data-stu-id="2b942-160">M x I = M</span></span>  
<span data-ttu-id="2b942-161">I x m = m</span><span class="sxs-lookup"><span data-stu-id="2b942-161">I x M = M</span></span>  
</dl>

## <a name="affine-transforms"></a><span data-ttu-id="2b942-162">Affine Transformationen</span><span class="sxs-lookup"><span data-stu-id="2b942-162">Affine Transforms</span></span>

<span data-ttu-id="2b942-163">Eine *affine Transformation* ist ein mathematischer Vorgang, der einen Koordinatenraum einem anderen zuordnet.</span><span class="sxs-lookup"><span data-stu-id="2b942-163">An *affine transform* is a mathematical operation that maps one coordinate space to another.</span></span> <span data-ttu-id="2b942-164">Anders ausgedrückt, ordnet Sie einen Satz von Punkten einem anderen Satz von Punkten zu.</span><span class="sxs-lookup"><span data-stu-id="2b942-164">In other words, it maps one set of points to another set of points.</span></span> <span data-ttu-id="2b942-165">Affine Transformationen verfügen über einige Features, die Sie in Computergrafiken nützlich machen.</span><span class="sxs-lookup"><span data-stu-id="2b942-165">Affine transforms have some features that make them useful in computer graphics.</span></span>

-   <span data-ttu-id="2b942-166">Affine Transformationen bewahren die *Granularität*.</span><span class="sxs-lookup"><span data-stu-id="2b942-166">Affine transforms preserve *collinearity*.</span></span> <span data-ttu-id="2b942-167">Wenn drei oder mehr Punkte in eine Linie fallen, bilden Sie nach der Transformation weiterhin eine Zeile.</span><span class="sxs-lookup"><span data-stu-id="2b942-167">If three or more points fall on a line, they still form a line after the transformation.</span></span> <span data-ttu-id="2b942-168">Gerade Linien bleiben gleich.</span><span class="sxs-lookup"><span data-stu-id="2b942-168">Straight lines remain straight.</span></span>
-   <span data-ttu-id="2b942-169">Die Komposition zweier affininer Transformationen ist eine affine Transformation.</span><span class="sxs-lookup"><span data-stu-id="2b942-169">The composition of two affine transforms is an affine transform.</span></span>

<span data-ttu-id="2b942-170">Affine Transformationen für 2D-Raum weisen die folgende Form auf:</span><span class="sxs-lookup"><span data-stu-id="2b942-170">Affine transforms for 2-D space have the following form.</span></span>

![Zeigt eine affine Transformation für 2-D-Raum.](images/matrix05.png)

<span data-ttu-id="2b942-172">Wenn Sie die zuvor angegebene Definition der Matrix Multiplikation anwenden, können Sie anzeigen, dass das Produkt von zwei affinen Transformationen eine weitere affine Transformation ist.</span><span class="sxs-lookup"><span data-stu-id="2b942-172">If you apply the definition of matrix multiplication given earlier, you can show that the product of two affine transforms is another affine transform.</span></span> <span data-ttu-id="2b942-173">Um einen 2D-Punkt mithilfe einer affinen Transformation zu transformieren, wird der Punkt als 1 × 3-Matrix dargestellt.</span><span class="sxs-lookup"><span data-stu-id="2b942-173">To transform a 2D point using an affine transform, the point is represented as a 1 × 3 matrix.</span></span>

<dl> <span data-ttu-id="2b942-174">P = \| x y 1 \|</span><span class="sxs-lookup"><span data-stu-id="2b942-174">P = \| x y 1 \|</span></span>  
</dl>

<span data-ttu-id="2b942-175">Die ersten beiden Elemente enthalten die x-und y-Koordinaten des Punkts.</span><span class="sxs-lookup"><span data-stu-id="2b942-175">The first two elements contain the x and y coordinates of the point.</span></span> <span data-ttu-id="2b942-176">Der Wert 1 wird in das dritte Element eingefügt, damit das mathematische Element ordnungsgemäß funktioniert.</span><span class="sxs-lookup"><span data-stu-id="2b942-176">The 1 is placed in the third element to make the math work out correctly.</span></span> <span data-ttu-id="2b942-177">Um die Transformation anzuwenden, Multiplizieren Sie die beiden Matrizen wie folgt.</span><span class="sxs-lookup"><span data-stu-id="2b942-177">To apply the transform, multiply the two matrices as follows.</span></span>

<dl> <span data-ttu-id="2b942-178">p ' = p × M</span><span class="sxs-lookup"><span data-stu-id="2b942-178">P' = P × M</span></span>  
</dl>

<span data-ttu-id="2b942-179">Dies wird wie folgt erweitert.</span><span class="sxs-lookup"><span data-stu-id="2b942-179">This expands to the following.</span></span>

![affine Transformation.](images/matrix06.png)

<span data-ttu-id="2b942-181">where</span><span class="sxs-lookup"><span data-stu-id="2b942-181">where</span></span>

<dl> <span data-ttu-id="2b942-182">x ' = AX + CY + e</span><span class="sxs-lookup"><span data-stu-id="2b942-182">x' = ax + cy + e</span></span>  
<span data-ttu-id="2b942-183">y ' = BX + dy + f</span><span class="sxs-lookup"><span data-stu-id="2b942-183">y' = bx + dy + f</span></span>  
</dl>

<span data-ttu-id="2b942-184">Um den transformierten Punkt zu erhalten, nehmen Sie die ersten beiden Elemente von Matrix P '.</span><span class="sxs-lookup"><span data-stu-id="2b942-184">To get the transformed point, take the first two elements of matrix P'.</span></span>

<dl> <span data-ttu-id="2b942-185">p = (x ', y ') = (AX + CY + e, BX + dy + f)</span><span class="sxs-lookup"><span data-stu-id="2b942-185">p = (x', y') = (ax + cy + e, bx + dy + f)</span></span>  
</dl>

> [!Note]  
> <span data-ttu-id="2b942-186">Eine Matrix mit 1 × *n* wird als *Zeilen Vektor* bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="2b942-186">A 1 × *n* matrix is called a *row vector*.</span></span> <span data-ttu-id="2b942-187">Direct2D und Direct3D verwenden Zeilen Vektoren zur Darstellung von Punkten im 2D-oder 3D-Raum.</span><span class="sxs-lookup"><span data-stu-id="2b942-187">Direct2D and Direct3D both use row vectors to represent points in 2D or 3D space.</span></span> <span data-ttu-id="2b942-188">Sie können ein entsprechendes Ergebnis mit einem Spalten Vektor (*n* × 1) und der Transformation der Transformationsmatrix erhalten.</span><span class="sxs-lookup"><span data-stu-id="2b942-188">You can get an equivalent result by using a column vector (*n* × 1) and transposing the transform matrix.</span></span> <span data-ttu-id="2b942-189">In den meisten Grafik Texten wird das Spalten Vektor Formular verwendet.</span><span class="sxs-lookup"><span data-stu-id="2b942-189">Most graphics texts use the column vector form.</span></span> <span data-ttu-id="2b942-190">In diesem Thema wird das Zeilen Vektor Formular für Konsistenz mit Direct2D und Direct3D dargestellt.</span><span class="sxs-lookup"><span data-stu-id="2b942-190">This topic presents the row vector form for consistency with Direct2D and Direct3D.</span></span>

 

<span data-ttu-id="2b942-191">In den nächsten Abschnitten werden die grundlegenden Transformationen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="2b942-191">The next several sections derive the basic transforms.</span></span>

### <a name="translation-transform"></a><span data-ttu-id="2b942-192">Übersetzungs Transformation</span><span class="sxs-lookup"><span data-stu-id="2b942-192">Translation Transform</span></span>

<span data-ttu-id="2b942-193">Die Übersetzungs Transformationsmatrix weist das folgende Format auf.</span><span class="sxs-lookup"><span data-stu-id="2b942-193">The translation transform matrix has the following form.</span></span>

![Übersetzungs Transformation.](images/matrix07.png)

<span data-ttu-id="2b942-195">Das Plugging eines Punkt- *P* in diese Gleichung ergibt folgendes:</span><span class="sxs-lookup"><span data-stu-id="2b942-195">Plugging a point *P* into this equation yields:</span></span>

<dl> <span data-ttu-id="2b942-196">P ' = (*x*  +  *DX*, *y*  +  *dy*)</span><span class="sxs-lookup"><span data-stu-id="2b942-196">P' = (*x* + *dx*, *y* + *dy*)</span></span>
</dl>

<span data-ttu-id="2b942-197">Dies entspricht dem Punkt (x, y), der von *DX* in der x-Achse und *dy* auf der y-Achse übersetzt wurde.</span><span class="sxs-lookup"><span data-stu-id="2b942-197">which corresponds to the point (x, y) translated by *dx* in the X-axis and *dy* in the Y-axis.</span></span>

![ein Diagramm, das die Übersetzung von zwei Punkten anzeigt.](images/graphics22.png)

### <a name="scaling-transform"></a><span data-ttu-id="2b942-199">Skalierungs Transformation</span><span class="sxs-lookup"><span data-stu-id="2b942-199">Scaling Transform</span></span>

<span data-ttu-id="2b942-200">Die Matrix der Skalierungs Transformation weist das folgende Format auf.</span><span class="sxs-lookup"><span data-stu-id="2b942-200">The scaling transform matrix has the following form.</span></span>

![Skalierungs Transformation.](images/matrix09.png)

<span data-ttu-id="2b942-202">Das Plugging eines Punkt- *P* in diese Gleichung ergibt folgendes:</span><span class="sxs-lookup"><span data-stu-id="2b942-202">Plugging a point *P* into this equation yields:</span></span>

<dl> <span data-ttu-id="2b942-203">P ' = (*x* ∙ *DX*, *y* ∙ *dy*)</span><span class="sxs-lookup"><span data-stu-id="2b942-203">P' = (*x* ∙ *dx*, *y* ∙ *dy*)</span></span>
</dl>

<span data-ttu-id="2b942-204">Dies entspricht dem Punkt (x, y), der von *DX* und *dy* skaliert wird.</span><span class="sxs-lookup"><span data-stu-id="2b942-204">which corresponds to the point (x,y) scaled by *dx* and *dy*.</span></span>

![ein Diagramm, das die Skalierung von zwei Punkten anzeigt.](images/graphics23.png)

### <a name="rotation-around-the-origin"></a><span data-ttu-id="2b942-206">Drehung um den Ursprung</span><span class="sxs-lookup"><span data-stu-id="2b942-206">Rotation Around the Origin</span></span>

<span data-ttu-id="2b942-207">Die Matrix zum Drehen eines Punkts um den Ursprung weist das folgende Format auf.</span><span class="sxs-lookup"><span data-stu-id="2b942-207">The matrix to rotate a point around the origin has the following form.</span></span>

![Zeigt eine Formel für eine Drehungs Transformation an.](images/matrix11.png)

<span data-ttu-id="2b942-209">Der transformierte Punkt ist:</span><span class="sxs-lookup"><span data-stu-id="2b942-209">The transformed point is:</span></span>

<dl> <span data-ttu-id="2b942-210">P ' = (*x* cos;– ysin-, *x* Sin;+ *y*-Nr.)</span><span class="sxs-lookup"><span data-stu-id="2b942-210">P' = (*x* cosΘ – ysinΘ, *x* sinΘ + *y* cosΘ)</span></span>
</dl>

<span data-ttu-id="2b942-211">Fest.</span><span class="sxs-lookup"><span data-stu-id="2b942-211">Proof.</span></span> <span data-ttu-id="2b942-212">Um anzuzeigen, dass P "eine Drehung darstellt, sollten Sie das folgende Diagramm in Erwägung gezogen.</span><span class="sxs-lookup"><span data-stu-id="2b942-212">To show that P' represents a rotation, consider the following diagram.</span></span>

![ein Diagramm, das die Drehung um den Ursprung anzeigt.](images/graphics24.png)

<span data-ttu-id="2b942-214">Gegeben:</span><span class="sxs-lookup"><span data-stu-id="2b942-214">Given:</span></span>

<dl> <dt>

<span data-ttu-id="2b942-215"><span id="P____x_y_"></span><span id="p____x_y_"></span><span id="P____X_Y_"></span>P = (x, y)</span><span class="sxs-lookup"><span data-stu-id="2b942-215"><span id="P____x_y_"></span><span id="p____x_y_"></span><span id="P____X_Y_"></span>P = (x,y)</span></span>
</dt> <dd>

<span data-ttu-id="2b942-216">Der ursprüngliche Punkt, der transformiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="2b942-216">The original point to transform.</span></span>

</dd> <dt>

<span data-ttu-id="2b942-217">Dargestellt</span><span class="sxs-lookup"><span data-stu-id="2b942-217">Φ</span></span>
</dt> <dd>

<span data-ttu-id="2b942-218">Der Winkel, der durch die Zeile (0,0) bis P gebildet wird.</span><span class="sxs-lookup"><span data-stu-id="2b942-218">The angle formed by the line (0,0) to P.</span></span>

</dd> <dt>

<span data-ttu-id="2b942-219">COS</span><span class="sxs-lookup"><span data-stu-id="2b942-219">Θ</span></span>
</dt> <dd>

<span data-ttu-id="2b942-220">Der Winkel, um den (x, y) zum Ursprung gedreht werden soll.</span><span class="sxs-lookup"><span data-stu-id="2b942-220">The angle by which to rotate (x,y) about the origin.</span></span>

</dd> <dt>

<span data-ttu-id="2b942-221"><span id="P_____x__y__"></span><span id="p_____x__y__"></span><span id="P_____X__Y__"></span>P ' = (x ', y ')</span><span class="sxs-lookup"><span data-stu-id="2b942-221"><span id="P_____x__y__"></span><span id="p_____x__y__"></span><span id="P_____X__Y__"></span>P' = (x',y')</span></span>
</dt> <dd>

<span data-ttu-id="2b942-222">Der transformierte Punkt.</span><span class="sxs-lookup"><span data-stu-id="2b942-222">The transformed point.</span></span>

</dd> <dt>

<span data-ttu-id="2b942-223"><span id="R"></span><span id="r"></span>R</span><span class="sxs-lookup"><span data-stu-id="2b942-223"><span id="R"></span><span id="r"></span>R</span></span>
</dt> <dd>

<span data-ttu-id="2b942-224">Die Länge der Zeile (0,0) bis P. Auch der Radius des Kreises der Drehung.</span><span class="sxs-lookup"><span data-stu-id="2b942-224">The length of the line (0,0) to P. Also the radius of the circle of rotation.</span></span>

</dd> </dl>

> [!Note]  
> <span data-ttu-id="2b942-225">Dieses Diagramm verwendet das in Geometry verwendete Standard Koordinatensystem, bei dem die positive y-Achse nach oben zeigt.</span><span class="sxs-lookup"><span data-stu-id="2b942-225">This diagram uses the standard coordinate system used in geometry, where the positive y-axis points up.</span></span> <span data-ttu-id="2b942-226">Direct2D verwendet das Windows-Koordinatensystem, bei dem die positive y-Achse nach unten zeigt.</span><span class="sxs-lookup"><span data-stu-id="2b942-226">Direct2D uses the Windows coordinate system, where the positive y-axis points down.</span></span>

 

<span data-ttu-id="2b942-227">Der Winkel zwischen der x-Achse und der Zeile (0, 0) bis P ' ist. +.</span><span class="sxs-lookup"><span data-stu-id="2b942-227">The angle between the x-axis and the line (0,0) to P' is Φ + Θ.</span></span> <span data-ttu-id="2b942-228">Die folgenden Identitäten enthalten:</span><span class="sxs-lookup"><span data-stu-id="2b942-228">The following identities hold:</span></span>

<dl> <span data-ttu-id="2b942-229">x = R.</span><span class="sxs-lookup"><span data-stu-id="2b942-229">x = R cosΦ</span></span>  
<span data-ttu-id="2b942-230">y = R</span><span class="sxs-lookup"><span data-stu-id="2b942-230">y = R sinΦ</span></span>  
<span data-ttu-id="2b942-231">x ' = R cos (es +-Taste)</span><span class="sxs-lookup"><span data-stu-id="2b942-231">x' = R cos(Φ + Θ)</span></span>  
<span data-ttu-id="2b942-232">y ' = R Sin (es +-Taste)</span><span class="sxs-lookup"><span data-stu-id="2b942-232">y' = R sin(Φ+ Θ)</span></span>  
</dl>

<span data-ttu-id="2b942-233">Lösen Sie nun für x ' und y ' in Bezug auf den Bereich.</span><span class="sxs-lookup"><span data-stu-id="2b942-233">Now solve for x' and y' in terms of Θ.</span></span> <span data-ttu-id="2b942-234">Durch die dreisprachigen Additions Formeln:</span><span class="sxs-lookup"><span data-stu-id="2b942-234">By the trigonometric addition formulas:</span></span>

<dl> <span data-ttu-id="2b942-235">x ' = R (COS;cos;– Sin;Sin;) = rcos;cos. – rsin;Sin;</span><span class="sxs-lookup"><span data-stu-id="2b942-235">x' = R(cosΦcosΘ – sinΦsinΘ) = RcosΦcosΘ – RsinΦsinΘ</span></span>  
<span data-ttu-id="2b942-236">y ' = R (SIN;COS;+ cos;Sin;) = rsin;cos;+ rcos;Sin;</span><span class="sxs-lookup"><span data-stu-id="2b942-236">y' = R(sinΦcosΘ + cosΦsinΘ) = RsinΦcosΘ + RcosΦsinΘ</span></span>  
</dl>

<span data-ttu-id="2b942-237">Dabei wird Folgendes ersetzt:</span><span class="sxs-lookup"><span data-stu-id="2b942-237">Substituting, we get:</span></span>

<dl> <span data-ttu-id="2b942-238">x ' = xcos;– ysin;</span><span class="sxs-lookup"><span data-stu-id="2b942-238">x' = xcosΘ – ysinΘ</span></span>  
<span data-ttu-id="2b942-239">y ' = xsin;+ ycos;</span><span class="sxs-lookup"><span data-stu-id="2b942-239">y' = xsinΘ + ycosΘ</span></span>  
</dl>

<span data-ttu-id="2b942-240">Dies entspricht dem zuvor gezeigten transformierten Punkt P.</span><span class="sxs-lookup"><span data-stu-id="2b942-240">which corresponds to the transformed point P' shown earlier.</span></span>

### <a name="rotation-around-an-arbitrary-point"></a><span data-ttu-id="2b942-241">Drehung um einen beliebigen Punkt</span><span class="sxs-lookup"><span data-stu-id="2b942-241">Rotation Around an Arbitrary Point</span></span>

<span data-ttu-id="2b942-242">Um einen anderen Punkt (x, y) als den Ursprung zu drehen, wird die folgende Matrix verwendet.</span><span class="sxs-lookup"><span data-stu-id="2b942-242">To rotate around a point (x,y) other than the origin, the following matrix is used.</span></span>

![Drehungs Transformation.](images/matrix13.png)

<span data-ttu-id="2b942-244">Sie können diese Matrix ableiten, indem Sie den Punkt (x, y) als Ursprung nehmen.</span><span class="sxs-lookup"><span data-stu-id="2b942-244">You can derive this matrix by taking the point (x,y) to be the origin.</span></span>

![ein Diagramm, das die Drehung um einen Punkt zeigt.](images/graphics25.png)

<span data-ttu-id="2b942-246">Let (x1, Y1) ist der Punkt, der sich aus dem Drehen des Punkts (X0, Y0) um den Punkt (x, y) ergibt.</span><span class="sxs-lookup"><span data-stu-id="2b942-246">Let (x1, y1) be the point that results from rotating the point (x0, y0) around the point (x,y).</span></span> <span data-ttu-id="2b942-247">Wir können x1 wie folgt ableiten.</span><span class="sxs-lookup"><span data-stu-id="2b942-247">We can derive x1 as follows.</span></span>

<dl> <span data-ttu-id="2b942-248">x1 = (X0 – x) cos;– (y0 – y) sin;+ x</span><span class="sxs-lookup"><span data-stu-id="2b942-248">x1 = (x0 – x)cosΘ– (y0 – y)sinΘ + x</span></span>  
<span data-ttu-id="2b942-249">x1 = x0cosΘ – y0sinΘ + \[ (1 – cosbe) + ysin; \]</span><span class="sxs-lookup"><span data-stu-id="2b942-249">x1 = x0cosΘ – y0sinΘ + \[ (1 – cosΘ) + ysinΘ \]</span></span>  
</dl>

<span data-ttu-id="2b942-250">Binden Sie diese Gleichung nun wieder in die Transformationsmatrix ein, indem Sie die Formel x1 = ax0 + cy0 + e aus früheren Versionen verwenden.</span><span class="sxs-lookup"><span data-stu-id="2b942-250">Now plug this equation back into the transform matrix, using the formula x1 = ax0 + cy0 + e from earlier.</span></span> <span data-ttu-id="2b942-251">Verwenden Sie das gleiche Verfahren, um Y1 abzuleiten.</span><span class="sxs-lookup"><span data-stu-id="2b942-251">Use the same procedure to derive y1.</span></span>

### <a name="skew-transform"></a><span data-ttu-id="2b942-252">Verzerrungs Transformation</span><span class="sxs-lookup"><span data-stu-id="2b942-252">Skew Transform</span></span>

<span data-ttu-id="2b942-253">Die Schiefe Transformation wird durch vier Parameter definiert:</span><span class="sxs-lookup"><span data-stu-id="2b942-253">The skew transform is defined by four parameters:</span></span>

-   <span data-ttu-id="2b942-254">$: Der Betrag, der entlang der x-Achse verzerrt werden soll, gemessen als Winkel von der y-Achse.</span><span class="sxs-lookup"><span data-stu-id="2b942-254">Θ: The amount to skew along the x-axis, measured as an angle from the y-axis.</span></span>
-   <span data-ttu-id="2b942-255">Ge: der Betrag, der entlang der y-Achse verzerrt werden soll, gemessen als Winkel von der x-Achse.</span><span class="sxs-lookup"><span data-stu-id="2b942-255">Φ: The amount to skew along the y-axis, measured as an angle from the x-axis.</span></span>
-   <span data-ttu-id="2b942-256">(*px*, *py*): die x-und y-Koordinaten des Punkts, an dem die Schiefe ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2b942-256">(*px*, *py*): The x- and y-coordinates of the point about which the skew is performed.</span></span>

<span data-ttu-id="2b942-257">Die Schiefe Transformation verwendet die folgende Matrix.</span><span class="sxs-lookup"><span data-stu-id="2b942-257">The skew transform uses the following matrix.</span></span>

![Schiefe-Transformation.](images/matrix14.png)

<span data-ttu-id="2b942-259">Der transformierte Punkt ist:</span><span class="sxs-lookup"><span data-stu-id="2b942-259">The transformed point is:</span></span>

<dl> <span data-ttu-id="2b942-260">P ' = (*x*  +  *y* Tangente – *py* tantzte, *y*  +  *x* Tangens) – *py* Tangens</span><span class="sxs-lookup"><span data-stu-id="2b942-260">P' = (*x* + *y* tanΘ – *py* tanΘ, *y* + *x* tanΦ) – *py* tanΦ</span></span>
</dl>

<span data-ttu-id="2b942-261">oder gleichwertig:</span><span class="sxs-lookup"><span data-stu-id="2b942-261">or equivalently:</span></span>

<dl> <span data-ttu-id="2b942-262">P ' = (*x* + (*y* – *py*) Tangente, *y* + (*x* – *px*) Tangens)</span><span class="sxs-lookup"><span data-stu-id="2b942-262">P' = (*x* + (*y* – *py*)tanΘ, *y* + (*x* – *px*)tanΦ)</span></span>
</dl>

<span data-ttu-id="2b942-263">Um zu sehen, wie diese Transformation funktioniert, sollten Sie jede Komponente einzeln in Erwägung gezogen.</span><span class="sxs-lookup"><span data-stu-id="2b942-263">To see how this transform works, consider each component individually.</span></span> <span data-ttu-id="2b942-264">Der Parameter "-Parameter" verschiebt jeden Punkt in der x-Richtung um einen Betrag, der gleich der Tand ist.</span><span class="sxs-lookup"><span data-stu-id="2b942-264">The Θ parameter moves every point in the x direction by an amount equal to tanΘ.</span></span> <span data-ttu-id="2b942-265">Das folgende Diagramm zeigt die Beziehung zwischen der-und der-Achse der x-Achse.</span><span class="sxs-lookup"><span data-stu-id="2b942-265">The following diagram shows the relation between Θ and the x-axis skew.</span></span>

![Diagramm, das die Schiefe entlang der x-Achse anzeigt.](images/graphics26.png)

<span data-ttu-id="2b942-267">Dies ist die gleiche Schiefe, die auf ein Rechteck angewendet wird:</span><span class="sxs-lookup"><span data-stu-id="2b942-267">Here is the same skew applied to a rectangle:</span></span>

![Diagramm, das die Schiefe entlang der x-Achse anzeigt, wenn es auf ein Rechteck angewendet wird.](images/graphics27.png)

<span data-ttu-id="2b942-269">Der-Parameter hat denselben Effekt, aber entlang der y-Achse:</span><span class="sxs-lookup"><span data-stu-id="2b942-269">The Φ parameter has the same effect, but along the y-axis:</span></span>

![Diagramm, das die Schiefe entlang der y-Achse anzeigt.](images/graphics28.png)

<span data-ttu-id="2b942-271">Das nächste Diagramm zeigt die auf ein Rechteck angewendete y-Achsen Schiefe.</span><span class="sxs-lookup"><span data-stu-id="2b942-271">The next diagram shows y-axis skew applied to a rectangle.</span></span>

![Diagramm, das die Schiefe entlang der y-Achse anzeigt, wenn es auf ein Rechteck angewendet wird.](images/graphics29.png)

<span data-ttu-id="2b942-273">Schließlich verschieben die Parameter *px* und *py* den Mittelpunkt für die Schiefe entlang der x-und y-Achse.</span><span class="sxs-lookup"><span data-stu-id="2b942-273">Finally, the parameters *px* and *py* shift the center point for the skew along the x- and y-axes.</span></span>

## <a name="representing-transforms-in-direct2d"></a><span data-ttu-id="2b942-274">Darstellen von Transformationen in Direct2D</span><span class="sxs-lookup"><span data-stu-id="2b942-274">Representing Transforms in Direct2D</span></span>

<span data-ttu-id="2b942-275">Alle Direct2D-Transformationen sind affine Transformationen.</span><span class="sxs-lookup"><span data-stu-id="2b942-275">All Direct2D transforms are affine transforms.</span></span> <span data-ttu-id="2b942-276">Direct2D unterstützt keine nicht affinen Transformationen.</span><span class="sxs-lookup"><span data-stu-id="2b942-276">Direct2D does not support non-affine transforms.</span></span> <span data-ttu-id="2b942-277">Transformationen werden durch die [**D2D1 \_ Matrix \_ 3x2 \_ F-**](/windows/desktop/Direct2D/d2d1-matrix-3x2-f) Struktur dargestellt.</span><span class="sxs-lookup"><span data-stu-id="2b942-277">Transforms are represented by the [**D2D1\_MATRIX\_3X2\_F**](/windows/desktop/Direct2D/d2d1-matrix-3x2-f) structure.</span></span> <span data-ttu-id="2b942-278">Diese Struktur definiert eine 3 × 2-Matrix.</span><span class="sxs-lookup"><span data-stu-id="2b942-278">This structure defines a 3 × 2 matrix.</span></span> <span data-ttu-id="2b942-279">Da die dritte Spalte einer affinen Transformation immer identisch ist ( \[ 0, 0, 1 \] ) und da Direct2D keine nicht affinen Transformationen unterstützt, ist es nicht erforderlich, die gesamte 3 × 3-Matrix anzugeben.</span><span class="sxs-lookup"><span data-stu-id="2b942-279">Because the third column of an affine transform is always the same (\[0, 0, 1\]), and because Direct2D does not support non-affine transforms, there is no need to specify the entire 3 × 3 matrix.</span></span> <span data-ttu-id="2b942-280">Intern verwendet Direct2D 3 × 3 Matrizen, um die Transformationen zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="2b942-280">Internally, Direct2D uses 3 × 3 matrices to compute the transforms.</span></span>

<span data-ttu-id="2b942-281">Die Member der [**D2D1 \_ Matrix \_ 3x2 \_ F**](/windows/desktop/Direct2D/d2d1-matrix-3x2-f) werden gemäß ihrer Indexposition benannt: das **\_ 11** -Element ist Element (1, 1), der **\_ 12** -Member ist Element (1, 2) usw.</span><span class="sxs-lookup"><span data-stu-id="2b942-281">The members of the [**D2D1\_MATRIX\_3X2\_F**](/windows/desktop/Direct2D/d2d1-matrix-3x2-f) are named according to their index position: the **\_11** member is element (1,1), the **\_12** member is element (1,2), and so forth.</span></span> <span data-ttu-id="2b942-282">Obwohl Sie die Strukturmember direkt initialisieren können, empfiehlt es sich, die [**D2D1:: Matrix3x2F**](/windows/desktop/api/d2d1helper/nl-d2d1helper-matrix3x2f) -Klasse zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="2b942-282">Although you can initialize the structure members directly, it is recommended to use the [**D2D1::Matrix3x2F**](/windows/desktop/api/d2d1helper/nl-d2d1helper-matrix3x2f) class.</span></span> <span data-ttu-id="2b942-283">Diese Klasse erbt **D2D1 \_ Matrix \_ 3x2 \_ F** und stellt Hilfsmethoden zum Erstellen einer der grundlegenden affinen Transformationen bereit.</span><span class="sxs-lookup"><span data-stu-id="2b942-283">This class inherits **D2D1\_MATRIX\_3X2\_F** and provides helper methods for creating any of the basic affine transforms.</span></span> <span data-ttu-id="2b942-284">Die-Klasse definiert auch [**Operator \* ()**](/windows/desktop/api/d2d1helper/nf-d2d1helper-matrix3x2f-operator-mult) zum Verfassen von zwei oder mehr Transformationen, wie in [Anwenden von Transformationen in Direct2D](applying-transforms-in-direct2d.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="2b942-284">The class also defines [**operator\*()**](/windows/desktop/api/d2d1helper/nf-d2d1helper-matrix3x2f-operator-mult) for composing two or more transforms, as described in [Applying Transforms in Direct2D](applying-transforms-in-direct2d.md).</span></span>

## <a name="next"></a><span data-ttu-id="2b942-285">Nächste</span><span class="sxs-lookup"><span data-stu-id="2b942-285">Next</span></span>

[<span data-ttu-id="2b942-286">Modul 4. Benutzereingabe</span><span class="sxs-lookup"><span data-stu-id="2b942-286">Module 4. User Input</span></span>](module-4--user-input.md)

 

 