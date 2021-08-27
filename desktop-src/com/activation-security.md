---
title: Aktivierungssicherheit
description: Aktivierungssicherheit
ms.assetid: 0c13d473-a9f9-40b5-951b-731eab736fe6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4be436997889edd14704d5fa7646db689bba405825c1e8bcf9d021ea850ae70f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048908"
---
# <a name="activation-security"></a>Aktivierungssicherheit

Die Aktivierungssicherheit (auch als Startsicherheit bezeichnet) hilft dabei, zu steuern, wer einen Server starten kann. Die Aktivierungssicherheit wird automatisch vom Dienststeuerungs-Manager (Service Control Manager, SCM) eines bestimmten Computers angewendet. Beim Empfang einer Anforderung von einem Client, ein Objekt zu aktivieren (wie unter [Instanzerstellungs-Hilfsfunktionen](instance-creation-helper-functions.md)beschrieben), überprüft der SCM die Anforderung auf Informationen zur Aktivierungssicherheit, die in seiner Registrierung gespeichert sind. (Die Aktivierungssicherheit wird auch auf Aktivierungen auf demselben Computer überprüft.)

Beim Bestimmen der Identität des Clients wird bei der Aktivierung das im Aufruf von [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)des Clients festgelegte Verkleinerungsflag untersucht. Wenn das Cloaking-Flag festgelegt ist (für dynamisches oder statisches Verkleinern), wird das Threadtoken ( falls vorhanden) verwendet, um die Identität des Clients zu bestimmen. Wenn kein Cloaking festgelegt ist, wird das Prozesstoken anstelle des Threadtokens verwendet.

Weitere Informationen zur Aktivierungssicherheit finden Sie unter [**COAUTHINFO**](/windows/desktop/api/wtypesbase/ns-wtypesbase-coauthinfo) und [**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Sicherheit in COM](security-in-com.md)
</dt> </dl>

 

 