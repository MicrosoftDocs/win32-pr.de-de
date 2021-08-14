---
description: So wie das System Sicherheitsbeschreibungen verwendet, um den Zugriff auf sicherungsfähige Objekte zu steuern, kann ein Server Sicherheitsbeschreibungen verwenden, um den Zugriff auf seine privaten Objekte zu steuern. Weitere Informationen zum Windows-Sicherheitsmodell finden Sie unter Access Control-Modell.
ms.assetid: d6219438-711a-4eda-a893-9095bce3a07d
title: ACL-basierte Access Control
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52867b78114474e1b7827bddf8fd17cd2f3fd71cd88b62cff25397e8bab9b4ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117785165"
---
# <a name="acl-based-access-control"></a>ACL-basierte Access Control

So wie das System [Sicherheitsbeschreibungen](security-descriptors.md) verwendet, um den Zugriff auf sicherungsfähige Objekte zu steuern, kann ein Server Sicherheitsbeschreibungen verwenden, um den Zugriff auf seine privaten Objekte zu steuern. Weitere Informationen zum Windows-Sicherheitsmodell finden Sie unter [Access Control Model](access-control-model.md).

Ein geschützter Server kann [eine Sicherheitsbeschreibung](security-descriptors-for-private-objects.md) mit einer DACL erstellen, die die Zugriffstypen angibt, die für verschiedene [Vertrauensnehmer](trustees.md)zulässig sind. In einem einfachen Fall könnte der Server einen einzelnen Sicherheitsdeskriptor erstellen, um [den Zugriff auf alle Daten und Funktionen des Servers zu steuern.](checking-access-to-private-objects.md) Für eine präzisere Granularität des Schutzes kann der Server Sicherheitsbeschreibungen für jedes seiner privaten Objekte oder für verschiedene Arten von Funktionen erstellen.

Wenn beispielsweise ein Client den Server auffordert, ein neues Objekt in einer Datenbank zu erstellen, kann der Server eine Sicherheitsbeschreibung für das neue private Objekt erstellen. Der Server könnte dann den Sicherheitsdeskriptor mit dem privaten Objekt in der Datenbank speichern. Wenn ein Client versucht, auf das Objekt zuzugreifen, ruft der Server die Sicherheitsbeschreibung ab, um die Zugriffsrechte des Clients zu überprüfen. Es ist wichtig zu beachten, dass es in einer Sicherheitsbeschreibung nichts gibt, das sie dem Objekt oder der Funktionalität zuweist, das bzw. die sie schützt. Stattdessen liegt es an dem geschützten Server, die Zuordnung beizubehalten.

Der Zugriff auf das private Objekt kann ebenfalls überwacht werden. Eine Beschreibung finden Sie unter Überwachen des [Zugriffs auf private Objekte.](auditing-access-to-private-objects.md)

 

 



