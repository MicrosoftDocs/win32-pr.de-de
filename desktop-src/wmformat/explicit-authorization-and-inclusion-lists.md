---
title: Explizite Autorisierungs-und Inklusions Listen
description: Explizite Autorisierungs-und Inklusions Listen
ms.assetid: b2e1cdd4-ea3c-4b05-a53a-2cdc12440645
keywords:
- Windows Media-Format-SDK, DRM-Export
- SDK für Windows Media-Format, exportieren
- Windows Media-Format-SDK, explizite Autorisierungs-und Inklusions Listen
- Windows Media-Format-SDK, Autorisierungs Listen
- Windows Media-Format-SDK, Inklusions Listen
- Digital Rights Management (DRM), exportieren
- DRM (Digital Rights Management), exportieren
- Digital Rights Management (DRM), explizite Autorisierung und Inklusions Listen
- DRM-(Digital Rights Management), explizite Autorisierungs-und Inklusions Listen
- Digital Rights Management (DRM), Autorisierungs Listen
- DRM (Digital Rights Management), Autorisierungs Listen
- Digital Rights Management (DRM), Inklusions Listen
- DRM (Digital Rights Management), Inklusions Listen
- Erweiterte APIs für den DRM-Client, explizite Autorisierung und Inklusions Listen
- Erweiterte Client-APIs, explizite Autorisierungs-und Inklusions Listen
- Erweiterte APIs für den DRM-Client, Autorisierungs Listen
- Erweiterte Client-APIs, Autorisierungs Listen
- Erweiterte APIs für den DRM-Client, Inklusions Listen
- Erweiterte Client-APIs, Inklusions Listen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2309bed28ffd3add2a75c1cd90488b9ef454659b
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104389854"
---
# <a name="explicit-authorization-and-inclusion-lists"></a>Explizite Autorisierungs-und Inklusions Listen

Lizenzen können eine Inklusions Liste enthalten, um den Export von Inhalten, die von Windows Media DRM geschützt werden, explizit in andere Inhalts Schutz Schemas (CPS) zu autorisieren. Gemäß den Bedingungen des Lizenzvertrags, den Sie bei Microsoft eingegeben haben, um den DRM-Export zu aktivieren, können Sie nur in ein gültiges CPS exportieren, das in der Inklusions Liste einer Lizenz angegeben ist.

Eine Inklusions Liste ist ein begrenztes Array von GUIDs (Global Unique Identifier), die jeweils ein bestimmtes autorisiertes CPS darstellen, in das der Inhalt exportiert werden kann. Die in einer Inklusions Liste aufgeführten GUIDs sind unabhängig von den Ausgabe Schutz Ebenen (OPL) und Content Protection Levels (CPL). Die Durchsetzung dieser Einschränkungen ist die Verantwortung ihrer Anwendung.

> [!Note]  
> Wenn Sie den Windows Media DRM-Export in komprimiertem Inhalt durchführen, greifen Sie über die [**iwmdrmlicense:: getinclusionlist**](iwmdrmlicense-getinclusionlist.md) -Methode auf die Aufnahme Liste zu. Wenn Sie den Windows Media DRM-Export auf nicht komprimierten Inhalt durchführen, verwenden Sie die [**IWMDRMReader3:: getinclusionlist**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader3-getinclusionlist) -Methode.

 

Wenden Sie sich an, um ein neues Inhalts Schutzsystem als Windows Media DRM zu registrieren, das in den Windows Media DRM-Export Kompatibilitäts Regeln zulässig ist wmla@microsoft.com .

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**DRM-Export**](drm-export.md)
</dt> </dl>

 

 




