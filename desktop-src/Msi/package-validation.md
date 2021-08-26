---
description: Es wird dringend empfohlen, die Überprüfung für jedes neue oder neu geänderte Installationspaket vor dem erstmaligen Installieren des Pakets ausführen.
ms.assetid: 47168c0b-82ab-4f1b-84d7-98c8f64d6da0
title: Paketvalidierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca2fb8fe877f68a1c787458e7703fb59f035031fc68bba1d75f24e86851aac7c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120074850"
---
# <a name="package-validation"></a>Paketvalidierung

Es wird dringend empfohlen, die Überprüfung für jedes neue oder neu geänderte Installationspaket vor dem erstmaligen Installieren des Pakets ausführen.

Die Paketvalidierung umfasst die folgenden drei Prozesse:

-   [Interne Überprüfung](internal-validation.md)
-   [Überprüfung des Zeichenfolgenpools](string-pool-validation.md)
-   [Interne Konsistenzauswertungen – ICEs](internal-consistency-evaluators-ices.md)

Mergemodule sollten mithilfe der unter Validating Merge Modules (Überprüfen von Mergemodulen) [beschriebenen Methode überprüft werden.](validating-merge-modules.md)

Evalcom2.dll stellt ein COM-Objekt zur Verfügung, das Validierungsvorgänge für Installationspakete und Mergemodule implementiert. Das Hauptobjekt implementiert Schnittstellen für C/C++-Programme. Weitere Informationen finden Sie unter [Validierungsautomatisierung.](validation-automation.md)

 

 



