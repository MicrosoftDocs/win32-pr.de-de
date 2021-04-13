---
title: Angeben der auszuführenden Aktionen
description: Angeben der auszuführenden Aktionen
ms.assetid: b6b094b1-276d-4f90-adc7-0f3507fdfe27
keywords:
- Advanced Systems Format (ASF), angeben von Aktionen
- ASF (Advanced Systems Format), angeben von Aktionen
- Digital Rights Management (DRM), angeben von Aktionen
- DRM (Digital Rights Management), angeben von Aktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d2bd39a04d9ac87c4492749ca5e250d587c0e25
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104389904"
---
# <a name="specifying-the-actions-to-be-performed"></a><span data-ttu-id="ead46-107">Angeben der auszuführenden Aktionen</span><span class="sxs-lookup"><span data-stu-id="ead46-107">Specifying the Actions To Be Performed</span></span>

<span data-ttu-id="ead46-108">Beim ersten Aufrufen von [**wmkreatereader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatereader) zum Erstellen des Reader-Objekts handelt es sich bei dem zweiten Parameter um einen bitweisen **or** von [**WMT- \_ Rechte**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_rights) Werten.</span><span class="sxs-lookup"><span data-stu-id="ead46-108">When you first call [**WMCreateReader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatereader) to create the reader object, the second parameter is a bitwise **OR** of [**WMT\_RIGHTS**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_rights) values.</span></span> <span data-ttu-id="ead46-109">Verwenden Sie diesen Parameter, um anzugeben, welche Aktion (n) die Anwendung für die erste zu öffnende Datei durchführen wird.</span><span class="sxs-lookup"><span data-stu-id="ead46-109">Use this parameter to specify which action(s) the application will take on the first file to be opened.</span></span> <span data-ttu-id="ead46-110">Diese Aktionen entsprechen direkt den rechten, die in der Lizenz angegeben werden können.</span><span class="sxs-lookup"><span data-stu-id="ead46-110">These actions correspond directly to rights that can be specified in the license.</span></span> <span data-ttu-id="ead46-111">Bei nachfolgenden Aufrufen von [**iwmreader:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open)können Sie die von Ihnen angeforderten Rechte ändern, indem Sie [**iwmdrmreader:: setdrmproperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-setdrmproperty)aufrufen, die definierte Konstante für die [**DRM- \_ Rechte**](drm-rights.md) Eigenschaft angeben und Zeichen folgen Literale (vom Typ " **WCHAR**"), die durch Semikolons getrennt sind, zur Identifizierung der Rechte verwenden.</span><span class="sxs-lookup"><span data-stu-id="ead46-111">On subsequent calls to [**IWMReader::Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open), you can modify the rights that you are requesting by calling [**IWMDRMReader::SetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-setdrmproperty), specifying the defined constant for the [**DRM\_Rights**](drm-rights.md) property, and using string literals (of type **WCHAR**) separated by semicolons to identify the rights.</span></span> <span data-ttu-id="ead46-112">Der folgende Code Ausschnitt fordert vier Rechte an: Geben Sie die Datei wieder, kopieren Sie Sie auf ein Gerät, und geben Sie Sie als Teil einer kollaborativen Wiedergabeliste an.</span><span class="sxs-lookup"><span data-stu-id="ead46-112">The following code snippet requests four rights: play the file, copy it to a device, and play it as part of a collaborative playlist.</span></span>


```C++
WCHAR wszRights[] = L"Play;Copy;CollaborativePlay";
p_WMDRMReader->SetDRMProperty(g_wszWMDRM_Rights, WMT_TYPE_STRING,
                              (BYTE*)wszRights, sizeof(wszRights));
```



> [!Note]  
> <span data-ttu-id="ead46-113">Verwechseln Sie die [**DRM- \_ Rechte**](drm-rights.md) Eigenschaft nicht mit der Eigenschaft [**DRM- \_ Flags**](drm-flags.md) , bei der es sich um ein **DWORD** handelt, das angibt, welche Rechte beim Kopieren von Inhalt von einer CD auf eine lokale DRM-Lizenz Version 1 angewendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="ead46-113">Do not confuse the [**DRM\_Rights**](drm-rights.md) property with the [**DRM\_Flags**](drm-flags.md) property, which is a **DWORD** used to specify which rights to apply to a local DRM version 1 license when copying content from a CD.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="ead46-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ead46-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ead46-115">**Geschützte Dateien werden gelesen.**</span><span class="sxs-lookup"><span data-stu-id="ead46-115">**Reading Protected Files**</span></span>](reading-protected-files.md)
</dt> </dl>

 

 




