---
description: Wenn dieses Bit für ein Bearbeitungssteuerelement festgelegt ist, erstellt das Installationsprogramm ein Bearbeitungssteuerelement mit mehreren Zeilen mit einer vertikalen Bildlaufleiste.
ms.assetid: cbdbe088-9cf1-4af8-a5f7-072faee7f34e
title: MultiLine-Steuerelementattribut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 474bf8a9b765f402924a554c9da064a8c60a01f6af910a3fd24c81d377978a93
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118943431"
---
# <a name="multiline-control-attribute"></a>MultiLine-Steuerelementattribut

Wenn dieses Bit für ein [Edit-Steuerelement](edit-control.md)festgelegt ist, erstellt das Installationsprogramm ein Bearbeitungssteuerelement mit mehreren Zeilen mit einer vertikalen Bildlaufleiste.

Wenn dieses Bit nicht festgelegt ist, wird ein normales Bearbeitungssteuerelement angezeigt.

## <a name="valid-controls"></a>Gültige Steuerelemente

[Bearbeiten Sie das Steuerelement](edit-control.md).



| Decimal | Hexadezimal | Konstante                            |
|---------|-------------|-------------------------------------|
| 65536   | 0x00010000  | **msidbControlAttributesMultiline** |



 

## <a name="remarks"></a>Hinweise

Um dieses Attribut für ein Steuerelement festzulegen, schließen Sie das MultiLine-Bit in die Attributes -Spalte des Datensatzes des Steuerelements in die [Control-Tabelle ein.](control-table.md)

Weitere Informationen finden Sie unter [Steuerelementattribute](control-attributes.md) und [Steuerelemente.](controls.md)

 

 



