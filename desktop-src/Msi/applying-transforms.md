---
description: Die Transformationen-Eigenschaft enthält die Liste der Transformationen für ein Installationspaket. Das Installationsprogramm wendet alle Transformationen in der Liste der Transformationen bei jeder Installation, Ankündigung, Installation nach Bedarf oder Wartungs Installation des Pakets an.
ms.assetid: dde2ef55-7794-4eb1-984a-ed13e990c97f
title: Anwenden von Transformationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2367e02396ec33e517f8abfe579060c0a0986be2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864476"
---
# <a name="applying-transforms"></a>Anwenden von Transformationen

Die [**Transformationen**](transforms.md) -Eigenschaft enthält die Liste der Transformationen für ein Installationspaket. Das Installationsprogramm wendet alle Transformationen in der Liste der Transformationen bei jeder Installation, Ankündigung, Installation nach Bedarf oder Wartungs Installation des Pakets an.

Die [**Transformationen**](transforms.md) -Eigenschaft wird festgelegt, indem die Liste der Transformationen in der Befehlszeile angegeben wird. Wenn Sie jedoch entweder die [Befehlszeilenoption](command-line-options.md)/JM oder/Ju verwenden, muss die Liste der Transformationen mithilfe der Option/t angegeben werden.

Beachten Sie, dass die Liste der Transformationen nach der Installation nicht geändert werden kann und nur durch Deinstallieren der Anwendung entfernt werden kann.

> [!Note]  
> Bei der Installation einer Anwendung oder eines Updates kann ein Windows Installer Paket nicht mehr als 255 Transformationen anwenden. Wenn viele Transformationen erforderlich sind, sollten Sie kombiniert werden, und vorherige veraltete Transformationen sollten entfernt werden.

 

Die folgende Tabelle enthält Beispiele für verschiedene Transformationen für Transformationen, die der Liste der Transformationen hinzugefügt werden können.



| Transformations Zeichenfolge                                                                                                              | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                             |
|--------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| transform1. MST;: transform2. MST;: transform3. MST                                                                                 | Transform2. MST und transform3. MST sind [eingebettete Transformationen](embedded-transforms.md). transform1. MST ist eine [sichere und Quell Umwandlung](secure-at-source-transforms.md) nur, wenn die [**transformssecure**](transformssecure.md) -Eigenschaft oder die [transformssecure-Richtlinie](transformssecure-policy.md) festgelegt ist, andernfalls ist transform1 eine [unsichere Transformation](unsecured-transforms.md). |
| \\\\Server \\ Freigabe \\ Pfad \\ transform1. MST;: transform2. MST                                                                        | Transform2. MST ist eine [eingebettete Transformation](embedded-transforms.md). transform1. MST ist eine [sichere vollständige Pfad Transformation](secure-full-path-transforms.md) , wenn die [**transformssecure**](transformssecure.md) -Eigenschaft oder die [transformssecure-Richtlinie](transformssecure-policy.md) festgelegt ist, andernfalls ist transform1 eine [unsichere Transformation](unsecured-transforms.md).                   |
| @: transform2. MST; transform1. MST @transform1.mst ;: transform2. MST<br/>                                                     | Transform2. MST ist eine eingebettete Transformation. transform1. MST ist eine eigenständige [Secure-at-Source-](secure-at-source-transforms.md)Transformation.                                                                                                                                                                                                                                                |
| \|\\\\Server \\ Freigabe \\ Pfad \\ transform1. MST;: transform2. MST \| : transform2. MST; \\ \\ Server \\ Freigabe \\ Pfad \\ transform1. MST<br/> | Transform2. MST ist eine eingebettete Transformation. transform1. MST ist eine eigenständige [Secure-Full-Path-](secure-full-path-transforms.md)Transformation.                                                                                                                                                                                                                                                 |



 

 

 




