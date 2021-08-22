---
description: Die TRANSFORMS-Eigenschaft enthält die Liste der Transformationen für ein Installationspaket. Das Installationsprogramm wendet alle Transformationen in der Transformationsliste bei jeder Installation, Ankündigung, Bedarfsbasierten Installation oder Wartungsinstallation des Pakets an.
ms.assetid: dde2ef55-7794-4eb1-984a-ed13e990c97f
title: Anwenden von Transformationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: daf6c1bd60a084b745df14d89772008867b618f3b21116ca20c5313747950b5c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119264250"
---
# <a name="applying-transforms"></a>Anwenden von Transformationen

Die [**TRANSFORMS-Eigenschaft**](transforms.md) enthält die Liste der Transformationen für ein Installationspaket. Das Installationsprogramm wendet alle Transformationen in der Transformationsliste bei jeder Installation, Ankündigung, Bedarfsbasierten Installation oder Wartungsinstallation des Pakets an.

Die [**TRANSFORMS-Eigenschaft**](transforms.md) wird festgelegt, indem die Liste der Transformationen in der Befehlszeile angegeben wird. Wenn Sie jedoch entweder die Befehlszeilenoption /jm oder [/ju](command-line-options.md)verwenden, muss die Transformationsliste mithilfe der Option /t angegeben werden.

Beachten Sie, dass die Liste der Transformationen nach der Installation nicht mehr geändert werden kann und nur durch Deinstallieren der Anwendung entfernt werden kann.

> [!Note]  
> Ein Windows Installer-Paket kann bei der Installation einer Anwendung oder eines Updates nicht mehr als 255 Transformationen anwenden. Wenn viele Transformationen erforderlich sind, sollten sie kombiniert und vorherige veraltete Transformationen entfernt werden.

 

Die folgende Tabelle enthält Beispiele für verschiedene Transformationszeichenfolgen, die der Transformationsliste hinzugefügt werden können.



| Transformationszeichenfolge                                                                                                              | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                             |
|--------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| transform1.mst;:transform2.mst;:transform3.mst                                                                                 | Transform2.mst und transform3.mst sind [eingebettete Transformationen.](embedded-transforms.md) transform1.mst ist nur dann eine sichere Quelltransformation, wenn die [**TRANSFORMSSECURE-Eigenschaft**](transformssecure.md) oder [die TransformsSecure-Richtlinie](transformssecure-policy.md) festgelegt ist. Andernfalls ist transform1 eine [ungesicherte Transformation.](unsecured-transforms.md) [](secure-at-source-transforms.md) |
| \\\\\\ \\ Serverfreigabepfad \\ transform1.mst;:transform2.mst                                                                        | Transform2.mst ist eine [eingebettete Transformation.](embedded-transforms.md) transform1.mst ist nur dann eine Transformation mit sicherem vollständigen Pfad, wenn die [**TRANSFORMSSECURE-Eigenschaft**](transformssecure.md) oder [die TransformsSecure-Richtlinie](transformssecure-policy.md) festgelegt ist. Andernfalls ist transform1 eine [ungesicherte Transformation.](unsecured-transforms.md) [](secure-full-path-transforms.md)                   |
| @:transform2.mst;transform1.mst @transform1.mst ;:transform2.mst<br/>                                                     | Transform2.mst ist eine eingebettete Transformation. transform1.mst ist eine [eigenständige, sichere Quelltransformation.](secure-at-source-transforms.md)                                                                                                                                                                                                                                                |
| \|\\\\server \\ share \\ path \\ transform1.mst;:transform2.mst \| :transform2.mst; \\ \\ \\ \\ Serverfreigabepfad \\ transform1.mst<br/> | Transform2.mst ist eine eingebettete Transformation. transform1.mst ist eine eigenständige Transformation mit sicherem [vollständigem Pfad.](secure-full-path-transforms.md)                                                                                                                                                                                                                                                 |



 

 

 




