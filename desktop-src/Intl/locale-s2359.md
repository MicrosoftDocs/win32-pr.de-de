---
description: Locale \_ S2359 und locale \_ SPM
ms.assetid: 8a97073e-84f6-47d9-98fb-65760e8a6cd8
title: LOCALE_S2359 und LOCALE_SPM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca0c22d541102fcdf0826778de591dc4100dda55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106347721"
---
# <a name="locale_s2359-and-locale_spm"></a>Locale \_ S2359 und locale \_ SPM

Zeichenfolge für den pm-Kenn Zeichner (zweite 12 Stunden des Tages). Die maximal zulässige Anzahl von Zeichen für diese Zeichenfolge unterscheidet sich für unterschiedliche Versionen von Windows.

**Windows XP:** 13 einschließlich eines abschließenden NULL-Zeichens für [**SetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-setlocaleinfoa). 15 einschließlich eines abschließenden NULL-Zeichens für [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa).

**Windows Me/98/95, Windows NT 4,0, Windows 2000:** 9 einschließlich eines abschließenden NULL-Zeichens.

**Windows Server 2003 und höher:** 15 einschließlich eines abschließenden NULL-Zeichens.

Windows 10 hat den Wert Gebiets Schema- **\_ SPM** als lesbares Synonym **für \_ locale S2359** hinzugefügt.

 

 



