---
description: Locale \_ S1159 und locale \_ Sam
ms.assetid: dc7058af-1d5f-40a0-8d0b-17d2ff5662ce
title: LOCALE_S1159 und LOCALE_SAM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6b41f98ea5c07f1d88534c1e47acecfa81a4e62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867052"
---
# <a name="locale_s1159-and-locale_sam"></a>Locale \_ S1159 und locale \_ Sam

Zeichenfolge für den am-Kenn Zeichner (erste 12 Stunden des Tages). Die maximale Anzahl von Zeichen, die für diese Zeichenfolge zulässig sind, einschließlich eines abschließenden NULL-Zeichens, unterscheidet sich für unterschiedliche Versionen von Windows.

**Windows XP:** 13 einschließlich eines abschließenden NULL-Zeichens für [**SetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-setlocaleinfoa). 15 einschließlich eines abschließenden NULL-Zeichens für [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa).

**Windows Me/98/95, Windows NT 4,0, Windows 2000:** 9 einschließlich eines abschließenden NULL-Zeichens.

**Windows Server 2003 und höher:** 15 einschließlich eines abschließenden NULL-Zeichens.

Windows 10 hat den Wert **locale \_ Sam** als ein besser lesbares Synonym für **locale \_ S1159** hinzugefügt.

 

 



