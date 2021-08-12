---
description: Sicherheitskontexteigenschaft
ms.assetid: 7ffae145-be13-4a2c-beb1-eaa1d11ad9a7
title: Sicherheitskontexteigenschaft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31c537dc8c9b925fff5f7fc4f3da99fd361bfb02f61008b7d7af8a421b9f1d11
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118546821"
---
# <a name="security-context-property"></a>Sicherheitskontexteigenschaft

Wie bei jedem automatischen Dienst, der von COM+ bereitgestellt wird, basiert die automatische Rollenüberprüfung auf Eigenschaften, die im Objektkontext enthalten sind. Die Ermittlung, ob bei einem Aufruf einer Komponente eine Sicherheitsüberprüfung durchgeführt werden muss, basiert auf der Sicherheitseigenschaft des Objektkontexts, der beim Instanziieren der konfigurierten Komponente erstellt wird.

In der Regel müssen Sie sich nicht um diese Eigenschaft sorgen. sie wird direkt von COM+ verwendet, nicht von Ihnen. Unter bestimmten Umständen möchten Sie jedoch möglicherweise eine strenge Kontrolle über die Aktivierung eines Objekts. In diesem Fall kann sich die Sicherheitseigenschaft darauf auswirken, in welchem Kontext Ihr Objekt aktiviert wird. Das heißt, wenn ein Objekt über eine Konfiguration verfügt, die mit dem Kontext seines Erstellers nicht kompatibel ist, wird es in seinem eigenen Kontext aktiviert. Die Sicherheitseigenschaft kann dies beeinflussen, ebenso wie jede Eigenschaft im Objektkontext.

Wenn Sie nicht möchten, dass Sicherheitseinstellungen die Aktivierung beeinflussen, können Sie nur zugriffsüberprüfung auf Prozessebene auswählen. Dadurch wird die Sicherheitseigenschaft für den Objektkontext unterdrückt, obwohl die rollenbasierte Überprüfung effektiv deaktiviert wird und Kontextinformationen für [Sicherheitsaufrufe nicht](security-call-context-information.md) verfügbar sind.

Weitere Informationen zu Zugriffsüberprüfungen auf Prozessebene finden Sie unter [Sicherheitsgrenzen.](security-boundaries.md) Informationen zum Festlegen der Sicherheit auf Prozessebene finden Sie unter [Festlegen einer Sicherheitsstufe für Zugriffsüberprüfungen.](setting-a-security-level-for-access-checks.md)

Weitere Informationen zum Objektkontext finden Sie unter [Kontexte.](com--contexts.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Effektives Entwerfen von Rollen](designing-roles-effectively.md)
</dt> <dt>

[Sicherheitsgrenzen](security-boundaries.md)
</dt> <dt>

[Kontextinformationen zu Sicherheitsaufrufen](security-call-context-information.md)
</dt> <dt>

[Verwenden von Rollen für die Clientautorisierung](using-roles-for-client-authorization.md)
</dt> </dl>

 

 



