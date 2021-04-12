---
description: Verwalten Sie die Smartcard-Datenbank, und aktualisieren Sie die Datenbank mithilfe eines angegebenen Resource Manager-Kontexts.
ms.assetid: a2f457e1-c042-42e7-9071-cf0edd68e27a
title: Verwaltungsfunktionen für Smartcard-Datenbanken
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c424494a30c71e15647da773027311ed53a2599
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347308"
---
# <a name="smart-card-database-management-functions"></a><span data-ttu-id="15a03-103">Verwaltungsfunktionen für Smartcard-Datenbanken</span><span class="sxs-lookup"><span data-stu-id="15a03-103">Smart Card Database Management Functions</span></span>

<span data-ttu-id="15a03-104">Die folgenden Funktionen verwalten die [*Smartcard-Datenbank*](../secgloss/s-gly.md)und aktualisieren die Datenbank mithilfe eines angegebenen [*Resource Manager-Kontexts*](../secgloss/r-gly.md).</span><span class="sxs-lookup"><span data-stu-id="15a03-104">The following functions manage the [*smart card database*](../secgloss/s-gly.md), updating the database by using a specified [*resource manager context*](../secgloss/r-gly.md).</span></span>

> [!Note]  
> <span data-ttu-id="15a03-105">Die Datenbanksicherheit wird durch das Platzieren von Zugriffsbeschränkungen für die Datenbank gewahrt, anstatt dem [*Smartcardsubsystem*](../secgloss/s-gly.md)Sicherheitsmechanismen hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="15a03-105">Database security is maintained by placing access restrictions on the database, rather than by adding security mechanisms to the [*smart card subsystem*](../secgloss/s-gly.md).</span></span>

 



| <span data-ttu-id="15a03-106">Thema</span><span class="sxs-lookup"><span data-stu-id="15a03-106">Topic</span></span>                                                            | <span data-ttu-id="15a03-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="15a03-107">Description</span></span>                                                                                                                                                             |
|------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="15a03-108">**Scardadressaderto Group**</span><span class="sxs-lookup"><span data-stu-id="15a03-108">**SCardAddReaderToGroup**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardaddreadertogroupa)           | <span data-ttu-id="15a03-109">Hinzufügen eines [*Readers*](../secgloss/r-gly.md) zu einer [*Lesergruppe*](../secgloss/r-gly.md)</span><span class="sxs-lookup"><span data-stu-id="15a03-109">Add a [*reader*](../secgloss/r-gly.md) to a [*reader group*](../secgloss/r-gly.md).</span></span> |
| [<span data-ttu-id="15a03-110">**Scardforgetcardtype**</span><span class="sxs-lookup"><span data-stu-id="15a03-110">**SCardForgetCardType**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardforgetcardtypea)               | <span data-ttu-id="15a03-111">Entfernen Sie eine Smartcard aus dem System.</span><span class="sxs-lookup"><span data-stu-id="15a03-111">Remove a smart card from the system.</span></span>                                                                                                                                    |
| [<span data-ttu-id="15a03-112">**Scardforgetreader**</span><span class="sxs-lookup"><span data-stu-id="15a03-112">**SCardForgetReader**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardforgetreadera)                   | <span data-ttu-id="15a03-113">Entfernen Sie einen Reader aus dem System.</span><span class="sxs-lookup"><span data-stu-id="15a03-113">Remove a reader from the system.</span></span>                                                                                                                                        |
| [<span data-ttu-id="15a03-114">**Scardforgetreadergroup**</span><span class="sxs-lookup"><span data-stu-id="15a03-114">**SCardForgetReaderGroup**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardforgetreadergroupa)         | <span data-ttu-id="15a03-115">Entfernen Sie eine Lesergruppe aus dem System.</span><span class="sxs-lookup"><span data-stu-id="15a03-115">Remove a reader group from the system.</span></span>                                                                                                                                  |
| [<span data-ttu-id="15a03-116">**Scardintroducecardtype**</span><span class="sxs-lookup"><span data-stu-id="15a03-116">**SCardIntroduceCardType**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardintroducecardtypea)         | <span data-ttu-id="15a03-117">Stellen Sie eine neue Karte für das System bereit.</span><span class="sxs-lookup"><span data-stu-id="15a03-117">Introduce a new card to the system.</span></span>                                                                                                                                     |
| [<span data-ttu-id="15a03-118">**Scardintroducereader**</span><span class="sxs-lookup"><span data-stu-id="15a03-118">**SCardIntroduceReader**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardintroducereadera)             | <span data-ttu-id="15a03-119">Stellen Sie dem System einen neuen Reader vor.</span><span class="sxs-lookup"><span data-stu-id="15a03-119">Introduce a new reader to the system.</span></span>                                                                                                                                   |
| [<span data-ttu-id="15a03-120">**Scardintroducereadergroup**</span><span class="sxs-lookup"><span data-stu-id="15a03-120">**SCardIntroduceReaderGroup**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardintroducereadergroupa)   | <span data-ttu-id="15a03-121">Stellen Sie dem System eine neue Lesergruppe vor.</span><span class="sxs-lookup"><span data-stu-id="15a03-121">Introduce a new reader group to the system.</span></span>                                                                                                                             |
| [<span data-ttu-id="15a03-122">**Scardremuvereaderfromgroup**</span><span class="sxs-lookup"><span data-stu-id="15a03-122">**SCardRemoveReaderFromGroup**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardremovereaderfromgroupa) | <span data-ttu-id="15a03-123">Entfernen eines Readers aus einer Lesergruppe</span><span class="sxs-lookup"><span data-stu-id="15a03-123">Remove a reader from a reader group.</span></span>                                                                                                                                    |



 

 

 
