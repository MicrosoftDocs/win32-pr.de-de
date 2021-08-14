---
title: Features des Replikationsmodells für Active Directory Domain Services
description: Das replikationsmodell, das in Active Directory Domain Services verwendet wird, wird als lose Multimasterkonsistenz mit Konvergenz bezeichnet.
ms.assetid: 8fd63871-68b4-4ed6-8165-145cbc90c213
ms.tgt_platform: multiple
keywords:
- Active Directory Domain Services, Replikationsmodell
- Replikationsmodellfeatures in Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd113ffe4182be47c9e8c84404fc748e417e78c866e41298ad19d8e7a0dec555
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118189531"
---
# <a name="features-of-the-replication-model-for-active-directory-domain-services"></a>Features des Replikationsmodells für Active Directory Domain Services

Das replikationsmodell, das in Active Directory Domain Services verwendet wird, wird als *lose Multimasterkonsistenz mit Konvergenz bezeichnet.* In diesem Modell kann das Verzeichnis viele Replikate haben. Ein Replikationssystem gibt an einem beliebigen Replikat vorgenommene Änderungen an alle anderen Replikate weiter. Es ist nicht garantiert, dass die Replikate zu einem bestimmten Zeitpunkt konsistent sind ("lose Konsistenz"), da Änderungen jederzeit auf jedes Replikat angewendet werden können ("Multimaster"). Wenn das System einen stabilen Zustand erreichen darf, in dem keine neuen Updates auftreten und alle vorherigen Updates vollständig repliziert wurden, werden alle Replikate garantiert auf denselben Satz von Werten konvergiert ("Konvergenz").

 

 




