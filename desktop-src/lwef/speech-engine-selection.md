---
title: Sprachmodul Auswahl
description: Sprachmodul Auswahl
ms.assetid: f5afedc6-093f-4247-a5c8-277d6b2d646c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a548f0201ba37c8acb867091cc690a913277ff06
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855979"
---
# <a name="speech-engine-selection"></a><span data-ttu-id="37b0d-103">Sprachmodul Auswahl</span><span class="sxs-lookup"><span data-stu-id="37b0d-103">Speech Engine Selection</span></span>

<span data-ttu-id="37b0d-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="37b0d-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="37b0d-105">Die Sprach-ID-Einstellung eines Zeichens bestimmt die Standardsprache für die Spracheingabe. Der Microsoft-Agent fordert SAPI für ein installiertes Modul an, das dieser Sprache entspricht.</span><span class="sxs-lookup"><span data-stu-id="37b0d-105">A character's language ID setting determines its default speech input language; Microsoft Agent requests SAPI for an installed engine that matches that language.</span></span> <span data-ttu-id="37b0d-106">Wenn eine Client Anwendung keine Spracheinstellung angibt, versucht der Microsoft-Agent, eine Spracherkennungs-Engine zu finden, die mit der Benutzer-ID der Standardsprache übereinstimmt (unter Verwendung der Hauptsprachen-ID, der Nebensprachen-ID).</span><span class="sxs-lookup"><span data-stu-id="37b0d-106">If a client application does not specify a language preference, Microsoft Agent will attempt to find a speech recognition engine that matches the user default language ID (using the major language ID, then the minor language ID).</span></span> <span data-ttu-id="37b0d-107">Wenn keine Engine verfügbar ist, die dieser Sprache entspricht, ist die Sprache für dieses Zeichen deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="37b0d-107">If no engine is available matching this language, speech is disabled for that character.</span></span>

<span data-ttu-id="37b0d-108">Sie können auch eine bestimmte Spracherkennungs-Engine anfordern, indem Sie die zugehörige Modus-ID angeben (mithilfe der Eigenschaft " [**srmodeid**](srmodeid-property.md) " des Zeichens).</span><span class="sxs-lookup"><span data-stu-id="37b0d-108">You can also request a specific speech recognition engine by specifying its mode ID (using the character [**SRModeID**](srmodeid-property.md) property).</span></span> <span data-ttu-id="37b0d-109">Wenn die Sprachen-ID für diese Modus-ID jedoch nicht mit der Spracheinstellung des Clients identisch ist, schlägt der-Befehl fehl (es wird ein Fehler im-Steuerelement ausgegeben).</span><span class="sxs-lookup"><span data-stu-id="37b0d-109">However, if the language ID for that mode ID does not match the client's language setting, the call will fail (raise an error in the control).</span></span> <span data-ttu-id="37b0d-110">Die Spracherkennungs-Engine verbleibt dann vom Client die letzte erfolgreich festgelegte Engine, oder, wenn keine, die Engine, die mit der aktuellen Systemsprachen-ID übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="37b0d-110">The speech recognition engine will then remain the last successfully set engine by the client, or if none, the engine that matches the current system language ID.</span></span> <span data-ttu-id="37b0d-111">Wenn es immer noch keine Entsprechung gibt, ist die Spracheingabe für diesen Client nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="37b0d-111">If there is still no match, speech input is not available for that client.</span></span>

<span data-ttu-id="37b0d-112">Der Microsoft-Agent lädt automatisch eine Spracherkennungs-Engine, wenn die Spracheingabe durch einen Benutzer initiiert wird, der den lauschenden Hotkey drückt, oder wenn der Input-Active Client die [**Abhör Methode aufruft**](listen-method.md) .</span><span class="sxs-lookup"><span data-stu-id="37b0d-112">Microsoft Agent automatically loads a speech recognition engine when speech input is initiated by a user pressing the Listening hotkey or the input-active client calls the [**Listen**](listen-method.md) method.</span></span> <span data-ttu-id="37b0d-113">Eine Engine kann jedoch auch geladen werden, wenn Sie die Mode-ID festlegen oder Abfragen, die Eigenschaften des Fensters "Sprachbefehle" festlegen oder Abfragen, [**srstatus**](srstatus-property.md)Abfragen oder die Sprache aktiviert ist und der Benutzer die Spracheingabe Seite der erweiterten Zeichen Optionen anzeigt.</span><span class="sxs-lookup"><span data-stu-id="37b0d-113">However, an engine may also be loaded when setting or querying its mode ID, setting or querying the properties of the Voice Commands Window, querying [**SRStatus**](srstatus-property.md), or when speech is enabled and the user displays the Speech Input page of the Advanced Character Options.</span></span> <span data-ttu-id="37b0d-114">Der Microsoft-Agent lädt jedoch nur die Sprach-Engines, die von Clients verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="37b0d-114">However, Microsoft Agent only keeps loaded the speech engines that clients are using.</span></span>

 

 




