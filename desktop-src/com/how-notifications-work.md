---
title: Funktionsweise von Benachrichtigungen
description: Funktionsweise von Benachrichtigungen
ms.assetid: faf66654-8233-49ac-a0fa-6cae51df0bea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68e90dfeb6e1df6de50ddaa3264a8c5475d280f30a72ad2d8c6acfffd39d60fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119756370"
---
# <a name="how-notifications-work"></a>Funktionsweise von Benachrichtigungen

Benachrichtigungen stammen aus der Objektanwendung und fließen über den Objekthandler an den Container. Wenn das Objekt ein verknüpftes Objekt ist, fängt das verknüpfte Objekt die Benachrichtigungen vom Objekthandler ab und benachrichtigt den Container direkt.

Eine Objektanwendung muss Registrierungsanforderungen verwalten und nachverfolgen, wohin welche Benachrichtigungen gesendet werden sollen, und diese Benachrichtigungen gegebenenfalls senden. OLE bietet zwei Komponentenobjekte, um diese Aufgabe zu vereinfachen: oleAdviseHolder für Verbunddokumentbenachrichtigungen und DataAdviseHolder für Datenbenachrichtigungen.

Objektanwendungen bestimmen die Bedingungen, die zum Senden jeder bestimmten Benachrichtigung auffordern, und die Häufigkeit, mit der jede Benachrichtigung gesendet werden soll. Wenn es sinnvoll ist, mehrere Benachrichtigungen zu senden, spielt es keine Rolle, welche Benachrichtigung zuerst gesendet wird. sie können in beliebiger Reihenfolge gesendet werden.

Die zeitliche Steuerung von Benachrichtigungen wirkt sich auf die Leistung und Koordination zwischen einer Objektanwendung und ihren Containern aus. Während Benachrichtigungen zu häufig langsam verarbeitet werden, führen zu selten gesendete Benachrichtigungen zu einem nicht synchronisierten Container. Die Benachrichtigungshäufigkeit kann mit der Rate verglichen werden, mit der eine Anwendung neu gepaint wird. Daher ist die Verwendung einer ähnlichen Logik für die Zeitliche Steuerung von Benachrichtigungen (wie bei der Neupaintierung verwendet) ratsam.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**CreateDataAdviseHolder**](/windows/win32/api/ole2/nf-ole2-createdataadviseholder)
</dt> <dt>

[**CreateOleAdviseHolder**](/windows/desktop/api/Ole2/nf-ole2-createoleadviseholder)
</dt> <dt>

[Benachrichtigungen](notifications.md)
</dt> </dl>

 

 