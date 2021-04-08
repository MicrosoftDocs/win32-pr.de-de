---
description: Gibt den angeforderten Frame aus einer geladenen Erfassung zurück.
ms.assetid: efd1cff5-a3a1-4910-b003-25b6e10dad6e
title: Expertgetframe-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExpertGetFrame
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 2bd02bde8caf157b6df6b1dd772a8f7574df0e57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862020"
---
# <a name="expertgetframe-function"></a><span data-ttu-id="9410f-103">Expertgetframe-Funktion</span><span class="sxs-lookup"><span data-stu-id="9410f-103">ExpertGetFrame function</span></span>

<span data-ttu-id="9410f-104">Die Funktion " **expertgetframe** " gibt den angeforderten Frame aus einer geladenen Erfassung zurück.</span><span class="sxs-lookup"><span data-stu-id="9410f-104">The **ExpertGetFrame** function returns the requested frame from a loaded capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="9410f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9410f-105">Syntax</span></span>


```C++
DWORD WINAPI ExpertGetFrame(
  _In_  HEXPERTKEY              hExpertKey,
  _In_  DWORD                   Direction,
  _In_  DWORD                   RequestFlags,
  _In_  DWORD                   RequestedFrameNumber,
  _In_  HFILTER                 hFilter,
  _Out_ LPEXPERTFRAMEDESCRIPTOR pEFrameDescriptor
);
```



## <a name="parameters"></a><span data-ttu-id="9410f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9410f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9410f-107">*hexpertkey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9410f-107">*hExpertKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9410f-108">Ein eindeutiger Experte Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="9410f-108">A unique expert identifier.</span></span> <span data-ttu-id="9410f-109">Netzwerkmonitor übergibt den *hexpertkey* -Bezeichner an den Experten, wenn er die [**Run**](run.md) -Funktion aufruft.</span><span class="sxs-lookup"><span data-stu-id="9410f-109">Network Monitor passes the *hExpertKey* identifier to the expert when it calls the [**Run**](run.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="9410f-110">*Richtung* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9410f-110">*Direction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9410f-111">Ein Wert, der angibt, wie Netzwerkmonitor nach dem Frame sucht.</span><span class="sxs-lookup"><span data-stu-id="9410f-111">A value that identifies how Network Monitor searches for the frame.</span></span>



| <span data-ttu-id="9410f-112">Wert</span><span class="sxs-lookup"><span data-stu-id="9410f-112">Value</span></span>                                                                                                                                                                                         | <span data-ttu-id="9410f-113">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="9410f-113">Meaning</span></span>                                |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="GET_SPECIFIED_FRAME"></span><span id="get_specified_frame"></span><dl> <span data-ttu-id="9410f-114"><dt>**\_angegebenen \_ Frame erhalten**</dt></span><span class="sxs-lookup"><span data-stu-id="9410f-114"><dt>**GET\_SPECIFIED\_FRAME**</dt></span></span> </dl>              | <span data-ttu-id="9410f-115">Gibt den angeforderten Frame zurück.</span><span class="sxs-lookup"><span data-stu-id="9410f-115">Return the requested frame.</span></span><br/> |
| <span id="GET_FRAME_NEXT_FORWARD"></span><span id="get_frame_next_forward"></span><dl> <span data-ttu-id="9410f-116"><dt>**\_Frame \_ weiter \_ leiten**</dt></span><span class="sxs-lookup"><span data-stu-id="9410f-116"><dt>**GET\_FRAME\_NEXT\_FORWARD**</dt></span></span> </dl>    | <span data-ttu-id="9410f-117">Gibt den nächsten Frame zurück.</span><span class="sxs-lookup"><span data-stu-id="9410f-117">Return the next frame.</span></span><br/>      |
| <span id="GET_FRAME_NEXT_BACKWARD"></span><span id="get_frame_next_backward"></span><dl> <span data-ttu-id="9410f-118"><dt>**\_Frame \_ nächste \_ rückwärts**</dt></span><span class="sxs-lookup"><span data-stu-id="9410f-118"><dt>**GET\_FRAME\_NEXT\_BACKWARD**</dt></span></span> </dl> | <span data-ttu-id="9410f-119">Gibt den vorherigen Frame zurück.</span><span class="sxs-lookup"><span data-stu-id="9410f-119">Return the previous frame.</span></span><br/>  |



 

