---
description: Die Erörterung der weltweiten Transformation stellt grundlegende Konzepte vor und bietet ausführliche Informationen zum Einrichten einer weltweiten Transformation.
ms.assetid: c3d3b247-e482-4750-a6fb-724f81ee2b19
title: Welt Transformation (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e192f8ce4350c767122ef60f3cd36777753d2e22
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392414"
---
# <a name="world-transform-direct3d-9"></a><span data-ttu-id="5e9d3-103">Welt Transformation (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="5e9d3-103">World Transform (Direct3D 9)</span></span>

<span data-ttu-id="5e9d3-104">Die Erörterung der weltweiten Transformation stellt grundlegende Konzepte vor und bietet ausführliche Informationen zum Einrichten einer weltweiten Transformation.</span><span class="sxs-lookup"><span data-stu-id="5e9d3-104">The discussion of the world transformation introduces basic concepts and provides details on how to set up a world transform.</span></span>

## <a name="what-is-a-world-transform"></a><span data-ttu-id="5e9d3-105">Was ist eine Welt Transformation?</span><span class="sxs-lookup"><span data-stu-id="5e9d3-105">What Is a World Transform?</span></span>

<span data-ttu-id="5e9d3-106">Eine Welt transformiert Änderungen an den Koordinaten des Modell Raums, wobei Scheitel Punkte in Bezug auf den lokalen Ursprung eines Modells definiert werden, in den Raum, in dem Vertices relativ zu einem Ursprung definiert werden, der von allen Objekten in einer Szene gemeinsam genutzt wird.</span><span class="sxs-lookup"><span data-stu-id="5e9d3-106">A world transform changes coordinates from model space, where vertices are defined relative to a model's local origin, to World Space, where vertices are defined relative to an origin common to all the objects in a scene.</span></span> <span data-ttu-id="5e9d3-107">Im Grunde stellt die Welt Transformation ein Modell in die Welt. Daher ist der Name.</span><span class="sxs-lookup"><span data-stu-id="5e9d3-107">In essence, the world transform places a model into the world; hence its name.</span></span> <span data-ttu-id="5e9d3-108">Das folgende Diagramm zeigt die Beziehung zwischen dem Weltkoordinaten System und dem lokalen Koordinatensystem eines Modells.</span><span class="sxs-lookup"><span data-stu-id="5e9d3-108">The following diagram shows the relationship between the world coordinate system and a model's local coordinate system.</span></span>

![Diagramm der Beziehung zwischen globalen Koordinaten und lokalen Koordinaten](images/worldcrd.png)

<span data-ttu-id="5e9d3-110">Die globale Transformation kann eine beliebige Kombination von Übersetzungen, Drehungen und Skalierungen enthalten.</span><span class="sxs-lookup"><span data-stu-id="5e9d3-110">The world transform can include any combination of translations, rotations, and scalings.</span></span>

## <a name="setting-up-a-world-matrix"></a><span data-ttu-id="5e9d3-111">Einrichten einer Welt Matrix</span><span class="sxs-lookup"><span data-stu-id="5e9d3-111">Setting Up a World Matrix</span></span>

<span data-ttu-id="5e9d3-112">Wie bei jeder anderen Transformation können Sie die Welt Transformation erstellen, indem Sie eine Reihe von Matrizen zu einer einzelnen Matrix verketten, die die Summe ihrer Auswirkungen enthält.</span><span class="sxs-lookup"><span data-stu-id="5e9d3-112">As with any other transform, create the world transform by concatenating a series of matrices into a single matrix that contains the sum total of their effects.</span></span> <span data-ttu-id="5e9d3-113">Im einfachsten Fall, wenn sich ein Modell am Ursprung der Welt befindet und seine lokalen Koordinatenachsen genauso wie der Raum Raum ausgerichtet sind, ist die Weltmatrix die Identitätsmatrix.</span><span class="sxs-lookup"><span data-stu-id="5e9d3-113">In the simplest case, when a model is at the world origin and its local coordinate axes are oriented the same as world space, the world matrix is the identity matrix.</span></span> <span data-ttu-id="5e9d3-114">Im Allgemeinen ist die Weltmatrix eine Kombination aus einer Übersetzung in den Raum und möglicherweise eine oder mehrere Drehungen, um das Modell nach Bedarf zu ändern.</span><span class="sxs-lookup"><span data-stu-id="5e9d3-114">More commonly, the world matrix is a combination of a translation into world space and possibly one or more rotations to turn the model as needed.</span></span>

<span data-ttu-id="5e9d3-115">Das folgende Beispiel aus einer fiktiven 3D-Modell Klasse, die in C++ geschrieben ist, verwendet die Hilfsfunktionen, die in der D3DX Utility Library enthalten sind, um eine Weltmatrix zu erstellen, die drei Drehungen enthält, um ein Modell zu orientieren, und eine Übersetzung, um es relativ zu seiner Position im Raum zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="5e9d3-115">The following example, from a fictitious 3D model class written in C++, uses the helper functions included in the D3DX utility library to create a world matrix that includes three rotations to orient a model and a translation to relocate it relative to its position in world space.</span></span>


```
/*
 * For the purposes of this example, the following variables
 * are assumed to be valid and initialized.
 *
 * The m_xPos, m_yPos, m_zPos variables contain the model's
 * location in world coordinates.
 *
 * The m_fPitch, m_fYaw, and m_fRoll variables are floats that 
 * contain the model's orientation in terms of pitch, yaw, and roll
 * angles, in radians.
 */
 
void C3DModel::MakeWorldMatrix( D3DXMATRIX* pMatWorld )
{
    D3DXMATRIX MatTemp;  // Temp matrix for rotations.
    D3DXMATRIX MatRot;   // Final rotation matrix, applied to 
                         // pMatWorld.
 
    // Using the left-to-right order of matrix concatenation,
    // apply the translation to the object's world position
    // before applying the rotations.
    D3DXMatrixTranslation(pMatWorld, m_xPos, m_yPos, m_zPos);
    D3DXMatrixIdentity(&MatRot);

    // Now, apply the orientation variables to the world matrix
    if(m_fPitch || m_fYaw || m_fRoll) {
        // Produce and combine the rotation matrices.
        D3DXMatrixRotationX(&MatTemp, m_fPitch);         // Pitch
        D3DXMatrixMultiply(&MatRot, &MatRot, &MatTemp);
        D3DXMatrixRotationY(&MatTemp, m_fYaw);           // Yaw
        D3DXMatrixMultiply(&MatRot, &MatRot, &MatTemp);
        D3DXMatrixRotationZ(&MatTemp, m_fRoll);          // Roll
        D3DXMatrixMultiply(&MatRot, &MatRot, &MatTemp);
 
        // Apply the rotation matrices to complete the world matrix.
        D3DXMatrixMultiply(pMatWorld, &MatRot, pMatWorld);
    }
}
```



<span data-ttu-id="5e9d3-116">Nachdem Sie die World Matrix vorbereitet haben, müssen Sie die [**IDirect3DDevice9:: setTransform**](/windows/desktop/api) -Methode aufrufen, um Sie festzulegen, indem Sie das [**D3DTS \_ World**](d3dts-world.md) -Makro für den ersten Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="5e9d3-116">After you prepare the world matrix, call the [**IDirect3DDevice9::SetTransform**](/windows/desktop/api) method to set it, specifying the [**D3DTS\_WORLD**](d3dts-world.md) macro for the first parameter.</span></span>

> [!Note]  
> <span data-ttu-id="5e9d3-117">Direct3D verwendet die Welt-und Ansichts Matrizen, die Sie zum Konfigurieren mehrerer interner Datenstrukturen festgelegt haben.</span><span class="sxs-lookup"><span data-stu-id="5e9d3-117">Direct3D uses the world and view matrices that you set to configure several internal data structures.</span></span> <span data-ttu-id="5e9d3-118">Jedes Mal, wenn Sie eine neue Welt-oder Sicht Matrix festlegen, berechnet das System die zugeordneten internen Strukturen neu.</span><span class="sxs-lookup"><span data-stu-id="5e9d3-118">Each time you set a new world or view matrix, the system recalculates the associated internal structures.</span></span> <span data-ttu-id="5e9d3-119">Wenn Sie diese Matrizen häufig festlegen, z. b. Tausende Male pro Frame, ist dies Rechenzeit aufwändig.</span><span class="sxs-lookup"><span data-stu-id="5e9d3-119">Setting these matrices frequently-for example, thousands of times per frame-is computationally time-consuming.</span></span> <span data-ttu-id="5e9d3-120">Sie können die Anzahl der erforderlichen Berechnungen minimieren, indem Sie Ihre Welt und Matrizen in einer World-View-Matrix verketten, die Sie als Weltmatrix festlegen, und dann die Ansichts Matrix auf die Identität festlegen.</span><span class="sxs-lookup"><span data-stu-id="5e9d3-120">You can minimize the number of required calculations by concatenating your world and view matrices into a world-view matrix that you set as the world matrix, and then setting the view matrix to the identity.</span></span> <span data-ttu-id="5e9d3-121">Behalten Sie zwischengespeicherte Kopien der einzelnen Welt, und zeigen Sie Matrizen an, sodass Sie die World Matrix nach Bedarf ändern, verketten und zurücksetzen können.</span><span class="sxs-lookup"><span data-stu-id="5e9d3-121">Keep cached copies of individual world and view matrices so that you can modify, concatenate, and reset the world matrix as needed.</span></span> <span data-ttu-id="5e9d3-122">Aus Gründen der Übersichtlichkeit wird in dieser Dokumentation Direct3D Samples diese Optimierung nur selten nutzen.</span><span class="sxs-lookup"><span data-stu-id="5e9d3-122">For clarity, in this documentation Direct3D samples rarely employ this optimization.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="5e9d3-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5e9d3-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5e9d3-124">Transformationen</span><span class="sxs-lookup"><span data-stu-id="5e9d3-124">Transforms</span></span>](transforms.md)
</dt> </dl>

 

 



