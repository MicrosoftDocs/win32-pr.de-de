---
title: Identitätswechsel
description: Der Identitätswechsel ist die Fähigkeit eines Threads, in einem Sicherheitskontext auszuführen, der sich von dem Kontext des Prozesses unterscheidet, der den Thread besitzt.
ms.assetid: b33ca3b0-0423-4338-b3d6-4bb3db3d3e1b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a735fa12e175ecec5dc2a7ed741843d713532e19
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104039683"
---
# <a name="impersonation"></a>Identitätswechsel

Der Identitätswechsel ist die Fähigkeit eines Threads, in einem Sicherheitskontext auszuführen, der sich von dem Kontext des Prozesses unterscheidet, der den Thread besitzt. Bei der Ausführung im Sicherheitskontext des Clients ist der Server in gewissem Maße der Client. Der Server Thread verwendet ein Zugriffs Token, das die Anmelde Informationen des Clients darstellt, um Zugriff auf die Objekte zu erhalten, auf die der Client Zugriff hat.

Der Hauptgrund für einen Identitätswechsel besteht darin, Zugriffsprüfungen für die Identität des Clients zu initiieren. Wird die Identität des Clients für Zugriffsprüfungen verwendet, kann der Zugriff je nach den Berechtigungen des Clients entweder eingeschränkt oder erweitert werden. Nehmen wir beispielsweise an, dass ein Dateiserver über Dateien mit vertraulichen Informationen verfügt und jede dieser Dateien durch eine ACL geschützt wird. Um zu verhindern, dass ein Client nicht autorisierten Zugriff auf Informationen in diesen Dateien erhält, kann der Server die Identität des Clients annehmen, bevor er auf die Dateien zugreift.

## <a name="access-tokens-for-impersonation"></a>Zugriffs Token für Identitätswechsel

Zugriffs Token sind Objekte, die den Sicherheitskontext eines Prozesses oder Threads beschreiben. Sie stellen Informationen bereit, die die Identität eines Benutzerkontos und eine Teilmenge der Berechtigungen enthalten, die für das Benutzerkonto verfügbar sind. Jeder Prozess verfügt über ein *Primäres Zugriffs Token* , das den Sicherheitskontext des Benutzerkontos beschreibt, das dem Prozess zugeordnet ist. Standardmäßig verwendet das System das primäre Token, wenn ein Thread des Prozesses mit einem Sicherungs fähigen Objekt interagiert. Wenn jedoch ein Thread die Identität eines Clients annimmt, verfügt der Identitätswechsel Thread sowohl über ein primäres Zugriffs Token als auch über ein Identitätswechsel *Token*. Das Identitätswechsel Token stellt den Sicherheitskontext des Clients dar, und dieses Zugriffs Token ist das Zugriffs Token, das während des Identitäts Wechsels für Zugriffs Überprüfungen verwendet wird. Wenn sich der Identitätswechsel übersteigt, verwendet der Thread nur das primäre Zugriffs Token.

Sie können die [**OpenProcessToken**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocesstoken) -Funktion verwenden, um ein Handle für das primäre Token eines Prozesses zu erhalten. Verwenden Sie die [**openthletotokenfunktion**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openthreadtoken) , um ein Handle für das Identitätswechsel Token eines Threads zu erhalten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Zugriffs Token](/windows/desktop/SecAuthZ/access-tokens)
</dt> <dt>

[Delegierung und Identitätswechsel](delegation-and-impersonation.md)
</dt> </dl>

 

 