---
title: Aktualisieren eines dynamischen Objekts
description: Ein Client kann die Gültigkeitsdauer (Time to Live, TTL) eines bestimmten Verzeichniseintrags aktualisieren, um ihn auf zwei Arten zu verbleiben, bevor ein LDAP-Update auf den Wert seines entryttl-Attributs durchgeführt wird, bevor der Eintrag in die Garbage Collection aufgenommen wird
ms.assetid: 5f51013c-b278-4ef7-a235-b238eed79a35
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7866c423fcb715289793a7beefa564150954257
ms.sourcegitcommit: 4d6ff888fd5825e78bc8fd5cdb21d4b542205039
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/18/2020
ms.locfileid: "106338103"
---
# <a name="refreshing-a-dynamic-object"></a><span data-ttu-id="fc258-103">Aktualisieren eines dynamischen Objekts</span><span class="sxs-lookup"><span data-stu-id="fc258-103">Refreshing a Dynamic Object</span></span>

<span data-ttu-id="fc258-104">Ein Client kann die Gültigkeitsdauer (Time to Live, TTL) eines bestimmten Verzeichniseintrags aktualisieren, um ihn auf zwei Arten aktiv zu halten:</span><span class="sxs-lookup"><span data-stu-id="fc258-104">A client can refresh the Time To Live (TTL) of a given directory entry to keep it alive in one of two ways:</span></span>

-   <span data-ttu-id="fc258-105">Das Ausführen eines LDAP-Updates auf den Wert seines **entryttl** -Attributs vor der Garbage Collection.</span><span class="sxs-lookup"><span data-stu-id="fc258-105">Performing an LDAP update to the value of its **entryTTL** attribute before the entry is garbage collected.</span></span> <span data-ttu-id="fc258-106">Diese Methode zum Aktualisieren eines dynamischen Eintrags im Verzeichnis ist eine zusätzliche (optionale) Funktion von Active Directory Domain Services, die nicht von RFC 2589 angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="fc258-106">This method of refreshing a dynamic entry in the directory is an additional (optional) feature of Active Directory Domain Services that is not specified by RFC 2589.</span></span>
-   <span data-ttu-id="fc258-107">Ausführen eines erweiterten LDAP-Vorgangs mit der OID 1.3.6.1.4.1.1466.101.119.1 für die TTL-Aktualisierung, wie in RFC 2589 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="fc258-107">Performing an LDAP extended operation with an OID of 1.3.6.1.4.1.1466.101.119.1 for TTL refresh, as stipulated in the RFC 2589.</span></span> <span data-ttu-id="fc258-108">Diese OID ist als **erweiterte LDAP- \_ TTL-op- \_ \_ \_ OID** in winldap. H definiert.</span><span class="sxs-lookup"><span data-stu-id="fc258-108">This OID is defined as **LDAP\_TTL\_EXTENDED\_OP\_OID** in WINLDAP.H.</span></span>

 
<span data-ttu-id="fc258-109">\* \* Anmerkung \* \* \*: dynamische Objekte werden vom Garbage Collector entfernt, wenn Sie abgelaufen sind. es gibt keine Phase des Objekts, das ein Tombstone ist, wenn es abgelaufen ist.</span><span class="sxs-lookup"><span data-stu-id="fc258-109">\*\*Remark\*\*\*: Dynamic objects are removed by Garbage Collector when they have expired, there is no phase of the object being a tombstone when it has expired.</span></span> <span data-ttu-id="fc258-110">Beim Aktualisieren von Objekten müssen Sie mit der AD-Replikations Latenz vorsichtig sein.</span><span class="sxs-lookup"><span data-stu-id="fc258-110">You need to be careful with the AD replication latency when you refresh objects.</span></span> <span data-ttu-id="fc258-111">Sie müssen sicherstellen, dass das Update zum Aktualisieren der Gültigkeitsdauer früh genug eintrifft, sodass alle Replikate des Namens Kontexts (vollständiger und globaler Katalog) die Aktualisierungs Transaktion sehen, bevor das Objekt lokal abläuft.</span><span class="sxs-lookup"><span data-stu-id="fc258-111">You have to ensure that the update to refresh the TTL arrives early enough so all replicas of the naming context (full and global catalog) see the refresh transaction before the object expires locally.</span></span>

 




