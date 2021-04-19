---
description: Die folgenden Funktionen werden mit Network DDE verwendet.
ms.assetid: 5fd61759-1792-4db0-9ad4-adf112294b9c
title: Network DDE-Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16e5ae6a38ec6324cf33b4f9c4ffc1af44473699
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373376"
---
# <a name="network-dde-functions"></a><span data-ttu-id="b9136-103">Network DDE-Funktionen</span><span class="sxs-lookup"><span data-stu-id="b9136-103">Network DDE Functions</span></span>

<span data-ttu-id="b9136-104">\[Network DDE wird nicht mehr unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b9136-104">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="b9136-105">Nddeapi.dll ist unter Windows Vista vorhanden, aber alle Funktionsaufrufe geben "ndde" \_ nicht \_ implementiert zurück.\]</span><span class="sxs-lookup"><span data-stu-id="b9136-105">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="b9136-106">Die folgenden Funktionen werden mit Network DDE verwendet.</span><span class="sxs-lookup"><span data-stu-id="b9136-106">The following functions are used with network DDE.</span></span>



| <span data-ttu-id="b9136-107">Funktion</span><span class="sxs-lookup"><span data-stu-id="b9136-107">Function</span></span>                                                   | <span data-ttu-id="b9136-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b9136-108">Description</span></span>                                                                                                           |
|------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b9136-109">**Ndaufgeterrorstring**</span><span class="sxs-lookup"><span data-stu-id="b9136-109">**NDdeGetErrorString**</span></span>](nddegeterrorstring.md)           | <span data-ttu-id="b9136-110">Konvertiert einen Fehlercode, der von einer Network DDE-Funktion zurückgegeben wird, in eine Fehler Zeichenfolge, die den zurückgegebenen Fehlercode</span><span class="sxs-lookup"><span data-stu-id="b9136-110">Converts an error code returned by a network DDE function into an error string that explains the returned error code.</span></span> |
| [<span data-ttu-id="b9136-111">**Ndde GetShareSecurity**</span><span class="sxs-lookup"><span data-stu-id="b9136-111">**NDdeGetShareSecurity**</span></span>](nddegetsharesecurity.md)       | <span data-ttu-id="b9136-112">Ruft die Sicherheits Beschreibung ab, die der DDE-Freigabe zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="b9136-112">Retrieves the security descriptor associated with the DDE share.</span></span>                                                      |
| [<span data-ttu-id="b9136-113">**Ndbegettrustedshare**</span><span class="sxs-lookup"><span data-stu-id="b9136-113">**NDdeGetTrustedShare**</span></span>](nddegettrustedshare.md)         | <span data-ttu-id="b9136-114">Ruft die einer DDE-Freigabe zugeordneten Optionen ab, die sich in der Liste der vertrauenswürdigen Freigaben des Server Benutzers befinden.</span><span class="sxs-lookup"><span data-stu-id="b9136-114">Retrieves the options associated with a DDE share that is in the server user's list of trusted shares.</span></span>                |
| [<span data-ttu-id="b9136-115">**Nddeisvalidapptopiclist**</span><span class="sxs-lookup"><span data-stu-id="b9136-115">**NDdeIsValidAppTopicList**</span></span>](nddeisvalidapptopiclist.md) | <span data-ttu-id="b9136-116">Bestimmt, ob eine Anwendung und eine Themen Zeichenfolge ("*appname* \| *TopicName*") die richtige Syntax verwendet.</span><span class="sxs-lookup"><span data-stu-id="b9136-116">Determines whether an application and topic string ("*AppName*\|*TopicName*") uses the proper syntax.</span></span>                 |
| [<span data-ttu-id="b9136-117">**Nddeisvalidsharename**</span><span class="sxs-lookup"><span data-stu-id="b9136-117">**NDdeIsValidShareName**</span></span>](nddeisvalidsharename.md)       | <span data-ttu-id="b9136-118">Bestimmt, ob ein Freigabe Name die richtige Syntax verwendet.</span><span class="sxs-lookup"><span data-stu-id="b9136-118">Determines whether a share name uses the proper syntax.</span></span>                                                               |
| [<span data-ttu-id="b9136-119">**Ndde setsharesecurity**</span><span class="sxs-lookup"><span data-stu-id="b9136-119">**NDdeSetShareSecurity**</span></span>](nddesetsharesecurity.md)       | <span data-ttu-id="b9136-120">Legt die Sicherheits Beschreibung fest, die der DDE-Freigabe zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="b9136-120">Sets the security descriptor associated with the DDE share.</span></span>                                                           |
| [<span data-ttu-id="b9136-121">**Ndabsettrustedshare**</span><span class="sxs-lookup"><span data-stu-id="b9136-121">**NDdeSetTrustedShare**</span></span>](nddesettrustedshare.md)         | <span data-ttu-id="b9136-122">Gewährt der angegebenen DDE-Freigabe den vertrauenswürdigen Status im Kontext des aktuellen Benutzers.</span><span class="sxs-lookup"><span data-stu-id="b9136-122">Grants the specified DDE share trusted status within the current user's context.</span></span>                                      |
| [<span data-ttu-id="b9136-123">**Ndabshareadd**</span><span class="sxs-lookup"><span data-stu-id="b9136-123">**NDdeShareAdd**</span></span>](nddeshareadd.md)                       | <span data-ttu-id="b9136-124">Erstellt eine neue DDE-Freigabe und fügt Sie dem DDE-Freigabe Datenbank-Manager (DSDM) hinzu.</span><span class="sxs-lookup"><span data-stu-id="b9136-124">Creates and adds a new DDE share to the DDE share database manager (DSDM).</span></span>                                            |
| [<span data-ttu-id="b9136-125">**Ndde sharedel**</span><span class="sxs-lookup"><span data-stu-id="b9136-125">**NDdeShareDel**</span></span>](nddesharedel.md)                       | <span data-ttu-id="b9136-126">Löscht eine DDE-Freigabe aus dem DSDM.</span><span class="sxs-lookup"><span data-stu-id="b9136-126">Deletes a DDE share from the DSDM.</span></span>                                                                                    |
| [<span data-ttu-id="b9136-127">**Ndde shareerum**</span><span class="sxs-lookup"><span data-stu-id="b9136-127">**NDdeShareEnum**</span></span>](nddeshareenum.md)                     | <span data-ttu-id="b9136-128">Ruft die Liste der verfügbaren DDE-Freigaben ab.</span><span class="sxs-lookup"><span data-stu-id="b9136-128">Retrieves the list of available DDE shares.</span></span>                                                                           |
| [<span data-ttu-id="b9136-129">**Ndde sharegetinfo**</span><span class="sxs-lookup"><span data-stu-id="b9136-129">**NDdeShareGetInfo**</span></span>](nddesharegetinfo.md)               | <span data-ttu-id="b9136-130">Ruft DDE-Freigabe Informationen ab.</span><span class="sxs-lookup"><span data-stu-id="b9136-130">Retrieves DDE share information.</span></span>                                                                                      |
| [<span data-ttu-id="b9136-131">**Nddesharesetinfo**</span><span class="sxs-lookup"><span data-stu-id="b9136-131">**NDdeShareSetInfo**</span></span>](nddesharesetinfo.md)               | <span data-ttu-id="b9136-132">Legt DDE-Freigabe Informationen fest.</span><span class="sxs-lookup"><span data-stu-id="b9136-132">Sets DDE share information.</span></span>                                                                                           |
| [<span data-ttu-id="b9136-133">**Nddebug-sharede**</span><span class="sxs-lookup"><span data-stu-id="b9136-133">**NDdeTrustedShareEnum**</span></span>](nddetrustedshareenum.md)       | <span data-ttu-id="b9136-134">Ruft die Namen aller Netzwerk-DDE-Freigaben ab, die im Kontext des aufrufenden Prozesses als vertrauenswürdig eingestuft werden.</span><span class="sxs-lookup"><span data-stu-id="b9136-134">Retrieves the names of all network DDE shares that are trusted in the context of the calling process.</span></span>                 |



 

 

 



