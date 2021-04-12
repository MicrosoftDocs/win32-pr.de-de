---
description: Terminologie, die zum Beschreiben von Transaktions-NTFS (TxF) verwendet wird.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 44cb060c-e6a6-48d6-bbcf-d8dc1ae8ceb2
title: TxF-Glossar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee17e9c53b804995e7ef3491b68e963e9311a37f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218012"
---
# <a name="txf-glossary"></a><span data-ttu-id="b13ed-103">TxF-Glossar</span><span class="sxs-lookup"><span data-stu-id="b13ed-103">TxF Glossary</span></span>

<dl> <dt>

<span data-ttu-id="b13ed-104"><span id="fs.availability"></span><span id="FS.AVAILABILITY"></span>**verfüg**</span><span class="sxs-lookup"><span data-stu-id="b13ed-104"><span id="fs.availability"></span><span id="FS.AVAILABILITY"></span>**availability**</span></span>
</dt> <dd>

<span data-ttu-id="b13ed-105">Verfügbarkeit bedeutet, dass ein Ressourcen-Manager Transaktionen abbricht, auch wenn dies zu einer Unterbrechung der Konsistenz führt, damit das System weiterhin neue Aufgaben ausführen kann.</span><span class="sxs-lookup"><span data-stu-id="b13ed-105">Availability means that a resource manager will abort transactions even if that would break consistency so that the system can continue to do new work.</span></span> <span data-ttu-id="b13ed-106">Der Standard Ressourcen-Manager erzwingt die Verfügbarkeit auf dem System Volume.</span><span class="sxs-lookup"><span data-stu-id="b13ed-106">The default resource manager forces availability on the system volume.</span></span> <span data-ttu-id="b13ed-107">Wenn das Transaktionsprotokoll z. b. voll ist, kann kein neuer Transaktionsprotokoll-Speicherplatz hinzugefügt werden, und eine ältere Transaktion, die abgebrochen wird, erfordert ein Ergebnis, das von einem übergeordneten Ressourcen-Manager bereitgestellt werden muss, damit eine verteilte Transaktion abgeschlossen wird. der Ressourcen-Manager wartet nicht auf den übergeordneten Transaktions-Manager und bricht diese Transaktion ab</span><span class="sxs-lookup"><span data-stu-id="b13ed-107">For example, if the transaction log is full, new transaction log space cannot be added, and an older transaction that would be aborted requires an outcome to be delivered from a superior resource manager in order for a distributed transaction to complete, the resource manager will not wait for the superior transaction manager and abort that transaction even though that potentially breaks consistency.</span></span>

</dd> <dt>

<span data-ttu-id="b13ed-108"><span id="fs.consistency"></span><span id="FS.CONSISTENCY"></span>**konsistent**</span><span class="sxs-lookup"><span data-stu-id="b13ed-108"><span id="fs.consistency"></span><span id="FS.CONSISTENCY"></span>**consistency**</span></span>
</dt> <dd>

<span data-ttu-id="b13ed-109">Konsistenz bedeutet, dass ein Ressourcen-Manager für neue Transaktionen einen Fehler erzeugt, wenn der Vorgang nicht fortgesetzt werden kann.</span><span class="sxs-lookup"><span data-stu-id="b13ed-109">Consistency means that a resource manager will fail new transactions if it cannot make forward progress.</span></span> <span data-ttu-id="b13ed-110">Wenn das Transaktionsprotokoll z. b. voll ist, kann kein neuer Transaktionsprotokoll-Speicherplatz hinzugefügt werden, und für eine ältere Transaktion, die abgebrochen wird, muss ein Ergebnis von einem übergeordneten Ressourcen-Manager bereitgestellt werden, damit eine verteilte Transaktion abgeschlossen werden kann. der Ressourcen-Manager wartet auf das Ergebnis.</span><span class="sxs-lookup"><span data-stu-id="b13ed-110">For example, if the transaction log is full, new transaction log space cannot be added, and an older transaction that would be aborted requires an outcome to be delivered from a superior resource manager in order for a distributed transaction to complete, the resource manager will wait for that outcome.</span></span>

</dd> <dt>

<span data-ttu-id="b13ed-111"><span id="fs.miniversion"></span><span id="FS.MINIVERSION"></span>**Triggerszenarios**</span><span class="sxs-lookup"><span data-stu-id="b13ed-111"><span id="fs.miniversion"></span><span id="FS.MINIVERSION"></span>**miniversion**</span></span>
</dt> <dd>

<span data-ttu-id="b13ed-112">Eine Triggerszenarios ist eine Version einer Datei, die von einem transaktiven Writer während einer Transaktion erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="b13ed-112">A miniversion is a version of a file that a transacted writer creates during a transaction.</span></span> <span data-ttu-id="b13ed-113">Die Triggerszenarios kann später in der Transaktion mit Schreib geschütztem Zugriff geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="b13ed-113">The miniversion can be opened later in the transaction with read-only access.</span></span>

</dd> <dt>

<span data-ttu-id="b13ed-114"><span id="fs.transacted_reader"></span><span id="FS.TRANSACTED_READER"></span>**transaktive Reader**</span><span class="sxs-lookup"><span data-stu-id="b13ed-114"><span id="fs.transacted_reader"></span><span id="FS.TRANSACTED_READER"></span>**transacted reader**</span></span>
</dt> <dd>

<span data-ttu-id="b13ed-115">Bei einem transaktiven Reader handelt es sich um ein transaktives Datei Handle, das mit einer beliebigen Berechtigung geöffnet ist, die Teil des generischen Lese Zugriffs ist, aber nicht Teil des generischen Schreibzugriffs ist.</span><span class="sxs-lookup"><span data-stu-id="b13ed-115">A transacted reader is a transacted file handle opened with any permission that is a part of generic read access, but is not part of generic write access.</span></span>

</dd> <dt>

<span data-ttu-id="b13ed-116"><span id="fs.transacted_writer"></span><span id="FS.TRANSACTED_WRITER"></span>**Transaktiver Writer**</span><span class="sxs-lookup"><span data-stu-id="b13ed-116"><span id="fs.transacted_writer"></span><span id="FS.TRANSACTED_WRITER"></span>**transacted writer**</span></span>
</dt> <dd>

<span data-ttu-id="b13ed-117">Bei einem transaktiven Writer handelt es sich um ein transaktives Datei Handle, das mit einer beliebigen Berechtigung geöffnet ist, die nicht Teil des allgemeinen Lese Zugriffs ist, aber Teil des generischen Schreibzugriffs ist.</span><span class="sxs-lookup"><span data-stu-id="b13ed-117">A transacted writer is a transacted file handle opened with any permission that is not part of generic read access, but is part of generic write access.</span></span>

</dd> </dl>

 

 



