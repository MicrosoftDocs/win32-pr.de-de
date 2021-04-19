---
title: Features des Replikations Modells für Active Directory Domain Services
description: Das in Active Directory Domain Services verwendete Replikations Modell wird als multimasterlose Konsistenz mit Konvergenz bezeichnet.
ms.assetid: 8fd63871-68b4-4ed6-8165-145cbc90c213
ms.tgt_platform: multiple
keywords:
- Active Directory Domain Services, Replikations Modell
- Features des Replikations Modells Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 923c49dd648063ebd6afd086be3729f28f1e4080
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341632"
---
# <a name="features-of-the-replication-model-for-active-directory-domain-services"></a>Features des Replikations Modells für Active Directory Domain Services

Das in Active Directory Domain Services verwendete Replikations Modell wird als *multimasterlose Konsistenz mit Konvergenz* bezeichnet. In diesem Modell kann das Verzeichnis über viele Replikate verfügen. ein Replikationssystem überträgt Änderungen an einem beliebigen Replikat an alle anderen Replikate. Es ist nicht garantiert, dass die Replikate zu einem bestimmten Zeitpunkt konsistent sind ("lose Konsistenz"), da Änderungen jederzeit auf ein beliebiges Replikat angewendet werden können ("Multimaster"). Wenn das System in der Lage ist, einen stabilen Zustand zu erreichen, in dem keine neuen Updates stattfinden und alle vorherigen Updates vollständig repliziert wurden, werden alle Replikate sicher mit dem gleichen Satz von Werten ("Konvergenz") zusammengeführt.

 

 




