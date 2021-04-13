---
description: Jeder sprach Bezeichner besteht aus einer primär Sprachen-ID, die die Sprache angibt, und einer unter Sprachen-ID, die das Land bzw. die Region angibt.
ms.assetid: 8a6373e0-46c2-4b1b-bc67-543f426ef15a
title: Sprach Bezeichner-Konstanten und Zeichen folgen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d80823e897a8325cbcb7207f91bde69397296767
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346039"
---
# <a name="language-identifier-constants-and-strings"></a><span data-ttu-id="1dbcd-103">Sprach Bezeichner-Konstanten und Zeichen folgen</span><span class="sxs-lookup"><span data-stu-id="1dbcd-103">Language Identifier Constants and Strings</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1dbcd-104">Sprach Bezeichner-Konstanten sind veraltet, und ihre Verwendung ist nicht empfehlenswert.</span><span class="sxs-lookup"><span data-stu-id="1dbcd-104">Language identifier constants are deprecated and their use is discouraged.</span></span> <span data-ttu-id="1dbcd-105">Die Verwendung von Gebiets Schema Namen anstelle von Gebiets Schema bezeichnermerkmalen ist immer vorzuziehen.</span><span class="sxs-lookup"><span data-stu-id="1dbcd-105">Use of locale names instead of locale identifiers is always preferable.</span></span>

<span data-ttu-id="1dbcd-106">Eine Beschreibung von Sprach [Bezeichnern](language-identifiers.md) finden Sie unter Sprach-ID.</span><span class="sxs-lookup"><span data-stu-id="1dbcd-106">See [language identifier](language-identifiers.md) for a description of language identifiers.</span></span>

<span data-ttu-id="1dbcd-107">Ein primärer oder unter Sprachen Bezeichner kann Benutzer definiert oder vordefiniert sein.</span><span class="sxs-lookup"><span data-stu-id="1dbcd-107">A primary or sublanguage identifier can be user-defined or predefined.</span></span> <span data-ttu-id="1dbcd-108">Informationen zu den vordefinierten primär Sprachen Bezeichnern mit Ihren gültigen unter Sprachen Bezeichnern finden Sie unter [[MS-LCID]: Referenz zur Windows-Sprach Code-ID (LCID)](/openspecs/windows_protocols/ms-lcid/70feba9f-294e-491e-b6eb-56532684c37f).</span><span class="sxs-lookup"><span data-stu-id="1dbcd-108">For the predefined primary language identifiers with their valid sublanguage identifiers, see [[MS-LCID]: Windows Language Code Identifier (LCID) Reference](/openspecs/windows_protocols/ms-lcid/70feba9f-294e-491e-b6eb-56532684c37f).</span></span>

> [!Note]  
> <span data-ttu-id="1dbcd-109">Wenn keine unter Sprachen-ID vorhanden ist, die mit einer primär Sprachen-ID verwendet werden kann, sollte die Anwendung den **\_ Standardwert von sublang** verwenden.</span><span class="sxs-lookup"><span data-stu-id="1dbcd-109">If there is no sublanguage identifier to use with a primary language identifier, your application should use **SUBLANG\_DEFAULT**.</span></span> <span data-ttu-id="1dbcd-110">Es sollte für Ressourcen, die für alle unter Sprachen einer Primärsprache identisch sind, die **Unterklasse \_** "lang" verwenden.</span><span class="sxs-lookup"><span data-stu-id="1dbcd-110">It should use **SUBLANG\_NEUTRAL** for resources that are the same for all sublanguages of a primary language.</span></span>

<span data-ttu-id="1dbcd-111">Ein benutzerdefinierter primärer sprach Bezeichner weist einen Wert im Bereich von 0x0200 bis 0x03ff auf.</span><span class="sxs-lookup"><span data-stu-id="1dbcd-111">A user-defined primary language identifier has a value in the range 0x0200 to 0x03ff.</span></span> <span data-ttu-id="1dbcd-112">Alle anderen Werte sind für die Verwendung durch das Betriebssystem reserviert.</span><span class="sxs-lookup"><span data-stu-id="1dbcd-112">All other values are reserved for operating system use.</span></span>

<span data-ttu-id="1dbcd-113">Ein benutzerdefinierter unter Sprachen Bezeichner weist einen Wert im Bereich von 0x20 bis 0x3f auf.</span><span class="sxs-lookup"><span data-stu-id="1dbcd-113">A user-defined sublanguage identifier has a value in the range 0x20 to 0x3f.</span></span> <span data-ttu-id="1dbcd-114">Alle anderen Werte sind für die Verwendung durch das Betriebssystem reserviert.</span><span class="sxs-lookup"><span data-stu-id="1dbcd-114">All other values are reserved for operating system use.</span></span>
