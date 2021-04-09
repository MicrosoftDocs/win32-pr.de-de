---
description: Dienst Objekt
ms.assetid: 4ce4e7f7-579d-41a5-a4e1-935ba0afce83
title: Dienst Objekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a3aabfc4e4366c54a5d30dbe5825f178378133d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868671"
---
# <a name="service-object"></a>Dienst Objekt

Das Dienst Objekt muss die folgenden Eigenschaften unterstützen.



| Eigenschaftsname                                                                                                                      | Erforderlich oder optional                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [WPD- \_ Objekt- \_ ID](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))                                                         | Erforderlich. .                                                                           |
| [übergeordnete WPD- \_ Objekt- \_ \_ ID](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))                                   | Erforderlich.                                                                             |
| [WPD- \_ Objekt \_ Name](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))                                                   | Erforderlich.                                                                             |
| [\_ \_ persistente \_ eindeutige \_ ID für WPD-Objekt](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85)) | Erforderlich.                                                                             |
| [WPD- \_ Objekt \_ IsHidden](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))                                       | Erforderlich, wenn das Dienst Objekt dem Benutzer nicht angezeigt werden soll.                       |
| [WPD- \_ Objekt \_ IsSystem](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))                                       | Erforderlich, wenn das Objekt ein Systemobjekt ist (z. b. eine Systemdatei). |
| [WPD- \_ Funktions \_ Objekt \_ Kategorie](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))     | Erforderlich. Dies stellt den Geräte Diensttyp dar, z. b. Dienst Kontakte.          |
| [WPD- \_ Dienst \_ Version](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))                                       | Erforderlich.                                                                             |
| [WPD \_ - \_ Speichertyp](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))                                                | Erforderlich, wenn der Dienst zum Speichern von Objekten verwendet wird.                                     |
| [WPD- \_ Speicher \_ Kapazität](/previous-versions/windows/hardware/drivers/ff597865(v=vs.85))                                    | Erforderlich, wenn der Dienst zum Speichern von Objekten verwendet wird.                                     |



 

## <a name="typical-resources"></a>Typische Ressourcen

Diese Objekte Hosten in der Regel keine Ressourcen.

## <a name="typical-formats"></a>Typische Formate

In der folgenden Liste werden typische Formate identifiziert, die vom Dienst Objekt verwendet werden. Dieses Objekt ist jedoch nicht auf diese Formate beschränkt.

-   Das WPD- \_ Objekt \_ Format ist \_ nicht angegeben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Anforderungen für Objekte**](requirements-for-objects.md)
</dt> </dl>

 

 
