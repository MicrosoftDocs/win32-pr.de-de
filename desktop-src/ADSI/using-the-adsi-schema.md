---
title: Verwenden des ADSI-Schemas
description: Ein Schema definiert das Universum von Objekten, die in einem Verzeichnis gespeichert sind.
ms.assetid: 140a5dd0-6f50-4f84-8708-45c0f1c6bdc4
ms.tgt_platform: multiple
keywords:
- Verwenden des ADSI-Schemas
- ADSI ADSI, using, ADSI-Schema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 478104a24d850f79cc52473f3d9e546936c56650
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "103858475"
---
# <a name="using-the-adsi-schema"></a>Verwenden des ADSI-Schemas

Ein Schema definiert das Universum von Objekten, die in einem Verzeichnis gespeichert sind. In Active Directory gibt das Schema an, welche Attribute ein Verzeichnisdienst Objekt haben kann oder muss. Außerdem gibt Sie den Wertebereich und die Syntax der Attribute an und gibt an, ob Sie einzelne oder mehrere Werte unterstützen. Kurz gesagt, ist das Schema nach Klassendefinitionen, Attribut Definitionen und Attribut Syntax angeordnet. ADSI bietet drei Schnittstellen zum Lesen von Attribut-, Klassen-und Syntax Daten aus einem Schema: [**iadsclass**](/windows/desktop/api/Iads/nn-iads-iadsclass), [**iadsproperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty)und [**iadssyntax**](/windows/desktop/api/Iads/nn-iads-iadssyntax).

Active Directory verwendet einen Satz von Schema Objekten, um eine dynamisch erweiterbare Schema Verwaltung bereitzustellen. Weitere Informationen zu einem unbekannten Objekt finden Sie in den zugehörigen Schema Objekten. Um eine neue Klassendefinition zu erstellen oder eine vorhandene Klassendefinition zu erweitern, können Sie die entsprechenden Schema Objekte erstellen oder erweitern. Schema Objekte werden im Schema Container eines bestimmten Verzeichnisses organisiert. Verwenden Sie zum Zugreifen auf eine Objekt Schema Klasse die [**IADs. Schema**](iads-property-methods.md) -Eigenschaft des-Objekts, um die ADsPath-Zeichenfolge abzurufen, und verwenden Sie diese Zeichenfolge, um eine Bindung an eine [**iadsclass**](/windows/desktop/api/Iads/nn-iads-iadsclass) -Schnittstelle in der Objekt Schema Klasse herzustellen.

Um Attribut Definitionen, d. h. den Wertebereich, die Syntax usw., zu bestimmen, überprüfen Sie die Schema Attribut Objekte für jede Eigenschaft, die vom Verzeichnisdienst Objekt unterstützt wird. Weitere Informationen zum Zugreifen auf die Schema Attribut Objekte finden Sie unter [**iadsproperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty).

ADSI abstrahiert die Syntax Daten bei Bedarf und ermöglicht die Verwendung von [**iadssyntax**](/windows/desktop/api/Iads/nn-iads-iadssyntax) , um die Syntax zu identifizieren, die für die Darstellung von Objektdaten erforderlich ist.

Weitere Informationen zum Active Directory Schema finden Sie unter [Active Directory Schema](/windows/desktop/AD/active-directory-schema). Codebeispiele, die zum Lesen des Schema Containers verwendet werden, finden Sie unter [Lesen des Schemas](reading-the-schema.md).

 

 