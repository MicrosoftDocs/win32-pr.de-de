---
description: Zusätzlich zur Verwendung des Standard Warteschlangen Rückrufs können Sie eine benutzerdefinierte Rückruf Routine schreiben.
ms.assetid: 68781565-71a2-43bf-ad01-7c1cdc514f7b
title: Erstellen einer benutzerdefinierten Warteschlangen Rückruf Routine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a119836e994709ff2d0fa21e12489af947394119
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866940"
---
# <a name="creating-a-custom-queue-callback-routine"></a>Erstellen einer benutzerdefinierten Warteschlangen Rückruf Routine

Zusätzlich zur Verwendung des Standard Warteschlangen Rückrufs können Sie eine benutzerdefinierte Rückruf Routine schreiben. Diese Funktion muss dieselbe Form wie [*File Callback*](/windows/win32/api/setupapi/nc-setupapi-psp_file_callback_a)aufweisen. Dies ist hilfreich, wenn Sie eine Rückruf Routine benötigen, um eine Benachrichtigung auf eine andere Weise als die von der Standard Warteschlangen-Rückruf Routine bereitgestellte zu verarbeiten.

Wenn nur ein kleiner Teil des Verhaltens der Standard Warteschlangen Rückruf Routine geändert werden muss, können Sie eine benutzerdefinierte Rückruf Routine erstellen, um die Benachrichtigungen zu filtern, und nur diejenigen behandeln, die ein spezielles Verhalten erfordern und [**setupdefaultqueuecallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka) für die anderen aufrufen.

Wenn Sie z. b. Datei Lösch Fehler Benutzer definiert behandeln möchten, können Sie eine benutzerdefinierte Rückruffunktion ( *MyCallback*) erstellen. Diese Funktion würde [**spfilenotify \_ deleteerror**](spfilenotify-deleteerror.md) -Benachrichtigungen abfangen und verarbeiten und die standardmäßige Warteschlangen Rückruffunktion für alle anderen Benachrichtigungen aufrufen. *MyCallback* gibt einen Wert für die Fehler Benachrichtigungen zum Löschen zurück. Für alle anderen Benachrichtigungen übergibt *MyCallback* den Wert, der von der Standard Warteschlangen Rückruf-Routine an die Warteschlange zurückgegeben wurde.

Diese Ablauf Steuerung wird in der folgenden Abbildung veranschaulicht.

![Pfeile und Felder mit Datenfluss für benutzerdefinierte Rückruffunktion](images/callback.png)

> [!IMPORTANT]
> Wenn die benutzerdefinierte Rückruffunktion die standardmäßige Warteschlangen Rückruf-Routine aufruft, muss Sie den von [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) oder [**setupinitdefaultqueuecallbackex**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallbackex) zurückgegebenen void-Zeiger an die Standard Rückruf Routine übergeben.

 

 

 
