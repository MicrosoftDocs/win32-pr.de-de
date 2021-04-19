---
description: Das Anforderungs Objekt wird mit com cokreateinstance erstellt und macht eine Schnittstelle (itrequest) verfügbar.
ms.assetid: 1e4c71ce-6846-4e64-9346-455ed82aa458
title: Request-Objekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c51e81cae01f2624ba863b304c0a5f732b221199
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356151"
---
# <a name="request-object"></a><span data-ttu-id="79102-103">Request-Objekt</span><span class="sxs-lookup"><span data-stu-id="79102-103">Request Object</span></span>

<span data-ttu-id="79102-104">Das Anforderungs Objekt wird mit com **cokreateinstance** erstellt und macht eine Schnittstelle ( [**itrequest**](/windows/desktop/api/tapi3if/nn-tapi3if-itrequest)) verfügbar.</span><span class="sxs-lookup"><span data-stu-id="79102-104">The Request Object is created using COM **CoCreateInstance** and exposes one interface, [**ITRequest**](/windows/desktop/api/tapi3if/nn-tapi3if-itrequest).</span></span> <span data-ttu-id="79102-105">Diese Schnittstelle macht die [**MakeCall**](/windows/desktop/api/tapi3if/nf-tapi3if-itrequest-makecall) -Methode verfügbar, die es einer TAPI 3-Anwendung ermöglicht, die unterstützte Telefonie zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="79102-105">This interface exposes the [**MakeCall**](/windows/desktop/api/tapi3if/nf-tapi3if-itrequest-makecall) method, which allows a TAPI 3 application to use Assisted Telephony.</span></span> <span data-ttu-id="79102-106">Die unterstützte Telefonie bietet telefoniefähigen Anwendungen einen einfachen Mechanismus für Telefonanrufe, ohne dass der Entwickler in Telefonieinformationen vollständig geschult werden muss.</span><span class="sxs-lookup"><span data-stu-id="79102-106">Assisted Telephony provides telephony-enabled applications with a simple mechanism for making phone calls without requiring the developer to become fully literate in telephony.</span></span>

<span data-ttu-id="79102-107">Beispielsweise kann eine Tabellenkalkulationsanwendung mithilfe der unterstützten telefonieschaltfläche eine Schaltfläche zum Abrufen hinzufügen, ohne dass die ausführlicheren Steuerelemente in einer vollständigen TAPI-Anwendung implementiert</span><span class="sxs-lookup"><span data-stu-id="79102-107">For example, a spreadsheet application can add a "Make Call" button using Assisted Telephony without implementing the more elaborate controls available in a full TAPI application.</span></span>

<span data-ttu-id="79102-108">Weitere Informationen finden Sie in der [Übersicht über die unterstützte Telefonie](assisted-telephony-overview.md) .</span><span class="sxs-lookup"><span data-stu-id="79102-108">See the [Assisted Telephony Overview](assisted-telephony-overview.md) for additional information.</span></span>

 

 



