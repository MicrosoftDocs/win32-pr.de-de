---
title: Explizite Autorisierungs- und Einschlusslisten
description: Explizite Autorisierungs- und Einschlusslisten
ms.assetid: b2e1cdd4-ea3c-4b05-a53a-2cdc12440645
keywords:
- Windows Medienformat-SDK, DRM-Export
- Windows Medienformat-SDK, Exportieren
- Windows Medienformat-SDK, explizite Autorisierungs- und Einschlusslisten
- Windows Medienformat-SDK, Autorisierungslisten
- Windows Medienformat-SDK, Aufnahmelisten
- Digital Rights Management (DRM), Export
- DRM (Digital Rights Management),Export
- Digital Rights Management (DRM), explizite Autorisierungs- und Aufnahmelisten
- DRM (Digital Rights Management), explizite Autorisierungs- und Aufnahmelisten
- Digital Rights Management (DRM), Autorisierungslisten
- DRM (Digital Rights Management), Autorisierungslisten
- Digital Rights Management (DRM), Aufnahmelisten
- DRM (Digital Rights Management), Aufnahmelisten
- Erweiterte DRM-Client-APIs, explizite Autorisierungs- und Aufnahmelisten
- Erweiterte Client-APIs, explizite Autorisierungs- und Aufnahmelisten
- Erweiterte APIs des DRM-Clients, Autorisierungslisten
- Erweiterte Client-APIs, Autorisierungslisten
- Erweiterte DRM-Client-APIs, Aufnahmelisten
- Erweiterte Client-APIs, Aufnahmelisten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ee489d91002cacf7d8a0c89ffeef1752cd844aa089fabbe636e5e50fc185a42
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089730"
---
# <a name="explicit-authorization-and-inclusion-lists"></a>Explizite Autorisierungs- und Einschlusslisten

Lizenzen können eine Aufnahmeliste enthalten, um den Export von Inhalten, die durch Windows Media DRM geschützt sind, explizit in andere Inhaltsschutzschemas (Content Protection Scheme, CPS) zu autorisieren. Gemäß den Bedingungen des Lizenzvertrags, den Sie mit Microsoft abschließen, um den DRM-Export zu ermöglichen, können Sie nur in einen gültigen CPS exportieren, der in der Aufnahmeliste einer Lizenz identifiziert wird.

Eine Aufnahmeliste ist ein umgrenztes Array von GUIDs (Globally Unique Identifiers), die jeweils einen bestimmten autorisierten CPS darstellen, in den der Inhalt exportiert werden kann. Die in einer Aufnahmeliste aufgeführten GUIDs sind unabhängig von den Ausgabeschutzebenen (Output Protection Levels, OPL) und den Inhaltsschutzebenen (Content Protection Levels, CPL). Das Erzwingen dieser Einschränkungen liegt in der Verantwortung Ihrer Anwendung.

> [!Note]  
> Wenn Sie Windows Medien-DRM-Export für komprimierten Inhalt ausführen, greifen Sie über die [**IWMDRMLicense::GetInclusionList-Methode**](iwmdrmlicense-getinclusionlist.md) auf die Aufnahmeliste zu. Wenn Sie Windows Medien-DRM-Export für nicht komprimierten Inhalt ausführen, verwenden Sie die [**IWMDRMReader3::GetInclusionList-Methode.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader3-getinclusionlist)

 

Wenden Sie sich an , um ein neues Inhaltsschutzsystem als Windows Media DRM Permitted Export in the Windows Media DRM export compliance rules (Medien-DRM-Exportkompatibilitätsregeln) zu wmla@microsoft.com registrieren.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**DRM-Export**](drm-export.md)
</dt> </dl>

 

 




