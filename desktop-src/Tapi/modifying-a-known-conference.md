---
description: Das folgende Code Fragment veranschaulicht die Änderung einer Zeitspanne für Konferenzen. Der Standard Zeitraum beträgt 30 Minuten. In diesem Fragment ist die Zeitspanne auf ein Jahr festgelegt.
ms.assetid: 7f05d62e-2bcc-4d98-8a71-97ed20a12af2
title: Ändern einer bekannten Konferenz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5bd58003b276bd3cdd54da2e7ed0df4f154311e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214367"
---
# <a name="modifying-a-known-conference"></a><span data-ttu-id="c78b4-105">Ändern einer bekannten Konferenz</span><span class="sxs-lookup"><span data-stu-id="c78b4-105">Modifying a Known Conference</span></span>

<span data-ttu-id="c78b4-106">\[Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c78b4-106">\[Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="c78b4-107">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="c78b4-107">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="c78b4-108">Das folgende Code Fragment veranschaulicht die Änderung der Zeitspanne einer Konferenz.</span><span class="sxs-lookup"><span data-stu-id="c78b4-108">The following code fragment illustrates modification of a conference's time span.</span></span> <span data-ttu-id="c78b4-109">Der Standard Zeitraum beträgt 30 Minuten.</span><span class="sxs-lookup"><span data-stu-id="c78b4-109">The default time span is thirty minutes.</span></span> <span data-ttu-id="c78b4-110">In diesem Fragment ist die Zeitspanne auf ein Jahr festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c78b4-110">In this fragment, the time span is set to one year.</span></span>

<span data-ttu-id="c78b4-111">Dieses Fragment geht davon aus, dass bereits eine [Verbindung mit einem ILS-Server](connecting-to-an-ils-server.md) hergestellt wurde und dass eine [Konferenz Verzeichnis Enumeration](enumerating-conference-directories.md) ausgeführt wurde, um den Verzeichniseintrag abzurufen, der geändert wird.</span><span class="sxs-lookup"><span data-stu-id="c78b4-111">This fragment assumes that [connecting to an ILS server](connecting-to-an-ils-server.md) has already been performed and that a [conference directory enumeration](enumerating-conference-directories.md) has been performed to obtain the directory entry that will be modified.</span></span>

<span data-ttu-id="c78b4-112">Dieses Fragment geht auch davon aus, dass es sich nicht um eine Multicast Konferenz handelt.</span><span class="sxs-lookup"><span data-stu-id="c78b4-112">This fragment also assumes this is not a multicast conference.</span></span> <span data-ttu-id="c78b4-113">Zum Ändern der Zeiten einer Multicast Konferenz ist eine Benachrichtigung über den Multicast Adress Zuordnungs Server erforderlich.</span><span class="sxs-lookup"><span data-stu-id="c78b4-113">Changing the times on a multicast conference requires notification of the multicast address allocation server.</span></span> <span data-ttu-id="c78b4-114">Ein Beispiel für das Arbeiten mit der Multicast Adressierung finden Sie unter Abrufen [einer Multicast Adresse](acquiring-a-multicast-address.md) .</span><span class="sxs-lookup"><span data-stu-id="c78b4-114">See [Acquiring a Multicast Address](acquiring-a-multicast-address.md) for an example of working with multicast addressing.</span></span>


```C++
// If ( hr != S_OK ) process the error here. 
```



## <a name="related-topics"></a><span data-ttu-id="c78b4-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c78b4-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c78b4-116">**Itdirectoryobjectconference**</span><span class="sxs-lookup"><span data-stu-id="c78b4-116">**ITDirectoryObjectConference**</span></span>](/windows/desktop/api/Rend/nn-rend-itdirectoryobjectconference)
</dt> </dl>

 

 



