---
description: Der Ressourcen-Manager wird als vertrauenswürdiger Dienst in einem einzigen Prozess ausgeführt. Alle Anforderungen für den Smartcardzugriff werden an den Ressourcen-Manager gestellt, der sie an den Leser weiter leitet, der die Zielkarte enthält.
ms.assetid: 4a62588a-14d9-43dc-9572-25a9cbcd0efd
title: Resource Manager-Implementierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9d0dfd21ed7da466f84e867a6d28b0e826fc5c4733f24d2f5e1f0562f1b4156
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118919149"
---
# <a name="resource-manager-implementation"></a>Resource Manager-Implementierung

Der [*Ressourcen-Manager*](../secgloss/r-gly.md) wird als vertrauenswürdiger Dienst in einem einzigen Prozess ausgeführt. Alle Anforderungen für den [*Smartcardzugriff*](../secgloss/s-gly.md) werden an den Ressourcen-Manager gestellt, der sie an den Leser weiter leitet, [*der*](../secgloss/r-gly.md) die Zielkarte enthält.

Smartcards werden häufig in Verbindung mit Sicherheit und persönlichem Datenschutz verwendet. Nach Möglichkeit verwendet der Ressourcen-Manager beim Zugriff auf einen Reader oder eine Smartcard die Sicherheitsmechanismen, die im zugrunde liegenden Betriebssystem vorhanden sind.

 

 
