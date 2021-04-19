---
description: Unter Windows Vista und höher können Sie Pseudo Gebiets Schemata zum Testen der Lokalisier barkeit von Anwendungen verwenden. Dieses Thema enthält Verfahren für die Verwendung von Pseudo Codes.
ms.assetid: 1eccdbb9-a1bd-443a-a5f6-d64c9e5c87b3
title: Verwenden von Pseudo Gebiets Schemata für Lokalisier barkeits Tests
ms.topic: article
ms.date: 07/05/2018
ms.openlocfilehash: f8c6b435b85a5bef98eff9bf76681096779433e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106357098"
---
# <a name="using-pseudo-locales-for-localizability-testing"></a>Verwenden von Pseudo Gebiets Schemata für Lokalisier barkeits Tests

[Pseudo](pseudo-locales.md) Gebiets Schemas sind in Windows Vista und höher integriert, sodass Sie über APIs für die nationale Sprachunterstützung (NLS) darauf zugreifen können. Sie können Pseudo Gebiets Schemas verwenden, um die [Lokalisier barkeit](/windows/uwp/design/globalizing/globalizing-portal) Ihrer Anwendungen zu testen. Dieses Thema enthält Verfahren für die Verwendung von Pseudo Codes.

> [!NOTE]
> Eine Aufgabe, die bei Pseudo Gebiets Schemata besonders berücksichtigt werden muss, besteht darin, Sie aufzulisten. ob in Ihrem Code oder in den Regions-und Sprachoptionen in der Systemsteuerung. Weitere Informationen dazu weiter unten in diesem Thema.

Die Namen der Pseudo Gebiets Schemata lauten "QPS-ploc", "QPS-Ploca" und "QPS-plocm". Ab Windows 10 ist auch das Pseudo Gebiets Schema "QPS-Latn-x-sh" verfügbar.

## <a name="retrieve-information-about-pseudo-locales"></a>Abrufen von Informationen zu Pseudo Gebiets Schemata

Sie können [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) zum Abrufen von Informationen zu einem Pseudo Gebiets Schema verwenden. Übergeben Sie den Namen des jeweiligen Pseudo Gebiets Schemas an die Funktion (siehe oben genannte Liste der Namen). Beispiel: "QPS-plocm" für das gespiegelte Pseudo Gebiets Schema.

```cpp
wchar_t languageIdentifier[5];
int rc{ ::GetLocaleInfoEx(L"qps-plocm", LOCALE_ILANGUAGE, languageIdentifier, 5) };
```

## <a name="use-localenametolcid-with-pseudo-locales"></a>Verwenden von LocaleNameToLCID mit Pseudo Gebiets Schemata

Sie können die NLS-Mapping-Funktion [**LocaleNameToLCID**](/windows/desktop/api/Winnls/nf-winnls-localenametolcid) mit dem Namen eines Pseudo Gebiets Schemas aufzurufen.

```cpp
LCID lcid{ ::LocaleNameToLCID(L"qps-plocm", 0) };
```

## <a name="enable-pseudo-locales-for-enumeration"></a>Pseudo Gebiets Schemas für Enumeration aktivieren

In Ihrer Anwendung können Sie [**enumsystemlocalesex**](/windows/desktop/api/Winnls/nf-winnls-enumsystemlocalesex) aufrufen, um die Gebiets Schemas aufzulisten, die vom System erkannt werden. Der Bereich Regions-und Sprachoptionen in der Systemsteuerung ruft auch **enumsystemlocalesex** auf, um die Liste der Gebiets Schemas, die es anzeigt, zu erstellen. Die vier oben aufgeführten Pseudo Gebiets Schemas werden jedoch standardmäßig nicht vom System erkannt, sodass Sie nicht von **enumsystemlocalesex** zurückgegeben werden. Für Systeme von Windows Vista bis einschließlich Windows 10, Version 1709, besteht die Lösung darin, Pseudo Gebiets Schemata durch Hinzufügen von Schlüsseln zur Windows-Registrierung zu aktivieren.

Die bearbeitvorgänge werden unter dem lokalen HKEY- \_ \_ Computer \\ System \\ CurrentControlSet \\ Control \\ nls Key für die auf dem Betriebs System installierten Sprachen vorgenommen. Sie können diese Einstellungen vornehmen, um die Pseudo Gebiets Schemas zu aktivieren. Jeder unten gezeigte Schlüssel ist die hexadezimale LCID, die dem aktivierten Pseudo Gebiets Schema entspricht. Jeder Wert ist vom Typ Zeichenfolge (reg \_ SZ).

```
[HKEY_LOCAL_MACHINE\System\CurrentControlSet\Control\Nls\Locale]
"00000501"="1" // qps-ploc (Windows Vista and later)
"000005fe"="7" // qps-ploca (Windows Vista and later)
"00000901"="1" // qps-Latn-x-sh (Windows 10 and later)
"000009ff"="d" // qps-plocm (Windows Vista and later)
```

Für Windows 10, Version 1803, wirkt sich die Bearbeitung der Windows-Registrierung wie folgt nicht aus. Sie können jedoch weiterhin die nicht aufzurufenden nls-APIs mit den Namen der Pseudo Gebiets Schemata (siehe die obigen Codebeispiele) zum Auffüllen Ihrer Benutzeroberfläche (UI) aufzurufen.

## <a name="related-topics"></a>Zugehörige Themen

* [Verwenden der Unterstützung für nationale Sprache](using-national-language-support.md)
* [Pseudo Gebiets Schemata](pseudo-locales.md)
* [Enumsystemlocalesex](/windows/desktop/api/Winnls/nf-winnls-enumsystemlocalesex)
* [GetLocaleInfoEx](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex)
* [LocaleNameToLCID](/windows/desktop/api/Winnls/nf-winnls-localenametolcid)
