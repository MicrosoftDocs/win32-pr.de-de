---
title: Remote Registrierungs Zugriff in 64-Bit-Windows
description: Der registrierungsredirector bietet über die regconnectregistry-Funktion Remote Zugriff auf die Registrierung auf 64-Bit-Fenstern.
ms.assetid: 7873c1e2-53fb-4c93-bf4c-251a13cd8db7
keywords:
- Remote Registrierungs Zugriff 64-Bit-Windows-Programmierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a139198ca08e0fdb9d7bcb070dcabf89dfa5403
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106340711"
---
# <a name="remote-registry-access-in-64-bit-windows"></a>Remote Registrierungs Zugriff in 64-Bit-Windows

Der registrierungsredirector bietet über die [**regconnectregistry**](/windows/desktop/api/winreg/nf-winreg-regconnectregistrya) -Funktion Remote Zugriff auf die Registrierung auf 64-Bit-Fenstern.

Handelt es sich bei dem Client um eine 32-Bit-Anwendung, greift er auf die standardmäßige 32-Bit-Registrierungs Ansicht des Servers zu. Wenn es sich bei dem Client um eine 64-Bit-Anwendung handelt, greift er auf die 64-Bit-Registrierungs Ansicht zu.

**Windows Server 2003:** Alle Clients greifen auf die 64-Bit-Registrierungs Ansicht zu, es sei denn, die Anwendung verwendet das Key \_ WOW64 \_ 32key-Flag. Dieses Verhalten hat sich in Windows Server 2003 mit Service Pack 1 (SP1) und Windows XP Professional x64 Edition geändert, vorausgesetzt, dass sowohl der Client als auch der Server diese Versionen von Windows ausführen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Registrierungs Redirector](registry-redirector.md)
</dt> <dt>

[Registrierungs Reflektion](registry-reflection.md)
</dt> </dl>

 

 