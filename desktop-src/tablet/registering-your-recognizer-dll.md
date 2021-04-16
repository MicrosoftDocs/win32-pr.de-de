---
description: Ihre Erkennungs-DLL muss für die Tablet PC-Plattform registriert sein, damit Sie verwendet werden kann. Die Erkennung muss bei der Installation die folgenden Änderungen an der Registrierung vornehmen.
ms.assetid: 1f1d826b-3968-424b-8da8-b69590058ff1
title: Registrieren der Erkennungs-DLL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51114f11868e6d45dc4d319dab60e5b4f094ddbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530275"
---
# <a name="registering-your-recognizer-dll"></a><span data-ttu-id="c7c08-104">Registrieren der Erkennungs-DLL</span><span class="sxs-lookup"><span data-stu-id="c7c08-104">Registering Your Recognizer DLL</span></span>

<span data-ttu-id="c7c08-105">Ihre Erkennungs-DLL muss für die Tablet PC-Plattform registriert sein, damit Sie verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="c7c08-105">Your recognizer DLL must be registered for the Tablet PC Platform to use it.</span></span> <span data-ttu-id="c7c08-106">Die Erkennung muss bei der Installation die folgenden Änderungen an der Registrierung vornehmen.</span><span class="sxs-lookup"><span data-stu-id="c7c08-106">The recognizer must make the following changes to the registry at installation.</span></span>

<span data-ttu-id="c7c08-107">Fügen Sie unter dem HKEY \_ local \_ Machine/Software/Microsoft/TPG/erkenzers/Registry Key einen neuen Schlüssel für jede CLSIDs Ihres erkenners hinzu.</span><span class="sxs-lookup"><span data-stu-id="c7c08-107">Add a new key for each of the CLSIDs of your recognizer under the HKEY\_LOCAL\_MACHINE/SOFTWARE/Microsoft/TPG/Recognizers/ registry key.</span></span> <span data-ttu-id="c7c08-108">Fügen Sie eine CLSID pro Sprache hinzu.</span><span class="sxs-lookup"><span data-stu-id="c7c08-108">Add one CLSID per language.</span></span> <span data-ttu-id="c7c08-109">In der folgenden Tabelle werden die Werte beschrieben, die unter allen Schlüsseln hinzugefügt werden sollen, die ihre CLSIDs enthalten.</span><span class="sxs-lookup"><span data-stu-id="c7c08-109">The following table describes the values that should be added underneath each of the keys containing your CLSIDs.</span></span>

> [!Note]  
> <span data-ttu-id="c7c08-110">Bei den Namen dieser Werte wird die Groß-/Kleinschreibung beachtet.</span><span class="sxs-lookup"><span data-stu-id="c7c08-110">The names of these values are case sensitive.</span></span>

 



| <span data-ttu-id="c7c08-111">Wertname</span><span class="sxs-lookup"><span data-stu-id="c7c08-111">Value name</span></span>                             | <span data-ttu-id="c7c08-112">Werttyp</span><span class="sxs-lookup"><span data-stu-id="c7c08-112">Value type</span></span>             | <span data-ttu-id="c7c08-113">Wertbeschreibung</span><span class="sxs-lookup"><span data-stu-id="c7c08-113">Value description</span></span>                                                                                                                                                                                                                                                                                                                                                                                  |
|----------------------------------------|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7c08-114">Funktionsflags für Erkennungsfunktionen</span><span class="sxs-lookup"><span data-stu-id="c7c08-114">Recognizer Capability Flags</span></span><br/> | <span data-ttu-id="c7c08-115">REG \_ DWORD</span><span class="sxs-lookup"><span data-stu-id="c7c08-115">REG\_DWORD</span></span><br/>  | <span data-ttu-id="c7c08-116">DWORD, das verwendet wird, um die Funktionen der Erkennung zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="c7c08-116">DWORD used to determine the capabilities of the recognizer.</span></span><br/>                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="c7c08-117">Erkennungs-DLL</span><span class="sxs-lookup"><span data-stu-id="c7c08-117">Recognizer DLL</span></span><br/>              | <span data-ttu-id="c7c08-118">REG- \_ SZ</span><span class="sxs-lookup"><span data-stu-id="c7c08-118">REG\_SZ</span></span><br/>     | <span data-ttu-id="c7c08-119">Vollständiger Pfad zur installierten Erkennungs Modul-dll.</span><span class="sxs-lookup"><span data-stu-id="c7c08-119">Full path to the installed recognizer DLL.</span></span><br/>                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="c7c08-120">Erkannte Sprachen</span><span class="sxs-lookup"><span data-stu-id="c7c08-120">Recognized Languages</span></span><br/>        | <span data-ttu-id="c7c08-121">REG- \_ Binärdatei</span><span class="sxs-lookup"><span data-stu-id="c7c08-121">REG\_BINARY</span></span><br/> | <span data-ttu-id="c7c08-122">Binäres Array, das die Sprache oder die Sprachen beschreibt, mit denen eine Erkennung arbeiten soll.</span><span class="sxs-lookup"><span data-stu-id="c7c08-122">Binary array describing the language or languages that a recognizer is designed to work with.</span></span><br/> <span data-ttu-id="c7c08-123">In "rectypes. h \_ " gibt die maximale Anzahl von Sprachen an, die maximale Anzahl von Sprachen, die von einer Erkennung unterstützt werden, und jede Sprache nimmt ein Wort an, das im Element "erkannte Sprachen" gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="c7c08-123">In rectypes.h, the MAX\_LANGUAGES define specifies the maximum number of languages supported by a recognizer, and each language takes a WORD to store in the "Recognized Languages" item.</span></span> <span data-ttu-id="c7c08-124">Die Größe des \_ Registrierungs Eintrags "reg Binary" sollte "Max \_ Languages \* sizeof (Word)" lauten.</span><span class="sxs-lookup"><span data-stu-id="c7c08-124">The size of the REG\_BINARY registry entry should be MAX\_LANGUAGES \* sizeof(WORD).</span></span><br/> |



 

 

 




