---
title: Sprach Leiste (TSF-Anwendungen)
description: Eine Anwendung kann der sprach Leiste keine Elemente hinzufügen. nur ein Text Dienst kann der sprach Leiste Elemente hinzufügen.
ms.assetid: facb0da1-3f80-4745-b021-c026e7e5356c
keywords:
- Text Services-Framework (TSF), sprach Leiste
- TSF (Text Dienst Framework), sprach Leiste
- TSF-aktivierte Anwendungen, sprach Leiste
- sprach Leiste
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef227b29c8b481bfaefc4a218305ba8974fe54e2
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "103858618"
---
# <a name="language-bar-tsf-applications"></a><span data-ttu-id="6d4c7-107">Sprach Leiste (TSF-Anwendungen)</span><span class="sxs-lookup"><span data-stu-id="6d4c7-107">Language Bar (TSF Applications)</span></span>

<span data-ttu-id="6d4c7-108">Eine Anwendung kann der sprach Leiste keine Elemente hinzufügen. nur ein Text Dienst kann der sprach Leiste Elemente hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="6d4c7-108">An application cannot add items to the language bar; only a text service can add items to the language bar.</span></span> <span data-ttu-id="6d4c7-109">Eine Anwendung kann Einfluss darauf haben, wie bestimmte Elemente in der sprach Leiste angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="6d4c7-109">An application can affect how certain items on the language bar appear.</span></span>

<span data-ttu-id="6d4c7-110">Mit dem " [GUID Depot \_ \_ Speech \_ ](predefined-compartments.md) "-Depot wird der Typ der Spracheingabe angegeben, die von der Anwendung akzeptiert werden kann: direkt Texteingabe (Diktat) und/oder Sprachbefehle.</span><span class="sxs-lookup"><span data-stu-id="6d4c7-110">The [GUID\_COMPARTMENT\_SPEECH\_DICTATIONSTAT](predefined-compartments.md) compartment is used to indicate the type of speech input that the application can accept: direct text input (dictation) and/or voice commands.</span></span> <span data-ttu-id="6d4c7-111">Standardmäßig ist das Diktat aktiviert, und der Sprachbefehl ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="6d4c7-111">By default, dictation is enabled and voice command is disabled.</span></span> <span data-ttu-id="6d4c7-112">Wenn die Anwendung Sprachbefehle akzeptieren kann, sollte Sie den Wert für den TF-Befehl [ \_ \_ aktivieren](speech-recognition-constants.md) , der in der Sprachausgabe des GUID-Depots abgelegt wurde \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="6d4c7-112">If the application can accept voice commands, it should set the [TF\_COMMANDING\_ENABLED](speech-recognition-constants.md) value in the GUID\_COMPARTMENT\_SPEECH\_DICTATIONSTAT compartment.</span></span> <span data-ttu-id="6d4c7-113">Wenn die Anwendung eine Diktat Annahme akzeptieren kann, sollte Sie den Wert für die TF- \_ Diktat \_ Aktivierung in der Sprachausgabe des GUID-Depots festlegen \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="6d4c7-113">If the application can accept dictation, it should set the TF\_DICTATION\_ENABLED value in the GUID\_COMPARTMENT\_SPEECH\_DICTATIONSTAT compartment.</span></span> <span data-ttu-id="6d4c7-114">Der TF- \_ Diktat \_ für den Wert oder der TF- \_ \_ Befehl für den Wert dieses Depots bestimmt, welche Mode-(Diktat-oder Befehls) Spracheingaben derzeit in ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="6d4c7-114">The TF\_DICTATION\_ON or TF\_COMMANDING\_ON value of this compartment determines which mode (dictation or command) speech input is currently in.</span></span>

<span data-ttu-id="6d4c7-115">Wenn die Anwendung persistente Speicherung von Eigenschafts Daten unterstützt, sollte das [GUID-Depot \_ \_ persistmenuaktiviertes](predefined-compartments.md) Depot auf einen Wert ungleich 0 (null) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="6d4c7-115">If the application supports persistent storage of property data, it should set the [GUID\_COMPARTMENT\_PERSISTMENUENABLED](predefined-compartments.md) compartment to a nonzero value.</span></span> <span data-ttu-id="6d4c7-116">Dies bewirkt, dass der sprach Text Dienst das Menü Element " **Sprach Daten speichern** " aktiviert.</span><span class="sxs-lookup"><span data-stu-id="6d4c7-116">This causes the speech text service to enable the **Save Speech Data** menu item.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6d4c7-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6d4c7-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6d4c7-118">Einrichten des Text Dienst-Frameworks</span><span class="sxs-lookup"><span data-stu-id="6d4c7-118">How To Set Up Text Services Framework</span></span>](how-to-set-up-tsf.md)
</dt> <dt>

[<span data-ttu-id="6d4c7-119">Sprach Leiste (Text Dienste)</span><span class="sxs-lookup"><span data-stu-id="6d4c7-119">Language Bar (Text Services)</span></span>](language-bar.md)
</dt> </dl>

 

 




