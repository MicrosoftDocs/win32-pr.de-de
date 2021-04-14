---
description: Die verbundene Identifizierung identifiziert die Partei, mit der tatsächlich eine Verbindung hergestellt wurde. Dies kann sich von der aufgerufenen Identifikation unterscheiden, wenn der Aufruf umgeleitet wurde.
ms.assetid: 3f9ba728-8e78-4f1f-a0c1-76799fd62c9d
title: Verbundene Identifizierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59fdb2f11b27bf9281b381170aa0d5b5ab027088
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104350568"
---
# <a name="connected-identification"></a><span data-ttu-id="2db90-104">Verbundene Identifizierung</span><span class="sxs-lookup"><span data-stu-id="2db90-104">Connected Identification</span></span>

<span data-ttu-id="2db90-105">Die verbundene Identifizierung identifiziert die Partei, mit der tatsächlich eine Verbindung hergestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="2db90-105">The connected identification identifies the party that was actually connected to.</span></span> <span data-ttu-id="2db90-106">Dies kann sich von der aufgerufenen Identifikation unterscheiden, wenn der Aufruf umgeleitet wurde.</span><span class="sxs-lookup"><span data-stu-id="2db90-106">This may be different from the called identification if the call was diverted.</span></span>

<span data-ttu-id="2db90-107">Nicht alle Dienstanbieter unterstützen die Verwendung dieser Informationen.</span><span class="sxs-lookup"><span data-stu-id="2db90-107">Not all service providers support use of this information.</span></span>

<span data-ttu-id="2db90-108">**TAPI 2. x:** Weitere Informationen finden Sie unter [**linegetcallinfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (**dwconnectedidflags**, **dwconnectedidsize**, **dwconnectedidoffset**, **dwconnectedidnamesize** und **dwconnectedidnameoffset** Members von *lpcallinfo*).</span><span class="sxs-lookup"><span data-stu-id="2db90-108">**TAPI 2.x:** See [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (**dwConnectedIDFlags**, **dwConnectedIDSize**, **dwConnectedIDOffset**, **dwConnectedIDNameSize**, and **dwConnectedIDNameOffset** members of *lpCallInfo*).</span></span>

<span data-ttu-id="2db90-109">**TAPI 3. x:** Siehe [**itcallinfo:: get \_ callinfostring**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfostring) (**cil \_ connectedidname** -Member von [**CallInfo \_ String**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_string)).</span><span class="sxs-lookup"><span data-stu-id="2db90-109">**TAPI 3.x:** See [**ITCallInfo::get\_CallInfoString**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfostring) (**CIL\_CONNECTEDIDNAME** member of [**CALLINFO\_STRING**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_string)).</span></span>

 

 
