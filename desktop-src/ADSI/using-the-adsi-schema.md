---
title: Verwenden des ADSI-Schemas
description: Ein Schema definiert das Universe der in einem Verzeichnis gespeicherten Objekte.
ms.assetid: 140a5dd0-6f50-4f84-8708-45c0f1c6bdc4
ms.tgt_platform: multiple
keywords:
- Verwenden des ADSI-Schemas
- ADSI ADSI , using, ADSI-Schema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8aaf49f75d026f52c644d06a6fe36e4555841e3e7bf587ffeb1e0277d1e5ac99
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119648820"
---
# <a name="using-the-adsi-schema"></a>Verwenden des ADSI-Schemas

Ein Schema definiert das Universe der in einem Verzeichnis gespeicherten Objekte. In Active Directory gibt das Schema an, welche Attribute ein Verzeichnisdienstobjekt aufweisen kann oder muss. Sie gibt auch den Wertbereich und die Syntax der Attribute an und gibt an, ob sie einzelne oder mehrere Werte unterstützen. Kurz gesagt: Das Schema ist nach Klassendefinitionen, Attributdefinitionen und Attributsyntax organisiert. ADSI stellt drei Schnittstellen zum Lesen von Attribut-, Klassen- und Syntaxdaten aus einem Schema bereit: [**IADsClass,**](/windows/desktop/api/Iads/nn-iads-iadsclass) [**IADsProperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty)und [**IADsSyntax**](/windows/desktop/api/Iads/nn-iads-iadssyntax).

Active Directory verwendet eine Reihe von Schemaobjekten, um eine dynamisch erweiterbare Schemaverwaltung bereitzustellen. Weitere Informationen zu einem unbekannten Objekt suchen Sie nach den zugehörigen Schemaobjekten. Um eine neue Klassendefinition zu erstellen oder eine vorhandene Klassendefinition zu erweitern, können Sie die entsprechenden Schemaobjekte erstellen oder erweitern. Schemaobjekte sind im Schemacontainer eines bestimmten Verzeichnisses organisiert. Um auf eine Objektschemaklasse zuzugreifen, verwenden Sie die [**IADs.Schema-Eigenschaft**](iads-property-methods.md) des -Objekts, um die ADsPath-Zeichenfolge abzurufen, und verwenden Sie diese Zeichenfolge, um eine Bindung an eine [**IADsClass-Schnittstelle**](/windows/desktop/api/Iads/nn-iads-iadsclass) für die Objektschemaklasse zu erstellen.

Um Attributdefinitionen zu bestimmen, d. h. den Wertebereich, die Syntax usw., überprüfen Sie die Schemaattributobjekte für jede Eigenschaft, die vom Verzeichnisdienstobjekt unterstützt wird. Weitere Informationen zum Zugreifen auf die Schemaattributobjekte finden Sie unter [**IADsProperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty).

ADSI abstrahiert die Syntaxdaten nach Bedarf und ermöglicht ihnen die Verwendung von [**IADsSyntax,**](/windows/desktop/api/Iads/nn-iads-iadssyntax) um die Syntax zu identifizieren, die zur Darstellung von Objektdaten erforderlich ist.

Weitere Informationen zum Active Directory-Schema finden Sie unter [Active Directory-Schema.](/windows/desktop/AD/active-directory-schema) Codebeispiele zum Lesen des Schemacontainers finden Sie unter [Lesen des Schemas.](reading-the-schema.md)

 

 