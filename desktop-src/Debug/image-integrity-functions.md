---
description: Die Bild Integritäts Funktionen verwalten den Satz von Zertifikaten in einer Bilddatei.
ms.assetid: db77b8af-3c36-4e01-88e0-4c44ef8504ff
title: Bild Integritäts Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a11678dbb12bcb9f29950589b60a84e00960b183
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041410"
---
# <a name="image-integrity-functions"></a><span data-ttu-id="23ab2-103">Bild Integritäts Funktionen</span><span class="sxs-lookup"><span data-stu-id="23ab2-103">Image Integrity Functions</span></span>

<span data-ttu-id="23ab2-104">Die Bild Integritäts Funktionen verwalten den Satz von Zertifikaten in einer Bilddatei.</span><span class="sxs-lookup"><span data-stu-id="23ab2-104">The image integrity functions manage the set of certificates in an image file.</span></span> <span data-ttu-id="23ab2-105">Routinen werden bereitgestellt, um Zertifikate hinzuzufügen, zu entfernen und abzufragen.</span><span class="sxs-lookup"><span data-stu-id="23ab2-105">Routines are provided to add, remove, and query certificates.</span></span> <span data-ttu-id="23ab2-106">Es ist auch eine Funktion zum Abrufen des Bytestreams einer Bilddatei verfügbar, die zum Berechnen eines Nachrichten Digest der Bilddatei erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="23ab2-106">There is also a function available for obtaining the byte stream of an image file required to calculate a message digest of the image file.</span></span> <span data-ttu-id="23ab2-107">Dies ist zum Erstellen von Signatur Zertifikaten erforderlich.</span><span class="sxs-lookup"><span data-stu-id="23ab2-107">This is needed to create signature certificates.</span></span>

<span data-ttu-id="23ab2-108">Jedes Zertifikat in einer Datei verfügt über einen Index, der sich ändern kann, wenn Zertifikate entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="23ab2-108">Every certificate in a file has an index which can change as certificates are removed.</span></span> <span data-ttu-id="23ab2-109">Neue Zertifikate werden immer am Ende der Liste vorhandener Zertifikate hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="23ab2-109">New certificates will always be added "at the end" of the list of existing certificates.</span></span> <span data-ttu-id="23ab2-110">Das heißt, es werden Indizes zugewiesen, die größer sind als alle derzeit verwendeten Indizes.</span><span class="sxs-lookup"><span data-stu-id="23ab2-110">That is, they will be assigned indices that are greater than any index currently in use.</span></span> <span data-ttu-id="23ab2-111">Im Allgemeinen sollte eine Anwendung nicht davon ausgehen, dass ein bestimmtes Zertifikat denselben Index wie das letzte Mal referenziert hat.</span><span class="sxs-lookup"><span data-stu-id="23ab2-111">In general, an application should not assume that a given certificate has the same index it had the last time it was referenced.</span></span>

-   [<span data-ttu-id="23ab2-112">**Digestfunction**</span><span class="sxs-lookup"><span data-stu-id="23ab2-112">**DigestFunction**</span></span>](/windows/desktop/api/Imagehlp/nc-imagehlp-digest_function)
-   [<span data-ttu-id="23ab2-113">**Imageaddcertificate**</span><span class="sxs-lookup"><span data-stu-id="23ab2-113">**ImageAddCertificate**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-imageaddcertificate)
-   [<span data-ttu-id="23ab2-114">**Imageenumeratecertificates**</span><span class="sxs-lookup"><span data-stu-id="23ab2-114">**ImageEnumerateCertificates**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-imageenumeratecertificates)
-   [<span data-ttu-id="23ab2-115">**Imagegetcertificatedata**</span><span class="sxs-lookup"><span data-stu-id="23ab2-115">**ImageGetCertificateData**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-imagegetcertificatedata)
-   [<span data-ttu-id="23ab2-116">**Imagegetcertifialisieheader**</span><span class="sxs-lookup"><span data-stu-id="23ab2-116">**ImageGetCertificateHeader**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-imagegetcertificateheader)
-   [<span data-ttu-id="23ab2-117">**Imagegetdigeststream**</span><span class="sxs-lookup"><span data-stu-id="23ab2-117">**ImageGetDigestStream**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-imagegetdigeststream)
-   [<span data-ttu-id="23ab2-118">**Imageremovecertificate**</span><span class="sxs-lookup"><span data-stu-id="23ab2-118">**ImageRemoveCertificate**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-imageremovecertificate)

 

 



