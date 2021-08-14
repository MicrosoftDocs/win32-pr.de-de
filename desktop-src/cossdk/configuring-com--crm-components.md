---
description: CRM-Komponenten können entweder in einer COM+-Serveranwendung oder einer COM+-Bibliotheksanwendung installiert werden.
ms.assetid: d1ce3a0c-1278-498c-b5dc-4e14b26b4fc2
title: Konfigurieren von COM+-CRM-Komponenten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c79f8c9716a9a4db2888231c886d3d1a4d929dd1a8dfb9f9f359ab03ec7670b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118307449"
---
# <a name="configuring-com-crm-components"></a>Konfigurieren von COM+-CRM-Komponenten

CRM-Komponenten können entweder in einer COM+-Serveranwendung oder einer COM+-Bibliotheksanwendung installiert werden. Sie müssen jedoch immer in einer COM+-Serveranwendung ausgeführt werden. Wenn sie in einer COM+-Bibliotheksanwendung installiert sind, sind sie nicht für die Verwendung in Clientprozessen verfügbar.

Wenn die CRM-Komponenten in einer Bibliotheksanwendung installiert sind, sind sie für mehrere Serveranwendung verfügbar. Wenn sie in einer bestimmten Serveranwendung installiert sind, sind sie nur für diese bestimmte Serveranwendung verfügbar.

Um die Verwendung eines CRM in einer Serveranwendung zu aktivieren, führen Sie die folgenden Schritte aus:

1.  Klicken Sie unter Komponentendienste auf der Eigenschaftenseite der Serveranwendung auf die **Registerkarte** Erweitert.

2.  Wählen Sie **die Option Kompensierende Ressourcen-Manager aktivieren** für diese Serveranwendung aus. Wenn diese Option nicht ausgewählt ist, wird bei versuchen, ein CRM in dieser Serveranwendung zu verwenden, ein Fehler angezeigt.

    > [!Note]  
    > Wenn sie in einer Bibliotheksanwendung installiert ist, ist es nicht erforderlich, die Option Enable **compensating Resource Managers** (Kompensierende Ressourcen-Manager aktivieren) für diese Bibliotheksanwendung auszuwählen. Diese Option muss jedoch für die Serveranwendung ausgewählt werden, in der CRM ausgeführt werden soll.

     

Es wird empfohlen, die CRM-Worker- und CRM-Kompensatorkomponenten für ein bestimmtes CRM in derselben Anwendung zu installieren.

Die empfohlenen Einstellungen für CRM-Komponenten lauten wie folgt.



| Komponente           | Einstellung                                                                                             |
|---------------------|------------------------------------------------------------------------------------------------------|
| **CRM-Worker**      | transaction = requiredsync = yesJIT = yesthreading model = Both (oder threading model = Apartment)     |
| **CRM-Kompensator** | transaction = disabledsync = disabledJIT = nothreading model = Both (oder threading model = Apartment) |



 

> [!Note]  
> Komponenten, die crm verwenden, müssen explizit ein Threadingmodell angeben, wenn sie registriert werden. Die Standardeinstellung "Hauptthread-Apartment" wird nicht unterstützt. Die einzigen beiden unterstützten Threadingmodelle sind Apartment und Beide.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[COM+ Compensating Resource Manager Concepts](com--compensating-resource-manager-concepts.md)
</dt> </dl>

 

 



