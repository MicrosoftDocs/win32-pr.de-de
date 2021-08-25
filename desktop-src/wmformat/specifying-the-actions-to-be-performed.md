---
title: Angeben der auszuführenden Aktionen
description: Angeben der auszuführenden Aktionen
ms.assetid: b6b094b1-276d-4f90-adc7-0f3507fdfe27
keywords:
- Advanced Systems Format (ASF), Angeben von Aktionen
- ASF (Advanced Systems Format), Angeben von Aktionen
- Digital Rights Management (DRM), Angeben von Aktionen
- DRM (Verwaltung digitaler Rechte),Angeben von Aktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2d27df2904aee061deb252e08b59e1e88e4d1cd9e151290cd940fc48a650404
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807800"
---
# <a name="specifying-the-actions-to-be-performed"></a>Angeben der auszuführenden Aktionen

Wenn Sie [**WMCreateReader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatereader) zum ersten Mal aufrufen, um das Readerobjekt zu erstellen, ist der zweite Parameter ein bitweises **OR** von [**WMT \_ RIGHTS-Werten.**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_rights) Verwenden Sie diesen Parameter, um anzugeben, welche Aktionen die Anwendung für die erste zu öffnende Datei ergreifen soll. Diese Aktionen entsprechen direkt den Rechten, die in der Lizenz angegeben werden können. Bei nachfolgenden Aufrufen von [**IWMReader::Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open)können Sie die angeforderten Rechte ändern, indem Sie [**IWMDRMReader::SetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-setdrmproperty)aufrufen, die definierte Konstante für die [**DRM \_ Rights-Eigenschaft**](drm-rights.md) angeben und Zeichenfolgenliterale (vom Typ **WCHAR**) durch Semikolons getrennt verwenden, um die Rechte zu identifizieren. Der folgende Codeausschnitt fordert vier Rechte an: die Datei wiedergeben, sie auf ein Gerät kopieren und als Teil einer gemeinsamen Wiedergabeliste wiedergeben.


```C++
WCHAR wszRights[] = L"Play;Copy;CollaborativePlay";
p_WMDRMReader->SetDRMProperty(g_wszWMDRM_Rights, WMT_TYPE_STRING,
                              (BYTE*)wszRights, sizeof(wszRights));
```



> [!Note]  
> Verwechseln Sie die [**DRM \_ Rights-Eigenschaft**](drm-rights.md) nicht mit der [**\_ DRM-Flags-Eigenschaft,**](drm-flags.md) bei der es sich um ein **DWORD** handelt, mit dem angegeben wird, welche Rechte beim Kopieren von Inhalten von einer CD auf eine lokale DRM-Lizenz der Version 1 angewendet werden sollen.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Lesen von geschützten Dateien**](reading-protected-files.md)
</dt> </dl>

 

 




