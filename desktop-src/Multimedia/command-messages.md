---
title: Befehlsmeldungen
description: Befehlsmeldungen
ms.assetid: 29b40f35-d390-49c3-99bd-c648c7c50504
keywords:
- MCI-Befehls Meldungen, Informationen zu
- MCI-Befehls Meldungen, Syntax
- mciSendCommand-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cc92b960e646ee1e452c7a356d0291c080d0162
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104516715"
---
# <a name="command-messages"></a><span data-ttu-id="cd12d-106">Befehlsmeldungen</span><span class="sxs-lookup"><span data-stu-id="cd12d-106">Command Messages</span></span>

<span data-ttu-id="cd12d-107">Die befehlsnachrichten Schnittstelle ist so konzipiert, dass Sie von Anwendungen verwendet wird, die eine Programmierschnittstelle in C-Sprache zum Steuern von Multimedia-Geräten benötigen.</span><span class="sxs-lookup"><span data-stu-id="cd12d-107">The command-message interface is designed to be used by applications requiring a C-language interface to control multimedia devices.</span></span> <span data-ttu-id="cd12d-108">Es verwendet ein Nachrichten Übergabe Paradigma für die Kommunikation mit MCI-Geräten.</span><span class="sxs-lookup"><span data-stu-id="cd12d-108">It uses a message-passing paradigm to communicate with MCI devices.</span></span> <span data-ttu-id="cd12d-109">Sie können einen Befehl mit der [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion senden.</span><span class="sxs-lookup"><span data-stu-id="cd12d-109">You can send a command by using the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function.</span></span>

<span data-ttu-id="cd12d-110">Die **mciSendCommand** -Funktion gibt bei Erfolg 0 zurück.</span><span class="sxs-lookup"><span data-stu-id="cd12d-110">The **mciSendCommand** function returns zero if successful.</span></span> <span data-ttu-id="cd12d-111">Wenn die Funktion fehlschlägt, enthält das nieder wertige Wort des Rückgabewerts einen Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="cd12d-111">If the function fails, the low-order word of the return value contains an error code.</span></span> <span data-ttu-id="cd12d-112">Sie können diesen Fehlercode an die [**mcigeterrorstring**](/previous-versions//dd757158(v=vs.85)) -Funktion übergeben, um eine Textbeschreibung des Fehlers zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="cd12d-112">You can pass this error code to the [**mciGetErrorString**](/previous-versions//dd757158(v=vs.85)) function to get a text description of the error.</span></span>

## <a name="syntax-of-command-messages"></a><span data-ttu-id="cd12d-113">Syntax von Befehls Meldungen</span><span class="sxs-lookup"><span data-stu-id="cd12d-113">Syntax of Command Messages</span></span>

<span data-ttu-id="cd12d-114">MCI-befehlsnachrichten bestehen aus den folgenden Elementen:</span><span class="sxs-lookup"><span data-stu-id="cd12d-114">MCI command messages consist of the following elements:</span></span>

-   <span data-ttu-id="cd12d-115">Ein konstanter Nachrichtenwert</span><span class="sxs-lookup"><span data-stu-id="cd12d-115">A constant message value</span></span>
-   <span data-ttu-id="cd12d-116">Eine-Struktur, die Parameter für den Befehl enthält.</span><span class="sxs-lookup"><span data-stu-id="cd12d-116">A structure containing parameters for the command</span></span>
-   <span data-ttu-id="cd12d-117">Ein Satz von Flags, die Optionen für den Befehl angeben und Felder im Parameter Block validieren.</span><span class="sxs-lookup"><span data-stu-id="cd12d-117">A set of flags specifying options for the command and validating fields in the parameter block</span></span>

<span data-ttu-id="cd12d-118">Im folgenden Beispiel wird die [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion verwendet, um den [**MCI- \_ Wiedergabe**](mci-play.md) Befehl an das Gerät zu senden, das durch einen Geräte Bezeichner identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="cd12d-118">The following example uses the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to send the [**MCI\_ PLAY**](mci-play.md) command to the device identified by a device identifier.</span></span>


```C++
mciSendCommand(wDeviceID,            // device identifier 
    MCI_PLAY,                        // command message 
    0,                               // flags 
    (DWORD)(LPVOID) &mciPlayParms);  // parameter block 
```



<span data-ttu-id="cd12d-119">Der im ersten Parameter angegebene Geräte Bezeichner wird abgerufen, wenn das Gerät mit dem [**MCI-Befehl \_ Öffnen**](mci-open.md) geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="cd12d-119">The device identifier given in the first parameter is retrieved when the device is opened using the [**MCI\_ OPEN**](mci-open.md) command.</span></span> <span data-ttu-id="cd12d-120">Der letzte Parameter ist die Adresse einer [**MCI- \_ Wiedergabe \_**](mci-play-parms.md) -Parameter-Struktur, die möglicherweise Informationen darüber enthält, wo die Wiedergabe begonnen und beendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="cd12d-120">The last parameter is the address of an [**MCI\_ PLAY\_ PARMS**](mci-play-parms.md) structure, which might contain information about where to begin and end playback.</span></span> <span data-ttu-id="cd12d-121">Viele MCI-befehlsnachrichten verwenden eine-Struktur, um Parameter dieser Art zu enthalten.</span><span class="sxs-lookup"><span data-stu-id="cd12d-121">Many MCI command messages use a structure to contain parameters of this kind.</span></span> <span data-ttu-id="cd12d-122">Der erste Member jeder dieser Strukturen gibt das Fenster an, das eine [**mm- \_ mcinotify**](mm-mcinotify.md) -Meldung empfängt, wenn der Vorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="cd12d-122">The first member of each of these structures identifies the window that receives an [**MM\_ MCINOTIFY**](mm-mcinotify.md) message when the operation finishes.</span></span>

 

 