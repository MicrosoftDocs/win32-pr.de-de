---
title: Das Benachrichtigungs Kennzeichen
description: Das Benachrichtigungs Kennzeichen
ms.assetid: ed5dbb0b-ce4d-4bda-8daa-c62cfda717d1
keywords:
- MCI_NOTIFY-Flag
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9093e539becb4ba2f09b48d628a57d8243bd837c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104390276"
---
# <a name="the-notify-flag"></a><span data-ttu-id="06d47-104">Das Benachrichtigungs Kennzeichen</span><span class="sxs-lookup"><span data-stu-id="06d47-104">The Notify Flag</span></span>

<span data-ttu-id="06d47-105">Das Flag "Benachrichtigen" (MCI \_ Notify) weist das Gerät an, eine [**mm-mcinotify**](mm-mcinotify.md) -Nachricht zu senden, wenn das Gerät eine Aktion abschließt.</span><span class="sxs-lookup"><span data-stu-id="06d47-105">The "notify" (MCI\_NOTIFY) flag directs the device to post an [**MM MCINOTIFY**](mm-mcinotify.md) message when the device completes an action.</span></span> <span data-ttu-id="06d47-106">Die Anwendung muss über eine Fenster Prozedur verfügen, um die mm-Meldung zu verarbeiten, \_ dass die Benachrichtigung eine beliebige Auswirkung hat.</span><span class="sxs-lookup"><span data-stu-id="06d47-106">Your application must have a window procedure to process the MM\_MCINOTIFY message for notification to have any effect.</span></span> <span data-ttu-id="06d47-107">Eine mm- \_ mcinotifizierungsmeldung gibt an, dass die Verarbeitung eines Befehls abgeschlossen wurde. es wird jedoch nicht angegeben, ob der Befehl erfolgreich ausgeführt wurde, fehlgeschlagen ist oder ersetzt oder abgebrochen wurde.</span><span class="sxs-lookup"><span data-stu-id="06d47-107">An MM\_MCINOTIFY message indicates that the processing of a command has completed, but it does not indicate whether the command was completed successfully, failed, or was superseded or aborted.</span></span>

<span data-ttu-id="06d47-108">Die Anwendung gibt das Handle für das Zielfenster der Nachricht an, wenn ein Befehl ausgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="06d47-108">The application specifies the handle to the destination window for the message when it issues a command.</span></span> <span data-ttu-id="06d47-109">In der Befehls Zeichenfolgen-Schnittstelle ist dieses Handle der letzte Parameter der [**mciSendString**](/previous-versions//dd757161(v=vs.85)) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="06d47-109">In the command-string interface, this handle is the last parameter of the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function.</span></span> <span data-ttu-id="06d47-110">In der befehlsnachrichten Schnittstelle wird das Handle in dem nieder wertigen Wort des **dwcallback** -Members der Struktur angegeben, die mit der Befehls Meldung gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="06d47-110">In the command-message interface, the handle is specified in the low-order word of the **dwCallBack** member of the structure sent with the command message.</span></span> <span data-ttu-id="06d47-111">(Jede Struktur, die einer Befehls Meldung zugeordnet ist, enthält diesen Member.)</span><span class="sxs-lookup"><span data-stu-id="06d47-111">(Every structure associated with a command message contains this member.)</span></span>

 

 