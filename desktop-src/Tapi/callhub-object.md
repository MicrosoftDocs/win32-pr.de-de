---
description: Das callhub-Objekt stellt eine Drittanbieter Ansicht eines mehr Parteien Aufrufes dar.
ms.assetid: ea23ae25-2fbb-4060-8273-cd7921d49e52
title: Callhub-Objekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d43594db13c9175490b4cbb0941d1fb4e45b2ced
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960106"
---
# <a name="callhub-object"></a>Callhub-Objekt

Das callhub-Objekt stellt eine Drittanbieter Ansicht eines mehr Parteien Aufrufes dar. Die zugeordneten Schnittstellen und Methoden erhalten und legen Informationen über den Hub fest, z. b. ob er aktiv ist. Mithilfe des callhub-Objekts kann ein Benutzer mit der erforderlichen Sicherheit andere Teilnehmer in einem Aufruf erkennen und möglicherweise steuern.

Ein callhub-Objekt kann nicht direkt von einer Anwendung erstellt werden. Ein callhub-Objekt wird indirekt erstellt, wenn ein eingehender Aufruf über TAPI 3 empfangen wird.

TAPI 3 nutzt TAPI-Dienstanbieter, um die erforderlichen Informationen über Aufrufe zur Implementierung mit dem callhub-Objekt bereitzustellen. Da nicht alle Dienstanbieter diese Informationen bereitstellen und nicht alle Hardware die callhub-Nachverfolgung unterstützen, sind die Informationen zu den anderen Benutzern in der Verbindung möglicherweise nur eingeschränkt oder nicht vorhanden.

Das Beispiel [Erstellen eines einfachen Konferenz](create-a-simple-conference.md) Codes veranschaulicht die Verwendung eines callhub-Objekts.

Unter [callhub-Objekt Schnittstellen](callhub-object-interfaces.md) finden Sie eine Liste aller Schnittstellen, die dem callhub-Objekt zugeordnet sind.

 

 



