---
description: In Direct3D 10 erfolgt der Zugriff auf Textur Ressourcen mit einer Ansicht, bei der es sich um einen Mechanismus zur Hardware Interpretation einer Ressource im Arbeitsspeicher handelt.
ms.assetid: ccfe6273-0dcf-4b42-9d74-665a0b4cd14a
title: Textur Sichten (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f06cd98a00782b826713e68304ad7cc132e4e0fe
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958462"
---
# <a name="texture-views-direct3d-10"></a>Textur Sichten (Direct3D 10)

In Direct3D 10 erfolgt der Zugriff auf Textur Ressourcen mit einer Ansicht, bei der es sich um einen Mechanismus zur Hardware Interpretation einer Ressource im Arbeitsspeicher handelt. Eine Ansicht ermöglicht es einer bestimmten Pipeline Stufe, nur auf die benötigten unter [Ressourcen](d3d10-graphics-programming-guide-resources-types.md) zuzugreifen, die in der von der Anwendung gewünschten Darstellung benötigt werden.

Eine Ansicht unterstützt das Konzept einer Ressource ohne Typ. Eine Ressource vom Typ "less" ist eine Ressource, die mit einer bestimmten Größe erstellt wurde, jedoch nicht mit einem bestimmten Datentyp. Die Daten werden dynamisch interpretiert, wenn Sie an die Pipeline gebunden werden.

Die folgende Abbildung zeigt ein Beispiel für die Bindung eines 2D-Textur Arrays mit 6 Texturen als Shaderressource, indem eine Shader-Ressourcen Ansicht dafür erstellt wird. Die Ressource wird dann als Array von Texturen adressiert. (Hinweis: eine untergeordnete Quelle kann nicht gleichzeitig als Eingabe und Ausgabe an die Pipeline gebunden werden.)

![Abbildung eines Textur Arrays mit sechs Texturen](images/d3d10-cube-texture-faces.png)

Wenn ein 2D-Textur Array als Renderziel verwendet wird, kann die Ressource als Array von 2D-Texturen (in diesem Beispiel 6) mit MipMap-Ebenen (in diesem Beispiel 3) angezeigt werden.

Erstellen Sie ein Ansichts Objekt für ein Renderziel durch Aufrufen von createrendertargetview. Anschließend wird omsetrendertargets aufgerufen, um die renderzielansicht auf die Pipeline festzulegen. Rendern Sie die Renderziele, indem Sie Draw aufrufen und den rendertargetarrayindex verwenden, um die richtige Textur im Array zu indizieren. Sie können einen unter Bericht (eine MipMap-Ebene, Array Index Kombination) verwenden, um eine Bindung an ein beliebiges Array von unter Ressourcen herzustellen. Sie könnten also an die zweite MipMap-Ebene binden und diese bestimmte MipMap-Ebene nur aktualisieren, wenn Sie möchten, wie in der folgenden Abbildung dargestellt.

![Darstellung der Bindung nur an die zweite MipMap-Ebene eines Textur Arrays](images/d3d10-cube-texture-faces-subresource.png)



|                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterschiede zwischen Direct3D 9 und Direct3D 10: in Direct3D 10 binden Sie eine Ressource nicht mehr direkt an die Pipeline, sondern erstellen eine Ansicht einer Ressource und legen dann die Ansicht auf die Pipeline fest. Dies ermöglicht die Validierung und Zuordnung in der Laufzeit und im Treiber bei der Ansichts Erstellung, wodurch die Typüberprüfung zur Bindungs Zeit minimiert wird.<br/> |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ressourcen (Direct3D 10)](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 




