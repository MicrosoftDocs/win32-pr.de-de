---
description: Eine MUI-Konsolenanwendung kann entweder Systemeinstellungen oder anwendungsspezifische Einstellungen für die Sprachen der Benutzeroberfläche unterstützen. In diesem Thema wird das Filtern von Sprachen für diese Art von Anwendung erläutert.
ms.assetid: 6d3c491f-3f5e-4592-aada-49b8b415b497
title: Filtern von Sprachen in einer MUI-Konsolenanwendung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d484835af211f59cc559f8e1cd0dd414af13a8db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865503"
---
# <a name="filtering-languages-in-a-mui-console-application"></a>Filtern von Sprachen in einer MUI-Konsolenanwendung

Eine MUI-Konsolenanwendung kann entweder Systemeinstellungen oder anwendungsspezifische Einstellungen für die Sprachen der Benutzeroberfläche unterstützen. In diesem Thema wird das Filtern von Sprachen für diese Art von Anwendung erläutert.

## <a name="limit-the-languages-to-display"></a>Einschränken der anzuzeigenden Sprachen

Anders als bei einem grafischen Fenster können in der Windows-Konsole [komplexe Skripts](uniscribe-glossary.md)wie Arabisch, Hebräisch, Persian, Hindi, Urdu, Thai und viele andere nicht angezeigt werden. Daher können viele Benutzeroberflächen Sprachen unter keinen Umständen von der Konsole angezeigt werden.

In der Konsole können nur Zeichen von der einzelnen [OEM-Codepage](code-pages.md) angezeigt werden, die der aktuellen Sprache für nicht-Unicode-Anwendungen zugeordnet ist. Für jede OEM-Codepage wird von der Konsole eine bestimmte Schriftart verwendet, und dies kann keine vollständige Abdeckung für diese Codepage bieten.

In diesen Konsolen bezogenen Einschränkungen wird die Anzahl der Benutzeroberflächen Sprachen reduziert, die von der-Konsole auf einem bestimmten Computer angezeigt werden können. Wenn z. b. die aktuelle Sprache für nicht-Unicode-Anwendungen Japanisch ist und der Benutzer versucht, deutschen Text in der Konsole anzuzeigen, werden Zeichen mit Umschlag Zeichen nicht ordnungsgemäß angezeigt. Wenn die aktuelle Sprache für nicht-Unicode-Anwendungen Deutsch ist und der Benutzer japanischen Text in der-Konsole anzeigen möchte, sind die Ergebnisse weitaus schlechter, und der Text wird fast unverständlich.

> [!Note]  
> Beachten Sie beim Bereitstellen von Konsolen Unterstützung für Ihre MUI-Anwendungen, dass die Konsole nur eingeschränkte Unterstützung für [Eingabemethoden-Editoren](input-method-manager.md)bietet.

 

## <a name="set-the-language-for-console-output"></a>Festlegen der Sprache für die Konsolenausgabe

Unter Windows Vista und höher legt eine Konsolenanwendung die Sprache fest, damit die Konsolen Anzeige durch Aufrufen von [**setthreadpreferreduilanguages**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages)unterstützt wird. In diesem Befehl übergibt die Anwendung den MUI \_ \_ -Konsolen Filter im *dwFlags* -Parameter und **null** für *pwszlanguagesbuffer*. Eine Alternative besteht darin, [**setthreaduilanguage**](/windows/win32/api/winnls/nf-winnls-setthreaduilanguage) mit dem sprach Bezeichner 0 (null) aufzurufen. Diese Einstellung bewirkt, dass die Funktion die Sprache auswählt, die die Konsolen Anzeige am besten unterstützt.

Unter Windows XP kann die Anwendung nur die Sprache für die Konsolenausgabe festlegen, indem [**setthreaduilanguage**](/windows/win32/api/winnls/nf-winnls-setthreaduilanguage) mit dem sprach Bezeichner 0 (null) aufgerufen wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Festlegen der Einstellungen für die Anwendungs Sprache](setting-application-language-preferences.md)
</dt> </dl>

 

 
