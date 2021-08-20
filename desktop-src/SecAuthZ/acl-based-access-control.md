---
description: So wie das System Sicherheitsdeskriptoren verwendet, um den Zugriff auf sicherungsfähige Objekte zu steuern, kann ein Server Sicherheitsdeskriptoren verwenden, um den Zugriff auf seine privaten Objekte zu steuern. Weitere Informationen zum Sicherheitsmodell Windows Finden Sie unter Access Control Model.
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

So wie das System [Sicherheitsdeskriptoren](security-descriptors.md) verwendet, um den Zugriff auf sicherungsfähige Objekte zu steuern, kann ein Server Sicherheitsdeskriptoren verwenden, um den Zugriff auf seine privaten Objekte zu steuern. Weitere Informationen zum Windows-Sicherheitsmodell finden Sie unter [Access Control Model](access-control-model.md).

Ein geschützter Server kann [einen Sicherheitsdeskriptor](security-descriptors-for-private-objects.md) mit einer DACL erstellen, die die Zugriffstypen angibt, die für verschiedene Vertrauenshänder [zulässig sind.](trustees.md) In einem einfachen Fall könnte der Server eine einzelne Sicherheitsbeschreibung erstellen, um den Zugriff auf alle Daten und Funktionen des Servers [zu steuern.](checking-access-to-private-objects.md) Für eine präzisere Granularität des Schutzes könnte der Server Sicherheitsbeschreibungen für jedes seiner privaten Objekte oder für verschiedene Arten von Funktionen erstellen.

Wenn ein Client z. B. den Server zur Erstellung eines neuen Objekts in einer Datenbank bittet, könnte der Server einen Sicherheitsdeskriptor für das neue private Objekt erstellen. Der Server könnte dann die Sicherheitsbeschreibung mit dem privaten Objekt in der Datenbank speichern. Wenn ein Client versucht, auf das Objekt zu zugreifen, ruft der Server den Sicherheitsdeskriptor ab, um die Zugriffsrechte des Clients zu überprüfen. Es ist wichtig zu beachten, dass es in einem Sicherheitsdeskriptor nichts gibt, das es dem Objekt oder der Funktionalität zuordnt, das bzw. die er schützt. Stattdessen liegt es an dem geschützten Server, die Zuordnung zu verwalten.

Der Zugriff auf das private Objekt kann auch überwacht werden. Eine Beschreibung [finden Sie unter](auditing-access-to-private-objects.md) Überwachen des Zugriffs auf private Objekte.

 

 



