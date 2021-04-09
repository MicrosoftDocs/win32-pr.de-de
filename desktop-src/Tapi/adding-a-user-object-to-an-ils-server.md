---
description: Das folgende Code Fragment veranschaulicht das Veröffentlichen eines Benutzer Objekts in einem ILS-Server. Nachdem ein Benutzerobjekt veröffentlicht wurde, können Remote Parteien das User-Objekt verwenden, um Aufrufe an den angegebenen Benutzer vorzunehmen.
ms.assetid: 8b68886c-0df5-4005-bcd5-1a18336f5192
title: Hinzufügen eines Benutzer Objekts zu einem ILS-Server
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f85b15dcdbca47187cf4155dfbf7535d06718c19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750784"
---
# <a name="adding-a-user-object-to-an-ils-server"></a><span data-ttu-id="3cdc4-104">Hinzufügen eines Benutzer Objekts zu einem ILS-Server</span><span class="sxs-lookup"><span data-stu-id="3cdc4-104">Adding a User Object to an ILS Server</span></span>

<span data-ttu-id="3cdc4-105">\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3cdc4-105">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="3cdc4-106">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="3cdc4-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="3cdc4-107">Das folgende Code Fragment veranschaulicht das Veröffentlichen eines Benutzer Objekts in einem ILS-Server.</span><span class="sxs-lookup"><span data-stu-id="3cdc4-107">The following code fragment illustrates publishing a user object in an ILS server.</span></span> <span data-ttu-id="3cdc4-108">Nachdem ein Benutzerobjekt veröffentlicht wurde, können Remote Parteien das User-Objekt verwenden, um Aufrufe an den angegebenen Benutzer vorzunehmen.</span><span class="sxs-lookup"><span data-stu-id="3cdc4-108">After a user object is published, remote parties can use the user object to make calls to the specified user.</span></span>

<span data-ttu-id="3cdc4-109">Dieses Fragment geht davon aus, dass bereits [eine Verbindung mit einem ILS-Server](connecting-to-an-ils-server.md) hergestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="3cdc4-109">This fragment assumes that [connecting to an ILS server](connecting-to-an-ils-server.md) has already been performed.</span></span>


```C++
hr = pDirectory->AddDirectoryObject(pDirectoryObject);
```



## <a name="related-topics"></a><span data-ttu-id="3cdc4-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3cdc4-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3cdc4-111">**Itdirectory**</span><span class="sxs-lookup"><span data-stu-id="3cdc4-111">**ITDirectory**</span></span>](/windows/desktop/api/Rend/nn-rend-itdirectory)
</dt> <dt>

[<span data-ttu-id="3cdc4-112">**Itdirectoryobject**</span><span class="sxs-lookup"><span data-stu-id="3cdc4-112">**ITDirectoryObject**</span></span>](/windows/desktop/api/Rend/nn-rend-itdirectoryobject)
</dt> <dt>

[<span data-ttu-id="3cdc4-113">**Itdirecteryobjectuser**</span><span class="sxs-lookup"><span data-stu-id="3cdc4-113">**ITDirectoryObjectUser**</span></span>](/windows/desktop/api/Rend/nn-rend-itdirectoryobjectuser)
</dt> </dl>

 

 



