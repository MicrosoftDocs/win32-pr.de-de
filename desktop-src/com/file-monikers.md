---
title: Dateimoniker
description: Dateimoniker
ms.assetid: 923f798d-d789-4e6d-b27e-dd5a72f92abf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa51d000964bcfe7cad29db333bbbbc68b3a94d0f977c47b29affab4eed0b139
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048288"
---
# <a name="file-monikers"></a>Dateimoniker

*Dateimoniker* sind die einfachste Monikerklasse. Dateimoniker können verwendet werden, um jedes Objekt zu identifizieren, das in einer eigenen Datei gespeichert ist. Ein Dateimoniker fungiert als Wrapper für den Pfadnamen, den das systemeigene Dateisystem der Datei zuweist. Der Aufruf [**von IMoniker::BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) für diesen Moniker würde dazu führen, dass dieses Objekt aktiviert wird und dann einen Schnittstellenzeiger auf das Objekt zurückgibt. Die Quelle des vom Moniker benannten Objekts muss eine Implementierung der [**IPersistFile-Schnittstelle**](/windows/desktop/api/ObjIdl/nn-objidl-ipersistfile) bereitstellen, um das Binden eines Dateimonikers zu unterstützen. Dateimoniker können entweder einen vollständigen oder einen relativen Pfad darstellen.

Beispielsweise würde der Dateimoniker für ein Tabellenkalkulationsobjekt, das als Datei C: Work gespeichert istMySheet.xls, Informationen enthalten, die diesem \\ \\ Pfadnamen entsprechen. Der Moniker würde jedoch nicht unbedingt aus derselben Zeichenfolge bestehen. Die Zeichenfolge ist nur der *Anzeigename*, eine Darstellung des Monikerinhalts, die für einen Endbenutzer von Bedeutung ist. Der Anzeigename, der über die [**IMoniker::GetDisplayName-Methode**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-getdisplayname) verfügbar ist, wird nur verwendet, wenn ein Moniker für einen Endbenutzer angezeigt wird. Diese Methode ruft den Anzeigenamen für eine der Monikerklassen ab. Intern speichert der Moniker möglicherweise die gleichen Informationen in einem Format, das effizienter für die Ausführung von Monikervorgängen ist, aber für Benutzer nicht sinnvoll ist. Wenn dasselbe Objekt dann durch einen Aufruf der [**BindToObject-Methode**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) gebunden wird, wird das Objekt aktiviert, wahrscheinlich durch Laden der Datei in die Kalkulationstabelle.

OLE bietet Monikeranbietern die Hilfsfunktion [**CreateFileMoniker,**](/windows/desktop/api/Objbase/nf-objbase-createfilemoniker) die ein Dateimonikerobjekt erstellt und seinen Zeiger auf den Anbieter zurückgibt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Antimoniker](anti-monikers.md)
</dt> <dt>

[Klassenmoniker](class-monikers.md)
</dt> <dt>

[Zusammengesetzte Moniker](composite-monikers.md)
</dt> <dt>

[Elementmoniker](item-monikers.md)
</dt> <dt>

[Zeigermoniker](pointer-monikers.md)
</dt> </dl>

 

 




