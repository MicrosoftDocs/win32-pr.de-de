---
description: Um dem Untermenü Programme ein Element hinzuzufügen, führen Sie die folgenden Schritte aus.
ms.assetid: F8793C33-2281-4E4A-9659-4189E1C8279A
title: Vorgehensweise beim Hinzufügen von Verknüpfungen zum Startmenü
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77ee942e07c48ed7addf07160412008bfb5b9322
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131629"
---
# <a name="how-to-add-shortcuts-to-the-start-menu"></a>Vorgehensweise beim Hinzufügen von Verknüpfungen zum Startmenü

Um dem Untermenü **Programme** ein Element hinzuzufügen, führen Sie die folgenden Schritte aus.

## <a name="instructions"></a>Instructions

### <a name="step-1"></a>Schritt 1:

Erstellen Sie eine [Shellverknüpfung](./links.md) mithilfe der [**IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) -Schnittstelle.

### <a name="step-2"></a>Schritt 2:

Rufen Sie den Speicherort des Ordners "Programme" mithilfe der Funktion " [**shgetknownfolderpath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath) " ab, und übergeben Sie [**folderid- \_ Programme**](knownfolderid.md).

### <a name="step-3"></a>Schritt 3:

Fügen Sie den shelllink zum Ordner Programme hinzu. Sie können auch einen Ordner im Ordner Programme erstellen und diesem Ordner den Link hinzufügen.

 

 
