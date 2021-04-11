---
description: Sicherheitskontext Eigenschaft
ms.assetid: 7ffae145-be13-4a2c-beb1-eaa1d11ad9a7
title: Sicherheitskontext Eigenschaft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54b061ef7c0d0d0c146b626c11fd550c48ab488a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214279"
---
# <a name="security-context-property"></a>Sicherheitskontext Eigenschaft

Wie bei jedem von com+ bereitgestellten automatischen Dienst basiert die automatische Rollen Überprüfung auf den Eigenschaften, die im Objekt Kontext enthalten sind. Die Bestimmung, ob eine Sicherheitsüberprüfung für einen-Rückruf in einer-Komponente durchgeführt werden muss, basiert auf der Security-Eigenschaft des Objekt Kontexts, der erstellt wird, wenn die konfigurierte Komponente instanziiert wird.

Im Allgemeinen müssen Sie sich nicht mit dieser Eigenschaft befassen. Sie wird direkt von com+ verwendet, nicht von Ihnen. In einigen Fällen möchten Sie jedoch möglicherweise eine strikte Kontrolle über die Aktivierung eines Objekts haben. In diesem Fall kann die Security-Eigenschaft den Kontext beeinflussen, in dem Ihr Objekt aktiviert ist. Das heißt, wenn für ein Objekt eine Konfiguration mit dem Kontext des Erstellers nicht kompatibel ist, wird es in einem eigenen Kontext aktiviert. Die Security-Eigenschaft kann dies beeinflussen, ebenso wie jede Eigenschaft im Objekt Kontext.

Wenn Sie nicht möchten, dass die Sicherheitseinstellungen die Aktivierung beeinflussen, können Sie nur die Zugriffs Überprüfung auf Prozessebene auswählen. Dadurch wird die Security-Eigenschaft des Objekt Kontexts unterdrückt, obwohl die rollenbasierte Überprüfung deaktiviert wird und die [Kontextinformationen für den Sicherheits Rückruf](security-call-context-information.md) nicht verfügbar sind.

Weitere Informationen zu Zugriffs Überprüfungen auf Prozessebene finden Sie unter [Sicherheitsgrenzen](security-boundaries.md). Informationen zum Festlegen der Sicherheit auf Prozessebene finden Sie unter [Festlegen einer Sicherheitsstufe für Zugriffs Überprüfungen](setting-a-security-level-for-access-checks.md).

Weitere Informationen zum Objekt Kontext finden Sie unter [Kontexte](com--contexts.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Effektives Entwerfen von Rollen](designing-roles-effectively.md)
</dt> <dt>

[Sicherheitsgrenzen](security-boundaries.md)
</dt> <dt>

[Informationen zum Sicherheits Aufrufkontext](security-call-context-information.md)
</dt> <dt>

[Verwenden von Rollen für die Client Autorisierung](using-roles-for-client-authorization.md)
</dt> </dl>

 

 



