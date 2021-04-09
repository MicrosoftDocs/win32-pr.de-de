---
description: Erstellt ein Kontext Objekt, das das angegebene Tablet-Gerät beschreibt.
ms.assetid: 76f48485-a958-4457-9b87-73de73fa671e
title: 'ITablet:: kreatecontext-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet.CreateContext
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 9f1214f7f9e429b5f9b5b9614c2ccfc7fd1800b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868284"
---
# <a name="itabletcreatecontext-method"></a><span data-ttu-id="719d0-103">ITablet:: kreatecontext-Methode</span><span class="sxs-lookup"><span data-stu-id="719d0-103">ITablet::CreateContext method</span></span>

<span data-ttu-id="719d0-104">Erstellt ein Kontext Objekt, das das angegebene Tablet-Gerät beschreibt.</span><span class="sxs-lookup"><span data-stu-id="719d0-104">Creates a context object that describes the specified tablet device.</span></span>

## <a name="syntax"></a><span data-ttu-id="719d0-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="719d0-105">Syntax</span></span>


```C++
HRESULT CreateContext(
  [in]      HWND                    hWnd,
  [in]      RECT                    *prcInput,
  [in]      DWORD                   dwOptions,
  [in]      TABLET_CONTEXT_SETTINGS *pTCS,
  [in]      CONTEXT_ENABLE_TYPE     cet,
  [out]     ITabletContext          **ppCtx,
  [in, out] TABLET_CONTEXT_ID       *pTcid,
  [in, out] PACKET_DESCRIPTION      **ppPD,
  [in]      ITabletEventSink        *pSink
);
```



## <a name="parameters"></a><span data-ttu-id="719d0-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="719d0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="719d0-107">*HWND* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="719d0-107">*hWnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="719d0-108">Das Fenster, an das der Tablet-Kontext angefügt wird.</span><span class="sxs-lookup"><span data-stu-id="719d0-108">The window to which the tablet context will be attached.</span></span>

</dd> <dt>

<span data-ttu-id="719d0-109">*prcinput* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="719d0-109">*prcInput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="719d0-110">\[in, eindeutig\]</span><span class="sxs-lookup"><span data-stu-id="719d0-110">\[in, unique\]</span></span>

<span data-ttu-id="719d0-111">Das frei Hand Eingabe Rechteck.</span><span class="sxs-lookup"><span data-stu-id="719d0-111">The ink input rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="719d0-112">*dwOptions* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="719d0-112">*dwOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="719d0-113">Flags, die Tablet-Kontextoptionen festlegen.</span><span class="sxs-lookup"><span data-stu-id="719d0-113">Flags that set tablet context options.</span></span>

</dd> <dt>

<span data-ttu-id="719d0-114">*PTCs* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="719d0-114">*pTCS* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="719d0-115">\[in, eindeutig\]</span><span class="sxs-lookup"><span data-stu-id="719d0-115">\[in, unique\]</span></span>

<span data-ttu-id="719d0-116">Ausführliche Informationen über den zu erstellenden Tablet-Kontext.</span><span class="sxs-lookup"><span data-stu-id="719d0-116">Detailed information about the tablet context to create.</span></span>

</dd> <dt>

<span data-ttu-id="719d0-117">*MEZ* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="719d0-117">*cet* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="719d0-118">Ein Wert, der Kontext Meldungen aktiviert oder deaktiviert, die an das Fenster gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="719d0-118">Value that enables or disables context messages being sent to the window.</span></span>

</dd> <dt>

<span data-ttu-id="719d0-119">*ppctx* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="719d0-119">*ppCtx* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="719d0-120">Ein Zeiger auf den neu erstellten Tablet-Kontext.</span><span class="sxs-lookup"><span data-stu-id="719d0-120">A pointer to the newly create tablet context.</span></span>

</dd> <dt>

<span data-ttu-id="719d0-121">*ptcid* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="719d0-121">*pTcid* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="719d0-122">Der Wert, der das Tablet eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="719d0-122">Value that uniquely identifies the tablet.</span></span>

</dd> <dt>

<span data-ttu-id="719d0-123">*pppd* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="719d0-123">*ppPD* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="719d0-124">Zeiger auf Informationen zu den Daten, die in den einzelnen Paketen enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="719d0-124">Pointer to information about what data is contained in each packet.</span></span>

