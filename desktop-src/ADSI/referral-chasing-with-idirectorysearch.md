---
title: Verweis Verfolgung mit idirector ysearch
description: Ein Verweis ist der Mechanismus, der von einem Verzeichnisserver verwendet wird, um einen Client an einen anderen Server weiterzuleiten, wenn er keine ausreichenden Daten über das von einer Abfrage angeforderte Objekt enthält.
ms.assetid: ef97eafd-5227-4dd7-9f8a-6b4591261f79
ms.tgt_platform: multiple
keywords:
- Verweis Verfolgung mit idirector ysearch ADSI
- ADSI, Search, idirector ysearch, andere Suchoptionen, Verweis Verfolgung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fae76139dc1a68c9345cd7a7b3bb894a50a2d7b
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "103949113"
---
# <a name="referral-chasing-with-idirectorysearch"></a><span data-ttu-id="a52b1-105">Verweis Verfolgung mit idirector ysearch</span><span class="sxs-lookup"><span data-stu-id="a52b1-105">Referral Chasing with IDirectorySearch</span></span>

<span data-ttu-id="a52b1-106">Ein Verweis ist der Mechanismus, der von einem Verzeichnisserver verwendet wird, um einen Client an einen anderen Server weiterzuleiten, wenn er keine ausreichenden Daten über das von einer Abfrage angeforderte Objekt enthält.</span><span class="sxs-lookup"><span data-stu-id="a52b1-106">A referral is the mechanism that a directory server uses to direct a client to another server when it does not contain sufficient data about the object requested by a query.</span></span>

<span data-ttu-id="a52b1-107">Bei einer Suche in einer Ebene oder einer Unterstruktur werden Verweise nur für bekannte, unmittelbar untergeordnete Domänen-, Schema-oder Konfigurations Container zurückgegeben. Dies sind untergeordnete Domänen, die direkte Nachfolger sind.</span><span class="sxs-lookup"><span data-stu-id="a52b1-107">In a one-level or subtree search, referrals are returned for known, immediately subordinate domain, schema, or configuration containers only; that is, child domains that are direct descendants.</span></span> <span data-ttu-id="a52b1-108">Weitere Informationen finden Sie unter [Suchbereich](/windows/desktop/AD/search-scope).</span><span class="sxs-lookup"><span data-stu-id="a52b1-108">For more information, see [Search Scope](/windows/desktop/AD/search-scope).</span></span>

<span data-ttu-id="a52b1-109">In einem Verzeichnis sind nicht alle Daten auf einem einzelnen Server verfügbar, sondern auf mehrere verschiedene Server über das Netzwerk verteilt.</span><span class="sxs-lookup"><span data-stu-id="a52b1-109">In a directory, not all data is available on a single server, rather, it is distributed over several different servers across the network.</span></span> <span data-ttu-id="a52b1-110">Wenn die Server die Daten gemeinsam nutzen, die andere Server bereitstellen können, können Sie Verweise auf einen Client bereitstellen, wenn eine angeforderte Abfrage nicht auf dem ursprünglichen Server aufgelöst werden kann.</span><span class="sxs-lookup"><span data-stu-id="a52b1-110">If the servers share the data that other servers can provide, they can provide referrals to a client when a requested query cannot be resolved on the originating server.</span></span> <span data-ttu-id="a52b1-111">Wenn ein Client z. b. Server a auffordert, ein Benutzerobjekt (u) abzufragen, kann eine die Suche auf Server B fortsetzen, wenn sich U nicht in einer befindet, aber als auf B festgelegt ist. Der Client hat die Möglichkeit, den Verweis nachzuverfolgen.</span><span class="sxs-lookup"><span data-stu-id="a52b1-111">For example, when a client asks Server A to query a user object (U), then A can suggest that the client continue the search on Server B if U does not reside on A, but is identified to be on B. The client has the choice to pursue the referral or not.</span></span> <span data-ttu-id="a52b1-112">Verweise geben an, dass der Client über vorherige Kenntnisse der Funktion der einzelnen Server verfügen muss, aber der Client muss den Typ der Verweise angeben, die ein Server ausführen sollte.</span><span class="sxs-lookup"><span data-stu-id="a52b1-112">Referrals free the client from having to possess previous knowledge of the capability of each server, but the client must specify the type of referrals a server should perform.</span></span>

<span data-ttu-id="a52b1-113">Legen Sie zum Aktivieren oder Deaktivieren der Verweis Verfolgung eine Suchoption für **ADS \_ searchpref \_ Chase \_ Referrals** mit einem **\_ ganzzahligen adstype** -Wert fest, der einen der ADS-enumerationsenumerationswerte für Enumerationswerte im ADS-enumerationsarray enthält, das an die [**IDirectorySearch:: setsearchpreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) -Methode weitergegeben wird. [**\_ \_ \_**](/windows/win32/api/iads/ne-iads-ads_chase_referrals_enum) [**\_ \_**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info)</span><span class="sxs-lookup"><span data-stu-id="a52b1-113">To enable or disable referral chasing, set an **ADS\_SEARCHPREF\_CHASE\_REFERRALS** search option with an **ADSTYPE\_INTEGER** value that contains one of the [**ADS\_CHASE\_REFERRALS\_ENUM**](/windows/win32/api/iads/ne-iads-ads_chase_referrals_enum) enumeration values in the [**ADS\_SEARCHPREF\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) array passed to the [**IDirectorySearch::SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) method.</span></span>

<span data-ttu-id="a52b1-114">Im folgenden Codebeispiel wird gezeigt, wie Sie Chase-Verweise aktivieren.</span><span class="sxs-lookup"><span data-stu-id="a52b1-114">The following code example shows how to enable chase referrals.</span></span>


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_CHASE_REFERRALS;
SearchPref.vValue.dwType = ADSTYPE_INTEGER;
SearchPref.vValue.Integer = ADS_CHASE_REFERRALS_ALWAYS;
```



<span data-ttu-id="a52b1-115">Weitere Informationen zu verweisen in Active Directory finden Sie unter [Verweise](/windows/desktop/AD/referrals).</span><span class="sxs-lookup"><span data-stu-id="a52b1-115">For more information about referrals in Active Directory, see [Referrals](/windows/desktop/AD/referrals).</span></span>

 

 