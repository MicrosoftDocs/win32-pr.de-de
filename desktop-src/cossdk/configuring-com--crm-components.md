---
description: CRM-Komponenten können entweder in einer COM+-Serveranwendung oder in einer COM+-Bibliotheks Anwendung installiert werden.
ms.assetid: d1ce3a0c-1278-498c-b5dc-4e14b26b4fc2
title: Com+ CRM-Komponenten werden konfiguriert.
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f3614c2c34d36cb140f08529c05b31bcc5a4c7f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106342780"
---
# <a name="configuring-com-crm-components"></a>Com+ CRM-Komponenten werden konfiguriert.

CRM-Komponenten können entweder in einer COM+-Serveranwendung oder in einer COM+-Bibliotheks Anwendung installiert werden. Allerdings müssen Sie immer in einer COM+-Serveranwendung ausgeführt werden. Wenn Sie in einer COM+-Bibliotheks Anwendung installiert sind, sind Sie nicht für die Verwendung in Client Prozessen verfügbar.

Wenn die CRM-Komponenten in einer Bibliotheks Anwendung installiert sind, sind Sie für mehr als eine Serveranwendung verfügbar. Wenn Sie in einer bestimmten Serveranwendung installiert sind, sind Sie nur für die jeweilige Serveranwendung verfügbar.

Um die Verwendung eines CRM in einer Serveranwendung zu aktivieren, führen Sie die folgenden Schritte aus:

1.  Klicken Sie unter Komponenten Dienste auf der Seite Server Anwendungseigenschaften auf die Registerkarte **erweitert** .

2.  Wählen Sie die Option **kompensierende Ressourcen-Manager aktivieren** für die Serveranwendung aus. Wenn diese Option nicht ausgewählt ist, können Versuche, ein CRM innerhalb dieser Serveranwendung zu verwenden, nicht ausgeführt werden.

    > [!Note]  
    > Wenn Sie in einer Bibliotheks Anwendung installiert sind, ist es nicht erforderlich, die Option **kompensierende Ressourcen-Manager aktivieren** für diese Bibliotheks Anwendung auszuwählen. diese Option muss jedoch für die Serveranwendung ausgewählt werden, in der das CRM ausgeführt werden soll.

     

Es wird empfohlen, die CRM-Worker-und CRM-kompenatorkomponenten für ein bestimmtes CRM in derselben Anwendung zu installieren.

Die empfohlenen Einstellungen für CRM-Komponenten lauten wie folgt.



| Komponente           | Einstellungen                                                                                             |
|---------------------|------------------------------------------------------------------------------------------------------|
| **CRM-Worker**      | Transaction = Requirements dsync = yesjit = yesthreading Model = both (oder Threading Model = Apartment)     |
| **CRM-kompenator** | Transaction = disabledsync = disabledjit = nothreading Model = both (oder Threading Model = Apartment) |



 

> [!Note]  
> Komponenten, die das CRM verwenden, müssen beim Registrieren explizit ein Threading Modell angeben. Der Standardwert "Hauptthread-Apartment" wird nicht unterstützt. Die einzigen beiden unterstützten Threading Modelle sind Apartment und beides.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Kompensierende com+-Ressourcen-Manager Konzepte](com--compensating-resource-manager-concepts.md)
</dt> </dl>

 

 