</dd> <dt>

<span data-ttu-id="719d0-125">*psink* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="719d0-125">*pSink* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="719d0-126">Das [**itableteventsink**](itableteventsink.md) -Objekt, in das Benachrichtigungs Meldungen gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="719d0-126">The [**ITabletEventSink**](itableteventsink.md) object where notification messages will be sent.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="719d0-127">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="719d0-127">Return value</span></span>

<span data-ttu-id="719d0-128">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="719d0-128">This method can return one of these values.</span></span>



| <span data-ttu-id="719d0-129">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="719d0-129">Return code</span></span>                                                                            | <span data-ttu-id="719d0-130">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="719d0-130">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="719d0-131"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="719d0-131"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="719d0-132">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="719d0-132">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="719d0-133"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="719d0-133"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="719d0-134">Es ist ein unbekannter Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="719d0-134">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="719d0-135">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="719d0-135">Remarks</span></span>

<span data-ttu-id="719d0-136">In der Regel Ruft eine Anwendung die Standardwerte aus der [**iTablet:: getdefaultcontextsettings-Methode**](itablet-getdefaultcontextsettings.md)ab, ändert die Werte entsprechend Ihren Anforderungen und übergibt dann die geänderte Einstellungs Struktur an die **iTablet:: deecontext-Methode**.</span><span class="sxs-lookup"><span data-stu-id="719d0-136">Typically, an application obtains the default values from the [**ITablet::GetDefaultContextSettings Method**](itablet-getdefaultcontextsettings.md), modifies values to suit their needs, and then passes the modified settings structure to the **ITablet::CreateContext Method**.</span></span>

> [!Note]  
> <span data-ttu-id="719d0-137">Sie müssen die [**itableteventsink-Schnittstelle**](itableteventsink.md) implementieren, wenn Sie die **iTablet:: CreateContext-Methode** aufrufen.</span><span class="sxs-lookup"><span data-stu-id="719d0-137">You must implement the [**ITabletEventSink Interface**](itableteventsink.md) when calling the **ITablet::CreateContext Method**.</span></span>

 

<span data-ttu-id="719d0-138">Der *dwOptions* -Parameter ist ein Satz von Bitflags, die Kontextoptionen beschreiben.</span><span class="sxs-lookup"><span data-stu-id="719d0-138">The *dwOptions* parameter is a set of bit flags that describe context options.</span></span> <span data-ttu-id="719d0-139">In der folgenden Tabelle werden diese Flags beschrieben.</span><span class="sxs-lookup"><span data-stu-id="719d0-139">The following table describes these flags.</span></span>



