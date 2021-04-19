---
title: IAgentAudioOutputPropertiesEx GetStatus
description: IAgentAudioOutputPropertiesEx GetStatus
ms.assetid: 29bf1379-eebe-4b8b-b8d0-b86d2da78b64
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f851c8fc73e9f427bd725d7ef647b84a68be13e4
ms.sourcegitcommit: 59ec383331366f8a62c94bb88468ca03e95c43f8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/13/2021
ms.locfileid: "107380744"
---
# <a name="iagentaudiooutputpropertiesexgetstatus"></a><span data-ttu-id="e7812-103">IAgentAudioOutputPropertiesEx::GetStatus</span><span class="sxs-lookup"><span data-stu-id="e7812-103">IAgentAudioOutputPropertiesEx::GetStatus</span></span>

<span data-ttu-id="e7812-104">\[Microsoft Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="e7812-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetStatus(
   long * plStatus,  // address of audio channel status
);
```

<span data-ttu-id="e7812-105">Ruft den Status des Audiokanals ab.</span><span class="sxs-lookup"><span data-stu-id="e7812-105">Retrieves the status of the audio channel.</span></span>

-   <span data-ttu-id="e7812-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="e7812-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="e7812-107"><span id="plStatus"></span><span id="plstatus"></span><span id="PLSTATUS"></span>*plStatus*</span><span class="sxs-lookup"><span data-stu-id="e7812-107"><span id="plStatus"></span><span id="plstatus"></span><span id="PLSTATUS"></span>*plStatus*</span></span>
</dt> <dd>

<span data-ttu-id="e7812-108">Status des Audioausgabekanals, der einer der folgenden Werte sein kann:</span><span class="sxs-lookup"><span data-stu-id="e7812-108">Status of the audio output channel, which may be one of the following values:</span></span>



| <span data-ttu-id="e7812-109">Wert</span><span class="sxs-lookup"><span data-stu-id="e7812-109">Value</span></span>                                                                         | <span data-ttu-id="e7812-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e7812-110">Description</span></span>                                                                                                    |
|-------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7812-111">**const unsigned short** **AUDIO STATUS AVAILABLE = \_ \_ 0;**</span><span class="sxs-lookup"><span data-stu-id="e7812-111">**const unsigned short** **AUDIO\_STATUS\_AVAILABLE = 0;**</span></span><br/>         | <span data-ttu-id="e7812-112">Der Audioausgabekanal ist verfügbar (nicht ausgelastet).</span><span class="sxs-lookup"><span data-stu-id="e7812-112">The audio output channel is available (not busy).</span></span>                                                              |
| <span data-ttu-id="e7812-113">**const unsigned short** **AUDIO STATUS \_ \_ NOAUDIO = 1;**</span><span class="sxs-lookup"><span data-stu-id="e7812-113">**const unsigned short** **AUDIO\_STATUS\_NOAUDIO = 1;**</span></span><br/>           | <span data-ttu-id="e7812-114">Die Audioausgabe wird nicht unterstützt. z. B. weil keine Soundkarte ist.</span><span class="sxs-lookup"><span data-stu-id="e7812-114">There is no support for audio output; for example, because there is no sound card.</span></span>                             |
| <span data-ttu-id="e7812-115">**const unsigned short** **AUDIO STATUS \_ \_ CANTOPENAUDIO = 2;**</span><span class="sxs-lookup"><span data-stu-id="e7812-115">**const unsigned short** **AUDIO\_STATUS\_CANTOPENAUDIO = 2;**</span></span><br/>     | <span data-ttu-id="e7812-116">Der Audioausgabekanal kann nicht geöffnet werden (ist ausgelastet). Dies liegt beispielsweise daran, dass eine andere Anwendung Audio abspielt.</span><span class="sxs-lookup"><span data-stu-id="e7812-116">The audio output channel can't be opened (is busy); for example, because another application is playing audio.</span></span> |
| <span data-ttu-id="e7812-117">**const unsigned short** **AUDIO STATUS \_ \_ USERSPEAKING = 3;**</span><span class="sxs-lookup"><span data-stu-id="e7812-117">**const unsigned short** **AUDIO\_STATUS\_USERSPEAKING = 3;**</span></span><br/>      | <span data-ttu-id="e7812-118">Der Audioausgabekanal ist ausgelastet, da der Server Spracheingaben des Benutzers verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="e7812-118">The audio output channel is busy because the server is processing user speech input</span></span>                            |
| <span data-ttu-id="e7812-119">**const unsigned short** **AUDIO STATUS \_ \_ CHARACTERSPEAKING = 4;**</span><span class="sxs-lookup"><span data-stu-id="e7812-119">**const unsigned short** **AUDIO\_STATUS\_CHARACTERSPEAKING = 4;**</span></span><br/> | <span data-ttu-id="e7812-120">Der Audioausgabekanal ist ausgelastet, da derzeit ein Zeichen spricht.</span><span class="sxs-lookup"><span data-stu-id="e7812-120">The audio output channel is busy because a character is currently speaking.</span></span>                                    |
| <span data-ttu-id="e7812-121">**const unsigned short** **AUDIO STATUS \_ \_ SROVERRIDEABLE = 5;**</span><span class="sxs-lookup"><span data-stu-id="e7812-121">**const unsigned short** **AUDIO\_STATUS\_SROVERRIDEABLE = 5;**</span></span><br/>    | <span data-ttu-id="e7812-122">Der Audioausgabekanal ist nicht ausgelastet, wartet aber auf die Spracheingabe des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="e7812-122">The audio output channel is not busy, but it is waiting for user speech input.</span></span>                                 |
| <span data-ttu-id="e7812-123">**const unsigned short** **AUDIO STATUS ERROR = \_ \_ 6;**</span><span class="sxs-lookup"><span data-stu-id="e7812-123">**const unsigned short** **AUDIO\_STATUS\_ERROR = 6;**</span></span><br/>             | <span data-ttu-id="e7812-124">Es gab ein anderes (unbekanntes) Problem beim Versuch, auf den Audioausgabekanal zu zugreifen.</span><span class="sxs-lookup"><span data-stu-id="e7812-124">There was some other (unknown) problem in attempting to access the audio output channel.</span></span>                       |



 

</dd> </dl>

<span data-ttu-id="e7812-125">Mit dieser Einstellung kann Ihre Clientanwendung den Status des Audioausgabekanals abfragen.</span><span class="sxs-lookup"><span data-stu-id="e7812-125">This setting enables your client application to query the state of the audio output channel.</span></span> <span data-ttu-id="e7812-126">Sie können damit bestimmen, ob Das Zeichen sprechen soll oder ob sie versuchen soll, den Lauschmodus zu aktivieren (mithilfe von **IAgentCharacterEx::Listen**).</span><span class="sxs-lookup"><span data-stu-id="e7812-126">You can use this to determine whether to have your character speak or to try to turn on Listening mode (using **IAgentCharacterEx::Listen**).</span></span>

 

 





