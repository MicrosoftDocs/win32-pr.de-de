---
description: Erstellen einer DirectShow-Filter-dll
ms.assetid: 142bc8a2-240d-418f-9374-62d34a76ec38
title: Erstellen einer DirectShow-Filter-dll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee964115e040d11ae10562b05899b2895f03d2fe
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106344771"
---
# <a name="how-to-create-a-directshow-filter-dll"></a>Erstellen einer DirectShow-Filter-dll

In diesem Artikel wird beschrieben, wie eine Komponente in Microsoft DirectShow als Dynamic Link Library (dll) implementiert wird. Dieser Artikel ist eine Fortsetzung der [Implementierung von IUnknown](how-to-implement-iunknown.md), in der beschrieben wird, wie Sie die **IUnknown** -Schnittstelle implementieren, indem Sie die Komponente von der [**cunknown**](cunknown.md) -Basisklasse ableiten.

Dieser Artikel enthält folgende Abschnitte.

-   [Klassen-und factoryvorlagen](class-factories-and-factory-templates.md)
-   [Factory-Vorlagen Array](factory-template-array.md)
-   [DLL-Funktionen](dll-functions.md)

Das Registrieren eines DirectShow-Filters (im Gegensatz zu einem generischen com-Objekt) erfordert einige zusätzliche Schritte, die in diesem Artikel nicht behandelt werden. Weitere Informationen zum Registrieren von Filtern finden [Sie unter Registrieren von DirectShow-Filtern](how-to-register-directshow-filters.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow und com](directshow-and-com.md)
</dt> </dl>

 

 



