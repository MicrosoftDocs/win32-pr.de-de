---
description: Auf Windows Vista und höher können Sie pseudolokale Gebietsschemas verwenden, um die Lokalisierbarkeit von Anwendungen zu testen. Dieses Thema enthält Verfahren für die Verwendung von Pseudocodes.
ms.assetid: 1eccdbb9-a1bd-443a-a5f6-d64c9e5c87b3
title: Verwenden von Pseudolokalitätsschemas für Lokalisierbarkeitstests
ms.topic: article
ms.date: 07/05/2018
ms.openlocfilehash: 72d84cbf324823a814c9412580b033792b0d1c8a45630bf2f4cb26dd8b2a1acf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119631720"
---
# <a name="using-pseudo-locales-for-localizability-testing"></a>Verwenden von Pseudolokalitätsschemas für Lokalisierbarkeitstests

[Pseudolokale](pseudo-locales.md) sind in Windows Vista und höher integriert, sodass Sie über NLS-APIs (National Language Support) darauf zugreifen können. Sie können Pseudo-Gebietsschemas verwenden, um die [Lokalisierbarkeit](/windows/uwp/design/globalizing/globalizing-portal) Ihrer Anwendungen zu testen. Dieses Thema enthält Verfahren für die Verwendung von Pseudocodes.

> [!NOTE]
> Eine Aufgabe, die bei pseudolokalen Gebietsschemas besondere Überlegungen erfordert, ist das Aufzählen dieser Gebietsschemas. ob in Ihrem Code oder im Regions- und Sprachoptionenteil der Systemsteuerung. Weitere Informationen dazu finden Sie weiter unten in diesem Thema.

Die Namen der Pseudolokale sind "qps-ploc", "qps-ploca" und "qps-plocm". Ab Windows 10 ist auch das Pseudolokal "qps-Latn-x-sh" verfügbar.

## <a name="retrieve-information-about-pseudo-locales"></a>Abrufen von Informationen zu Pseudolokalen

Sie können [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) verwenden, um Informationen zu einem Pseudo-Gebietsschema abzurufen. Übergeben Sie den Namen des bestimmten Pseudo-Gebietsschemas an die Funktion (siehe Liste der Namen oben). Beispiel: "qps-plocm" für das gespiegelte Pseudoschema.

```cpp
wchar_t languageIdentifier[5];
int rc{ ::GetLocaleInfoEx(L"qps-plocm", LOCALE_ILANGUAGE, languageIdentifier, 5) };
```

## <a name="use-localenametolcid-with-pseudo-locales"></a>Verwenden von LocaleNameToLCID mit Pseudolokalen

Sie können die NLS-Zuordnungsfunktion [**LocaleNameToLCID**](/windows/desktop/api/Winnls/nf-winnls-localenametolcid) mit dem Namen eines Pseudo-Gebietsschemas aufrufen.

```cpp
LCID lcid{ ::LocaleNameToLCID(L"qps-plocm", 0) };
```

## <a name="enable-pseudo-locales-for-enumeration"></a>Aktivieren von Pseudolokalen für die Enumeration

In Ihrer Anwendung können Sie [**EnumSystemLocalesEx**](/windows/desktop/api/Winnls/nf-winnls-enumsystemlocalesex) aufrufen, um die gebietsschemas aufzuzählen, die das System erkennt. Der Regionale und Sprachoptionen-Teil des Systemsteuerung ruft auch **EnumSystemLocalesEx** auf, um die Liste der angezeigten Gebietsschemas zu erstellen. Standardmäßig werden die vier oben aufgeführten Pseudolokale vom System jedoch nicht erkannt, sodass sie nicht von **EnumSystemLocalesEx** zurückgegeben werden. Für Systeme von Windows Vista bis einschließlich Windows 10 Version 1709 besteht die Lösung darin, Pseudolokale durch Hinzufügen von Schlüsseln zur Windows Registry zu aktivieren.

Die Änderungen werden unter dem \_ \_ HKEY LOCAL MACHINE System \\ \\ CurrentControlSet \\ Control \\ Nls-Schlüssel für die auf dem Betriebssystem installierten Sprachen vorgenommen. Sie können diese Einstellungen vornehmen, um die Pseudolokale zu aktivieren. Jeder unten gezeigte Schlüssel ist die hexadezimale LCID, die dem aktivierten Pseudo-Gebietsschema entspricht. Jeder Wert ist vom Typ String (REG \_ SZ).

```
[HKEY_LOCAL_MACHINE\System\CurrentControlSet\Control\Nls\Locale]
"00000501"="1" // qps-ploc (Windows Vista and later)
"000005fe"="7" // qps-ploca (Windows Vista and later)
"00000901"="1" // qps-Latn-x-sh (Windows 10 and later)
"000009ff"="d" // qps-plocm (Windows Vista and later)
```

Für Windows 10 Version 1803 hat das Bearbeiten der Windows Registry wie folgt keine Auswirkungen. Sie können jedoch weiterhin die nicht aufzählenden NLS-APIs mit den Namen der Pseudolokale aufrufen (siehe die obigen Codebeispiele), um Ihre Benutzeroberfläche (UI) aufzufüllen.

## <a name="related-topics"></a>Zugehörige Themen

* [Verwenden der Unterstützung für nationale Sprachen](using-national-language-support.md)
* [Pseudo-Gebietsschemas](pseudo-locales.md)
* [EnumSystemLocalesEx](/windows/desktop/api/Winnls/nf-winnls-enumsystemlocalesex)
* [GetLocaleInfoEx](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex)
* [LocaleNameToLCID](/windows/desktop/api/Winnls/nf-winnls-localenametolcid)
