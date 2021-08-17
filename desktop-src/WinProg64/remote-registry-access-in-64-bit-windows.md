---
title: Remoteregistrierungszugriff in 64-Bit-Windows
description: Der Registrierungs-Redirector bietet Remotezugriff auf die Registrierung auf 64-Bit-Windows über die RegConnectRegistry-Funktion.
ms.assetid: 7873c1e2-53fb-4c93-bf4c-251a13cd8db7
keywords:
- 64-Bit-Windows-Programmierung für den Remoteregistrierungszugriff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f066641b080ace60a62c882a4abd0190e20537259517a2e789b4d450e352349
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118561451"
---
# <a name="remote-registry-access-in-64-bit-windows"></a>Remoteregistrierungszugriff in 64-Bit-Windows

Der Registrierungs-Redirector bietet Remotezugriff auf die Registrierung auf 64-Bit-Windows über die [**RegConnectRegistry-Funktion.**](/windows/desktop/api/winreg/nf-winreg-regconnectregistrya)

Wenn der Client eine 32-Bit-Anwendung ist, greift er auf die standardmäßige 32-Bit-Registrierungsansicht des Servers zu. Wenn der Client eine 64-Bit-Anwendung ist, greift er auf die 64-Bit-Registrierungsansicht zu.

**Windows Server 2003:** Alle Clients greifen auf die 64-Bit-Registrierungsansicht zu, es sei denn, die Anwendung verwendet das \_ KEY WOW64 \_ 32KEY-Flag. Dieses Verhalten hat sich mit Windows Server 2003 mit Service Pack 1 (SP1) und Windows XP Professional x64 Edition geändert, vorausgesetzt, dass sowohl der Client als auch der Server diese Versionen von Windows ausführen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Registrierungsumleitung](registry-redirector.md)
</dt> <dt>

[Registrierungsreflektion](registry-reflection.md)
</dt> </dl>

 

 