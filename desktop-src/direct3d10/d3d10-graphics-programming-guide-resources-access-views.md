---
description: In Direct3D 10 wird mit einer Ansicht auf Texturressourcen zugegriffen. Dies ist ein Mechanismus für die Hardwareinterpretation einer Ressource im Arbeitsspeicher.
ms.assetid: ccfe6273-0dcf-4b42-9d74-665a0b4cd14a
title: Texturansichten (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc420e39c4d577947cae657f3296b15f0052db9e823e07d3a3ba1ccb641fb6b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118101345"
---
# <a name="texture-views-direct3d-10"></a>Texturansichten (Direct3D 10)

In Direct3D 10 wird mit einer Ansicht auf Texturressourcen zugegriffen. Dies ist ein Mechanismus für die Hardwareinterpretation einer Ressource im Arbeitsspeicher. Eine Ansicht ermöglicht einer bestimmten Pipelinephase, nur auf die [benötigten Unterressourcen](d3d10-graphics-programming-guide-resources-types.md) in der von der Anwendung gewünschten Darstellung zuzugreifen.

Eine Ansicht unterstützt das Konzept einer typfreien Ressource. Eine ressource ohne Typ ist eine Ressource, die mit einer bestimmten Größe, aber nicht mit einem bestimmten Datentyp erstellt wurde. Die Daten werden dynamisch interpretiert, wenn sie an die Pipeline gebunden sind.

Die folgende Abbildung zeigt ein Beispiel für die Bindung eines 2D-Texturarrays mit 6 Texturen als Shaderressource, indem eine Shaderressourcenansicht dafür erstellt wird. Die Ressource wird dann als Array von Texturen adressiert. (Hinweis: Eine Unterressource kann nicht gleichzeitig als Eingabe und Ausgabe an die Pipeline gebunden werden.)

![Abbildung eines Texturarrays mit sechs Texturen](images/d3d10-cube-texture-faces.png)

Wenn Sie ein 2D-Texturarray als Renderziel verwenden, kann die Ressource als Array von 2D-Texturen (in diesem Beispiel 6) mit Mipmapebenen (in diesem Beispiel 3) angezeigt werden.

Erstellen Sie ein Ansichtsobjekt für ein Renderziel, indem Sie CreateRenderTargetView aufrufen. Rufen Sie dann OMSetRenderTargets auf, um die Renderzielansicht auf die Pipeline festzulegen. Rendern Sie in die Renderziele, indem Sie Draw aufrufen und renderTargetArrayIndex verwenden, um die richtige Textur im Array zu indizieren. Sie können eine Unterressource (mipmap-Ebene, Arrayindexkombination) verwenden, um eine Bindung an ein beliebiges Array von Unterressourcen vorzunehmen. Sie können also an die zweite Mipmapebene binden und diese bestimmte Mipmapebene nur aktualisieren, wenn Sie möchten, wie in der folgenden Abbildung dargestellt.

![Abbildung der Bindung nur an die zweite Mipmapebene eines Texturarrays](images/d3d10-cube-texture-faces-subresource.png)



Unterschiede zwischen Direct3D 9 und Direct3D 10:

- In Direct3D 10 binden Sie eine Ressource nicht mehr direkt an die Pipeline, Sie erstellen eine Ansicht einer Ressource und legen die Ansicht dann auf die Pipeline fest. Dies ermöglicht die Überprüfung und Zuordnung in der Laufzeit und im Treiber bei der Erstellung der Ansicht, wodurch die Typüberprüfung zur Bindungszeit minimiert wird.



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ressourcen (Direct3D 10)](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 




