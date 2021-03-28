---
description: Damit Ihre Anwendung mit dem Synchronisierungs-Manager zusammenarbeiten kann, müssen Sie ein Component Object Model (com)-Objekt implementieren, um Synchronisierungs Benachrichtigungen zu verarbeiten, die Sie von syncmgr erhalten.
title: Verwenden des Synchronisierungs-Managers aus einem Programm
ms.topic: article
ms.date: 05/31/2018
ms.assetid: bf18d493-0fe7-46e7-9686-f7ee75b3039b
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 9bd5abdc382c82c6c1aafcda3a967337384dc807
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530176"
---
# <a name="using-synchronization-manager-from-a-program"></a>Verwenden des Synchronisierungs-Managers aus einem Programm

Damit Ihre Anwendung mit dem Synchronisierungs-Manager zusammenarbeiten kann, müssen Sie ein Component Object Model (com)-Objekt implementieren, um Synchronisierungs Benachrichtigungen zu verarbeiten, die Sie von syncmgr erhalten. Der Handler Ihrer Anwendung führt die Synchronisierung für die Elemente aus, die Sie verarbeiten. In Ihrem Handler enthalten ist, müssen Sie die [**isyncmgrsync**](/windows/desktop/api/Mobsync/nn-mobsync-isyncmgrsynchronize) -Schnittstelle implementieren. Außerdem müssen Sie ein Enumeratorobjekt und [**isyncmgrenumitems**](/windows/desktop/api/mobsync/nn-mobsync-isyncmgrenumitems) für alle separaten Elemente bereitstellen, die Ihre Anwendung synchronisieren kann.

Syncmgr implementiert [**isyncmgrsynchronizecallback**](/windows/desktop/api/mobsync/nn-mobsync-isyncmgrsynchronizecallback) und [**isyncmgrsynchronizone voke**](/windows/desktop/api/Mobsync/nn-mobsync-isyncmgrsynchronizeinvoke).

Die syncmgr ruft Methoden in Ihrer [**isyncmgrsync**](/windows/desktop/api/Mobsync/nn-mobsync-isyncmgrsynchronize) -Funktion auf, um Informationen zu den Elementen, die von der Anwendung verarbeitet werden, und Informationen zu dem Handler zu erhalten, den Sie für die Synchronisierung dieser Elemente bereitstellen.

Zur Laufzeit führt der Synchronisierungs Vorgang die folgenden Schritte aus.

1.  Syncmgr benachrichtigt Ihre Anwendung, dass es Zeit für die Synchronisierung für eines der Elemente ist, die Ihre Anwendung verarbeitet, indem Sie die [**isyncmgrsync:: Initialize**](/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronize-initialize) -Methode aufrufen.
2.  Syncmgr ruft [**isyncmgrsync:: enumsyncmgritems**](/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronize-enumsyncmgritems) auf, um die [**isyncmgrenumitems**](/windows/desktop/api/mobsync/nn-mobsync-isyncmgrenumitems) -Schnittstelle für die Elemente zu erhalten, die von Ihrer Anwendung verarbeitet werden.
3.  Syncmgr ruft [**isyncmgrsync:: setprogresscallback**](/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronize-setprogresscallback) auf, um dem Handler den Schnittstellen Zeiger für die [**isyncmgrsynchronizecallback**](/windows/desktop/api/mobsync/nn-mobsync-isyncmgrsynchronizecallback) -Schnittstelle bereitzustellen. Der Handler verwendet diese Schnittstelle, um während der Synchronisierung einen Rückruf an syncmgr durchzusetzen.
4.  Syncmgr ruft dann Ihre [**isyncmgrsync::P Analyse forsync**](/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronize-prepareforsync) -Methode auf, um dem Handler zu gestatten, alle Benutzeroberflächen Elemente anzuzeigen, die vor Beginn der Synchronisierung erforderlich sind. Eine e-Mail-Anwendung kann z. b. ein Benutzer Anmelde Dialogfeld anzeigen.
5.  Der Handler ruft [**isyncmgrsynchronizecallback:: enablemodeless**](/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronizecallback-enablemodeless) vor und nach dem Anzeigen von Elementen der Benutzeroberfläche auf. Der Handler ruft [**isyncmgrsynchronizecallback**](/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronizecallback-prepareforsynccompleted) auf, wenn Sie fertig sind:P.
6.  Syncmgr ruft Ihre [**isyncmgrsync::**](/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronize-synchronize) Sync-Methode auf, um die Synchronisierung zu starten.

Während des Synchronisierungs Vorgangs ruft syncmgr weiterhin Methoden in Ihrer [**isyncmgrsync**](/windows/desktop/api/Mobsync/nn-mobsync-isyncmgrsynchronize) -Schnittstelle auf. Sie kann Ihre Handlerfehler, den Fortschritt und Benachrichtigungen senden. Sie kann auch die Elemente auflisten, die von der Anwendung verarbeitet werden, oder Ihre Anwendung können Eigenschaften für die Elemente anzeigen.

Der Handler ruft Methoden in [**isyncmgrsynchronizecallback**](/windows/desktop/api/mobsync/nn-mobsync-isyncmgrsynchronizecallback) auf, um zu bestimmen, ob ein Element übersprungen werden soll, um Fehler zu protokollieren und während des Synchronisierungs Vorgangs Statusinformationen bereitzustellen.

Weitere Informationen finden Sie auf den entsprechenden Referenzseiten für die beteiligten Schnittstellen.

Wenn die Synchronisierung abgeschlossen ist, ruft der Handler [**isyncmgrsynchronizecallback:: synchronizeabgeschlossene**](/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronizecallback-synchronizecompleted)auf.

 

 



