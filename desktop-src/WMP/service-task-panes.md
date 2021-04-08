---
title: Aufgabenbereiche für Dienste
description: Aufgabenbereiche für Dienste
ms.assetid: f626fa85-7590-4e87-bd5c-7ffdcb14be8b
keywords:
- Windows Media Player Online Stores, Aufgabenbereiche für Dienste
- Online Stores, Aufgabenbereiche für Dienste
- Typ 2 Online Stores, Dienstaufgaben Bereiche
- Windows Media Player Online Stores, Aufgabenbereiche
- Online Stores, Aufgabenbereiche
- Typ 2 Online Stores, Aufgabenbereiche
- Aufgabenbereiche für Windows Media Player, Dienste
- Windows Media Player, Aufgabenbereiche
- Aufgabenbereiche für Dienste
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4f882e46a7252792db5b551b25869c7711f9d31
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037108"
---
# <a name="service-task-panes"></a>Aufgabenbereiche für Dienste

In Windows Media Player 10 können Online Store-Anbieter Windows Media Player so konfigurieren, dass so viele als drei Aufgabenbereiche angezeigt werden, die als Dienstaufgaben Bereiche bezeichnet werden. Jeder Dienstaufgaben Bereich wird durch eine anpassbare Schaltfläche dargestellt, die von Windows Media Player auf der rechten Seite der Features-Taskleiste angezeigt wird.

Jeder Dienstaufgaben Bereich hostet eine Webseite, bei der es sich um die Benutzeroberfläche für eine bestimmte Online Store-Funktion handelt. Das Erscheinungsbild der Dienstaufgaben Bereiche wird durch das servicinput FO-XML-Dokument definiert. In diesem Dokument werden die Dienstaufgaben Bereiche durch drei Elemente dargestellt: **ServiceTask1**, **ServiceTask2** und **ServiceTask3**. Diese Dienstaufgaben Bereiche sollen Folgendes bereitstellen:

-   Ein Musikdienst.
-   Ein Videodienst.
-   Ein Radiodienst.

Sie können diese Features in einer beliebigen Reihenfolge in Windows Media Player positionieren, aber **ServiceTask1** muss der primäre Aufgabenbereich sein, damit Sie an der kommerziellen Aktivität beteiligt sind.

Die in jedem Dienstaufgaben Bereich gehostete Webseite hat Zugriff auf das **externe** Objekt. Dieses Objekt stellt Methoden, Eigenschaften und ein Ereignis bereit, die spezielle Funktionen für Webseiten in Windows Media Player bereitstellen. Beispielsweise können Sie das-Ereignis und die-Eigenschaften von **extern** verwenden, damit die Darstellung der Webseite dem Farbschema entspricht, das der Benutzer für Windows Media Player ausgewählt hat.

In Windows Media Player 11 sind keine Dienstaufgaben Bereiche vorhanden. Stattdessen gibt es eine einzelne Registerkarte " **Online Stores** ", die die Hauptwebseite für den aktiven Online Store hostet. Im serviceingefo-Dokument wird die Registerkarte " **Online Stores** " durch das **ServiceTask1** -Element dargestellt. die **ServiceTask2** -und **ServiceTask3** -Elemente werden ignoriert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Informationen zu Typ 2 Online Stores**](about-type-2-online-stores.md)
</dt> <dt>

[**Externes Objekt für den Typ 2-Online Speicher**](external-object-for-type-2-online-stores.md)
</dt> <dt>

[**ServiceInfo-Dokument für einen Typ 2-Online Store**](serviceinfo-document-for-a-type-2-online-store.md)
</dt> </dl>

 

 




