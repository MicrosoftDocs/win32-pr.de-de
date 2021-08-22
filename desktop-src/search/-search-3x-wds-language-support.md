---
description: In diesem Thema wird beschrieben, wie Windows Search mehrere Sprachen unterstützt.
ms.assetid: a800d2ac-3aee-4e74-a29a-a70355138ebc
title: Von Windows Search unterstützte Sprachen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 812252fa6815bb8f32df684b51d4f39bca4105d7997b07bd930ab761cb082f91
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119396540"
---
# <a name="languages-supported-by-windows-search"></a>Von Windows Search unterstützte Sprachen

In diesem Thema wird beschrieben, wie Windows Search mehrere Sprachen unterstützt.

## <a name="tokenization-wordbreakers-and-language-resources"></a>Tokenisierung, Wordbreakers und Sprachressourcen

Windows Die Suche ist sprachunabhängig, aber die Genauigkeit der Suche in verschiedenen Sprachen kann aufgrund der Art und Weise variieren, in der Wordbreaker Text tokenisieren. Wordbreaker implementieren verschiedene Tokenisierungsregeln für Sprachen und teilen Text in einzelne Token oder Wörter auf, die indiziert oder durchsucht werden sollen.

Sowohl die Sprache des indizierten Texts als auch die Abfragezeichenfolge werden in Token unterteilt. Da Tokenisierungsregeln je nach Sprache variieren, gibt es separate Wörtertrennungen für jede Sprache oder Familie von Sprachen. Wenn zwischen der Abfragesprache und der indizierten Sprache ein Konflikt besteht, können die Ergebnisse unvorhersehbar sein.

Windows Die Suche enthält einen klar definierten Satz von Wörterbreakern. Klassische Wordbreaker- und Wortstammschutzkomponenten werden in Windows Vista und höher unterstützt. Wenn die Sprache eines Dokuments nicht bestimmt werden kann, versucht Windows Search, die Sprache zu erkennen, um den am besten geeigneten Wordbreaker zu identifizieren. Windows Bei der Suche wird versucht, die Sprache zu erkennen, indem die [**GetSystemPreferredUILanguages-Funktion**](/windows/win32/api/winnls/nf-winnls-getsystempreferreduilanguages) aufgerufen wird, um die erste LANGUAGE-Sprache (MULTIPLE Benutzeroberfläche) zu bestimmen (die in der Regel die Sprache der Systembenutzeroberfläche ist, es sei denn, DIE LANGUAGE Packs sind installiert). Wenn dieser Aufruf erfolgreich ist, wird der Wordbreaker für die erste LANGUAGE LANGUAGE verwendet. Wenn beim Aufruf von **GetSystemPreferredUILanguages** ein Fehler auftritt, ruft Windows Search das Systemschema ab, indem die [**GetSystemDefaultLCID-Funktion**](/windows/win32/api/winnls/nf-winnls-getsystemdefaultlcid) aufgerufen wird, und verwendet den wordbreaker, der diesem Gebietsschema zugeordnet ist.

Wenn kein Wordbreaker für eine Sprache installiert ist, unterbricht Windows Suche den Leerraum mithilfe des **neutralen** Wortbreakers.

Sie können eine Sprache über die Registrierung entfernen, wie im folgenden Beispiel veranschaulicht.

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Control
            ContentIndex
               Language
                  Dutch_Dutch
                     (Default)
                     Locale
                     NoiseFile
                     StemmerClass = CLSID
                     WBreakerClass = CLSID
