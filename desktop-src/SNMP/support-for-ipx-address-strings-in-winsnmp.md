---
title: Unterstützung für IPX-Adress Zeichenfolgen in WinSNMP
description: WinSNMP 2,0 formalisiert die Verwendung von IPX-Adress Zeichenfolgen.
ms.assetid: b90b8e95-dab0-483b-9336-07e20c122cba
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc33c3ff3b589f9614b139260cef993e232f4343
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707313"
---
# <a name="support-for-ipx-address-strings-in-winsnmp"></a><span data-ttu-id="688de-103">Unterstützung für IPX-Adress Zeichenfolgen in WinSNMP</span><span class="sxs-lookup"><span data-stu-id="688de-103">Support for IPX Address Strings in WinSNMP</span></span>

<span data-ttu-id="688de-104">WinSNMP 2,0 formalisiert die Verwendung von IPX-Adress Zeichenfolgen.</span><span class="sxs-lookup"><span data-stu-id="688de-104">WinSNMP 2.0 formalizes the use of IPX address strings.</span></span> <span data-ttu-id="688de-105">Wenn Sie eine IPX-Adress Zeichenfolge als Eingabeparameter für die [**snmpstrautoentity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtoentity) -Funktion angeben, müssen Sie die Zeichenfolge mit den folgenden Standards formatieren:</span><span class="sxs-lookup"><span data-stu-id="688de-105">If you specify an IPX address string as an input parameter to the [**SnmpStrToEntity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtoentity) function, you must format the string using the following standards:</span></span>

-   <span data-ttu-id="688de-106">Eine Netzwerk Nummer, die aus acht hexadezimalen Ziffern besteht (bei Bedarf mit NULL gefüllt)</span><span class="sxs-lookup"><span data-stu-id="688de-106">A network number that consists of eight hexadecimal digits (zero-filled if necessary)</span></span>
-   <span data-ttu-id="688de-107">Ein Trennzeichen (":", "." oder "–")</span><span class="sxs-lookup"><span data-stu-id="688de-107">A separator (either ":", "." or " – ")</span></span>
-   <span data-ttu-id="688de-108">Eine Knotennummer, die aus 12 hexadezimalen Ziffern besteht (bei Bedarf mit NULL gefüllt)</span><span class="sxs-lookup"><span data-stu-id="688de-108">A node number that consists of 12 hexadecimal digits (zero-filled if necessary)</span></span>

<span data-ttu-id="688de-109">Beispiel: 00000001:00081a0d01c2 oder 00000001.00081 a0d01c2.</span><span class="sxs-lookup"><span data-stu-id="688de-109">For example, 00000001:00081A0D01C2 or 00000001.00081a0d01c2.</span></span> <span data-ttu-id="688de-110">Hexadezimale Ziffern können groß-oder Kleinbuchstaben sein.</span><span class="sxs-lookup"><span data-stu-id="688de-110">Hexadecimal digits can be uppercase or lowercase.</span></span>

<span data-ttu-id="688de-111">Dies ist das Format, das die [**snmpentitytostr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpentitytostr) -Funktion verwendet, um eine IPX-Adress Zeichenfolge zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="688de-111">This is the format the [**SnmpEntityToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpentitytostr) function uses to return an IPX address string.</span></span> <span data-ttu-id="688de-112">Die Zeichenfolge wird zurückgegeben, wenn eine Anwendung, die in einem der nicht übersetzten Snmpapi-Modi betrieben wird, \_ die **snmpentitydestr** -Funktion aufruft.</span><span class="sxs-lookup"><span data-stu-id="688de-112">The string is returned when an application that is operating in one of the SNMPAPI\_UNTRANSLATED modes calls the **SnmpEntityToStr** function.</span></span> <span data-ttu-id="688de-113">Die Zeichenfolge kann auch zurückgegeben werden, wenn die Anwendung im Snmpapi \_ -übersetzten Modus betrieben wird und kein benutzerfreundlicher Name für die Entität verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="688de-113">The string can also be returned when the application is operating in SNMPAPI\_TRANSLATED mode and no user-friendly name is available for the entity.</span></span>

 

 




