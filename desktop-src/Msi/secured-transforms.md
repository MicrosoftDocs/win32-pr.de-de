---
description: Sichere Transformationen sind manchmal aus Sicherheitsgründen erforderlich.
ms.assetid: c6019b28-b0a7-4104-9d78-b4b4228635b8
title: Gesicherte Transformationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e07c36b70827c301117bff7d98b30aae2990efb80f892bda24b0be35cbba5316
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120040840"
---
# <a name="secured-transforms"></a>Gesicherte Transformationen

Sichere Transformationen sind manchmal aus Sicherheitsgründen erforderlich. Gesicherte Transformationen werden lokal auf dem Computer des Benutzers an einem Speicherort gespeichert, an dem der Benutzer in einem sicheren Dateisystem keinen Schreibzugriff hat. Solche Transformationen werden an diesem Speicherort während der Installation oder Ankündigung des Pakets zwischengespeichert. Nur Administratoren und das lokale System haben Schreibzugriff auf diesen Speicherort. Ein Benutzer ohne Administratorrechte kann die Transformationsdatei nicht ändern. Bei [nachfolgenden Bedarfsinstallationen oder](installation-on-demand.md) [Wartungsinstallationen](maintenance-installation.md) des Pakets verwendet das Installationsprogramm die zwischengespeicherten Transformationen.

Legen Sie zum Angeben des geschützten [Transformationsspeichers die TransformsSecure-Richtlinie](transformssecure-policy.md)fest, legen Sie die [**TRANSFORMSSECURE-Eigenschaft**](transformssecure.md) fest, oder übergeben Sie das @- oder -Symbol in der \| Transformationsliste. Beachten Sie, dass Sie keine gesicherten und ungesicherten Transformationen in derselben Transformationsliste enthalten können. Weitere Informationen [finden Sie unter Anwenden von Transformationen.](applying-transforms.md)

Durch das Entfernen des Produkts durch einen Benutzer werden alle geschützten Transformationen für dieses Produkt vom Computer des Benutzers entfernt.

Wenn das Installationsprogramm ermittelt, dass eine gesicherte Transformation nicht lokal verfügbar ist, versucht es, den Transformationscache aus einer Quelle wiederherzustellen. Sichere Transformationen können secure-at-source oder secure-full-path sein:

-   [Secure-at-Source-Transformationen,](secure-at-source-transforms.md) die im lokalen Transformationscache fehlen, werden aus dem Stamm der Quelle der .msi wiederhergestellt.
-   Transformationen mit sicherem vollständigen Pfad, die im lokalen [Transformationscache](secure-full-path-transforms.md) fehlen, werden aus dem ursprünglichen vollständigen Pfad wiederhergestellt, der in der Liste der Transformationen angegeben ist.

 

 



