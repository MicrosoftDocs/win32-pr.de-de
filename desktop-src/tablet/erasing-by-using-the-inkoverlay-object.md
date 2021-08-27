---
description: Das InkOverlay-Objekt kann an ein Fenstersteuerelement angefügt werden und wird verwendet, um grundlegende Ink-Funktionen zu aktivieren.
ms.assetid: c15d80dc-0cbf-48a2-9f5d-d94d521b1a8c
title: Löschen mithilfe des InkOverlay-Objekts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb6d95e7939bc53c534d3bfc9a542e40b95fbce05234000e24b107f0f2625eae
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120110940"
---
# <a name="erasing-by-using-the-inkoverlay-object"></a>Löschen mithilfe des InkOverlay-Objekts

Das [**InkOverlay-Objekt**](inkoverlay-class.md) kann an ein Fenstersteuerelement angefügt werden und wird verwendet, um grundlegende Ink-Funktionen zu aktivieren. Sie können das **InkOverlay-Objekt** verwenden, um Denkdaten zu löschen, indem Sie die [**EditingMode-Eigenschaft**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_editingmode) auf **Löschen** festlegen. Anschließend können Sie die [**EraserMode-Eigenschaft**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_erasermode) entweder auf die **Stroke-** oder **Point-Member** von [**InkOverlayEraserMode**](/windows/desktop/api/msinkaut/ne-msinkaut-inkoverlayerasermode)festlegen. Durch Festlegen der **EraserMode-Eigenschaft** auf **Strich** werden ganze Striche gelöscht. Wenn Sie die **EraserMode-Eigenschaft** auf **Point** festlegen, wird die Vom Cursor übergebene Ink gelöscht.

 

 



