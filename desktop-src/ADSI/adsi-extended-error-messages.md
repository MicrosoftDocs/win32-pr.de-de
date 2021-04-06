---
title: Erweiterte ADSI-Fehlermeldungen
description: Dieses Thema enthält eine Liste der Themen, in denen erläutert wird, wie Sie mit den von IADs, IADsContainer, IDirectoryObject und IDirectorySearch zurückgegebenen ADSI-Fehlermeldungen arbeiten.
ms.assetid: cfec86cb-fe90-4e2b-8c9d-06e175253fa4
ms.tgt_platform: multiple
keywords:
- Erweiterte ADSI-Fehlermeldungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab374f18892c0ff336ef588dce477db60405ab19
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036329"
---
# <a name="adsi-extended-error-messages"></a><span data-ttu-id="5cf27-104">Erweiterte ADSI-Fehlermeldungen</span><span class="sxs-lookup"><span data-stu-id="5cf27-104">ADSI Extended Error Messages</span></span>

<span data-ttu-id="5cf27-105">Abgesehen von den **HRESULT** -Werten werden von mehreren ADSI-Systemanbietern (größtenteils LDAP) zusätzliche Fehler Daten für Vorgänge zurückgegeben, die von den folgenden Schnittstellen ausgeführt werden:</span><span class="sxs-lookup"><span data-stu-id="5cf27-105">Apart from the **HRESULT** values, several ADSI system providers (mostly LDAP) return additional error data for operations performed by the following interfaces:</span></span>

-   [<span data-ttu-id="5cf27-106">**IADs**</span><span class="sxs-lookup"><span data-stu-id="5cf27-106">**IADs**</span></span>](/windows/desktop/api/Iads/nn-iads-iads)
-   [<span data-ttu-id="5cf27-107">**IADsContainer**</span><span class="sxs-lookup"><span data-stu-id="5cf27-107">**IADsContainer**</span></span>](/windows/desktop/api/Iads/nn-iads-iadscontainer)
-   [<span data-ttu-id="5cf27-108">**IDirectoryObject**</span><span class="sxs-lookup"><span data-stu-id="5cf27-108">**IDirectoryObject**</span></span>](/windows/desktop/api/Iads/nn-iads-idirectoryobject)
-   [<span data-ttu-id="5cf27-109">**IDirectorySearch**</span><span class="sxs-lookup"><span data-stu-id="5cf27-109">**IDirectorySearch**</span></span>](/windows/desktop/api/Iads/nn-iads-idirectorysearch)

<span data-ttu-id="5cf27-110">Ein Teil dieser erweiterten Fehler Daten ist die Zeichenfolge, die vom Server als Teil des Nachrichten Ergebnisses gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="5cf27-110">A part of such extended error data is the string sent by the server as a part of the message result.</span></span>

<span data-ttu-id="5cf27-111">Rufen Sie [**adsgetlasterror**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetlasterror) auf, um solche erweiterten Fehlermeldungen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="5cf27-111">Call [**ADsGetLastError**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetlasterror) to retrieve such extended error messages.</span></span> <span data-ttu-id="5cf27-112">Der erste Parameter dieser Funktion, *lperror*, ist ein **DWORD** -Wert.</span><span class="sxs-lookup"><span data-stu-id="5cf27-112">The first parameter of this function, *lpError*, is a **DWORD** value.</span></span> <span data-ttu-id="5cf27-113">Bei einem Active Directory Server versucht ADSI, eine LDAP-Fehlermeldung einem entsprechenden Win32-Fehlercode zuzuordnen, und weist den Win32-Fehler Codewert *lperror* zu.</span><span class="sxs-lookup"><span data-stu-id="5cf27-113">For an Active Directory server, ADSI attempts to map an LDAP error message to an appropriate Win32 error code and assigns the Win32 error code value to *lpError*.</span></span> <span data-ttu-id="5cf27-114">Wenn die Zuordnung nicht aufgelöst werden kann, weist ADSI *lperror* **fehlerhafte \_ \_ Daten** zu, wie es bei jedem anderen Verzeichnisserver der Fall ist.</span><span class="sxs-lookup"><span data-stu-id="5cf27-114">Failing to resolve the mapping, ADSI assigns **ERROR\_INVALID\_DATA** to *lpError*, as it does for any other directory server.</span></span> <span data-ttu-id="5cf27-115">In allen Fällen leitet ADSI die Zeichenfolge der Fehlerbeschreibung über *lperrorbuf*, den zweiten Parameter der **adsgetlasterror** -Funktion, vom Server an den Client weiter.</span><span class="sxs-lookup"><span data-stu-id="5cf27-115">In all cases, ADSI faithfully relays the string of the error description from the server to the client through *lpErrorBuf*, the second parameter of the **ADsGetLastError** function.</span></span>

 

 




