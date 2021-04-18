---
title: Automatisch generierte Texturkoordinaten (Direct3D 9)
description: Das System kann die transformierte Position des Kamera Raums oder das normale von einem Scheitelpunkt als Texturkoordinaten verwenden oder die drei Element Vektoren berechnen, die zum Adressieren einer kubischen Umgebungs Zuordnung verwendet werden.
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de8a6328df66296c0948c53be68109a9f5afbbb6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106338924"
---
# <a name="auto-generated-texture-coordinates-direct3d-9"></a>Automatisch generierte Texturkoordinaten (Direct3D 9)

Das System kann die transformierte Position des Kamera Raums oder das normale von einem Scheitelpunkt als Texturkoordinaten verwenden oder die drei Element Vektoren berechnen, die zum Adressieren einer kubischen Umgebungs Zuordnung verwendet werden. Wie bei Texturkoordinaten, die Sie explizit in einem Scheitelpunkt angeben, können Sie automatisch generierte Texturkoordinaten als Eingabe für Texturkoordinaten Transformationen verwenden.

Automatisch generierte Texturkoordinaten können die für Geometriedaten erforderliche Bandbreite erheblich reduzieren, da explizite Texturkoordinaten im Scheitelpunkt Format vermieden werden müssen. In vielen Fällen können die vom System generierten Texturkoordinaten mit Transformationen verwendet werden, um besondere Effekte zu erzeugen. Natürlich handelt es sich hierbei um ein spezielles Feature, das Sie in vielen Fällen explizite Texturkoordinaten verwenden können.

## <a name="configuring-automatically-generated-texture-coordinates"></a>Konfigurieren automatisch generierter Texturkoordinaten

In C++ steuert der D3DTSS \_ texcoordindex Texture-Stage State (aus dem [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md) -Enumerationstyp), wie das System Texturkoordinaten generiert.

Normalerweise weist dieser Zustand das System an, einen bestimmten Satz von Texturkoordinaten zu verwenden, die im Scheitelpunkt Format codiert sind. Wenn Sie die Flags D3DTSS \_ TCI \_ cameraspacenormal, D3DTSS \_ TCI \_ cameraspaceposition oder D3DTSS \_ TCI \_ cameraspacereflectionvector in den Wert einschließen, den Sie diesem Zustand zuweisen, ist das Systemverhalten sehr unterschiedlich. Wenn eines dieser Flags vorhanden ist, ignoriert die Textur Phase die Texturkoordinaten innerhalb des Vertex-Formats zugunsten der vom System generierten Koordinaten. Die Bedeutung für jedes Flag ist in der folgenden Liste aufgeführt.

-   D3DTSS \_ TCI \_ cameraspacenormal

    Verwenden Sie den Vertex normal als Eingabe Texturkoordinaten, der in den Kamerabereich transformiert wurde.

-   D3DTSS \_ TCI \_ cameraspaceposition

    Verwenden Sie die Vertex-Position, die in den Kamerabereich transformiert wird, als Eingabe Texturkoordinaten.

-   D3DTSS \_ TCI \_ cameraspacereflectionvector

    Verwenden Sie den reflektionvektor, transformiert in den Kamera Raum, als Eingabe Texturkoordinaten. Der reflektionvektor wird aus der eintexposition der Eingabe und dem normalen Vektor berechnet.

Die Flags für Texturkoordinaten Indizes schließen sich gegenseitig aus. In diesem Beispiel wird Folgendes verwendet:

-   Die Scheitelpunkt Position (im Kamera Zeichen) als Eingabe Texturkoordinaten für diese Textur Phase.
-   Der im D3DRENDERSTATE WRAP1-renderzustand festgelegte Wrap-Modus. \_


```
// Assume d3dDevice is a valid pointer to an IDirect3DDevice9 interface
d3dDevice->SetTextureStageState(0, D3DTSS_TEXCOORDINDEX, 
                                   D3DTSS_TCI_CAMERASPACEPOSITION | 1);
```



Automatisch generierte Texturkoordinaten sind besonders nützlich als Eingabewerte für eine Texturkoordinaten Transformation oder, um zu vermeiden, dass Ihre Anwendung drei-Element-Vektoren für kubische Umgebungs Zuordnungen berechnen muss.

Kugel Zuordnung verwendet eine vorberechnete Textur Zuordnung (zur Modell Zeit), die die gesamte Umgebung enthält, wie Sie von einer Chrome-Kugel reflektiert wird. Direct3D verfügt über eine Textur Koordinate-Generierungs Funktion, die den renderzustand D3DTSS \_ TCI \_ cameraspacenormal verwendet, der die normale des Scheitel Punkts im Kamerabereich einnimmt und eine Textur Transformation zum Generieren von Texturkoordinaten einfügt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verarbeitung von Texturkoordinaten](texture-coordinate-processing.md)
</dt> <dt>

[Transformationen für Texturkoordinaten (Direct3D 9)](texture-coordinate-transformations.md)
</dt> <dt>

[Kubische Umgebungs Zuordnung (Direct3D 9)](cubic-environment-mapping.md)
</dt> </dl>

 

 
