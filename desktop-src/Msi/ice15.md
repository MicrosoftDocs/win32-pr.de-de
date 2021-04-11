---
description: ICE15 überprüft, ob Inhaltstyp-und Erweiterungs Verweise in den MIME-und Erweiterungs Tabellen einander einander entsprechen. Die MIME-Tabelle muss auf einen Inhaltstyp auf eine Erweiterung verweisen, auf die die Erweiterungs Tabelle auf denselben Inhaltstyp zurückverweist.
ms.assetid: 8a38c8d2-324d-4de9-932b-d188ff5ccbaf
title: ICE15
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb39b3c617db41e9e58a226f1eeb92c3d733ebad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042539"
---
# <a name="ice15"></a>ICE15

ICE15 überprüft, ob Inhaltstyp-und Erweiterungs Verweise in den [MIME](mime-table.md) -und [Erweiterungs](extension-table.md) Tabellen einander einander entsprechen. Die MIME-Tabelle muss auf einen Inhaltstyp auf eine Erweiterung verweisen, auf die die Erweiterungs Tabelle auf denselben Inhaltstyp zurückverweist.

Mehrere Erweiterungen können auf denselben MIME-Typ verweisen, solange der MIME-Typ auf eine der Erweiterungen zurückverweist. Mehrere MIME-Typen können auf dieselbe Erweiterung verweisen, solange die Erweiterung auf einen der MIME-Typen zurückverweist.

Beachten Sie, dass die MIME- \_ Spalte in der Erweiterungs Tabelle nicht auf NULL festgelegt werden kann, wenn ein MIME auf eine Erweiterung verweist.

## <a name="result"></a>Ergebnis

ICE15 gibt einen Fehler aus, wenn der Inhaltstyp und die Erweiterungs Verweise nicht gegenseitig sind.

## <a name="example"></a>Beispiel

ICE15 gibt zwei Fehlermeldungen für das folgende Beispiel aus:

-   Der Inhaltstyp "Test/x-Flas" in der MIME-Tabelle verweist auf die Erweiterung "TST", aber die Erweiterung "TST" in der Erweiterungs Tabelle verweist auf "Flas/x- Dies ist kein gegenseitiger Wert.
-   Die Inhaltstyp-Klappen/x-Klappen verweisen auf die Erweiterungs-FLP, aber diese Erweiterung weist einen NULL-Eintrag in der MIME- \_ Spalte der Erweiterungs Tabelle auf.

[MIME-Tabelle](mime-table.md) (partiell)



| ContentType   | Durchwahl\_ |
|---------------|-------------|
| Test/x-Test   | TST         |
| Klappen/x-Klappen | FLP         |



 

[Erweiterungs Tabelle](extension-table.md) (partiell)



| Durchwahl | Medi\_        |
|-----------|---------------|
| TST       | Klappen/x-Klappen |
| FLP       | Null          |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ice-Referenz](ice-reference.md)
</dt> </dl>

 

 



