---
description: Fragen Sie die Smartcard-Datenbank ab. Sie können eine Liste von Smartcards bereitstellen, die von einem bestimmten Benutzer bereitgestellt werden, die Schnittstellen und den primären Dienstanbieter einer bestimmten Karte, die für das System definierten Lesergruppen und die Leser innerhalb einer Gruppe von Lesergruppen.
ms.assetid: a30cbb99-522c-4752-bfcd-75be608785f1
title: Smartcard-Datenbankabfrage Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd74c15eb475d5de9ccce84ba5936b724c0d8d82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217458"
---
# <a name="smart-card-database-query-functions"></a><span data-ttu-id="7f455-104">Smartcard-Datenbankabfrage Funktionen</span><span class="sxs-lookup"><span data-stu-id="7f455-104">Smart Card Database Query Functions</span></span>

<span data-ttu-id="7f455-105">Mit den folgenden Funktionen wird die [*Smartcard-Datenbank*](../secgloss/s-gly.md)abgefragt.</span><span class="sxs-lookup"><span data-stu-id="7f455-105">The following functions query the [*smart card database*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="7f455-106">Sie können eine Liste von Smartcards bereitstellen, die von einem bestimmten Benutzer bereitgestellt werden, die Schnittstellen und den [*primären Dienstanbieter*](../secgloss/p-gly.md) einer bestimmten Karte, die für das System definierten [*Lesergruppen*](../secgloss/r-gly.md) und die [*Leser*](../secgloss/r-gly.md) innerhalb einer Gruppe von Lesergruppen.</span><span class="sxs-lookup"><span data-stu-id="7f455-106">They can provide a list of smart cards supplied by a specific user, the interfaces and [*primary service provider*](../secgloss/p-gly.md) of a specific card, the [*reader groups*](../secgloss/r-gly.md) defined for the system, and the [*readers*](../secgloss/r-gly.md) within a set of reader groups.</span></span>

<span data-ttu-id="7f455-107">Wenn Sie diese Funktionen verwenden, können Sie die gesamte smartcarddatenbank Abfragen, oder Sie können die Suche eingrenzen, indem Sie den [*Resource Manager-Kontext*](../secgloss/r-gly.md)festlegen.</span><span class="sxs-lookup"><span data-stu-id="7f455-107">When you use these functions, you can query the complete smart card database, or you can narrow the search by setting the [*resource manager context*](../secgloss/r-gly.md).</span></span> <span data-ttu-id="7f455-108">Der Resource Manager-Kontext wird durch Aufrufen von [**SCardEstablishContext**](/windows/desktop/api/Winscard/nf-winscard-scardestablishcontext) festgelegt, bevor eine Abfragefunktion aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="7f455-108">The resource manager context is set by calling [**SCardEstablishContext**](/windows/desktop/api/Winscard/nf-winscard-scardestablishcontext) before calling a query function.</span></span>

> [!Note]  
> <span data-ttu-id="7f455-109">Ohne einen angegebenen Kontext sind einige Informationen möglicherweise aufgrund von Sicherheitseinschränkungen noch nicht zugänglich.</span><span class="sxs-lookup"><span data-stu-id="7f455-109">Without a specified context, some information may still be inaccessible due to security restrictions.</span></span>

 



| <span data-ttu-id="7f455-110">Thema</span><span class="sxs-lookup"><span data-stu-id="7f455-110">Topic</span></span>                                                  | <span data-ttu-id="7f455-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7f455-111">Description</span></span>                                                                                                                                                                          |
|--------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7f455-112">**"Scardgetproviderid"**</span><span class="sxs-lookup"><span data-stu-id="7f455-112">**SCardGetProviderId**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardgetproviderida)       | <span data-ttu-id="7f455-113">Ruft den Bezeichner (GUID) des [*primären Dienstanbieters*](../secgloss/p-gly.md) für die angegebene Karte ab.</span><span class="sxs-lookup"><span data-stu-id="7f455-113">Retrieve the identifier (GUID) of the [*primary service provider*](../secgloss/p-gly.md) for the given card.</span></span> |
| [<span data-ttu-id="7f455-114">**Scardlistcards**</span><span class="sxs-lookup"><span data-stu-id="7f455-114">**SCardListCards**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardlistcardsa)               | <span data-ttu-id="7f455-115">Abrufen einer Liste von Karten, die bereits von einem bestimmten Benutzer in das System eingefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="7f455-115">Retrieve a list of cards previously introduced to the system by a specific user.</span></span>                                                                                                     |
| [<span data-ttu-id="7f455-116">**Scardlistinterfaces**</span><span class="sxs-lookup"><span data-stu-id="7f455-116">**SCardListInterfaces**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardlistinterfacesa)     | <span data-ttu-id="7f455-117">Abrufen der Bezeichner (GUIDs) der Schnittstellen, die von einer angegebenen Karte bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="7f455-117">Retrieve the identifiers (GUIDs) of the interfaces supplied by a given card.</span></span>                                                                                                         |
| [<span data-ttu-id="7f455-118">**Scardlistreadergroups**</span><span class="sxs-lookup"><span data-stu-id="7f455-118">**SCardListReaderGroups**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardlistreadergroupsa) | <span data-ttu-id="7f455-119">Rufen Sie eine Liste der Lesergruppen ab, die bereits im System eingeführt wurden.</span><span class="sxs-lookup"><span data-stu-id="7f455-119">Retrieve a list of reader groups that have previously been introduced to the system.</span></span>                                                                                                 |
| [<span data-ttu-id="7f455-120">**SCardListReaders**</span><span class="sxs-lookup"><span data-stu-id="7f455-120">**SCardListReaders**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardlistreadersa)           | <span data-ttu-id="7f455-121">Ruft die Liste der Leser innerhalb einer Gruppe benannter Lesergruppen ab.</span><span class="sxs-lookup"><span data-stu-id="7f455-121">Retrieve the list of readers within a set of named reader groups.</span></span>                                                                                                                    |



 

 

 
