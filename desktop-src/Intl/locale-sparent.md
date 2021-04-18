---
description: LOCALE- \_ sparent
ms.assetid: 3fa0bc36-7577-4b5a-b557-8ac42e8594a8
title: LOCALE_SPARENT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f35a774c6a7f8eea631a2d6579b97058b30acdfe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350819"
---
# <a name="locale_sparent"></a>LOCALE- \_ sparent

**Windows Vista und höher:** Ein Fallback-Gebiets Schema, das vom Ressourcen Lade Modul verwendet wird. Die maximale Anzahl von Zeichen, die für diese Zeichenfolge zulässig ist, ist 85, einschließlich eines abschließenden NULL-Zeichens.

Gebiets Schemas haben eine Hierarchie, in der das übergeordnete Element eines bestimmten Gebiets Schemas ein neutrales Gebiets Schema Ein bestimmtes Gebiets Schema ist sowohl einer Sprache als auch einem Land/einer Region zugeordnet, während ein neutrales Gebiets Schema einer Sprache zugeordnet ist, aber keinem Land/keiner Region zugeordnet ist. Das übergeordnete Gebiets Schema wird verwendet, um den ersten Fall Back zu entscheiden, der ausprobiert werden soll, wenn eine Ressource für ein bestimmtes Gebiets Schema nicht verfügbar ist. Das übergeordnete Gebiets Schema für "en-US" (0x0409) lautet z. b. "en" (0x0009). Wenn eine Ressource für das spezifische Gebiets Schema "en-US" nicht verfügbar ist, greift das Ressourcen Lade Modul auf die Ressource zurück, die für das neutrale Gebiets Schema "en" verfügbar ist. Weitere Informationen zur Fall Back Strategie für den Ressourcen Ladedienst finden Sie unter [Benutzeroberflächen-sprach Verwaltung](user-interface-language-management.md) .

Dieses Muster ist für vordefinierte Gebiets Schemata einheitlich. Das übergeordnete Gebiets Schema wird jedoch nicht durch eine Manipulation des Gebiets Schema namens bestimmt. Das heißt, [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) und [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) analysieren eine Zeichenfolge, z. b. "en-US", nicht, um den Wert "en" zu erhalten. Stattdessen sehen Sie sich die gespeicherten Gebiets Schema Daten an. Bei vordefinierten Gebiets Schemata folgt der Wert dem erwarteten Muster, bei dem das übergeordnete Element eines bestimmten Gebiets Schemas das entsprechende neutrale Gebiets Schema und das übergeordnete Element eines neutralen Gebiets Schemas das invariante Gebiets Schema ist. Es wird empfohlen, dass benutzerdefinierte Gebiets Schemas eine ähnliche Strategie hinsichtlich der Definition ihres übergeordneten Gebiets Schemas befolgen. Dies wird jedoch nicht erzwungen. Die Anwendung, die ein benutzerdefiniertes Gebiets Schema implementiert, kann ein weniger offensichtlich entsprechendes übergeordnetes

> [!Note]  
> Da keine der Funktionen, die unter [Aufrufen der "locale Name"-Funktion](calling-the--locale-name--functions.md) beschrieben werden, neutrale Gebiets Schemas als Eingaben akzeptieren, sind diese Gebiets Schema \_ Daten sehr eingeschränkt. Vor allem kann weder [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) noch [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) neutrale Gebiets Schemas als Eingaben akzeptieren.

 

 

 