| <span data-ttu-id="719d0-140">FlagName</span><span class="sxs-lookup"><span data-stu-id="719d0-140">Flag Name</span></span>                                | <span data-ttu-id="719d0-141">Wert</span><span class="sxs-lookup"><span data-stu-id="719d0-141">Value</span></span>                                                                                                                                                                                         | <span data-ttu-id="719d0-142">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="719d0-142">Description</span></span>                                                                                                                                                                                                                                                              |
|------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="719d0-143">TCXO- \_ Rand</span><span class="sxs-lookup"><span data-stu-id="719d0-143">TCXO\_MARGIN</span></span><br/>                  | <span data-ttu-id="719d0-144">0x00000001</span><span class="sxs-lookup"><span data-stu-id="719d0-144">0x00000001</span></span><br/>                                                                                                                                                                         | <span data-ttu-id="719d0-145">Gibt an, dass der Eingabe Kontext auf dem Tablet einen Rand hat.</span><span class="sxs-lookup"><span data-stu-id="719d0-145">Specifies that the input context on the tablet will have a margin.</span></span> <span data-ttu-id="719d0-146">Der Rand ist ein Bereich außerhalb des angegebenen Eingabe Bereichs, in dem Ereignisse dem Rand des Eingabe Bereichs zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="719d0-146">The margin is an area outside the specified input area where events will be mapped to the edge of the input area.</span></span> <span data-ttu-id="719d0-147">Diese Funktion erleichtert das Eingeben von Punkten am Rand des Kontexts.</span><span class="sxs-lookup"><span data-stu-id="719d0-147">This feature makes it easier to input points at the edge of the context.</span></span><br/> |
| <span data-ttu-id="719d0-148">TCXO- \_ prähook</span><span class="sxs-lookup"><span data-stu-id="719d0-148">TCXO\_PREHOOK</span></span><br/>                 | <span data-ttu-id="719d0-149">0x00000002</span><span class="sxs-lookup"><span data-stu-id="719d0-149">0x00000002</span></span><br/>                                                                                                                                                                         | <span data-ttu-id="719d0-150">Der prähook Ruft Pakete vor regulären Kontexten und posthooken ab.</span><span class="sxs-lookup"><span data-stu-id="719d0-150">Prehook gets packets before regular contexts and posthooks.</span></span> <span data-ttu-id="719d0-151">Sie erhalten Pakete in der Reihenfolge ihrer Erstellung.</span><span class="sxs-lookup"><span data-stu-id="719d0-151">They get packets in the order of their creation.</span></span><br/>                                                                                                                                                  |
| <span data-ttu-id="719d0-152">TCXO- \_ Cursor \_ Zustand</span><span class="sxs-lookup"><span data-stu-id="719d0-152">TCXO\_CURSOR\_STATE</span></span><br/>           | <span data-ttu-id="719d0-153">0x00000004</span><span class="sxs-lookup"><span data-stu-id="719d0-153">0x00000004</span></span><br/>                                                                                                                                                                         | <span data-ttu-id="719d0-154">Der TC gibt Pakete zurück, auch wenn der Cursor aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="719d0-154">The TC will return packets even if the cursor is up.</span></span> <span data-ttu-id="719d0-155">Standardmäßig gibt ein TC nur Pakete zurück, wenn der Cursor nicht angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="719d0-155">By default, a TC will only return packets when the cursor is down.</span></span><br/>                                                                                                                                       |
| <span data-ttu-id="719d0-156">TCXO \_ kein \_ Cursor \_ nach unten</span><span class="sxs-lookup"><span data-stu-id="719d0-156">TCXO\_NO\_CURSOR\_DOWN</span></span><br/>        | <span data-ttu-id="719d0-157">0x00000008</span><span class="sxs-lookup"><span data-stu-id="719d0-157">0x00000008</span></span><br/>                                                                                                                                                                         | <span data-ttu-id="719d0-158">Der TC gibt keine Pakete zurück, wenn der Cursor nicht angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="719d0-158">The TC will not return packets when the cursor is down.</span></span><br/>                                                                                                                                                                                                       |
| <span data-ttu-id="719d0-159">TCXO \_ nicht \_ integriert</span><span class="sxs-lookup"><span data-stu-id="719d0-159">TCXO\_NON\_INTEGRATED</span></span><br/>         | <span data-ttu-id="719d0-160">0x00000010</span><span class="sxs-lookup"><span data-stu-id="719d0-160">0x00000010</span></span><br/>                                                                                                                                                                         | <span data-ttu-id="719d0-161">Der Kontext ist nicht integriert.</span><span class="sxs-lookup"><span data-stu-id="719d0-161">The context will be non-integrated.</span></span><br/>                                                                                                                                                                                                                           |
| <span data-ttu-id="719d0-162">TCXO \_ posthook</span><span class="sxs-lookup"><span data-stu-id="719d0-162">TCXO\_POSTHOOK</span></span><br/>                | <span data-ttu-id="719d0-163">0x00000020</span><span class="sxs-lookup"><span data-stu-id="719d0-163">0x00000020</span></span><br/>                                                                                                                                                                         | <span data-ttu-id="719d0-164">Posthoochs erhalten Pakete nach regulären Tablet-Kontexten, aber vor dem Systemkontext.</span><span class="sxs-lookup"><span data-stu-id="719d0-164">Posthooks get packets after regular tablet contexts but before the system context.</span></span> <span data-ttu-id="719d0-165">Sie erhalten Pakete in umgekehrter Reihenfolge ihrer Erstellung.</span><span class="sxs-lookup"><span data-stu-id="719d0-165">They get packets in the reverse order of their creation.</span></span><br/>                                                                                                                   |
| <span data-ttu-id="719d0-166">TCXO \_ - \_ Cursor nicht anzeigen \_</span><span class="sxs-lookup"><span data-stu-id="719d0-166">TCXO\_DONT\_SHOW\_CURSOR</span></span><br/>      | <span data-ttu-id="719d0-167">0x00000080</span><span class="sxs-lookup"><span data-stu-id="719d0-167">0x00000080</span></span><br/>                                                                                                                                                                         | <span data-ttu-id="719d0-168">Der TC legt die Cursorposition nicht fest.</span><span class="sxs-lookup"><span data-stu-id="719d0-168">The TC will not set the cursor position.</span></span><br/>                                                                                                                                                                                                                      |
| <span data-ttu-id="719d0-169">TCXO \_ - \_ TCS nicht validieren \_</span><span class="sxs-lookup"><span data-stu-id="719d0-169">TCXO\_DONT\_VALIDATE\_TCS</span></span><br/>     | <span data-ttu-id="719d0-170">0x00000100</span><span class="sxs-lookup"><span data-stu-id="719d0-170">0x00000100</span></span><br/>                                                                                                                                                                         | <span data-ttu-id="719d0-171">Der TC überprüft nicht die GUIDs, die in den Einstellungen des Tablet-Kontexts an die unterstützten Eigenschaften des Geräts übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="719d0-171">The TC will not validate the GUIDS passed in the tablet context settings against the supported properties of the device.</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="719d0-172">TCXO \_ ermöglicht \_ Flicks</span><span class="sxs-lookup"><span data-stu-id="719d0-172">TCXO\_ALLOW\_FLICKS</span></span><br/>           | <span data-ttu-id="719d0-173">0x00000400</span><span class="sxs-lookup"><span data-stu-id="719d0-173">0x00000400</span></span><br/>                                                                                                                                                                         | <span data-ttu-id="719d0-174">Der TC ermöglicht das Durchführen der Flick Erkennung (Standardmäßig ist dies nur für System Kontexte zulässig), und der Client erhält "SE"- \_ Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="719d0-174">The TC will allow flick detection to take place (by default this is only allowed on system contexts), and the client will get SE\_FLICK events.</span></span><br/>                                                                                                               |
| <span data-ttu-id="719d0-175">TCXO- \_ Klicks zum Zulassen von \_ Feedback \_</span><span class="sxs-lookup"><span data-stu-id="719d0-175">TCXO\_ALLOW\_FEEDBACK\_TAPS</span></span><br/>   | <span data-ttu-id="719d0-176">0x00000800</span><span class="sxs-lookup"><span data-stu-id="719d0-176">0x00000800</span></span><br/>                                                                                                                                                                         | <span data-ttu-id="719d0-177">Der TC ermöglicht das Anzeigen von Stift Feedback.</span><span class="sxs-lookup"><span data-stu-id="719d0-177">The TC will allow pen feedback to be shown.</span></span> <span data-ttu-id="719d0-178">Standardmäßig ist dies nur für System Kontexte zulässig.</span><span class="sxs-lookup"><span data-stu-id="719d0-178">By default, this is only allowed on system contexts.</span></span><br/>                                                                                                                                                              |
| <span data-ttu-id="719d0-179">TCXO \_ - \_ Feedback zulassen ( \_ Fass)</span><span class="sxs-lookup"><span data-stu-id="719d0-179">TCXO\_ALLOW\_FEEDBACK\_BARREL</span></span><br/> | <span data-ttu-id="719d0-180">0x00001000</span><span class="sxs-lookup"><span data-stu-id="719d0-180">0x00001000</span></span><br/>                                                                                                                                                                         | <span data-ttu-id="719d0-181">Der TC ermöglicht das Anzeigen von Stift Feedback.</span><span class="sxs-lookup"><span data-stu-id="719d0-181">The TC will allow pen feedback to be shown.</span></span> <span data-ttu-id="719d0-182">Standardmäßig ist dies nur für System Kontexte zulässig.</span><span class="sxs-lookup"><span data-stu-id="719d0-182">By default, this is only allowed on system contexts.</span></span><br/>                                                                                                                                                              |
| <span data-ttu-id="719d0-183">Alle TCXO \_</span><span class="sxs-lookup"><span data-stu-id="719d0-183">TCXO\_ALL</span></span><br/>                     | <span data-ttu-id="719d0-184">TCXO- \_ Rand \| TCXO \_ prehook \| TCXO- \_ Cursor \_ Status \| TCXO \_ kein \_ Cursor \_ nach unten \| TCXO \_ nicht \_ integriert \| TCXO \_ posthook \| TCXO nicht \_ \_ anzeigen \_ Cursor \| TCXO nicht \_ \_ validieren \_ TCS</span><span class="sxs-lookup"><span data-stu-id="719d0-184">TCXO\_MARGIN \| TCXO\_PREHOOK \| TCXO\_CURSOR\_STATE \| TCXO\_NO\_CURSOR\_DOWN \| TCXO\_NON\_INTEGRATED \| TCXO\_POSTHOOK \| TCXO\_DONT\_SHOW\_CURSOR \| TCXO\_DONT\_VALIDATE\_TCS</span></span><br/> | <span data-ttu-id="719d0-185">Alle definierten Optionen für den Tablet-Kontext.</span><span class="sxs-lookup"><span data-stu-id="719d0-185">All defined tablet context options.</span></span><br/>                                                                                                                                                                                                                           |
| <span data-ttu-id="719d0-186">TCXO- \_ Hook</span><span class="sxs-lookup"><span data-stu-id="719d0-186">TCXO\_HOOK</span></span><br/>                    | <span data-ttu-id="719d0-187">TCXO- \_ prehook \| TCXO \_ posthook</span><span class="sxs-lookup"><span data-stu-id="719d0-187">TCXO\_PREHOOK \| TCXO\_POSTHOOK</span></span><br/>                                                                                                                                                    | <span data-ttu-id="719d0-188">Kombiniert die Funktionen vor Hook und posthook.</span><span class="sxs-lookup"><span data-stu-id="719d0-188">Combines pre-hook and post-hook functionality.</span></span><br/>                                                                                                                                                                                                                |



 

