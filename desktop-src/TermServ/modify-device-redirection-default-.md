---
title: Ändern der Standardeinstellung für Geräte Umleitung
description: Da Remotedesktop Gatewayserver versuchen, sichere Geräte Umleitungs Richtlinien zu erzwingen, bevor Sie die Client Verbindung an einen Remotedesktop-Sitzungshost Server weiterleiten, müssen Sie diese Standardeinstellung möglicherweise in einigen Fällen deaktivieren.
ms.assetid: 03F2617C-D478-4A51-9EEC-E9643CA831B7
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 925099b94c75dca39d381bdf57ae9730fb840da7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856292"
---
# <a name="modify-device-redirection-default"></a>Ändern der Standardeinstellung für Geräte Umleitung

Da Remotedesktop Gatewayserver versuchen, sichere Geräte Umleitungs Richtlinien zu erzwingen, bevor Sie die Client Verbindung an einen Remotedesktop-Sitzungshost Server weiterleiten, müssen Sie diese Standardeinstellung möglicherweise in einigen Fällen deaktivieren.

Unter Windows Server 2008 R2 und höher wird von Remotedesktop Gatewayservern standardmäßig versucht, sichere Geräte Umleitungs Richtlinien zu erzwingen, bevor die Client Verbindung an einen Remotedesktop-Sitzungshost Server weitergeleitet wird. Diese Funktion wird jedoch von einigen Servern nicht unterstützt. Dies wird z. b. für Verbindungen zu Hyper-V-Konsolen Sitzungen nicht unterstützt, und es ist möglicherweise erforderlich, die Standardeinstellung zu deaktivieren, um die Verbund Authentifizierung zu unterstützen. In diesen Fällen kann dieses Feature deaktiviert werden, indem Sie den folgenden Registrierungsschlüssel erstellen, um Verbindungen zuzulassen.

**HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ Terminal Server Gateway \\ prerdpdisableregkey**

Wenn dieser Schlüssel vorhanden ist, erzwingt das Remotedesktop Gateway keine Geräte Umleitung.

 

 




