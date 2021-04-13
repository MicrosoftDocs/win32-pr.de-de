---
description: Die Konstanten "audclnt \_ sessionflags \_ xxx" geben Merkmale einer Audiositzung an, die dem Stream zugeordnet ist.
ms.assetid: 5745d5bc-71e8-4b33-8227-c1c84226b6ee
title: AUDCLNT_SESSIONFLAGS_XXX Konstanten (audiosessiontypes. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e2152c33103ca3366399995b7d11bb072f2bdd2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483923"
---
# <a name="audclnt_sessionflags_xxx-constants"></a><span data-ttu-id="50d20-103">Audclnt \_ sessionflags \_ xxx-Konstanten</span><span class="sxs-lookup"><span data-stu-id="50d20-103">AUDCLNT\_SESSIONFLAGS\_XXX Constants</span></span>

<span data-ttu-id="50d20-104">Die Konstanten "audclnt \_ sessionflags \_ xxx" geben Merkmale einer Audiositzung an, die dem Stream zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="50d20-104">The AUDCLNT\_SESSIONFLAGS\_XXX constants indicate characteristics of an audio session associated with the stream.</span></span> <span data-ttu-id="50d20-105">Diese Optionen können von einem Client während der Initialisierung des Datenstroms durch den *StreamFlags* -Parameter der [**iaudioclient:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) -Methode angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="50d20-105">A client can specify these options during the initialization of the stream by through the *StreamFlags* parameter of the [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) method.</span></span>



| <span data-ttu-id="50d20-106">Konstante/Wert</span><span class="sxs-lookup"><span data-stu-id="50d20-106">Constant/value</span></span>                                                                                                                                                                                                                                                                                                                   | <span data-ttu-id="50d20-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="50d20-107">Description</span></span>                                                                                                                                                                                                                                                                                                      |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="AUDCLNT_SESSIONFLAGS_EXPIREWHENUNOWNED"></span><span id="audclnt_sessionflags_expirewhenunowned"></span><dl> <span data-ttu-id="50d20-108">" <dt>**Audclnt \_ " Sessionflags \_ expireexpinicht im Besitz**</dt> von <dt>0x10000000</dt></span><span class="sxs-lookup"><span data-stu-id="50d20-108"><dt>**AUDCLNT\_SESSIONFLAGS\_EXPIREWHENUNOWNED**</dt> <dt>0x10000000 </dt></span></span> </dl>                       | <span data-ttu-id="50d20-109">Die Sitzung läuft ab, wenn keine zugeordneten Streams vorhanden sind und die besitzenden Sitzungs Steuerungs Objekte Verweise enthalten.</span><span class="sxs-lookup"><span data-stu-id="50d20-109">The session expires when there are no associated streams and owning session control objects holding references.</span></span><br/>                                                                                                                                                                                       |
| <span id="AUDCLNT_SESSIONFLAGS_DISPLAY_HIDE"></span><span id="audclnt_sessionflags_display_hide"></span><dl> <span data-ttu-id="50d20-110">" <dt>**Audclnt \_ " Sessionflags- \_ Anzeige \_ Ausblenden**</dt> <dt>0x20000000</dt></span><span class="sxs-lookup"><span data-stu-id="50d20-110"><dt>**AUDCLNT\_SESSIONFLAGS\_DISPLAY\_HIDE**</dt> <dt>0x20000000 </dt></span></span> </dl>                                     | <span data-ttu-id="50d20-111">Wenn die Audiositzung erstellt wird, wird das Volume-Steuerelement auf der volumemixer-Benutzeroberfläche ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="50d20-111">The volume control is hidden in the volume mixer user interface when the audio session is created.</span></span> <span data-ttu-id="50d20-112">Wenn die mit dem Stream verknüpfte Sitzung bereits vorhanden ist, bevor [**iaudioclient:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) den Stream öffnet, wird das volumesteuerelement im volumemixer angezeigt.</span><span class="sxs-lookup"><span data-stu-id="50d20-112">If the session associated with the stream already exists before [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) opens the stream, the volume control is displayed in the volume mixer.</span></span><br/> |
| <span id="_AUDCLNT_SESSIONFLAGS_DISPLAY_HIDEWHENEXPIRED"></span><span id="_audclnt_sessionflags_display_hidewhenexpired"></span><dl> <span data-ttu-id="50d20-113"><dt> **Audclnt \_ sessionflags \_ Display \_ hideabgelaufabgelaufenes**</dt> <dt>0x40000000</dt></span><span class="sxs-lookup"><span data-stu-id="50d20-113"><dt> **AUDCLNT\_SESSIONFLAGS\_DISPLAY\_HIDEWHENEXPIRED**</dt> <dt>0x40000000 </dt></span></span> </dl> | <span data-ttu-id="50d20-114">Das volumesteuerelement ist in der volumemixer-Benutzeroberfläche ausgeblendet, nachdem die Sitzung abgelaufen ist.</span><span class="sxs-lookup"><span data-stu-id="50d20-114">The volume control is hidden in the volume mixer user interface after the session expires.</span></span> <br/>                                                                                                                                                                                                           |



## <a name="requirements"></a><span data-ttu-id="50d20-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="50d20-115">Requirements</span></span>



| <span data-ttu-id="50d20-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="50d20-116">Requirement</span></span> | <span data-ttu-id="50d20-117">Wert</span><span class="sxs-lookup"><span data-stu-id="50d20-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50d20-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="50d20-118">Minimum supported client</span></span><br/> | <span data-ttu-id="50d20-119">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="50d20-119">Windows 7 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="50d20-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="50d20-120">Minimum supported server</span></span><br/> | <span data-ttu-id="50d20-121">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="50d20-121">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="50d20-122">Header</span><span class="sxs-lookup"><span data-stu-id="50d20-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="50d20-123"><dt>Audiosessiontypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="50d20-123"><dt>Audiosessiontypes.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50d20-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="50d20-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50d20-125">Kernaudiokonstanten</span><span class="sxs-lookup"><span data-stu-id="50d20-125">Core Audio Constants</span></span>](core-audio-constants.md)
</dt> <dt>

[<span data-ttu-id="50d20-126">**Iaudiosessioncontrol**</span><span class="sxs-lookup"><span data-stu-id="50d20-126">**IAudioSessionControl**</span></span>](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol)
</dt> </dl>

 

 




