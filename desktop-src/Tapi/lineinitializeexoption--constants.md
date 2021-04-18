---
description: Die lineinitializeexoption- \_ Konstanten geben an, welcher Ereignis Benachrichtigungs Mechanismus beim Initialisieren einer Sitzung verwendet werden soll.
ms.assetid: 77674a45-7133-4518-af47-a9d58392b80b
title: LINEINITIALIZEEXOPTION_ Konstanten (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86543c367877d74562cc0af13261881b7df19982
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371460"
---
# <a name="lineinitializeexoption_-constants"></a><span data-ttu-id="a1b29-103">Lineinitializeexoption- \_ Konstanten</span><span class="sxs-lookup"><span data-stu-id="a1b29-103">LINEINITIALIZEEXOPTION\_ Constants</span></span>

<span data-ttu-id="a1b29-104">Die **lineinitializeexoption \_** -Konstanten geben an, welcher Ereignis Benachrichtigungs Mechanismus beim Initialisieren einer Sitzung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a1b29-104">The **LINEINITIALIZEEXOPTION\_** constants specify which event notification mechanism to use when initializing a session.</span></span>

<dl> <dt>

<span data-ttu-id="a1b29-105"><span id="LINEINITIALIZEEXOPTION_CALLHUBTRACKING"></span><span id="lineinitializeexoption_callhubtracking"></span>**lineinitializeexoption \_ callhubtracking**</span><span class="sxs-lookup"><span data-stu-id="a1b29-105"><span id="LINEINITIALIZEEXOPTION_CALLHUBTRACKING"></span><span id="lineinitializeexoption_callhubtracking"></span>**LINEINITIALIZEEXOPTION\_CALLHUBTRACKING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a1b29-106">Die Anwendung möchte den Ereignis Benachrichtigungs Mechanismus für den callhub-Nachverfolgung verwenden.</span><span class="sxs-lookup"><span data-stu-id="a1b29-106">The application desires to use the call hub tracking event notification mechanism.</span></span> <span data-ttu-id="a1b29-107">Diese Konstante ist nur für Anwendungen verfügbar, die eine TAPI-Version von 3,0 oder höher aushandeln.</span><span class="sxs-lookup"><span data-stu-id="a1b29-107">This constant is exposed only to applications that negotiate a TAPI version of 3.0 or higher.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a1b29-108"><span id="LINEINITIALIZEEXOPTION_USECOMPLETIONPORT"></span><span id="lineinitializeexoption_usecompletionport"></span>**lineinitializeexoption \_ usecompletionport**</span><span class="sxs-lookup"><span data-stu-id="a1b29-108"><span id="LINEINITIALIZEEXOPTION_USECOMPLETIONPORT"></span><span id="lineinitializeexoption_usecompletionport"></span>**LINEINITIALIZEEXOPTION\_USECOMPLETIONPORT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a1b29-109">Die Anwendung möchte den Ereignis Benachrichtigungs Mechanismus für den Abschluss Port verwenden.</span><span class="sxs-lookup"><span data-stu-id="a1b29-109">The application desires to use the Completion Port event notification mechanism.</span></span> <span data-ttu-id="a1b29-110">Dieses Flag ist nur für Anwendungen verfügbar, die eine TAPI-Version von 2,0 oder höher aushandeln.</span><span class="sxs-lookup"><span data-stu-id="a1b29-110">This flag is exposed only to applications that negotiate a TAPI version of 2.0 or higher.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a1b29-111"><span id="LINEINITIALIZEEXOPTION_USEEVENT"></span><span id="lineinitializeexoption_useevent"></span>**lineinitializeexoption \_ useevent**</span><span class="sxs-lookup"><span data-stu-id="a1b29-111"><span id="LINEINITIALIZEEXOPTION_USEEVENT"></span><span id="lineinitializeexoption_useevent"></span>**LINEINITIALIZEEXOPTION\_USEEVENT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a1b29-112">Die Anwendung möchte den Ereignis Benachrichtigungs Mechanismus Ereignishandler verwenden.</span><span class="sxs-lookup"><span data-stu-id="a1b29-112">The application desires to use the Event Handle event notification mechanism.</span></span> <span data-ttu-id="a1b29-113">Dieses Flag ist nur für Anwendungen verfügbar, die eine TAPI-Version von 2,0 oder höher aushandeln.</span><span class="sxs-lookup"><span data-stu-id="a1b29-113">This flag is exposed only to applications that negotiate a TAPI version of 2.0 or higher.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a1b29-114"><span id="LINEINITIALIZEEXOPTION_USEHIDDENWINDOW"></span><span id="lineinitializeexoption_usehiddenwindow"></span>**lineinitializeexoption \_ usehiddenwindow**</span><span class="sxs-lookup"><span data-stu-id="a1b29-114"><span id="LINEINITIALIZEEXOPTION_USEHIDDENWINDOW"></span><span id="lineinitializeexoption_usehiddenwindow"></span>**LINEINITIALIZEEXOPTION\_USEHIDDENWINDOW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a1b29-115">Die Anwendung möchte den Ereignis Benachrichtigungs Mechanismus für ausgeblendete Fenster verwenden.</span><span class="sxs-lookup"><span data-stu-id="a1b29-115">The application desires to use the Hidden Window event notification mechanism.</span></span> <span data-ttu-id="a1b29-116">Dieses Flag ist nur für Anwendungen verfügbar, die eine TAPI-Version von 2,0 oder höher aushandeln.</span><span class="sxs-lookup"><span data-stu-id="a1b29-116">This flag is exposed only to applications that negotiate a TAPI version of 2.0 or higher.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a1b29-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a1b29-117">Remarks</span></span>

<span data-ttu-id="a1b29-118">Weitere Informationen zum Betrieb dieser Optionen finden Sie unter [**lineinitializeex**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa) .</span><span class="sxs-lookup"><span data-stu-id="a1b29-118">See [**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa) for further details on the operation of these options.</span></span>

## <a name="requirements"></a><span data-ttu-id="a1b29-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a1b29-119">Requirements</span></span>



| <span data-ttu-id="a1b29-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a1b29-120">Requirement</span></span> | <span data-ttu-id="a1b29-121">Wert</span><span class="sxs-lookup"><span data-stu-id="a1b29-121">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="a1b29-122">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="a1b29-122">TAPI version</span></span><br/> | <span data-ttu-id="a1b29-123">Erfordert TAPI 2,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="a1b29-123">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="a1b29-124">Header</span><span class="sxs-lookup"><span data-stu-id="a1b29-124">Header</span></span><br/>       | <dl> <span data-ttu-id="a1b29-125"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="a1b29-125"><dt>Tapi.h</dt></span></span> </dl> |



 

 




