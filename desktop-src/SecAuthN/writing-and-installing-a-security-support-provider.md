---
description: Der Entwurf von SSPI ermöglicht das Schreiben und Hinzufügen zusätzlicher SSPs zum System.
ms.assetid: 0d462340-e485-4746-b627-d823752462d9
title: Schreiben und Installieren eines Sicherheitssupportanbieters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11ac7125c386314ec7772a5e6079f423af0aaf5c9f7dd820a24c042d99834d74
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118914749"
---
# <a name="writing-and-installing-a-security-support-provider"></a>Schreiben und Installieren eines Sicherheitssupportanbieters

Der Entwurf von SSPI ermöglicht das Schreiben und Hinzufügen zusätzlicher SSPs zum System. Ein für ein Sicherheitsmodell spezifischer [*SSP*](../secgloss/s-gly.md) kann je nach Grad der Integration mit dem Betriebssystem relativ einfach oder mit hoher Komplexität entwickelt werden. Ein Client-SSP, der Verbindungen mit einem neuen Servertyp zulässt, kann sehr schnell entwickelt werden, während ein vollständiger SSP, der einen lokalen Identitätswechsel ermöglicht, mehr Aufwand erfordern würde.

SSPs werden installiert, indem ein **REG \_ SZ-Wert** in der Registrierung wie folgt aktualisiert wird:

**HKEY \_ LOCAL \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **SecurityProviders**  =  *Provider1.dll, Provider2.dll,*...    <dl> <dt>

            Data type
</dt> <dd>            REG \_ SZ</dd> </dl>

Eine einzelne DLL kann mehrere SSPs enthalten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Einschränkungen beim Registrieren und Installieren eines Sicherheitspakets](restrictions-around-registering-and-installing-a-security-package.md)
</dt> </dl>

 

 
