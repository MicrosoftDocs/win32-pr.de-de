---
description: Der Entwurf von SSPI ermöglicht das Schreiben und Hinzufügen zusätzlicher SSPs zum System.
ms.assetid: 0d462340-e485-4746-b627-d823752462d9
title: Schreiben und Installieren eines Security Support Provider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e19f827ddf2b0352acc889df3ed1d5b3dfff52c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353552"
---
# <a name="writing-and-installing-a-security-support-provider"></a>Schreiben und Installieren eines Security Support Provider

Der Entwurf von SSPI ermöglicht das Schreiben und Hinzufügen zusätzlicher SSPs zum System. Ein [*SSP*](../secgloss/s-gly.md) , der für ein Sicherheitsmodell spezifisch ist, kann je nach Ebene der Integration mit dem Betriebssystem relativ einfach oder sehr komplex entwickelt werden. Ein Client-SSP, der Verbindungen mit einem neuen Servertyp zulässt, kann sehr schnell entwickelt werden, wohingegen ein vollständiger SSP, der einen lokalen Identitätswechsel bereitstellt, einen höheren Aufwand erfordert.

SSPs werden durch Aktualisieren eines **reg \_ SZ** -Werts in der Registrierung installiert, der sich wie folgt befindet:

**HKEY \_ Lokales \_ Computer** \\ **System** \\ **CurrentControlSet**- \\ **Steuer** Element \\ **SecurityProviders**  =  *Provider1.dll, Provider2.dll*...    <dl> <dt>

            Data type
</dt> <dd>            REG- \_ SZ</dd> </dl>

Eine einzelne DLL kann mehrere SSPs enthalten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Einschränkungen bei der Registrierung und Installation eines Sicherheitspakets](restrictions-around-registering-and-installing-a-security-package.md)
</dt> </dl>

 

 
