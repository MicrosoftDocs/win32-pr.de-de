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
# <a name="specifying-the-actions-to-be-performed"></a>Angeben der auszuführenden Aktionen

Beim ersten Aufrufen von [**wmkreatereader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatereader) zum Erstellen des Reader-Objekts handelt es sich bei dem zweiten Parameter um einen bitweisen **or** von [**WMT- \_ Rechte**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_rights) Werten. Verwenden Sie diesen Parameter, um anzugeben, welche Aktion (n) die Anwendung für die erste zu öffnende Datei durchführen wird. Diese Aktionen entsprechen direkt den rechten, die in der Lizenz angegeben werden können. Bei nachfolgenden Aufrufen von [**iwmreader:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open)können Sie die von Ihnen angeforderten Rechte ändern, indem Sie [**iwmdrmreader:: setdrmproperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-setdrmproperty)aufrufen, die definierte Konstante für die [**DRM- \_ Rechte**](drm-rights.md) Eigenschaft angeben und Zeichen folgen Literale (vom Typ " **WCHAR**"), die durch Semikolons getrennt sind, zur Identifizierung der Rechte verwenden. Der folgende Code Ausschnitt fordert vier Rechte an: Geben Sie die Datei wieder, kopieren Sie Sie auf ein Gerät, und geben Sie Sie als Teil einer kollaborativen Wiedergabeliste an.


```C++
WCHAR wszRights[] = L"Play;Copy;CollaborativePlay";
p_WMDRMReader->SetDRMProperty(g_wszWMDRM_Rights, WMT_TYPE_STRING,
                              (BYTE*)wszRights, sizeof(wszRights));
```



> [!Note]  
> Verwechseln Sie die [**DRM- \_ Rechte**](drm-rights.md) Eigenschaft nicht mit der Eigenschaft [**DRM- \_ Flags**](drm-flags.md) , bei der es sich um ein **DWORD** handelt, das angibt, welche Rechte beim Kopieren von Inhalt von einer CD auf eine lokale DRM-Lizenz Version 1 angewendet werden sollen.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Geschützte Dateien werden gelesen.**](reading-protected-files.md)
</dt> </dl>

 

 




