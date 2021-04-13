---
title: Dateimoniker
description: Dateimoniker
ms.assetid: 923f798d-d789-4e6d-b27e-dd5a72f92abf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5c18beeff04804b11f04c0a2c211f2dd09dd60d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309635"
---
# <a name="file-monikers"></a>Dateimoniker

*Dateimoniker* sind die einfachste Monikerklasse. Dateimoniker können verwendet werden, um alle Objekte zu identifizieren, die in einer eigenen Datei gespeichert sind. Ein dateimoniker fungiert als Wrapper für den Pfadnamen, den das systemeigene Dateisystem der Datei zuweist. Das Aufrufen von [**IMoniker:: BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) für diesen Moniker würde dazu führen, dass dieses Objekt aktiviert wird und dann einen Schnittstellen Zeiger auf das-Objekt zurückgibt. Die Quelle des Objekts, das vom Moniker benannt wird, muss eine Implementierung der [**IPersistFile**](/windows/desktop/api/ObjIdl/nn-objidl-ipersistfile) -Schnittstelle bereitstellen, um die Bindung eines dateimonikers zu unterstützen. Dateimoniker können entweder einen kompletten oder einen relativen Pfad darstellen.

Beispielsweise würde der dateimoniker für ein Tabellenobjekt, das als Datei C: WorkMySheet.xls gespeichert ist, Informationen enthalten, die dem \\ \\ Pfadnamen entsprechen. Der Moniker würde jedoch nicht notwendigerweise aus derselben Zeichenfolge bestehen. Die Zeichenfolge ist nur Ihr *Display Name*, eine Darstellung der Inhalte des Monikers, die für einen Endbenutzer von Bedeutung sind. Der Anzeige Name, der über die [**IMoniker:: GetDisplayName**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-getdisplayname) -Methode verfügbar ist, wird nur verwendet, wenn ein Moniker für einen Endbenutzer angezeigt wird. Diese Methode ruft den anzeigen Amen für jede der Monikerklassen ab. Intern kann der Moniker die gleichen Informationen in einem Format speichern, das für die Ausführung von monikervorgängen effizienter ist, aber für Benutzer nicht sinnvoll ist. Wenn das gleiche Objekt dann durch einen Aufrufen der [**BindTo Object**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) -Methode gebunden wird, wird das Objekt aktiviert, wahrscheinlich durch Laden der Datei in das Arbeitsblatt.

OLE bietet monikeranbietern die Hilfsfunktion " [**kreatefilemoniker**](/windows/desktop/api/Objbase/nf-objbase-createfilemoniker) ", die ein dateimonikerobjekt erstellt und seinen Zeiger auf den Anbieter zurückgibt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Anti-Moniker](anti-monikers.md)
</dt> <dt>

[Klassenmoniker](class-monikers.md)
</dt> <dt>

[Zusammengesetzte Moniker](composite-monikers.md)
</dt> <dt>

[Elementmoniker](item-monikers.md)
</dt> <dt>

[Zeigermoniker](pointer-monikers.md)
</dt> </dl>

 

 




