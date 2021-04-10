---
description: Informationen zum Sicherheits Aufrufkontext
ms.assetid: 8b170c17-f095-4c25-9ee2-480681b7e5f6
title: Informationen zum Sicherheits Aufrufkontext
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 213e21d684d004ed18e5b9aa536e03ae8292307e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214281"
---
# <a name="security-call-context-information"></a>Informationen zum Sicherheits Aufrufkontext

Die rollenbasierte Sicherheit basiert auf einem allgemeinen Mechanismus, mit dem Sie Sicherheitsinformationen zu allen upstreamaufrufern in der Kette von Aufrufen Ihrer Komponente abrufen können. Diese Informationen sind nur verfügbar, wenn die Rollen Überprüfung auf Komponentenebene aktiviert ist. Ausführliche Informationen zum Festlegen der Sicherheit auf Komponentenebene finden Sie unter [Festlegen einer Sicherheitsstufe für Zugriffs Überprüfungen](setting-a-security-level-for-access-checks.md).

Sie können die [**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext) -Schnittstelle verwenden, um Programm gesteuert auf Kontextinformationen für den Sicherheits Aufruf zuzugreifen. Eine Beschreibung finden Sie Unterprogramm gesteuerte [Komponentensicherheit](programmatic-component-security.md).

Der Kontext für den Sicherheits Aufruf wird bei jedem Überschreiten einer Sicherheitsgrenze weitergegeben. Bei Aufrufen zwischen Komponenten innerhalb einer Anwendung, die sich innerhalb derselben Sicherheitsgrenze befinden, werden keine Aufruf Kontextinformationen übermittelt. Bei Aufrufen zwischen Prozessen oder Anwendungen innerhalb eines Prozesses rufen Sie Kontextinformationen auf.

Diese Funktion ist besonders nützlich, wenn Sie eine ausführliche Überwachung und Protokollierung durchführen möchten. Sie können Sicherheitsinformationen für jeden Upstreamaufrufer abrufen und aufzeichnen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Effektives Entwerfen von Rollen](designing-roles-effectively.md)
</dt> <dt>

[Sicherheitsgrenzen](security-boundaries.md)
</dt> <dt>

[Sicherheitskontext Eigenschaft](security-context-property.md)
</dt> <dt>

[Verwenden von Rollen für die Client Autorisierung](using-roles-for-client-authorization.md)
</dt> </dl>

 

 



