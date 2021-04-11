---
description: Der Els-Skript Erkennungsdienst heißt Microsoft Script-Erkennung.
ms.assetid: daf9f549-1eff-4666-b777-227ec31fba30
title: Microsoft-Skript Erkennung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fd38b36cb409c1f03d84b9fc21f2fe4439b8152
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130312"
---
# <a name="microsoft-script-detection"></a><span data-ttu-id="278fb-103">Microsoft-Skript Erkennung</span><span class="sxs-lookup"><span data-stu-id="278fb-103">Microsoft Script Detection</span></span>

<span data-ttu-id="278fb-104">Der Els-Skript Erkennungsdienst heißt Microsoft Script-Erkennung.</span><span class="sxs-lookup"><span data-stu-id="278fb-104">The ELS script detection service is called Microsoft Script Detection.</span></span> <span data-ttu-id="278fb-105">Dieser Dienst ermöglicht es Anwendungen, die Skripts zu erkennen, in denen Text geschrieben wurde.</span><span class="sxs-lookup"><span data-stu-id="278fb-105">This service allows applications to detect the scripts in which text is written.</span></span> <span data-ttu-id="278fb-106">Die NLS-Entsprechung (National Language Support) eines Skript Erkennungs Dienstanbieter ist die [getstringscripts](/windows/desktop/api/Winnls/nf-winnls-getstringscripts) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="278fb-106">The National Language Support (NLS) counterpart of a script detection service is the [GetStringScripts](/windows/desktop/api/Winnls/nf-winnls-getstringscripts) function.</span></span> <span data-ttu-id="278fb-107">Der Els-Dienst ruft jedoch zusätzlich die Textbereiche ab, die zu jedem Schreibsystem gehören.</span><span class="sxs-lookup"><span data-stu-id="278fb-107">However, the ELS service additionally retrieves the text ranges that belong to each writing system.</span></span>

## <a name="input-to-microsoft-script-detection"></a><span data-ttu-id="278fb-108">Eingabe für die Microsoft-Skript Erkennung</span><span class="sxs-lookup"><span data-stu-id="278fb-108">Input to Microsoft Script Detection</span></span>

<span data-ttu-id="278fb-109">Die Eingabe für den Microsoft Script-Erkennungsdienst ist UTF-16-Text, für den der Dienst Skript Bereiche bestimmt.</span><span class="sxs-lookup"><span data-stu-id="278fb-109">The input to the Microsoft Script Detection service is UTF-16 text for which the service determines script ranges.</span></span>

## <a name="output-of-microsoft-script-detection"></a><span data-ttu-id="278fb-110">Ausgabe der Microsoft-Skript Erkennung</span><span class="sxs-lookup"><span data-stu-id="278fb-110">Output of Microsoft Script Detection</span></span>

<span data-ttu-id="278fb-111">Die Ausgabe des Microsoft Script-Erkennungs Dienstanbieter ist ein Array von Bereichen, die jeweils eine mit NULL endenden UTF-16-Zeichenfolge mit dem Unicode-angegebenen Namen des zugeordneten Schreibsystems enthalten.</span><span class="sxs-lookup"><span data-stu-id="278fb-111">The output of the Microsoft Script Detection service is an array of ranges, each containing a null-terminated UTF-16 string with the Unicode-specified name of the associated writing system.</span></span> <span data-ttu-id="278fb-112">Der Dienst meldet reguläre allgemeine (zyyy) und geerbte (Qaai) Zeichen, die dem vorherigen Skript Bereich angehören.</span><span class="sxs-lookup"><span data-stu-id="278fb-112">The service reports regular common (Zyyy) and inherited (Qaai) characters as belonging to the previous script range.</span></span> <span data-ttu-id="278fb-113">Beginnende gängige und geerbte Zeichen werden als zum nächsten Skript Bereich gehörend gemeldet.</span><span class="sxs-lookup"><span data-stu-id="278fb-113">Beginning common and inherited characters are reported as belonging to the next script range.</span></span> <span data-ttu-id="278fb-114">Wenn alle Zeichen im Eingabetext allgemein oder vererbt sind, ist die Ausgabe des dienstantrags ein einzelner Bereich mit der leeren Zeichenfolge als Daten.</span><span class="sxs-lookup"><span data-stu-id="278fb-114">If all the characters in the input text are common or inherited, the output of the service is a single range with the empty string as its data.</span></span>

## <a name="microsoft-script-detection-operation"></a><span data-ttu-id="278fb-115">Microsoft-Skript Erkennungs Vorgang</span><span class="sxs-lookup"><span data-stu-id="278fb-115">Microsoft Script Detection Operation</span></span>

<span data-ttu-id="278fb-116">Der Microsoft Script-Erkennungsdienst ordnet dem vorangehenden Schreibsystem die Code Punkte zu, die dem allgemeinen Bereich angehören.</span><span class="sxs-lookup"><span data-stu-id="278fb-116">The Microsoft Script Detection service maps the code points belonging to the common range to the preceding writing system.</span></span> <span data-ttu-id="278fb-117">Alternativ kann der Dienst die Code Punkte dem nächsten Schreibsystem zuordnen, wenn sich die Code Punkte am Anfang der Eingabe Zeichenfolge befinden.</span><span class="sxs-lookup"><span data-stu-id="278fb-117">Alternatively, the service can map the code points to the next writing system if the code points are at the beginning of the input string.</span></span> <span data-ttu-id="278fb-118">Die Anwendung muss sich nicht mit dem allgemeinen Bereich beschäftigen.</span><span class="sxs-lookup"><span data-stu-id="278fb-118">The application does not have to deal with the common range at all.</span></span>

## <a name="microsoft-script-detection-guid"></a><span data-ttu-id="278fb-119">Microsoft-Skript Erkennungs-GUID</span><span class="sxs-lookup"><span data-stu-id="278fb-119">Microsoft Script Detection GUID</span></span>

<span data-ttu-id="278fb-120">Die GUID für den Microsoft Sprachenerkennung-Dienst wird in elssrvc. h deklariert, wie im folgenden Code gezeigt.</span><span class="sxs-lookup"><span data-stu-id="278fb-120">The GUID for the Microsoft Language Detection service is declared in Elssrvc.h, as shown in the following code.</span></span>


```C++
// {2D64B439-6CAF-4f6b-B688-E5D0F4FAA7D7}
static const GUID ELS_GUID_SCRIPT_DETECTION =
    { 0x2D64B439, 0x6CAF, 0x4F6B, { 0xB6, 0x88, 0xE5, 0xD0, 0xF4, 0xFA, 0xA7, 0xD7 } };
```



## <a name="related-topics"></a><span data-ttu-id="278fb-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="278fb-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="278fb-122">Informationen zu erweiterten linguistischen Diensten</span><span class="sxs-lookup"><span data-stu-id="278fb-122">About Extended Linguistic Services</span></span>](about-extended-linguistic-services.md)
</dt> </dl>

 

 



