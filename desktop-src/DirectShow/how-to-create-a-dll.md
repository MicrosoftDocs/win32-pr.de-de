---
description: Erstellen einer DirectShow-Filter-DLL
ms.assetid: 142bc8a2-240d-418f-9374-62d34a76ec38
title: Erstellen einer DirectShow-Filter-DLL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 443f8aff88cf73198ed7c417da77f6febf33e18806efba5431e18117ddd2c32e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079010"
---
# <a name="how-to-create-a-directshow-filter-dll"></a>Erstellen einer DirectShow-Filter-DLL

In diesem Artikel wird beschrieben, wie Sie eine Komponente als Dll (Dynamic Link Library) in Microsoft DirectShow implementieren. Dieser Artikel ist eine Fortsetzung von How to Implement IUnknown ( Implementieren von [IUnknown).](how-to-implement-iunknown.md)Darin wird beschrieben, wie Sie die **IUnknown-Schnittstelle** implementieren, indem Sie Ihre Komponente von der [**CUnknown-Basisklasse**](cunknown.md) ableiten.

Dieser Artikel enthält folgende Abschnitte.

-   [Klassenfactorys und Factoryvorlagen](class-factories-and-factory-templates.md)
-   [Factoryvorlagenarray](factory-template-array.md)
-   [DLL-Funktionen](dll-functions.md)

Das Registrieren eines DirectShow-Filters (im Gegensatz zu einem generischen COM-Objekt) erfordert einige zusätzliche Schritte, die in diesem Artikel nicht behandelt werden. Informationen zum Registrieren von Filtern finden Sie unter [Registrieren von DirectShow-Filtern.](how-to-register-directshow-filters.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow und COM](directshow-and-com.md)
</dt> </dl>

 

 



