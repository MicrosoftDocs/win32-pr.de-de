---
description: Beschreibt das Ergebnis, das Sie optional festlegen können, nachdem eine Anzeige Senke-notalisierung in der WFD- \_ \_ \_ Benachrichtigungs \_ Rückruffunktion angezeigt wird.
ms.assetid: 6ED04294-2ED9-455B-9274-8C3DB06D4B21
title: WFD_DISPLAY_SINK_NOTIFICATION_RESULT-Struktur (WF-Sink. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WFD_DISPLAY_SINK_NOTIFICATION
api_type:
- HeaderDef
api_location:
- wfdsink.h
ms.openlocfilehash: dc23416d4d13284862aea652dd71909e71879afc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362707"
---
# <a name="wfd_display_sink_notification_result-structure"></a><span data-ttu-id="36ad3-103">WFD- \_ Anzeige \_ Senke- \_ Benachrichtigungs \_ Ergebnis Struktur</span><span class="sxs-lookup"><span data-stu-id="36ad3-103">WFD\_DISPLAY\_SINK\_NOTIFICATION\_RESULT structure</span></span>

<span data-ttu-id="36ad3-104">In der **WFD- \_ \_ \_ Benachrichtigungs \_ Ergebnis** Struktur wird das Ergebnis beschrieben, das Sie optional festlegen können, nachdem Sie die Anzeige Senke-notalisierung in der [**WFD- \_ \_ \_ Benachrichtigungs \_ Rückruf**](wfd-display-sink-notification-callback.md) Funktion verarbeitet haben.</span><span class="sxs-lookup"><span data-stu-id="36ad3-104">The **WFD\_DISPLAY\_SINK\_NOTIFICATION\_RESULT** structure describes the result that you can optionally set after processing a display sink notfication in the [**WFD\_DISPLAY\_SINK\_NOTIFICATION\_CALLBACK**](wfd-display-sink-notification-callback.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="36ad3-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="36ad3-105">Syntax</span></span>


```C++
typedef struct _WFD_DISPLAY_SINK_NOTIFICATION {
  WFD_DISPLAY_SINK_OBJECT_HEADER     Header;
  WFD_DISPLAY_SINK_NOTIFICATION_TYPE type;
  union {
    struct {
      DOT11_WPS_CONFIG_METHOD ConfigMethod;
      UINT32                  uPassKeyLength;
      WCHAR                   Passkey[WFD_SINK_WPS_INFO_MAX_PASSKEY_LENGTH];
    } ProvisioningData;
    struct {
      PWSTR strProfile;
    } ReconnectData;
  };
} WFD_DISPLAY_SINK_NOTIFICATION, *PWFD_DISPLAY_SINK_NOTIFICATION;
```



## <a name="members"></a><span data-ttu-id="36ad3-106">Member</span><span class="sxs-lookup"><span data-stu-id="36ad3-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="36ad3-107">**Header**</span><span class="sxs-lookup"><span data-stu-id="36ad3-107">**Header**</span></span>
</dt> <dd>

<span data-ttu-id="36ad3-108">Ein [**WFD- \_ Anzeige- \_ \_ senkobjektheader \_**](wfd-display-sink-object-header.md) , der die im Benachrichtigungs Ergebnis enthaltenen Daten beschreibt.</span><span class="sxs-lookup"><span data-stu-id="36ad3-108">A [**WFD\_DISPLAY\_SINK\_OBJECT\_HEADER**](wfd-display-sink-object-header.md) that describes the data included in the notification result.</span></span>

</dd> <dt>

<span data-ttu-id="36ad3-109">**type**</span><span class="sxs-lookup"><span data-stu-id="36ad3-109">**type**</span></span>
</dt> <dd>

<span data-ttu-id="36ad3-110">Ein [**WFD \_ - \_ \_ \_ Benachrichtigungstyp**](wfd-display-sink-notification-type.md) Wert, der den Typ des Benachrichtigungs Ergebnisses angibt.</span><span class="sxs-lookup"><span data-stu-id="36ad3-110">A [**WFD\_DISPLAY\_SINK\_NOTIFICATION\_TYPE**](wfd-display-sink-notification-type.md) value that indicates the type of the notification result.</span></span> <span data-ttu-id="36ad3-111">Dieser Parameter bestimmt auch, welche Informationen in der Union unten verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="36ad3-111">This parameter also determines which Info to use in the union below.</span></span>

</dd> <dt>

<span data-ttu-id="36ad3-112">**Provisioningdata**</span><span class="sxs-lookup"><span data-stu-id="36ad3-112">**ProvisioningData**</span></span>
</dt> <dd>

<span data-ttu-id="36ad3-113">Informationen zum Ergebnis einer Bereitstellungs Anforderung.</span><span class="sxs-lookup"><span data-stu-id="36ad3-113">Info about the result of a provisioning request.</span></span> <span data-ttu-id="36ad3-114">Verwenden Sie diese Einstellung, wenn der *Typ* den Wert **provisioningrequestnotification** hat.</span><span class="sxs-lookup"><span data-stu-id="36ad3-114">Use this if *type* has the value **ProvisioningRequestNotification**.</span></span>

<dl> <dt>

<span data-ttu-id="36ad3-115">**Configmethod**</span><span class="sxs-lookup"><span data-stu-id="36ad3-115">**ConfigMethod**</span></span>
</dt> <dd>

<span data-ttu-id="36ad3-116">Die Methode für die Anzeige der Benutzeroberfläche für die interaktive Annahme.</span><span class="sxs-lookup"><span data-stu-id="36ad3-116">The method for showing UI for interactive acceptance.</span></span>

</dd> <dt>

<span data-ttu-id="36ad3-117">**upasskeylength**</span><span class="sxs-lookup"><span data-stu-id="36ad3-117">**uPassKeyLength**</span></span>
</dt> <dd>

<span data-ttu-id="36ad3-118">Die Anzahl der breit Zeichen in einem *Passkey*, wobei kein NULL-Terminator gezählt wird.</span><span class="sxs-lookup"><span data-stu-id="36ad3-118">The number of wide characters in *Passkey*, not counting any NULL-terminator.</span></span>

</dd> <dt>

<span data-ttu-id="36ad3-119">**Hauptschlüssel**</span><span class="sxs-lookup"><span data-stu-id="36ad3-119">**Passkey**</span></span>
</dt> <dd>

<span data-ttu-id="36ad3-120">Enthält den Pass-Key als Array von breit Zeichen.</span><span class="sxs-lookup"><span data-stu-id="36ad3-120">Contains the pass key as an array of wide characters.</span></span> <span data-ttu-id="36ad3-121">\_ \_ Die maximale Passkey-Länge der WFD-Sink-WPS- \_ Informationen \_ \_ \_ ist als Wert (8) definiert.</span><span class="sxs-lookup"><span data-stu-id="36ad3-121">WFD\_SINK\_WPS\_INFO\_MAX\_PASSKEY\_LENGTH is defined as the value (8).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="36ad3-122">**Reconnectdata**</span><span class="sxs-lookup"><span data-stu-id="36ad3-122">**ReconnectData**</span></span>
</dt> <dd>

<span data-ttu-id="36ad3-123">Informationen zum Ergebnis einer Anforderung zum erneuten Verbinden.</span><span class="sxs-lookup"><span data-stu-id="36ad3-123">Info about the result of a reconnect request.</span></span> <span data-ttu-id="36ad3-124">Verwenden Sie diese Eigenschaft, wenn der *Typ* den Wert **reconnectrequestnotification** hat.</span><span class="sxs-lookup"><span data-stu-id="36ad3-124">Use this if *type* has the value **ReconnectRequestNotification**.</span></span>

<dl> <dt>

<span data-ttu-id="36ad3-125">**"Trend Profil"**</span><span class="sxs-lookup"><span data-stu-id="36ad3-125">**strProfile**</span></span>
</dt> <dd>

<span data-ttu-id="36ad3-126">Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die das Profil beschreibt.</span><span class="sxs-lookup"><span data-stu-id="36ad3-126">A pointer to a NULL-terminated string describing the profile.</span></span>

</dd> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="36ad3-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="36ad3-127">Requirements</span></span>



| <span data-ttu-id="36ad3-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="36ad3-128">Requirement</span></span> | <span data-ttu-id="36ad3-129">Wert</span><span class="sxs-lookup"><span data-stu-id="36ad3-129">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="36ad3-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="36ad3-130">Minimum supported client</span></span><br/> | <span data-ttu-id="36ad3-131">\[Nur Desktop-Apps Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="36ad3-131">Windows 8.1 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="36ad3-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="36ad3-132">Minimum supported server</span></span><br/> | <span data-ttu-id="36ad3-133">Nur Windows Server 2012 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="36ad3-133">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="36ad3-134">Header</span><span class="sxs-lookup"><span data-stu-id="36ad3-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="36ad3-135"><dt>WF-Senke. h</dt></span><span class="sxs-lookup"><span data-stu-id="36ad3-135"><dt>Wfdsink.h</dt></span></span> </dl> |



 

 




