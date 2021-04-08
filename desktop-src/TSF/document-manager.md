---
title: Dokument-Manager
description: Dokument-Manager
ms.assetid: e30087b6-524a-481e-845d-0348bac3830a
keywords:
- Text Services-Framework (TSF), Dokument-Manager
- TSF (Text Dienste-Framework), Dokument-Manager
- Text Dienste, Dokument-Manager
- TSF-aktivierte Anwendungen, Dokument-Manager
- Dokument-Manager
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc2182782218ad6a8aa0a70f296f639560307249
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708915"
---
# <a name="document-manager"></a>Dokument-Manager

## <a name="applications"></a>Anwendungen

Zum Erstellen eines Dokument-Manager-Objekts wird von einer Anwendung [ITfThreadMgr:: kreatedocumentmgr](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-createdocumentmgr)aufgerufen. Die Anwendung erstellt ein separates Dokument-Manager-Objekt für jedes einzelne Dokument, das die Anwendung verwaltet. Die Anwendung verwendet den Dokument-Manager zum Erstellen von Bearbeitungs Kontexten, zum Hinzufügen eines Kontexts zum Kontext Stapel und zum Entfernen eines Kontexts aus dem Kontext Stapel.

## <a name="text-services"></a>Text Dienste

Ein Text Dienst erstellt nie ein Dokument-Manager-Objekt. Stattdessen ruft der Text Dienst das aktuell aktive Dokument-Manager-Objekt durch Aufrufen von [ITfThreadMgr:: GetFocus](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-getfocus)ab. Ein Text Dienst verwendet den Dokument-Manager zum Abrufen des Kontexts am Anfang des Stapels.

Ein Text Dienst kann auch den Dokument-Manager verwenden, um einen eigenen Kontext zu erstellen und ihn aus dem Kontext Stapel hinzuzufügen und zu entfernen. Dies geschieht normalerweise, wenn der Text Dienst eine modale Benutzeroberfläche anzeigen muss, z. b. Wenn eine Liste von Wörtern angezeigt wird, um dem Benutzer die Auswahl eines Worts zu ermöglichen. Wenn die Liste angezeigt wird, platziert der Text Dienst seinen eigenen Kontext auf dem Stapel. Wenn die Wort Liste verworfen wird, entfernt der Text Dienst seinen Kontext aus dem Stapel.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ITfDocumentMgr](/windows/desktop/api/Msctf/nn-msctf-itfdocumentmgr)
</dt> <dt>

[ITfThreadMgr:: kreatedocumentmgr](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-createdocumentmgr)
</dt> <dt>

[ITfThreadMgr:: GetFocus](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-getfocus)
</dt> </dl>

 

 




