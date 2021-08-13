---
description: Dienstobjekt
ms.assetid: 4ce4e7f7-579d-41a5-a4e1-935ba0afce83
title: Dienstobjekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2587ca25e1e9fc225a0b555263bf3f3f4e725c83e5f9b01e716fd6fa191fc270
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119445583"
---
# <a name="service-object"></a>Dienstobjekt

Das Dienstobjekt muss die folgenden Eigenschaften unterstützen.



| Eigenschaftsname                                                                                                                      | Erforderlich oder optional                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [\_ \_ WPD-OBJEKT-ID](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))                                                         | Erforderlich. .                                                                           |
| [ÜBERGEORDNETE ID \_ DES WPD-OBJEKTS \_ \_](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))                                   | Erforderlich.                                                                             |
| [\_WPD-OBJEKTNAME \_](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))                                                   | Erforderlich.                                                                             |
| [PERSISTENTE EINDEUTIGE ID \_ DES WPD-OBJEKTS \_ \_ \_](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85)) | Erforderlich.                                                                             |
| [\_WPD-OBJEKT \_ ISHIDDEN](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))                                       | Erforderlich, wenn das Dienstobjekt dem Benutzer nicht angezeigt werden soll.                       |
| [\_WPD-OBJEKT \_ ISSYSTEM](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))                                       | Erforderlich, wenn das -Objekt ein Systemobjekt ist (z. B. stellt es eine Systemdatei dar). |
| [WPD \_ FUNCTIONAL \_ OBJECT \_ CATEGORY](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))     | Erforderlich. Dies stellt den Gerätediensttyp dar, z. B. SERVICE Contacts.          |
| [\_WPD-DIENSTVERSION \_](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))                                       | Erforderlich.                                                                             |
| [\_WPD-SPEICHERTYP \_](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))                                                | Erforderlich, wenn der Dienst zum Speichern von Objekten verwendet wird.                                     |
| [\_ \_ WPD-SPEICHERKAPAZITÄT](/previous-versions/windows/hardware/drivers/ff597865(v=vs.85))                                    | Erforderlich, wenn der Dienst zum Speichern von Objekten verwendet wird.                                     |



 

## <a name="typical-resources"></a>Typische Ressourcen

Diese Objekte hosten in der Regel keine Ressourcen.

## <a name="typical-formats"></a>Typische Formate

In der folgenden Liste sind typische Formate aufgeführt, die vom Dienstobjekt verwendet werden. Dieses Objekt ist jedoch nicht auf diese Formate beschränkt.

-   \_ \_ WPD-OBJEKTFORMAT \_ NICHT ANGEGEBEN

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Anforderungen für Objekte**](requirements-for-objects.md)
</dt> </dl>

 

 
