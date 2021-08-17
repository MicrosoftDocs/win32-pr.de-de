---
description: NLS enthält eine Reihe von API-Funktionen, mit denen Ihre Anwendungen Gebietsschemadaten zwischen Gebietsschemabezeichnern und Gebietsschemanamen zuordnen und neutrale Gebietsschemas auflisten können.
ms.assetid: 01bc261d-dfee-430e-86c9-cfafe82856c8
title: Zuordnen von Gebietsschemadaten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1576844f13dda80a6b9d754fc807ef8a35514dcfedd88dc04cf233cfb2a1bfb5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119147192"
---
# <a name="mapping-locale-data"></a>Zuordnen von Gebietsschemadaten

NLS enthält eine Reihe von API-Funktionen, mit denen Ihre Anwendungen Gebietsschemadaten zwischen [Gebietsschemabezeichnern](locale-identifiers.md) und [Gebietsschemanamen](locale-names.md)zuordnen und neutrale Gebietsschemas auflisten können. In diesem Thema wird die Verwendung dieser Funktionen auf Windows Vista und höher und auf Betriebssystemen vor Windows Vista (manchmal auch als "Downlevelsysteme" bezeichnet) erläutert.

## <a name="map-locale-data-on-windows-vista-and-later"></a>Zuordnen von Gebietsschemadaten auf Windows Vista und höher

NLS bietet mehrere Gebietsschemazuordnungsfunktionen für die Verwendung durch Anwendungen, die Sie für die Ausführung auf Windows Vista und höher entwickeln. Sie enthält auch Funktionen, mit denen Ihre Anwendungen neutrale Gebietsschemas aufzählen können.

**Verwenden der Standardkonvertierungsfunktionen für die Datenzuordnung**

Um eine Zuordnung zwischen einem Gebietsschemanamen und einem Gebietsschemabezeichner zu erstellen, kann Ihre Anwendung die [**LocaleNameToLCID-Funktion**](/windows/desktop/api/Winnls/nf-winnls-localenametolcid) aufrufen. Die Anwendung verwendet [**LCIDToLocaleName,**](/windows/desktop/api/Winnls/nf-winnls-lcidtolocalename) um eine Zuordnung zwischen einem Gebietsschemabezeichner und einem Gebietsschemanamen zu erstellen.

**Auflisten neutraler Gebietsschemas**

Um neutrale Gebietsschemas für Windows 7 und höher aufzuzählen, kann Ihre Anwendung [**EnumSystemLocalesEx**](/windows/desktop/api/Winnls/nf-winnls-enumsystemlocalesex) aufrufen, wobei *dwFlags* auf [**LOCALE \_ NEUTRALDATA**](locale-neutraldata.md)festgelegt ist. Es kann auch [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) verwenden, wobei *LCType* auf [**LOCALE \_ INEUTRAL**](locale-ineutral.md)festgelegt ist.

## <a name="map-locale-data-on-pre-windows-vista-operating-systems"></a>Zuordnen von Gebietsschemadaten auf Betriebssystemen vor Windows Vista

NLS enthält eine Direct Link Library (DLL), die für Anwendungen verwendet werden soll, die Sie für die Ausführung auf Betriebssystemen vor Windows Vista entwickeln. Die DLL unterstützt sowohl Konvertierungs- als auch Auflistungsfunktionen für die Datenzuordnung.

> [!Note]  
> Anwendungen, die nur auf Windows Vista und höher ausgeführt werden, sollten nicht die Downlevel-Zuordnungs- oder Auflistungsfunktionen verwenden.

 

**Verwenden der Downlevelkonvertierungsfunktionen für die Datenzuordnung**

Ihre Anwendung, die auf ein downlevel-System ausgerichtet ist, kann die [**DownlevelLCIDToLocaleName-Funktion**](downlevellcidtolocalename.md) aufrufen, um einen Gebietsschemabezeichner in einen Gebietsschemanamen zu konvertieren. Wenn ein Gebietsschemaname in einen Gebietsschemabezeichner konvertiert werden muss, sollte [**downlevelLocaleNameToLCID**](downlevellocalenametolcid.md)aufgerufen werden.

**Verwenden der Downlevel-Auflistungsfunktionen zum Auflisten neutraler Gebietsschemas**

Ihre Anwendung sollte die [**DownlevelGetParentLocaleLCID**](downlevelgetparentlocalelcid.md) aufrufen, um den Gebietsschemabezeichner des übergeordneten Elements für ein Gebietsschema abzurufen. Wenn die Anwendung den Gebietsschemanamen des übergeordneten Gebietsschemas abrufen muss, sollte sie [**DownlevelGetParentLocaleName**](downlevelgetparentlocalename.md)aufrufen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden der Unterstützung für nationale Sprachen](using-national-language-support.md)
</dt> <dt>

[Gebietsschemabezeichner](locale-identifiers.md)
</dt> <dt>

[Gebietsschemanamen](locale-names.md)
</dt> </dl>

 

 



