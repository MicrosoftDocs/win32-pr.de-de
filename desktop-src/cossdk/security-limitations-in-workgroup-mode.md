---
description: Sicherheitseinschränkungen im Arbeitsgruppen Modus
ms.assetid: 05c0aba7-b94b-49d4-a0fc-1ff0a23550b3
title: Sicherheitseinschränkungen im Arbeitsgruppen Modus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eabe38b8d05c49382ae6dd8337b883a6f4a8079a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345433"
---
# <a name="security-limitations-in-workgroup-mode"></a>Sicherheitseinschränkungen im Arbeitsgruppen Modus

Die Konfiguration der [Message Queuing](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) Arbeitsgruppe lässt nicht zu, dass der com+-Dienst in der Warteschlange die Anwendungssicherheit unterstützt. Wenn Sie Message Queuing mit der Arbeitsgruppen Konfiguration installiert haben, müssen Sie die [Sicherheit](specifying-the-authentication-protocol.md) für jede Anwendung in der Warteschlange, auf die in dieser Konfiguration zugegriffen wird, deaktivieren, indem Sie im Dialogfeld " **Eigenschaften** " der com+-Anwendung auf **der Registerkarte** "Queue" die Option **keine Meldungen authentifizieren** auswählen. Dies sollte nur in einem vertrauenswürdigen Netzwerk erfolgen und muss sowohl auf dem Client als auch auf dem Server ausgeführt werden, wenn die Anwendung bereits exportiert wurde.

 

 



