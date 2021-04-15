---
title: Informationen zur Ddeml
description: In diesem Thema wird der dynamische Datenaustausch erläutert.
ms.assetid: 155b4cb0-dfbb-42f5-9fa3-8129349a0754
keywords:
- Windows-Benutzeroberfläche, dynamischer Datenaustausch (DDE)
- Dynamischer Datenaustausch (DDE), Informationen zu
- DDE (dynamischer Datenaustausch), Informationen zu
- Datenaustausch, dynamischer Datenaustausch (DDE)
- Windows-Benutzeroberfläche, dynamischer Datenaustausch Verwaltungs Bibliothek (Ddeml)
- Dynamischer Datenaustausch Management Library (Ddeml), Informationen zu
- Ddeml (dynamischer Datenaustausch Verwaltungs Bibliothek), Informationen zu
- Datenaustausch, dynamischer Datenaustausch Verwaltungs Bibliothek (Ddeml)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84ed77565c8b4e20841ad2ef80ae84c1f5c39724
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104516088"
---
# <a name="about-the-ddeml"></a>Informationen zur Ddeml

Dynamischer Datenaustausch (DDE) unterscheidet sich vom Datenübertragungsmechanismus für Zwischenablage. Ein Unterschied besteht darin, dass die Zwischenablage fast immer als einmalige Antwort auf eine bestimmte Aktion durch den Benutzer verwendet wird – z. b. Wenn Sie in einem Menü auf **Einfügen** klicken. Obwohl DDE auch von einem Benutzer initiiert werden kann, wird es in der Regel ohne weitere Beteiligung des Benutzers fortgesetzt.

Die dynamischer Datenaustausch Management Library (Ddeml) stellt eine Schnittstelle bereit, die das Hinzufügen von DDE-Funktionen zu einer Anwendung vereinfacht. Anstatt DDE-Nachrichten direkt zu senden, zu veröffentlichen und zu verarbeiten, verwendet eine Anwendung die von der Ddeml bereitgestellten Funktionen zum Verwalten von DDE-Konversationen. Eine DDE-Konversation ist die Interaktion zwischen Client-und Server Anwendungen. Die Ddeml bietet auch eine Möglichkeit zum Verwalten der Zeichen folgen und Daten, die von DDE-Anwendungen gemeinsam genutzt werden. Anstatt Atome und Zeiger auf freigegebene Speicher Objekte zu verwenden, erstellen und verarbeiten DDE-Anwendungen Zeichen folgen Handles, die Zeichen folgen und Daten Handles identifizieren, mit denen DDE-Objekte identifiziert werden. Die Ddeml stellt eine Funktion ([**DDENameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice)) bereit, die es einer Serveranwendung ermöglicht, die von ihr unterstützten Dienstnamen zu registrieren. Die Dienstnamen werden dann an andere Anwendungen im System übertragen, die die Namen zum Herstellen einer Verbindung mit dem Server verwenden. Die Ddeml gewährleistet außerdem die Kompatibilität zwischen DDE-Anwendungen, da Sie das DDE-Protokoll konsistent implementieren müssen.

Vorhandene Anwendungen, die das Nachrichten basierte DDE-Protokoll verwenden, sind vollständig kompatibel mit denen, die die Ddeml verwenden; Das heißt, eine Anwendung, die Nachrichten basiertes DDE verwendet, kann Konversationen einrichten und Transaktionen mit Anwendungen ausführen, die die Ddeml verwenden. Anstatt DDE-Nachrichten in der neuen Anwendung zu verwenden, nutzen Sie die Ddeml und die vielen Verbesserungen, die Sie bietet.

Um die Ddeml zu verwenden, müssen Sie die Ddeml einschließen. H-Header Datei in ihren Quelldateien, Verknüpfung mit der user32. LIB-Datei, und stellen Sie sicher, dass sich die DDEML.DLL Datei im Systempfad befindet.

Wenn eine Ddeml-Funktion fehlschlägt, kann eine Anwendung die [**ddegetlasterror**](/windows/desktop/api/Ddeml/nf-ddeml-ddegetlasterror) -Funktion aufrufen, um die Ursache des Fehlers zu ermitteln. **DDE GetLastError** gibt einen Fehlerwert zurück, der die Ursache des letzten Fehlers angibt.

 

 




