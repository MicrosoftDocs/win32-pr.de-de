---
description: LOCALE- \_ SISO- \* Konstanten
ms.assetid: c830e9e9-b58a-4d31-929a-ed699bc08d9f
title: LOCALE_SISO *-Konstanten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16a3d7583bc920daa2edc85b641f191b016bbbd5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103959873"
---
# <a name="locale_siso-constants"></a><span data-ttu-id="ffbb1-103">LOCALE- \_ SISO- \* Konstanten</span><span class="sxs-lookup"><span data-stu-id="ffbb1-103">LOCALE\_SISO\* Constants</span></span>

<span data-ttu-id="ffbb1-104">In diesem Thema werden die \_ von NLS verwendeten Gebiets Schema-SISO- \* Konstanten definiert.</span><span class="sxs-lookup"><span data-stu-id="ffbb1-104">This topic defines the LOCALE\_SISO\* constants used by NLS.</span></span>



| <span data-ttu-id="ffbb1-105">Wert</span><span class="sxs-lookup"><span data-stu-id="ffbb1-105">Value</span></span>                     | <span data-ttu-id="ffbb1-106">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="ffbb1-106">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                              |
|---------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ffbb1-107">LOCALE \_ SISO3166CTRYNAME</span><span class="sxs-lookup"><span data-stu-id="ffbb1-107">LOCALE\_SISO3166CTRYNAME</span></span>  | <span data-ttu-id="ffbb1-108">**Windows Me/98, Windows NT 4,0:** Name des Landes bzw. der Region, basierend auf dem ISO-Standard 3166, z. b. "US" für die USA.</span><span class="sxs-lookup"><span data-stu-id="ffbb1-108">**Windows Me/98, Windows NT 4.0:** Country/region name, based on ISO Standard 3166, such as "US" for the United States.</span></span> <span data-ttu-id="ffbb1-109">Dies kann auch eine Zahl, z. b. "029", für die Karibik zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="ffbb1-109">This can also return a number, such as "029" for Caribbean.</span></span> <span data-ttu-id="ffbb1-110">Die maximale Anzahl von Zeichen, die für diese Zeichenfolge zulässig ist, ist neun, einschließlich eines abschließenden NULL-Zeichens.</span><span class="sxs-lookup"><span data-stu-id="ffbb1-110">The maximum number of characters allowed for this string is nine, including a terminating null character.</span></span>                                                                                        |
| <span data-ttu-id="ffbb1-111">LOCALE \_ SISO3166CTRYNAME2</span><span class="sxs-lookup"><span data-stu-id="ffbb1-111">LOCALE\_SISO3166CTRYNAME2</span></span> | <span data-ttu-id="ffbb1-112">**Windows Vista und höher:** Aus drei Buchstaben bestehender ISO-Regions Name (ISO 3166 3-Buchstabe-Code für das Land/die Region), z. b. "USA" für die USA.</span><span class="sxs-lookup"><span data-stu-id="ffbb1-112">**Windows Vista and later:** Three-letter ISO region name (ISO 3166 three-letter code for the country/region), such as "USA" for the United States.</span></span> <span data-ttu-id="ffbb1-113">Dies kann auch eine Zahl, z. b. "029", für die Karibik zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="ffbb1-113">This can also return a number, such as "029" for Caribbean.</span></span> <span data-ttu-id="ffbb1-114">Die maximale Anzahl von Zeichen, die für diese Zeichenfolge zulässig ist, ist neun, einschließlich eines abschließenden NULL-Zeichens.</span><span class="sxs-lookup"><span data-stu-id="ffbb1-114">The maximum number of characters allowed for this string is nine, including a terminating null character.</span></span>                                                            |
| <span data-ttu-id="ffbb1-115">LOCALE \_ SISO639LANGNAME</span><span class="sxs-lookup"><span data-stu-id="ffbb1-115">LOCALE\_SISO639LANGNAME</span></span>   | <span data-ttu-id="ffbb1-116">**Windows Me/98, Windows NT 4,0:** Der abgekürzte Name der Sprache, der vollständig auf den ISO Standard 639-Werten basiert, in Kleinbuchstaben, wie z. b. "en" für Englisch.</span><span class="sxs-lookup"><span data-stu-id="ffbb1-116">**Windows Me/98, Windows NT 4.0:** The abbreviated name of the language based entirely on the ISO Standard 639 values, in lowercase form, such as "en" for English.</span></span> <span data-ttu-id="ffbb1-117">Dabei kann es sich um einen Code aus drei Buchstaben für Sprachen handeln, die keinen aus zwei Buchstaben bestehenden Code haben, z. b. "Haw" für Hawaiisch.</span><span class="sxs-lookup"><span data-stu-id="ffbb1-117">This can be a 3-letter code for languages that don't have a 2-letter code, such as "haw" for Hawaiian.</span></span> <span data-ttu-id="ffbb1-118">Die maximale Anzahl von Zeichen, die für diese Zeichenfolge zulässig ist, ist neun, einschließlich eines abschließenden NULL-Zeichens.</span><span class="sxs-lookup"><span data-stu-id="ffbb1-118">The maximum number of characters allowed for this string is nine, including a terminating null character.</span></span> |
| <span data-ttu-id="ffbb1-119">LOCALE \_ SISO639LANGNAME2</span><span class="sxs-lookup"><span data-stu-id="ffbb1-119">LOCALE\_SISO639LANGNAME2</span></span>  | <span data-ttu-id="ffbb1-120">**Windows Vista und höher:** Aus drei Buchstaben bestehender ISO-Sprach Name (in Kleinbuchstaben) (ISO 639-2 aus drei Buchstaben bestehenden Code für die Sprache), z. b. "eng" für Englisch.</span><span class="sxs-lookup"><span data-stu-id="ffbb1-120">**Windows Vista and later:** Three-letter ISO language name, in lowercase form (ISO 639-2 three-letter code for the language), such as "eng" for English.</span></span> <span data-ttu-id="ffbb1-121">Die maximale Anzahl von Zeichen, die für diese Zeichenfolge zulässig ist, ist neun, einschließlich eines abschließenden NULL-Zeichens.</span><span class="sxs-lookup"><span data-stu-id="ffbb1-121">The maximum number of characters allowed for this string is nine, including a terminating null character.</span></span>                                                                                                                  |



 

 

 



