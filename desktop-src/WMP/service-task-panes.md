---
title: Aufgabenbereiche des Diensts
description: Aufgabenbereiche des Diensts
ms.assetid: f626fa85-7590-4e87-bd5c-7ffdcb14be8b
keywords:
- Windows Media Player,Dienste-Aufgabenbereiche
- Onlineshops,Dienste-Aufgabenbereiche
- Geben Sie 2 Onlineshops,Dienste-Aufgabenbereiche ein.
- Windows Media Player,Aufgabenbereiche
- Onlineshops, Aufgabenbereiche
- Geben Sie 2 Onlineshops,Aufgabenbereiche ein.
- Windows Media Player,Service-Aufgabenbereiche
- Windows Media Player,Aufgabenbereiche
- Aufgabenbereiche des Diensts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d445e3fa5393dddb8e3dcc835317c8e5a284cb46f0a4a0e2b1f65fe2ea2d7b30
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119646510"
---
# <a name="service-task-panes"></a>Aufgabenbereiche des Diensts

In Windows Media Player 10 können Onlineshopanbieter Windows Media Player so konfigurieren, dass bis zu drei Aufgabenbereiche angezeigt werden, die als Dienstaufgabe bereiche bezeichnet werden. Jeder Dienstaufgabebereich wird durch eine anpassbare Schaltfläche dargestellt, Windows Media Player auf der rechten Seite der Taskleiste Features angezeigt wird.

Jeder Dienstaufgabebereich hostet eine Webseite, die die Benutzeroberfläche für ein bestimmtes Onlineshopfeature ist. Die Darstellung der Aufgabenbereiche des Diensts wird durch das ServiceInfo-XML-Dokument definiert. In diesem Dokument werden die Aufgabenbereiche des Diensts durch drei Elemente dargestellt: **ServiceTask1,** **ServiceTask2** und **ServiceTask3.** Diese Dienste-Aufgabenbereiche sollen Folgendes bereitstellen:

-   Ein Musikdienst.
-   Ein Videodienst.
-   Ein Funkdienst.

Sie können diese Features in Windows Media Player beliebigen Reihenfolge positionieren, aber **ServiceTask1** muss der primäre Aufgabenbereich für die Nutzung kommerzieller Aktivitäten sein.

Die webseite, die in jedem Dienstaufgabebereich gehostet wird, hat Zugriff auf das **Objekt External.** Dieses Objekt stellt Methoden, Eigenschaften und ein Ereignis zur Verfügung, die spezielle Funktionen für Webseiten in Windows Media Player. Beispielsweise können Sie das -Ereignis  und die Eigenschaften von Extern verwenden, um die Darstellung Ihrer Webseite mit dem Farbschema übereinstimmen zu lassen, das der Benutzer für die Windows Media Player.

In Windows Media Player 11 gibt es keine Dienste-Aufgabenbereiche. Stattdessen gibt es eine einzelne **Registerkarte Onlineshops,** die die Hauptwebseite für den aktiven Onlineshop hostet. Im ServiceInfo-Dokument wird die **Registerkarte Onlineshops** durch das **ServiceTask1-Element** dargestellt. Die **Elemente ServiceTask2** **und ServiceTask3** werden ignoriert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Informationen zu Onlineshops vom Typ 2**](about-type-2-online-stores.md)
</dt> <dt>

[**Externes Objekt für Onlinespeicher vom Typ 2**](external-object-for-type-2-online-stores.md)
</dt> <dt>

[**ServiceInfo-Dokument für eine Online-Store**](serviceinfo-document-for-a-type-2-online-store.md)
</dt> </dl>

 

 




