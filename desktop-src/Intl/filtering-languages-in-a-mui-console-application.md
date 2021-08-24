---
description: Eine CONSOLE-Konsolenanwendung kann entweder Systemeinstellungen oder anwendungsspezifische Einstellungen für ihre Benutzeroberflächensprachen unterstützen. In diesem Thema wird die Filterung von Sprachen für diese Art von Anwendung erläutert.
ms.assetid: 6d3c491f-3f5e-4592-aada-49b8b415b497
title: Filtern von Sprachen in einer CONSOLE-Konsolenanwendung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bcdd8fc0f7f63b5771f5b75b86ce5e76ab2420d407832d77b731ad952174cee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120041320"
---
# <a name="filtering-languages-in-a-mui-console-application"></a>Filtern von Sprachen in einer CONSOLE-Konsolenanwendung

Eine CONSOLE-Konsolenanwendung kann entweder Systemeinstellungen oder anwendungsspezifische Einstellungen für ihre Benutzeroberflächensprachen unterstützen. In diesem Thema wird die Filterung von Sprachen für diese Art von Anwendung erläutert.

## <a name="limit-the-languages-to-display"></a>Einschränken der anzuzeigende Sprachen

Im Gegensatz zu einem grafischen Fenster kann die Windows-Konsole [keine komplexen Skripts](uniscribe-glossary.md)anzeigen, z. B. Arabisch, Hebräisch, Griechisch, Hindi, Urdu, Thai, usw. Daher können viele Sprachen der Benutzeroberfläche unter keinen Umständen von der Konsole angezeigt werden.

Die Konsole kann nur Zeichen von der einzelnen [OEM-Codepage](code-pages.md) anzeigen, die der aktuellen Sprache für Nicht-Unicode-Anwendungen zugeordnet ist. Für jede OEM-Codepage verwendet die Konsole eine bestimmte Schriftart, und dies bietet möglicherweise keine vollständige Abdeckung für diese Codepage.

Diese konsolenbezogenen Einschränkungen verringern die Anzahl der Benutzeroberflächensprachen, die die Konsole auf einem bestimmten Computer anzeigen kann. Wenn die aktuelle Sprache für Nicht-Unicode-Anwendungen beispielsweise Japanisch ist und der Benutzer versucht, deutschen Text in der Konsole anzuzeigen, werden Zeichen mit Umlauten nicht ordnungsgemäß angezeigt. Wenn die aktuelle Sprache für Nicht-Unicode-Anwendungen Deutsch ist und der Benutzer japanischen Text in der Konsole anzeigen möchte, sind die Ergebnisse viel schlechter, wodurch der Text fast unverständlich wird.

> [!Note]  
> Beachten Sie beim Bereitstellen von Konsolenunterstützung für Ihre CAB-Anwendungen, dass die Konsole nur eingeschränkte Unterstützung für [Eingabemethoden-Editoren](input-method-manager.md)bietet.

 

## <a name="set-the-language-for-console-output"></a>Festlegen der Sprache für die Konsolenausgabe

Auf Windows Vista und höher legt eine Konsolenanwendung die Sprache zur Unterstützung der Konsolenanzeige fest, indem [**SetThreadPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages)aufgerufen wird. In diesem Aufruf übergibt die Anwendung DEN CONSOLE \_ \_ FILTER im *dwFlags-Parameter* und **NULL** für *pwszLanguagesBuffer.* Eine Alternative besteht darin, [**SetThreadUILanguage**](/windows/win32/api/winnls/nf-winnls-setthreaduilanguage) mit dem Sprachbezeichner 0 aufzurufen. Diese Einstellung bewirkt, dass die Funktion die Sprache auswählt, die die Konsolenanzeige am besten unterstützt.

Auf Windows XP kann die Anwendung die Sprache für die Konsolenausgabe nur festlegen, indem [**SetThreadUILanguage**](/windows/win32/api/winnls/nf-winnls-setthreaduilanguage) mit dem Sprachbezeichner 0 aufgerufen wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Festlegen von Einstellungen für die Anwendungssprache](setting-application-language-preferences.md)
</dt> </dl>

 

 
