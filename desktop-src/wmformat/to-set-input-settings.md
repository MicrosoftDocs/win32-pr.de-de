---
title: So legen Sie Eingabeeinstellungen fest
description: So legen Sie Eingabeeinstellungen fest
ms.assetid: 288801a7-793f-43bd-9c5a-f9e1bd86ecc3
keywords:
- Advanced Systems Format (ASF), Eingabeeinstellungen
- ASF (Advanced Systems Format), Eingabeeinstellungen
- Profile, Eingabeeinstellungen
- Codecs, Eingabeeinstellungen
- Streams, Eingabeeinstellungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e7b2db64a7346cc8b9d46c48f0add79dafcac95
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "103948443"
---
# <a name="to-set-input-settings"></a><span data-ttu-id="8789d-108">So legen Sie Eingabeeinstellungen fest</span><span class="sxs-lookup"><span data-stu-id="8789d-108">To Set Input Settings</span></span>

<span data-ttu-id="8789d-109">Die grundlegenden Eigenschaften von Eingabemedien und Streamingmedien werden durch die [**WM- \_ \_ Medientyp**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) Struktur definiert.</span><span class="sxs-lookup"><span data-stu-id="8789d-109">The basic properties of input media and stream media are defined by the [**WM\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) structure.</span></span> <span data-ttu-id="8789d-110">Bei Eingabe Formaten werden die Medientyp Informationen von der Anwendung festgelegt.</span><span class="sxs-lookup"><span data-stu-id="8789d-110">For input formats, the media type information is set by your application.</span></span> <span data-ttu-id="8789d-111">Bei streamformaten werden die Medientyp Informationen in dem Profil festgelegt, das Sie dem Writer zuweisen.</span><span class="sxs-lookup"><span data-stu-id="8789d-111">For stream formats, the media type information is set in the profile you assign to the writer.</span></span> <span data-ttu-id="8789d-112">Einige Eigenschaften sind vom Medientyp unabhängig und müssen für eine Eingabe festgelegt werden, bevor der Schreibvorgang beginnt.</span><span class="sxs-lookup"><span data-stu-id="8789d-112">Some properties are independent of media type and must be set for an input before writing begins.</span></span> <span data-ttu-id="8789d-113">Bei diesen Eigenschaften handelt es sich um Codec-und Writer-Funktionen, die vom Streamtyp unabhängig sind. Sie müssen festgelegt werden, nachdem das Profil im Writer zugewiesen wurde, aber bevor das Schreiben beginnt.</span><span class="sxs-lookup"><span data-stu-id="8789d-113">These properties are codec and writer features that are independent of stream type, and must be set after the profile is assigned in the writer but before writing begins.</span></span>

<span data-ttu-id="8789d-114">Für das Festlegen einer Eingabe Einstellung ist ein aufrufsbefehl von [**IWMWriterAdvanced2:: \* tinputsetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting)erforderlich.</span><span class="sxs-lookup"><span data-stu-id="8789d-114">Setting an input setting requires a call to [**IWMWriterAdvanced2::SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting).</span></span> <span data-ttu-id="8789d-115">Sie können auch den aktuellen Wert einer Einstellung mit einem Aufrufen von [**IWMWriterAdvanced2:: getinputsetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-getinputsetting)überprüfen.</span><span class="sxs-lookup"><span data-stu-id="8789d-115">You can also check the current value of a setting with a call to [**IWMWriterAdvanced2::GetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-getinputsetting).</span></span>

## <a name="related-topics"></a><span data-ttu-id="8789d-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8789d-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8789d-117">**Verwenden von Profilen mit dem Writer**</span><span class="sxs-lookup"><span data-stu-id="8789d-117">**To Use Profiles with the Writer**</span></span>](to-use-profiles-with-the-writer.md)
</dt> <dt>

[<span data-ttu-id="8789d-118">**Schreiben von ASF-Dateien**</span><span class="sxs-lookup"><span data-stu-id="8789d-118">**Writing ASF Files**</span></span>](writing-asf-files.md)
</dt> <dt>

[<span data-ttu-id="8789d-119">**Schreiben von bildstreams**</span><span class="sxs-lookup"><span data-stu-id="8789d-119">**Writing Image Streams**</span></span>](writing-image-streams.md)
</dt> </dl>

 

 




