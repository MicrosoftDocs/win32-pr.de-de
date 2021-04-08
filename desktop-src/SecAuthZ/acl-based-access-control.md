---
description: Ebenso wie das System Sicherheits Deskriptoren zum Steuern des Zugriffs auf Sicherungs fähige Objekte verwendet, kann ein Server Sicherheits Deskriptoren verwenden, um den Zugriff auf seine privaten Objekte zu steuern. Weitere Informationen zum Windows-Sicherheitsmodell finden Sie unter Access Control Modell.
ms.assetid: d6219438-711a-4eda-a893-9095bce3a07d
title: ACL-basiertes Access Control
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b477f998b7866c66860b94c3ff1266392f49373
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756184"
---
# <a name="acl-based-access-control"></a>ACL-basiertes Access Control

Ebenso wie das System [Sicherheits Deskriptoren](security-descriptors.md) zum Steuern des Zugriffs auf Sicherungs fähige Objekte verwendet, kann ein Server Sicherheits Deskriptoren verwenden, um den Zugriff auf seine privaten Objekte zu steuern. Weitere Informationen zum Windows-Sicherheitsmodell finden Sie unter [Access Control Modell](access-control-model.md).

Ein geschützter Server kann [eine Sicherheits Beschreibung](security-descriptors-for-private-objects.md) mit einer DACL erstellen, die die Zugriffs Typen angibt, die für verschiedene [Treuhänder](trustees.md)zulässig sind. In einem einfachen Fall könnte der Server einen einzelnen Sicherheits Deskriptor erstellen, um den [Zugriff auf alle Daten und Funktionen des Servers zu steuern](checking-access-to-private-objects.md). Um eine präzisere Granularität des Schutzes zu erzielen, könnte der Server Sicherheits Deskriptoren für die einzelnen privaten Objekte oder für verschiedene Arten von Funktionen erstellen.

Wenn ein Client z. b. den Server auffordert, ein neues Objekt in einer Datenbank zu erstellen, könnte der Server eine Sicherheits Beschreibung für das neue private Objekt erstellen. Der Server kann dann die Sicherheits Beschreibung mit dem privaten Objekt in der Datenbank speichern. Wenn ein Client versucht, auf das Objekt zuzugreifen, ruft der Server die Sicherheits Beschreibung ab, um die Zugriffsrechte des Clients zu überprüfen. Beachten Sie, dass es in einer Sicherheits Beschreibung nichts gibt, das Sie dem Objekt oder der Funktionalität zuordnet, das Sie schützt. Stattdessen ist es für den geschützten Server, die Zuordnung aufrechtzuerhalten.

Der Zugriff auf das private Objekt kann auch überwacht werden. Eine Beschreibung hierzu finden Sie unter Überwachen des [Zugriffs auf private Objekte](auditing-access-to-private-objects.md) .

 

 



