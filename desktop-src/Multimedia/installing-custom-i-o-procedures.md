---
title: Installieren benutzerdefinierter e/a-Prozeduren
description: Installieren benutzerdefinierter e/a-Prozeduren
ms.assetid: 7b26a062-fa52-4de3-b8c8-b9f9167068fc
keywords:
- Multimedia-Datei-e/a, benutzerdefinierte Verfahren
- Datei-e/a, benutzerdefinierte Prozeduren
- Eingabe und Ausgabe (e/a), benutzerdefinierte Prozeduren
- E/a (Eingabe und Ausgabe), benutzerdefinierte Prozeduren
- Installieren benutzerdefinierter e/a-Prozeduren
- benutzerdefinierte e/a
- mmioinstallioproc-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1574b7076e7344fa8e800ef1f18ad13fcfd3f3af
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104390307"
---
# <a name="installing-custom-io-procedures"></a><span data-ttu-id="a8e44-110">Installieren benutzerdefinierter e/a-Prozeduren</span><span class="sxs-lookup"><span data-stu-id="a8e44-110">Installing Custom I/O Procedures</span></span>

<span data-ttu-id="a8e44-111">Zum Installieren einer e/a-Prozedur, die dem zugeordnet ist. Dateinamenerweiterung des Bogens, verwenden Sie die [**mmioinstallioproc**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc) -Funktion wie folgt:</span><span class="sxs-lookup"><span data-stu-id="a8e44-111">To install an I/O procedure associated with the .ARC filename extension, use the [**mmioInstallIOProc**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc) function as follows:</span></span>


```C++
mmioInstallIOProc (mmioFOURCC('A', 'R', 'C', ' '), 
    (LPMMIOPROC)lpmmioproc, MMIO_INSTALLPROC); 
```



<span data-ttu-id="a8e44-112">Wenn Sie eine e/a-Prozedur mit [**mmioinstallioproc**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc)installieren, bleibt die Prozedur installiert, bis Sie Sie entfernen.</span><span class="sxs-lookup"><span data-stu-id="a8e44-112">When you install an I/O procedure using [**mmioInstallIOProc**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc), the procedure remains installed until you remove it.</span></span> <span data-ttu-id="a8e44-113">Die e/a-Prozedur wird für jede Datei verwendet, die Sie öffnen, solange die Datei über die entsprechende Dateierweiterung verfügt.</span><span class="sxs-lookup"><span data-stu-id="a8e44-113">The I/O procedure is used for any file you open as long as the file has the appropriate filename extension.</span></span>

<span data-ttu-id="a8e44-114">Sie können auch eine e/a-Prozedur vorübergehend mithilfe der [**mmioopen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) -Funktion installieren.</span><span class="sxs-lookup"><span data-stu-id="a8e44-114">You can also temporarily install an I/O procedure by using the [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) function.</span></span> <span data-ttu-id="a8e44-115">In diesem Fall wird die e/a-Prozedur nur mit einer Datei verwendet, die mit **mmioopen** geöffnet wurde, und wird entfernt, wenn die Datei mit der [**mmioclose**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioclose) -Funktion geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="a8e44-115">In this case, the I/O procedure is used only with a file opened by using **mmioOpen** and is removed when the file is closed by using the [**mmioClose**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioclose) function.</span></span> <span data-ttu-id="a8e44-116">Verwenden Sie zum Angeben einer e/a-Prozedur, wenn Sie eine Datei mit **mmioopen** öffnen, den *lpmmioinfo* -Parameter wie folgt, um auf eine [**mmioinfo**](/previous-versions//dd757322(v=vs.85)) -Struktur zu verweisen:</span><span class="sxs-lookup"><span data-stu-id="a8e44-116">To specify an I/O procedure when you open a file by using **mmioOpen**, use the *lpmmioinfo* parameter to reference an [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) structure as follows:</span></span>

1.  <span data-ttu-id="a8e44-117">Legen Sie den **fccioproc** -Member auf **null** fest.</span><span class="sxs-lookup"><span data-stu-id="a8e44-117">Set the **fccIOProc** member to **NULL**.</span></span>
2.  <span data-ttu-id="a8e44-118">Legen Sie den **pioproc** -Member auf die Prozedur Instanz-Adresse des e/a-Verfahrens fest.</span><span class="sxs-lookup"><span data-stu-id="a8e44-118">Set the **pIOProc** member to the procedure-instance address of the I/O procedure.</span></span>
3.  <span data-ttu-id="a8e44-119">Legen Sie alle anderen Mitglieder auf 0 (null) fest (es sei denn, Sie öffnen eine Speicherdatei oder lesen oder schreiben direkt in den Datei-e/a-Puffer).</span><span class="sxs-lookup"><span data-stu-id="a8e44-119">Set all other members to zero (unless you are opening a memory file, or directly reading or writing to the file I/O buffer).</span></span>

<span data-ttu-id="a8e44-120">Entfernen Sie alle e/a-Prozeduren, die Sie installiert haben, bevor Sie die Anwendung beenden.</span><span class="sxs-lookup"><span data-stu-id="a8e44-120">Be sure to remove any I/O procedures you have installed before you exit your application.</span></span>

 

 