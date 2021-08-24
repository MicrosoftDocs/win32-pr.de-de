---
description: Damit Ihre Anwendung mit dem Synchronisierungs-Manager arbeiten kann, müssen Sie ein COM-Objekt (Component Object Model) implementieren, um Synchronisierungsbenachrichtigungen zu verarbeiten, die Sie von SyncMgr erhalten.
title: Verwenden des Synchronisierungs-Managers aus einem Programm
ms.topic: article
ms.date: 05/31/2018
ms.assetid: bf18d493-0fe7-46e7-9686-f7ee75b3039b
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 11e959399624d30e1e6d7ce87fb8bb247de7c9c420ef9b2427c7b9bdeb00e7f4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119709380"
---
# <a name="using-synchronization-manager-from-a-program"></a>Verwenden des Synchronisierungs-Managers aus einem Programm

Damit Ihre Anwendung mit dem Synchronisierungs-Manager arbeiten kann, müssen Sie ein COM-Objekt (Component Object Model) implementieren, um Synchronisierungsbenachrichtigungen zu verarbeiten, die Sie von SyncMgr erhalten. Der Handler Ihrer Anwendung führt die Synchronisierung für die elemente aus, die Sie behandeln. In Ihrem Handler enthalten, müssen Sie die [**ISyncMgrSynchronize-Schnittstelle**](/windows/desktop/api/Mobsync/nn-mobsync-isyncmgrsynchronize) implementieren. Außerdem müssen Sie ein Enumeratorobjekt und [**ISyncMgrEnumItems**](/windows/desktop/api/mobsync/nn-mobsync-isyncmgrenumitems) für alle separaten Elemente bereitstellen, die ihre Anwendung synchronisieren kann.

SyncMgr implementiert [**ISyncMgrSynchronizeCallback**](/windows/desktop/api/mobsync/nn-mobsync-isyncmgrsynchronizecallback) und [**ISyncMgrSynchronizeInvoke.**](/windows/desktop/api/Mobsync/nn-mobsync-isyncmgrsynchronizeinvoke)

SyncMgr ruft Methoden in [**ISyncMgrSynchronize**](/windows/desktop/api/Mobsync/nn-mobsync-isyncmgrsynchronize) auf, um Informationen zu den Elementen abzurufen, die ihre Anwendung verarbeitet, sowie Informationen zu dem Handler, den Sie zum Synchronisieren dieser Elemente bereitstellen.

Zur Laufzeit folgt der Synchronisierungsprozess diesen Schritten.

1.  SyncMgr benachrichtigt Ihre Anwendung, dass es an der Zeit ist, die Synchronisierung für eines der Elemente durchzuführen, die ihre Anwendung verarbeitet, indem die [**ISyncMgrSynchronize::Initialize-Methode**](/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronize-initialize) aufgerufen wird.
2.  SyncMgr ruft [**ISyncMgrSynchronize::EnumSyncMgrItems**](/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronize-enumsyncmgritems) auf, um die [**ISyncMgrEnumItems-Schnittstelle**](/windows/desktop/api/mobsync/nn-mobsync-isyncmgrenumitems) für die elemente abzurufen, die von Ihrer Anwendung verarbeitet werden.
3.  SyncMgr ruft [**ISyncMgrSynchronize::SetProgressCallback**](/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronize-setprogresscallback) auf, um Ihrem Handler den Schnittstellenzeiger für die [**ISyncMgrSynchronizeCallback-Schnittstelle**](/windows/desktop/api/mobsync/nn-mobsync-isyncmgrsynchronizecallback) bereitzustellen. Ihr Handler verwendet diese Schnittstelle, um während der Synchronisierung einen Rückruf an SyncMgr durchzuführen.
4.  SyncMgr ruft dann die [**ISyncMgrSynchronize::P repareForSync-Methode**](/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronize-prepareforsync) auf, um dem Handler die Möglichkeit zu geben, alle Benutzeroberflächenelemente anzuzeigen, die vor Beginn der Synchronisierung erforderlich sind. Beispielsweise kann eine E-Mail-Anwendung ein Benutzeranmeldungsdialogfeld anzeigen.
5.  Ihr Handler ruft [**ISyncMgrSynchronizeCallback::EnableModeless**](/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronizecallback-enablemodeless) vor und nach dem Anzeigen von Benutzeroberflächenelementen auf. Der Handler ruft [**ISyncMgrSynchronizeCallback::P repareForSyncCompleted**](/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronizecallback-prepareforsynccompleted) auf, wenn Sie fertig sind.
6.  SyncMgr ruft Ihre [**ISyncMgrSynchronize::Synchronize-Methode**](/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronize-synchronize) auf, um die Synchronisierung zu starten.

Während des Synchronisierungsprozesses ruft SyncMgr weiterhin Methoden in Ihrer [**ISyncMgrSynchronize-Schnittstelle**](/windows/desktop/api/Mobsync/nn-mobsync-isyncmgrsynchronize) auf. Sie kann Handlerfehler, Status und Benachrichtigungen senden. Sie kann auch die Elemente aufzählen, die von Ihrer Anwendung verarbeitet werden, oder es der Anwendung ermöglichen, Eigenschaften für die Elemente anzuzeigen.

Ihr Handler ruft Methoden in [**ISyncMgrSynchronizeCallback**](/windows/desktop/api/mobsync/nn-mobsync-isyncmgrsynchronizecallback) auf, um zu bestimmen, ob ein Element übersprungen werden soll, um Fehler zu protokollieren und Während des Synchronisierungsprozesses Statusinformationen zu veröffentlichen.

Weitere Informationen finden Sie auf den zugehörigen Referenzseiten für die beteiligten Schnittstellen.

Wenn die Synchronisierung abgeschlossen ist, ruft Ihr Handler [**ISyncMgrSynchronizeCallback::SynchronizeCompleted auf.**](/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronizecallback-synchronizecompleted)

 

 



