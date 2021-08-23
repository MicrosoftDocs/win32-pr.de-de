---
title: Ändern der Standardeinstellung für die Geräteumleitung
description: Da Remotedesktop Gatewayserver versuchen, sichere Richtlinien für die Geräteumleitung zu erzwingen, bevor die Clientverbindung an einen Remotedesktop-Sitzungshost-Server übergeben wird, müssen Sie diese Standardeinstellung möglicherweise in einigen Fällen deaktivieren.
ms.assetid: 03F2617C-D478-4A51-9EEC-E9643CA831B7
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b74515f6bf79b42c129ec7c113729b9871d4e4bfb0101f845f91dcac0d49237
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119138169"
---
# <a name="modify-device-redirection-default"></a>Ändern der Standardeinstellung für die Geräteumleitung

Da Remotedesktop Gatewayserver versuchen, sichere Richtlinien für die Geräteumleitung zu erzwingen, bevor die Clientverbindung an einen Remotedesktop-Sitzungshost-Server übergeben wird, müssen Sie diese Standardeinstellung möglicherweise in einigen Fällen deaktivieren.

Auf Windows Server 2008 R2 und höher versuchen Remotedesktop Gatewayserver standardmäßig, sichere Richtlinien für die Geräteumleitung zu erzwingen, bevor die Clientverbindung an einen Remotedesktop-Sitzungshost übergeben wird. Dieses Feature wird jedoch von einigen Servern nicht unterstützt. Dies wird beispielsweise für Verbindungen mit Hyper-V-Konsolensitzungen nicht unterstützt, und es kann erforderlich sein, die Standardeinstellung zu deaktivieren, um die Verbundauthentifizierung zu unterstützen. In diesen Fällen kann dieses Feature deaktiviert werden, indem der folgende Registrierungsschlüssel erstellt wird, damit Verbindungen möglich sind.

**HKEY \_ LOCAL MACHINE Software Microsoft Terminal Server Gateway \_ \\ \\ \\ \\ preRDPDisableRegKey**

Wenn dieser Schlüssel vorhanden ist, erzwingt Remotedesktop Gateway keine Geräteumleitung.

 

 




