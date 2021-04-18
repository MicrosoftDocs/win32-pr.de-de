---
title: Ändern der Sicherheits Standardwerte für einen Computer
description: Ändern der Sicherheits Standardwerte für einen Computer
ms.assetid: c6d84375-59ea-42d5-87f9-af514b6f7d7c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6607e7a17e7db1f8852dff42e62384c730090bbb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104387950"
---
# <a name="modifying-the-security-defaults-for-a-computer"></a>Ändern der Sicherheits Standardwerte für einen Computer

Es wird nicht empfohlen, die systemweiten Sicherheitseinstellungen zu ändern, da dies Auswirkungen auf alle com-Server Anwendungen hat, die nicht Ihre eigene Prozess weite Sicherheit festlegen, und möglicherweise verhindern, dass Sie ordnungsgemäß funktionieren. Wenn Sie die systemweiten Sicherheitseinstellungen ändern, um die Sicherheitseinstellungen für eine bestimmte COM-Anwendung zu beeinflussen, sollten Sie stattdessen die Prozess weiten Sicherheitseinstellungen für die jeweilige COM-Anwendung ändern. Weitere Informationen zum Festlegen der Prozess weiten Sicherheit finden Sie unter [Setting Process-Wide Security](setting-processwide-security.md).

Bestimmte Werte in der Registrierung bestimmen die Sicherheitseinstellungen für Anwendungen, die [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)nicht aufzurufen. Sie können diese Einstellungen mit Dcomcnfg.exe ändern.

Weitere Informationen finden Sie unter den folgenden Themen:

-   [Registrierungs Werte für die System-Wide Sicherheit](registry-values-for-machine-wide-security.md)
-   [Festlegen der System-Wide Sicherheit mithilfe von DCOMCNFG](setting-machine-wide-security-using-dcomcnfg.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Festlegen der Prozess weiten Sicherheit](setting-processwide-security.md)
</dt> <dt>

[Festlegen der Sicherheit für COM-Anwendungen](setting-security-for-com-applications.md)
</dt> </dl>

 

 




