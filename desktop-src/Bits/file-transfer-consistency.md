---
title: Datei Übertragungs Konsistenz
description: Bits gewährleistet, dass die Version der Datei, die Sie überträgt, basierend auf der Dateigröße und dem Zeitstempel und nicht auf dem Inhalt konsistent ist (Bits schützt nicht vor man-in-the-Middle-Angriffen).
ms.assetid: ba82f172-a3ac-49d6-bccd-7d0b68ba66de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 533bc0c0db9708528d4ae919572d6e4c1d251ac8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855476"
---
# <a name="file-transfer-consistency"></a><span data-ttu-id="7a9a2-103">Datei Übertragungs Konsistenz</span><span class="sxs-lookup"><span data-stu-id="7a9a2-103">File Transfer Consistency</span></span>

<span data-ttu-id="7a9a2-104">Bits gewährleistet, dass die Version der Datei, die Sie überträgt, basierend auf der Dateigröße und dem Zeitstempel und nicht auf dem Inhalt konsistent ist (Bits schützt nicht vor man-in-the-Middle-Angriffen).</span><span class="sxs-lookup"><span data-stu-id="7a9a2-104">BITS guarantees that the version of the file it transfers is consistent based on the file size and time stamp, not content (BITS does not protect against man-in-the-middle attacks).</span></span> <span data-ttu-id="7a9a2-105">Um den Inhalt selbst zu überprüfen, können Sie die [**IBackgroundCopyFile3:: gettemporaryname**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyfile3-gettemporaryname) -Methode verwenden, um den Namen der Datei abzurufen, die den heruntergeladenen Inhalt enthält, den Inhalt mithilfe Ihres eigenen Mechanismus überprüfen und dann die [**IBackgroundCopyFile3:: setvalidationstate**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyfile3-setvalidationstate) -Methode aufrufen, um Bits anzuzeigen, wenn der Inhalt der Datei gültig ist.</span><span class="sxs-lookup"><span data-stu-id="7a9a2-105">To verify the contents yourself, you can use the [**IBackgroundCopyFile3::GetTemporaryName**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyfile3-gettemporaryname) method to get the name of the file that contains the downloaded content, verify the contents using your own mechanism, and then call the [**IBackgroundCopyFile3::SetValidationState**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyfile3-setvalidationstate) method to indicate to BITS if the contents of the file is valid.</span></span> <span data-ttu-id="7a9a2-106">Wenn Sie den Überprüfungs Zustand auf **false** festgelegt haben und der Inhalt vom Ursprungsserver stammt, wechselt der Auftrag in den Fehlerzustand.</span><span class="sxs-lookup"><span data-stu-id="7a9a2-106">If you set the validation state to **FALSE** and the content is from the origin server, the job goes into the error state.</span></span> <span data-ttu-id="7a9a2-107">Wenn der Inhalt von einem Peer stammt, lädt Bits die Datei vom Ursprungsserver herunter.</span><span class="sxs-lookup"><span data-stu-id="7a9a2-107">If the content is from a peer, BITS downloads the file from the origin server.</span></span>

<span data-ttu-id="7a9a2-108">Wenn die Dateigröße oder der Zeitstempel beim Übertragen der Datei von Bits geändert wird, wird die Übertragung dieser Datei von Bits neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="7a9a2-108">For downloads, if the file size or time stamp changes while BITS is transferring the file, BITS restarts the transfer of that file only.</span></span> <span data-ttu-id="7a9a2-109">Wenn der Download Auftrag z. b. zwei Dateien enthält und die Dateien auf dem Server aktualisiert werden, während Bits die zweite Datei überträgt, wird die Übertragung der zweiten Datei von Bits neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="7a9a2-109">For example, if the download job contains two files and the files are updated on the server while BITS is transferring the second file, BITS restarts the transfer of the second file only.</span></span> <span data-ttu-id="7a9a2-110">Die erste Datei, die bereits erfolgreich übertragen wurde, wird nicht aktualisiert, um die neuen Änderungen widerzuspiegeln.</span><span class="sxs-lookup"><span data-stu-id="7a9a2-110">The first file, which already transferred successfully, is not updated to reflect the new changes.</span></span>

<span data-ttu-id="7a9a2-111">Beachten Sie Folgendes: Wenn Sie der Besitzer der Datei sind, die vom Server heruntergeladen wird, sollten Sie eine neue URL für jede neue Version der Datei erstellen.</span><span class="sxs-lookup"><span data-stu-id="7a9a2-111">Note that if you own the file being downloaded from the server, you should create a new URL for each new version of the file.</span></span> <span data-ttu-id="7a9a2-112">Wenn Sie die gleiche URL für neue Versionen der Datei verwenden, können einige Proxy Server veraltete Daten aus Ihrem Cache verarbeiten, da Sie nicht mit dem ursprünglichen Server überprüft werden, wenn die Datei veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="7a9a2-112">If you use the same URL for new versions of the file, some proxy servers may serve stale data from their cache because they do not verify with the original server if the file is stale.</span></span>

<span data-ttu-id="7a9a2-113">Wenn bei Uploads die Dateigröße oder der Zeitstempel während der Dateiübertragung geändert wird, generiert Bits einen Fehler, und der Auftrag wird in den Status Fehler des Status "BG- \_ Auftragsstatus" versetzt \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="7a9a2-113">For uploads, if the file size or time stamp changes during the file transfer, BITS generates an error and the job is placed in the BG\_JOB\_STATE\_ERROR state.</span></span>

<span data-ttu-id="7a9a2-114">Bits synchronisiert keine Übertragungsanforderungen, wenn mindestens ein Benutzer anfordert, dass dieselbe Datei an denselben Speicherort übertragen wird.</span><span class="sxs-lookup"><span data-stu-id="7a9a2-114">BITS does not synchronize transfer requests when one or more users request that the same file be transferred to the same location.</span></span> <span data-ttu-id="7a9a2-115">Bits überträgt die Datei für jede Anforderung separat.</span><span class="sxs-lookup"><span data-stu-id="7a9a2-115">BITS transfers the file for each request separately.</span></span>

 

 