## <a name="requirements"></a><span data-ttu-id="719d0-189">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="719d0-189">Requirements</span></span>



| <span data-ttu-id="719d0-190">Anforderung</span><span class="sxs-lookup"><span data-stu-id="719d0-190">Requirement</span></span> | <span data-ttu-id="719d0-191">Wert</span><span class="sxs-lookup"><span data-stu-id="719d0-191">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="719d0-192">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="719d0-192">Minimum supported client</span></span><br/> | <span data-ttu-id="719d0-193">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="719d0-193">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="719d0-194">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="719d0-194">Minimum supported server</span></span><br/> | <span data-ttu-id="719d0-195">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="719d0-195">None supported</span></span><br/>                                                              |
| <span data-ttu-id="719d0-196">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="719d0-196">Library</span></span><br/>                  | <dl> <span data-ttu-id="719d0-197"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="719d0-197"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="719d0-198">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="719d0-198">See also</span></span>

<dl> <dt>

[<span data-ttu-id="719d0-199">**ITablet-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="719d0-199">**ITablet Interface**</span></span>](itablet.md)
</dt> <dt>

[<span data-ttu-id="719d0-200">**Kontext \_ enable \_ Type-Enumeration**</span><span class="sxs-lookup"><span data-stu-id="719d0-200">**CONTEXT\_ENABLE\_TYPE Enumeration**</span></span>](context-enable-type.md)
</dt> <dt>

[<span data-ttu-id="719d0-201">**Struktur der Tablet- \_ Kontext \_ Einstellungen**</span><span class="sxs-lookup"><span data-stu-id="719d0-201">**TABLET\_CONTEXT\_SETTINGS Structure**</span></span>](tablet-context-settings.md)
</dt> <dt>

[<span data-ttu-id="719d0-202">**Paket \_ Beschreibungs Struktur**</span><span class="sxs-lookup"><span data-stu-id="719d0-202">**PACKET\_DESCRIPTION Structure**</span></span>](/windows/desktop/api/tpcshrd/ns-tpcshrd-packet_description)
</dt> <dt>

[<span data-ttu-id="719d0-203">**Itabletcontextp-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="719d0-203">**ITabletContextP Interface**</span></span>](itabletcontextp.md)
</dt> <dt>

[<span data-ttu-id="719d0-204">**Itableteventsink-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="719d0-204">**ITabletEventSink Interface**</span></span>](itableteventsink.md)
</dt> </dl>

 

 




