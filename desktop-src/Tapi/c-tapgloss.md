---
description: Die folgenden Begriffe sind nützlich, um die TAPI-Technologie zu verstehen.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 23331332-38bc-41b9-84c4-281722ddf563
title: C (telefonieapi)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c6fade540235ef6c68b42a0aba364038d674e12
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106350573"
---
# <a name="c-telephony-api"></a><span data-ttu-id="4ab9e-103">C (telefonieapi)</span><span class="sxs-lookup"><span data-stu-id="4ab9e-103">C (Telephony API)</span></span>

<span data-ttu-id="4ab9e-104">[a](a-tapgloss.md) [B](b-tapgloss.md) C [D](d-tapgloss.md) [E](e-tapgloss.md) F G [H](h-tapgloss.md) [I](i-tapgloss.md) J [K](k-tapgloss.md) [L](l-tapgloss.md) [M](m-tapgloss.md) N O [P](p-tapgloss.md) Q [R](r-tapgloss.md) [S](s-tapgloss.md) [T](t-tapgloss.md) [U](u-tapgloss.md) [V](v-tapgloss.md) [W](w-tapgloss.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="4ab9e-104">[A](a-tapgloss.md) [B](b-tapgloss.md) C [D](d-tapgloss.md) [E](e-tapgloss.md) F G [H](h-tapgloss.md) [I](i-tapgloss.md) J [K](k-tapgloss.md) [L](l-tapgloss.md) [M](m-tapgloss.md) N O [P](p-tapgloss.md) Q [R](r-tapgloss.md) [S](s-tapgloss.md) [T](t-tapgloss.md) [U](u-tapgloss.md) [V](v-tapgloss.md) [W](w-tapgloss.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="4ab9e-105"><span id="tapi2.call_classification_tapgloss"></span><span id="TAPI2.CALL_CLASSIFICATION_TAPGLOSS"></span>**aufrufsklassifizierung**</span><span class="sxs-lookup"><span data-stu-id="4ab9e-105"><span id="tapi2.call_classification_tapgloss"></span><span id="TAPI2.CALL_CLASSIFICATION_TAPGLOSS"></span>**call classification**</span></span>
</dt> <dd>

<span data-ttu-id="4ab9e-106">TAPI-Prozess, der Änderungen in der Art des Medien Stroms (sprach-, Fax-, Datenmodem usw.) für beteiligte Anwendungen meldet.</span><span class="sxs-lookup"><span data-stu-id="4ab9e-106">TAPI process that reports changes in the type of media stream (voice, fax, data modem, and so on) to participating applications.</span></span>

</dd> <dt>

<span data-ttu-id="4ab9e-107"><span id="tapi2.call_progress_monitoring_tapgloss"></span><span id="TAPI2.CALL_PROGRESS_MONITORING_TAPGLOSS"></span>**Statusüberwachung für Aufrufe**</span><span class="sxs-lookup"><span data-stu-id="4ab9e-107"><span id="tapi2.call_progress_monitoring_tapgloss"></span><span id="TAPI2.CALL_PROGRESS_MONITORING_TAPGLOSS"></span>**call progress monitoring**</span></span>
</dt> <dd>

<span data-ttu-id="4ab9e-108">Der Prozess des Lauschens auf akustische Töne, wie z. b. einem Wählton, speziellen Informations Tönen, ausgelasteten Signalen und ringbacktönen, um den Status eines Aufrufes zu bestimmen (sein Status durch das Netzwerk).</span><span class="sxs-lookup"><span data-stu-id="4ab9e-108">The process of listening for audible tones such as a dial tone, special information tones, busy signals, and ringback tones to determine the state of a call (its progress through the network).</span></span>

</dd> <dt>

<span data-ttu-id="4ab9e-109"><span id="tapi2.call_redirection_tapgloss"></span><span id="TAPI2.CALL_REDIRECTION_TAPGLOSS"></span>**Rückruf Umleitung**</span><span class="sxs-lookup"><span data-stu-id="4ab9e-109"><span id="tapi2.call_redirection_tapgloss"></span><span id="TAPI2.CALL_REDIRECTION_TAPGLOSS"></span>**call redirection**</span></span>
</dt> <dd>

<span data-ttu-id="4ab9e-110">Eine Funktion, die es einer Anwendung ermöglicht, einen Angebots Anruf an eine andere Adresse zu entfernen, ohne zuerst den Anruf zu beantworten.</span><span class="sxs-lookup"><span data-stu-id="4ab9e-110">A function that allows an application to deflect an offering call to another address without first answering the call.</span></span> <span data-ttu-id="4ab9e-111">Die Rückruf Umleitung unterscheidet sich von der Weiterleitungs Weiterleitung in dieser Telefon Weiterleitung durch den Switch, ohne dass die Anwendung einbezogen wird. die Umleitung kann per Aufruf durch die Anwendung durchgeführt werden, z. b. durch Aufrufer-ID-Informationen.</span><span class="sxs-lookup"><span data-stu-id="4ab9e-111">Call redirection differs from call forwarding in that call forwarding is performed by the switch without the involvement of the application; redirection can be done on a call-by-call basis by the application, for example, driven by caller ID information.</span></span> <span data-ttu-id="4ab9e-112">Dies unterscheidet sich von der Telefon Übertragung, da bei der Übertragung eines Aufrufes erforderlich ist, dass der-Befehl</span><span class="sxs-lookup"><span data-stu-id="4ab9e-112">It differs from call transfer in that transferring a call requires that the call first be answered.</span></span> <span data-ttu-id="4ab9e-113">Weitere Informationen finden Sie unter "Name *-ID*", " *Caller-ID*", " [*Umleitungs*](r-tapgloss.md)-ID" [](r-tapgloss.md)</span><span class="sxs-lookup"><span data-stu-id="4ab9e-113">See *called-ID*, *caller-ID*, [*redirecting ID*](r-tapgloss.md), [*redirection ID*](r-tapgloss.md).</span></span>

</dd> <dt>

<span data-ttu-id="4ab9e-114"><span id="tapi2.called_id_tapgloss"></span><span id="TAPI2.CALLED_ID_TAPGLOSS"></span>**aufgerufene ID**</span><span class="sxs-lookup"><span data-stu-id="4ab9e-114"><span id="tapi2.called_id_tapgloss"></span><span id="TAPI2.CALLED_ID_TAPGLOSS"></span>**called-ID**</span></span>
</dt> <dd>

<span data-ttu-id="4ab9e-115">Identifiziert die ursprüngliche Zieladresse eines Aufrufes.</span><span class="sxs-lookup"><span data-stu-id="4ab9e-115">Identifies the original destination address of a call.</span></span> <span data-ttu-id="4ab9e-116">Siehe " *Umleitung*".</span><span class="sxs-lookup"><span data-stu-id="4ab9e-116">See *call redirection*.</span></span>

</dd> <dt>

<span data-ttu-id="4ab9e-117"><span id="tapi2.caller_id_tapgloss"></span><span id="TAPI2.CALLER_ID_TAPGLOSS"></span>**Anrufer-ID**</span><span class="sxs-lookup"><span data-stu-id="4ab9e-117"><span id="tapi2.caller_id_tapgloss"></span><span id="TAPI2.CALLER_ID_TAPGLOSS"></span>**caller-ID**</span></span>
</dt> <dd>

<span data-ttu-id="4ab9e-118">Identifiziert die Ursprungsadresse eines Aufrufes.</span><span class="sxs-lookup"><span data-stu-id="4ab9e-118">Identifies the originating address of a call.</span></span> <span data-ttu-id="4ab9e-119">Siehe " *Umleitung*".</span><span class="sxs-lookup"><span data-stu-id="4ab9e-119">See *call redirection*.</span></span>

</dd> <dt>

<span data-ttu-id="4ab9e-120"><span id="tapi2.central_office_tapgloss"></span><span id="TAPI2.CENTRAL_OFFICE_TAPGLOSS"></span>**Zentral Niederlassung**</span><span class="sxs-lookup"><span data-stu-id="4ab9e-120"><span id="tapi2.central_office_tapgloss"></span><span id="TAPI2.CENTRAL_OFFICE_TAPGLOSS"></span>**central office**</span></span>
</dt> <dd>

<span data-ttu-id="4ab9e-121">Lokale Einrichtung der Telefongesellschaft, die den Telefondienst in einem bestimmten Bereich bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="4ab9e-121">Telephone company's local facility that provides telephone service in a specific area.</span></span> <span data-ttu-id="4ab9e-122">In der Regel werden Abonnenten Zeilen mit dem Wechsel von Geräten verknüpft, die andere Abonnenten lokal und über lange Distanz miteinander verbinden.</span><span class="sxs-lookup"><span data-stu-id="4ab9e-122">Typically, subscribers' lines are joined to switching equipment that connects other subscribers to each other, locally and over long distance.</span></span> <span data-ttu-id="4ab9e-123">Auch als *Co* bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="4ab9e-123">Also called *CO*.</span></span>

</dd> <dt>

<span data-ttu-id="4ab9e-124"><span id="tapi2.centrex_tapgloss"></span><span id="TAPI2.CENTREX_TAPGLOSS"></span>**Centrex**</span><span class="sxs-lookup"><span data-stu-id="4ab9e-124"><span id="tapi2.centrex_tapgloss"></span><span id="TAPI2.CENTREX_TAPGLOSS"></span>**Centrex**</span></span>
</dt> <dd>

<span data-ttu-id="4ab9e-125">Ein Geschäfts Telefondienst, der von einem lokalen Telefonunternehmen von einer lokalen Niederlassung angeboten wird.</span><span class="sxs-lookup"><span data-stu-id="4ab9e-125">A business telephone service offered by a local telephone company from a local, central office.</span></span>

</dd> <dt>

<span data-ttu-id="4ab9e-126"><span id="tapi2.computer_centric_connection_tapgloss"></span><span id="TAPI2.COMPUTER_CENTRIC_CONNECTION_TAPGLOSS"></span>**Computer zentrierte Verbindung**</span><span class="sxs-lookup"><span data-stu-id="4ab9e-126"><span id="tapi2.computer_centric_connection_tapgloss"></span><span id="TAPI2.COMPUTER_CENTRIC_CONNECTION_TAPGLOSS"></span>**computer-centric connection**</span></span>
</dt> <dd>

<span data-ttu-id="4ab9e-127">Eine Verbindung, bei der eine Computer-Add-in-Karte oder ein externes Feld verwendet wird, das mit dem Telefon Netzwerk und dem Telefon Satz verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="4ab9e-127">A connection that uses a computer add-in card or external box that is connected to both the telephone network and the phone set.</span></span> <span data-ttu-id="4ab9e-128">Vergleichen Sie die [*Telefon zentrierte Verbindung*](p-tapgloss.md).</span><span class="sxs-lookup"><span data-stu-id="4ab9e-128">Compare [*phone-centric connection*](p-tapgloss.md).</span></span>

</dd> <dt>

<span data-ttu-id="4ab9e-129"><span id="tapi2.connected_id_tapgloss"></span><span id="TAPI2.CONNECTED_ID_TAPGLOSS"></span>**verbundene ID**</span><span class="sxs-lookup"><span data-stu-id="4ab9e-129"><span id="tapi2.connected_id_tapgloss"></span><span id="TAPI2.CONNECTED_ID_TAPGLOSS"></span>**connected-ID**</span></span>
</dt> <dd>

<span data-ttu-id="4ab9e-130">Der Bezeichner für die Partei, mit der der-Rückruf tatsächlich verbunden war.</span><span class="sxs-lookup"><span data-stu-id="4ab9e-130">Identifier for the party to which the call was actually connected.</span></span> <span data-ttu-id="4ab9e-131">Dies kann sich von der aufgerufenen Partei unterscheiden, wenn der Aufruf umgeleitet wurde.</span><span class="sxs-lookup"><span data-stu-id="4ab9e-131">This may be different from the called party if the call was diverted.</span></span>

</dd> </dl>

 

 



