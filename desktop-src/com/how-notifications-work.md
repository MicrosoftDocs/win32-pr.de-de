---
title: Funktionsweise von Benachrichtigungen
description: Funktionsweise von Benachrichtigungen
ms.assetid: faf66654-8233-49ac-a0fa-6cae51df0bea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9665b327d164a4e105f8adba3328be284fbe1fa0
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104391080"
---
# <a name="how-notifications-work"></a>Funktionsweise von Benachrichtigungen

Benachrichtigungen stammen aus der Objekt Anwendung und fließen mithilfe des Objekt Handlers zum Container. Wenn das Objekt ein verknüpftes Objekt ist, fängt das verknüpfte Objekt die Benachrichtigungen vom Objekt Handler ab und benachrichtigt den Container direkt.

Eine Objekt Anwendung muss Registrierungsanforderungen verwalten und nachverfolgen, wohin welche Benachrichtigungen gesendet und welche Benachrichtigungen gesendet werden sollen. OLE stellt zwei Komponenten Objekte zur Vereinfachung dieser Aufgabe bereit: oleadviseholder für Verbund Dokument Benachrichtigungen und dataadviseholder für Daten Benachrichtigungen.

Objekt Anwendungen bestimmen die Bedingungen, die das Senden der einzelnen Benachrichtigungen auffordern, sowie die Häufigkeit, mit der jede Benachrichtigung gesendet werden soll. Wenn es sinnvoll ist, mehrere Benachrichtigungen zu senden, spielt es keine Rolle, welche Benachrichtigung zuerst gesendet wird. Sie können in beliebiger Reihenfolge gesendet werden.

Die zeitliche Steuerung von Benachrichtigungen wirkt sich auf die Leistung und Koordination zwischen einer Objekt Anwendung und ihren Containern aus. Benachrichtigungen, die zu häufig zu langsam verarbeitet werden, führen zu einem nicht synchron gesendeten Benachrichtigungs Container. Die Benachrichtigungs Häufigkeit kann mit der Rate verglichen werden, mit der eine Anwendung neu zeichnet. Daher ist die Verwendung einer ähnlichen Logik für die zeitliche Steuerung von Benachrichtigungen (wie zum Neuzeichnen verwendet) ratsam.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**"Kreatedataadvierholder"**](/windows/win32/api/ole2/nf-ole2-createdataadviseholder)
</dt> <dt>

[**"Kreateoleadvicholder"**](/windows/desktop/api/Ole2/nf-ole2-createoleadviseholder)
</dt> <dt>

[Benachrichtigungen](notifications.md)
</dt> </dl>

 

 