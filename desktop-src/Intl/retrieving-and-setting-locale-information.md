---
description: Abrufen und Festlegen von Gebietsschemainformationen
ms.assetid: 7675f826-76be-4361-a82c-9573040a7e72
title: Abrufen und Festlegen von Gebietsschemainformationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d02c2bb58328529781309ce8284310acbcb6fb545ecdc076df295cd020344a4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120130310"
---
# <a name="retrieving-and-setting-locale-information"></a>Abrufen und Festlegen von Gebietsschemainformationen

Die Anwendung muss bestimmte Informationen zu [verfügbaren Gebietsschemas und Sprachen](locales-and-languages.md)abrufen und festlegen können. Jedes Element von Gebietsschemainformationen, z. B. der Name eines bestimmten Wochentags oder das als Dezimaltrennzeichen verwendete Zeichen, verfügt über eine entsprechende Konstante. Die verfügbaren Konstanten werden in [Gebietsschemainformationskonstanten](locale-information-constants.md)definiert.

Ihre Anwendung speichert und bearbeitet Gebietsschemainformationen immer als auf NULL endende Zeichenfolge. Binärdaten sind nicht zulässig, und alle numerischen Werte müssen als Text angegeben werden. Jeder Informationstyp hat ein bestimmtes Format. Darüber hinaus sind mehrere Typen miteinander verknüpft, sodass das Ändern eines Typs auch den Wert des anderen Typs ändert.

Um Gebietsschemainformationen abzurufen, ruft die Anwendung [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) oder [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) mit der Konstante auf, die den erforderlichen Informationen entspricht. Die Anwendung kann [**SetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-setlocaleinfoa) aufrufen, um ein Element mit Gebietsschemainformationen festzulegen.

> [!Note]  
> Obwohl ein [Gebietsschemabezeichner](locale-identifiers.md) möglicherweise unterstützt wird, ist er nicht für die Verwendung durch eine Anwendung verfügbar, es sei denn, das entsprechende Gebietsschema ist ebenfalls installiert.

 

Da sich die meisten Gebietsschemainformationskonstanten gegenseitig ausschließen, kann jeweils nur ein Informationstyp verarbeitet werden. Ausnahmen von dieser Regel sind [LOCALE \_ USE CP \_ \_ ACP,](locale-use-cp-acp.md) [LOCALE RETURN \_ \_ NUMBER](locale-return-constants.md)und [LOCALE \_ NOUSEROVERRIDE](locale-nouseroverride.md), die mit anderen Konstanten mit einem binären OR kombiniert werden können.

> [!Caution]  
> Von der Verwendung von LOCALE \_ NOUSEROVERRIDE wird dringend abgeraten, da benutzereinstellungen deaktiviert werden.

 

Wie eine Reihe von Anwendungen, z. B. Microsoft Active Directory, kann Ihre Anwendung ihre Zeichenfolgen in einer sortierbaren Datenbank verwalten. Weitere Informationen finden Sie unter [Handling Sorting in Your Applications](handling-sorting-in-your-applications.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden der Unterstützung für nationale Sprachen](using-national-language-support.md)
</dt> <dt>

[Gebietsschemainformationskonstanten](locale-information-constants.md)
</dt> <dt>

[Behandeln der Sortierung in Ihren Anwendungen](handling-sorting-in-your-applications.md)
</dt> <dt>

[Arbeiten mit benutzerdefinierten Gebietsschemas](working-with-custom-locales.md)
</dt> </dl>

 

 



