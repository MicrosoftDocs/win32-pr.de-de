---
description: Transaktionale NTFS-Funktionen (TxF).
ms.assetid: fb6be33c-9d6c-48b2-a4da-31c60af8d972
title: TxF-Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b59fa3c9a1323ce77c97ee36390190ea6301d71d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758832"
---
# <a name="txf-functions"></a><span data-ttu-id="823aa-103">TxF-Funktionen</span><span class="sxs-lookup"><span data-stu-id="823aa-103">TxF Functions</span></span>

<span data-ttu-id="823aa-104">Transaktionale NTFS (TxF) bietet die folgenden Funktionen.</span><span class="sxs-lookup"><span data-stu-id="823aa-104">Transactional NTFS (TxF) provides the following functions.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="823aa-105">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="823aa-105">In this section</span></span>



| <span data-ttu-id="823aa-106">Funktion</span><span class="sxs-lookup"><span data-stu-id="823aa-106">Function</span></span>                                                                      | <span data-ttu-id="823aa-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="823aa-107">Description</span></span>                                                                                                                  |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="823aa-108">**Txflogkreatefilereadcontext**</span><span class="sxs-lookup"><span data-stu-id="823aa-108">**TxfLogCreateFileReadContext**</span></span>](/windows/desktop/api/TxfW32/nf-txfw32-txflogcreatefilereadcontext)<br/> | <span data-ttu-id="823aa-109">Erstellt einen Kontext, der zum Lesen von Replikations Datensätzen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="823aa-109">Creates a context to be used to read replication records.</span></span><br/>                                                         |
| [<span data-ttu-id="823aa-110">**Txflogdestroyread Context**</span><span class="sxs-lookup"><span data-stu-id="823aa-110">**TxfLogDestroyReadContext**</span></span>](/windows/desktop/api/TxfW32/nf-txfw32-txflogdestroyreadcontext)<br/>       | <span data-ttu-id="823aa-111">Schließt einen von der [**txflogkreatefilereadcontext**](/windows/desktop/api/TxfW32/nf-txfw32-txflogcreatefilereadcontext) -Funktion erstellten Lese Kontext.</span><span class="sxs-lookup"><span data-stu-id="823aa-111">Closes a read context created by the [**TxfLogCreateFileReadContext**](/windows/desktop/api/TxfW32/nf-txfw32-txflogcreatefilereadcontext) function.</span></span><br/> |
| [<span data-ttu-id="823aa-112">**Txflogreadrecords**</span><span class="sxs-lookup"><span data-stu-id="823aa-112">**TxfLogReadRecords**</span></span>](/windows/desktop/api/TxfW32/nf-txfw32-txflogreadrecords)<br/>                     | <span data-ttu-id="823aa-113">Liest die Redo-Einträge aus dem Protokoll.</span><span class="sxs-lookup"><span data-stu-id="823aa-113">Reads the redo records from the log.</span></span><br/>                                                                              |



 

 

 




