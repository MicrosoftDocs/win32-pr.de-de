---
description: Die Erörterung der Welttransformation führt grundlegende Konzepte ein und enthält Details zum Einrichten einer Welttransformation.
ms.assetid: c3d3b247-e482-4750-a6fb-724f81ee2b19
title: World Transform (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfbddefbaa5ad4bd41e7dafa79e086605d8f40e761cca2bd6ce9b9c0b212950a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118518903"
---
# <a name="world-transform-direct3d-9"></a>World Transform (Direct3D 9)

Die Erörterung der Welttransformation führt grundlegende Konzepte ein und enthält Details zum Einrichten einer Welttransformation.

## <a name="what-is-a-world-transform"></a>Was ist eine Welttransformation?

Eine Welttransformation ändert Koordinaten vom Modellraum, in dem Scheitelpunkte relativ zum lokalen Ursprung eines Modells definiert werden, in World Space, wobei Scheitelpunkte relativ zu einem Ursprung definiert werden, der allen Objekten in einer Szene gemeinsam ist. Im Wesentlichen platziert die Welttransformation ein Modell in die Welt. daher sein Name. Das folgende Diagramm zeigt die Beziehung zwischen dem Weltkoordinatensystem und dem lokalen Koordinatensystem eines Modells.

![Diagramm der Beziehung zwischen Weltkoordinaten und lokalen Koordinaten](images/worldcrd.png)

Die Welttransformation kann eine beliebige Kombination aus Übersetzungen, Drehungen und Skalierungen umfassen.

## <a name="setting-up-a-world-matrix"></a>Einrichten einer Weltmatrix

Erstellen Sie wie bei jeder anderen Transformation die Welttransformation, indem Sie eine Reihe von Matrizen in eine einzelne Matrix verketten, die die Summe ihrer Effekte enthält. Im einfachsten Fall ist die Weltmatrix die Identitätsmatrix, wenn sich ein Modell am Ursprung der Welt befindet und seine lokalen Koordinatenachsen dem Weltraum entsprechen. In der Regel ist die Weltmatrix eine Kombination aus einer Übersetzung in den Weltraum und möglicherweise einer oder mehreren Drehungen, um das Modell nach Bedarf zu drehen.

Im folgenden Beispiel aus einer fiktiven 3D-Modellklasse, die in C++ geschrieben wurde, werden die Hilfsfunktionen verwendet, die in der Hilfsprogrammbibliothek D3DX enthalten sind, um eine Weltmatrix zu erstellen, die drei Drehungen enthält, um ein Modell zu orientieren, und eine Übersetzung, um es relativ zu seiner Position im Weltraum zu verschieben.


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



Nachdem Sie die Weltmatrix vorbereitet haben, rufen Sie die [**IDirect3DDevice9::SetTransform-Methode**](/windows/desktop/api) auf, um sie festzulegen, und geben Sie das [**D3DTS \_ WORLD-Makro**](d3dts-world.md) für den ersten Parameter an.

> [!Note]  
> Direct3D verwendet die Welt- und Ansichtsmatrizen, die Sie zum Konfigurieren mehrerer interner Datenstrukturen festgelegt haben. Jedes Mal, wenn Sie eine neue Welt oder Ansichtsmatrix festlegen, berechnet das System die zugeordneten internen Strukturen neu. Das häufige Festlegen dieser Matrizen , z. B. Tausende Male pro Frame, ist rechenintensiv. Sie können die Anzahl der erforderlichen Berechnungen minimieren, indem Sie Ihre Welt verketten und Matrizen in einer Weltansichtsmatrix anzeigen, die Sie als Weltmatrix festlegen, und dann die Ansichtsmatrix auf die Identität festlegen. Behalten Sie zwischengespeicherte Kopien einzelner Welten bei, und zeigen Sie Matrizen an, damit Sie die Weltmatrix nach Bedarf ändern, verketten und zurücksetzen können. Aus Gründen der Übersichtlichkeit verwenden Direct3D-Beispiele in dieser Dokumentation diese Optimierung selten.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Transformationen](transforms.md)
</dt> </dl>

 

 



