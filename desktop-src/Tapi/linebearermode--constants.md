---
description: Die \_ Bit-Flag-Konstanten linebearermode beschreiben verschiedene bearermodi eines Aufrufes.
ms.assetid: 87e46ec9-ed5f-4ff5-a382-34eb164f4e66
title: LINEBEARERMODE_ Konstanten (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc7d48689dd435e0a07e1ce9fa5a2a9915b1bf69
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367110"
---
# <a name="linebearermode_-constants"></a><span data-ttu-id="97f61-103">Linebearermode- \_ Konstanten</span><span class="sxs-lookup"><span data-stu-id="97f61-103">LINEBEARERMODE\_ Constants</span></span>

<span data-ttu-id="97f61-104">Die Bit-Flag-Konstanten **linebearermode \_ beschreiben verschiedene bearermodi** eines Aufrufes.</span><span class="sxs-lookup"><span data-stu-id="97f61-104">The **LINEBEARERMODE\_** bit-flag constants describe different bearer modes of a call.</span></span> <span data-ttu-id="97f61-105">Wenn eine Anwendung einen-Befehl aufruft, kann Sie einen bestimmten bearermodus anfordern.</span><span class="sxs-lookup"><span data-stu-id="97f61-105">When an application makes a call, it can request a specific bearer mode.</span></span> <span data-ttu-id="97f61-106">Diese Modi werden verwendet, um eine bestimmte Dienst Qualität für die angeforderte Verbindung vom zugrunde liegenden Telefon Netzwerk auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="97f61-106">These modes are used to select a certain quality of service for the requested connection from the underlying telephone network.</span></span> <span data-ttu-id="97f61-107">Bearermodi, die in einer bestimmten Zeile verfügbar sind, sind eine Geräte Funktion der Zeile.</span><span class="sxs-lookup"><span data-stu-id="97f61-107">Bearer modes available on a given line are a device capability of the line.</span></span>

<dl> <dt>

<span data-ttu-id="97f61-108"><span id="LINEBEARERMODE_ALTSPEECHDATA"></span><span id="linebearermode_altspeechdata"></span>**linebearermode- \_ altredner Daten**</span><span class="sxs-lookup"><span data-stu-id="97f61-108"><span id="LINEBEARERMODE_ALTSPEECHDATA"></span><span id="linebearermode_altspeechdata"></span>**LINEBEARERMODE\_ALTSPEECHDATA**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="97f61-109">Die Alternative Übertragung von Sprache oder uneingeschränkten Daten beim gleichen-Rückruf (ISDN).</span><span class="sxs-lookup"><span data-stu-id="97f61-109">The alternate transfer of speech or unrestricted data on the same call (ISDN).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97f61-110"><span id="LINEBEARERMODE_DATA"></span><span id="linebearermode_data"></span>**linebearermode- \_ Daten**</span><span class="sxs-lookup"><span data-stu-id="97f61-110"><span id="LINEBEARERMODE_DATA"></span><span id="linebearermode_data"></span>**LINEBEARERMODE\_DATA**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="97f61-111">Die uneingeschränkte Datenübertragung beim-Befehl.</span><span class="sxs-lookup"><span data-stu-id="97f61-111">The unrestricted data transfer on the call.</span></span> <span data-ttu-id="97f61-112">Die Datenrate wird separat angegeben.</span><span class="sxs-lookup"><span data-stu-id="97f61-112">The data rate is specified separately.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97f61-113"><span id="LINEBEARERMODE_MULTIUSE"></span><span id="linebearermode_multiuse"></span>**linebearermode- \_ Multiuse**</span><span class="sxs-lookup"><span data-stu-id="97f61-113"><span id="LINEBEARERMODE_MULTIUSE"></span><span id="linebearermode_multiuse"></span>**LINEBEARERMODE\_MULTIUSE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="97f61-114">Der von ISDN definierte Multiuse-Modus.</span><span class="sxs-lookup"><span data-stu-id="97f61-114">The multiuse mode defined by ISDN.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97f61-115"><span id="LINEBEARERMODE_NONCALLSIGNALING"></span><span id="linebearermode_noncallsignaling"></span>**linebearermode- \_ noncallsignsignalisierung**</span><span class="sxs-lookup"><span data-stu-id="97f61-115"><span id="LINEBEARERMODE_NONCALLSIGNALING"></span><span id="linebearermode_noncallsignaling"></span>**LINEBEARERMODE\_NONCALLSIGNALING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="97f61-116">Dies entspricht einer nicht dem Rückruf zugeordneten Signalverbindung von der Anwendung zum Dienstanbieter oder Switch (wird von TAPI als Medienstrom behandelt).</span><span class="sxs-lookup"><span data-stu-id="97f61-116">This corresponds to a non-call-associated signaling connection from the application to the service provider or switch (treated as a media stream by TAPI).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97f61-117"><span id="LINEBEARERMODE_PASSTHROUGH"></span><span id="linebearermode_passthrough"></span>**linebearermode- \_ Passthrough**</span><span class="sxs-lookup"><span data-stu-id="97f61-117"><span id="LINEBEARERMODE_PASSTHROUGH"></span><span id="linebearermode_passthrough"></span>**LINEBEARERMODE\_PASSTHROUGH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="97f61-118">Wenn ein-Befehl in der Passthrough-Anleitung von linebearermode aktiv ist \_ , ermöglicht der Dienstanbieter den direkten Zugriff auf die angefügte Hardware, die von der Anwendung gesteuert werden kann.</span><span class="sxs-lookup"><span data-stu-id="97f61-118">When a call is active in LINEBEARERMODE\_PASSTHROUGH, the service provider gives direct access to the attached hardware for control by the application.</span></span> <span data-ttu-id="97f61-119">Dieser Modus wird hauptsächlich von Anwendungen verwendet, die eine temporäre direkte Steuerung von asynchronen Modems aufrufen, auf die über die [Kommunikationsfunktionen](/windows/desktop/DevIO/communications-functions)zugegriffen wird, um spezielle Features zu konfigurieren oder zu verwenden, die andernfalls vom Dienstanbieter nicht unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="97f61-119">This mode is used primarily by applications desiring temporary direct control over asynchronous modems, accessed through the [communications functions](/windows/desktop/DevIO/communications-functions), for the purpose of configuring or using special features not otherwise supported by the service provider.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97f61-120"><span id="LINEBEARERMODE_RESTRICTEDDATA"></span><span id="linebearermode_restricteddata"></span>**linebearermode \_ restricteddata**</span><span class="sxs-lookup"><span data-stu-id="97f61-120"><span id="LINEBEARERMODE_RESTRICTEDDATA"></span><span id="linebearermode_restricteddata"></span>**LINEBEARERMODE\_RESTRICTEDDATA**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="97f61-121">Bearerdienst für digitale Daten, bei denen nur die nieder wertigen sieben Bits jedes Oktetts Benutzerdaten enthalten können (z. b. für den Wechsel von 56kBit/s-Dienst).</span><span class="sxs-lookup"><span data-stu-id="97f61-121">Bearer service for digital data in which only the low-order seven bits of each octet may contain user data (for example, for Switched 56kbit/s service).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97f61-122"><span id="LINEBEARERMODE_SPEECH"></span><span id="linebearermode_speech"></span>**linebearermode- \_ Sprache**</span><span class="sxs-lookup"><span data-stu-id="97f61-122"><span id="LINEBEARERMODE_SPEECH"></span><span id="linebearermode_speech"></span>**LINEBEARERMODE\_SPEECH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="97f61-123">Dies entspricht der "G. 711"-Sprachübertragung für den-Befehl.</span><span class="sxs-lookup"><span data-stu-id="97f61-123">This corresponds to G.711 speech transmission on the call.</span></span> <span data-ttu-id="97f61-124">Das Netzwerk kann Verarbeitungstechniken wie z. b. eine analoge Übertragung, einen Echo Abbruch und Komprimierung/Dekomprimierung verwenden.</span><span class="sxs-lookup"><span data-stu-id="97f61-124">The network can use processing techniques such as analog transmission, echo cancellation, and compression/decompression.</span></span> <span data-ttu-id="97f61-125">Die bitintegrität ist nicht sicher.</span><span class="sxs-lookup"><span data-stu-id="97f61-125">Bit integrity is not assured.</span></span> <span data-ttu-id="97f61-126">Die Sprache ist nicht für die Unterstützung von Fax-und Modem Medientypen vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="97f61-126">Speech is not intended to support fax and modem media types.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97f61-127"><span id="LINEBEARERMODE_VOICE"></span><span id="linebearermode_voice"></span>**linebearermode- \_ Stimme**</span><span class="sxs-lookup"><span data-stu-id="97f61-127"><span id="LINEBEARERMODE_VOICE"></span><span id="linebearermode_voice"></span>**LINEBEARERMODE\_VOICE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="97f61-128">Dies ist ein regulärer 3,1 kHz-bearerdienstanbieter-bearerdienst.</span><span class="sxs-lookup"><span data-stu-id="97f61-128">This is a regular 3.1 kHz analog voice-grade bearer service.</span></span> <span data-ttu-id="97f61-129">Die bitintegrität ist nicht sicher.</span><span class="sxs-lookup"><span data-stu-id="97f61-129">Bit integrity is not assured.</span></span> <span data-ttu-id="97f61-130">Voice kann Fax-und Modem Medientypen unterstützen.</span><span class="sxs-lookup"><span data-stu-id="97f61-130">Voice can support fax and modem media types.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="97f61-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="97f61-131">Remarks</span></span>

<span data-ttu-id="97f61-132">Die höherwertigen 16 Bits können für gerätespezifische Erweiterungen zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="97f61-132">The high-order 16 bits can be assigned for device-specific extensions.</span></span> <span data-ttu-id="97f61-133">Die nieder wertigen 16 Bits sind reserviert.</span><span class="sxs-lookup"><span data-stu-id="97f61-133">The low-order 16 bits are reserved.</span></span>

<span data-ttu-id="97f61-134">Beachten Sie, dass bearermodus und Medientyp unterschiedliche Vorstellungen sind.</span><span class="sxs-lookup"><span data-stu-id="97f61-134">Note that bearer mode and media type are different notions.</span></span> <span data-ttu-id="97f61-135">Der bearermodus eines Aufrufes ist ein Hinweis auf die Qualität der Telefonverbindung, die in erster Linie vom Netzwerk bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="97f61-135">The bearer mode of a call is an indication of the quality of the telephone connection as provided primarily by the network.</span></span> <span data-ttu-id="97f61-136">Der Medientyp eines Aufrufes ist ein Hinweis auf den Typ des Informationsdaten Stroms, der über diesen Befehl ausgetauscht wird.</span><span class="sxs-lookup"><span data-stu-id="97f61-136">The media type of a call is an indication of the type of information stream that is exchanged over that call.</span></span> <span data-ttu-id="97f61-137">Gruppe 3: Fax-oder Datenmodem sind Medientypen, die einen Anruf mit einem 3,1 kHz-sprach Träger Modus verwenden.</span><span class="sxs-lookup"><span data-stu-id="97f61-137">Group 3 fax or data modem are media types that use a call with a 3.1 kHz voice bearer mode.</span></span>

## <a name="requirements"></a><span data-ttu-id="97f61-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="97f61-138">Requirements</span></span>



| <span data-ttu-id="97f61-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="97f61-139">Requirement</span></span> | <span data-ttu-id="97f61-140">Wert</span><span class="sxs-lookup"><span data-stu-id="97f61-140">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="97f61-141">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="97f61-141">TAPI version</span></span><br/> | <span data-ttu-id="97f61-142">Erfordert TAPI 2,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="97f61-142">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="97f61-143">Header</span><span class="sxs-lookup"><span data-stu-id="97f61-143">Header</span></span><br/>       | <dl> <span data-ttu-id="97f61-144"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="97f61-144"><dt>Tapi.h</dt></span></span> </dl> |



 

