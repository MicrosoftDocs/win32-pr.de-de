---
description: TAPI weist Sitzungs Bezeichner zu, die für jede Sitzung und Anwendung eindeutig sind.
ms.assetid: 711a9bc6-ffc6-499b-8653-ba230028c146
title: Sitzungsbezeichner
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e135beb439d1c5fb2fdd46d4986cd35dc5ae49b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104393802"
---
# <a name="session-identifier"></a><span data-ttu-id="50586-103">Sitzungsbezeichner</span><span class="sxs-lookup"><span data-stu-id="50586-103">Session Identifier</span></span>

<span data-ttu-id="50586-104">TAPI weist Sitzungs Bezeichner zu, die für jede Sitzung und Anwendung eindeutig sind.</span><span class="sxs-lookup"><span data-stu-id="50586-104">TAPI assigns session identifiers that are unique for each session and application.</span></span> <span data-ttu-id="50586-105">Eine Anwendung verwendet eine Sitzungs-ID, um mit TAPI über eine bestimmte Sitzung zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="50586-105">An application uses a session identifier to communicate with TAPI concerning a specific session.</span></span> <span data-ttu-id="50586-106">Eine Anwendung erhält in der Regel einen Bezeichner, indem eine neue Kommunikationssitzung erstellt wird oder wenn TAPI eine Sitzung anbietet.</span><span class="sxs-lookup"><span data-stu-id="50586-106">An application typically obtains an identifier either by creating a new communications session or when TAPI offers a session.</span></span>

<span data-ttu-id="50586-107">Ein Sitzungs Bezeichner kann nicht verwendet werden, um Informationen an eine andere Anwendung zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="50586-107">A session identifier cannot be used to pass information to another application.</span></span> <span data-ttu-id="50586-108">Verwenden Sie zu diesem Zweck die [Telefonnummer](call-id-ovr.md), die von einem Dienstanbieter zugewiesen werden kann.</span><span class="sxs-lookup"><span data-stu-id="50586-108">For this purpose, use the [Call ID](call-id-ovr.md), which may be assigned by a service provider.</span></span>

<span data-ttu-id="50586-109">Weitere Informationen zu Vorgängen, die Sitzungen erstellen und eine Sitzungs-ID zurückgeben, finden Sie unter [Initiieren einer Sitzung](initiate-a-session-ovr.md) .</span><span class="sxs-lookup"><span data-stu-id="50586-109">See [Initiate a session](initiate-a-session-ovr.md) for information on operations that create sessions and return a session identifier.</span></span> <span data-ttu-id="50586-110">Weitere Informationen zu Vorgängen, die Sitzungs Bezeichner von TAPI abrufen, finden [Sie unter reagieren auf eine Sitzung](respond-to-session-initiated-elsewhere-ovr.md) .</span><span class="sxs-lookup"><span data-stu-id="50586-110">See [Respond to session initiated elsewhere](respond-to-session-initiated-elsewhere-ovr.md) for operations that acquire session identifiers from TAPI.</span></span> <span data-ttu-id="50586-111">Weitere Informationen zum Freigeben von Sitzungs Ressourcen finden Sie unter [Beenden einer Sitzung](terminate-a-session-ovr.md) .</span><span class="sxs-lookup"><span data-stu-id="50586-111">See [Terminate a Session](terminate-a-session-ovr.md) for information on releasing session resources.</span></span>

<span data-ttu-id="50586-112">Alle Dienstanbieter müssen eine bestimmte Form der Sitzungs Identifikation unterstützen.</span><span class="sxs-lookup"><span data-stu-id="50586-112">All service providers must support some form of session identification.</span></span>

<span data-ttu-id="50586-113">**TAPI 2. x:** Der primäre Bezeichner einer Kommunikationssitzung ist das-Anweisungs Handle.</span><span class="sxs-lookup"><span data-stu-id="50586-113">**TAPI 2.x:** The primary identifier of a communications session is the call handle.</span></span>

<span data-ttu-id="50586-114">**TAPI 3. x:** Eine Sitzung wird durch ein [Aufruf Objekt](call-object.md) dargestellt, und der primäre Bezeichner ist ein Zeiger auf die [**itcallinfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="50586-114">**TAPI 3.x:** A session is represented by a [Call Object](call-object.md) and the primary identifier is a pointer to the [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo) interface.</span></span>

 

 