</dd> <dt>

<span data-ttu-id="9410f-120">*Requestflags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9410f-120">*RequestFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9410f-121">Die Flags, die angeben, wie Netzwerkmonitor die Anforderung verarbeiten soll.</span><span class="sxs-lookup"><span data-stu-id="9410f-121">The flags that specify how Network Monitor should handle the request.</span></span> <span data-ttu-id="9410f-122">Geben Sie mindestens eines der folgenden Flags an.</span><span class="sxs-lookup"><span data-stu-id="9410f-122">Specify one or more of the following flags.</span></span>



| <span data-ttu-id="9410f-123">Wert</span><span class="sxs-lookup"><span data-stu-id="9410f-123">Value</span></span>                                                                                                                                                                                             | <span data-ttu-id="9410f-124">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="9410f-124">Meaning</span></span>                                                                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FLAGS_DEFER_TO_UI_FILTER"></span><span id="flags_defer_to_ui_filter"></span><dl> <span data-ttu-id="9410f-125"><dt>**Flags \_ werden \_ an \_ UI- \_ Filter zurück verschoben**</dt></span><span class="sxs-lookup"><span data-stu-id="9410f-125"><dt>**FLAGS\_DEFER\_TO\_UI\_FILTER**</dt></span></span> </dl> | <span data-ttu-id="9410f-126">Bevor Sie den Anzeige Filter Parameter des in *hfilter* angegebenen Experten anwenden, wenden Sie den Anzeige Filter an, den Netzwerkmonitor verwendet, wenn der Experte startet.</span><span class="sxs-lookup"><span data-stu-id="9410f-126">Before applying the display filter parameter of the expert which is specified in *hFilter*, apply the display filter that Network Monitor is using when the expert starts.</span></span><br/>                                                                                                                              |
| <span id="FLAGS_ATTACH_PROPERTIES"></span><span id="flags_attach_properties"></span><dl> <span data-ttu-id="9410f-127"><dt>**Flags \_ - \_ Eigenschaften anfügen**</dt></span><span class="sxs-lookup"><span data-stu-id="9410f-127"><dt>**FLAGS\_ATTACH\_PROPERTIES**</dt></span></span> </dl>      | <span data-ttu-id="9410f-128">Die Eigenschaften, die alle Protokoll Parser mit den beanspruchten Abschnitten dieses Frames suchen, werden an den Frame angefügt.</span><span class="sxs-lookup"><span data-stu-id="9410f-128">The properties that all protocol parsers find with claimed sections of this frame are attached to the frame.</span></span> <span data-ttu-id="9410f-129">Wenn das-Flag nicht festgelegt ist, wird das **lppropertytable** -Feld der Expertenstruktur von " [**expertenframedescriptor**](expertframedescriptor.md) " (von " **Peer framedescriptor**" zurückgegeben) auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="9410f-129">If the flag is not set, the **lpPropertyTable** field of the [**EXPERTFRAMEDESCRIPTOR**](expertframedescriptor.md) structure (returned by **pEFrameDescriptor**) will be set to **NULL**.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="9410f-130">*Requestedframenreber* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9410f-130">*RequestedFrameNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9410f-131">Die Nummer des angeforderten Frames.</span><span class="sxs-lookup"><span data-stu-id="9410f-131">The number of the requested frame.</span></span>

</dd> <dt>

