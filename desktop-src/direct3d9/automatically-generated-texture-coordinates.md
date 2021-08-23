---
title: Automatisch generierte Texturkoordinaten (Direct3D 9)
description: Das System kann die transformierte Kameraraumposition oder die Normalität aus einem Scheitelpunkt als Texturkoordinaten verwenden oder die drei Elementvektoren berechnen, die zum Adressieren einer kubischen Umgebungskarte verwendet werden.
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7aa4354002c920f73667f97de9a4185579a8c4c7b4563aebf1f3328753c88d01
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119608010"
---
# <a name="auto-generated-texture-coordinates-direct3d-9"></a>Automatisch generierte Texturkoordinaten (Direct3D 9)

Das System kann die transformierte Kameraraumposition oder die Normalität aus einem Scheitelpunkt als Texturkoordinaten verwenden oder die drei Elementvektoren berechnen, die zum Adressieren einer kubischen Umgebungskarte verwendet werden. Wie Texturkoordinaten, die Sie explizit in einem Scheitelpunkt angeben, können Sie automatisch generierte Texturkoordinaten als Eingabe für Texturkoordinatentransformationen verwenden.

Automatisch generierte Texturkoordinaten können die für Geometriedaten erforderliche Bandbreite erheblich reduzieren, da keine expliziten Texturkoordinaten im Scheitelpunktformat erforderlich sind. In vielen Fällen können die Texturkoordinaten, die das System generiert, mit Transformationen verwendet werden, um spezielle Effekte zu erzeugen. Dies ist natürlich ein spezielles Feature, und Sie verwenden in vielen Fällen explizite Texturkoordinaten.

## <a name="configuring-automatically-generated-texture-coordinates"></a>Konfigurieren automatisch generierter Texturkoordinaten

In C++ steuert der Texturphasenzustand D3DTSS \_ TEXCOORDINDEX (aus dem [**enumerationierten D3DTEXTURESTAGESTATETYPE-Typ),**](./d3dtexturestagestatetype.md) wie das System Texturkoordinaten generiert.

Normalerweise weist dieser Zustand das System an, einen bestimmten Satz von Texturkoordinaten zu verwenden, die im Scheitelpunktformat codiert sind. Wenn Sie die Flags D3DTSS \_ TCI \_ CAMERASPACENORMAL, D3DTSS \_ TCI \_ CAMERASPACEPOSITION oder D3DTSS \_ TCI \_ CAMERASPACEREFLECTIONVECTOR in den Wert einschließen, den Sie diesem Zustand zuweisen, unterscheidet sich das Systemverhalten erheblich. Wenn eines dieser Flags vorhanden ist, ignoriert die Texturphase die Texturkoordinaten im Scheitelpunktformat zugunsten von Koordinaten, die das System generiert. Die Bedeutungen für die einzelnen Flags werden in der folgenden Liste angezeigt.

-   D3DTSS \_ TCI \_ CAMERASPACENORMAL

    Verwenden Sie den Vertex normal, der in den Kameraraum transformiert wird, als Eingabetexturkoordinaten.

-   D3DTSS \_ TCI \_ CAMERASPACEPOSITION

    Verwenden Sie die in den Kameraraum transformierte Scheitelpunktposition als Eingabetexturkoordinaten.

-   D3DTSS \_ TCI \_ CAMERASPACEREFLECTIONVECTOR

    Verwenden Sie den in den Kameraraum transformierten Reflektionsvektor als Eingabetexturkoordinaten. Der Reflektionsvektor wird aus der Eingabevertexposition und dem normalen Vektor berechnet.

Die Texturkoordinatenindexflags schließen sich gegenseitig aus. In diesem Beispiel wird Folgendes verwendet:

-   Die Scheitelpunktposition (im Kameraraum) als Eingabetexturkoordinaten für diese Texturphase
-   Der im D3DRENDERSTATE \_ WRAP1-Renderzustand festgelegte Umbruchmodus


```
// Assume d3dDevice is a valid pointer to an IDirect3DDevice9 interface
d3dDevice->SetTextureStageState(0, D3DTSS_TEXCOORDINDEX, 
                                   D3DTSS_TCI_CAMERASPACEPOSITION | 1);
```



Automatisch generierte Texturkoordinaten sind besonders nützlich als Eingabewerte für eine Texturkoordinatentransformation oder um die Notwendigkeit zu vermeiden, dass Ihre Anwendung Vektoren mit drei Elementen für kubische Umgebungszuordnungen berechnet.

Bei der Kugelzuordnung wird eine vorab berechnete Texturkarte (zur Modellzeit) verwendet, die die gesamte Umgebung enthält, die von einer Chrome-Kugel reflektiert wird. Direct3D verfügt über eine Texturkoordinatengenerierungsfunktion mit dem Renderzustand D3DTSS \_ TCI \_ CAMERASPACENORMAL, die die Normalität des Scheitelpunkts im Kameraraum annimmt und sie durch eine Texturtransformation zum Generieren von Texturkoordinaten versetzt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Texturkoordinatenverarbeitung](texture-coordinate-processing.md)
</dt> <dt>

[Transformationen für Texturkoordinaten (Direct3D 9)](texture-coordinate-transformations.md)
</dt> <dt>

[Kubische Umgebungszuordnung (Direct3D 9)](cubic-environment-mapping.md)
</dt> </dl>

 

 
