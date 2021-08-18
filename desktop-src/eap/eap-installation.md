---
title: EAP-Installation
description: Anbieter implementieren EAPs, auch als Authentifizierungsprotokolle bezeichnet, in DlLs (Dynamic Link Libraries).
ms.assetid: af10b1e9-45c9-4640-ba79-fc9c23cc3c47
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9a790f4282ef2658bacdd7f25be647234c3cf32d62ca80e8ce2745da3f4f738
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118984450"
---
# <a name="eap-installation"></a>EAP-Installation

Anbieter implementieren EAPs, auch als Authentifizierungsprotokolle bezeichnet, in DlLs (Dynamic Link Libraries). Eine DLL für das Authentifizierungsprotokoll muss sich sowohl auf dem Client- als auch auf dem Servercomputer befinden. Der Einfachheit halber können die Client- und Server-DLLs identisch sein. Dies ist jedoch keine Voraussetzung. Beachten Sie außerdem, dass dieselbe DLL möglicherweise mehr als ein Authentifizierungsprotokoll unterstützt.

Der Hersteller sollte Setupsoftware bereitstellen, um die DLL zu installieren und zu entfernen. Die Setupsoftware sollte auch die entsprechenden Schlüssel und Werte für das Authentifizierungsprotokoll in der Systemregistrierung erstellen und sie bei der Deinstallation entfernen.

Bei der Installation jeder EAP-DLL sollte der folgende Registrierungsschlüssel erstellt werden.

**HKEY \_ LOCAL \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **Rasman** \\ **COMMERCE** \\ **EAP** \\ **&lt; eaptypeid &gt;**

Im vorherigen Pfad ist **&lt; eaptypeid &gt;** die ID des Authentifizierungsprotokolls. Der Anbieter muss diese ID von der Internet Assigned Numbers Authority (IANA) abrufen.

Weitere Informationen und eine Beschreibung der unterstützten Werte für diesen Schlüssel finden Sie unter [Authentication Protocol Registry Values](authentication-protocol-registry-values.md).

 

 




