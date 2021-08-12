---
title: Informationen zur DDEML
description: In diesem Thema wird der dynamische Datenaustausch erläutert.
ms.assetid: 155b4cb0-dfbb-42f5-9fa3-8129349a0754
keywords:
- Windows Benutzeroberfläche,dynamische Daten Exchange (DDE)
- dynamische Daten Exchange (DDE), Informationen
- DDE (dynamische Daten Exchange),Informationen
- Datenaustausch, dynamische Daten Exchange (DDE)
- Windows Benutzeroberfläche,dynamische Daten Exchange Management Library (DDEML)
- dynamische Daten Exchange Management Library (DDEML), Informationen
- DDEML (dynamische Daten Exchange Management Library),Informationen
- Datenaustausch,dynamische Daten Exchange Management Library (DDEML)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 755d4efea534918ac3fd3da46364e3cb528e4199498ea7533c1635af6780cc08
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118545561"
---
# <a name="about-the-ddeml"></a>Informationen zur DDEML

dynamische Daten Exchange (DDE) unterscheidet sich vom Datenübertragungsmechanismus in der Zwischenablage. Ein Unterschied besteht darin, dass die Zwischenablage fast immer als einmalige Antwort auf eine bestimmte Aktion des Benutzers verwendet wird, z. B. durch Klicken auf **Einfügen** aus einem Menü. DDE kann zwar auch von einem Benutzer initiiert werden, wird aber in der Regel ohne weitere Beteiligung des Benutzers fortgesetzt.

Die dynamische Daten Exchange Management Library (DDEML) stellt eine Schnittstelle bereit, die das Hinzufügen von DDE-Funktionen zu einer Anwendung vereinfacht. Anstatt DDE-Nachrichten direkt zu senden, zu posten und zu verarbeiten, verwendet eine Anwendung die von der DDEML bereitgestellten Funktionen, um DDE-Konversationen zu verwalten. Eine DDE-Konversation ist die Interaktion zwischen Client- und Serveranwendungen. Die DDEML bietet auch eine Möglichkeit zum Verwalten der Zeichenfolgen und Daten, die von DDE-Anwendungen gemeinsam genutzt werden. Anstatt Atome und Zeiger auf Freigegebene Speicherobjekte zu verwenden, erstellen DDE-Anwendungen Zeichenfolgenhandles, die Zeichenfolgen identifizieren, und Datenhandles, die DDE-Objekte identifizieren, und tauschen sie aus. Die DDEML stellt eine Funktion ([**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice)) bereit, mit der eine Serveranwendung die unterstützten Dienstnamen registrieren kann. Die Dienstnamen werden dann an andere Anwendungen im System übertragen, die die Namen verwenden, um eine Verbindung mit dem Server herzustellen. Die DDEML stellt auch die Kompatibilität zwischen DDE-Anwendungen sicher, indem sie die konsistente Implementierung des DDE-Protokolls erfordert.

Vorhandene Anwendungen, die das nachrichtenbasierte DDE-Protokoll verwenden, sind vollständig mit anwendungen kompatibel, die die DDEML verwenden. Das heißt, eine Anwendung, die nachrichtenbasierte DDE verwendet, kann Konversationen herstellen und Transaktionen mit Anwendungen mithilfe der DDEML ausführen. Anstatt DDE-Nachrichten in Ihrer neuen Anwendung zu verwenden, nutzen Sie die DDEML und die vielen Verbesserungen, die sie bietet.

Um die DDEML verwenden zu können, müssen Sie die DDEML einschließen. H-Headerdatei in Ihren Quelldateien, Link mit USER32. LIB-Datei, und stellen Sie sicher, dass sich die DDEML.DLL Datei im Pfad des Systems befindet.

Wenn bei einer DDEML-Funktion ein Fehler auftritt, kann eine Anwendung die [**DdeGetLastError-Funktion**](/windows/desktop/api/Ddeml/nf-ddeml-ddegetlasterror) aufrufen, um die Ursache des Fehlers zu ermitteln. **DdeGetLastError** gibt einen Fehlerwert zurück, der die Ursache des letzten Fehlers angibt.

 

 




