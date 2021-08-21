---
title: Die FORMATETC-Struktur
description: Die FORMATETC-Struktur ist ein generalisiertes Zwischenablageformat, das erweitert wurde, um ein Zielgerät, einen Aspekt oder eine Ansicht der Daten und ein Speichermedium zu umfassen.
ms.assetid: 46d8988a-4b97-4c86-8b1b-db87044a7e01
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4048b64c8b8d91abf42d43d558d103a2bfd827016c5670c17a082a7ab1fdc87
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118103721"
---
# <a name="the-formatetc-structure"></a>Die FORMATETC-Struktur

Die FORMATETC-Struktur ist ein generalisiertes Zwischenablageformat,  das erweitert wurde, um ein Zielgerät, einen Aspekt oder eine Ansicht der Daten und ein Speichermedium zu umfassen. Ein Datenverbraucher, z. B. eine OLE-Containeranwendung, übergibt die [**FORMATETC-Struktur**](/windows/win32/api/objidl/ns-objidl-formatetc) als Argument in Aufrufen von [**IDataObject,**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) um den Typ der Daten anzugeben, die aus einer Datenquelle stammen, z. B. ein zusammengesetztes Dokumentobjekt. Die Quelle verwendet die **FORMATETC-Struktur,** um zu beschreiben, welche Formate sie bereitstellen kann.

[**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) kann praktisch alle Daten beschreiben, einschließlich anderer Objekte wie Moniker. Ein Container kann eines seiner eingebetteten Objekte bitten, seine Datenformate auflisten, indem er [**IDataObject::EnumFormatEtc**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-enumformatetc)aufruft, das ein Enumeratorobjekt zurückgibt, das die [**IEnumFORMATETC-Schnittstelle**](/windows/desktop/api/ObjIdl/nn-objidl-ienumformatetc) implementiert. Anstatt nur darauf zu antworten, dass es "Text und eine Bitmap" enthält, kann das Objekt eine ausführliche Beschreibung der Daten bereitstellen, einschließlich des Geräts (normalerweise Bildschirm oder Drucker), für das es gerendert wird, des Aspekts, der dem Benutzer angezeigt werden soll (vollständiger Inhalt, Miniaturansicht, Symbol oder formatiert für den Druck) und des Speichermediums, das die Daten enthält (globaler Speicher,  Datenträgerdatei, Speicherobjekt oder Stream). Diese Fähigkeit, Daten genau zu beschreiben, führt zu einer höheren Drucker- und Bildschirmausgabe sowie zu einer höheren Effizienz beim Durchsuchen von Daten, wobei eine Miniaturansicht viel schneller abgerufen und angezeigt werden kann als ein vollständig detailliertes Rendering.

In der folgenden Tabelle sind felder der [**FORMATETC-Datenstruktur**](/windows/win32/api/objidl/ns-objidl-formatetc) und die von ihnen angegebenen Informationen aufgeführt.



| Feld                   | Bedeutung                                                                                                                                                                                                                                                                    |
|-------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **cfFormat**<br/> | Das Format, in dem die Daten gerendert werden sollen. Dabei kann es sich um ein Standardformat für die Zwischenablage, ein proprietäres Format oder ein OLE-Format handelt. Weitere Informationen zu OLE-Formaten finden Sie unter [Verbunddokumente](compound-documents.md).<br/>                                          |
| **Ptd**<br/>      | Eine [**DVTARGETDEVICE-Struktur,**](/windows/win32/api/objidl/ns-objidl-dvtargetdevice) die genügend Informationen über ein Windows-Zielgerät enthält, z. B. einen Bildschirm oder Drucker, sodass ein Handle für seinen Gerätekontext (hDC) mithilfe der [**CreateDC-Funktion**](/windows/desktop/api/wingdi/nf-wingdi-createdca) erstellt werden kann. <br/> |
| **Dwaspect**<br/> | Der Aspekt oder die Ansicht der zu rendernden Daten; kann der vollständige Inhalt, eine Miniaturansicht, ein Symbol oder zum Drucken formatiert sein.<br/>                                                                                                                                  |
| **Lindex**<br/>   | Der Teil des Aspekts, der von Interesse ist; für den aktuellen muss der Wert -1 sein, was angibt, dass die gesamte Ansicht von Interesse ist.<br/>                                                                                                                                |
| **Tymed**<br/>    | Das Speichermedium der Daten. Dabei kann es sich um globalen Arbeitsspeicher, eine Datenträgerdatei oder eine Instanz einer der COM-Schnittstellen für strukturierten Speicher (Structured Storage) verfügen.<br/>                                                                                                                                   |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Datenformate und Übertragungsmedien](data-formats-and-transfer-media.md)
</dt> </dl>

 

