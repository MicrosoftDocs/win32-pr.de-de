---
description: Zusätzlich zur Verwendung des standardmäßigen Warteschlangenrückrufs können Sie eine benutzerdefinierte Rückrufroutine schreiben.
ms.assetid: 68781565-71a2-43bf-ad01-7c1cdc514f7b
title: Erstellen einer benutzerdefinierten Warteschlangenrückrufroutine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0602e32ef97ea962ca91375318bb563c0809da0dc4877aa6c9439644b52408e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118887506"
---
# <a name="creating-a-custom-queue-callback-routine"></a>Erstellen einer benutzerdefinierten Warteschlangenrückrufroutine

Zusätzlich zur Verwendung des standardmäßigen Warteschlangenrückrufs können Sie eine benutzerdefinierte Rückrufroutine schreiben. Diese Funktion muss das gleiche Formular wie [*FileCallback haben.*](/windows/win32/api/setupapi/nc-setupapi-psp_file_callback_a) Dies ist nützlich, wenn Sie eine Rückrufroutine benötigen, um eine Benachrichtigung auf eine andere Weise als die von der standarden Warteschlangenrückrufroutine bereitgestellte Zu behandeln.

Wenn nur ein kleiner Teil des Standardverhaltens der Warteschlangenrückrufroutine geändert werden muss, können Sie eine benutzerdefinierte Rückrufroutine erstellen, um die Benachrichtigungen zu filtern. Dabei werden nur die Benachrichtigungen, die ein besonderes Verhalten erfordern, und den [**Aufruf von SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka) für die anderen Benutzer durchgeführt.

Wenn Sie z. B. Fehler beim Löschen von Dateien benutzerdefinierte behandeln möchten, können Sie eine benutzerdefinierte Rückruffunktion erstellen: *MyCallback*. Diese Funktion würde [**SPFILENOTIFY \_ DELETEERROR-Benachrichtigungen**](spfilenotify-deleteerror.md) abfangen und verarbeiten und die Standardmäßige Warteschlangenrückruffunktion für alle anderen Benachrichtigungen aufrufen. *MyCallback gibt* einen Wert für die Benachrichtigungen zu Löschfehlern zurück. Für alle anderen Benachrichtigungen *übergibt MyCallback* den Wert, den die Standardmäßige Warteschlangenrückrufroutine an die Warteschlange zurückgegeben hat.

Dieser Ablauf der Steuerung wird im folgenden Diagramm veranschaulicht.

![Pfeile und Felder mit Datenfluss für benutzerdefinierte Rückruffunktion](images/callback.png)

> [!IMPORTANT]
> Wenn die benutzerdefinierte Rückruffunktion die Standardmäßige Warteschlangenrückrufroutine aufruft, muss sie den void-Zeiger, der von [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) oder [**SetupInitDefaultQueueCallbackEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallbackex) zurückgegeben wird, an die Standardrückrufroutine übergeben.

 

 

 
