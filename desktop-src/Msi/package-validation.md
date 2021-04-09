---
description: Es wird dringend empfohlen, die Validierung für jedes neue oder neu geänderte Installationspaket auszuführen, bevor Sie versuchen, das Paket zum ersten Mal zu installieren.
ms.assetid: 47168c0b-82ab-4f1b-84d7-98c8f64d6da0
title: Paketvalidierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 058fbd5bff08701f9603938a631de4e8a59857d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864080"
---
# <a name="package-validation"></a>Paketvalidierung

Es wird dringend empfohlen, die Validierung für jedes neue oder neu geänderte Installationspaket auszuführen, bevor Sie versuchen, das Paket zum ersten Mal zu installieren.

Die Paket Validierung umfasst die folgenden drei Prozesse:

-   [Interne Validierung](internal-validation.md)
-   [Zeichen folgen-Pool-Validierung](string-pool-validation.md)
-   [Interne Konsistenz Auswertung-ICES](internal-consistency-evaluators-ices.md)

Mergemodule sollten mithilfe der in [Validieren von Mergemodulen](validating-merge-modules.md)beschriebenen Methode überprüft werden.

Evalcom2.dll stellt ein COM-Objekt bereit, das Validierungs Vorgänge für Installationspakete und Mergemodule implementiert. Das Hauptobjekt implementiert Schnittstellen für C/C++-Programme. Weitere Informationen finden Sie unter [Validation Automation](validation-automation.md).

 

 



