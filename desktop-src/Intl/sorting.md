---
description: Für NLS wird die Sortierung (auch als &\# 0034; COLLATIONS&\# 0034;) bezeichnet. die Anordnung von Zeichen folgen.
ms.assetid: 8ca3af60-1ddb-4bfb-8aa6-8db769b3982d
title: Sortierung (Internationalisierung)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f49a5abb8371a00ad9ee63f929b4aaf4b18b11be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218545"
---
# <a name="sorting"></a>Sortierung

Bei nls ist das Sortieren (auch als "Sortierung" bezeichnet) die Anordnung von Zeichen folgen. Es gibt zwei Arten der Sortierung:

-   Linguistische Sortierung. Ordnet Zeichen folgen mit ähnlichen linguistischen Merkmalen in Gruppen (sortiert) an.
-   Ordnungszahl (nicht linguistisch). Ordnet die Zeichen folgen in einer geordneten Sequenz an.

Die Sortierung verwendet die NLS-Zeichen folgen Vergleichsfunktionen, wie z. b. [CompareString](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) und [**LCMapString**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa), oder Wrapper-API-Funktionen, wie z. b. [lstraucmp](/windows/win32/api/winbase/nf-winbase-lstrcmpa), die intern die NLS-Zeichen folgen Vergleichsfunktionen aufzurufen.

Ausführliche Informationen zum Implementieren von Sortierungen in Ihren Anwendungen finden Sie unter [Handling Sortieren in Ihren Anwendungen](handling-sorting-in-your-applications.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zur Unterstützung der Landessprache](about-national-language-support.md)
</dt> <dt>

[Behandeln von Sortierungen in Ihren Anwendungen](handling-sorting-in-your-applications.md)
</dt> <dt>

[**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw)
</dt> <dt>

[LCMapString](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa)
</dt> </dl>

 

 
