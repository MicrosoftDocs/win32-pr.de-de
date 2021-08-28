---
description: Für NLS, Sortierung (auch als \# 0034 &;Sortierung&\# 0034;) ist die Anordnung von Zeichenfolgen.
ms.assetid: 8ca3af60-1ddb-4bfb-8aa6-8db769b3982d
title: Sortieren (Internationalisierung)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3dbedf872c953a45ca7064eccd4ba16019a857c35186261695e094be03cd054
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120130210"
---
# <a name="sorting"></a>Sortierung

Für NLS ist die Sortierung (auch als "Sortierung" bezeichnet) die Anordnung von Zeichenfolgen. Es gibt zwei Arten der Sortierung:

-   Linguistische Sortierung. Ordnet Zeichenfolgen mit ähnlichen linguistischen Merkmalen in Gruppen an (nach Sortierungen).
-   Ordinalsortierung (nicht linguistisch). Ordnet die Zeichenfolgen in einer geordneten Sequenz an.

Beim Sortieren werden die NLS-Zeichenfolgenvergleichsfunktionen wie [CompareString](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) und [**LCMapString**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa)oder "Wrapper"-API-Funktionen wie [lstrcmp](/windows/win32/api/winbase/nf-winbase-lstrcmpa)verwendet, die die NLS-Zeichenfolgenvergleichsfunktionen intern aufrufen.

Weitere Informationen zum Implementieren der Sortierung in Ihren Anwendungen finden Sie unter [Handling Sorting in Your Applications](handling-sorting-in-your-applications.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zur Unterstützung der Landessprache](about-national-language-support.md)
</dt> <dt>

[Behandeln der Sortierung in Ihren Anwendungen](handling-sorting-in-your-applications.md)
</dt> <dt>

[**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw)
</dt> <dt>

[LCMapString](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa)
</dt> </dl>

 

 
