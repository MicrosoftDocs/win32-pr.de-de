---
description: Eine Zertifikat Kette ist eine hierarchische Sammlung von Zertifikaten, die vom Endbenutzer oder Computer zurück zu einer Vertrauensstellung führt, in der Regel die Stamm Zertifizierungsstelle (Certification Authority, ca) einer Organisation.
ms.assetid: 53701ede-269c-4949-b839-3f2b64cb5510
title: Zertifikatkette
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e7509adb164c98cf07912af00af0d91c27ab8df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363001"
---
# <a name="certificate-chain"></a>Zertifikatkette

Eine Zertifikat Kette ist eine hierarchische Sammlung von Zertifikaten, die vom Endbenutzer oder Computer zurück zu einer Vertrauensstellung führt, in der Regel die Stamm Zertifizierungsstelle (Certification Authority, ca) einer Organisation. Da alle Parteien das Stamm Zertifikat wahrscheinlich als vertrauenswürdig einstufen, kann eine Partei durch Überprüfen der Zertifikat Kette eine Vertrauensstellung in einem Endentitäts Zertifikat erlangen. Die Überprüfung erfordert in der Regel die Einrichtung der einzelnen Zertifikate in der Kette:

-   Wird vom öffentlichen Schlüssel im vorherigen Zertifikat signiert.
-   Ist nicht abgelaufen.
-   Wurde nicht widerrufen.
-   Entspricht den Richtlinien, die von vorherigen Zertifikaten festgelegt wurden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Zertifikat Hierarchie](about-certificate-hierarchy.md)
</dt> <dt>

[Kreuz Zertifizierung](about-cross-certification.md)
</dt> <dt>

[Trust-Modelle](about-trust-models.md)
</dt> </dl>

 

 



