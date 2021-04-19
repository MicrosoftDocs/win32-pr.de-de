---
description: Der Ressourcen-Manager wird als vertrauenswürdiger Dienst in einem einzelnen Prozess ausgeführt. Alle Anforderungen für den Smartcardzugriff werden auf den Ressourcen-Manager gerichtet, der Sie an den Reader weiterleitet, der die Ziel Karte enthält.
ms.assetid: 4a62588a-14d9-43dc-9572-25a9cbcd0efd
title: Ressourcen-Manager-Implementierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04ec653f999b74bb9851893b11e1fa49120a7bd6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348590"
---
# <a name="resource-manager-implementation"></a>Ressourcen-Manager-Implementierung

Der [*Ressourcen-Manager*](../secgloss/r-gly.md) wird als vertrauenswürdiger Dienst in einem einzelnen Prozess ausgeführt. Alle Anforderungen für den [*Smartcardzugriff*](../secgloss/s-gly.md) werden auf den Ressourcen-Manager gerichtet, der Sie an den [*Reader*](../secgloss/r-gly.md) weiterleitet, der die Ziel Karte enthält.

Smartcards werden häufig in Verbindung mit der Sicherheit und der persönlichen Privatsphäre verwendet. Wenn möglich, verwendet der Ressourcen-Manager die Sicherheitsmechanismen, die im zugrunde liegenden Betriebssystem vorhanden sind, wenn Sie auf einen Reader oder eine Smartcard zugreifen.

 

 