<span data-ttu-id="9410f-132">*hfilter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9410f-132">*hFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9410f-133">Ein Handle für den expertenanzeigefilter.</span><span class="sxs-lookup"><span data-stu-id="9410f-133">A handle to the expert display filter.</span></span> <span data-ttu-id="9410f-134">Wenn der Experte keinen Anzeige Filter hat, legen Sie den-Parameter auf **null** fest.</span><span class="sxs-lookup"><span data-stu-id="9410f-134">If the expert does not have a display filter, set the parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="9410f-135">*Peer Frame Deskriptor* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="9410f-135">*pEFrameDescriptor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9410f-136">Die Expertenstruktur von " [**expertenframedescriptor**](expertframedescriptor.md) ", die den Frame bei der Rückgabe beschreibt.</span><span class="sxs-lookup"><span data-stu-id="9410f-136">The [**EXPERTFRAMEDESCRIPTOR**](expertframedescriptor.md) structure that, on return, describes the frame.</span></span> <span data-ttu-id="9410f-137">Der Experte muss den von dieser Struktur verwendeten Arbeitsspeicher zuordnen und freigeben.</span><span class="sxs-lookup"><span data-stu-id="9410f-137">The expert must allocate and free the memory that this structure uses.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9410f-138">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9410f-138">Return value</span></span>

<span data-ttu-id="9410f-139">Wenn die Funktion erfolgreich ist, ist der Rückgabewert nmerr \_ Success.</span><span class="sxs-lookup"><span data-stu-id="9410f-139">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="9410f-140">Wenn die Funktion nicht erfolgreich ist, gibt der Rückgabewert den Grund für den Fehler an.</span><span class="sxs-lookup"><span data-stu-id="9410f-140">If the function is unsuccessful, the return value indicates the reason for the failure.</span></span> <span data-ttu-id="9410f-141">Wenn der Rückgabewert nmerr- \_ Experte \_ beendet ist, muss der Experte sofort bereinigen und zurückgeben. der Benutzer hat den expertenlauf abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="9410f-141">If the return value is NMERR\_EXPERT\_TERMINATE, the expert must immediately clean up and return; the user has aborted the expert run.</span></span>

## <a name="remarks"></a><span data-ttu-id="9410f-142">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9410f-142">Remarks</span></span>

<span data-ttu-id="9410f-143">Wenn Sie Flags \_ \_ Eigenschaften anfügen festlegen, benötigt der-Befehl mehr Ressourcen, als wenn Sie das-Flag nicht festlegen.</span><span class="sxs-lookup"><span data-stu-id="9410f-143">If you set FLAGS\_ATTACH\_PROPERTIES, the call requires more resources than if you do not set the flag.</span></span> <span data-ttu-id="9410f-144">Wenn das Flag nicht festgelegt ist, zeigt ein Zeiger auf den rohrahmen und auf Daten über den Frame.</span><span class="sxs-lookup"><span data-stu-id="9410f-144">If the flag is not set, a pointer points to the raw frame and to data about the frame.</span></span> <span data-ttu-id="9410f-145">Wenn dieses Flag festgelegt ist, fügt Netzwerkmonitor alle Eigenschaften an den Frame an, indem jeder Parser aufgerufen wird, der einen Teil des Frames beansprucht.</span><span class="sxs-lookup"><span data-stu-id="9410f-145">If this flag is set, Network Monitor attaches all properties to the frame by calling every parser that claims a portion of the frame.</span></span> <span data-ttu-id="9410f-146">Dies kann ein langsamer Prozess sein.</span><span class="sxs-lookup"><span data-stu-id="9410f-146">This can be a slow process.</span></span>

<span data-ttu-id="9410f-147">Experten sollten das Flag zum Anfügen von Flags nicht festlegen, \_ \_ es sei denn, die Experten benötigen die Eigenschaften, die Parser an den Frame anfügen.</span><span class="sxs-lookup"><span data-stu-id="9410f-147">Experts should not set the FLAGS\_ATTACH\_PROPERTIES flag unless the experts require the properties that parsers attach to the frame.</span></span> <span data-ttu-id="9410f-148">Wenn möglich, sollten Experten die Funktion " **expertgetframe** " ohne das-Flag aufrufen und dann die erforderlichen Daten direkt aus dem Frame extrahieren.</span><span class="sxs-lookup"><span data-stu-id="9410f-148">If possible, experts should call the **ExpertGetFrame** function without the flag, and then extract the required data directly from the frame.</span></span>

