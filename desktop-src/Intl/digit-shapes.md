---
description: Arabisch und viele andere Sprachen verfügen über klassische Formen für Zahlen, die sich von den herkömmlichen westlichen Ziffern unterscheiden, die am häufigsten auf Computern verwendet werden.
ms.assetid: 6b5267d8-b102-410c-bdc9-831555ca2f84
title: Ziffern Formen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6e6581b8b0eb87ae09b387c038c1ceba43125ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360784"
---
# <a name="digit-shapes"></a>Ziffern Formen

Arabisch und viele andere Sprachen verfügen über klassische Formen für Zahlen, die sich von den herkömmlichen westlichen Ziffern unterscheiden, die am häufigsten auf Computern verwendet werden. Um Mehrdeutigkeit beim Benennen dieser Formen zu vermeiden, verwendet dieses Dokument die folgenden Namen aus dem Unicode-Standard.



| Unicode-Name der Ziffern                                     | Verwendetes Land/Region                                    |
|----------------------------------------------------------------|--------------------------------------------------------------|
| Europäische Ziffern                                                | Europa, Nordamerika und viele weitere Länder/Regionen       |
| Arabic-Indic Ziffern                                            | Arabische Länder/Regionen (obwohl viele europäische Ziffern verwenden) |
| Weitere nationale Ziffern: indic-Ziffern, thailändische Ziffern und ähnliches | Verschiedene Länder/Regionen                                    |



 

Unicode bietet separate Code Punkte für jede Ziffern Form. Daher kann die Anwendung für den Zugriff auf spezielle sprach Ziffern Formen die relevanten Unicode-Zeichen Codes für die Ziffern oberhalb, u + 0030 bis U + 0039 verwenden. Diese Codes werden immer mit der entsprechenden Form angezeigt, die der Schriftart Verfügbarkeit unterliegen.

Die Unicode-Zeichen Codes U + 0030 bis u + 0039 stellen nominell die europäischen Ziffern 0 bis 9 dar, ihre Ziffern Form kann jedoch geändert werden. GDI-und DirectWrite-Text-APIs stellen Mechanismen bereit, mit denen Anwendungen dieses Verhalten steuern können. (Siehe beispielsweise [**scriptapplydigitsubstitution**](/windows/desktop/api/Usp10/nf-usp10-scriptapplydigitsubstitution) oder [**idwrite tetextanalysissink:: setnumersubstitution**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalysissink-setnumbersubstitution).) Das Verhalten in einigen Shellsteuerelementen und Benutzeroberflächen-Frameworks kann auf Benutzer Gebiets Schema Einstellungen für die Ziffern Ersetzung reagieren. Das Gebiets Schema [ \_ idigitsubstitution](locale-idigitsubstitution.md) LCTYPE kann verwendet werden, um Standardeinstellungen für die Ersetzungs Ersetzung für verschiedene Gebiets Schemas oder die Desktop Einstellungen des aktuellen Benutzers für die Ziffern Ersetzung abzurufen.

## <a name="native-digits"></a>Native Ziffern

Native Ziffern sind die vom Benutzer ausgewählten Ziffern Formen im Eigenschaften Blatt " **Zahl** " im Bereich "Regions-und Sprachoptionen" der Systemsteuerung. Um die vom Benutzer bevorzugte Ziffern Präsentation zu finden, verwendet Ihre Anwendung die [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) -Funktion oder die [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) -Funktion mit der " [locale- \_ snativedigits](locale-snative-constants.md) "-Konstante, die die Gebiets Schema Informationen darstellt.

> [!Note]  
> In der Regel werden Unicode-Ziffern Codes in Lauf Zeit Betriebssystemroutinen generiert. Daher müssen allgemeine Lauf Zeit Betriebssysteme aktualisiert werden, damit die Anwendung die [Gebiets \_ Schema-snativedigits](locale-snative-constants.md) entsprechend überprüfen kann.

 

## <a name="digit-substitution"></a>Ziffern Ersetzung

Die Anwendung kann die Ziffern Ersetzung verwenden, um dem Betriebssystem mitzuteilen, wie Ziffern u + 0030 bis u + 0039 gedruckt werden sollen. Dieser Vorgang wird von der [ \_ idigitsubstitution](locale-idigitsubstitution.md) -Schema-Konstante gesteuert.

## <a name="digit-shaping-for-a-single-function"></a>Ziffern Strukturierung für eine einzelne Funktion

Die [resulttextout](/windows/win32/api/wingdi/nf-wingdi-exttextouta)-, [getcharakteriplacement](/windows/win32/api/wingdi/nf-wingdi-getcharacterplacementa)-und [GCP- \_ Ergebnis](/windows/win32/api/wingdi/ns-wingdi-gcp_resultsa) Funktionen verfügen über Flags, die die Ersetzung von Unicode-Codes U + 0030 bis u + 0039 für die Dauer des Funktions Aufrufes steuern. Diese Flags überschreiben regionale Einstellungen in der Systemsteuerung, setzen jedoch nicht die Einstellungen zurück. Außerdem überschreiben Sie nicht die Unicode-Codes NADS und Nods. Die folgenden Flags sind verfügbar.



| Flags                 | Verwendete Ziffern                      | Verwendung in                   |
|-----------------------|----------------------------------|---------------------------|
| Eto- \_ numericslatin    | Europäische Ziffern                  | **Exttextout**            |
| Eto \_ numericslocal    | Für das Gebiets Schema geeignete Ziffern | **Exttextout**            |
| GCP- \_ numericslatin    | Europäische Ziffern                  | **GetCharacterPlacement** |
| GCP \_ numericslocal    | Für das Gebiets Schema geeignete Ziffern | **GetCharacterPlacement** |
| gcpclass- \_ latinnumber | Europäische Ziffern                  | **GCP- \_ Ergebnisse**          |
| gcpclass \_ localnumber | Für das Gebiets Schema geeignete Ziffern | **GCP- \_ Ergebnisse**          |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zur Unterstützung der Landessprache](about-national-language-support.md)
</dt> <dt>

[**Getlocaleingefo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa)
</dt> <dt>

[**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex)
</dt> </dl>

 

 
