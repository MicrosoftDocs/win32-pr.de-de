---
description: Transformationen, die nicht wie unter Sichere Transformationen beschrieben gesichert wurden, sind standardmäßig ungesicherte Transformationen.
ms.assetid: feace6c3-7828-44d0-8d2b-482a02e8e0c0
title: Ungesicherte Transformationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6bb234a0cdee852d3a5e1717642f5325283a571b740c9d7b4a5f6901afb52c1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119499610"
---
# <a name="unsecured-transforms"></a>Ungesicherte Transformationen

Transformationen, die nicht wie unter Sichere [Transformationen](secured-transforms.md) beschrieben gesichert wurden, sind standardmäßig ungesicherte Transformationen.

Um eine ungesicherte Transformation beim Installieren eines Pakets anzuwenden, übergeben Sie die Transformationsdateinamen in der [**TRANSFORMS-Eigenschaft**](transforms.md) oder Befehlszeilenzeichenfolge. Beginnen Sie die Zeichenfolge nicht mit den Zeichen @ oder , oder legen \| Sie die [TransformsSecure-Richtlinie](transformssecure-policy.md) oder die [**TRANSFORMSSECURE-Eigenschaft**](transformssecure.md) fest. Beachten Sie, dass Sie keine ungesicherten Transformationen und [geschützten Transformationen](secured-transforms.md) in derselben Transformationsliste kombinieren können.

Wenn das Paket im Benutzerinstallationskontext installiert [](installation-context.md)oder angekündigt wird und über ungesicherte Transformationen verfügt, speichert das Installationsprogramm die Transformationsquelle im Ordner Anwendungsdaten im Profil des Benutzers. Dies ermöglicht es einem Benutzer, seine Anpassung eines Produkts beim Wechsel zwischen Computern zu verwalten.

Wenn das Paket im Installationskontext pro Computer [](installation-context.md)installiert oder angekündigt wird und ungesicherte Transformationen verwendet, speichert das Installationsprogramm die Transformationsquelle im Ordner %windir% \\ Installer.

Während einer erstmaligen Installation des Pakets sucht das Installationsprogramm zunächst in der Quelle, die von der [**TRANSFORMS-Eigenschaft**](transforms.md) oder Befehlszeilenzeichenfolge bereitgestellt wird, nach der Transformation. Wenn diese Quelle nicht verfügbar ist, sucht das Installationsprogramm nach der Transformation in der Quelle des Pakets neben der .msi Datei.

Während einer [Wartungsinstallation](maintenance-installation.md)sucht das Installationsprogramm am Cachespeicherort nach der Transformation. Wenn die zwischengespeicherte Kopie der Transformation nicht mehr verfügbar ist, sucht das Installationsprogramm in der Quelle des Pakets neben der .msi Transformation.

Weitere Informationen finden Sie unter [Anwenden von Transformationen](applying-transforms.md) und [Quellresilienz.](source-resiliency.md)

 

 



