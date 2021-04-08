---
description: Tspimess Age ist ein Enumerationstyp, der den Satz zusätzlicher LineEvent-und phoneevent-Funktionen definiert, die in TSPI angezeigt werden und nicht in TAPI angezeigt werden.
ms.assetid: b3c4ce68-033f-42f1-8c37-66326d21bf32
title: Tspimess Age
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75ed5f081c367c675c565f64146b2201890b8306
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753720"
---
# <a name="tspimessage"></a><span data-ttu-id="80f02-103">Tspimess Age</span><span class="sxs-lookup"><span data-stu-id="80f02-103">TSPIMessage</span></span>

<span data-ttu-id="80f02-104">**Tspimess Age** ist ein Enumerationstyp, der den Satz zusätzlicher [**LineEvent**](/windows/win32/api/tspi/nc-tspi-lineevent) -und [**phoneevent**](/windows/desktop/api/tspi/nc-tspi-phoneevent) -Funktionen definiert, die in TSPI angezeigt werden und nicht in TAPI angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="80f02-104">**TSPIMessage** is an enumeration type that defines the set of additional [**LINEEVENT**](/windows/win32/api/tspi/nc-tspi-lineevent) and [**PHONEEVENT**](/windows/desktop/api/tspi/nc-tspi-phoneevent) functions appearing in TSPI that do not appear in TAPI.</span></span>

## <a name="parameters"></a><span data-ttu-id="80f02-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="80f02-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80f02-106"><span id="TSPI_MESSAGE_BASE"></span><span id="tspi_message_base"></span>TSPI- \_ Nachrichten \_ Basis</span><span class="sxs-lookup"><span data-stu-id="80f02-106"><span id="TSPI_MESSAGE_BASE"></span><span id="tspi_message_base"></span>TSPI\_MESSAGE\_BASE</span></span>
</dt> <dd>

<span data-ttu-id="80f02-107">Die niedrigste Zahl im Bereich von TSPI-spezifischen Nachrichten Werten.</span><span class="sxs-lookup"><span data-stu-id="80f02-107">The lowest number in the range of TSPI-specific message values.</span></span> <span data-ttu-id="80f02-108">Dieser Wert hat keine Bedeutung, sondern dient als Basis zum Definieren der anderen Werte.</span><span class="sxs-lookup"><span data-stu-id="80f02-108">This value has no meaning by itself, but serves as a base for defining the other values.</span></span>

</dd> <dt>

<span data-ttu-id="80f02-109"><span id="LINE_NEWCALL"></span><span id="line_newcall"></span>Zeilen \_ neueinrufe</span><span class="sxs-lookup"><span data-stu-id="80f02-109"><span id="LINE_NEWCALL"></span><span id="line_newcall"></span>LINE\_NEWCALL</span></span>
</dt> <dd>

<span data-ttu-id="80f02-110">Gibt an, dass ein neuer, eingehender-Aufrufvorgang eingetroffen ist und ihn in TAPI einführt.</span><span class="sxs-lookup"><span data-stu-id="80f02-110">Specifies that a new, incoming call has arrived and introduces it to TAPI.</span></span> <span data-ttu-id="80f02-111">Dies muss die erste Nachricht sein, die für einen neuen eingehenden-Befehl an TAPI gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="80f02-111">This must be the first message sent to TAPI for a new incoming call.</span></span> <span data-ttu-id="80f02-112">TAPI gibt seinen nicht transparenten Bezeichner für den-Rückruf als Teil der Verarbeitung dieser Nachricht zurück.</span><span class="sxs-lookup"><span data-stu-id="80f02-112">TAPI returns its opaque identifier for the call as part of its handling of this message.</span></span>

</dd> <dt>

<span data-ttu-id="80f02-113"><span id="LINE_CALLDEVSPECIFIC"></span><span id="line_calldevspecific"></span>Zeile \_ calldevspecific</span><span class="sxs-lookup"><span data-stu-id="80f02-113"><span id="LINE_CALLDEVSPECIFIC"></span><span id="line_calldevspecific"></span>LINE\_CALLDEVSPECIFIC</span></span>
</dt> <dd>

<span data-ttu-id="80f02-114">Gibt an, dass auf einem Telefongerät ein Geräte spezifisches Ereignis aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="80f02-114">Specifies that a device-specific event has occurred on a call device.</span></span>

</dd> <dt>

<span data-ttu-id="80f02-115"><span id="LINE_CALLDEVSPECIFICFEATURE"></span><span id="line_calldevspecificfeature"></span>LINE \_ calldevspecificfeature</span><span class="sxs-lookup"><span data-stu-id="80f02-115"><span id="LINE_CALLDEVSPECIFICFEATURE"></span><span id="line_calldevspecificfeature"></span>LINE\_CALLDEVSPECIFICFEATURE</span></span>
</dt> <dd>

<span data-ttu-id="80f02-116">Gibt an, dass auf einem Telefongerät ein Geräte spezifisches Funktions Ereignis aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="80f02-116">Specifies that a device-specific feature event has occurred on a call device.</span></span>

</dd> </dl>

 

 
