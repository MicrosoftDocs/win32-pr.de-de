---
description: Bei Transformationen, die nicht gesichert wurden, wie in gesicherte Transformationen beschrieben, handelt es sich standardmäßig um unsichere Transformationen.
ms.assetid: feace6c3-7828-44d0-8d2b-482a02e8e0c0
title: Unsichere Transformationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6743898142197d87d4e3fef5d0f48778f6261ff4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352790"
---
# <a name="unsecured-transforms"></a>Unsichere Transformationen

Bei Transformationen, die nicht gesichert wurden, wie in [gesicherte Transformationen](secured-transforms.md) beschrieben, handelt es sich standardmäßig um unsichere Transformationen.

Wenn Sie bei der Installation eines Pakets eine unsichere Transformation anwenden möchten, übergeben Sie die Transformations Dateinamen in der [**Transformationen**](transforms.md) -Eigenschaft oder der Befehlszeilen Zeichenfolge. Beginnen Sie die Zeichenfolge nicht mit @ oder \| Zeichen, oder legen Sie die [transformssecure-Richtlinie](transformssecure-policy.md) oder die [**transformssecure**](transformssecure.md) -Eigenschaft fest. Beachten Sie, dass Sie unsichere Transformationen und [gesicherte Transformationen](secured-transforms.md) nicht in derselben Transformations Liste kombinieren können.

Wenn das Paket im [Installations Kontext](installation-context.md)pro Benutzer installiert oder angekündigt wird und ungesicherte Transformationen aufweist, speichert das Installationsprogramm die Transformations Quelle im Ordner Anwendungsdaten im Profil des Benutzers. Dadurch kann ein Benutzer seine Anpassung eines Produkts während der Umstellung zwischen Computern beibehalten.

Wenn das Paket im [Installations Kontext](installation-context.md)pro Computer installiert oder angekündigt wird und ungesicherte Transformationen verwendet, speichert das Installationsprogramm die Transformations Quelle im Ordner "% windir% \\ Installer".

Während der erstmaligen Installation des Pakets sucht der Installer zuerst nach der Transformation an der Quelle, die von der [**Transformationen**](transforms.md) -Eigenschaft oder der Befehlszeilen Zeichenfolge bereitgestellt wird. Wenn diese Quelle nicht verfügbar ist, sucht das Installationsprogramm an der Quelle des Pakets neben der MSI-Datei nach der Transformation.

Während einer [Wartungs Installation](maintenance-installation.md)sucht das Installationsprogramm am Cache Speicherort nach der Transformation. Wenn die zwischengespeicherte Kopie der Transformation nicht verfügbar ist, sucht das Installationsprogramm an der Quelle des Pakets neben der MSI-Datei nach der Transformation.

Weitere Informationen finden Sie unter [Anwenden von Transformationen](applying-transforms.md) und [Quellen Resilienz](source-resiliency.md).

 

 



