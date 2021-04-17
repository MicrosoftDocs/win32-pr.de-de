---
title: Voraussetzungen für das Installieren einer Schema Erweiterung
description: Um das Schema zu ändern, stellen Sie sicher, dass Sie über die folgenden Rechte verfügen und über die folgenden Informationen verfügen. Sie müssen über ausreichende Rechte verfügen, um das Schema zu ändern.
ms.assetid: f7795eac-2b95-4b6c-a2f5-8728316059ab
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 275f468df54b9ced3dcca0648e4cc3602ab71422
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/20/2020
ms.locfileid: "104314374"
---
# <a name="prerequisites-for-installing-a-schema-extension"></a><span data-ttu-id="65cfb-103">Voraussetzungen für das Installieren einer Schema Erweiterung</span><span class="sxs-lookup"><span data-stu-id="65cfb-103">Prerequisites for Installing a Schema Extension</span></span>

<span data-ttu-id="65cfb-104">Um das Schema zu ändern, stellen Sie sicher, dass Sie über die folgenden Rechte verfügen und die folgenden Informationen beachten:</span><span class="sxs-lookup"><span data-stu-id="65cfb-104">To modify the schema, ensure you have the following rights and are aware of the following information:</span></span>

-   <span data-ttu-id="65cfb-105">Sie müssen über ausreichende Rechte verfügen, um das Schema zu ändern.</span><span class="sxs-lookup"><span data-stu-id="65cfb-105">You must have sufficient rights to modify the schema.</span></span> <span data-ttu-id="65cfb-106">Das Schema enthält alle Daten Definitionen für Active Directory Domain Services für das gesamte Unternehmen.</span><span class="sxs-lookup"><span data-stu-id="65cfb-106">The schema contains all of the data definitions for Active Directory Domain Services for the entire enterprise.</span></span> <span data-ttu-id="65cfb-107">Um das Schema zu aktualisieren, muss ein Benutzer Mitglied der Gruppe "Schema Administratoren" sein, oder es muss die Berechtigung zum Aktualisieren des Schemas delegiert worden sein.</span><span class="sxs-lookup"><span data-stu-id="65cfb-107">To update the schema, a user must be a member of the Schema Administrators group, or have been delegated the rights to update the schema.</span></span>
-   <span data-ttu-id="65cfb-108">Schema Änderungen können nur am Schema Master vorgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="65cfb-108">You can only make schema changes at the schema master.</span></span> <span data-ttu-id="65cfb-109">Weitere Informationen finden Sie unter [Erkennen des Schema Masters](detecting-the-schema-master.md).</span><span class="sxs-lookup"><span data-stu-id="65cfb-109">For more information, see [Detecting the Schema Master](detecting-the-schema-master.md).</span></span>
-   <span data-ttu-id="65cfb-110">Der Schema Master muss beschreibbar sein. Das heißt, die Sicherheits intersperre in der Registrierung muss entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="65cfb-110">The schema master must be writable; that is, the safety interlock in the registry must be removed.</span></span> <span data-ttu-id="65cfb-111">Weitere Informationen finden Sie unter [Aktivieren von Schema Änderungen am Schema Master](enabling-schema-changes-at-the-schema-master.md).</span><span class="sxs-lookup"><span data-stu-id="65cfb-111">For more information, see [Enabling Schema Changes at the Schema Master](enabling-schema-changes-at-the-schema-master.md).</span></span>
-   <span data-ttu-id="65cfb-112">Weitere Informationen zum Überprüfen, ob der Schema Master geändert werden kann, und zum Ändern der Einstellungen finden Sie unter "XADM: nicht zum Aktualisieren des Schemas auf dem Schema Besitzer" in der Hilfe-und Support Knowledge Base unter [https://support.microsoft.com/kb/261231](https://support.microsoft.com/kb/261231) .</span><span class="sxs-lookup"><span data-stu-id="65cfb-112">For more information about how to check whether the schema master can be modified, and how to change its settings, see "XADM: Unable to Update the Schema on the Schema Owner" in the Help and Support Knowledge Base at [https://support.microsoft.com/kb/261231](https://support.microsoft.com/kb/261231) .</span></span>

 

 




