---
title: Die OLE-Speicherzuweisung
description: Die OLE-Speicherzuweisung
ms.assetid: 026c62e5-c296-4059-b028-77c98fdb77ce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a64fedd610fd8fd6dab0bcd14deb37e04f6df74d
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104102398"
---
# <a name="the-ole-memory-allocator"></a>Die OLE-Speicherzuweisung

Die com-Bibliothek stellt eine Implementierung eines Speicher belegers bereit, der Thread sicher ist. (Das heißt, es können keine Probleme in Multithread-Situationen verursacht werden.) Wenn der Besitz eines zugeordneten Arbeitsspeichers über eine COM-Schnittstelle oder zwischen einem Client und der com-Bibliothek übermittelt wird, müssen Sie diesen com-Allocator verwenden, um den Arbeitsspeicher zuzuordnen. Bei der internen Zuordnung zu einem Objekt können alle gewünschten Zuordnungs Schemas verwendet werden, aber die com-Speicher Belegung ist eine praktische, effiziente und Thread sichere Zuweisung.

Ein Aufrufen der API-Funktion [**CoGetMalloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetmalloc) stellt einen Zeiger auf die OLE-Zuweisung bereit, bei der es sich um eine Implementierung der [**imzuzuordnungsschnittstelle**](/windows/win32/api/objidlbase/nn-objidlbase-imalloc) handelt. Es ist jedoch effizienter, die Hilfsfunktionen [**cotaskmemzuzugsc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc), [**cotaskmemrebelegc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemrealloc)und [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)aufzurufen, die einen Zeiger auf die Arbeitsspeicher Zuweisung einbinden, die entsprechende **imzuzuordnungsmethode** aufrufen und dann den Zeiger auf die Zuweisung freigeben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwalten der Speicher Belegung](managing-memory-allocation.md)
</dt> <dt>

[Die com-Bibliothek](the-com-library.md)
</dt> </dl>

 

 