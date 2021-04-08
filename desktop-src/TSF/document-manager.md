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
# <a name="document-manager"></a><span data-ttu-id="20a29-108">Dokument-Manager</span><span class="sxs-lookup"><span data-stu-id="20a29-108">Document Manager</span></span>

## <a name="applications"></a><span data-ttu-id="20a29-109">Anwendungen</span><span class="sxs-lookup"><span data-stu-id="20a29-109">Applications</span></span>

<span data-ttu-id="20a29-110">Zum Erstellen eines Dokument-Manager-Objekts wird von einer Anwendung [ITfThreadMgr:: kreatedocumentmgr](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-createdocumentmgr)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="20a29-110">To create a document manager object an application calls [ITfThreadMgr::CreateDocumentMgr](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-createdocumentmgr).</span></span> <span data-ttu-id="20a29-111">Die Anwendung erstellt ein separates Dokument-Manager-Objekt für jedes einzelne Dokument, das die Anwendung verwaltet.</span><span class="sxs-lookup"><span data-stu-id="20a29-111">The application creates a separate document manager object for each individual document that the application maintains.</span></span> <span data-ttu-id="20a29-112">Die Anwendung verwendet den Dokument-Manager zum Erstellen von Bearbeitungs Kontexten, zum Hinzufügen eines Kontexts zum Kontext Stapel und zum Entfernen eines Kontexts aus dem Kontext Stapel.</span><span class="sxs-lookup"><span data-stu-id="20a29-112">The application uses the document manager to create edit contexts, add a context to the context stack and remove a context from the context stack.</span></span>

## <a name="text-services"></a><span data-ttu-id="20a29-113">Text Dienste</span><span class="sxs-lookup"><span data-stu-id="20a29-113">Text Services</span></span>

<span data-ttu-id="20a29-114">Ein Text Dienst erstellt nie ein Dokument-Manager-Objekt.</span><span class="sxs-lookup"><span data-stu-id="20a29-114">A text service never creates a document manager object.</span></span> <span data-ttu-id="20a29-115">Stattdessen ruft der Text Dienst das aktuell aktive Dokument-Manager-Objekt durch Aufrufen von [ITfThreadMgr:: GetFocus](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-getfocus)ab.</span><span class="sxs-lookup"><span data-stu-id="20a29-115">Instead, the text service obtains the currently active document manager object by calling [ITfThreadMgr::GetFocus](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-getfocus).</span></span> <span data-ttu-id="20a29-116">Ein Text Dienst verwendet den Dokument-Manager zum Abrufen des Kontexts am Anfang des Stapels.</span><span class="sxs-lookup"><span data-stu-id="20a29-116">A text service uses the document manager to obtain the context at the top of the stack.</span></span>

<span data-ttu-id="20a29-117">Ein Text Dienst kann auch den Dokument-Manager verwenden, um einen eigenen Kontext zu erstellen und ihn aus dem Kontext Stapel hinzuzufügen und zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="20a29-117">A text service can also use the document manager to create its own context and add and remove it from the context stack.</span></span> <span data-ttu-id="20a29-118">Dies geschieht normalerweise, wenn der Text Dienst eine modale Benutzeroberfläche anzeigen muss, z. b. Wenn eine Liste von Wörtern angezeigt wird, um dem Benutzer die Auswahl eines Worts zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="20a29-118">This is normally done when the text service must display some modal user interface, such as when a list of words is displayed to enable the user to select a word.</span></span> <span data-ttu-id="20a29-119">Wenn die Liste angezeigt wird, platziert der Text Dienst seinen eigenen Kontext auf dem Stapel.</span><span class="sxs-lookup"><span data-stu-id="20a29-119">When the list is displayed, the text service places its own context on the stack.</span></span> <span data-ttu-id="20a29-120">Wenn die Wort Liste verworfen wird, entfernt der Text Dienst seinen Kontext aus dem Stapel.</span><span class="sxs-lookup"><span data-stu-id="20a29-120">When the word list is dismissed, the text service removes its context from the stack.</span></span>

## <a name="related-topics"></a><span data-ttu-id="20a29-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="20a29-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="20a29-122">ITfDocumentMgr</span><span class="sxs-lookup"><span data-stu-id="20a29-122">ITfDocumentMgr</span></span>](/windows/desktop/api/Msctf/nn-msctf-itfdocumentmgr)
</dt> <dt>

[<span data-ttu-id="20a29-123">ITfThreadMgr:: kreatedocumentmgr</span><span class="sxs-lookup"><span data-stu-id="20a29-123">ITfThreadMgr::CreateDocumentMgr</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-createdocumentmgr)
</dt> <dt>

[<span data-ttu-id="20a29-124">ITfThreadMgr:: GetFocus</span><span class="sxs-lookup"><span data-stu-id="20a29-124">ITfThreadMgr::GetFocus</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-getfocus)
</dt> </dl>

 

 




