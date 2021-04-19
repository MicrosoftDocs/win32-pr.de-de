---
description: Durch die Verwendung der imm-Funktionalität in ihrer IME-fähigen Anwendung können Benutzer alle möglichen Zeichen Werte merken.
ms.assetid: 43b3e561-b844-4688-ab3d-d99f92ed140e
title: Informationen über den Eingabemethoden-Manager
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af7b96c64eba5ddfb6966c96d88792fd657f94aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353582"
---
# <a name="about-input-method-manager"></a><span data-ttu-id="3828f-103">Informationen über den Eingabemethoden-Manager</span><span class="sxs-lookup"><span data-stu-id="3828f-103">About Input Method Manager</span></span>

<span data-ttu-id="3828f-104">Durch die Verwendung der imm-Funktionalität in ihrer IME-fähigen Anwendung können Benutzer alle möglichen Zeichen Werte merken.</span><span class="sxs-lookup"><span data-stu-id="3828f-104">Use of the IMM functionality in your IME-aware application relieves users of the need to remember all possible character values.</span></span> <span data-ttu-id="3828f-105">Stattdessen ermöglicht es dem IME, die Tastatureingaben eines Benutzers zu überwachen, die vom Benutzer gewünschten Zeichen zu erwarten und eine Liste von Kandidaten Zeichen zur Auswahl zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="3828f-105">Instead, it allows the IME to monitor a user's keystrokes, anticipates the characters the user might want, and presents a list of candidate characters from which to choose.</span></span>

> [!Note]  
> <span data-ttu-id="3828f-106">Der imm führt ähnliche Vorgänge wie das [Text Services-Framework](../tsf/text-services-framework.md)aus, die von Anwendungen verwendet werden, die mit Text Diensten kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="3828f-106">The IMM performs similar operations to those of the [Text Services Framework](../tsf/text-services-framework.md), used by applications that communicate with text services.</span></span>

 

<span data-ttu-id="3828f-107">Standardmäßig stellt das IMM-Fenster ein IME-Fenster bereit, über das der Benutzer Tastatureingaben und Ansichten eingibt und Kandidaten auswählt.</span><span class="sxs-lookup"><span data-stu-id="3828f-107">By default, the IMM provides an IME window through which the user enters keystrokes and views and selects candidates.</span></span> <span data-ttu-id="3828f-108">Anwendungen können die imm-Funktionen und-Nachrichten verwenden, um Ihre eigenen IME-Fenster zu erstellen und zu verwalten. dabei wird eine benutzerdefinierte Schnittstelle bereitgestellt, während die Konvertierungs Funktionen von</span><span class="sxs-lookup"><span data-stu-id="3828f-108">Applications can use the IMM functions and messages to create and manage their own IME windows, providing a custom interface while using the conversion capabilities of the IME.</span></span>

<span data-ttu-id="3828f-109">Der imm ist nur auf ostasiatischen, lokalisierten Windows-Betriebssystemen (Chinesisch, Japanisch, Koreanisch) aktiviert.</span><span class="sxs-lookup"><span data-stu-id="3828f-109">The IMM is only enabled on East Asian (Chinese, Japanese, Korean) localized Windows operating systems.</span></span> <span data-ttu-id="3828f-110">Auf diesen Systemen Ruft die Anwendung [GetSystemMetrics](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) mit SM \_ DbcsEnabled auf, um zu bestimmen, ob der imm aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="3828f-110">On these systems, the application calls [GetSystemMetrics](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) with SM\_DBCSENABLED to determine if the IMM is enabled.</span></span>

<span data-ttu-id="3828f-111">**Windows 2000:** In allen lokalisierten Sprachversionen ist eine Funktions Unterstützung mit vollem Funktionsumfang verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3828f-111">**Windows 2000:** Full-featured IMM support is provided in all localized language versions.</span></span> <span data-ttu-id="3828f-112">Der imm ist jedoch nur aktiviert, wenn ein asiatisches Sprachpaket installiert ist.</span><span class="sxs-lookup"><span data-stu-id="3828f-112">However, the IMM is enabled only when an Asian language pack is installed.</span></span> <span data-ttu-id="3828f-113">Eine IME-fähige Anwendung kann [GetSystemMetrics](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) mit SM \_ immenabled aufrufen, um zu bestimmen, ob der imm aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="3828f-113">An IME-aware application can call [GetSystemMetrics](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) with SM\_IMMENABLED to determine if the IMM is enabled.</span></span>

<span data-ttu-id="3828f-114">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="3828f-114">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="3828f-115">Kandidatenlisten</span><span class="sxs-lookup"><span data-stu-id="3828f-115">Candidate Lists</span></span>](candidate-lists.md)
-   [<span data-ttu-id="3828f-116">Kompositions Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="3828f-116">Composition String</span></span>](composition-string.md)
-   [<span data-ttu-id="3828f-117">Hexin Unicode-IME</span><span class="sxs-lookup"><span data-stu-id="3828f-117">HexToUnicode IME</span></span>](hextounicode-ime.md)
-   [<span data-ttu-id="3828f-118">Abkürzungstasten</span><span class="sxs-lookup"><span data-stu-id="3828f-118">Hot Keys</span></span>](hot-keys.md)
-   [<span data-ttu-id="3828f-119">IME-Nachrichten</span><span class="sxs-lookup"><span data-stu-id="3828f-119">IME Messages</span></span>](ime-messages.md)
-   [<span data-ttu-id="3828f-120">IME-Fenster Klasse</span><span class="sxs-lookup"><span data-stu-id="3828f-120">IME Window Class</span></span>](ime-window-class.md)
-   [<span data-ttu-id="3828f-121">Eingabe Kontext</span><span class="sxs-lookup"><span data-stu-id="3828f-121">Input Context</span></span>](input-context.md)
-   [<span data-ttu-id="3828f-122">Fenster "Status", "Komposition" und "Kandidaten"</span><span class="sxs-lookup"><span data-stu-id="3828f-122">Status, Composition, and Candidates Windows</span></span>](status--composition--and-candidates-windows.md)

 

 
