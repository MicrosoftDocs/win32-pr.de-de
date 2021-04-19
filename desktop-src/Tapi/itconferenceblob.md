---
description: Bearbeitet eine Text Konferenzbeschreibung.
ms.assetid: b9ce61d1-3fc5-4963-8d2f-586a4b6a159d
title: Itconferendceblob-Schnittstelle (sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c961b8fb006f1e172f82827216292cb9d12a158f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352999"
---
# <a name="itconferenceblob-interface"></a><span data-ttu-id="515d9-103">Itconferendceblob-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="515d9-103">ITConferenceBlob interface</span></span>

<span data-ttu-id="515d9-104">\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="515d9-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="515d9-105">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="515d9-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="515d9-106">Die **itconferenceblob** -Schnittstelle bearbeitet eine Text Konferenzbeschreibung.</span><span class="sxs-lookup"><span data-stu-id="515d9-106">The **ITConferenceBlob** interface manipulates a textual conference description.</span></span> <span data-ttu-id="515d9-107">Die-Schnittstelle ist für das Format und die Syntax der Konferenzbeschreibung unabhängig.</span><span class="sxs-lookup"><span data-stu-id="515d9-107">The interface is intended to be independent of the format and syntax of the conference description.</span></span> <span data-ttu-id="515d9-108">Um bestimmte Aspekte der Konferenzbeschreibung zu bearbeiten, muss die Anwendung eine andere Schnittstelle Abfragen.</span><span class="sxs-lookup"><span data-stu-id="515d9-108">To manipulate specific aspects of the conference description, the application must query for another interface.</span></span> <span data-ttu-id="515d9-109">Zurzeit werden nur SDP-Konferenz Beschreibungen unterstützt. die Anwendung muss **QueryInterface** für [**itsdp**](itsdp.md) verwenden, um auf die verschiedenen Felder der SDP-Konferenzbeschreibung zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="515d9-109">Currently, only SDP conference descriptions are supported; the application must use **QueryInterface** for [**ITSdp**](itsdp.md) to access the various fields of the SDP conference description.</span></span> <span data-ttu-id="515d9-110">Die **itconferenceblob** -Schnittstelle wird erstellt, indem **QueryInterface** für [**itdirectoryobject**](/windows/desktop/api/Rend/nn-rend-itdirectoryobject)aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="515d9-110">The **ITConferenceBlob** interface is created by calling **QueryInterface** on [**ITDirectoryObject**](/windows/desktop/api/Rend/nn-rend-itdirectoryobject).</span></span>

## <a name="members"></a><span data-ttu-id="515d9-111">Member</span><span class="sxs-lookup"><span data-stu-id="515d9-111">Members</span></span>

<span data-ttu-id="515d9-112">Die **itconferdenceblob** -Schnittstelle erbt von der [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="515d9-112">The **ITConferenceBlob** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="515d9-113">**Itconferenceblob** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="515d9-113">**ITConferenceBlob** also has these types of members:</span></span>

-   [<span data-ttu-id="515d9-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="515d9-114">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="515d9-115">Methoden</span><span class="sxs-lookup"><span data-stu-id="515d9-115">Methods</span></span>

<span data-ttu-id="515d9-116">Die **itconferenumceblob** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="515d9-116">The **ITConferenceBlob** interface has these methods.</span></span>



| <span data-ttu-id="515d9-117">Methode</span><span class="sxs-lookup"><span data-stu-id="515d9-117">Method</span></span>                                                             | <span data-ttu-id="515d9-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="515d9-118">Description</span></span>                                                                                                                                   |
|:-------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="515d9-119">**\_Zeichensatz erhalten**</span><span class="sxs-lookup"><span data-stu-id="515d9-119">**get\_CharacterSet**</span></span>](itconferenceblob-get-characterset.md)     | <span data-ttu-id="515d9-120">Ruft den [**BLOB- \_ Zeichen \_ Satz**](blob-character-set.md) Indikator ab, der anzeigt, ob BLOB-Zeichen in ASCII, Unicode usw. enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="515d9-120">Gets the [**BLOB\_CHARACTER\_SET**](blob-character-set.md) indicator of whether blob characters are in ASCII, Unicode, and so on.</span></span><br/> |
| [<span data-ttu-id="515d9-121">**get- \_ Konferenz-BLOB**</span><span class="sxs-lookup"><span data-stu-id="515d9-121">**get\_ConferenceBlob**</span></span>](itconferenceblob-get-conferenceblob.md) | <span data-ttu-id="515d9-122">Ruft einen Zeiger auf das Konferenz-BLOB ab.</span><span class="sxs-lookup"><span data-stu-id="515d9-122">Gets a pointer to the conference blob.</span></span><br/>                                                                                             |
| [<span data-ttu-id="515d9-123">**Init**</span><span class="sxs-lookup"><span data-stu-id="515d9-123">**Init**</span></span>](itconferenceblob-init.md)                              | <span data-ttu-id="515d9-124">Initialisiert das Konferenz-BLOB.</span><span class="sxs-lookup"><span data-stu-id="515d9-124">Initializes the conference blob.</span></span><br/>                                                                                                   |
| [<span data-ttu-id="515d9-125">**Setconfererceblob**</span><span class="sxs-lookup"><span data-stu-id="515d9-125">**SetConferenceBlob**</span></span>](itconferenceblob-setconferenceblob.md)    | <span data-ttu-id="515d9-126">Führt einen Commit für Änderungen am Konferenz-BLOB aus.</span><span class="sxs-lookup"><span data-stu-id="515d9-126">Commits changes to the conference blob.</span></span><br/>                                                                                            |



 

## <a name="requirements"></a><span data-ttu-id="515d9-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="515d9-127">Requirements</span></span>



| <span data-ttu-id="515d9-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="515d9-128">Requirement</span></span> | <span data-ttu-id="515d9-129">Wert</span><span class="sxs-lookup"><span data-stu-id="515d9-129">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="515d9-130">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="515d9-130">TAPI version</span></span><br/> | <span data-ttu-id="515d9-131">Erfordert TAPI 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="515d9-131">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="515d9-132">Header</span><span class="sxs-lookup"><span data-stu-id="515d9-132">Header</span></span><br/>       | <dl> <span data-ttu-id="515d9-133"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="515d9-133"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="515d9-134">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="515d9-134">Library</span></span><br/>      | <dl> <span data-ttu-id="515d9-135"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="515d9-135"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="515d9-136">DLL</span><span class="sxs-lookup"><span data-stu-id="515d9-136">DLL</span></span><br/>          | <dl> <span data-ttu-id="515d9-137"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="515d9-137"><dt>Sdpblb.dll</dt></span></span> </dl> |



 

