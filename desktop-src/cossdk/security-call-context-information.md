---
description: Kontextinformationen für Sicherheitsaufrufe
ms.assetid: 8b170c17-f095-4c25-9ee2-480681b7e5f6
title: Kontextinformationen für Sicherheitsaufrufe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0aed07f79fdba16f0ea6139a58cc50871d795e1eacbf94737b04dbf5f1fe900
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118546867"
---
# <a name="security-call-context-information"></a>Kontextinformationen für Sicherheitsaufrufe

Die rollenbasierte Sicherheit basiert auf einem allgemeinen Mechanismus, mit dem Sie Sicherheitsinformationen zu allen Upstreamaufrufern in der Kette der Aufrufe ihrer Komponente abrufen können. Diese Informationen sind nur verfügbar, wenn die Rollenüberprüfung auf Komponentenebene aktiviert ist. Ausführliche Informationen zum Festlegen der Sicherheit auf Komponentenebene finden Sie unter [Festlegen einer Sicherheitsstufe für Zugriffsüberprüfungen.](setting-a-security-level-for-access-checks.md)

Sie können die [**ISecurityCallContext-Schnittstelle**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext) verwenden, um programmgesteuert auf Sicherheitsaufrufkontextinformationen zuzugreifen. Eine Beschreibung finden Sie unter [Programmgesteuerte Komponentensicherheit.](programmatic-component-security.md)

Der Kontext für Sicherheitsaufrufe wird jedes Mal übergeben, wenn eine Sicherheitsgrenze überschritten wird. Für Aufrufe zwischen Komponenten innerhalb einer Anwendung, die sich innerhalb derselben Sicherheitsgrenze befinden, werden keine Aufrufkontextinformationen übergeben. Für Aufrufe zwischen Prozessen oder zwischen Anwendungen innerhalb eines Prozesses werden Kontextinformationen entlang von aufgerufen.

Diese Funktion ist besonders nützlich, wenn Sie eine detaillierte Überwachung und Protokollierung durchführen möchten. Sie können Sicherheitsinformationen für jeden Upstreamaufrufer abrufen und aufzeichnen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Effektives Entwerfen von Rollen](designing-roles-effectively.md)
</dt> <dt>

[Sicherheitsgrenzen](security-boundaries.md)
</dt> <dt>

[Sicherheitskontexteigenschaft](security-context-property.md)
</dt> <dt>

[Verwenden von Rollen für die Clientautorisierung](using-roles-for-client-authorization.md)
</dt> </dl>

 

 



