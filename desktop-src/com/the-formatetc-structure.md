---
title: Die FORMATETC-Struktur
description: Die FORMATETC-Struktur ist ein generalisiertes Zwischenablage Format, das für ein Zielgerät, einen Aspekt oder eine Sicht der Daten und ein Speichermedium erweitert wurde.
ms.assetid: 46d8988a-4b97-4c86-8b1b-db87044a7e01
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ece0079cf2c0f07b7356f07ee2c53b1279b7ce7
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730544"
---
# <a name="the-formatetc-structure"></a>Die FORMATETC-Struktur

Die FORMATETC-Struktur ist ein generalisiertes Zwischenablage Format, das für ein Zielgerät, einen *Aspekt* oder eine Sicht der Daten und ein Speichermedium erweitert wurde. Ein Datenconsumer, z. b. eine OLE-Containeranwendung, übergibt die [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) -Struktur als Argument in Aufrufen von [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) , um den Typ der gewünschten Daten aus einer Datenquelle anzugeben, z. b. ein Verbund Dokument Objekt. Die Quelle verwendet die **FORMATETC** -Struktur, um die Formate zu beschreiben, die Sie bereitstellen kann.

[**Formatusw**](/windows/win32/api/objidl/ns-objidl-formatetc) . kann praktisch alle Daten beschreiben, einschließlich anderer Objekte, wie z. b. Moniker. Ein Container kann eines seiner eingebetteten Objekte bitten, seine Datenformate durch Aufrufen von [**IDataObject:: EnumFormatEtc**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-enumformatetc)aufzulisten, das ein Enumeratorobjekt zurückgibt, das die [**IEnumFORMATETC**](/windows/desktop/api/ObjIdl/nn-objidl-ienumformatetc) -Schnittstelle implementiert. Anstatt zu antworten, dass Sie nur über "Text und eine Bitmap" verfügen. das-Objekt kann eine detaillierte Beschreibung der Daten bereitstellen, einschließlich des Geräts (normalerweise Bildschirm oder Drucker), für das es gerendert wird, des Aspekts, der dem Benutzer angezeigt wird (vollständiger Inhalt, Miniaturansicht, Symbol oder formatiert für das Drucken), und dem Speichermedium mit den Daten (globaler Arbeitsspeicher, Datenträger Datei, Speicher Objekt). , oder Stream). Diese Möglichkeit, Daten eng zu beschreiben, führt in der Zeit zu einer höheren Qualität von Drucker und Bildschirmausgabe sowie zu einer höheren Effizienz beim Durchsuchen von Daten, bei der eine Miniaturansicht viel schneller abgerufen und angezeigt wird als ein vollständig ausführliches Rendering.

In der folgenden Tabelle sind die Felder der [**formatusw**](/windows/win32/api/objidl/ns-objidl-formatetc) .-Datenstruktur und die von Ihnen angegebenen Informationen aufgeführt.



| Feld                   | Bedeutung                                                                                                                                                                                                                                                                    |
|-------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **cfFormat**<br/> | Das Format, in dem die Daten gerendert werden sollen. Hierbei kann es sich um ein Standardmäßiges Zwischenablage Format, ein proprietäres Format oder ein OLE-Format handeln. Weitere Informationen zu OLE-Formaten finden Sie unter zusammen [gesetzte Dokumente](compound-documents.md).<br/>                                          |
| **ptd**<br/>      | Eine [**DVTARGETDEVICE**](/windows/win32/api/objidl/ns-objidl-dvtargetdevice) -Struktur, die genügend Informationen über ein Windows-Zielgerät enthält, z. b. einen Bildschirm oder Drucker, damit ein Handle für den Gerätekontext (HDC) mithilfe [**der Funktion "**](/windows/desktop/api/wingdi/nf-wingdi-createdca) -Funktion" erstellt werden kann. <br/> |
| **dwAspect**<br/> | Der Aspekt oder die Ansicht der Daten, die gerendert werden sollen. kann der vollständige Inhalt, eine Miniaturansicht oder ein Symbol sein oder zum Drucken formatiert werden.<br/>                                                                                                                                  |
| **Lindex**<br/>   | Der Teil des Aspekts, der von Interesse ist. für den aktuellen muss der Wert-1 lauten, was darauf hinweist, dass die gesamte Ansicht von Interesse ist.<br/>                                                                                                                                |
| **TYMED**<br/>    | Das Speichermedium der Daten, bei dem es sich um globalen Speicher, eine Datenträger Datei oder eine Instanz von einer der strukturierten Speicher Schnittstellen von com handeln kann.<br/>                                                                                                                                   |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Datenformate und Übertragungsmedien](data-formats-and-transfer-media.md)
</dt> </dl>

 

