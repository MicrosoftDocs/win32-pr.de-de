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
# <a name="world-transform-direct3d-9"></a>Welt Transformation (Direct3D 9)

Die Erörterung der weltweiten Transformation stellt grundlegende Konzepte vor und bietet ausführliche Informationen zum Einrichten einer weltweiten Transformation.

## <a name="what-is-a-world-transform"></a>Was ist eine Welt Transformation?

Eine Welt transformiert Änderungen an den Koordinaten des Modell Raums, wobei Scheitel Punkte in Bezug auf den lokalen Ursprung eines Modells definiert werden, in den Raum, in dem Vertices relativ zu einem Ursprung definiert werden, der von allen Objekten in einer Szene gemeinsam genutzt wird. Im Grunde stellt die Welt Transformation ein Modell in die Welt. Daher ist der Name. Das folgende Diagramm zeigt die Beziehung zwischen dem Weltkoordinaten System und dem lokalen Koordinatensystem eines Modells.

![Diagramm der Beziehung zwischen globalen Koordinaten und lokalen Koordinaten](images/worldcrd.png)

Die globale Transformation kann eine beliebige Kombination von Übersetzungen, Drehungen und Skalierungen enthalten.

## <a name="setting-up-a-world-matrix"></a>Einrichten einer Welt Matrix

Wie bei jeder anderen Transformation können Sie die Welt Transformation erstellen, indem Sie eine Reihe von Matrizen zu einer einzelnen Matrix verketten, die die Summe ihrer Auswirkungen enthält. Im einfachsten Fall, wenn sich ein Modell am Ursprung der Welt befindet und seine lokalen Koordinatenachsen genauso wie der Raum Raum ausgerichtet sind, ist die Weltmatrix die Identitätsmatrix. Im Allgemeinen ist die Weltmatrix eine Kombination aus einer Übersetzung in den Raum und möglicherweise eine oder mehrere Drehungen, um das Modell nach Bedarf zu ändern.

Das folgende Beispiel aus einer fiktiven 3D-Modell Klasse, die in C++ geschrieben ist, verwendet die Hilfsfunktionen, die in der D3DX Utility Library enthalten sind, um eine Weltmatrix zu erstellen, die drei Drehungen enthält, um ein Modell zu orientieren, und eine Übersetzung, um es relativ zu seiner Position im Raum zu verschieben.


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



Nachdem Sie die World Matrix vorbereitet haben, müssen Sie die [**IDirect3DDevice9:: setTransform**](/windows/desktop/api) -Methode aufrufen, um Sie festzulegen, indem Sie das [**D3DTS \_ World**](d3dts-world.md) -Makro für den ersten Parameter angeben.

> [!Note]  
> Direct3D verwendet die Welt-und Ansichts Matrizen, die Sie zum Konfigurieren mehrerer interner Datenstrukturen festgelegt haben. Jedes Mal, wenn Sie eine neue Welt-oder Sicht Matrix festlegen, berechnet das System die zugeordneten internen Strukturen neu. Wenn Sie diese Matrizen häufig festlegen, z. b. Tausende Male pro Frame, ist dies Rechenzeit aufwändig. Sie können die Anzahl der erforderlichen Berechnungen minimieren, indem Sie Ihre Welt und Matrizen in einer World-View-Matrix verketten, die Sie als Weltmatrix festlegen, und dann die Ansichts Matrix auf die Identität festlegen. Behalten Sie zwischengespeicherte Kopien der einzelnen Welt, und zeigen Sie Matrizen an, sodass Sie die World Matrix nach Bedarf ändern, verketten und zurücksetzen können. Aus Gründen der Übersichtlichkeit wird in dieser Dokumentation Direct3D Samples diese Optimierung nur selten nutzen.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Transformationen](transforms.md)
</dt> </dl>

 

 