<span data-ttu-id="9410f-149">Wenn der Experte " **expertengetframe** " aufruft, ohne das Flag "Flags" \_ Anfügen zu \_ müssen, und die diesem Frame zugeordneten Eigenschaften erfordert (z. b. ein Ereignis), ruft der Experte " **expertgetframe** " mit den gleichen Parametern auf, mit Ausnahme der folgenden:</span><span class="sxs-lookup"><span data-stu-id="9410f-149">If the expert calls **ExpertGetFrame** without the FLAGS\_ATTACH\_PROPERTIES flag and requires the properties associated with that frame (an event, for example), the expert calls **ExpertGetFrame** with the same parameters except for the following:</span></span>

``` syntax
Direction = EXPERT_GET_SPECIFIED_FRAME;
RequestFlags &= (~EXPERT_DEFER_TO_UI_FILTER) | EXPERT_ATTACH_PROPERTIES;
RequestedFrameNumber= (The actual frame number you want);
hFilter = NULL;
pEFrameDescriptor = (The same one as last time);
```

<span data-ttu-id="9410f-150">Mit dem vorangehenden Code wird sichergestellt, dass der Experte den erforderlichen Frame erhält, ohne dass der Filter Code erneut aufgerufen werden muss.</span><span class="sxs-lookup"><span data-stu-id="9410f-150">Using the preceding code ensures that the expert gets the required frame without having to call filter code again.</span></span>

<span data-ttu-id="9410f-151">Sie können den *hfilter* -Parameter als **LPVOID** festlegen.</span><span class="sxs-lookup"><span data-stu-id="9410f-151">You can set the *hFilter* parameter as an **LPVOID**.</span></span> <span data-ttu-id="9410f-152">Wenn Sie vorhanden ist, übergibt der zurückgegebene Frame diesen Filter.</span><span class="sxs-lookup"><span data-stu-id="9410f-152">If it exists, the returned frame passes this filter.</span></span> <span data-ttu-id="9410f-153">Wenn der Experte keinen Anzeige Filter hat, der an die Funktion übergeben werden soll (wenn *hfilter* **null** ist), wird der zurückgegebene Frame nicht gefiltert.</span><span class="sxs-lookup"><span data-stu-id="9410f-153">If the expert does not have a display filter to pass to the function (if *hFilter* is **NULL** ), then the frame returned is not filtered.</span></span>

<span data-ttu-id="9410f-154">Die Funktion " **expertgetframe** " kann nur von Experten aufgerufen werden, die die Exportfunktion " [**Run**](run.md) " oder " [**configure**](configure.md) " implementieren.</span><span class="sxs-lookup"><span data-stu-id="9410f-154">The **ExpertGetFrame** function can only be called by experts that implement the [**Run**](run.md) or [**Configure**](configure.md) export function.</span></span>

## <a name="requirements"></a><span data-ttu-id="9410f-155">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9410f-155">Requirements</span></span>



| <span data-ttu-id="9410f-156">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9410f-156">Requirement</span></span> | <span data-ttu-id="9410f-157">Wert</span><span class="sxs-lookup"><span data-stu-id="9410f-157">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="9410f-158">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9410f-158">Minimum supported client</span></span><br/> | <span data-ttu-id="9410f-159">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9410f-159">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="9410f-160">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9410f-160">Minimum supported server</span></span><br/> | <span data-ttu-id="9410f-161">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9410f-161">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="9410f-162">Header</span><span class="sxs-lookup"><span data-stu-id="9410f-162">Header</span></span><br/>                   | <dl> <span data-ttu-id="9410f-163"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="9410f-163"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="9410f-164">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="9410f-164">Library</span></span><br/>                  | <dl> <span data-ttu-id="9410f-165"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9410f-165"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="9410f-166">DLL</span><span class="sxs-lookup"><span data-stu-id="9410f-166">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9410f-167"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9410f-167"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




