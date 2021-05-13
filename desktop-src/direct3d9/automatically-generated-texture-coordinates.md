---
title: Automatisch generierte Texturkoordinaten (Direct3D 9)
description: Das System kann die transformierte Kameraraumposition oder die Normalität aus einem Scheitelpunkt als Texturkoordinaten verwenden oder die drei Elementvektoren berechnen, die zum Adressieren einer kubischen Umgebungskarte verwendet werden.
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b01addbe354fb910ef68e1fc693e7dfffb1ceacf
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109843291"
---
# <a name="auto-generated-texture-coordinates-direct3d-9"></a>Automatisch generierte Texturkoordinaten (Direct3D 9)

Das System kann die transformierte Kameraraumposition oder die Normalität aus einem Scheitelpunkt als Texturkoordinaten verwenden oder die drei Elementvektoren berechnen, die zum Adressieren einer kubischen Umgebungskarte verwendet werden. Wie Texturkoordinaten, die Sie explizit in einem Scheitelpunkt angeben, können Sie automatisch generierte Texturkoordinaten als Eingabe für Texturkoordinatentransformationen verwenden.

Automatisch generierte Texturkoordinaten können die für Geometriedaten erforderliche Bandbreite erheblich reduzieren, da keine expliziten Texturkoordinaten im Scheitelpunktformat erforderlich sind. In vielen Fällen können die Texturkoordinaten, die das System generiert, mit Transformationen verwendet werden, um spezielle Effekte zu erzeugen. Dies ist natürlich ein spezielles Feature, und Sie verwenden in vielen Fällen explizite Texturkoordinaten.

## <a name="configuring-automatically-generated-texture-coordinates"></a>Konfigurieren automatisch generierter Texturkoordinaten

In C++ steuert der Texturphasenzustand D3DTSS \_ TEXCOORDINDEX (aus dem [**enumerationierten D3DTEXTURESTAGESTATETYPE-Typ),**](./d3dtexturestagestatetype.md) wie das System Texturkoordinaten generiert.

Normalerweise weist dieser Zustand das System an, einen bestimmten Satz von Texturkoordinaten zu verwenden, die im Scheitelpunktformat codiert sind. Wenn Sie die TCI-Flags D3DTSS \_ \_ CAMERASPACENORMAL, D3DTSS \_ TCI \_ CAMERASPACEPOSITION oder D3DTSS \_ TCI \_ CAMERASPACEREFLECTIONVECTOR in den Wert einschließen, den Sie diesem Zustand zuweisen, unterscheidet sich das Systemverhalten erheblich. Wenn eines dieser Flags vorhanden ist, ignoriert die Texturphase die Texturkoordinaten im Scheitelpunktformat zugunsten von Koordinaten, die das System generiert. Die Bedeutungen der einzelnen Flags werden in der folgenden Liste angezeigt.

-   D3DTSS \_ TCI \_ CAMERASPACENORMAL

    Verwenden Sie den Scheitelpunkt normal, transformiert in den Kameraraum, als Eingabetexturkoordinaten.

-   D3DTSS \_ TCI \_ CAMERASPACEPOSITION

    Verwenden Sie die Scheitelpunktposition, transformiert in den Kameraraum, als Eingabetexturkoordinaten.

-   D3DTSS \_ TCI \_ CAMERASPACEREFLECTIONVECTOR

    Verwenden Sie den Reflektionsvektor, der in den Kameraraum transformiert wird, als Eingabetexturkoordinaten. Der Reflektionsvektor wird aus der Position des Eingabe-Scheitelpunkts und dem normalen Vektor berechnet.

Die Texturkoordinatenindexflags schließen sich gegenseitig aus. In diesem Beispiel wird Folgendes verwendet:

-   Die Scheitelpunktposition (im Kameraraum) als Eingabetexturkoordinaten für diese Texturphase
-   Der im D3DRENDERSTATE WRAP1-Renderzustand festgelegte \_ Wrap-Modus


```
// Assume d3dDevice is a valid pointer to an IDirect3DDevice9 interface
d3dDevice->SetTextureStageState(0, D3DTSS_TEXCOORDINDEX, 
                                   D3DTSS_TCI_CAMERASPACEPOSITION | 1);
```



Automatisch generierte Texturkoordinaten sind am nützlichsten als Eingabewerte für eine Texturkoordinatentransformation oder um zu vermeiden, dass Ihre Anwendung dreielementige Vektoren für kubische Umgebungszuordnungen berechnen muss.

Bei der Kugelzuordnung wird eine vorbesetzte Texturzuordnung (zur Modellzeit) verwendet, die die gesamte Umgebung enthält, wie durch eine Chrome-Kugel dargestellt. Direct3D verfügt über ein Texturkoordinatengenerierungsfeature unter Verwendung des Renderzustands D3DTSS \_ TCI CAMERASPACENORMAL, das den Normalwert des Scheitelpunkts im Kameraraum übernimmt und durch eine Texturtransformation versetzt, um Texturkoordinaten zu \_ generieren.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Texturkoordinatenverarbeitung](texture-coordinate-processing.md)
</dt> <dt>

[Texturkoordinatentransformationen (Direct3D 9)](texture-coordinate-transformations.md)
</dt> <dt>

[Kubische Umgebungszuordnung (Direct3D 9)](cubic-environment-mapping.md)
</dt> </dl>

 

 