```

> [!TIP]
> Wenn Sie Änderungen an der Registrierung vornehmen, starten Sie Windows Suchen neu.

 

Wenn Windows Search einen neuen Wordbreaker erfordert, wird der Klassenbezeichner (CLSID) gelesen, und der instanziierte Wordbreaker wird zwischengespeichert.

Sie können einen benutzerdefinierten Wordbreaker für eine Sprache erstellen, indem Sie die [**IWordBreaker-Schnittstelle**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordbreaker) implementieren. Windows Die Suche ruft dann die **IWordBreaker-Methoden** auf, wenn Inhaltsindizes erstellt und Abfragen ausgeführt werden.

Gebietsschemainformationen für indizierten Inhalt werden aus der Quelle des Inhalts abgerufen. Wenn der Quell implementer das Gebietsschema des indizierten Inhalts nicht kennt, sollte das Gebietsschema auf [**LOCALE \_ NEUTRAL**](../intl/locale-neutral.md)festgelegt werden.

Wenn Sie beispielsweise einen Filterhandler (eine Implementierung der [**IFilter-Schnittstelle),**](https://www.bing.com/search?q=**IFilter**) einen Eigenschaftenhandler oder einen Protokollhandler implementieren, sollten Sie das Gebietsschema für indizierten Inhalt auf [**LOCALE \_ NEUTRAL**](../intl/locale-neutral.md) festlegen, es sei denn, Sie verfügen über bestimmte Gebietsschemainformationen und sind sich dessen Genauigkeit sicher.

> [!TIP]
> Wenn eine Indexabfrage auf Benutzereingaben basiert, sollte das Gebietsschema mit der Sprache übereinstimmen, in die der Benutzer eingibt. Sie können dieses Gebietsschema ermitteln, indem Sie die [**GetKeyboardLayout-Funktion**](/windows/win32/api/winuser/nf-winuser-getkeyboardlayout) aufrufen.

 

## <a name="languages-supported-by-wordbreakers"></a>Von Wordbreakers unterstützte Sprachen

Windows Die Suche umfasst Wörterbreaker, um die folgenden Sprachen zu unterstützen.



| Registrierungsschlüssel             | Sprache (Untersprache)                            | LCID   |
|--------------------------|---------------------------------------------------|--------|
| **\_Arabisch–ArabischArabia**  | Arabisch (neutral)                                  | 0x0001 |
| **Default \_ (Standardwert)**     | Pausieren (neutral)                                  | 0x0045 |
| **Standardeinstellung \_ "100"**   | Bulgarisch (Bulgarien)                              | 0x0402 |
| **\_Default (Standardeinstellung)**     | Katalanisch (Katalanisch)                                 | 0x0403 |
| **Chinesisch \_ (Hongkong)**    | Chinesisch (Hongkong SAR, VR China)                      | 0x0C04 |
| **\_Chinesisch (vereinfacht)**  | Chinesisch (vereinfacht)                              | 0x0804 |
| **\_Chinesisch (traditionell)** | Chinesisch (traditionell)                             | 0x0404 |
| **Standardeinstellung \_ "100"**    | Kroatisch (Kroatien)                                | 0x041A |
| **Tschechisch \_ (Standard)**       | Tschechisch (Tschechische Republik)                            | 0x0405 |
| **Standard für Dänisch \_**      | Dänisch (Dänemark)                                  | 0x0406 |
| **\_Niederländisch (Niederländisch)**         | Niederländisch (Niederlande)                               | 0x0413 |
| **Englisch \_ (Vereinigtes Königreich)**          | Walisisch (Großbritannien)                          | 0x0809 |
| **Englisch \_ (USA)**          | Englisch (USA)                           | 0x0409 |
| **Default \_ (Finnisch, Standard)**     | Finnisch (Finnland)                                 | 0x040B |
| **\_Französisch (Französisch)**       | Französisch (Frankreich)                                   | 0x040C |
| **\_Deutsch**       | Deutsch (Deutschland)                                  | 0x0407 |
| **Griechisch \_ (Standard)**       | Griechisch (Griechenland)                                    | 0x0408 |
| **\_Gujarati-Standard**    | Gujarati (Indien)                                  | 0x0447 |
| **Hebräische \_ Standardeinstellung**      | Hebräisch (neutral)                                  | 0x000D |
| **\_Hindi-Standard**       | Hindi (Indien)                                     | 0x0439 |
| **Ungarisch \_ (Standard)**   | Ungarisch (Ungarn)                               | 0x040E |
| **Islandser \_ Standardwert**   | Isländisch (Island)                               | 0x040F |
| **Indonesische \_ Standardeinstellung**  | Indonesisch (Indonesien)                            | 0x0421 |
| **Italienisch \_ (Italienisch)**     | Italienisch (Italien)                                   | 0x0410 |
| **Japanischer \_ Standardwert**    | Japanisch (Japan)                                  | 0x0411 |
| **Kannada \_ Default**     | Kannada (Indien)                                   | 0x044B |
| **Koreanisch \_ (Standard)**      | Koreanisch (Korea)                                    | 0x0412 |
| **Standardmäßiger \_ Standardwert**     | Lettisch (Lettland)                                  | 0x0426 |
| **Standardmäßiger \_ Standardwert**  | Litauisch (Litauisch)                           | 0x0427 |
| **\_Malaiisch-Australien**      | Malaiisch (Malaysia)                                  | 0x043E |
| **\_Mallam-Standardwert**   | Mallamlam (neutral)                               | 0x004C |
| **Marathi \_ Default**     | Marathi (Indien)                                   | 0x044E |
| **Norwegisch \_ Bokmal**    | Norwegisch, Bokmål (Norwegen)                        | 0x0414 |
| **Polnisch \_ (Standard)**      | Polnisch (Polen)                                   | 0x0415 |
| **Portugiesisch \_ (Portugal)** | Portugiesisch (Portugal)                             | 0x0816 |
| **Portugiesisch \_ (Brasilien)**   | Portugiesisch (Brasilien)                               | 0x0416 |
| **Punjabi-Standard \_**     | Punjabi (Indien)                                   | 0x0446 |
| **Standardmäßige \_ Standardeinstellungen**    | Rumänisch (Rumänien)                                | 0x0418 |
| **Russisch \_ (Standard)**     | Russisch (neutral)                                 | 0x0019 |
| **\_Kyrillisch (Kyrillisch)**    | Serbisch (Früher, Kyrillisch) | 0x0C1A |
| **\_Lateinisch (Serbisch)**       | Serbisch (Früher, Serbisch, Lateinisch)    | 0x081A |
| **Standardeinstellung \_ "Slowakisch"**      | Slowakisch (Slowakei)                                 | 0x041B |
| **Standardmäßiger \_ Standardwert**   | Slowenisch (Slowenien)                              | 0x0424 |
| **Spanisch \_ Modern**      | Spanisch (Spanien, Moderne Sortierung)                      | 0x0C0A |
| **Standardwert \_ für "Schwedisch"**     | Schwedisch (Schweden)                                  | 0x041D |
| **\_Standardeinstellung**       | Tamil (Indien)                                     | 0x0449 |
| **Telugu-Standard \_**      | Telugu (Indien)                                    | 0x044A |
| **\_Thailändisch Standard**        | Thai (Thailand)                                   | 0x041E |
| **Türkisch \_ (Standardeinstellung)**     | Türkisch (Türkei)                                  | 0x041F |
| **Standardmäßige \_ Standardeinstellungen**   | Ukrainisch (Ukraine)                               | 0x0422 |
| **Urdu \_ Default**        | Urdu (Pakistan)                                   | 0x0420 |
| **\_Standardeinstellung**  | Vietnamesisch (Vietnam)                              | 0x042A |



 

> [!Note]  
> LCIDs für einige Sprachen in der Tabelle werden mithilfe des Sprachbezeichners, des Untersprachebezeichners und des Sortierbezeichners generiert.

 

Weitere Informationen zu Sprachen und zugeordneten Bezeichnern finden Sie unter [Sprachbezeichnerkonst konstanten und Zeichenfolgen](../intl/language-identifier-constants-and-strings.md).

> [!Note]  
> Es gibt keine Garantie, dass alle diese Sprachregistrierungsschlüssel auf einem bestimmten Computer vorhanden sind. Der Wordbreaker für eine beliebige Sprache kann je nach Benutzereinstellungen auf dem Computer installiert sein.

 

**Ab Windows 8.1** die bevorzugte Methode zur Verwendung von Wordbreakern über die WinRT-API-WordsSegmenter-Klasse . [](/uwp/api/Windows.Data.Text.WordsSegmenter?view=winrt-19041)

## <a name="additional-resources"></a>Weitere Ressourcen

-   Informationen zum Implementieren und Verwenden von benutzerdefinierten Wörterumbrüchen und Wortstammlern für zusätzliche Sprachen und Windows finden Sie unter Erweitern von [Sprachressourcen in Windows Search.](extending-language-resources-in-windows-search.md)
-   Wenn Sie die Sprache eines Texts identifizieren müssen, können Sie die automatische Spracherkennung (Language Auto-Detection, LAD) verwenden, die in Windows 7 und höher verfügbar ist. Weitere Informationen finden Sie unter [Erweiterte linguistische Dienste](../intl/extended-linguistic-services.md) (ELS).
-   Informationen zum Verwalten, Abfragen und Erweitern des Indexes finden Sie im Windows [Search Developer es Guide (Entwicklerhandbuch für die Suche).](-search-developers-guide-entry-page.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Übersicht über Windows Search](-search-3x-wds-overview.md)
</dt> <dt>

[Windows Search als Entwicklungsplattform](-search-3x-wds-development-ovr.md)
</dt> <dt>

[Verwenden von verwaltetem Code mit Shelldaten und Windows Search](-search-3x-wds-managed-code.md)
</dt> </dl>

 

 
