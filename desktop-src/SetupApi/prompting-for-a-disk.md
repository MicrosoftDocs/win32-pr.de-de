---
description: Um ein Dialogfeld zu generieren, in dem der Benutzer aufgefordert wird, den nächsten Datenträger einzufügen oder einen neuen Quellpfad anzugeben, rufen Sie setuppromptfordisk auf.
ms.assetid: a780e7ab-bd96-43e4-9425-e15a758391f4
title: Eingabeaufforderung für einen Datenträger
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 404e88611ec21b7a29d69ab306dc0e7c4e1b98e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106347413"
---
# <a name="prompting-for-a-disk"></a>Eingabeaufforderung für einen Datenträger

Um ein Dialogfeld zu generieren, in dem der Benutzer aufgefordert wird, den nächsten Datenträger einzufügen oder einen neuen Quellpfad anzugeben, rufen Sie [**setuppromptfordisk**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptfordiska)auf. Diese Funktion wird von Rückruf Routinen verwendet, um eine Benutzeroberfläche zu generieren, wenn die Benachrichtigung [**spfilenotify \_ needmedia**](spfilenotify-needmedia.md)an die Rückruf Routine gesendet wird.

Das von [**setuppromptfordisk**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptfordiska) generierte Dialogfeld gibt dem Benutzer die Möglichkeit, einen Datenträger einzufügen, einen neuen Quellpfad anzugeben oder die Installation abzubrechen.

Sie können Flags verwenden, die beim Aufrufen von [**setuppromptfordisk**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptfordiska) angegeben wurden, um das Layout und Verhalten des Dialog Felds zu ändern. Mithilfe dieser Flags können Sie steuern, ob das Dialogfeld Schaltflächen enthält, die es dem Benutzer ermöglichen, einen neuen Quellpfad zu suchen oder die aktuelle Datei zu überspringen. Mit den Flags können Sie auch Dialogfeld Verhalten steuern, wie z. b. beim ersten anzeigen, und Sie können als Vordergrund Fenster angezeigt werden.

 

 



