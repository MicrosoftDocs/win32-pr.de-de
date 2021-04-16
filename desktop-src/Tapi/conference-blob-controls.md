---
description: Das folgende Diagramm zeigt die Hauptobjekte, die an den BLOB-Steuerelementen der TAPI 3-Konferenz beteiligt sind Die angezeigten Schnittstellen sind mit den relevanten Referenzseiten hyperverknüpft.
ms.assetid: 535bbb33-01cb-4484-b216-4808e47e4db5
title: Konferenz-BLOB-Steuerelemente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bacf13567abd46f56c399cefa732be97b081cfd3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527224"
---
# <a name="conference-blob-controls"></a><span data-ttu-id="ab5f4-104">Konferenz-BLOB-Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="ab5f4-104">Conference Blob Controls</span></span>

<span data-ttu-id="ab5f4-105">\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ab5f4-105">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="ab5f4-106">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="ab5f4-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="ab5f4-107">Das folgende Diagramm zeigt die Hauptobjekte, die an den BLOB-Steuerelementen der TAPI 3-Konferenz beteiligt sind</span><span class="sxs-lookup"><span data-stu-id="ab5f4-107">The following diagram illustrates the main objects involved in TAPI 3 conference blob controls.</span></span> <span data-ttu-id="ab5f4-108">Die angezeigten Schnittstellen sind mit den relevanten Referenzseiten hyperverknüpft.</span><span class="sxs-lookup"><span data-stu-id="ab5f4-108">Interfaces shown are hyperlinked into the relevant reference pages.</span></span>

![Conference BLOB-Steuerelemente und-Schnittstellen](images/rendblob.png)

<span data-ttu-id="ab5f4-110">Das Konferenz-BLOB enthält anbieterspezifische Informationen zu einem Konferenz Objekt.</span><span class="sxs-lookup"><span data-stu-id="ab5f4-110">The conference blob contains provider-specific information on a conference object.</span></span> <span data-ttu-id="ab5f4-111">Ein Zeiger auf das [**itconferenceblob**](itconferenceblob.md) -Schnittstellen-BLOB wird durch die Durchführung einer QueryInterface-Schnittstelle auf [**itdirectoryobjectconference**](/windows/desktop/api/Rend/nn-rend-itdirectoryobjectconference)abgerufen.</span><span class="sxs-lookup"><span data-stu-id="ab5f4-111">A pointer to the [**ITConferenceBlob**](itconferenceblob.md) interface blob is obtained by doing a QueryInterface on [**ITDirectoryObjectConference**](/windows/desktop/api/Rend/nn-rend-itdirectoryobjectconference).</span></span> <span data-ttu-id="ab5f4-112">Die **itconferenceblob** -Schnittstelle bietet Methoden für die grundlegende Bearbeitung eines generischen Konferenz-BLOBs.</span><span class="sxs-lookup"><span data-stu-id="ab5f4-112">The **ITConferenceBlob** interface provides methods for basic manipulation of a generic conference blob.</span></span> <span data-ttu-id="ab5f4-113">Eine Anwendung, die nicht-SDP-Konferenz-blobvorgänge verwendet, muss für die Detail Bearbeitung eigene Methoden implementieren.</span><span class="sxs-lookup"><span data-stu-id="ab5f4-113">An application using non-SDP conference blobs must implement its own methods for detail manipulation.</span></span>

<span data-ttu-id="ab5f4-114">Rendezvous stellt die [**itsdp**](itsdp.md) -Schnittstelle zum Bearbeiten von SDP-Konferenz-blobden bereit.</span><span class="sxs-lookup"><span data-stu-id="ab5f4-114">Rendezvous provides the [**ITSdp**](itsdp.md) interface for manipulating SDP conference blobs.</span></span> <span data-ttu-id="ab5f4-115">Der SDP ist ein Protokoll zum Beschreiben von Multimedia-Sitzungen und ihrer zugehörigen Zeit Planungsinformationen.</span><span class="sxs-lookup"><span data-stu-id="ab5f4-115">The SDP is a protocol for describing multimedia sessions and their related scheduling information.</span></span> <span data-ttu-id="ab5f4-116">Weitere Informationen zum SDP-Protokoll finden Sie unter Internet Engineering Task Force (IETF) RFC 2327 mit dem Titel "SDP: Sitzungs Beschreibungs Protokoll".</span><span class="sxs-lookup"><span data-stu-id="ab5f4-116">For additional information on the SDP protocol, locate Internet Engineering Task Force (IETF) RFC 2327 entitled "SDP: Session Description Protocol."</span></span> <span data-ttu-id="ab5f4-117">Wenn die **itsdp** -Schnittstelle für ein bestimmtes Konferenz-BLOB vorhanden ist, können Sie einen Zeiger darauf abrufen, indem Sie eine **QueryInterface** für [**itconferenceblob**](itconferenceblob.md)durchgeführt haben.</span><span class="sxs-lookup"><span data-stu-id="ab5f4-117">If the **ITSDP** interface exists for a given conference blob, you can obtain a pointer to it by doing a **QueryInterface** on [**ITConferenceBlob**](itconferenceblob.md).</span></span>

<span data-ttu-id="ab5f4-118">Für SDP-Konferenz-blobspeicher ermöglichen die Schnittstellen [**ittimecollection**](ittimecollection.md), [**ittime**](ittime.md), [**itmediacollection**](itmediacollection.md)und [**ITmedia**](itmedia.md) eine ausführliche Steuerung der SDP-Konferenzzeit und der Medien Merkmale.</span><span class="sxs-lookup"><span data-stu-id="ab5f4-118">For SDP conference blobs, the [**ITTimeCollection**](ittimecollection.md), [**ITTime**](ittime.md), [**ITMediaCollection**](itmediacollection.md), and [**ITMedia**](itmedia.md) interfaces allow detailed control of SDP conference time and media characteristics.</span></span>

 

 



