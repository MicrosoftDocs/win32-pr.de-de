---
title: Iagentaudiooutputpropertiesex GetStatus
description: Iagentaudiooutputpropertiesex GetStatus
ms.assetid: 29bf1379-eebe-4b8b-b8d0-b86d2da78b64
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9dd89f4b3d8101ff15b868551626775e6f2e341f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388472"
---
# <a name="iagentaudiooutputpropertiesexgetstatus"></a><span data-ttu-id="178e5-103">Iagentaudiooutputpropertiesex:: GetStatus</span><span class="sxs-lookup"><span data-stu-id="178e5-103">IAgentAudioOutputPropertiesEx::GetStatus</span></span>

<span data-ttu-id="178e5-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="178e5-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetStatus(
   long * plStatus,  // address of audio channel status
);
```

<span data-ttu-id="178e5-105">Ruft den Status des Audiokanals ab.</span><span class="sxs-lookup"><span data-stu-id="178e5-105">Retrieves the status of the audio channel.</span></span>

-   <span data-ttu-id="178e5-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="178e5-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="178e5-107"><span id="plStatus"></span><span id="plstatus"></span><span id="PLSTATUS"></span>*plstatus*</span><span class="sxs-lookup"><span data-stu-id="178e5-107"><span id="plStatus"></span><span id="plstatus"></span><span id="PLSTATUS"></span>*plStatus*</span></span>
</dt> <dd>

<span data-ttu-id="178e5-108">Status des audioausgabekanals, bei dem es sich um einen der folgenden Werte handeln kann:</span><span class="sxs-lookup"><span data-stu-id="178e5-108">Status of the audio output channel, which may be one of the following values:</span></span>



| <span data-ttu-id="178e5-109">Wert</span><span class="sxs-lookup"><span data-stu-id="178e5-109">Value</span></span>                                                                         | <span data-ttu-id="178e5-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="178e5-110">Description</span></span>                                                                                                    |
|-------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="178e5-111">**Ganzzahl ohne Vorzeichen Short** **- \_ Audiostatus \_ verfügbar = 0;**</span><span class="sxs-lookup"><span data-stu-id="178e5-111">**const unsigned short** **AUDIO\_STATUS\_AVAILABLE = 0;**</span></span><br/>         | <span data-ttu-id="178e5-112">Der audioausgabechannel ist verfügbar (nicht ausgelastet).</span><span class="sxs-lookup"><span data-stu-id="178e5-112">The audio output channel is available (not busy).</span></span>                                                              |
| <span data-ttu-id="178e5-113">**Ganzzahl ohne Vorzeichen Short** -Audiostatus (Ganzzahl ohne Vorzeichen Short) **\_ \_ noaudio= 1;**</span><span class="sxs-lookup"><span data-stu-id="178e5-113">**const unsigned short** **AUDIO\_STATUS\_NOAUDIO = 1;**</span></span><br/>           | <span data-ttu-id="178e5-114">Die Audioausgabe wird nicht unterstützt. Dies ist beispielsweise der Fall, weil keine Soundkarte vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="178e5-114">There is no support for audio output; for example, because there is no sound card.</span></span>                             |
| <span data-ttu-id="178e5-115">der Konstante **Ganzzahl ohne Vorzeichen Short** **\_ Audiostatus \_ kanopenaudio= 2;**</span><span class="sxs-lookup"><span data-stu-id="178e5-115">**const unsigned short** **AUDIO\_STATUS\_CANTOPENAUDIO = 2;**</span></span><br/>     | <span data-ttu-id="178e5-116">Der audioausgabechannel kann nicht geöffnet werden (ist ausgelastet); beispielsweise, weil eine andere Anwendung Audiofunktionen wieder gibt.</span><span class="sxs-lookup"><span data-stu-id="178e5-116">The audio output channel can't be opened (is busy); for example, because another application is playing audio.</span></span> |
| <span data-ttu-id="178e5-117">" **Ganzzahl ohne Vorzeichen Short** **\_ \_ audiouser sprechender" = 3;**</span><span class="sxs-lookup"><span data-stu-id="178e5-117">**const unsigned short** **AUDIO\_STATUS\_USERSPEAKING = 3;**</span></span><br/>      | <span data-ttu-id="178e5-118">Der audioausgabechannel ist ausgelastet, weil der Server die Benutzer Spracheingabe verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="178e5-118">The audio output channel is busy because the server is processing user speech input</span></span>                            |
| <span data-ttu-id="178e5-119">Konstante **unsignierte** **\_ kurzaudiostatus \_ = 4;**</span><span class="sxs-lookup"><span data-stu-id="178e5-119">**const unsigned short** **AUDIO\_STATUS\_CHARACTERSPEAKING = 4;**</span></span><br/> | <span data-ttu-id="178e5-120">Der audioausgabechannel ist ausgelastet, weil zurzeit ein Zeichen spricht.</span><span class="sxs-lookup"><span data-stu-id="178e5-120">The audio output channel is busy because a character is currently speaking.</span></span>                                    |
| <span data-ttu-id="178e5-121">" **Ganzzahl ohne Vorzeichen Short** **\_ Audiostatus" \_ sroverrideable = 5;**</span><span class="sxs-lookup"><span data-stu-id="178e5-121">**const unsigned short** **AUDIO\_STATUS\_SROVERRIDEABLE = 5;**</span></span><br/>    | <span data-ttu-id="178e5-122">Der audioausgabechannel ist nicht ausgelastet, aber er wartet auf die Benutzer Spracheingabe.</span><span class="sxs-lookup"><span data-stu-id="178e5-122">The audio output channel is not busy, but it is waiting for user speech input.</span></span>                                 |
| <span data-ttu-id="178e5-123">**Ganzzahl ohne Vorzeichen Short** **- \_ audiostatusfehler \_ = 6;**</span><span class="sxs-lookup"><span data-stu-id="178e5-123">**const unsigned short** **AUDIO\_STATUS\_ERROR = 6;**</span></span><br/>             | <span data-ttu-id="178e5-124">Beim Versuch, auf den audioausgabechannel zuzugreifen, ist ein anderes (Unbekanntes) Problem aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="178e5-124">There was some other (unknown) problem in attempting to access the audio output channel.</span></span>                       |



 

</dd> </dl>

<span data-ttu-id="178e5-125">Mit dieser Einstellung kann Ihre Client Anwendung den Status des audioausgabekanals Abfragen.</span><span class="sxs-lookup"><span data-stu-id="178e5-125">This setting enables your client application to query the state of the audio output channel.</span></span> <span data-ttu-id="178e5-126">Sie können dies verwenden, um zu bestimmen, ob Ihr Zeichen sprechen soll oder zu versuchen, den Empfangsmodus zu aktivieren (mit [**iagentcharakteriex::**](lwef.iagentcharacterex::listen_method)Listening).</span><span class="sxs-lookup"><span data-stu-id="178e5-126">You can use this to determine whether to have your character speak or to try to turn on Listening mode (using [**IAgentCharacterEx::Listen**](lwef.iagentcharacterex::listen_method)).</span></span>

 

 





