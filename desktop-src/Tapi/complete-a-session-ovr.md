---
description: Mit Abschluss Vorgängen kann eine Anwendung festlegen, wie eine Sitzung behandelt werden soll, wenn Faktoren wie z. b. ein ausgelasteter Ziel eine normale Verbindung verhindern.
ms.assetid: 71e61376-7913-42a9-a8e2-2ea6e4918f30
title: Sitzung beenden
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5736b6be452413811f3530f44db280fe4e2a682f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345780"
---
# <a name="complete-a-session"></a><span data-ttu-id="575e5-103">Sitzung beenden</span><span class="sxs-lookup"><span data-stu-id="575e5-103">Complete a Session</span></span>

<span data-ttu-id="575e5-104">Mit Abschluss Vorgängen kann eine Anwendung festlegen, wie eine Sitzung behandelt werden soll, wenn Faktoren wie z. b. ein ausgelasteter Ziel eine normale Verbindung verhindern.</span><span class="sxs-lookup"><span data-stu-id="575e5-104">Completion operations allow an application to specify how it wants to handle a session when factors such as a busy destination prevent normal connection.</span></span>

<span data-ttu-id="575e5-105">Die [linecallcomplmode- \_ Konstanten](./linecallcomplmode--constants.md) definieren die möglichen Optionen, die eine Anwendung möglicherweise besitzt, je nach den Funktionen des Dienstanbieters.</span><span class="sxs-lookup"><span data-stu-id="575e5-105">The [LINECALLCOMPLMODE\_ Constants](./linecallcomplmode--constants.md) define the possible options an application might have, depending on service provider capabilities.</span></span>

<span data-ttu-id="575e5-106">Für eine bestimmte Adresse können zu einem beliebigen Zeitpunkt mehrere Anforderungen zum Abrufen von Anforderungen ausgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="575e5-106">Multiple call completion requests might be outstanding for a given address at any one time.</span></span> <span data-ttu-id="575e5-107">Zum Identifizieren einzelner Anforderungen gibt die Implementierung einen [Vervollständigungs Bezeichner](completion-id-ovr.md)zurück.</span><span class="sxs-lookup"><span data-stu-id="575e5-107">To identify individual requests, the implementation returns a [completion identifier](completion-id-ovr.md).</span></span> <span data-ttu-id="575e5-108">Wenn eine Anforderung zum Abschließen einer Anforderung in Bearbeitung abgebrochen wird, wird dieser Bezeichner für den Bezeichner verwendet</span><span class="sxs-lookup"><span data-stu-id="575e5-108">Canceling a call completion request in progress also uses this call completion identifier.</span></span>

<span data-ttu-id="575e5-109">**TAPI 2. x:** Siehe [**linecompletecall,**](/windows/win32/api/tapi/nf-tapi-linecompletecall) [**lineuncompletecall.**](/windows/win32/api/tapi/nf-tapi-lineuncompletecall)</span><span class="sxs-lookup"><span data-stu-id="575e5-109">**TAPI 2.x:** See [**lineCompleteCall**](/windows/win32/api/tapi/nf-tapi-linecompletecall), [**lineUncompleteCall**](/windows/win32/api/tapi/nf-tapi-lineuncompletecall).</span></span>

<span data-ttu-id="575e5-110">**TAPI 3. x:** Weitere Informationen finden Sie unter [**itbasiccallcontrol:: Connect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-connect), [**itbasiccallcontrol::D isconnect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-disconnect).</span><span class="sxs-lookup"><span data-stu-id="575e5-110">**TAPI 3.x:** See [**ITBasicCallControl::Connect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-connect), [**ITBasicCallControl::Disconnect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-disconnect).</span></span>

 

 
