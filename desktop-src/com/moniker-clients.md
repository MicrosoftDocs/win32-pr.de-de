---
title: Monikerclients
description: Monikerclients müssen zunächst einen Moniker erhalten, und es gibt mehrere Möglichkeiten, wie ein monikerclient einen Moniker erhalten kann.
ms.assetid: ab1758c4-8dfc-47f6-8e1b-875e033a54d6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b8435389539f39d8ce71246267cd265c3e4edb9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341422"
---
# <a name="moniker-clients"></a>Monikerclients

Monikerclients müssen zunächst einen Moniker erhalten, und es gibt mehrere Möglichkeiten, wie ein monikerclient einen Moniker erhalten kann. Wenn z. b. der Endbenutzer in OLE-Verbund Dokumenten ein verknüpftes Element erstellt (entweder mithilfe des Dialog Felds " **Objekt einfügen** ", der Zwischenablage oder Drag & amp; Drop), wird ein Moniker als Teil des verknüpften Elements eingebettet. In diesem Fall hat der Programmierer minimalen Kontakt mit Monikern. Wenn Sie über einen Schnittstellen Zeiger auf ein Objekt verfügen, das die [**IMoniker**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) -Schnittstelle implementiert, können Sie dieses Programm gesteuert verwenden, um einen Moniker zu erhalten, und es gibt Methoden für andere Schnittstellen, die für die Rückgabe von Monikern definiert sind.

Es gibt verschiedene Arten von Monikern, die zur Identifizierung verschiedener Arten von Objekten verwendet werden, aber für einen monikerclient sehen alle Moniker identisch aus. Ein monikerclient ruft einfach [**IMoniker:: bindjeobject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) für einen Moniker auf und Ruft einen Schnittstellen Zeiger auf das Objekt ab, das der Moniker identifiziert. Unabhängig davon, ob der Moniker ein Objekt so groß wie ein gesamtes Arbeitsblatt oder so klein wie eine einzelne Zelle in einer Kalkulations Tabelle identifiziert, gibt der Aufruf von **BindToObject** einen Zeiger auf dieses Objekt zurück. Wenn das Objekt bereits ausgeführt wird, wird es von **bindtoken** im Arbeitsspeicher gefunden. Wenn das Objekt passiv auf dem Datenträger gespeichert wird, findet " **BindTo Object** " einen Server für dieses Objekt, führt den Server aus und versetzt den Server in den Status "wird ausgeführt". Alle Details des Bindungs Prozesses werden im monikerclient ausgeblendet. Daher ist es für einen monikerclient sehr einfach, den Moniker zu verwenden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Monikeranbieter](moniker-providers.md)
</dt> <dt>

[OLE-Monikerimplementierungen](ole-moniker-implementations.md)
</dt> </dl>

 

 




