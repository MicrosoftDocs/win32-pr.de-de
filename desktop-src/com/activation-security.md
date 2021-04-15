---
title: Aktivierungs Sicherheit
description: Aktivierungs Sicherheit
ms.assetid: 0c13d473-a9f9-40b5-951b-731eab736fe6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e5b01b918666e911d96ed16528ba5045103f445
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104474405"
---
# <a name="activation-security"></a>Aktivierungs Sicherheit

Die Aktivierungs Sicherheit (auch als Start Sicherheit bezeichnet) unterstützt die Steuerung der Benutzer, die einen Server starten können. Die Aktivierungs Sicherheit wird automatisch durch den Dienststeuerungs-Manager (Service Control Manager, SCM) eines bestimmten Computers angewendet. Beim Empfang einer Anforderung von einem Client zum Aktivieren eines Objekts (wie in [Hilfsfunktionen](instance-creation-helper-functions.md)für die Instanzerstellung beschrieben) überprüft der SCM die Anforderung auf die in der Registrierung gespeicherten Aktivierungs Sicherheitsinformationen. (Die Aktivierungs Sicherheit wird auch für dieselben Computer Aktivierungen geprüft.)

Beim Bestimmen der Identität des Clients prüft die Aktivierung das Cloaking-Flag, das im Client- [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)-Befehl festgelegt wurde. Wenn das Cloaking-Flag festgelegt ist (für dynamisches oder statisches Cloaking), wird das Thread Token verwendet, falls vorhanden, um die Identität des Clients zu bestimmen. Wenn kein Cloaking festgelegt ist, wird das Prozess Token anstelle des Thread Tokens verwendet.

Weitere Informationen zur Aktivierungs Sicherheit finden Sie unter [**coauthinfo**](/windows/desktop/api/wtypesbase/ns-wtypesbase-coauthinfo) und [**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Sicherheit in com](security-in-com.md)
</dt> </dl>

 

 