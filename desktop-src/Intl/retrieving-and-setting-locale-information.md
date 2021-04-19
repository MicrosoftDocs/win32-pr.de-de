---
description: Abrufen und Festlegen von Gebiets Schema Informationen
ms.assetid: 7675f826-76be-4361-a82c-9573040a7e72
title: Abrufen und Festlegen von Gebiets Schema Informationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9f9faa8749073016862587330776f32e65749b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346300"
---
# <a name="retrieving-and-setting-locale-information"></a>Abrufen und Festlegen von Gebiets Schema Informationen

Die Anwendung muss in der Lage sein, bestimmte Informationen zu verfügbaren Gebiets Schemata [und Sprachen](locales-and-languages.md)abzurufen und festzulegen. Jedes Element von Gebiets Schema Informationen, z. b. der Name eines bestimmten Wochentags oder das Zeichen, das als Dezimaltrennzeichen verwendet wird, verfügt über eine entsprechende Konstante. Die verfügbaren Konstanten werden in den Gebiets Schema [Informations Konstanten](locale-information-constants.md)definiert.

Die Gebiets Schema Informationen werden von Ihrer Anwendung immer als eine mit NULL endenden Zeichenfolge gespeichert und manipuliert. Binäre Daten sind nicht zulässig, und alle numerischen Werte müssen als Text angegeben werden. Jede Art von Informationen hat ein bestimmtes Format. Außerdem werden mehrere Typen miteinander verknüpft, sodass durch das Ändern eines Typs auch der Wert des anderen Typs geändert wird.

Zum Abrufen von Gebiets Schema Informationen Ruft die Anwendung [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) oder [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) mit der Konstante auf, die den erforderlichen Informationen entspricht. Die Anwendung kann [**SetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-setlocaleinfoa) aufrufen, um ein Element mit Gebiets Schema Informationen festzulegen.

> [!Note]  
> Obwohl ein Gebiets Schema [Bezeichner](locale-identifiers.md) unterstützt werden kann, ist er nicht für die Verwendung durch eine Anwendung verfügbar, es sei denn, das entsprechende Gebiets Schema ist ebenfalls installiert.

 

Da die meisten Gebiets Schema Informations Konstanten sich gegenseitig ausschließen, kann jeweils nur ein Typ von Informationen verarbeitet werden. Die Ausnahmen für diese Regel sind [locale \_ \_ \_ ACP](locale-use-cp-acp.md), locale [ \_ Return \_ Number](locale-return-constants.md)und [locale \_ nouseroverride](locale-nouseroverride.md), die mit anderen Konstanten kombiniert werden können, die eine Binärdatei oder verwenden.

> [!Caution]  
> Es wird dringend davon abgeraten, Gebiets Schema \_ nominserüberschreibung zu verwenden, da die Benutzereinstellungen deaktiviert werden.

 

Wie eine Reihe von Anwendungen, z. b. Microsoft Active Directory, kann Ihre Anwendung ihre Zeichen folgen in einer sortierbaren Datenbank beibehalten. Weitere Informationen finden Sie unter [Handling Sortieren in Ihren Anwendungen](handling-sorting-in-your-applications.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden der Unterstützung für nationale Sprache](using-national-language-support.md)
</dt> <dt>

[Gebiets Schema Informations Konstanten](locale-information-constants.md)
</dt> <dt>

[Behandeln von Sortierungen in Ihren Anwendungen](handling-sorting-in-your-applications.md)
</dt> <dt>

[Arbeiten mit benutzerdefinierten Gebiets Schemas](working-with-custom-locales.md)
</dt> </dl>

 

 



