---
description: LOCALE \_ SPARENT
ms.assetid: 3fa0bc36-7577-4b5a-b557-8ac42e8594a8
title: LOCALE_SPARENT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11383e6fcdd216a1837d9f2f31e70a26821d394c3c56ea614b1df197bbe35c76
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105920"
---
# <a name="locale_sparent"></a>LOCALE \_ SPARENT

**Windows Vista und höher:** Fallback-Gebietsschema, das vom Ressourcenladeprogramm verwendet wird. Die maximale Anzahl von Zeichen, die für diese Zeichenfolge zulässig sind, beträgt 85, einschließlich eines abschließenden NULL-Zeichens.

Gebietsschemas verfügen über eine Hierarchie, in der das übergeordnete Element eines bestimmten Gebietsschemas ein neutrales Gebietsschema ist. Ein bestimmtes Gebietsschema ist sowohl einer Sprache als auch einem Land/einer Region zugeordnet, während ein neutrales Gebietsschema einer Sprache, aber keinem Land/keiner Region zugeordnet ist. Das übergeordnete Gebietsschema wird verwendet, um zu entscheiden, ob der erste Fallback versucht werden soll, wenn eine Ressource für ein bestimmtes Gebietsschema nicht verfügbar ist. Das übergeordnete Gebietsschema für "en-US" (0x0409) ist beispielsweise "en" (0x0009). Wenn eine Ressource für das spezifische Gebietsschema "en-US" nicht verfügbar ist, greift das Ressourcenladeprogramm zurück, um die Ressource zu verwenden, die für das neutrale Gebietsschema "en" verfügbar ist. Weitere Informationen zur Fallbackstrategie für Ressourcenlader finden Sie unter [Benutzeroberfläche Language Management.](user-interface-language-management.md)

Dieses Muster ist für vordefinierte Gebietsschemas konsistent. Das übergeordnete Gebietsschema wird jedoch nicht durch eine Bearbeitung des Gebietsschemanamens bestimmt. Das heißt, [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) und [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) analysieren keine Zeichenfolge wie "en-US", um den Wert "en" abzurufen. Stattdessen sehen sie sich die gespeicherten Gebietsschemadaten an. Bei vordefinierten Gebietsschemas folgt der Wert dem erwarteten Muster, bei dem das übergeordnete Element eines bestimmten Gebietsschemas das entsprechende neutrale Gebietsschema und das übergeordnete Gebietsschema eines neutralen Gebietsschemas das invariante Gebietsschema ist. Es wird zwar empfohlen, dass benutzerdefinierte Gebietsschemas eine ähnliche Strategie in Bezug auf die Definition ihres übergeordneten Gebietsschemas verfolgen, dies wird jedoch nicht erzwungen. Die Anwendung, die ein benutzerdefiniertes Gebietsschema implementiert, kann ein weniger offensichtlich geeignetes übergeordnetes Element angeben.

> [!Note]  
> Da keine der unter Aufrufen der Funktion ["Gebietsschemaname"](calling-the--locale-name--functions.md) beschriebenen Funktionen neutrale Gebietsschemas als Eingaben akzeptiert, sind diese LOCALE \_ SPARENT-Daten nur sehr eingeschränkt zu verwenden. Insbesondere akzeptieren weder [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) noch [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) neutrale Gebietsschemas als Eingaben.

 

 

 



