---
description: Das DivisionResult-Objekt stellt eine Momentaufnahme der Layoutanalyse der im Divider-Objekt enthaltenen Striche dar. Sie enthält die Strichklassifizierungs- und Gruppierungsinformationen aus der Layoutanalyse.
ms.assetid: 2bcf5223-7bf4-420c-8f04-a972f04f262d
title: Arbeiten mit dem DivisionResult-Objekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b1bb001ecc57c0925253b01b129e0c6fcf0c0243c5a77f0eb697e2cc5c618d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118715070"
---
# <a name="working-with-the-divisionresult-object"></a>Arbeiten mit dem DivisionResult-Objekt

Das **DivisionResult-Objekt** stellt eine Momentaufnahme der Layoutanalyse der im Divider-Objekt enthaltenen **Striche** dar. Sie enthält die Strichklassifizierungs- und Gruppierungsinformationen aus der Layoutanalyse.

Sie können Informationen aus dem **DivisionResult-Objekt** nach strukturellem Elementtyp, z. B. Zeichnen oder Handschriften, erhalten. Das **DivisionResult-Objekt** kann beibehalten werden, nachdem das **Divider-Objekt** zerstört wurde. In Automation wird dieses Objekt als [**IInkDivisionResult Interface-Objekt**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) bezeichnet.

Die [**Strokes-Eigenschaft**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes) des **DivisionResult-Objekts** enthält eine Kopie der **Strokes-Auflistung** im **Divider-Objekt** zum Zeitpunkt der **DivisionResult-Objekt** erstellt wurde.

Die [**InkDivisionType-Enumeration**](/windows/win32/api/msinkaut15/ne-msinkaut15-inkdivisiontype) definiert die strukturellen Elementtypen, die von der Layoutanalyse erkannt werden.

Die [**ResultByType-Methode**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-resultbytype) des **DivisionResult-Objekts** gibt eine **DivisionUnits-Auflistung** zurück, die alle strukturellen Elemente eines bestimmten Typs enthält. Ein einzelnes strukturelles Element wird durch ein **DivisionUnit-Objekt** dargestellt. Jedes Mal, wenn Sie die **ResultByType-Methode** aufrufen, erstellt das **DivisionResult-Objekt** eine **DivisionUnits-Auflistung.** Weitere Informationen zum **DivisionUnit-Objekt** finden Sie unter [Arbeiten mit dem DivisionUnit-Objekt](working-with-the-divisionunit-object.md).

 

 
